# Suedeapple

Personal portfolio website for Paul Wright — Certified Umbraco Master Developer, website designer, and ASP.NET developer based in Lancashire/Manchester.

## Tech Stack

- **HTML5** — `index.html` (main), `thanks/index.html` (post-form thank-you)
- **SCSS** — source in `css/styles.scss` and partials under `css/scss/`
- **JavaScript** — source in `js/main.js`
- **Libraries:** GSAP (scroll animations), Typed.js (typewriter effect), Lenis (smooth scrolling), FontAwesome (icons via CDN)
- **Build tool:** Vite

## Directory Structure

```
index.html             # Main page
thanks/index.html      # Thank-you page after contact form submission
vite.config.js         # Vite config (multi-page, SCSS)
package.json
css/
  styles.scss          # SCSS entry point
  scss/                # SCSS partials (layout, components, helpers, utils)
js/
  main.js              # JS entry point (GSAP, Lenis, Typed.js logic)
public/
  img/
    logos/             # Client logos (SVG)
    work/              # Portfolio project images (WebP)
    me/                # Profile images
  apple-touch-icon.png # Favicons — add these to public/ if not present
  favicon-*.png
  site.webmanifest
dist/                  # Vite build output (gitignored)
```

## Build

```bash
npm install
npm run dev      # dev server at http://localhost:5173
npm run build    # production build to dist/
npm run preview  # preview dist/ locally
```

Edit source files (`css/styles.scss`, `css/scss/**`, `js/main.js`) — Vite handles compilation. Never edit `dist/` directly.

## CSS / FOUC

The SCSS is referenced as a `<link>` in `<head>` (not imported via JS) so the browser loads it as a blocking stylesheet, preventing flash of unstyled content. Keep it this way.

## Deployment

Hosted on Vercel. Connect the GitHub repo in the Vercel dashboard — auto-deploys on every push to `main`. No config file needed; Vercel auto-detects Vite with `dist/` as output.

## Testing

No automated tests. Verify changes with `npm run dev` and check responsiveness across breakpoints (desktop-first media queries).
