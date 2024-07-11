# Building-with-Polygon-Bridge

## Overview

This project demonstrates the creation, deployment, and transfer of an NFT collection using Ethereum and Polygon networks. It utilizes DALLE 2 or Midjourney for generating images, IPFS via pinata.cloud for storage, and deploys ERC721 or ERC1155 contracts on the sepolia Ethereum Testnet.

## Steps to Setup and Deploy

### Step 1: Generate NFT Collection

1. Use DALLE 2 or Midjourney to generate a 5-item NFT collection.
2. Store each generated item on IPFS using pinata.cloud.

### Step 2: Deploy ERC721/ERC1155 Contract

1. Deploy an ERC721 or ERC1155 contract on the sepolia Ethereum Testnet.
2. Implement a `promptDescription` function on the contract to return the prompt used for generating the images.

### Step 3: Map Your NFT Collection

Map your NFT collection using the Polygon network token mapper. This step is optional but helps with visualization and interoperability.

### Step 4: Write Hardhat Scripts

#### Batch Minting Script

Write a Hardhat script to batch mint all NFTs. ERC721A standard is recommended for optimal performance.

#### Batch Transfer to Polygon amoy

Write a Hardhat script to batch transfer all NFTs from Ethereum to Polygon amoy using the FxPortal Bridge.

1. Approve the NFTs for transfer.
2. Deposit the NFTs to the FxPortal Bridge.

### Step 5: Testing

Test the functionality using the following steps:

1. Test `balanceOf` function on the Polygon amoy network to ensure NFTs were transferred successfully.

## Usage

### Prerequisites

- Node.js installed
- Hardhat configured with Ethereum and Polygon network settings
- sepolia Ethereum Testnet and Polygon amoy network accounts with testnet ETH/MATIC

### Installation

1. Clone the repository.
2. Install dependencies using `npm install`.

### Deployment

1. Configure your `.env` file with necessary API keys and network settings.
2. Deploy contracts using Hardhat: `npx hardhat run scripts/deploy.js --network sepolia`.

### Running Scripts

1. Run batch minting script: `npx hardhat run scripts/batchMint.js --network sepolia`.
2. Run batch transfer script: `npx hardhat run scripts/batchTransfer.js --network amoy`.

### Testing

1. Test balance on Polygon amoy: `npx hardhat run scripts/testBalance.js --network amoy`.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to DALLE 2 and Midjourney for image generation tools.
- IPFS and pinata.cloud for decentralized storage.
- Ethereum and Polygon for blockchain infrastructure.

---
