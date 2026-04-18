## Suedeapple 👋

Personal portfolio website for [Paul Wright](https://www.suedeapple.co.uk) — Certified Umbraco Master Developer, website designer, and ASP.NET developer based in Lancashire/Manchester.

### Tech Stack

- **HTML5** — `index.htm` (main), `thanks/index.htm` (post-form thank-you)
- **SCSS** — source in `css/styles.scss`, compiled to `css/styles.min.css`
- **JavaScript** — source in `js/scripts.js`, minified to `js/scripts.min.js`
- **Libraries:** GSAP, Typed.js, Lenis, FontAwesome

### Deployment

Pushes to `main` are automatically deployed to Webwiz hosting via FTP using GitHub Actions. Add the following secrets to your repository before the workflow will run:

| Secret | Description |
|---|---|
| `FTP_SERVER` | Webwiz FTP hostname |
| `FTP_USERNAME` | FTP username |
| `FTP_PASSWORD` | FTP password |
