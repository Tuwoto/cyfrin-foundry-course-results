# Foundry Course

This repo is the conclusion of my results after completing Cyfrin Updraft’s **Foundry fundamentals** course. 

---

## Quick overview
- **Course focus:** Foundry toolchain (forge, anvil, cast), scripting deployments, local deployment, verifying contracts on Etherscan, and private key handling for deployments.  
- **Why I chose this course:** Foundry is a modern, fast, Solidity-native framework, widely used by developers.

## Course link
- Foundry fundamentals — Cyfrin Updraft: https://updraft.cyfrin.io/courses/foundry

## What I built (files)
- `foundry.toml` — project configuration for Foundry.  
- `script/DeployScript.s.sol` — deployment script(s) for local and Sepolia deployment.   
- `src/` —  Solidity contracts.
- `broadcast/` Local deployment broadcast logs.

## Key Foundry commands I learned (some notable examples)
```bash
# installing foundry
# curl -L https://foundry.paradigm.xyz | bash

# running a local node (anvil)
anvil

# build
forge build

# running a deployment script locally
forge script script/DeployContratc.s.sol --broadcast --private-key $PRIVATE_KEY --rpc-url $RPC_URL

# deploying to Sepolia
forge script script/DeployContract.s.sol --rpc-url $SEPOLIA_RPC_URL --broadcast --private-key $PRIVATE_KEY

# interacting with the contract inside Foundry
cast send <address> "store(uint256)" value --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY

cast call <address> "retrieve()(uint256)" --rpc-url $SEPOLIA_RPC_URL

# how to use encrypted private keys in Foundry
cast wallet import defaultKey --interactive

```

## Private key & security practices
I vowed to never use my real private keys associated with real money in plain text or .env file. Instead, I'll use the command line to pass private keys or, betterm use the encryption methods like keystore. 

P.S.: files here contain dummy keys only.

## Deployment 
- Foundry-deployed contract on Sepolia: `0x3be76412fa7cb14c9f861d2df0e468a2d5fc98ec`
- Link on Etherscan: https://sepolia.etherscan.io/address/0x3be76412fa7cb14c9f861d2df0e468a2d5fc98ec.

## What I learned beyond Solidity
- How to structure a repo.  
- How to automate deployments and verification from a script.  
- Using Copilot inside VS Code to speed up boilerplate.
- Where to go for information and how to use AI in the best way to assist for dev needs.
- Private key security practices & encryption methods.
- How to use GitHub and push repos to GitHub from local host.

---