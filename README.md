# Billboard demo — Netlify deploy

This folder is a **static site**. Do not run a build step.

## Deploy (recommended)

1. Zip **this folder’s contents** (the files inside `billboard-demo`, not the parent Downloads folder), **or** connect a Git repo whose **publish directory** is this folder.
2. In Netlify: **Add new site** → **Deploy manually** (drag-and-drop the folder).
3. Ensure the deployed site root contains **`index.html`** next to **`spiral.png`**, **`layer1.png`**, etc.

Opening `https://yoursite.netlify.app/` loads **`index.html`** automatically. You do not need a special URL path.

## If the site is blank or assets 404

- **Wrong publish directory:** The site root must be the folder that contains `index.html` and the PNGs. If your repo has a parent folder, set **Base directory** / **Publish directory** to `billboard-demo` (or the folder name you use).
- **Case-sensitive paths:** Asset names are lowercase: `layer1.png`, `spiral.png` (Linux servers are strict).
- **HTTPS:** The page loads Three.js from a CDN; use the deployed `https://` URL, not `file://`.

## Local preview

```bash
cd billboard-demo
python3 -m http.server 8765
```

Then open `http://localhost:8765/`.
