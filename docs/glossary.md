# Payout states glossary

Payouts move through these states in order:

- `received` — The payout request has been received and recorded by the system.
- `proposed` — A payout has been proposed and is awaiting authorization.
- `authorized` — The payout has been approved/authorized for execution.
- `resolving` — The system is resolving the destination or route details needed to send the payout.
- `attempting` — A payout attempt is currently in progress.
- `settled` — The payout completed successfully and funds have been settled.
- `failed` — The payout attempt failed and did not settle successfully.
- `unknown` — The current payout state cannot be determined yet.
- `stuck` — The payout is not progressing and requires attention/intervention.
