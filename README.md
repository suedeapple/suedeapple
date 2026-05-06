## Suedeapple 👋

Personal portfolio website for [Paul Wright](https://www.suedeapple.co.uk) — Certified Umbraco Master Developer, website designer, and ASP.NET developer based in Lancashire/Manchester.

### Tech Stack

- **HTML5** — `index.html` (main), `thanks/index.html` (post-form thank-you)
- **SCSS** — source in `css/styles.scss` and partials under `css/scss/`
- **JavaScript** — source in `js/main.js`
- **Libraries:** GSAP, Typed.js, Lenis, FontAwesome (CDN)
- **Build tool:** Vite

### Getting Started

```bash
npm install
npm run dev
```

### Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start local dev server at `http://localhost:5173` |
| `npm run build` | Build for production into `dist/` |
| `npm run preview` | Preview the production build locally |

### Deployment

Hosted on [Vercel](https://vercel.com). Connect the GitHub repo in the Vercel dashboard — it auto-deploys on every push to `main`.
