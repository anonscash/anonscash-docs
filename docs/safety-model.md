# Safety model

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

The safety model focuses on three principles:
user-controlled funds, on-chain verification, and predictable behavior.

## Non-custodial by design

• Users sign their own transactions.
• Funds are never held in a centralized service.
• There are no accounts, profiles, or internal balances.
• Withdrawals only succeed with valid, unused proofs.

Because the system does not hold custody, there is no pooled balance controlled
by an operator and no off-chain accounting that users must trust.

## On-chain verification

Every withdrawal is verified by on-chain programs. This ensures:

• proofs are checked publicly  
• double withdrawals are prevented  
• invalid claims are rejected  
• program logic cannot be bypassed  

The chain enforces correctness instead of relying on a private server or hidden
logic.

## Fixed, transparent rules

The interface uses predictable denominations and a simple deposit–withdraw
flow. There is no dynamic routing, no variable liquidity logic, and no hidden
execution path.

Users always know:

• what they are depositing  
• what they can withdraw  
• how the proof will be checked  
• that every check happens on-chain  

## No hidden state

The system does not maintain:

• user accounts  
• off-chain records  
• internal ledgers  
• behavioral profiles  

Each proof stands on its own. The program only verifies whether a claim has
already been used and whether it meets the on-chain rules.

## Operational boundaries

The interface provides:

• private deposits  
• private withdrawals  
• clean separation between funding and receiving wallets  

It does not offer:

• asset mixing  
• cross-chain obfuscation  
• custody of user funds  
• liquidity management  
• batching or relaying services  

By keeping the scope narrow, the safety model stays clean and easy to reason
about.

## Summary

anons.cash uses a minimal, transparent safety model built around
non-custodial control, on-chain verification, and zero-knowledge proofs. Users
retain ownership of their funds, the chain enforces the rules, and the
withdrawal proof removes the link between funding and receiving wallets while
preserving correctness.
