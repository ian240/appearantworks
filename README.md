# appearant.works

One-page site for Appearant 梨所當然, a game localization studio.

Static HTML, no build step. Deploys to GitHub Pages from the repo root.

## Deploying

This folder is the **contents** of a separate public GitHub repo, not a subfolder of it.
`index.html` must sit at that repo's root.

Live at `https://appearant.works`, deployed from **`github.com/ian240/appearantworks`**
(no hyphen).

1. Copy everything here into that repo
2. Settings → Pages → Deploy from a branch → `main` → `/ (root)`
3. Settings → Pages → Custom domain → `appearant.works` → Enforce HTTPS

Full procedure, including DNS and Gandi Mail, is in
[`../domain-email-website-setup.md`](../domain-email-website-setup.md).

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site. Inline CSS, no dependencies except Google Fonts. |
| `CNAME` | Tells GitHub Pages the custom domain. Do not delete. |
| `.nojekyll` | Skips Jekyll processing. |
| `assets/seal-*.png` | Seal-only no-border logo, from `../assets/Logo/Logo Seal/`. |
| `assets/games/` | Per-game key art (`<slug>-art.jpg`, 1200×900) and title logos (`<slug>-logo.png`, at most 600 px wide). |
| `assets/og.png` | Link preview card, 1200×630. |
| `robots.txt`, `sitemap.xml` | Standard crawl files. |

## Editing

Copy follows the developer deck, [`../deck-developers.md`](../deck-developers.md). Every
string on the page comes from a slide, and the games section mirrors the portfolio slides
in deck order. When the deck changes, change the page to match. Where the deck has a gap,
the page keeps the same gap.

Key art was cut from the 2026-08-17 client drop: center-cropped to 4:3, 1200 px wide, JPEG
q78. Logos use the same trim-and-shrink recipe as
[`../assets/client-titles/collected-assets.md`](../assets/client-titles/collected-assets.md).
Logo corners follow the deck. Star Trucker has no overlay because its logo is part of the art.
Mr. Prepper has no art anywhere, so its panel is Seal Brown with the title set in type.

Brand rules come from [`../assets/design-spec.md`](../assets/design-spec.md):
Warm Paper `#DACFC0` ground, Olive Green `#637159` ink, Seal Brown `#AC9A8C` and Soft Taupe
`#C9BDB4` panels, accents small only. Sofia Sans with IBM Plex Sans TC for Chinese.
Lowercase-leaning, rounded, flat, generous negative space. No gradients or shadows. No em
dashes, per the deck.
