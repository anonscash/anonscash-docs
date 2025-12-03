# Wallet separation

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

Wallet separation means using different wallets for funding, receiving, and
operating on-chain without creating visible links between them. On Solana, this
is difficult by default because every transfer is public and easily traced.

anons.cash solves this by breaking the direct link between the wallet that
deposits and the wallet that withdraws. The withdrawal proof confirms the user
has a valid claim in the pool but does not reveal which deposit belongs to
them.

## Why wallet separation matters

Solana activity is transparent. Without a separation step:

• personal wallets link to public identities  
• trading wallets link to funding sources  
• team, treasury, and personal wallets become entangled  
• rotating addresses does not hide the funding path  

Once funding links exist, they are permanent on-chain.

## How anons.cash implements wallet separation

1. A user deposits from a funding wallet.  
2. Later, they withdraw to a receiving wallet, using a proof instead of a
   direct transfer.  
3. The public chain shows a deposit and a withdrawal but does not show that
   they belong to the same user.  
4. The withdrawal wallet has no visible connection to the funding wallet.  

This creates clean separation betw
