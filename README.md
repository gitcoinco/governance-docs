# Gitcoin Governance Contracts   

For Gitcoin governance's initial milestone one release we establish the foundational components of a decentralized governance system based primarily on the standard set by [Compound Finance](https://github.com/compound-finance/compound-protocol/tree/v2.8.1). 

The retroactive GTC token distribution is front lined by the [Quadratic Lands](https://gitcoin.co/quadraticlands) experience where users claim their GTC tokens based on past activities and contributions on Gitcoin.co. You can find more information on the [GTC Airdrop here](./<link-to-article>). 

## Contract Deployment & Admin Guides: 

Here you can find a guide on [how to deploy the Gitcoin governance contracts with Brownie](DEPLOYMENT-GUIDE.md).

# Primary Contracts 

1) [GTC.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GTA.sol) - ERC20 contract for the GTC Token forked from [Uni.sol](https://github.com/Uniswap/governance/blob/master/contracts/Uni.sol)
2) [TokenDistributor.sol](https://github.com/gitcoinco/governance/blob/main/contracts/TokenDistributor.sol) - Contract responsible for distributing initial batch of GTC tokens to the community  
3) [GovernorAlpha.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GovernorAlpha.sol) - The governance module for the protocol
4) [TimeLock.sol](https://github.com/gitcoinco/governance/blob/main/contracts/Timelock.sol) -  The Timelock contract can modify system parameters, logic, and contracts in a 'time-delayed, opt-out' upgrade pattern 
5) [TreasuryVester.sol](https://github.com/gitcoinco/governance/blob/main/contracts/TreasuryVester.sol) - Contract that can be used to establish vested treasury tokens 


## 1 - [GTC Token](./GTC-TOKEN.md) 

The [GTC.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GTA.sol) contract is an ERC20 contract forked from Uniswap/Compound. Beyond the standard ERC20 functionally it also has a token delegation feature that allows token holders to allocate voting shares to other addresses or delegates. More detailed info on the contract can be found [here](./GTC-TOKEN.md). 

## 2 - [GTC Token Distributor](./TOKEN-DISTRIBUTOR.md) 
The primary purpose of our [token distribution contract](https://github.com/gitcoinco/governance/blob/main/contracts/TokenDistributor.sol) is to facilitate retroactive distribution of GTC tokens to users of the Gitcoin protocol. 

## 3 - [GovernorAlpha](./ZACTODO.md)
[Gitcoin GovernorAlpha](https://github.com/gitcoinco/governance/blob/main/contracts/GovernorAlpha.sol) This contract... 

## 4 - [TimeLock](./ZACTODO.md)
[Gitcoin TimeLock](https://github.com/gitcoinco/governance/blob/main/contracts/Timelock.sol) This contract...

## 5 - [TreasuryVester](./ZACTODO.md)
[Gitcoin TerasuryVester](https://github.com/gitcoinco/governance/blob/main/contracts/TreasuryVester.sol) This contract... 

---





