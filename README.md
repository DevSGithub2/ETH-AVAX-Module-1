# Smart Token Project

This project demonstrates the implementation of a smart token using Solidity on Remix IDE. It showcases the functionality of require, assert, and revert statements within a smart contract. It is a simple example designed to show how these statements can be used to enforce conditions, ensure internal consistency, and manage execution flow in smart contracts

## Description

This project implements a smart token using Solidity on the Remix IDE platform. It includes functions to set a value and demonstrates the usage of require, assert, and revert statements within a smart contract.

The SimpleContract includes three functions:

1. setValue(uint256 _value): Sets value if _value is greater than zero.

2. doubleValue(): Returns double the value, ensuring value is positive.

3. resetValue(): Resets value to zero, reverting if already zero.

## Getting Started

### Installing

To interact with the smart contract, follow these steps:

* Clone the repository or download the RequireAssertRevertExample.sol file.
* Open the file in Remix IDE or any Solidity-compatible IDE.

### Executing program
Follow these steps to run the program:

* Compile the smart contract.
* Deploy the smart contract to a local or test network.
* Use Remix IDE's interface to call the setValue, doubleValue, and resetValue functions.
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract SimpleContract {
    uint256 public value;

    // Function to set a value that uses require() to check validity
    function setValue(uint256 _value) public {
        require(_value > 0, "Value must be greater than zero");
        value = _value;
    }

    // Function that uses assert() to ensure internal consistency
    function doubleValue() public view returns (uint256) {
        assert(value > 0); // Ensure that value has been set
        return value * 2;
    }

    // Function to reset value, with a meaningful use of revert()
    function resetValue(uint256 _newValue) public {
        require(_newValue >= 0, "New value must be non-negative");

        if (_newValue == value) {
            revert("New value cannot be the same as the current value");
        }

        value = _newValue;
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
