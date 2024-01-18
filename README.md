# BeautyProductToken 

## Overview

The BeautyProductToken is a Solidity smart contract deployed on the Ethereum blockchain that represents a tokenized system for managing beauty product transactions. This contract extends the functionality of the ERC-20 token standard and incorporates features for minting, burning, cosmetic redemption, and token rewards.

## Contract Features

### ERC-20 Compliance

The BeautyProductToken contract is compliant with the ERC-20 token standard. It inherits from the OpenZeppelin ERC-20 implementation and includes additional functionalities.

### Ownable

The contract utilizes the Ownable contract from OpenZeppelin, ensuring that only the owner of the contract can execute certain functions, such as minting new tokens.

### ERC20Burnable

This contract extends the ERC20Burnable contract from OpenZeppelin, allowing token holders to burn their own tokens, reducing the total supply.

### Cosmetic Redemption

The contract introduces a mechanism for users to redeem beauty products using their tokens. Each cosmetic item is associated with a specific cost in tokens, and users can exchange their tokens for these cosmetics. The redeemed cosmetics are recorded, and the user's balance is updated accordingly.

### Token Transfer

Token holders can transfer their tokens to other addresses using the standard ERC-20 `transfer` function. Additionally, there is a custom `transferTokens` function to facilitate token transfers on behalf of another address.

### Minting and Burning

The contract includes functions to mint new tokens (only accessible by the owner) and burn existing tokens (accessible by any token holder). Minting allows for the creation of new tokens, while burning reduces the total supply.

## Cosmetic Options

The contract supports multiple cosmetic options, such as Lipstick, Eyeshadow, Perfume, and Foundation. The associated costs for each cosmetic are predefined during contract deployment.

## Events

The contract emits two types of events:

1. `CosmeticRedeemed`: Triggered when a user redeems a cosmetic, providing details about the donor address, cosmetic name, and the associated cost.
2. `TokensRewarded`: Triggered when the owner rewards tokens to a recipient, providing details about the recipient's address and the rewarded token sum.

## Usage

The contract can be deployed on the Ethereum blockchain, and users can interact with it using a compatible Ethereum wallet or through a decentralized application (DApp). Owners can mint new tokens, users can burn their tokens, and everyone can participate in cosmetic redemption and token transfers.

