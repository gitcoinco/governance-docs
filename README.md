# Gitcoin Governance Contracts   

For Gitcoin governance's initial milestone one release we establish the foundational components of a decentralized governance system based primarily on the standard set by [Compound Finance](https://github.com/compound-finance/compound-protocol/tree/v2.8.1). 

The retroactive GTC token distribution is front lined by the [Quadratic Lands](https://gitcoin.co/quadraticlands) experience where users claim their GTC tokens based on past activities and contributions on Gitcoin.co. You can find more information on the [GTC Airdrop here](https://gitcoin.co/blog/introducing-gtc-gitcoins-governance-token/). 

## Contract Deployment & Admin Guides:

You can find the [Gitcoin Governance repository here](https://github.com/gitcoinco/governance). 

Here you can find a guide on [how to deploy the Gitcoin governance contracts with Brownie](DEPLOYMENT-GUIDE.md).

# Primary Contracts 

1) [GTC.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GTC.sol) - [Mainnet contract @ 0xDe30da39c46104798bB5aA3fe8B9e0e1F348163F](https://etherscan.io/address/0xDe30da39c46104798bB5aA3fe8B9e0e1F348163F) - ERC20 contract for the GTC Token forked from [Uni.sol](https://github.com/Uniswap/governance/blob/master/contracts/Uni.sol). 
2) [TokenDistributor.sol](https://github.com/gitcoinco/governance/blob/main/contracts/TokenDistributor.sol) - [Mainnet contract @ 0xDE3e5a990bCE7fC60a6f017e7c4a95fc4939299E ](https://etherscan.io/address/0xDE3e5a990bCE7fC60a6f017e7c4a95fc4939299E) - Retroactive distribution contract used to distribute initial batch of GTC tokens to the community.   
3) [GovernorAlpha.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GovernorAlpha.sol) - [Mainnet contract @ 0xDbD27635A534A3d3169Ef0498beB56Fb9c937489](https://etherscan.io/address/0xDbD27635A534A3d3169Ef0498beB56Fb9c937489)The governance module for the protocol. 
4) [TimeLock.sol](https://github.com/gitcoinco/governance/blob/main/contracts/Timelock.sol) - [Mainnet contract @ 0x57a8865cfB1eCEf7253c27da6B4BC3dAEE5Be518](https://etherscan.io/address/0x57a8865cfB1eCEf7253c27da6B4BC3dAEE5Be518) - The Timelock contract can modify system parameters, logic, and contracts in a 'time-delayed, opt-out' upgrade pattern. 
5) [TreasuryVester.sol](https://github.com/gitcoinco/governance/blob/main/contracts/TreasuryVester.sol) - [Mainnet contract @ 0x44Aa9c5a034C1499Ec27906E2D427b704b567ffe](https://etherscan.io/address/0x44Aa9c5a034C1499Ec27906E2D427b704b567ffe) - Contract used to establish vested treasury for tokens.  


## 1 - [GTC Token](./GTC-TOKEN.md) 

The [GTC.sol](https://github.com/gitcoinco/governance/blob/main/contracts/GTA.sol) contract is an ERC20 contract forked from Uniswap/Compound. Beyond the standard ERC20 functionally it also has a token delegation feature that allows token holders to allocate voting shares to other addresses or delegates. More detailed info on the contract can be found [here](./GTC-TOKEN.md). 

## 2 - [GTC Token Distributor](./TOKEN-DISTRIBUTOR.md) 
The primary purpose of our [token distribution contract](https://github.com/gitcoinco/governance/blob/main/contracts/TokenDistributor.sol) is to facilitate retroactive distribution of GTC tokens to users of the Gitcoin protocol. 

## 3 - GovernorAlpha
[Gitcoin GovernorAlpha](https://github.com/gitcoinco/governance/blob/main/contracts/GovernorAlpha.sol)  

## 4 - TimeLock
[Gitcoin TimeLock](https://github.com/gitcoinco/governance/blob/main/contracts/Timelock.sol) 

## 5 - TreasuryVester
[Gitcoin TerasuryVester](https://github.com/gitcoinco/governance/blob/main/contracts/TreasuryVester.sol) 

---





