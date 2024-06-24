MyToken Smart Contract


Introduction

Welcome to the MyToken Smart Contract. This contract is a basic implementation of an ERC-20 like token using Solidity. The token is named "NEXA" with the abbreviation "EON".

Features

1.Token Name: NEXA

2.Token Symbol: EON

3.Total Supply: The aggregate amount of tokens in circulation.

4.Balances: A mapping that records token balances for each address.

Contract Specifications

Public Variables
1.tokenName: The name of the token.

2.tokenAbbry: The abbreviation of the token.

3.totalSupply: The total number of tokens issued.

4.balances: A mapping that tracks the token balance for each address.

Functions

Mint Function
This function creates new tokens and assigns them to a specified address, increasing the total supply.

function mint(address _address, uint _value) public

Parameters:
`_address`: The recipient address of the newly minted tokens.
`_value`: The number of tokens to mint.

Burn Function
This function removes tokens from a specified address, reducing the total supply, provided the address has sufficient tokens.

function burn(address _address, uint _value) public


Parameters:
_address: The address from which tokens will be burned.
_value: The number of tokens to burn.

How to Use

Minting Tokens

To mint tokens, call the `mint` function with the recipient address and the amount of tokens to mint.
MyToken.mint(0xYourAddress, 100);


Burning Tokens

To burn tokens, call the `burn` function with the address from which to burn tokens and the amount of tokens to burn.
MyToken.burn(0xYourAddress, 50);


Deployment

Follow these steps to deploy the MyToken contract:

1.Install Node.js.

2.Install Truffle and Ganache.

3.Initialize a new Truffle project:

4.Add the MyToken contract code to a new file named MyToken.sol in the contracts directory.

5.Compile and deploy the contract:

6.Use the Truffle console to interact with the contract:
