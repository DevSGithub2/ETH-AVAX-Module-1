# Smart Token Project

This project demonstrates the implementation of a smart token using Solidity on Remix IDE. It showcases the functionality of require, assert, and revert statements within a smart contract, providing a practical example of error handling and validation in blockchain development.

## Description

This project implements a smart token using Solidity on the Remix IDE platform. It includes functions to set a value and demonstrates the usage of require, assert, and revert statements within a smart contract.

## Getting Started

### Installing

To interact with the smart contract, follow these steps:

* Clone the repository or download the RequireAssertRevertExample.sol file.
* Open the file in Remix IDE or any Solidity-compatible IDE.

### Executing program
Follow these steps to run the program:

* Compile the smart contract.
* Deploy the smart contract to a local or test network.
* Use Remix IDE's interface to call the setValue, requireStatement, assertStatement, and revertStatement functions.

```
// SPDX-License-Identifier: MIT
  pragma solidity ^0.8.0;

  contract RequireAssertRevertExample {
      uint256 public value;

 // Function to set the value
   function setValue(uint256 _newValue) public {
   value = _newValue;
     }
 // Function to demonstrate require statement
    function requireStatement(uint256 _requiredValue) public view {
     require(value >= _requiredValue, "Value must be greater than or equal to the required value");
    }

 // Function to demonstrate assert statement
     function assertStatement() public view {
     assert(value != 0);
        }
 // Function to demonstrate revert statement
     function revertStatement() public pure {
     revert("This function always reverts");
                       }
    }
```

## Help

For any issues or questions, please refer to the Remix IDE documentation or Solidity documentation.
command to run if program contains helper info


## Authors

Dev Sagar - [@DevSGithub2](https://github.com/DevSGitub2)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
