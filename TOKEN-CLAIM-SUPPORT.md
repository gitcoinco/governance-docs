## Quadratic Lands & Gitcoin GTC Token Distribution Support Guide

- Chat support is available on the [Gitcoin Discord](https://discord.gg/gitcoin) (channel #issues-support) 

- Non-technical questions on the [Quadratic Lands FAQ](https://gitcoin.co/quadraticlands/faq)

- [Gitcoin Support](https://support.gitcoin.co) 

- Bug reports can be filed directly on the [Gitcoin Website repository](https://github.com/gitcoinco/web/issues)

<details>
  <summary>How do I know if i'm eligible for the airdrop?</summary>
  
  Tokens are being airdropped to people who have been active on Gitcoin.co through bounties, hackathons, and grants using a custom distribution algorithm. At the time of token launch (5/25/2021), there are three different ways to see/know if you are eligible for the air drop.  
  1. The [Gitcoin.co](https://gitcoin.co) landing page will show that you have a claim available in the banner 
  2. You will see a message message on the [Quadratic Lands Mission](http://gitcoin.co/quadraticlands/mission) page: 
  > Complete all 3 missions to receive your tokens.
  3. The [Quadratic Lands](https://gitcoin.co/quadraticlands) landing page will show a claim total in the navigation bar  
</details>

### Quadratic Lands Token Distribution web3 support

1) Token Claim - After completing the first two missions (1-proof of knowledge and 2- proof of use) eligible users will arrive at the third mission, proof of receive.

    When you click `claim` in the receive mission, you will be prompted to broadcast a transaction to the Gitcoin Token Distribution contract. 

    If you are having issues with your token claim please here are a few things to check/confirm:

        1) your wallet is connected to the Ethereum Mainnet 
        2) you don't have any old/stale transactions pending transactions on your account
        3) you have enough Ethereum in your account to cover the gas fees


2) Delegate Voting Power - After you've successfully claimed your airdrop (or even if a friend sent you tokens and/or your acquired them elsewhere) you can delegate your voting power using the [Stewards interface](https://gitcoin.co/quadraticlands/stewards) in the Quadratic Lands. This is a relatively straight forward web3 interaction in which you will call the `delegate` function on the GTC token contract. If you're having issues delegating through the Quadratic Lands UI you can also try delegating voting power using our [Tally interface](need production link) or even with [Etherscan](https://etherscan.io/address/0xde30da39c46104798bb5aa3fe8b9e0e1f348163f#writeContract). 

3) Signed Message Vote - If you choose to not delegate your voting power to a steward (power to the people FTW!) you will be asked to help chart the future of Gitcoin by proving feedback on the development road map.  You will be prompted to sign a message with your active Ethereum account to solidify your preference. This signed message does not require any gas fees and is not  being broadcast on-chain for now. While it's possible that Gitcoin could use these signed messages as a foundation for a future airdrop or something, for now we're just collecting these votes up to help us better understand what direction the Gitcoin community would like to see Gitcoin go. 
