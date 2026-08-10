# appearant.works

One-page site for Appearant 梨所當然, a game localization studio.

Static HTML, no build step. Deploys to GitHub Pages from the repo root.

## Deploying

This folder is the **contents** of a separate public GitHub repo, not a subfolder of it.
`index.html` must sit at that repo's root.

1. Copy everything here into a public repo
2. Settings → Pages → Deploy from a branch → `main` → `/ (root)`
3. Settings → Pages → Custom domain → `appearant.works` → Enforce HTTPS

Full procedure, including DNS and Google Workspace, is in
[`../domain-email-website-setup.md`](../domain-email-website-setup.md).

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole site. Inline CSS, no dependencies except Google Fonts. |
| `CNAME` | Tells GitHub Pages the custom domain. Do not delete. |
| `.nojekyll` | Skips Jekyll processing. |
| `assets/seal-*.png` | Seal-only no-border logo, from `../assets/Logo/Logo Seal/`. |
| `assets/og.png` | Link preview card, 1200×630. |
| `robots.txt`, `sitemap.xml` | Standard crawl files. |

## Editing

Copy is the live version of [`../website-onepager.md`](../website-onepager.md). Change the
copy doc when the wording changes, so the two do not drift.

Brand rules come from [`../assets/design-spec.md`](../assets/design-spec.md):
Warm Paper `#DACFC0` ground, Olive Green `#637159` ink, Seal Brown `#AC9A8C` and Soft Taupe
`#C9BDB4` panels, accents small only. Sofia Sans with IBM Plex Sans TC for Chinese.
Lowercase-leaning, rounded, flat, generous negative space. No gradients or shadows.

The golden-yellow gamescom chip is the page's one accent. Remove that block after
30 August 2026.
