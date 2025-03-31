# Lost Cats NFT Minting DApp

## Project Overview

The Lost Cats NFT Minting DApp provides a streamlined platform for users to create and mint unique digital assets (NFTs) on the Solana blockchain. Leveraging Solana’s high-speed, low-cost transaction capabilities, the application ensures an efficient and accessible user experience.

## Key Features

- **Solana Blockchain Integration**: Rapid, cost-effective NFT minting using Solana's blockchain technology.
- **Metaplex Candy Machine Support**: Utilizes the robust Metaplex Candy Machine framework for comprehensive NFT management.
- **Wallet Connectivity**: Compatible with a wide range of wallets including Phantom, Slope, Solflare, Sollet, Solong, Ledger, and SafePal.
- **Responsive User Interface**: Ensures seamless usability across various devices and screen sizes.
- **Advanced NFT Minting Capabilities**:
  - Public minting with countdown timer
  - Whitelist and presale functionalities
  - Civic gatekeeper integration
  - SPL-token minting support

![Candy Machine Preview Image](https://i.ibb.co/h7L0M3G/repo-bg.png)

## Supported Wallets

![Supported Wallets](https://i.ibb.co/DC6Wt66/wallets.png)

For detailed setup instructions for Metaplex Candy Machine V2, refer to [Metaplex's documentation](https://docs.metaplex.com/candy-machine-v2/Introduction).

## Quick Deployment (Vercel)

Deploy instantly on Vercel by forking this repository and customizing your deployment through commits.

[Deploy with Vercel](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FFulgurus%2Fcandy-machine-v2-responsive-ui&env=REACT_APP_CANDY_MACHINE_ID,REACT_APP_SOLANA_NETWORK,REACT_APP_SOLANA_RPC_HOST&envDescription=Populate%20REACT_APP_CANDY_MACHINE_ID%20with%20your%20candy%20machine%20public%20key%2C%20REACT_APP_SOLANA_NETWORK%20with%20the%20solana%20network%20(devnet%2Fmainnet-beta)%20and%20REACT_APP_SOLANA_RPC_HOST%20with%20the%20RPC%20URL%20(example%20for%20devnet%20%3A%20https%3A%2F%2Fapi.devnet.solana.com)&envLink=https%3A%2F%2Fdocs.solana.com%2Fcluster%2Frpc-endpoints%23mainnet-beta&demo-title=My%20Demo%20Mint%20Page&demo-description=A%20one-click%20generated%20solana%20minting%20responsive%20website.&demo-url=https%3A%2F%2Fwww.mintgatsbyclub.net%2F&demo-image=https%3A%2F%2Fi.imgur.com%2FWWSvkBO.png)

## Setup Instructions

### Prerequisites

- Node.js (v16 or lower recommended)
- Yarn package manager
- Visual Studio Code (or any suitable code editor)
- Solana CLI toolkit ([Installation Guide](https://docs.solana.com/cli/install-solana-cli-tools))
- Metaplex CLI ([Installation Guide](https://hackmd.io/@levicook/HJcDneEWF))

### Installation Steps

1. **Clone Repository**:

```bash
git clone https://github.com/Fulgurus/candy-machine-v2-responsive-ui.git
cd candy-machine-v2-responsive-ui
```

2. **Configure Environment Variables**:

Rename `.env.example` to `.env` and set:

```
REACT_APP_CANDY_MACHINE_ID=your_candy_machine_pubkey
REACT_APP_SOLANA_NETWORK=devnet
REACT_APP_SOLANA_RPC_HOST=https://api.devnet.solana.com

# Optional SPL Token Settings
REACT_APP_SPL_TOKEN_TO_MINT_NAME=token_name
REACT_APP_SPL_TOKEN_TO_MINT_DECIMALS=9
```

3. **Install Dependencies and Run the Application**:

- Install dependencies:

```bash
yarn install
```

- Start the development server:

```bash
yarn start
```

- Build for production:

```bash
yarn build
```

4. **Customize UI**:

- Update CSS variables in `App.css`:

```css
:root {
  --main-background-color: #343A50;
  --card-background-color: #804980;
  --countdown-background-color: #433765;
  --main-text-color: #F7F6F4;
  --title-text-color: #3CBA8B;
}
```

- Replace demo images and edit website title in `public/index.html`.

- Modify UI elements in `Home.tsx` as needed.

## Available Commands

- **Development Mode**:

```bash
yarn start
```

- **Testing**:

```bash
yarn test
```

- **Production Build**:

```bash
yarn build
```
