# State of Your AI: preview

The direction mock for State of Your AI, served as a site behind a password. `index.html` is the mock encrypted with the password (AES-256-GCM, key from PBKDF2) and a small gate that decrypts it in the browser; nothing readable lives in this repository or its history. Every push to `main` deploys it to GitHub Pages.

The organisation in the mock, Northgate Housing, is fictional.

## Updating

The readable mock and the build live in the product repo. From its `design/mock/preview` folder, with this repo cloned alongside:

```
PREVIEW_PASSWORD=<the password> node build.mjs
```

That rewrites `index.html` here. Commit and push it. The password is not written down in either repository.

## Where it is

https://stateofyour.ai, by the CNAME file; https://stuartridout.github.io/statepreview/ redirects there. Pages was switched on by hand on 2 Oct 2026 (Settings, Pages, Source: GitHub Actions), because a workflow's own token is not allowed to create the site; the first two runs failed at that step. If the custom domain ever shows a certificate warning, "Enforce HTTPS" in the same settings page is the switch, available once GitHub has issued the certificate.
