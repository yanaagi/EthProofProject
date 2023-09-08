# EthProofProject
MyToken Smart Contract

Introduction
This is a simple Solidity smart contract for creating and managing a custom token on the Ethereum blockchain. The contract implements the basic functionality of a token, including minting and burning tokens. The token is created with specified details such as name, symbol, and initial total supply.

SPDX-License-Identifier: MIT
This contract is licensed under the MIT License. Please refer to the SPDX-License-Identifier header in the contract code for more details.

Requirements
Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply).
Your contract will have a mapping of addresses to balances (address => uint).
You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount.
Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”.
Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned.
Contract Details
Token Details
name: A public variable representing the name of the token.
symbol: A public variable representing the symbol or abbreviation of the token.
totalSupply: A public variable representing the total supply of the token.
Balances
balances: A mapping that associates Ethereum addresses with their respective token balances.
Constructor
The constructor initializes the contract with the provided token name, symbol, and initial total supply. It assigns the entire initial supply to the sender of the contract.
Mint Function
mint(address _receiver, uint256 _value): This function allows the contract owner to mint new tokens. It takes two parameters: _receiver (the address to receive the newly minted tokens) and _value (the amount of tokens to mint). The function increases the total supply by the specified value and adds the minted tokens to the balance of the receiver.
Burn Function
burn(address _owner, uint256 _value): This function allows any token holder to burn their tokens. It takes two parameters: _owner (the address of the token holder) and _value (the amount of tokens to burn). The function deducts the specified value from the total supply and reduces the token holder's balance accordingly. It includes conditions to ensure that the token holder has a sufficient balance for burning.
Usage
To use this smart contract, you can deploy it to the Ethereum blockchain. Make sure to provide the desired token name, symbol, and initial total supply during deployment. After deployment, you can interact with the contract to mint and burn tokens as needed.

License
This smart contract is licensed under the MIT License. See the LICENSE file for more details.

Note: This is a simple example contract and should not be used in production without proper security audits and additional features as required for your use case.
