# Overview

anons.cash is a non-custodial Solana transfer interface that provides clean
wallet separation and private withdrawals using zero-knowledge proofs.

Users deposit SOL from one wallet and later withdraw to a different wallet
without exposing the link between them. The withdrawal proof shows the user has
a valid claim in the pool while keeping the original deposit address private.
Verification happens entirely on-chain.

Funds stay in user-controlled wallets at all times. There are no accounts, no
off-chain balances, and no custodial exposure. The design supports simple,
practical wallet separation for private transfers on Solana.
