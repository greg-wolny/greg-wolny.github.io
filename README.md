# greg-wolny.github.io

Umbrella site for Greg Wolny's apps. Hosted on GitHub Pages — every push to `main` auto-publishes to `https://greg-wolny.github.io/`.

## Layout

```
.
├── index.html              # umbrella homepage
├── styles.css              # umbrella styles
├── postcard/               # Postcard landing + legal pages
│   ├── index.html
│   ├── privacy.html
│   ├── support.html
│   └── styles.css
└── mimic/                  # Mimic landing + legal pages
    ├── index.html
    ├── privacy.html
    ├── support.html
    └── styles.css
```

URL map:

- `https://greg-wolny.github.io/` — apps hub
- `https://greg-wolny.github.io/postcard/` — Postcard landing
- `https://greg-wolny.github.io/postcard/privacy` — Postcard privacy policy (App Store metadata URL)
- `https://greg-wolny.github.io/postcard/support` — Postcard support page (App Store metadata URL)
- `https://greg-wolny.github.io/mimic/` — Mimic landing
- `https://greg-wolny.github.io/mimic/privacy` — Mimic privacy policy (App Store metadata URL)
- `https://greg-wolny.github.io/mimic/support` — Mimic support page (App Store metadata URL)

Adding a new app: create a folder `<app-name>/` with its own `index.html` + supporting pages. Link it from the umbrella `index.html`.

## First-time GitHub setup

1. Create a public repo on GitHub named exactly `greg-wolny.github.io` (must match your username).
2. Inside this folder:
   ```bash
   git init
   git add -A
   git commit -m "Initial scaffold"
   git branch -M main
   git remote add origin git@github.com:greg-wolny/greg-wolny.github.io.git
   git push -u origin main
   ```
3. GitHub Pages publishes automatically — no separate Settings flip needed when the repo is named `<username>.github.io`.
4. First publish takes ~30-60 seconds. Subsequent pushes redeploy in seconds.

## Before App Store submission

- Replace the placeholder support email in `postcard/support.html` and `postcard/privacy.html` with a real address.
- Re-read `postcard/privacy.html` against the current state of the app (it's accurate as of 2026-05-05; revisit when material data flows change).
- App Store metadata URLs:
  - Privacy policy: `https://greg-wolny.github.io/postcard/privacy`
  - Support: `https://greg-wolny.github.io/postcard/support`
