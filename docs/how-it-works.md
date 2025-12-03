# How it works

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

The system has two simple stages: deposit and withdrawal. Both are handled
through on-chain programs, and users stay in control of their funds at every
step.

## 1. Deposit

A user deposits a fixed amount of SOL into the pool from any wallet they
choose. The deposit creates an entry in the pool that can later be withdrawn
using a proof. The deposit transaction is on-chain and visible like any other
Solana transfer.

What the deposit does not reveal is the identity of the future withdrawal
wallet. Deposits only confirm that the user has contributed to the pool and
has a claim they can exercise later.

## 2. Generate a withdrawal proof

When the user wants to withdraw, they generate a zero-knowledge proof. The
proof shows two things:

• they have a valid, unused claim in the pool  
• they are not attempting to withdraw more than once  

The proof does not reveal which deposit belongs to the user. It only proves
that a legitimate claim exists.

## 3. Withdraw to any wallet

The user submits the proof along with the withdrawal transaction. The on-chain
program verifies the proof and then releases the funds to the withdrawal
wallet.

Because the proof hides which deposit is being used, there is no visible link
between the funding wallet and the receiving wallet.

## Key properties

• Users stay non-custodial, signing every transaction themselves  
• There are no accounts, profiles, or off-chain balances  
• Verification is handled entirely by on-chain programs  
• The funding and receiving wallets cannot be linked through transaction flow  
• Only valid, unused proofs are accepted, preventing double withdrawals  

## Summary

anons.cash provides a simple, predictable flow: deposit from one wallet, then
withdraw to another with a
