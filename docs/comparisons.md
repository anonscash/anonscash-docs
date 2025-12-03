# Comparisons

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

This page outlines the main categories of privacy approaches on Solana and how
anons.cash fits into them. The goal is to give users and developers a simple,
accurate frame of reference.

## 1. Direct transfers

Direct transfers are the default on Solana. They are transparent and link the
sender and receiver immediately. Even if wallets rotate, the funding path
remains public.

Direct transfers offer:

• full transparency  
• no privacy layer  
• permanent linking of funding and receiving wallets  

## 2. Centralized mixers or custodial services

Some services pool user funds and redistribute them manually. These usually
require users to give up custody, trust an operator, or interact with off-chain
logic.

Characteristics:

• user funds held by a central party  
• private off-chain accounting  
• users rely on the operator to process withdrawals  
• increased regulatory exposure  

These systems do not match the goals of anons.cash.

## 3. Cross-chain obfuscation tools

Cross-chain routes can make tracing harder by moving assets across multiple
chains. This increases complexity and operational risk, and often depends on
trusted bridges.

Characteristics:

• higher complexity  
• new attack surfaces  
• potential custody or bridge risks  
• inconsistent privacy results  

anons.cash does not use cross-chain flows.

## 4. Non-custodial pooled withdrawals with zero-knowledge proo
