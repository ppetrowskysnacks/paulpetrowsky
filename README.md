# paulpetrowsky.com

Personal portfolio site. Pure static HTML, CSS, and woff2 fonts — no build step.

## Quick start

```bash
npm install        # one-time, installs browser-sync
npm run dev        # live-reload server at http://localhost:3000
```

Edit `index.html` and the page refreshes automatically.

## Layout

```
paulpetrowsky-com/
├── index.html       # the whole site
├── fonts/           # Geomanist + DDC Hardware woff2s
├── netlify.toml     # cache headers, security headers
├── package.json     # dev server only
└── .gitignore
```

## Deployment

Hosted on **Netlify** with Git auto-deploy.

- **Production:** every push to `main` deploys to paulpetrowsky.com.
- **Previews:** every PR gets its own preview URL.
- **Rollback:** Netlify dashboard → Deploys → pick any past deploy → "Publish deploy."

### Manual deploys (optional)

```bash
npx netlify-cli login          # one-time
npm run deploy:preview         # draft URL
npm run deploy:prod            # publishes to production
```

## V1 scope

Single-page credentialing surface. Not a multi-case-study portfolio (that's V2).
Sections: header, positioning paragraph, gated Meta case study, selected work,
two testimonials, contact. The Meta case study is gated behind a `mailto:`
link in V1. Better gating (password / Netlify Identity) is V1.1.

## V2 backlog

- Long-form Meta case study page (gated)
- Additional case studies
- Refreshed post-Meta testimonials
- Open Graph image
