#Metacrafters Intermediate ETH + AVAX Module 3 [Types of Functions]
The project consists of creating, minting, burning, and transferring tokens using ERC20 with validation and error catching.
Description
This code will create, mint, burn, and transfer a token called DND Coin [DND]. The purpose is to demonstrate the student's mastery of different function types, complete with explanation and code walkthrough, to assess the student's skill in this level of Solidity programming.


#code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/utils/math/SafeMath.sol";

contract DNDCoin is ERC20 {
    address public owner;

    // For demonstration purposes
    uint256 public constant MAX_SUPPLY = 100000; // Max supply set to 100000

    modifier onlyOwner() {
        require(msg.sender == owner, "Only the owner is allowed to initiate this function");
        _;
    }

    modifier validateMint(uint256 value) {
        require(totalSupply() + value <= MAX_SUPPLY, "Exceeds maximum supply");
        _;
    }

    constructor(uint256 initialSupply) ERC20("DND Coin", "DND") {
        _mint(msg.sender, initialSupply);
        owner = msg.sender;
    }

    function mint(address to, uint256 value) external onlyOwner validateMint(value) {
        _mint(to, value);
    }

    function transfer(address to, uint256 value) public override returns (bool) {
        _transfer(msg.sender, to, value);
        return true;
    }

    function burn(address from, uint256 value) external {
        _burn(from, value);
    }
}

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar.

Executing program
Compile the program by pressing (ctrl + s) or click the compile button from the top left side of the screen.
Deploy the smart contract under the Deploy & Run Transactions tab by setting an initial value.
Authors
Prince kumar
Email=kumarprincerajput124@gmail.com
