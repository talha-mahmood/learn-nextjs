# Solidity Variables

Solidity supports three types of variables.

###State Variables

Variables whose values are permanently stored in a contract storage.

```solidity
pragma solidity ^0.5.0;
contract SolidityTest {
   uint storedData;      // State variable
   constructor() public {
      storedData = 10;   // Using State variable
   }
}

###Local Variables

Variables whose values are available only within a function where it is defined. Function parameters are always local to that function.

```solidity
pragma solidity ^0.5.0;
contract SolidityTest {
   uint storedData; // State variable
   constructor() public {
      storedData = 10;   
   }
   function getResult() public view returns(uint){
      uint a = 1; // local variable
      uint b = 2;
      uint result = a + b;
      return result; //access the local variable
   }
}


### Global Variables

These are special variables which exist in global workspace and provide information about the blockchain and transaction properties.


### `blockhash(uint blockNumber) returns (bytes32)`
Hash of the given block - only works for 256 most recent, excluding current, blocks

### `block.coinbase returns (address payable)`
Current block miner's address

### `block.difficulty returns (uint)`
Current block difficulty

### `block.gaslimit returns (uint)`
Current block gaslimit

### `block.number returns (uint)`
Current block number

### `block.timestamp returns (uint)`
Current block timestamp as seconds since unix epoch

### `gasleft() returns (uint256)`
Remaining gas

### `msg.data returns (bytes calldata)`
Complete calldata

### `msg.sender returns (address payable)`
Sender of the message (current caller)

### `msg.sig returns (bytes4)`
First four bytes of the calldata (function identifier)

### `msg.value returns (uint)`
Number of wei sent with the message

### `now returns (uint)`
Current block timestamp

### `tx.gasprice returns (uint)`
Gas price of the transaction

### `tx.origin returns (address payable)`
Sender of the transaction


### Solidity Variable Names

1-While naming your variables in Solidity, keep the following rules in mind.

2-You should not use any of the Solidity reserved keywords as a variable name. These keywords are mentioned in the next section. For example, break or boolean variable names are not valid.

3-Solidity variable names should not start with a numeral (0-9). They must begin with a letter or an underscore character. For example, 123test is an invalid variable name but _123test is a valid one.

4-Solidity variable names are case-sensitive. For example, Name and name are two different variables.