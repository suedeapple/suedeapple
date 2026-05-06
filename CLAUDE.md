# Suedeapple

Personal portfolio website for Paul Wright — Certified Umbraco Master Developer, website designer, and ASP.NET developer based in Lancashire/Manchester.

## Tech Stack

- **HTML5** – `index.html` (main), `thanks/index.html` (post-form thank-you)
- **SCSS** – source in `css/styles.scss` and partials under `css/scss/`
- **JavaScript** – source in `js/main.js` (main page), `js/thanks.js` (thank-you page)
- **Libraries:** GSAP (scroll animations), Typed.js (typewriter effect), Lenis (smooth scrolling), FontAwesome (icons via CDN)
- **Build tool:** Vite

## Directory Structure

```
index.html             # Main page
thanks/index.html      # Thank-you page after contact form submission
vite.config.js         # Vite config (multi-page, SCSS)
package.json
css/
  styles.scss          # SCSS source (entry point)
  scss/                # SCSS partials
js/
  main.js              # Main JS entry (imports SCSS + scripts logic)
  thanks.js            # Thanks page entry (imports SCSS only)
img/
  logos/               # Client logos (SVG)
  work/                # Portfolio project images (WebP)
  me/                  # Profile images
public/                # Static assets served at root (favicons, site.webmanifest)
dist/                  # Vite build output (gitignored)
```

## Build / Compilation

Vite project. Install dependencies and use the standard scripts:

```
npm install
npm run dev      # local dev server at http://localhost:5173
npm run build    # outputs to dist/
npm run preview  # preview the dist/ build locally
```

When making CSS/JS changes, edit the source files (`css/styles.scss`, `css/scss/**`, `js/main.js`). Vite handles compilation.

## Deployment

Hosted on Vercel. Vercel auto-detects Vite and runs `vite build` with `dist/` as the output directory.

**Recommended:** connect the GitHub repo to Vercel via the dashboard — it will auto-deploy on every push to `main`, no GitHub Action needed.

**GitHub Action (`.github/workflows/deploy.yml`):** if you prefer CI-based deployment, set three repo secrets — `VERCEL_TOKEN`, `VERCEL_ORG_ID`, `VERCEL_PROJECT_ID` — from your Vercel project settings.

Favicon files (`apple-touch-icon.png`, `favicon-*.png`, `site.webmanifest`) should be placed in the `public/` directory so Vercel serves them at the root path.

## Testing

No automated tests. Verify changes with `npm run dev` and check responsiveness across breakpoints (desktop-first media queries).
