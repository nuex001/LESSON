# LESSON

What is Solidity? Solidity is like a recipe that tells Ethereum how to cook up smart contracts. A smart contract is like a robot that follows instructions and handles money all by itself. Once you write the contract, you can't change it—just like you can't unbake a cake!
In our last class, we talked about Solidity and variables, so we will be doing a revision today.
First of all, head over to Remix, go to the "Create File" section, create a file, and name it with a .sol extension, just like .js or .html.
We will then start up our first contract. First, we need our MTN network, Airtel users should sit by the side abeg 😂.
So first, for our Solidity, we need to have our license there. Me self no get the licenses offhead but this is it:
// SPDX-License-Identifier: MIT

License Identifier 📜
This line is a license declaration that tells the world how the code can be used.
SPDX stands for "Software Package Data Exchange," a standard used to define software licenses.
MIT is a type of open-source license that allows anyone to use, modify, and distribute the code.
It helps developers avoid legal issues by clearly stating the permissions for using the smart contract.
Other License Types:
// SPDX-License-Identifier: MIT → Fully open-source, anyone can use it.
// SPDX-License-Identifier: GPL-3.0 → A more restrictive license that requires sharing modified versions.
// SPDX-License-Identifier: UNLICENSED → No license, meaning private use only.
Compiler Version
Next, we add our instruction for compiling:
pragma solidity ^0.8.0;

This line tells the compiler which version of Solidity to use.
pragma means "rule" or "instruction."
solidity tells the compiler we are using Solidity.
^0.8.0 means use Solidity version 0.8.0 or higher, but below 0.9.0.
Other Versions:
pragma solidity ^0.8.0; → Uses 0.8.0 or newer (but below 0.9.0).
pragma solidity >=0.7.0 <0.9.0; → Allows any version from 0.7.0 to 0.8.x.
pragma solidity 0.8.19; → Uses Solidity version 0.8.19 only.
Why is this needed?
Solidity updates frequently, fixing bugs and adding new features. By specifying a version, you ensure your contract runs correctly without unexpected issues in newer versions.

Defining Our Contract
Now, we get to our contract! Just like a JavaScript class, we start with contract, followed by the name of the contract, and then { everything goes inside here }.
contract MyFirstContract {
    // Contract logic goes here
}

We can deploy this right now!

Solidity Variables
We also talked about variables in Solidity:
// Uint and Int types
uint private number1 = 10;
uint public number2 = number1;
int public num1 = -1;

// String type
string public name = "10101";

// Boolean type
bool public isMale = false;

// Address type
address public myAddress = 0xb9f75cB1B7eC69529190d973eB12D796236a0E90;

// Arrays
uint[] public numArr = [1, 2, 3];
string[] public strArr = ["1", "2", "3", "5"];

Visibility Keywords
We also covered private, internal, external, and public:
private: Only available inside the contract.
internal: Available inside the contract and child contracts.
external: Can only be called from outside the contract.
public: Can be accessed both inside and outside the contract.

Auto-Increment Example
We also built an auto-increment function using 
contract Counter {
    uint public count;

    function incrementCount() external {
        count += 1;
    }
}

This function increases count by 1 each time it is called.

Next Steps
Now that we understand Solidity basics, we will start working on integrating a frontend using HTML and JavaScript to interact with our smart contract!

