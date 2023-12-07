# Automated Smart Contract Lottery with Chainlink Integration

## Overview
Welcome to the automated smart contract lottery system! This project harnesses the power of Chainlink to create a decentralized and automated lottery experience. Users can enter the lottery by contributing funds to the smart contract, and the Chainlink Coordinator checks periodically to determine if the conditions for a draw have been met.

### Key Features
- **Automated Draws:** The lottery draw is automated, with no manual intervention required once set up.
- **Chainlink Integration:** Utilizes Chainlink for reliable, decentralized coordination and random number generation.
- **Transparent and Fair:** The winner selection process is transparent, relying on Chainlink's random number generation for fairness.
- **Direct Payouts:** Winners receive their funds automatically, directly from the contract.

### How It Works
1. **Entering the Lottery:** Participants enter the lottery by sending funds to the contract.
2. **Draw Conditions Check:** The Chainlink Coordinator periodically checks if the conditions for a lottery draw are met, based on a predefined time interval.
3. **Random Number Request:** Once the conditions are fulfilled, the Coordinator requests a random number from the Chainlink node.
4. **Winner Calculation and Payout:** The lottery winner is calculated based on the received random number, and the prize money is automatically sent to the winner's address.

### Requirements
For the lottery to function seamlessly, it is essential that:
- The Chainlink Coordinator always has sufficient LINK to cover operational fees and ensure uninterrupted service.

### Quickstart
To get started with this project, follow these steps:

1. Clone the repository:
```shell
$ git clone https://github.com/Cyfrin/foundry-smart-contract-lottery-f23
```


3. Navigate to the project directory:
```shell
$ cd foundry-smart-contract-lottery-f23
```


4. Build the project using Foundry:
```shell
$ forge build
```
   
## Deployment to Testnet or Mainnet

### Environment Variable Setup
To prepare for deployment:

- **Set up your Environment Variables:** 
  - `SEPOLIA_RPC_URL`: This is the URL of the Sepolia testnet node you are using. You can set this up for free with Alchemy.
  - `PRIVATE_KEY`: Use the private key of your development account (e.g., from MetaMask). Remember, for development purposes, use a key without real funds. [Learn how to export it here](Your-Link-To-Export-Instructions).
  
  Add these variables to a `.env` file as shown in the provided `.env.example`.

- **Optional:** Include your `ETHERSCAN_API_KEY` for contract verification on Etherscan.

### Acquiring Testnet ETH
- Visit [faucets.chain.link](https://faucets.chain.link) to receive testnet ETH, which should then appear in your MetaMask wallet.

### Deploying the Contract
- Run the following command to deploy:
  ```shell
  make deploy ARGS="--network sepolia"


## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
