The Irys CLI is a simple command-line tool for interacting with Irys. This guide covers setup on ETH Sepolia testnet to fund your wallet, check balance, and upload files with permanent storage.

# ♻ Irys CLI - Easy Setup Guide
---

## 📌 Part 1 – Introduction & Requirements

*Requirements:*

- Ubuntu (20.04 / 22.04 / 24.04)  
- 4GB RAM minimum  
- 10–20GB SSD  
- Burner wallet (never use your main wallet!)  
- ETH Sepolia testnet RPC (from [Chainlist](https://chainlist.org))  
- ETH Sepolia faucet (get free tokens from [Alchemy Faucet](https://sepoliafaucet.com))  

---

## ⚡ Part 2 – Installation Steps

### Step 1: Install Dependencies
```bash
sudo apt-get update && sudo apt-get upgrade -y
```
```bash
sudo apt install curl iptables build-essential git wget lz4 jq make protobuf-compiler cmake gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev screen ufw -y
```

### Step 2: Install Node.js & npm

For Linux (Ubuntu):
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - && sudo apt install -y nodejs
```
For Mac:
```bash
brew install node
```
Check version:
```bash
node -v
npm -v
```

### Step 3: Install IRYS CLI
```bash
sudo npm i -g @irys/cli
```
Verify Installation:
```bash
irys
```

---

## ⚡ Part 3 – Fund Wallet, Check Balance & Upload File

### Step 4: Fund Your Wallet
```bash
irys fund 2000000 \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --provider-url https://1rpc.io/sepolia
```
• Replace PRIVATE_KEY with your own key (put it without 0x & must use burner wallet)

• Amount 2000000 is in wei


### Step 5: Check Balance
```bash
irys balance WALLET_ADDRESS \
  -n devnet \
  -t ethereum \
  -w Private_Key \
  --provider-url https://1rpc.io/sepolia
```
Replace WALLET_ADDRESS  with your own address


### Step 6: Upload File

1. Move any test image/video (e.g., test.png) into Ubuntu’s home or root folder.

2. Verify it exists:
```bash
ls -a
```
3. Upload:
```bash
irys upload FILE_NAME \
  -n devnet \
  -t ethereum \
  -w PRIVATE_KEY \
  --tags FILE_NAME FILE_FORMAT \
  --provider-url https://1rpc.io/sepolia
```
• Replace FILE_NAME with its actual one:
• Replace PRIVATE_KEY with your own key
• Replace FILE_NAME & FILE_FORMAT (JPG,PNG)






YOU ARE GOOD TO GO

                                            BYE CUTIESSSS <3  









