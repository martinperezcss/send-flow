# 💸 SendFlow

A modern, multi-chain decentralized app (DApp) to **send ETH and tokens**, **track balances**, and **view transaction history**. Designed with a polished UI, animated visuals, custom gas controls, and seamless wallet integration.

---

## 🚀 Features

- 🔗 **Wallet Connection** – Connect MetaMask and other wallets using RainbowKit & wagmi.
- 💰 **Send ETH / Tokens** – Choose gas presets or set your own Gwei manually.
- ⚡ **Custom Gas Limit** – Set a custom gas limit for advanced control over transaction execution.
- 👛 **Live Balances** – View your ETH and token holdings across major EVM chains.
- 📜 **Transaction History** – With filtering, search, and CSV export.
- 🔔 **Modern Notifications** – Real-time feedback via [Sonner](https://sonner.emilkowal.ski/).
- 🌌 **Animated Background** – Interactive particles when no wallet is connected.
- 📱 **Responsive UI** – Built with TailwindCSS for mobile and desktop support.
- 🧪 **Test Coverage** – Core components tested with Jest + React Testing Library.

---

## ⛽ Understanding Gas, Gas Price, and Gas Limit

- **Gas** is the unit that measures the computational effort required to execute operations on the Ethereum network.
- **Gas Price** is the amount you are willing to pay per unit of gas, usually denominated in Gwei. Higher gas price = faster confirmation.
- **Gas Limit** is the maximum amount of gas you allow for a transaction. For simple ETH transfers, the minimum is 21,000, but interacting with contracts or sending tokens requires more.

### How Custom Gas Limit Works in SendFlow

- By default, the app estimates the required gas limit for your transaction.
- You can manually increase the gas limit if you want to ensure your transaction does not run out of gas (useful for complex contract interactions).
- If you set the gas limit below the estimated minimum, the app will prevent the transaction and show an error.
- For simple ETH transfers, only 21,000 gas is used, even if you set a higher limit (the unused gas is refunded).

> **Tip:** For most users, the estimated gas limit is sufficient. Customizing is for advanced users or special contract interactions.

---

## 🌍 Supported Networks

- Ethereum Mainnet
- Polygon
- Arbitrum
- Optimism
- Base
- Sepolia (testnet)
- Binance Smart Chain (BSC)
- BSC Testnet

> ⚠️ **Sepolia is for testing only**. ETH there is not real. To perform actual transactions, switch to **Ethereum Mainnet** or another production network and ensure your wallet has real funds.

---

## 🧑‍🏫 Quick Start (MetaMask + Sepolia Testnet)

### 1. Install MetaMask

- Go to [https://metamask.io](https://metamask.io)
- Install the browser extension
- Create or import a wallet
- Securely back up your secret recovery phrase — **never share it**

### 2. Add Sepolia Test Network

- Open MetaMask
- Click the network dropdown (e.g., “Ethereum Mainnet”)
- Click **"Show/hide test networks"**
- Enable testnets and select **"Sepolia Test Network"**

### 3. Get Sepolia Test ETH

To test the app on the Sepolia testnet, you’ll need some test ETH (not real funds):

- Copy your wallet address from MetaMask
- Visit the Google Cloud faucet to claim free Sepolia ETH:
  - 🔗 [Google Cloud Sepolia Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)
  
- Paste your wallet address in the faucet form
- Follow the instructions to receive test ETH in your wallet
- Wait a few minutes, then check your wallet balance in MetaMask

> ⚠️ **Sepolia ETH is not real ETH**. It is only for testing and development. To send real funds, use **Ethereum Mainnet** or another mainnet and ensure your wallet is funded.

### Why use Sepolia?

- **No cost for testing:** Sepolia ETH is free and available in large quantities, making it perfect for testing and development.
- **Realistic environment:** The Sepolia testnet is a mirror of the Ethereum Mainnet, allowing you to test real-world scenarios before moving to mainnet.

---

## 📦 Tech Stack

- **React** – Framework
- **RainbowKit + wagmi** – Wallet support & chain switching
- **ethers.js** – Blockchain interaction
- **Alchemy SDK** – Balances, tokens, transactions
- **axios** – REST API calls
- **tsParticles** – Animated visual background
- **TailwindCSS** – Utility-first UI
- **Sonner** – Toast notifications
- **Jest + React Testing Library** – Testing

---

## ⚙️ How to Run Locally

```bash
git clone https://github.com/casaislabs/send-flow.git
cd send-flow
yarn install
yarn start
```
---

## 🔐 Environment Variables

Create a `.env` file in the root folder and fill in the required API keys:

```env
REACT_APP_ETHERSCAN_API_KEY=your_key
REACT_APP_BSCSCAN_API_KEY=your_key
REACT_APP_POLYGONSCAN_API_KEY=your_key
REACT_APP_ARBISCAN_API_KEY=your_key
REACT_APP_OPTIMISM_API_KEY=your_key
REACT_APP_SEPOLIA_API_KEY=your_key
REACT_APP_BSCSCAN_TESTNET_API_KEY=your_key
REACT_APP_ALCHEMY_API_KEY=your_key
REACT_APP_WALLETCONNECT_PROJECT_ID=your_project_id
```
You can get these keys from:

- [Etherscan](https://etherscan.io/myapikey)
- [Alchemy](https://dashboard.alchemy.com/)
- [WalletConnect](https://cloud.walletconnect.com/)
- [PolygonScan](https://polygonscan.com/myapikey)
- [Arbiscan](https://arbiscan.io/myapikey)
- [Optimism](https://optimistic.etherscan.io/myapikey)
- [Sepolia Faucet](https://cloud.google.com/application/web3/faucet/ethereum/sepolia)
- [BSCScan (Mainnet & Testnet)](https://bscscan.com/myapikey)

---

## 🔧 Running Tests

The project includes tests for key components. To run them, simply execute:

```bash
yarn test
```
Tests are located in `src/App.test.js`.

---

## 🎨 UI/UX Design

The app features a modern and user-friendly design built using **TailwindCSS**. Animations and real-time notifications enhance the user experience, while the app is fully responsive for both desktop and mobile devices.

---

## 📂 Project Structure

```bash
src/
├── components/          # Core UI components (e.g., Wallet connecti, Token Balances, Send ETH)
├── context/             # Global state management (e.g., Wallet, Balances)
├── config/              # Wallet connection configuration (e.g., wagmi, RainbowKit)
├── tests/               # Jest tests
public/                  # Static files, including index.html
.env                     # Environment variables (don't commit to GitHub)
```
---

## 💡 Value Highlights

- **Modern UX** – Animations, instant feedback, and attractive design
- **Multi-chain** – Full support for multiple EVM networks
- **Transaction History Export** – Download transactions as CSV
- **Custom Gas** – Advanced control for power users
- **Modular & Tested Code** – Easy to maintain and extend
- **Sonner Notifications** – Clear, professional user experience
- **Visual Effects** – Interactive animated particles

---

## 👨‍💻 Contributing

We welcome contributions! If you'd like to contribute, follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a pull request

Please ensure your code follows the existing style and passes the tests.

---

## 📝 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
