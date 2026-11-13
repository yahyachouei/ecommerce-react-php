# Volt Market

A responsive electronics storefront demo for PC parts, televisions and accessories. The initial 26-product catalog in `data/products.json` seeds a SQLite database (`data/volt-market.sqlite`) on first run. Product changes made in the admin panel are stored in SQLite; cart, wishlist, comparison, theme and demo orders are stored in the current browser.

## Run locally

1. Install Node.js 20.9 or newer.
2. In this folder run `npm install`.
3. Start the development server with `npm run dev`.
4. Open the local URL printed by Next.js (usually `http://localhost:3000`).

Use `npm run typecheck` and `npm run build` to check the project.

## Product admin

1. Copy `.env.example` to `.env.local` and fill in all three values.
2. Set a private username and a unique password with at least 12 characters. Set `ADMIN_SESSION_SECRET` to a random secret of at least 32 characters; for example, generate one with `node -e "console.log(require('node:crypto').randomBytes(32).toString('hex'))"`.
3. Restart the app and open `/admin`. Sign in with the environment-configured owner credentials. In **Team access**, create staff usernames and passwords; staff can manage products, while only the owner can add or remove staff accounts.

Staff passwords are stored as one-way scrypt hashes and cannot be viewed again. Share the credentials privately. The team page reports a user as online while their signed-in admin page has checked in during the last 75 seconds; otherwise it shows their last activity. Removing a staff account revokes their active sessions.

The SQLite database is created and seeded automatically on the first request. Back up `data/volt-market.sqlite` to retain product edits and staff accounts. For hosting, set `VOLT_DATABASE_PATH` to a writable persistent volume: SQLite requires a local persistent disk and is not suitable for ephemeral/serverless filesystems.

## Demo boundaries

All prices, availability, ratings and reviews are sample data in MAD. Checkout stores an illustrative order in local browser storage; it does not take payment, reserve inventory, send an order to a store, or require a real account. The card option is a payment-method selection only and never asks for card details. Replace the sample content and contact details before a real launch.

The admin panel has owner and staff access levels for catalog management; team accounts and presence are local to the SQLite database. It does not turn the sample checkout into a real payment or order system.

## Main routes

`/` home · `/category/GPUs` catalog · `/product/gpu-geforce-rtx-4070-super` product · `/cart` · `/checkout` · `/pc-builder` · `/compare` · `/wishlist` · `/account` · `/track-order` · `/contact` · `/about` · `/faq` · `/warranty` · `/admin`
