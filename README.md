<div align="center">
  <h1>BitLogix</h1>
  <p>
    <strong>Blockchain-Powered Supply Chain Magic</strong>
  </p>

</div>

Welcome to the BitLogix Supply Chain Management DApp, a pioneering solution poised to redefine how enterprises manage their logistics. Built on the [BitTorrent-chain](https://testscan.bt.io), BitLogix empowers businesses with real-time transparency, secure transactions, and streamlined operations.

As businesses navigate the complex world of logistics, BitLogix emerges as a beacon of technological advancement. Our DApp is designed to streamline supply chain operations, reducing friction and enhancing trust between stakeholders. With our DApp, businesses can navigate the complexities of logistics with confidence, knowing that they have a trusted partner.


# Features

- **Effortless Registration**: Simplified onboarding for enterprises and recipients.
- **Transparent Tracking**: Track products in real-time with immutable blockchain records.
- **Automated Payments**: Smart contracts for instant, error-free payments upon receipt confirmation.
- **Token Rewards**: Token reward system allows users to claim tokens as a one-time reward, promoting active participation and collaboration within the supply chain ecosystem. 
- **Quality Control:** Enterprises can control product quality and ensure compliance.
- **NFT Rewards:** Enterprises can issue NFTs as rewards to the Person-in-Charge.
- **Robust Security**: Built with a decentralized architecture for data integrity.
 
# Architecture

## Components

* **Frontend:** The frontend of our Dapp offers an intuitive interface for users to manage their supply chains efficiently, with seamless integration of Metamask for secure transactions.
* **BitLogix Smart Contract:** The BitLogix core smart contract manages registration, product creation, payment automation, and token rewards.
* **BitLogixNFT Smart Contract:** A specialized smart contract that allows enterprises to mint and transfer NFTs as reward to recipient associated with products for maintaining quality of product leads to enhancing quality control.
* **Metamask:** Metamask, a popular Ethereum wallet extension, is seamlessly integrated to facilitate secure transactions, account management, and interactions with the Ethereum blockchain.
* **Backend:** BitLogix's backend infrastructure supports data management and decentralized file storage.
* **MongoDB:** A scalable and flexible NoSQL database that stores essential data related to user accounts, product details, and transaction history.
* **IPFS:** A distributed file system for storing and retrieving large files and IPFS URIs associated with NFTs. IPFS ensures data availability and reliability while reducing centralized data dependencies.

# Local installation

1. Clone the repository

First, you need to clone the repository

```
git clone https://github.com/suraj719/BitLogix
```

2. Install Dependencies

Install the project's dependencies using Yarn:

```
npm install
```

3. Start the Project

Once all the dependencies are installed, you can start the project:

```
npm run dev
```

The project should now be running on `http://localhost:3000`

# Usage

* Enterprises and recipients can easily register to access BitLogix.
* Enterprises create products, recipients confirm receipt for efficient tracking.
* Active participants earn tokens as one-time rewards within the ecosystem.
* Enterprises ensure product quality and compliance by contacting the Person-in-Charge.
* Enterprises issue NFTs as rewards to the Person-in-Charge for quality control and communication enhancement.
* Metamask integration ensures secure transactions and interactions with the BitTorrent chain.

# Smart contract Documentation

BitLogix relies on two essential smart contracts deployed on the BitTorrent chain:

* BitLogix Smart Contract
* BitLogixNFT Smart Contract 

## BitLogix Smart Contract

The BitLogix Smart Contract serves as the backbone of our supply chain management DApp. It manages user registration, product creation, payment automation, and token rewards.

**Functions**

```
registerEntity(string memory name, string memory businessDetails, string memory govAuthorizedID) external
```
* Allows enterprises to register within the BitLogix ecosystem.

```
registerRecipient(string memory name, string memory placeOfBusiness, string memory govAuthorizedID) external
```
* Allows recipients to register within the BitLogix ecosystem.

```
claimTokens() external
```
* Enables registered entities and recipients to claim tokens as a one-time reward.

```
deposit() external payable
```

* Lets users deposit BTT tokens into the contract.

```
createProduct(string memory name, uint256 Price, uint256 quantity, string memory pickupPlace, string memory destinationPlace, address recipientAddress) external
```
* Allows registered enterprises to create products for delivery, automating payment and product tracking.

```
confirmReceipt(address entityAddress, uint256 productIndex) external
```
* Allows recipients to confirm product receipt and release payment to the enterprise.

```
getContractBalance() external view returns (uint256)
```
* Allows users to check the token balance of the contract.

```
withdrawPlatformFees() external
```
* Lets the contract owner withdraw platform fees.

## BitLogixNFT Smart Contract

The BitLogixNFT Smart Contract enhances quality control within BitLogix. It allows enterprises to mint and transfer NFTs associated with products.

**Functions**

```
mintNFT(address to, string memory ipfsURI) public onlyOwner
```
* Allows the contract owner (BitLogix) to mint new NFTs with associated IPFS URIs.

```
setBaseURI(string memory newBaseURI) public onlyOwner
```
* Enables the contract owner to update the base URI for token metadata.

```
tokenURI(uint256 tokenId) public view override returns (string memory)
```
* Retrieves token-specific URIs for NFTs.

# Troubleshooting

# Contribution guidline

# Team Members

# Acknowledgement 
