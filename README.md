# Jarvis AI — public branding site

Static homepage + privacy policy for Google OAuth consent branding.

**Not** Jarvis Core. Contains no secrets, tokens, or calendar data.

## Intended GitHub Pages URLs

After a **public** repository `jarvis-ai-site` is created under `IvoryXXX` and Pages is enabled (root `/`):

- Homepage: `https://ivoryxxx.github.io/jarvis-ai-site/`
- Privacy: `https://ivoryxxx.github.io/jarvis-ai-site/privacy.html`

## Local preview

Open `index.html` in a browser, or:

```powershell
cd D:\AI\Projects\jarvis-ai-site
python -m http.server 8766 --bind localhost
```

Then visit `http://localhost:8766/` and `http://localhost:8766/privacy.html`.

## Deploy (only after explicit approval)

`gh pages` CLI is not required. Typical flow with authenticated `gh`:

```powershell
cd D:\AI\Projects\jarvis-ai-site
git init
git add index.html privacy.html styles.css README.md
git commit -m "Add Jarvis AI OAuth branding pages."
gh repo create jarvis-ai-site --public --source=. --remote=origin --push
```

Then in GitHub: **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `/ (root)` → Save**.

Do **not** put these files into the private `jarvis-core` repository as a substitute for a public Pages site—Google needs a publicly reachable HTTPS URL.
