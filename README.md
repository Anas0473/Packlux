<p align="center">
  <img src="public/packlux-logo.png" alt="Packlux" width="360" />
</p>

<h1 align="center">Small packs. Big discoveries.</h1>

<p align="center">
  A playful Danish storefront for Japanese Pokémon booster packs.<br />
  Built for the excitement of the next great pull.
</p>

<p align="center">
  <a href="https://packlux-87w.pages.dev/"><strong>Explore Packlux</strong></a>
  &nbsp; · &nbsp;
  <a href="https://packlux-87w.pages.dev/#sortiment">Browse the packs</a>
  &nbsp; · &nbsp;
  <a href="https://packlux-87w.pages.dev/#holo">Spin the holo card</a>
</p>

---

## A little collector energy

Bright blue and yellow, chunky outlines, floating packs, and a little holographic
magic. Packlux brings a playful trading-card feel to a lightweight storefront,
with Danish copy, DKK prices, and a focus on delivery in Denmark.

- **The real lineup:** 30th Celebration, Storm Emerald, White Flare, and Pokémon Card 151.
- **Packs in the spotlight:** transparent product photos, clear prices, and stock counts.
- **Give it a spin:** a floating, draggable 360° card with angle-reactive rainbow shine.
- **Two sides to discover:** Mew's 151 pack on the front, our Packlux logo on the back.
- **Made for small screens too:** responsive layouts, touch controls, and keyboard support.
- **Keep it calm:** pause the floating animation, or use your device's reduced-motion setting.

> **Getting ready to open:** the site is live, but orders and payments are not
> enabled. Stock counts are a manually maintained snapshot, not live inventory.
> The spinning card is a visual demo; its branded back is not the pack's actual reverse side.

## Under the wrapper

| Layer | Built with |
| --- | --- |
| Website | [Astro](https://astro.build/) with TypeScript |
| Look and feel | Custom CSS, gradients, and 3D transforms |
| Interaction | Browser-native pointer and keyboard events |
| Hosting | [Cloudflare Pages](https://pages.cloudflare.com/) |
| Deployments | GitHub pushes to `main` |

No 3D engine, Blender model, database, or paid service is required for the current
site. The holographic effect runs directly in the browser.

## Run it locally

Use **Node.js 24.21.0**, pinned in [`.node-version`](.node-version).

```sh
npm ci
npm run dev
```

| Command | What it does |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Generate the production site in `dist/` |
| `npm run preview` | Preview the production build locally |

### Where things live

```text
src/
  pages/index.astro        Storefront, product data, prices, and stock
  components/HoloCard.astro
                          Interactive two-sided holographic card
public/
  packlux-logo.png         Packlux branding
  products/               Transparent booster-pack photos
```

Update the `boosterPacks` array in [`src/pages/index.astro`](src/pages/index.astro)
to change the displayed prices or stock counts. Card artwork and interaction live
in [`src/components/HoloCard.astro`](src/components/HoloCard.astro).

### Spin controls

| Input | Action |
| --- | --- |
| Drag left or right | Rotate the card through 360° |
| Arrow keys, with the card focused | Rotate or tilt |
| Enter, Space, or **Vend kortet** | Flip the card |
| Home or **Nulstil** | Restore the starting angle |
| **Pause svævning** | Pause or resume floating |

Vertical touch scrolling stays available. Reduced-motion preferences disable
automatic floating.

## From commit to Cloudflare

The GitHub repository is connected to Cloudflare Pages. Push to `main` to trigger
an automatic production deployment.

| Build setting | Value |
| --- | --- |
| Framework preset | Astro |
| Production branch | `main` |
| Build command | `npm run build` |
| Output directory | `dist` |
| Root directory | Repository root |

The build runtime comes from `.node-version`. No environment variables or server
adapter are needed for the current static site.

## Still to unpack

Before accepting orders:

- [ ] Shopping cart and server-validated checkout
- [ ] Payment integration and confirmed-payment handling
- [ ] Live inventory and order management
- [ ] Shipping rates and delivery options
- [ ] Complete business details, sales terms, and privacy information

Hosting currently uses Cloudflare's free Pages tier. Payment processing, shipping,
and an optional custom domain may still have costs.

---

<p align="center">
  <strong>Packlux</strong> · CVR: 46860330<br />
  <a href="mailto:packluxdk@gmail.com">packluxdk@gmail.com</a><br />
  <sub>Independent store. Not affiliated with The Pokémon Company.</sub>
</p>
