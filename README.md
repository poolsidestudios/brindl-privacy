# brindl-privacy

The two public pages Brindl needs for the App Store: a privacy policy and a
support page. Hand-written static HTML with inline styles - no build step, no
dependencies.

## Where they are served

**Netlify is the intended home**, matching `pitbox-privacy`, because a Netlify
project URL does not carry the account name the way a GitHub Pages project site
does (`poolsidestudios.github.io/...` is structural there and cannot be removed
without a custom domain).

| Page | URL (the only valid one) | ASC field |
|---|---|---|
| `index.html` | https://brindl-privacy.netlify.app/ | Privacy Policy URL |
| `support.html` | https://brindl-privacy.netlify.app/support.html | Support URL |

**GitHub Pages is deliberately OFF for this repo** (repo Settings > Pages >
Build and deployment > Branch > None). `poolsidestudios.github.io/brindl-privacy`
is not a mirror and not a fallback - it is dead, on purpose, so there is exactly
one live copy of these pages and no chance of the two drifting or of the
account-name URL leaking into a store field.

Netlify project: `brindl-privacy` (team `poolsidestudios`, site id
`097ebfaf-8a78-46d7-ad3a-466fa37cc93a`) -
https://app.netlify.com/projects/brindl-privacy

## Publishing

This repo is the single source of truth. Edit a file, push to `main`, and
Netlify publishes it automatically - the project is linked to this repo and
`netlify.toml` pins the publish directory to the root, so there is nothing to
configure and nothing to upload.

**Never hand-upload to Netlify** (drag-and-drop deploys included). A manual
deploy wins until the next push, so the live site would stop matching this repo
and nobody would be able to tell from the files.

Keep the two in sync when app behaviour changes: the support page describes
real flows (join codes, the billing PIN reset, backups, what billing does and
does not do), so a feature change can make it wrong.
