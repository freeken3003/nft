# CryptoPoops Cadence File

This Cadence file implements the `CryptoPoops` smart contract, which is built on top of the `NonFungibleToken` contract. It enables the creation, ownership, and management of non-fungible tokens (NFTs) called "CryptoPoops".

## Features

- **NFT Creation**: Users can create unique CryptoPoops NFTs with custom attributes such as name, favorite food, and lucky number.
- **Token Management**: The contract allows users to deposit, withdraw, and manage their CryptoPoops NFTs.
- **Event Logging**: Events are emitted for important contract actions like initialization, deposit, and withdrawal.
- **Collection Interface**: Provides a public interface `MyCollectionPublic` for interacting with user collections.

## Smart Contract Components

### CryptoPoops Contract

- **totalSupply**: Tracks the total supply of CryptoPoops NFTs.
- **Events**:
- `ContractInitialized`: Emitted when the contract is initialized.
- `Withdraw`: Emitted when a user withdraws an NFT.
- `Deposit`: Emitted when a user deposits an NFT.

### NFT Resource

- Defines the attributes of a CryptoPoops NFT, including name, favorite food, and lucky number.
- Implements the `MyCollectionPublic` interface.

### Collection Resource

- Implements the `NonFungibleToken.Provider`, `NonFungibleToken.Receiver`, `NonFungibleToken.CollectionPublic`, and `MyCollectionPublic` interfaces.
- Manages the ownership and operations of CryptoPoops NFTs within a collection.
- Provides functions for depositing, withdrawing, and accessing NFTs.

### Minter Resource

- Handles the creation of new CryptoPoops NFTs.

## Functions

- **createEmptyCollection**: Creates an empty collection of CryptoPoops NFTs.
- **createNFT**: Creates a new CryptoPoops NFT with specified attributes.
- **createMinter**: Creates a new instance of the Minter resource.

## Initialization

- Initializes the contract with total supply set to 0.
- Emits the `ContractInitialized` event.
- Saves the Minter resource to storage.
