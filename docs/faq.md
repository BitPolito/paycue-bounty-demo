# FAQ

## What is this repository for?

It demonstrates automated contribution rewards: merging a pull request that
closes a bounty issue pays its author.

## How can contributors receive a reward as L-USDT on Liquid testnet?

For this demo, a merged pull request that closes a bounty issue can pay the
author in **L-USDT on Liquid testnet** (via KaleidoSwap on the demo bounty
board). Testnet funds have no real-world value.

### What a Liquid testnet address looks like

Use a **Liquid testnet** address that starts with `tlq1` (confidential /
blech32). Example shape:

```
tlq1qq…example…only
```

Do not use:

- a Liquid **mainnet** address (`lq1…` / `ex1…`)
- an unconfidential Liquid testnet bech32 alone when the board expects `tlq1…`
  (`tex1…` is a different encoding)
- a Lightning invoice or Lightning Address (those are for the sats rail)

### How to register the payout address

1. Register your GitHub username and a `tlq1…` payout address on the demo's
   bounty board **before** the pull request is merged, **or**
2. Override for a single bounty by adding this line to the pull request
   description:

```
Payout: tlq1…your-own-liquid-testnet-address
```

Always use an address you control. Do not paste another contributor's address
or a docs example.

### Quick checklist

- Address starts with `tlq1` (Liquid testnet)
- Registered on the bounty board **or** `Payout:` is in the PR description
- PR description also includes `Closes #<issue>` so the merge matches the bounty
- One payout per bounty issue (first merged PR wins)
