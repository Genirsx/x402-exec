# xdefi.app

> **Cross-chain DeFi Application for x402x Protocol**

xdefi.app is a decentralized finance (DeFi) application built on top of the x402x settlement framework. It provides a user-friendly interface for cross-chain token swaps and bridges, leveraging the x402 protocol's programmable settlement capabilities.

## Purpose

This application serves as:
- **Reference Implementation**: Demonstrates how to integrate x402x protocol in a production DeFi application
- **User Interface**: Provides swap and bridge functionality with wallet connection (WalletConnect AppKit)
- **Testing Platform**: Allows users to interact with x402x settlement contracts and hooks in a real-world scenario

## Features

- 🔄 **Token Swap**: Trade tokens instantly with best-in-class UX
- 🌉 **Cross-chain Bridge**: Move assets seamlessly across networks
- 💼 **Wallet Integration**: Connect via WalletConnect AppKit (wagmi/viem)
- 🎨 **Modern UI**: Built with React, TypeScript, and shadcn/ui components
- ⚡ **Fast Development**: Powered by Vite for instant hot module replacement

## Tech Stack

- React + Vite + TypeScript
- Tailwind CSS
- [shadcn-ui](https://github.com/shadcn-ui/ui/)
- [react-router-dom](https://www.npmjs.com/package/react-router-dom)
- WalletConnect AppKit (wagmi/viem)
- @x402x/core (x402x settlement SDK)

## Getting Started

### Prerequisites

You need a WalletConnect project ID. Create one at https://cloud.walletconnect.com.

### Environment Setup

Create a `.env` file with:

```bash
VITE_WALLETCONNECT_PROJECT_ID=your_project_id_here
```

### Installation & Development

```bash
# Install dependencies
pnpm install

# Start development server
pnpm run dev
```

### Build for Production

```bash
# Build the application
pnpm run build

# Preview production build
pnpm run preview
```

## Integration with x402x

xdefi.app is tightly integrated with the x402x settlement framework:

- Uses `@x402x/core` SDK for interacting with SettlementRouter contracts
- Implements payment flows using the x402 protocol's EIP-3009 authorization
- Supports facilitator fees and custom hooks for programmable settlements
- Demonstrates real-world usage of TransferHook, NFTMintHook, and RewardHook

For more information about x402x protocol, see the [main README](../../README.md).

## Project Structure

```md
xdefi-app/
├── public/            # Public assets
├── src/               # Application source code
│   ├── components/    # React components (UI components, swap, bridge)
│   ├── contexts/      # React contexts (Theme, Web3)
│   ├── config/        # App configuration
│   ├── hooks/         # Custom React hooks
│   ├── lib/           # Utility functions
│   ├── pages/         # Page components (Swap, Bridge, FAQ)
│   ├── App.tsx        # Application entry point
│   ├── index.css      # Main CSS and Tailwind configuration
│   ├── main.tsx       # Main rendering file
│   └── Router.tsx     # Routes component
├── index.html         # HTML entry point
├── tsconfig.json      # TypeScript configuration
└── vite.config.ts     # Vite configuration
```

## Related Projects

This app is part of the x402-exec monorepo:
- **SettlementRouter**: Core settlement contracts (see [contracts/](../../contracts/))
- **Facilitator**: Backend service for processing payments (see [facilitator/](../../facilitator/))
- **Showcase**: Full-stack demo application (see [examples/showcase/](../../examples/showcase/))

## License

This project is licensed under the Apache-2.0 License. See the [LICENSE](LICENSE) file for details.
