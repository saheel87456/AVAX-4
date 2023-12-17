# Token Contract 

## Overview

This Solidity smart contract represents a custom ERC-20 token named "Degen" (DGN) with additional functionalities such as token minting, burning, transferring, and gadget redemption. The contract is based on the OpenZeppelin ERC-20 and Ownable contracts, providing a foundation for creating and managing fungible tokens.

## Features

1. **Minting Tokens:**
   - The contract owner can mint new tokens and allocate them to a specified address.

2. **Burning Tokens:**
   - Token holders can burn their own tokens, reducing their balance. A corresponding event, `LogMessage`, is emitted upon successful token burning.

3. **Transferring Tokens:**
   - Token holders can transfer tokens to other addresses, ensuring they have sufficient funds.

4. **Gadget Redemption:**
   - Users can redeem gadgets by providing the gadget name and the desired quantity (load). The contract supports four predefined gadgets: Monitor, Drone, AugmentedReality, and iPad. The gadgets have associated prices and available loads, which are checked before redemption.

## Gadget Structure

The contract defines a `Gadget` struct with the following properties:

- `gadgetName`: Name of the gadget.
- `gadgetPrice`: Price of the gadget in tokens.
- `gadgetLoad`: Available quantity/load of the gadget.

## Usage

1. **Contract Deployment:**
   - Deploy the contract on the Ethereum blockchain.

2. **Minting Tokens:**
   - The contract owner can mint new tokens using the `mintTokens` function.

3. **Burning Tokens:**
   - Token holders can burn their tokens using the `burnTokens` function, ensuring they have sufficient funds.

4. **Transferring Tokens:**
   - Token holders can transfer tokens to other addresses using the `transferTokens` function.

5. **Gadget Redemption:**
   - Users can redeem gadgets by providing the gadget name and the desired quantity (load) using the `redeemGadget` function.

## Gadget Initialization

- The contract initializes four gadgets (Monitor, Drone, AugmentedReality, and iPad) with predefined prices and loads.

## Requirements

- This contract assumes the use of OpenZeppelin contracts, particularly ERC-20, Ownable, and ERC-20 Burnable.

## License

- This contract is released under the MIT License. See the `LICENSE` file for details.
