# FAQ

## What is this repository for?

It demonstrates automated contribution rewards: merging a pull request that
closes a bounty issue pays its author.

## What happens if two pull requests close the same issue, or GitHub sends the merge webhook twice?

Only the first merged pull request to claim the bounty is paid. When a later
merged pull request closes the same issue, the board sees that the issue
already has a claim and skips another payout.

If GitHub resends a merge webhook, the saved claim prevents the issue from
being claimed again. Paycue also submits a payout with a stable obligation key
for that repository and issue, so retrying the same bounty cannot create a
second payment.
