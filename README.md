# Functions And Erros
This assesment explains how the require, assert and revert function statement works, In the Module 1 of the Avalanche in MetaCrafters.

# Description
So first we have the constructor. The constructor is executed once we deploy our contract, It has an Require it needs to pass the condition first before going to the next function that has the assert, The Assert function statement will now check if the variable is true or false if it false it will now be reverted. If it not it will go to the if statement that has the Revert function statement if it's condition is met it will be reverted and if it's not met it will now go to the change the value of the variable

# Getting Started 
So to run this go to https://remix.ethereum.org/ 
Once you're in the website click the start coding and put the provided code here. Then go to Solidity Compiler and run it. And now go to Deploy and Run Transaction to try the provided code.

     // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.0;
    
    contract ErrorHandling {
    
      uint public age;
    
      constructor(uint _age) {
        require(_age >= 18 && _age <= 65, "Age must be between 18 and 65");
        age = _age;
      }
    
      function setAge(uint _newAge) public {
        assert(age > 0);

    
    if (_newAge < 18) {
      revert("Age cannot be set below 18");
    }

    age = _newAge;
       }
     }


# Author 
Dela Cruz, Dex Zyrius B. (3.1 BSIT)
