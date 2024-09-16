# DND Coin (DND) - ERC20 Token Project

## Description
This project demonstrates the creation, minting, burning, and transferring of a custom ERC20 token called **DND Coin (DND)** using Solidity. It validates maximum supply and ensures only the owner can mint new tokens. This project is part of the Metacrafters Intermediate ETH + AVAX Module 3 to showcase different function types in Solidity and error handling.

## Features
- **Minting**: Owner can mint tokens while ensuring the total supply doesn’t exceed the maximum limit of 100,000.
- **Burning**: Tokens can be burned from any address to reduce the total supply.
- **Transferring**: Allows transferring tokens between addresses.
- **Error Handling**: Includes error handling for validation and ownership.

## How to Use

### Prerequisites
- Solidity ^0.8.18
- Remix IDE (https://remix.ethereum.org/)
- MetaMask (for Ethereum wallet integration)

### Steps to Deploy and Test
1. Go to [Remix Ethereum IDE](https://remix.ethereum.org/).
2. Create a new file and paste the Solidity code.
3. Compile the code (`Ctrl + S`) or use the "Compile" button.
4. Go to the **Deploy & Run Transactions** tab, select the contract, and set an initial supply.
5. Interact with the contract functions:
    - **Mint**: To mint new tokens as the owner.
    - **Transfer**: To transfer tokens to another address.
    - **Burn**: To burn tokens from an address.

### Code Walkthrough
- **Mint Function**: Allows the owner to mint new tokens. Validates that the total supply does not exceed the maximum limit.
- **Transfer Function**: Allows transferring tokens between addresses. Uses the `_transfer` method from the ERC20 base contract.
- **Burn Function**: Allows burning tokens to reduce the total supply.

### Loom Video
[https://www.loom.com/share/7ad362ea6b474c12bd49b4a5050aeeb2)

## Author
**Prince Kumar**  
Email: [kumarprincerajput124@gmail.com](mailto:kumarprincerajput124@gmail.com)

## License
This project is licensed under the MIT License.
