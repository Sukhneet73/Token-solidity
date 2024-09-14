`MyToken` Smart Contract

`NEXA`  is a simple ERC20-like token implemented in Solidity. This contract allows for minting and burning of tokens. It is designed to be a straightforward example of a custom token on the Ethereum blockchain.

Token Details

Name: NEXA
Symbol: EON
Decimals: 18 (standard for ERC20 tokens)
Total Supply: Initially 0
Contract Features
Functions

Minting Tokens The mint function allows the creation of new tokens and assigns them to a specified address.

function mint(address _to, uint256 _value) public;

Parameters:

_to: The address to receive the minted tokens. _value: The number of tokens to mint.

Burning Tokens The burn function allows the destruction of tokens from a specified address, reducing the total supply.

function burn(address _to, uint256 _value) public;

Parameters:

_to: The address from which tokens will be burned. _value: The number of tokens to burn.

Usage Deployment To deploy the `MyToken` contract, you will need an Ethereum development environment such as Truffle, Hardhat, or Remix. Below is a basic example using Remix:

Open Remix. 1.Create a new file and paste the `MyToken` contract code.

2.Compile the contract.

3.Deploy the contract using the "Deploy" button in Remix.

Interacting with the Contract Once deployed, you can interact with the contract using web3.js, ethers.js, or directly via Remix.

Mint Tokens To mint tokens, call the mint function with the recipient's address and the amount of tokens to mint.

Example using Remix:

1.Select the deployed `MyToken` contract.

2.Select the mint function.

3.Enter the recipient's address and the amount of tokens to mint.

4.Click "Transact" to execute the transaction.

Burn Tokens To burn tokens, call the burn function with the address from which to burn tokens and the amount to burn.

Example using Remix:

1.Select the deployed Nexa contract.

2.Select the burn function.

3.Enter the address from which to burn tokens and the amount to burn.

4.Click "Transact" to execute the transaction.



