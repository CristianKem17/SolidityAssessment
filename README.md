# Introduction

Hello, My name is Cristian Kem D. Morales. A 2nd-year student at the National Teachers College.

# Hello World

This Solidity program is simple and demonstrates the mint and burn functions in the Solidity programming language. 


## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a two function that is to mint the tokens and burn the tokens. This program serves as an assessment to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

To create this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Do this code.

```javascript
// SPDX-License-Identifier: MIT
contract MyToken {

    // public variables here
    string public tokenName = "Morales";
    string public tokenAbbrv = "Morals";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address ADDress, uint VALue) public {
        totalSupply += VALue;
        balances[ADDress] += VALue;
    }

    // burn function
    function burn (address ADDress, uint VALue) public {
        if (balances[ADDress] >= VALue)
        totalSupply -= VALue;
        balances[ADDress] -= VALue;
    }

}
```

### Executing program

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Assessment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Assessment" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can copy to the clipboard and paste it on burn, mint and balances in the deployed contracts. Put any amount of token you want in value, so that you can mint it. Check the amount of token you minted in totalSupply and balances, Once you confirm it you can now burn it by puttting how much the amount of tokens you want to burn because it will be subtracted to the tokens that minted then click on the "burn" function. Finally, click on the "transact" button to execute the function and you will see how much tokens you have left.

## Authors

CristianKem17

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
