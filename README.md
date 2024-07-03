# CustomToken Smart Contract

## Overview

The `CustomToken` smart contract is a simple implementation of a custom ERC20-like token on the Ethereum blockchain. It includes basic functionalities such as minting and burning tokens.

## Token Details

- **Token Name:** Custom Coin
- **Token Symbol:** CC
- **Total Supply:** Variable, can be increased through minting and decreased through burning.

## Contract Structure

### Public Variables

- `tokenName`: The name of the token. In this case, it's "Custom Coin".
- `tokenAbbrv`: The abbreviation of the token. In this case, it's "CC".
- `totalSupply`: The total supply of the token in circulation.

### Mappings

- `balances`: A mapping from addresses to their respective token balances.

### Functions

#### mint

Increases the total supply of tokens and adds the specified amount to the balance of the given address.

```solidity
function mint(address _address, uint _value) public
_address: The address to which the tokens will be minted.
_value: The amount of tokens to mint.
##### burn
Decreases the total supply of tokens and removes the specified amount from the balance of the given address. The function requires that the address has enough balance to burn.
function burn(address _address, uint _value) public
_address: The address from which the tokens will be burned.
_value: The amount of tokens to burn.
Usage
Minting Tokens
To mint tokens, call the mint function with the recipient's address and the amount of tokens to mint:
mint(0xRecipientAddress, amount);
Burning Tokens
To burn tokens, call the burn function with the holder's address and the amount of tokens to burn:
burn(0xHolderAddress, amount);
Make sure that the address has enough balance to burn the specified amount.
