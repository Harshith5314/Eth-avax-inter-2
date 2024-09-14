---

# Token Management System

This project is a decentralized application (DApp) for managing ERC-20 tokens on the Ethereum blockchain. It allows users to **mint**, **burn**, **transfer**, and **check the balance** of tokens using a simple web interface. The DApp interacts with an Ethereum smart contract deployed on the blockchain via **Web3.js** and **MetaMask**.

## Features

1. **Mint Tokens**: Mint new tokens to a specific Ethereum address.
2. **Burn Tokens**: Burn (destroy) tokens from your balance.
3. **Transfer Tokens**: Transfer tokens from one address to another.
4. **Check Balance**: View the balance of tokens for a specific address.

## Prerequisites

Before running the DApp, ensure you have the following installed:

- **Node.js** (v18.20.4 or higher recommended)
- **MetaMask** browser extension (for interacting with Ethereum accounts)
- **Hardhat** (for compiling and deploying smart contracts)
- **http-server** (for hosting the DApp)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/token-management-system.git
   cd token-management-system
   ```

2. Install the necessary dependencies:
   ```bash
   npm install
   ```

3. Compile the smart contracts using Hardhat:
   ```bash
   npx hardhat compile
   ```

4. Deploy the smart contract:
   ```bash
   npx hardhat run scripts/deploy.js --network [your-network]
   ```

   After deployment, note down the contract address.

5. Update the contract address and ABI in `app.js`:
   - Replace the placeholder `contractAddress` with the address of your deployed contract.
   - Replace the placeholder `contractABI` with your actual ABI.

6. Install **http-server** to run the DApp locally:
   ```bash
   npm install -g http-server
   ```

7. Start the DApp:
   ```bash
   http-server
   ```

8. Open the DApp in your browser at `http://localhost:8080` (or the appropriate URL displayed after starting the server).

## How to Use

### MetaMask Setup

1. Open MetaMask and connect it to your Ethereum wallet.
2. Ensure you are on the same network as the one where the contract is deployed (e.g., Ropsten, Rinkeby, or a local testnet).
3. When you load the DApp, it will automatically request MetaMask to connect to your wallet.

### Functions

#### 1. Mint Tokens

To mint new tokens:

1. Enter the Ethereum address where the tokens should be minted.
2. Enter the number of tokens you wish to mint.
3. Click **Mint Tokens**.
4. MetaMask will prompt you to confirm the transaction.

Upon successful minting, the status will display a success message.

#### 2. Burn Tokens

To burn tokens from your account:

1. Enter the number of tokens you wish to burn.
2. Click **Burn Tokens**.
3. Confirm the transaction in MetaMask.

The tokens will be removed from your balance.

#### 3. Transfer Tokens

To transfer tokens:

1. Enter the recipient's Ethereum address.
2. Enter the number of tokens to transfer.
3. Click **Transfer Tokens**.
4. Confirm the transaction in MetaMask.

Upon successful transfer, the status will display a success message.

#### 4. Check Balance

To check the balance of an address:

1. Enter the Ethereum address whose balance you want to check.
2. Click **Check Balance**.
3. The balance will be displayed on the screen.

## Project Structure

- **contracts/**: Contains the Solidity smart contracts.
- **scripts/**: Scripts for deploying the smart contracts.
- **front_end/**: Contains the HTML, CSS, and JS files for the front-end DApp.
- **hardhat.config.js**: Hardhat configuration file.
- **app.js**: JavaScript file for interacting with the smart contract via Web3.js.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
