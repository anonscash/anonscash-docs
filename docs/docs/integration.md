# Integration

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

This page explains how anons.cash fits into the Solana ecosystem and how the
interface can be integrated into external tools, bots, or services.

## High-level structure

anons.cash consists of:

• an on-chain program that verifies zero-knowledge withdrawal proofs  
• a client-side flow that handles proof generation  
• a simple UI layer for deposits and withdrawals  

The deposit and withdrawal logic is exposed through standard Solana
transactions. Developers can integrate with the flow by interacting with the
same on-chain instructions used by the interface.

## Integration goals

Integrations usually aim to:

• deposit from a controlled wallet  
• generate a withdrawal proof in a secure environment  
• withdraw to a target wallet without exposing links  
• embed the deposit or withdrawal steps into an existing workflow  

This allows services to offer private funding paths without taking custody of
user assets.

## Proof generation

Zero-knowledge proofs are generated client-side. The proof confirms that a
valid deposit exists and has not been spent. It does not reveal the deposit
wallet.

Developers can run the proof generation logic:

• inside a backend environment  
• inside a secure client environment  
• inside a bot or automated workflow  

The proof remains local until it is submitted along with the withdrawal
transaction.

## On-chain interaction

Integrators interact with two primary actions:

1. **Deposit:**  
   Send a transaction to the deposit instruction with the fixed denomination.

2. **Withdraw:**  
   Submit a withdrawal instruction containing the zero-knowledge proof.

The on-chain program verifies the proof and enforces that each claim is used
once. There is no additional state to manage.

## No accounts or custody

Integration does not require:

• registering users  
• creating accounts  
• maintaining internal balances  
• holding user funds  
• storing off-chain logs  

The interface is stateless beyond verifying whether a claim has been used.

## Typical use cases

Services integrate anons.cash to:

• provide private funding for bots  
• separate operational wallets from public-facing wallets  
• allow users to rotate receiving addresses safely  
• enable clean wal
