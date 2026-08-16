# kiertotie.fi

Public-facing site for [Kiertotie](https://kiertotie.fi), an iOS app for finding independently-owned cafés, restaurants, and points of interest in Finland. Deployed to GitHub Pages via `.github/workflows/deploy-pages.yml` on every push to `main`.

This is a separate, public repo from the app's main (private) source repo — GitHub's free tier only serves Pages from public repos, and the app repo stays private.

## Structure

- `index.html` — landing page
- `privacy/index.html` — privacy policy, served at `/privacy` (also see `PRIVACY.md` for the plain-text source)
- `assets/` — icon images generated from the app's icon
- `CNAME` — custom domain (`kiertotie.fi`)

## One-time GitHub setup

In this repo's **Settings → Pages**, set **Source** to "GitHub Actions" (not "Deploy from a branch"). Then point the `kiertotie.fi` domain's DNS at GitHub Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Updating content

Edit the relevant `.html`, push to `main`, and the workflow redeploys automatically — no build step, it's a static site.
