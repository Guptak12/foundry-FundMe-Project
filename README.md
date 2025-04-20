# FundMe Smart Contract Project

A decentralized crowdfunding platform built with **Foundry** and **Solidity**. This project is inspired by the idea of allowing users to contribute ETH to a smart contract, and the owner can withdraw the funds when needed.

## 🛠️ Tech Stack

- **Solidity** – Smart contract language
- **Foundry** – Fast, portable and modular toolkit for Ethereum application development
- **Chainlink** – For fetching real-time ETH/USD price data via oracles
- **Remappings** – For managing imports
- **Forge** – CLI for building and testing smart contracts

## 📂 Project Structure

```
fundme-foundry/
│
├── src/
│   ├── FundMe.sol                # Main FundMe contract
│   └── PriceConverter.sol        # Library to convert ETH to USD
│
├── script/
│   └── DeployFundMe.s.sol       # Script to deploy FundMe contract
│
├── test/
│   └── FundMeTest.t.sol         # Unit tests for the contract
│
├── lib/                         # Dependencies (e.g., Chainlink contracts)
├── .env                         # Environment variables
├── foundry.toml                 # Foundry configuration
└── README.md                    # Project documentation
```

## 🚀 Getting Started

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation) installed

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

- Create a `.env` file with the following:

```env
PRIVATE_KEY=your_private_key
ETHERSCAN_API_KEY=your_etherscan_api_key
RPC_URL=your_rpc_url
```

### Install Dependencies

```bash
forge install
```

### Compile Contracts

```bash
forge build
```

### Run Tests

```bash
forge test
```

### Deploy the Contract

```bash
forge script script/DeployFundMe.s.sol:DeployFundMe --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast --verify
```

> ⚠️ Make sure your `.env` file is correctly configured and you have sufficient testnet/mainnet ETH.

## 💡 Features

- Users can fund the contract with ETH
- Owner can withdraw funds
- Integration with Chainlink price feeds for ETH/USD conversion
- Unit-tested and modular code structure

## 🧪 Testing

This project uses `forge test` for running tests, with custom assertions for gas estimation and correctness of fund management logic.

## 📝 License

This project is licensed under the MIT License.

## 🤝 Acknowledgements

- [Patrick Collins](https://github.com/PatrickAlphaC) – for the original concept
- [Foundry Book](https://book.getfoundry.sh/) – Foundry documentation
- [Chainlink](https://docs.chain.link/) – Oracle provider

---

Made with ❤️ using Foundry.
