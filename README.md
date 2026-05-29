# Dameka Dublin — Portfolio

Personal portfolio site. Static HTML/CSS/JS — no build step, no dependencies.
Designed to be served as a GitHub Pages **user site** at `https://DDublin1.github.io`.

```
.
├── index.html              # the whole page
├── README.md
└── assets/
    ├── style.css           # all styling
    ├── script.js           # scroll reveal, sticky nav, mobile menu
    ├── favicon.svg
    └── Dameka_Dublin_CV.docx   # linked by the "Download CV" buttons
```

## View it locally

Just open `index.html` in a browser. (Fonts load from Google Fonts, so you need
to be online for the typography to look right.)

To preview with a local server instead:

```powershell
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages (user site)

A user site lives in a repo named exactly `<username>.github.io`.

```powershell
# from inside this PORTFOLIO folder
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/DDublin1/DDublin1.github.io.git
git push -u origin main
```

1. Create the repo on GitHub first, named **`DDublin1.github.io`** (public).
2. Run the commands above.
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch → Branch: `main` / `/ (root)`** → Save.
4. Wait ~1 minute. The site goes live at **https://DDublin1.github.io**.

## Customising

- **Add your headshot.** In `index.html`, find the `<div class="avatar">` in the
  hero card and replace it with:
  ```html
  <img class="avatar" src="assets/headshot.jpg" alt="Dameka Dublin" />
  ```
  Drop a `headshot.jpg` into `assets/` (roughly 4:3, around 800px wide is plenty).
- **Project links.** The `↗` buttons currently point at your GitHub profile.
  Swap each `href="https://github.com/DDublin1"` for the specific repo URL once
  the projects are public.
- **Accent colour / fonts.** Change the CSS variables at the top of
  `assets/style.css` (`--accent`, `--serif`, `--sans`, `--mono`).
- **CV.** Replace `assets/Dameka_Dublin_CV.docx` with an updated file (a PDF is
  often nicer for downloads — if you swap to PDF, update the `href`s in
  `index.html`, there are two: in the hero and in the contact section).
