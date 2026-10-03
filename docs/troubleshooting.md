# Bounty payout troubleshooting

After a pull request is merged, find its bounty on the board. The status chip
and payout progress show whether it is waiting, queued, refused, or paid. Open
the payout details for the reason. A refusal does not undo the merge or the
bounty claim.

## The swap provider refused the amount

**What the board shows:** `payout failed`; the payout progress may say
`Maker refused the swap` and include the provider's reason.

**Why:** A Liquid payout must fit the provider's current per-swap range. The
Signet maker currently accepts 50,000–211,864 sats; providers can change their
limits. The operator console's **Routes and their limits** section shows the
current range.

**What to do:** Check the current range and ask the maintainer whether the
bounty can be adjusted or paid through another supported route. Contributors
cannot change an already-merged bounty's amount themselves.

## A per-payout cap or recipient limit was reached

**What the board shows:** `payout failed`; the payout progress gives the
policy reason, such as `Amount … is above the 150,000 sat limit per payout` or
`Recipient limit reached: … of 5 payouts in 60 min`.

**Why:** The contribution demo currently caps one payout at 150,000 sats and
limits one recipient to five payouts per hour. The live **Operator policy**
section shows the active values, which may change.

**What to do:** Contact the maintainer with the bounty and the reason shown on
the board. The maintainer must change the applicable policy or arrange another
route; retrying the same payout will not bypass a limit.

## The demo budget is exhausted

**What the board shows:** `payout failed`, with a reason such as
`Budget exhausted: … committed`.

**Why:** The contribution and game demos share a 600,000-sat budget by
default, so other demo payouts can use it first. The live **Operator policy**
section shows the active budget and usage.

**What to do:** Ask the maintainer to replenish or raise the demo budget. This
is an operator action; submitting the same bounty again will not restore the
budget.

## No payout address is registered

**What the board shows:** `waiting for address`; payout progress says
`waiting for a payout address`.

**Why:** The merge claimed the bounty, but the board has no usable address for
the pull request author.

**What to do:** Register a supported Liquid address or Lightning Address on
the bounty board using the same GitHub username that authored the merged pull
request. The board submits the waiting payout after registration. The claim
stays attached to that first merged pull request.

The contribution demo pays on Signet/Liquid testnet; its testnet rewards have
no real-money value.
