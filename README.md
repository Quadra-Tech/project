# QuadraTech - Next-Gen Quadratic Funding

**QuadraTech is the next-gen quadratic funding engine.** Built on Enclave E3, it keeps votes and donations encrypted while publishing verifiable results, fair by design, bribery-resistant, and more powerful than MACI. Private votes. Public trust and decentralized.

## 🚀 Quick Start

Get QuadraTech running in 3 simple steps:

### 1. Install Dependencies
```bash
pnpm install
```

### 2. Setup Development Environment
```bash
pnpm dev:setup
```
This command will:
- Build all necessary containers
- Compile smart contracts
- Prepare ZK circuits
- Set up the development infrastructure

### 3. Start All Services
```bash
pnpm dev:up
```
This will launch:
- **Anvil** (local blockchain)
- **Ciphernodes** (encryption network)
- **QuadraTech Server** (backend API)
- **QuadraTech Client** (web interface at http://localhost:3000)

### 4. Interact via CLI
```bash
pnpm cli
```
Use the CLI to:
- Initialize new funding rounds
- Decrypt and publish results
- Manage the system

## 🎯 How to Use

1. **Open your browser** → Navigate to `http://localhost:3000`

2. **Connect your wallet** → Add Anvil's private key to MetaMask:
   ```
   0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80
   ```

3. **Switch to Anvil network** → The app will prompt you to switch networks

4. **Create a new round** → Run `pnpm cli` in a terminal and select "Initialize new E3 round"

5. **Participate** → Vote and contribute to funding rounds through the web interface

6. **View results** → After a round ends, decrypt results via CLI to see encrypted votes revealed

## 📁 Project Structure

```
QuadraTech/
├── client/                  # React frontend application
├── server/                  # Rust backend server
├── program/                 # RISC Zero computation program
├── contracts/               # Smart contracts (Solidity)
├── circuits/                # Noir circuits for ZK proofs
├── scripts/                 # Development utilities
└── enclave.config.yaml      # Ciphernode configuration
```

## 🛠️ Prerequisites

Before getting started, install:

- [Rust](https://rust-lang.org/tools/install/)
- [Foundry](https://getfoundry.sh)
- [RISC Zero](https://dev.risczero.com/api/zkvm/install)
- [Node.js](https://nodejs.org/en/download)
- [pnpm](https://pnpm.io)
- [MetaMask](https://metamask.io)

### Quick Install

```bash
# Install Rust
curl https://sh.rustup.rs -sSf | sh

# Install Foundry
curl -L https://foundry.paradigm.xyz | bash

# Install RISC Zero
curl -L https://risczero.com/install | bash
rzup install cargo-risczero

# Install pnpm
npm install -g pnpm
```

## 🧹 Clean Up

To remove all build artifacts and start fresh:

```bash
# From the enclave root directory
cd ../../
pnpm clean
```

## 🔑 Key Features

- **🔒 Encrypted Votes** → All votes remain encrypted using FHE (Fully Homomorphic Encryption)
- **✅ Verifiable Results** → ZK proofs ensure computation correctness without revealing individual votes
- **🛡️ Bribery-Resistant** → Impossible to prove how you voted, preventing coercion
- **⚖️ Quadratic Funding** → Democratic funding allocation that amplifies small donors
- **🌐 Decentralized** → No single point of failure or trust

## 📚 Advanced Usage

### Manual Server Start

```bash
cd server
cargo run --bin server
```

### Manual Client Start

```bash
cd client
pnpm dev
```

### Run Ciphernodes

```bash
./scripts/dev_cipher.sh
```

## 🐛 Troubleshooting

**Votes not showing in Historic polls?**
- Make sure the round has ended (check expiration time)
- Run `pnpm cli` and select "Decrypt and publish result"
- The votes need to be decrypted before they appear

**Services not starting?**
- Run `pnpm clean` from the enclave root
- Delete `node_modules` and run `pnpm install` again
- Make sure ports 3000, 4000, and 8545 are available

## 📄 License

This project is licensed under the LGPL-3.0+ license.

## 🤝 Contributing

Contributions are welcome! Please read the [Contributor License Agreement](https://github.com/gnosisguild/CLA) before submitting.

---

**Built with [Enclave Protocol](https://enclave.gg)** | Encrypted Execution Environments for Web3
