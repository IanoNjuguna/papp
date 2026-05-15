# Solidity Hardhat + Wagmi Template

A full-stack Web3 development template.

## Features

- **Smart Contract Development**: Hardhat with TypeScript and Polkadot integration
- **Frontend**: Vue.js application with Web3 connectivity
- **Modern Web3 Stack**: Wagmi, Viem, and TanStack Query for optimal DX
- **UI Components**: DaisyUI + Tailwind CSS for beautiful, responsive interfaces
- **Type Safety**: Full TypeScript support across all components
- **Development Tools**: ESLint configuration and automated contract verification

## Project Structure

``` txt
├── hardhat/              # Smart contract development environment
│   ├── contracts/        # Solidity smart contracts
│   ├── scripts/          # Deployment and interaction scripts
│   └── ignition/         # Hardhat Ignition deployment modules

└── dapp-vue/             # Vue.js frontend application
    └── src/
        ├── components/   # Vue components
        └── config/       # Contract configurations
```

## Smart Contract

The template includes a **MessageBoard** (Bulletin Board) contract that demonstrates:

- Message posting with sender tracking
- Circular buffer storage (last 8 messages)
- Message retrieval by sender or index
- Event emission for frontend integration
- Input validation and gas optimization

### Potential Use Cases

- **Decentralized Social Feeds**: Microblogging and uncensorable global chat.
- **Review & Rating Systems**: Immutable reviews tied to wallet activity.
- **Digital Guestbooks**: "Proof of attendance" registries for events or communities.
- **Decentralized Notice Boards**: DAO announcements or classifieds.
- **Basic Oracles**: Simple data feeds where authorized addresses push off-chain events to the board.

## Getting Started

### Prerequisites

- Node.js 18+
- npm, yarn, or bun package manager

### Installation

This project uses monorepo structure with workspaces. Install all dependencies from the root directory:

```bash
# Install all workspace dependencies
npm install
```

### 1. Smart Contract Development

```bash
# Deploy to Polkadot Asset Hub testnet
npm run deploy -w hardhat

# Interact with deployed contract
npm run interact -w hardhat

# Verify contract
npm run verify -w hardhat
```

Or navigate to the hardhat directory:

```bash
cd hardhat
npm run deploy
npm run interact
npm run verify
```

### 2. Frontend Development

Run the frontend application:

```bash
# From root directory
npm run dev -w dapp-vue
```

Or navigate to the frontend directory:

```bash
cd dapp-vue
npm run dev
```

## Environment Setup

Create a `.env` file in the `hardhat` directory:

```env
PRIVATE_KEY=your_private_key_here
```

## Network Configuration

The template is pre-configured for:

- **Local Development**: Hardhat network.

- **Testnet**: any EVM compatible testnet but you will need to change the RPC URL and Private Key.

## Frontend Features

The Vue application includes:

- **Wallet Connection**: Connect/disconnect Web3 wallets
- **Account Balance**: Display native token balance
- **Message Posting**: Submit messages to the smart contract
- **Message Display**: View recent messages with sender information
- **Responsive Design**: Mobile-friendly interface with DaisyUI components

## Available Scripts

You can run scripts from the root directory using the `-w` flag or navigate to the specific workspace.

### Hardhat

- `npm run deploy -w hardhat` - Deploy contracts to testnet
- `npm run interact -w hardhat` - Run interaction scripts
- `npm run verify -w hardhat` - Verify deployed contracts
- `npm run accounts -w hardhat` - Show account information
- `npm run lint -w hardhat` - Run ESLint

### Frontend (Vue)

- `npm run dev -w dapp-vue` - Start Vue dev server
- `npm run build -w dapp-vue` - Build Vue for production
- `npm run preview -w dapp-vue` - Preview Vue production build
- `npm run lint -w dapp-vue` - Run ESLint for Vue

## Technology Stack

### Smart Contracts

- **Hardhat**: Development environment and testing framework
- **Solidity**: Smart contract programming language
- **Polkadot**: Target blockchain platform
- **TypeScript**: Type-safe development

### Frontend

- **Vue 3**: Modern frontend framework
- **Wagmi**: Vue hooks for Ethereum
- **Viem**: TypeScript interface for Ethereum
- **TanStack Query**: Data fetching and caching
- **Tailwind CSS**: Utility-first CSS framework
- **DaisyUI**: Component library for Tailwind CSS

## Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License

[cc-nc-sa-4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
