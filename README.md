# Skyfire Homepage Prototype

A self-contained, single-file marketing prototype for **Skyfire** — verified identity and payment credentials for AI agents.

Modeled on the production design system at [skyfire.xyz](https://skyfire.xyz): Geist + Inter typography, ink/red/teal/orange palette, pill buttons, and the same proportions used on the live site.

## Run it

The page is one file with everything inlined (assets, icons, animations). To preview:

- **Just open it**: double-click `index.html`. It renders identically from `file://` — brand SVGs and Material Symbols icons are embedded as inline data; only Google Fonts loads from the network.
- **Or serve it locally**: any static server works. Examples:
  ```bash
  npx serve .
  # or
  python3 -m http.server 8000
  ```

## What's on the page

- **Sticky nav** — Skyfire wordmark + nav items, "Launch Skyfire" CTA right-aligned, matching the live site's header dimensions
- **Hero** — "Access. Identity. Checkout. The Agent Trust Stack." with a stacked SVG diagram on the right:
  - Skyfire (Agent Wallet) → Agent → Security bar → Websites / Login / Checkout
  - Brand partner logos scroll horizontally through the Security bar (auto, seamless loop)
  - Material Symbols icons inside each destination (`smart_toy`, `public`, `key`, `shopping_cart`)
  - Animated KYA token pills on every flow arrow
- **What KYA Powers** — two-card section (Access & Login, Checkout & Payments) with an auto-scrolling chip ticker for partner names (hover to pause)
- **Coverage band** — "Covering more than 60% of the Web" with 11 partner wordmarks in a centered 6 + 5 grid (Akamai, DataDome, Cequence, F5, Fastly, Imperva, HUMAN Security, Okta, Auth0, Ory, Forter)
- **One unified trust stack** — three-product table (Know Your Agent, Agentic Wallet, Buy for Me)
- **Enable Agent Access at Internet Scale** — dark card with a parallel stacked SVG diagram (User + Skyfire → Agent → Security → Websites / APIs / Agent Protocols)
- **Live walkthrough demo** — animated 4-step pipeline (Token Request → Website Login → Checkout → Live Transaction) driving a live ledger of agent transactions
- **Footer** — dark, three columns

## Tech notes

- **One file**, no build step, no framework. Vanilla HTML + CSS + a small amount of JS for the demo animation and scroll-reveal observer.
- **All SVGs are inlined** (either as inline `<svg>` markup or as base64 data URIs) so the file is portable and `file://` safe.
- **Material Symbols icons** are inlined as SVG `<path>` data — no web-font dependency for the diagram icons.
- **External dependencies**: only Google Fonts (Inter, Geist, JetBrains Mono) loaded over the network.

## Editing

The hero copy lives in the `<header class="hero">` block. The two SVG diagrams (hero + access card) are inline — search for `class="hero-svg"` and `class="access-svg"`. Everything else is straightforward HTML.

Coordinates in the diagrams snap to a grid: the destination columns are locked to `x = 80 / 240 / 400` in viewBox space, and arrows + KYA pills sit on the same vertical lines.

## Credits

Partner brand wordmarks remain the property of their respective owners (Akamai, DataDome, Cequence, F5, Fastly, Imperva, HUMAN Security, Okta, Auth0, Ory, Forter). Use of these marks in a "supported by" / "ecosystem" placement typically requires written permission from each company before public deployment.

Material Symbols icons © Google, [Apache 2.0 licensed](https://github.com/google/material-design-icons).
