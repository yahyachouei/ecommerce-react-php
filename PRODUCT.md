# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Assumption from the supplied brief: Moroccan electronics shoppers and PC builders comparing parts, TVs, and accessories in MAD.

## Product Purpose

An online electronics storefront for discovering and comparing computer components and televisions, configuring a compatible PC build, and placing or tracking an order.

## Positioning

The requested experience brings PC-part discovery, a socket-aware build planner, television shopping, and customer-service paths together in one storefront.

## Capabilities and Constraints

The product catalog is initialized from `data/products.json` into a SQLite database and can be managed through a credential-protected admin panel at `/admin`. Cart, wishlist, comparison, theme and demo orders use browser storage. This remains a demonstration, not a connected inventory, payment, customer identity, or order-management service. Card and cash-on-delivery selections are checkout demonstrations and must not collect or transmit payment credentials. Prices and stock are illustrative MAD sample data.

Owner credentials and a signing secret must be configured in local environment variables; no default credentials are shipped. The owner can create staff accounts from `/admin`; staff can manage products, while only the owner can manage accounts. Staff passwords use one-way hashes, and online presence is based on an admin-page heartbeat within 75 seconds. The SQLite database requires writable persistent local storage when deployed.

## Brand Commitments

The user requested a clean, premium, technology-focused identity, dark mode by default with a light-mode toggle, a bold electric-blue or violet accent, responsive layouts, modern sans-serif typography, generous spacing, rounded cards, subtle shadows, and smooth hover animations. Store name and tagline are open for this implementation to choose.

## Evidence on Hand

No real catalog, customer reviews, business contact details, policies, or brand assets were supplied. Product records, ratings, reviews, and contact examples in the first version are synthetic demonstration content and must be replaced with verified business information before launch.

## Product Principles

- Keep shopping, comparison, and PC building understandable.
- Show the important details needed to choose electronics.
- Make cart and wishlist state useful across visits on one browser.
- Clearly distinguish local demonstration behavior from live commerce services.
