# anonscash-docs

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

This repository contains the technical documentation for how anons.cash works,
the flow from deposit to withdrawal, the role of zero-knowledge proofs, and the
safety model that keeps the system predictable and fully on-chain.

## What anons.cash does

• lets users deposit SOL from one wallet  
• lets them withdraw to a different wallet without exposing the link  
• verifies every withdrawal proof on-chain  
• keeps funds in user-controlled wallets at all times  
• avoids accounts, custody, and off-chain balances  

The interface provides a simple, narrow function: private transfers and clean
wallet separation on Solana.

## Documentation

Core pages:

- [Overview](docs/overview.md)  
- [How it works](docs/how-it-works.md)  
- [Wallet separation](docs/wallet-separation.md)  
- [Zero-knowledge withdrawals](docs/zk-withdrawals.md)  
- [Safety model](docs/safety-model.md)  
- [Integration](docs/integration.md)  
- [Comparisons](docs/comparisons.md)

Each document explains a single part of the system in a clear, minimal format.

## Scope and boundaries

anons.cash does not:

• hold custody of user assets  
• run accounts, profiles, or identity systems  
• mix assets or perform cross-chain routing  
• store off-chain logs or internal balances  

The system sticks to a predictable deposit–withdraw flow with fixed
denominations and on-chain verification.

## Website

https://anons.cash

