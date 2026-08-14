# brindl-privacy

GitHub Pages site serving the two public pages Brindl needs for the App Store.

| Page | URL | ASC field |
|---|---|---|
| `index.html` | https://poolsidestudios.github.io/brindl-privacy/ | Privacy Policy URL |
| `support.html` | https://poolsidestudios.github.io/brindl-privacy/support.html | Support URL |

Both are hand-written static HTML with inline styles - no build step, no
dependencies. Edit the file, push to `main`, and Pages redeploys.

Keep the two in sync when app behaviour changes: the support page describes
real flows (join codes, the billing PIN reset, backups, what billing does and
does not do), so a feature change can make it wrong.
