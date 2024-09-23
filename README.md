MyToken (NEXA)


Project Title
MyToken (NEXA) - A basic ERC20-like token implemented in Solidity.

Description
This smart contract allows users to mint and burn tokens in a basic token system built on the Ethereum blockchain. The contract owner can create tokens (mint), and anyone with tokens can reduce their balance (burn). This contract includes features such as token supply management and balance tracking via mappings.

Getting Started

Installing
To get started with this contract, follow these steps:

1.Install Remix IDE or use Hardhat as your development environment.

2.If using Hardhat, set up a new project by running the following commands:

mkdir MyTokenProject
cd MyTokenProject
npm init -y
npm install --save-dev hardhat
npx hardhat


3.Create a Solidity file MyToken.sol and paste the code provided below.

pragma solidity >=0.6.12 <0.9.0;

contract MyToken {
  // Public variables here
  string public tokenName = "NEXA";
  string public symbol = "EON"; 
  uint public totalSupply = 0;

  // Mapping variables here
  mapping(address => uint) public balances;

  // Mint function
  function mint(address _address, uint _value) public {
    totalSupply += _value;
    balances[_address] += _value;
  }

  // Burn function
  function burn(address _address, uint _value) public {
    if (balances[_address] >= _value) {
      totalSupply -= _value;
      balances[_address] -= _value;
    }
  }
}



Modifications

1.You can modify tokenName, symbol, and initial totalSupply as per your project's requirements.
2.Make sure to set up your development environment correctly depending on the platform you're using (Remix or Hardhat).

Executing the Program

Using Remix IDE:
1.Open Remix IDE.
2.Create a new file named MyToken.sol and paste the provided Solidity code.
3.Compile the contract using the Solidity compiler in Remix.
4.Deploy the contract to the testnet or local environment (JavaScript VM).
5.After deployment, you can call the mint and burn functions by interacting with the deployed contract.

Using Hardhat:

1.Compile the contract using Hardhat:
npx hardhat compile

2.Deploy the contract with Hardhat (create a deployment script first):

npx hardhat run scripts/deploy.js --network <network_name>

3.Interact with the deployed contract using a script or directly on the network.

Help

Common Issues:

1.Ensure that your Solidity version in the code matches the compiler version in Remix or Hardhat.
2.If using Hardhat, ensure you have the correct configuration for the network and accounts in the hardhat.config.js file.

Commands: To view more details about Hardhat commands, run:

npx hardhat help

Authors

Metacrafter Sukhneet
Github Username:Sukhneet73

License

This project is licensed under the MIT License - see the LICENSE.md file for details.
