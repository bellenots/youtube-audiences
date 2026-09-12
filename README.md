# YouTube Audiences: Overall vs Left vs Right

Static single-page site comparing YouTube Overall Top 100 vs Left / Right political commentary audiences (snapshot Sep 2026).

**No build step required.** Open `index.html` locally or deploy the folder as static files.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | Dark-themed public page (works offline) |
| `data.json` | Same numbers in machine-readable form |
| `assets/` | Chart / infographic PNGs |
| `vercel.json` | Static deploy config for Vercel |

## Local preview

```bash
# Option A — open directly (fully offline)
open index.html          # macOS
xdg-open index.html      # Linux

# Option B — tiny local server
npx serve .
# or: python3 -m http.server 8080
```

## Deploy

Any static host works. Point the publish directory at this folder (site root = where `index.html` lives).

### Vercel

```bash
npx vercel --yes
# or connect the repo in the Vercel dashboard; Framework Preset: Other
```

`vercel.json` sets a static rewrite so `/` serves `index.html`.

### Netlify

- Drag-and-drop this folder in the Netlify UI, **or**
- Publish directory: `.` (repo root of this site)
- Build command: leave empty

### GitHub Pages

1. Push this folder to a repo (or `/docs` on `main`).
2. Settings → Pages → Deploy from branch → select the folder with `index.html`.
3. Or use Actions with `peaceiris/actions-gh-pages` / `actions/upload-pages-artifact`.

### Cloudflare Pages

- Build command: empty  
- Build output directory: `/` (or `.`)

## Colors

- Background `#0f1419` · Cards `#1a222d`
- Overall `#4C78A8` · Left `#5B8DEF` · Right `#E45756`

## Caveats (shown on page)

- Overall is global entertainment — different genre than political.
- Leans are analyst judgment.
- Cable (Fox/CNN/MS NOW) omitted from political top-10 for creator comparison.
- Sources: vidIQ, SocialBlade, Feedspot; snapshot Sep 2026.
