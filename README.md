# Khedmti MVP 0.1

A bilingual Arabic/French clickable prototype for a home-services marketplace in Morocco.

## Run locally
- Open `index.html` in a browser to try the basic prototype.
- For installable PWA/offline service worker support, serve this folder over HTTPS or localhost, e.g. `python3 -m http.server 8000`, then visit `http://localhost:8000`.

## Prototype features
- Arabic/French language toggle and RTL/LTR layout
- Customer/worker role toggle
- Service categories, request creation, worker offers, customer selection, completion confirmation
- Demo wallet, simulated top-up review and transaction history
- Local browser storage

## Important limitations
This is a UI/flow prototype only. It is **not ready for real users or store submission**. Data is stored locally in the browser and is not shared between users/devices. There is no real authentication, SMS verification, server database, secure admin, payment integration, location matching, push notifications, or robust dispute handling. Wallet balances and commissions are simulated; do not accept real payments or rely on this prototype for actual billing.

## Suggested next implementation phase
1. Create a Supabase project and tables for profiles, service_requests, offers, wallets, wallet_transactions, and completion confirmations.
2. Enforce all wallet changes server-side via secure database functions/transactions; clients must never write balances directly.
3. Add authentication, phone verification, role-based row-level security, admin-only top-up approval, audit logs, and dispute flow.
4. Test with a small group of workers and clients before store release.
