pragma solidity >=0.4.0 <0.6.0;

```// This is a simple Solidity file with a single contract definition
contract SimpleStorage {
   uint storedData; // state variable

   // Function to set storedData
   function set(uint x) public {
      storedData = x; // set the value of storedData
   }

   // Function to get storedData
   function get() public view returns (uint) {
      return storedData; // return the value of storedData
   }
}```
