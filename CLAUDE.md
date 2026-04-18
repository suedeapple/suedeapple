# Suedeapple

Personal portfolio website for Paul Wright — Certified Umbraco Master Developer, website designer, and ASP.NET developer based in Lancashire/Manchester.

## Tech Stack

- **HTML5** – `index.htm` (main), `thanks/index.htm` (post-form thank-you)
- **SCSS** – source in `css/styles.scss` and partials under `css/scss/`
- **JavaScript** – source in `js/scripts.js`
- **Libraries:** GSAP (scroll animations), Typed.js (typewriter effect), Lenis (smooth scrolling), FontAwesome (icons)

## Directory Structure

```
index.htm              # Main page
thanks/index.htm       # Thank-you page after contact form submission
css/
  styles.scss          # SCSS source
  styles.min.css       # Compiled/minified output (edit this when no SCSS compiler available)
  scss/                # SCSS partials
js/
  scripts.js           # JS source
  scripts.min.js       # Minified output
img/
  logos/               # Client logos (SVG)
  work/                # Portfolio project images (WebP)
  me/                  # Profile images
```

## Build / Compilation

No build tooling is committed to this repo. SCSS and JS are compiled externally:

- `css/styles.scss` → `css/styles.min.css`
- `js/scripts.js` → `js/scripts.min.js`

When making CSS/JS changes, edit the **source** files and recompile, or edit the minified files directly if a compiler is not available.

## Deployment

Static site hosted on IIS (indicated by the gitignored `web.config`). No build step required — deploy all files as-is.

## Testing

No automated tests or CI pipeline. Verify changes by opening `index.htm` in a browser and checking responsiveness across breakpoints (desktop-first media queries).
