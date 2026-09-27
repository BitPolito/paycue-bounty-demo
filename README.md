# Payhook bounty demo

This repository is the playground for the **Payhook contribution reward demo**.
Issues labelled `bounty: <sats>` are paid automatically when a pull request
that closes them is merged. Signet/testnet only: no real money.

## How to claim a bounty

1. Pick an open issue with a `bounty: …` label.
2. Register your GitHub username and a payout address on the demo's bounty
   board: a Liquid testnet address (`tlq1…`) receives L-USDT through
   KaleidoSwap; a Lightning Address receives sats.
3. Open a pull request whose description contains `Closes #<issue>`.
   Optional: add a line `Payout: <address>` to override your registered address.
4. When a maintainer merges it, the payout starts within seconds. Watch it on
   the bounty board.

One payout per bounty issue, whoever merges first.
