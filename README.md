# $ヤギ — Nagi and Pokke

Website for $ヤギ, the Solana coin for Nagi and Pokke, JR East's weeding goats at Yotsuya Station.

- `public/index.html` — the whole site (one file, images embedded). English / 中文.
- `wrangler.jsonc` — Cloudflare Workers config. Serves `public/` as static assets.

## Deploy

**Manual:** Cloudflare → Workers & Pages → `yagi-solana` → upload `public/index.html`.

**Automatic (recommended):** connect this repo to the `yagi-solana` Worker
(Settings → Build → Connect repository). Every push to `main` redeploys the site.
Build command: none. Deploy command: `npx wrangler deploy`.

## Editing coins

Coins in the ecosystem totals are listed in `ECO_COINS` inside `public/index.html`.
Live prices, market caps and liquidity load from DexScreener in the browser, so numbers never need a redeploy.

Last deploy trigger: 2026-10-23 19:23 JST
