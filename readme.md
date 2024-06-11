# ERC20 Token Contract

This repository contains a Solidity implementation of an ERC20 token standard compliant smart contract. The contract allows for the creation, management, and transfer of tokens on the Ethereum blockchain. It includes functionalities such as transferring tokens between addresses, approving spending on behalf of another address, and minting/burning tokens.

## Table of Contents

- [Overview](#overview)
- [Contract Structure](#contract-structure)
- [Functions](#functions)
- [Events](#events)

## Overview

The ERC20 token contract is designed to facilitate the issuance and transfer of tokens on the Ethereum network. It adheres to the ERC20 standard, which specifies a common interface for tokens to interact with wallets, exchanges, and other decentralized applications.

## Contract Structure

The contract consists of several key components:

- **State Variables**: Includes `totalSupply`, `balanceOf`, `allowance`, `name`, `symbol`, and `decimals` to manage the token's supply, balances, allowances, and metadata.
- **Constructor**: Initializes the token's name, symbol, and decimals upon deployment.
- **Transfer Functionality**: Implements `transfer`, `approve`, and `transferFrom` functions to manage token transfers and approvals.
- **Minting and Burning**: Provides `_mint` and `_burn` internal functions, along with `mint` and `burn` external functions, to control the token's supply.

## Functions

### Constructor

- **Purpose**: Initializes the token's basic properties.
- **Parameters**:
  - `_name`: The name of the token.
  - `_symbol`: The symbol of the token.
  - `_decimals`: The number of decimal places the token can be divided into.
- **Modifiers**: None.

### Transfer

- **Purpose**: Transfers a specified amount of tokens from the caller's account to a recipient's account.
- **Parameters**:
  - `recipient`: The address receiving the tokens.
  - `amount`: The amount of tokens to transfer.
- **Returns**: A boolean indicating success.

### Approve

- **Purpose**: Allows an address (`spender`) to withdraw the caller's tokens up to the `amount`.
- **Parameters**:
  - `spender`: The address allowed to spend tokens.
  - `amount`: The maximum amount of tokens that can be spent.
- **Returns**: A boolean indicating success.

### TransferFrom

- **Purpose**: Transfers a specified amount of tokens from one address to another using the caller's allowance.
- **Parameters**:
  - `sender`: The address from which tokens will be transferred.
  - `recipient`: The address to which tokens will be transferred.
  - `amount`: The amount of tokens to transfer.
- **Returns**: A boolean indicating success.

### Mint

- **Purpose**: Creates new tokens and assigns them to an address.
- **Parameters**:
  - `to`: The address to receive the newly minted tokens.
  - `amount`: The amount of tokens to mint.
- **Modifiers**: None.

### Burn

- **Purpose**: Destroys tokens from an address.
- **Parameters**:
  - `from`: The address from which tokens will be burned.
  - `amount`: The amount of tokens to burn.
- **Modifiers**: None.

## Events

- **Transfer**: Emitted whenever tokens are transferred between accounts.
- **Approval**: Emitted when an allowance is approved for a spender.

## Deployment

To deploy this contract, compile it using a Solidity compiler compatible with version `^0.8.24`. Deploy the compiled contract to the Ethereum network of your choice.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
