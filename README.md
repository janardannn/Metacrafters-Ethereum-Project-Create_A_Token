# Metacrafters-Ethereum-Project-Create_A_Token

## Solidity Contract: Counter-Strike Token

This Solidity contract, named `CounterStrike`, represents a simple token contract with the following features:

### Public Variables
1. `name`: The name of the token, set to "Counter-Strike Token". Its constant so we cannot reassign any value.
2. `symbol`: The abbreviation of the token, set to "CSGO". This variable is also constant.
3. `totalSupply`: The total supply of the token, initially set to 0.

### Mapping
The contract uses a mapping `balances` to store the token balances of individual addresses.

### Mint Function
The `mint` function creates new tokens and assign them to a specified address. It takes two parameters:
- `addr`: The address to which the tokens will be minted.
- `amount`: The number of tokens to be minted.

The function updates the `totalSupply` by adding the `amount` and increases the balance of the specified `addr` by the same `amount` in the balances mapping.

### Burn Function
The `burn` function destroys existing tokens. It takes two parameters:
- `addr`: The address from which the tokens will be burned.
- `amount`: The number of tokens to be burned.

The function first checks if the balance of the specified `addr` is greater than or equal to the `amount` to be burned. If the condition is met, it decreases the `totalSupply` by the `amount` and decreases the balance of the specified `addr` by the same `amount`.

This contract provides a basic implementation of a token with the ability to mint and burn tokens.
