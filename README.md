# brindl-privacy

The two public pages Brindl needs for the App Store: a privacy policy and a
support page. Hand-written static HTML with inline styles - no build step, no
dependencies.

## Where they are served

**Netlify is the intended home**, matching `pitbox-privacy`, because a Netlify
project URL does not carry the account name the way a GitHub Pages project site
does (`poolsidestudios.github.io/...` is structural there and cannot be removed
without a custom domain).

| Page | Netlify (preferred) | GitHub Pages (still live) | ASC field |
|---|---|---|---|
| `index.html` | https://brindl-privacy.netlify.app/ | https://poolsidestudios.github.io/brindl-privacy/ | Privacy Policy URL |
| `support.html` | https://brindl-privacy.netlify.app/support.html | https://poolsidestudios.github.io/brindl-privacy/support.html | Support URL |

Netlify project: `brindl-privacy` (team `poolsidestudios`, site id
`097ebfaf-8a78-46d7-ad3a-466fa37cc93a`) -
https://app.netlify.com/projects/brindl-privacy

## Publishing

This repo stays the single source of truth. Edit a file, push to `main`.

- **GitHub Pages** redeploys on its own.
- **Netlify** redeploys on its own ONCE the project is linked to this repo
  (Netlify project > Build & deploy > link repository, branch `main`).
  `netlify.toml` already pins the publish directory to the repo root, so there
  is nothing to configure by hand. Until that link exists, Netlify needs a
  manual deploy and the two hosts can drift.

Keep the two in sync when app behaviour changes: the support page describes
real flows (join codes, the billing PIN reset, backups, what billing does and
does not do), so a feature change can make it wrong.
