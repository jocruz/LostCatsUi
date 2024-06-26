# 🚀 Introduction
# Lost Cats NFT Minting DApp

## Overview
The Lost Cats NFT Minting DApp allows users to mint unique digital assets, known as NFTs (Non-Fungible Tokens), on the Solana blockchain. Built with cutting-edge technology, this DApp leverages Solana's high-speed and low-cost transactions, providing an efficient and user-friendly experience.

## Key Features
- **Solana Integration**: Utilizes Solana's blockchain for fast and low-cost NFT minting.
- **Metaplex & Candy Machine**: Powered by Metaplex's Candy Machine, offering a robust and flexible framework for NFT drops.
- **Wallet Connectivity**: Supports multiple wallets, including Phantom, Slope, Solflare, Sollet, Solong, Ledger, and SafePal, for a seamless transaction experience.
- **Responsive UI**: Ensures a smooth user experience across various devices and screen sizes.

## Technology Stack
- **React & TypeScript**: Front-end development with React for dynamic user interfaces, coupled with TypeScript for type safety.
- **Material-UI**: Utilizes Material-UI for a sleek, modern look and feel.
- **Anchor**: Leverages Anchor, a framework for Solana's Sealevel runtime, to facilitate smart contract interaction.
- **Solana Web3.js**: Direct interaction with the Solana blockchain through JavaScript.

### 🌟 Features:
- **Prod-ready Responsive UI**: Customize it easily in just 5 minutes!
- **Full Candy Machine V2 Support**: All functionalities are auto-detected and kept up-to-date:
  - Public mint (includes countdown for future dates)
  - Civic support (gatekeeper)
  - Whitelist functionality
  - Presale options
  - End date/number settings (endSettings)
  - SPL-token minting capability

![Candy Machine Preview Image](https://i.ibb.co/h7L0M3G/repo-bg.png)

### 🏦 Supported Wallets
![Supported Wallets](https://i.ibb.co/DC6Wt66/wallets.png)

📚 For setup instructions for a V2 candy machine, please refer to [Metaplex's documentation](https://docs.metaplex.com/candy-machine-v2/Introduction).

## 🖱 One-Click Vercel Deployment

Deploy the prod package instantly on Vercel with just one click! Simply customize your GitHub fork of this project and commit updates. Vercel will handle the deployment for each new commit.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2FFulgurus%2Fcandy-machine-v2-responsive-ui&env=REACT_APP_CANDY_MACHINE_ID,REACT_APP_SOLANA_NETWORK,REACT_APP_SOLANA_RPC_HOST&envDescription=Populate%20REACT_APP_CANDY_MACHINE_ID%20with%20your%20candy%20machine%20public%20key%2C%20REACT_APP_SOLANA_NETWORK%20with%20the%20solana%20network%20(devnet%2Fmainnet-beta)%20and%20REACT_APP_SOLANA_RPC_HOST%20with%20the%20RPC%20URL%20(example%20for%20devnet%20%3A%20https%3A%2F%2Fapi.devnet.solana.com)&envLink=https%3A%2F%2Fdocs.solana.com%2Fcluster%2Frpc-endpoints%23mainnet-beta&demo-title=My%20Demo%20Mint%20Page&demo-description=A%20one-click%20generated%20solana%20minting%20responsive%20website.&demo-url=https%3A%2F%2Fwww.mintgatsbyclub.net%2F&demo-image=https%3A%2F%2Fi.imgur.com%2FWWSvkBO.png)

#### 2. Define your environment variables (`.env` file)

## Getting Set Up

### Prerequisites

**REQUIRE NODEJS VERSION <= 16 (version 17 not supported)**.

* Download a Code Editor such as Visual Studio Code.

* Ensure you have both `nodejs` and `yarn` installed. `nodejs` recommended version is 16.

* Follow the instructions [here](https://docs.solana.com/cli/install-solana-cli-tools) to install the Solana Command Line Toolkit.

* Follow the instructions [here](https://hackmd.io/@levicook/HJcDneEWF) to install the Metaplex Command Line Utility.
  * Installing the Command Line Package is currently an advanced task that will be simplified eventually.

### Installation

#### 1. Fork the project & clone it. Example:

```
git clone https://github.com/Fulgurus/candy-machine-v2-responsive-ui.git
```

#### 2. Define your environment variables (.env file)

Rename the `.env.example` file at the root directory to `.env` and update the following variables in the `.env` file:

```
REACT_APP_CANDY_MACHINE_ID=__PLACEHOLDER__
```
set __PLACEHOLDER__ with the candy machine pubkey you get once you upload & create your candy machine in Metaplex project. You can find back the value from the `.cache/temp.json` file of your Metaplex project. This file is created when you run the `ts-node candy-machine-v2-cli.ts upload ...` command.

```
REACT_APP_SOLANA_NETWORK=devnet
```

This identifies the Solana network you want to connect to. Options are `devnet`, `testnet`, and `mainnet`.

```
REACT_APP_SOLANA_RPC_HOST=https://api.devnet.solana.com
```

This identifies the RPC server your web app will access the Solana network through.


If you are using a custom SPL Token to MINT, you have two additional environment parameters to set :


```
REACT_APP_SPL_TOKEN_TO_MINT_NAME=
```

Spl-token name to display next the price.

```
REACT_APP_SPL_TOKEN_TO_MINT_DECIMALS=9
```

Spl-token decimals were defined during its creation with --decimals parameter. If you didn't use that parameter, then by default your SPL Token got 9 decimals.

More info about it there : https://spl.solana.com/token

#### 3. Build the project and test. Go to the root project directory and type the commands :

To install dependencies :

```
yarn install
```

To test the app locally in the development mode (localhost:3000) :

```
yarn start
```

To build the production package (generated in build folder of the project) :

```
yarn build
```

#### 4. Customize the website UI :

##### 4.1 `App.css` : update 5 main CSS variables with your custom colors :

```
:root {
  --main-background-color: #343A50;
  --card-background-color: #804980;
  --countdown-background-color: #433765;
  --main-text-color:#F7F6F4;
  --title-text-color:#3CBA8B;
}
```

Next to that, make sure to update background image by overwriting your own background PNG file in src/img folder.

##### 4.2 `public` folder :

- Update existing demo cool cats images (cool-cats.gif, logo.png) with your owns images in project `public` folder. Make sure to name them identically.
- Add your custom website title in `index.html` : `<title>Mint Page</title>`

##### 4.3 `Home.tsx` :

Scroll down down to line 380 (`return <main> [...]`) and start to update all titles/menu/text/images/text... as wished in the whole React HTML block.

That's it ! Enjoy your beautiful candy machine :)


##  Available Commands Recap :

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

### `yarn build`


### `yarn eject`



