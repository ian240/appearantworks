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
| `assets/games/` | Per-game key art as WebP at 480, 800 and 1100 px (`<slug>-art-<w>.webp`), an 800 px JPEG fallback (`<slug>-art.jpg`), and title logos (`<slug>-logo.png`). |
| `assets/og.png` | Link preview card, 1200×630. |
| `robots.txt`, `sitemap.xml` | Standard crawl files. |

## Editing

Copy follows the developer deck, [`../deck-developers.md`](../deck-developers.md). Every
string on the page comes from a slide, and the games section mirrors the portfolio slides
in deck order. When the deck changes, change the page to match. Where the deck has a gap,
the page keeps the same gap.

Key art was cut from the 2026-08-17 client drop and center-cropped to 4:3. It is served
through `<picture>` with a WebP `srcset` (quality 72), so a browser fetches only the width
it needs. The art panel is at most about 660 CSS px wide, which is why the largest cut is
1100 px. On desktop the whole games section loads about 470 KB. Logos are trimmed, sized to
twice their largest display width, and saved as 128-color PNGs. That beat WebP for flat logo
art: Superliminal is 6.5 KB as PNG and 47.6 KB as WebP. Logo corners follow the deck. Star
Trucker has no overlay because its logo is part of the art.

Mr. Prepper was taken off the page on 2026-09-15, because no art for it exists anywhere.

Brand rules come from [`../assets/design-spec.md`](../assets/design-spec.md):
Warm Paper `#DACFC0` ground, Olive Green `#637159` ink, Seal Brown `#AC9A8C` and Soft Taupe
`#C9BDB4` panels, accents small only. Sofia Sans with IBM Plex Sans TC for Chinese.
Lowercase-leaning, rounded, flat, generous negative space. No gradients or shadows. No em
dashes, per the deck.
