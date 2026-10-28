# Payout States Glossary

- **received**: The payout request has been received and queued.
- **proposed**: A payout transaction has been proposed but not yet authorized.
- **authorized**: The payout has been authorized and is ready for execution.
- **resolving**: The system is resolving the destination address or payment route.
- **attempting**: The payout is being attempted (transaction broadcast or Lightning payment in flight).
- **settled**: The payout completed successfully and funds are delivered.
- **failed**: The payout failed and will not be retried automatically.
- **unknown**: The payout status could not be determined (e.g., network timeout).
- **stuck**: The payout is pending but not progressing, requiring manual intervention.
