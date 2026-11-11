# Packlux

![Packlux logo](public/packlux-logo.png)

Danish launch page for a future Pokemon booster-pack shop. Built with Astro and
deployed as a static site on Cloudflare Pages.
The storefront uses a playful blue-and-yellow palette, comic-style outlines,
rounded controls, and product photos supplied by the store.

This is not an operational shop: checkout, payment processing, customer accounts,
and order collection are not enabled. The catalog shows four Japanese Pokemon
booster packs: 30th Celebration, Storm Emerald, White Flare, and Pokemon Card 151.
Product photos in `public/products/` have transparent backgrounds and are also used
in the hero. Product images sit above separate bordered detail boxes.
Prices in DKK and stock counts are manually maintained in the `boosterPacks` array
in `src/pages/index.astro`, based on the store's supplied inventory sheet.
They are a static inventory snapshot, not live stock tracking. Purchase buttons
remain disabled until checkout is implemented.

## Interactive holographic card

`src/components/HoloCard.astro` displays an original, fictional card using CSS
3D transforms, front/back faces, and angle-dependent holographic gradients.
Drag horizontally to rotate through 360 degrees (mouse or touch); vertical touch
scrolling is preserved. Arrow keys rotate/tilt the focused card; Enter, Space,
or the flip button turns it over. Home or Reset restores the initial angle.
Floating can be paused and is disabled by the reduced-motion preference.
This is a browser-rendered visual demo, not a Blender model, product, or pack-opening flow.

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
