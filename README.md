# Draw3D legal pages

Static Privacy Policy + Terms of Service pages for the Google Play listing, meant to be
served from a **separate public GitHub repo** via GitHub Pages (the app repo is private, so
Pages can't serve from it on a free plan).

## Files

- `index.html` — small landing page linking both documents
- `privacy-policy.html` — the URL for the Play Console / AdMob / Data safety forms
- `terms-of-service.html`

## Before publishing — placeholders to review

- **Contact email**: currently `support@draw3d.app` — the same dummy as `AppConfig.CONTACT_EMAIL`.
  Replace in all three HTML files *and* in `AppConfig.kt` when you have the real address.
- **App name**: "Draw3D" — must match the final Play Store listing name.
- **Developer name**: "Daniel Pitropovski" (privacy §intro, terms §1).
- **Governing law**: Czech Republic (terms §13) — confirm this is where you'll publish from.
- **Crashlytics**: the privacy policy already covers it ("may use"), fine whether or not
  Firebase ends up wired in.

## Deployed (done 2 July 2026)

Repo: `https://github.com/BargoEmbargo/mannequink-legal` (public), GitHub Pages serving
`main` / root. Live URLs:

- `https://bargoembargo.github.io/mannequink-legal/privacy-policy.html`
- `https://bargoembargo.github.io/mannequink-legal/terms-of-service.html`

Paste the privacy-policy URL into **Play Console → App content → Privacy policy** (and into
the Data safety form where asked). Updating the pages later = edit + `git push`; the URL
never changes.

Note: the nested `legal/.git` (created in step 2) keeps this folder out of the app repo's
git — the app repo sees it as one untracked directory. If you'd rather also version these
sources in the app repo, skip `git init` here and push from a copy instead.
