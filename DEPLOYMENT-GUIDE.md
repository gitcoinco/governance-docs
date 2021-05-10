# Guide to Deploying Contracts With Brownie 

## Brownie Install Setup

Brownie is a Python-based development and testing framework for smart contracts targeting the Ethereum Virtual Machine. Detailed instructions for installing Brownie can be found [here](https://eth-brownie.readthedocs.io/en/stable/install.html). 

One nice thing about Brownie is that you can install it using pipx and it will install Brownie into a virtual environment which makes it available directly from the command line. Once installed, you will never have to activate a virtual environment prior to using Brownie.

#### Setting up your brownie config file(s)

If you're just testing locally you probably don't need to get these setup, but if you're going to be deploying contracts to testnets or mainnet then it might make more sense to set these up.  

1) `brownie-config.yaml` - If saved in the root directory of a project it will be loaded whenever that project is active. If saved in your home path, it will always be loaded. More info on how to setup/configure [brownie-config.yaml here](https://eth-brownie.readthedocs.io/en/stable/config.html#config). 

2) `network-config.yaml` - While network configurations can also be put in brownie-config.yaml it's a good idea to put your network configs outside your repo directory as it will likely contain some private info. By default, Brownie will install a network-config file in `~/.brownie/network-config.yaml`

You can set things like Infura keys and test mnemonics in your local network-config.yaml so you don't have to manually set them with environment variables.

## Deploy Governance Contracts Locally 

### Single contract deployment 

Deploying a single contract with Brownie is easy. Read on or check out [their docs here](https://eth-brownie.readthedocs.io/en/stable/core-contracts.html#deploying-contracts):

1) open the Brownie console:

```bash 
brownie console
``` 
note: As of this writing the ganache-cli (used by brownie to launch local chain) doesn't seem to play well with the latest version of nodejs. If you're using nvm you can run: `nvm use node 12` and it will fire up without issue. 

Each contract in the `/contracts` folder is compiled when the console is loaded and made available by name to interact with directly on the command line. For example, if you want look at what the constructor parameters are for the GTC contract:

```python
>>>GTC.deploy
```
Brownie will show all the parameters for that function:
```python
<ContractConstructor 'GTC.constructor(address account, address minter_, uint256 mintingAllowedAfter_)'>
```
So we know we need to feed three params to the contract on deployment. To deploy the GTC contract all we have to do is:

```python
>>> import time 
>>> mint_after = time.time() + 120
>>> GTC.deploy(accounts[0], accounts[0], mint_after, {"from": accounts[0]})
```
results:
```python
Transaction sent: 0x6dbf45e791e076ebf781fc8a6770ed8894bca98a36348ada1bbce3505a30ee79
  Gas price: 0.0 gwei   Gas limit: 12000000   Nonce: 1
  GTC.constructor confirmed - Block: 2   Gas used: 2196530 (18.30%)
  GTC deployed at: 0xf22BaCbE9ba2F3c6Cb3416639195b108C444B99A

<GTC Contract '0xf22BaCbE9ba2F3c6Cb3416639195b108C444B99A'>
```

The `mintingAllowedAfter_` parameter just needs to be a unix time stamp after the contract is deployed. For this local testnet example, because the Brownie console is a python shell, we can just grab current time python style and add a small buffer so the deploy doesn't fail. 

The fourth parameter, `{"from": accounts[0]}` is a Brownie specific requirement that forces us to explicitly state which address we're deploying the contract from. You can learn more about how accounts work in Brownie here. 

### Deploying All Gitcoin Governance Contracts At Once With a Script
#### Getting your environmental variables setup 
Before you run the deploy all script, you will probably want to familiarize yourself with the envars. 

You can use this [script](https://github.com/gitcoinco/governance/blob/main/scripts/deploy-all.py) to easily deploy all contract and automatically run some of the base configurations like this:

```bash
brownie console 
```
This will launch a local Ethereum test/dev chain using `ganache-cli`. Next, from the within the brownie console run the deployment script: 

```python
>>> run('deploy-all')
```

## Running Test 
TODO

## Other Things
### Running MythX Scan
Running a MythX scan with Brownie is as simple as setting your MythX API key:

` export MYTHX_API_KEY='your-really-long-api-key-goes-here'`

The from your contracts directory you can simply run:

`brownie analyze` 

More info on configuration options and accessing scan results can be found in the [Brownie docs](https://eth-brownie.readthedocs.io/en/stable/tests-security-analysis.html#security-analysis-with-mythx). 

---


