# Payout states

These states describe a bounty payout's progress, not whether a testnet reward has real-money value.

- `received` — Paycue has recorded a qualifying event and created the payout obligation.
- `proposed` — The payout is awaiting policy evaluation and has not yet been authorized.
- `authorized` — Policy approved the payout, and its amount is reserved for this obligation.
- `resolving` — Paycue is resolving the recipient into a payment destination, such as a Lightning invoice.
- `attempting` — Paycue has submitted the payment to the provider and is waiting for a definitive result.
- `settled` — The payment provider confirmed that the payment completed.
- `failed` — The payout reached a definitive failure and will not proceed automatically.
- `unknown` — Paycue cannot yet determine the payment outcome and must reconcile the existing attempt before deciding what to do.
- `stuck` — The payment cannot be retried safely without intervention, so it needs manual review.
