# Error-Handling
Explains how the require, assert, and revert function statements works


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
