# Packlux

![Packlux logo](public/packlux-logo.png)

Danish launch page for a future Pokemon booster-pack shop. Built with Astro and
deployed as a static site on Cloudflare Pages.

This is not an operational shop: no products, checkout, payment processing,
customer accounts, or order collection are enabled. The pack illustrations are
original placeholders, not actual products.

## Local development

Use Node.js 24.21.0 (also pinned in `.node-version`).

```sh
npm ci
npm run dev
```

Run `npm run build` to generate `dist/`, or `npm run preview` to preview a build.
Page content and styling are in `src/pages/index.astro`.

## Cloudflare Pages

Connect the GitHub repository `Anas0473/Packlux` using the Pages Git integration.

| Setting | Value |
| --- | --- |
| Production branch | `main` |
| Framework preset | Astro |
| Build command | `npm run build` |
| Build output directory | `dist` |
| Root directory | Repository root (default) |

The `.node-version` file selects the build runtime. No environment variables,
database, paid services, or server adapter are required for this launch page.
Pushes to `main` trigger production builds once the Git integration is enabled.

## Before accepting orders

Add verified product details and licensed product photography, stock management,
server-validated checkout, payment confirmation handling, shipping rates, and
accurate business, privacy, and sales terms. Payment processing and delivery
can have per-order costs even when hosting has no monthly cost.
