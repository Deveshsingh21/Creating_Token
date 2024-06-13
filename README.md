

# Video Description 
https://www.loom.com/share/c2a208579253425eb0969101e6d055b8?sid=d7c55a66-2b7d-42a3-96f2-299d50a6a0fe
# Creating A Token Using Solidity
This Smart Contract made on Solidity  defines a simple token contract with minting and burning functionalities.The Contract allows us for the creation and destruction of tokens. 

## Description
The MyToken contract implements the functions to handle the token on Ethereum Blockchain. It includes

Public Variables to store the Token's Details which Includes TokenName, TokenAbbrevation, TotalNumberofTokens.
 A Mapping is done for address to uint which is named balances.
 A mint function is added to create new tokens and add them to specified address.
A burn function is added to destroy tokens from a specified address and ensuring that address has enough balance.

## Getting Started
# Installing
Remix - An Online Solidity IDE is used to run this program

### Executing program
> Go to Remix Website at REMIX IDE
> Create a NEW file there by clicking on the "+" icon on the left hand sidebar.
> Name the file as you want and save it with .sol extension
> Copy the code Given Below:

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., CreatingToken.sol). Copy and paste the following code into the file:

```Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

  
contract MyToken {

    // public variables here
    string public TokenName = "Chhota Bheem";
    string public TokenAbbrevation = "CHHTBHM";
    uint public TotalNumberofTokens = 0;

    // mapping variable here
    mapping (address => uint) public balances;

    // mint function
    function mintingTokens(address _userAddress,uint _amtToken)public{
      TotalNumberofTokens += _amtToken;
      balances[_userAddress] += _amtToken;
    }

    // burn function
    function burnToken(address _userAddress, uint _amtToken)public{
      if(_amtToken <= balances[_userAddress]){
         TotalNumberofTokens -= _amtToken;
         balances[_userAddress] -= _amtToken;
      }
    }

}


```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Creatingtoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mintingTokens , burnToken function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the " burnToken"or "mintingTokens" function. Finally, click on the "transact" button to execute the function and retrieve the output.

## Authors
Metacrafters
Devesh Singh
deveshsingh5603@gmail.com


## License

Th is project is licensed under the MIT License - see the LICENSE.md file for details
