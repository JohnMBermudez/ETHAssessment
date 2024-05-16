# My Token
This project is a simple Ethereum token contract that has function call mint and burn.

## Description
Written in Solidity, a programming language used to create smart contracts on the Ethereum blockchain, this program is a straightforward contract. 
The contract has two functions. The first is the mint function, which adds tokens to the address you provide and raises the overall supply. 
The second is the burn function, which works in opposition to mint by removing tokens from the specified address and reducing the overall supply. 
only in the event that the address has sufficient tokens to burn.


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. 
Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

pragma solidity 0.8.18;
contract myToken {

    // public variables here
    string public tokenName = "META";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances [_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        } 
    } 
}

Select the "Solidity Compiler" tab from the sidebar on the left to begin compiling the code. 
Click "Compile myToken.sol" after ensuring that the "Compiler" option is set to "0.8.18" (or another compatible version).

Selecting the "Deploy & Run Transactions" tab from the left-hand sidebar will allow you to deploy the contract after the code has been compiled. 
Click the "Deploy" button after choosing the "MyToken" contract from the dropdown menu.

Calling the function will allow you to communicate with the contract after it has been deployed. Select the "MyToken" contract located in the sidebar on the left. 
and after that select the "mint" option. Copy the account address at the top, paste it, and enter the desired number to add an address.

## Authors
BSIT 2.1 Bermudez, John Michael M. Bermudez
