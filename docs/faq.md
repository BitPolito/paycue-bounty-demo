# FAQ

## What is this repository for?

It demonstrates automated contribution rewards: merging a pull request that
closes a bounty issue pays its author.

## How can contributors receive a reward as L-USDT on Liquid testnet?

For this demo, contributors can receive their reward as L-USDT on the Liquid
(testnet) network. Register a Liquid testnet payout address on the bounty
board before the pull request is merged, or include a `Payout: <address>` line
in the pull request description to use a different address for that bounty.

A Liquid testnet address starts with `tlq1` (for example,
`tlq1…`). This is distinct from a mainnet Liquid address and from a Lightning
invoice or Lightning Address. The demo uses testnet funds, so the payout has
no real-world value.
