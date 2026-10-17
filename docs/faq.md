# FAQ

## What is this repository for?

It demonstrates automated contribution rewards: merging a pull request that
closes a bounty issue pays its author.

## How do Lightning Address payouts work and why do they settle in seconds?

A Lightning Address looks like an email address (e.g. `user@domain.com`), but functions as an internet identifier for Bitcoin Lightning Network endpoints under the LNURL-pay (LUD-16 and LUD-06) protocol specifications:

1. **LNURL Resolution**: When a contributor reward or bounty is dispatched, the sender's client performs an HTTPS lookup at `https://domain.com/.well-known/lnurlp/user`.
2. **Metadata & Callback**: The recipient's lightning node or custodial bridge returns a JSON payload detailing the accepted minimum and maximum satoshi limits and a designated callback URL.
3. **Invoice Generation**: The sender requests a tailored BOLT11 invoice for the exact bounty amount from the callback URL.
4. **Off-Chain Routing**: The payment routes through the peer-to-peer network via Hashed Time-Locked Contracts (HTLCs) across established payment channels.

Because Lightning payments update channel balances cryptographically off-chain without waiting for on-chain Bitcoin blockchain block confirmations (which take ~10 minutes per block), the payment executes with sub-satoshi routing fees and settles definitively in seconds.
