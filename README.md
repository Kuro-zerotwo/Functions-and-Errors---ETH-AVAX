# Functions-and-Errors---ETH-AVAX
## Description
The `ErrorHandling` smart contract demonstrates essential error management techniques crucial for secure Ethereum smart contracts. It utilizes `require()` in `totestRequire(uint num)` to enforce the condition `num > 15`, preventing invalid operations and ensuring contract reliability. `totestRevert(uint num)` uses `revert()` for exiting transaction with clear error message when condition `num <= 20` is violated, maintaining transaction integrity. Furthermore, `totestAssert()` employs `assert()` to validate critical state condition (`n == 0`), halting execution upon detecting potential contract logic errors. These mechanisms collectively enhance contract robustness, offering effective error handling.

# Getting Started

### Installing
*No Installation Required

### Execution of Program

* To execute the program
1. Open in Remix IDE
2. Create a new file and paste the 'ErrorHandling' contract code into the file.
3. Compile
4. Deploy
* Contract
```cpp
//write a smart contract that implements the require(), assert() and revert() statements
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract ErrorHandling {

    function totestRequire(uint num) public pure returns(string memory) {
        require(num > 15, "Input should be greater than 15");
         return "Valid Input(Require)";
    }

    function totestRevert(uint num) public pure returns (string memory) {
        if (num <= 20) {                                   //if yes then revert else valid input
            revert("Input should be greater than 20");
        }
            return "Valid Input(Revert)";                   
       
    }

    uint public n;
    function totestAssert() public view returns (string memory){
        assert(n == 0);
        return "Passed Assert Test";
    }
    function increment_n() public
    {
        n++;
    }

}
```
## Help
If you encounter any issues or have questions regarding the contract, please feel free to open an issue in this repository or contact the authors directly.

## Authors
* Anita Devi- https://github.com/Kuro-zerotwo
  
## License 
This project is licensed under the MIT License - see the LICENSE.md file for details.
