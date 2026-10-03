# Paycue bounty demo

[English](README.md) | **Italiano**

Questo repository è l'ambiente dimostrativo del **Paycue contribution reward demo**.
Le issue con l'etichetta `bounty: <sats>` vengono pagate automaticamente quando
viene unita una pull request che le chiude. Solo Signet/testnet: nessun denaro
reale.

## Come richiedere una bounty

1. Scegli una issue aperta con l'etichetta `bounty: …`.
2. Registra il tuo nome utente GitHub e un indirizzo di pagamento sulla
   bacheca del progetto: un indirizzo Liquid testnet (`tlq1…`) riceve L-USDT
   tramite KaleidoSwap; un Lightning Address riceve sats.
3. Apri una pull request la cui descrizione contenga `Closes #<issue>`.
   Facoltativo: aggiungi una riga `Payout: <address>` per usare un indirizzo
   diverso da quello registrato.
4. Quando un maintainer la unisce, il pagamento parte entro pochi secondi.
   Puoi seguirne lo stato sulla bacheca.

Ogni bounty associata a un'issue viene pagata una sola volta: il pagamento va
all'autore della prima pull request che viene unita.
