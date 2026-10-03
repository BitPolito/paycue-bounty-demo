# FAQ

## What is this repository for?

It demonstrates automated contribution rewards: merging a pull request that
closes a bounty issue pays its author.

## Can I be paid to a Lightning Address?

Yes. A Lightning Address such as `name@domain` can receive sats. Paycue looks
up the address through LNURL-pay, obtains an invoice, and pays it over the
Lightning Network. Because the payment settles over Lightning rather than
waiting for an on-chain block confirmation, the route is designed to settle
in seconds. The receiver's service and network availability can affect the
actual time, and the receiver's LNURL-pay service sets its accepted amount
range.

This bounty demo is testnet-only; its rewards have no real-money value.
