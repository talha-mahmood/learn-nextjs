# Solidity Source File

A Solidity source file can contain any number of contract definitions, import directives, and pragma directives.

## Pragma

The first line is a pragma directive which specifies that the source code is written for Solidity version 0.4.0 or newer, up to, but not including, version 0.6.0. 

```solidity
pragma solidity >=0.4.0 <0.6.0;

A pragma directive is always local to a source file, and if you import another file, the pragma from that file will not automatically apply to the importing file.

To specify a pragma for a file which will not compile earlier than version 0.4.0 and will not work on a compiler starting from version 0.5.0, use the following syntax:

pragma solidity ^0.4.0;
Here, the second condition is added by using the caret (^) symbol.

Contract
A Solidity contract is a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain.

contract SimpleStorage {
   uint storedData;
   function set(uint x) public {
      storedData = x;
   }
   function get() public view returns (uint) {
      return storedData;
   }
}
The line uint storedData; declares a state variable called storedData of type uint, and the functions set and get can be used to modify or retrieve the value of the variable.

Importing Files
Solidity supports import statements that are very similar to those available in JavaScript.

The following statement imports all global symbols from "filename".

import "filename";
The following example creates a new global symbol symbolName whose members are all the global symbols from "filename".

import * as symbolName from "filename";
To import a file x from the same directory as the current file, use import "./x" as x;. If you use import "x" as x; instead, a different file could be referenced in a global "include directory".

Reserved Keywords
Following are the reserved keywords in Solidity −

abstract, after, alias, apply, auto, case, catch, copyof, default, define, final, immutable, implements, in, inline, let, macro, match, mutable, null, of, override, partial, promise, reference, relocatable, sealed, sizeof, static, supports, switch, try, typedef, typeof, unchecked.