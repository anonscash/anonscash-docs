# Zero-knowledge withdrawals

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

Zero-knowledge withdrawals are the core mechanism that breaks the link between
a user’s deposit wallet and their withdrawal wallet. The proof shows the user
has a valid, unused claim in the pool without revealing which deposit belongs
to them.

## What the proof demonstrates

A zero-knowledge withdrawal proof confirms:

• the user made a deposit of the required denomination  
• the deposit has not already been used for a withdrawal  
• the user is entitled to withdraw exactly once  

It does not reveal:

• the deposit address  
• the time the deposit was made  
• the user’s identity  
• the link between the funding and receiving wallets  

The proof replaces the direct transfer path that would normally tie the two
wallets together on-chain.

## How the withdrawal works

1. The user generates a zero-knowledge proof locally.  
2. The proof commits to a valid deposit without revealing which one.  
3. The proof is submitted with the withdrawal transaction.  
4. The on-chain program verifies the proof.  
5. If valid, funds are released to the withdrawal wallet.  

This sequence provides privacy without introducing custody or off-chain
balance tracking.

## Wh
