# MyToken

This is a simple ERC-20 token contract implemented in Solidity. The contract allows for the creation and destruction of tokens, as well as storing information about the token.

## Requirements

1. The contract has public variables that store the details about the coin:
   - `tkn_name`: A string representing the name of the token.
   - `tkn_abbvy`: A string representing the abbreviation of the token.
   - `ttl_supply`: An unsigned integer representing the total supply of the token.

2. The contract has a mapping of addresses to balances:
   - `balnc`: A mapping that associates addresses with their corresponding token balances.

3. The contract has a `mint` function that increases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `location`: The address to which the tokens will be minted.
     - `val`: The amount of tokens to be minted.
   - Actions:
     - Increase the `ttl_supply` by `val`.
     - Increase the balance of the `location` by `val`.

4. The contract has a `burn` function that decreases the total supply and the balance of the "sender" address by a given value:
   - Parameters:
     - `location`: The address from which the tokens will be burned.
     - `val`: The amount of tokens to be burned.
   - Actions:
     - Check if the balance of the `location` is greater than or equal to `val`.
     - If true, decrease the `ttl_supply` by `val`.
     - Decrease the balance of the `location` by `val`.

## Usage

1. Deploy the `MyToken` contract to a supported Ethereum network.

2. Once deployed, you can interact with the contract by calling the following functions:

   - `mint`: Creates new tokens and assigns them to a specified address.
     - Parameters:
       - `location`: The address to which the tokens will be minted.
       - `val`: The amount of tokens to be minted.

   - `burn`: Destroys existing tokens by reducing the total supply and the balance of a specified address.
     - Parameters:
       - `location`: The address from which the tokens will be burned.
       - `val`: The amount of tokens to be burned.

## Authors

Shivam Singh  

## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.

