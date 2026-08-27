# Portfolio — Zubaer Alam Bihim

Static site, no build step. Ready for GitHub Pages.

## Structure

```
index.html          <- live site (light, client-facing; "Switch theme" -> index-v2.html)
index-v2.html       <- alternate dark theme (same data; "Switch theme" -> index.html)
assets/img/hero.jpg
assets/img/projects/*.jpg
```

Both live pages are single self-contained files (inline CSS/JS). Project data is duplicated in
`index.html` and `index-v2.html` — edit both when a link or description changes.

## Before you deploy

1. Headshot at `assets/img/hero.jpg` (shown in both themes) and project screenshots at
   `assets/img/projects/` — already present; replace as needed.
2. Confirm the GitHub/LinkedIn/dev.to URLs (`github.com/bihim`, `linkedin.com/in/bihim`, `dev.to/bihim`)
   in both files' footers and contact sections.

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
```

Repo `bihim/portfolio` deploys from `main` (root) to **https://bihim.co** via `CNAME`.

## Notes

- No backend: the contact form opens the visitor's email client via `mailto:` — nothing is stored or transmitted server-side.
- Animations respect `prefers-reduced-motion`.
