# 👷 Setting up HardHat with MetaMask

Hardhat is an Ethereum development environment for professionals. It facilitates performing frequent tasks, such as running tests, automatically checking code for mistakes or interacting with a smart contract.

MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain. &#x20;

Setting up your local development environment enables you to develop and test smart contracts locally without the need of any test ETH (that is quite hard to get nowadays) or wait for any transaction to be mined.

This tutorial helps you in:

* setting up HardHat
* connecting MetaMask to your newly setup HardHat network
* deploying smart contracts to HardHat locally from Cranq

Prerequisites:

* NodeJs installed ([latest LTS or newer](https://nodejs.org/en/download/))

Steps

1. Setting up HardHat is pretty easy just:
   1. create a new empty folder somewhere on your computer
   2. run the following command in this folder to create an empty project\
      `npm init -y`
   3. install hardhat locally by \
      `npm install --save-dev hardhat`
   4. create a `hardhat.config.js` file in this folder with the following content:\
      \
      `module.exports = {` \
      &#x20; `solidity: "0.8.17",` \
      &#x20; `networks: {` \
      &#x20;   `hardhat: {` \
      &#x20;     `mining: {` \
      &#x20;       `auto: false,` \
      &#x20;       `interval: 5000` \
      &#x20;     `}` \
      &#x20;   `}` \
      &#x20; `}` \
      `};`
   5. run the following command in this folder from a terminal to start your local hardhat network:\
      `npx hardhat node`\
      ``\
      ``On your terminal you'll see displayed the RPC url of the local HardHat network and 20 newly created accounts. Like on the below screenshot:\
      \
      <img src="../.gitbook/assets/image (1).png" alt="" data-size="original">\
      \
      You'll need these information in the later steps.
   6. follow on with setting up MetaMask as shown from point 11 of our tutorial about [Setting up Ganache with MetaMask](setting-up-ganache-with-metamask.md) \
      Parameters of the custom network will be slightly different:\
      ![](<../.gitbook/assets/image (10).png>)
      * RPC URL: [http://127.0.0.1:8545/](http://127.0.0.1:8545/)
      * Chain ID: 31337

