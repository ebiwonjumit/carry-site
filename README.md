# Carry site

Static, single-file build of the Carry marketing site and app prototype. All 8 pages use hash routing (`#home`, `#markets`, `#market`, `#strategy`, `#dashboard`, `#positions`, `#deposit`, `#advanced`), so no server rewrites are needed.

## Run locally

```bash
npm run dev
# open http://localhost:3000
```

## Push to GitHub

```bash
git init
git add .
git commit -m "Carry site"
git branch -M main
git remote add origin https://github.com/<you>/carry-site.git
git push -u origin main
```

## Deploy on Vercel

1. In Vercel, click **Add New → Project** and import the GitHub repo.
2. Framework preset: **Other**. Build command: leave empty. Output directory: `public` (already set in `vercel.json`).
3. Deploy.

Or from the CLI: `npx vercel --prod`.

## Notes

- `public/coin-terminal-standalone.html` is the 3D Coin Terminal, embedded on the Strategy Coin page (`#strategy`). Add `?embed` to the URL to hide the drag hint. `public/assets/coin-terminal-front@2x.png` is its loading poster.
- `public/index.html` is a compiled bundle. Make design changes in the source design file and re-export; don't hand-edit the bundle.
- Market, position and token data are sample values, and wallet actions are simulated. Nothing connects to a chain yet.
- Disclaimers are placeholders pending legal review.
