# GitHub Pages site for Recs

This folder is a complete repo. Push its contents (including the hidden `.nojekyll` and `.well-known/`) to a **public repo named `b-fishman.github.io`**, then Settings > Pages > Source: Deploy from a branch, `main`, `/ (root)`.

Pages:
- `https://b-fishman.github.io/recs/privacy.html` and `/recs/terms.html` (refresh with `npm run hosting:sync` after editing `www/privacy.html` or `www/terms.html`)
- `https://b-fishman.github.io/recs/i/?c=CODE` invite landing: tries `recs://invite/CODE`, then shows the code and the App Store link
- `https://b-fishman.github.io/.well-known/apple-app-site-association` for universal links

Universal links only work from a **user site** repo named exactly `b-fishman.github.io`, because Apple fetches the association file from the root of the host. A project repo (for example `b-fishman/recs`) serves at `/recs/` only, so the association file is not found: the pages still work, but invite links open the landing page instead of the app, which then offers `recs://invite/CODE` and shows the code to type in.
