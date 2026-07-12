# Academic personal website

A clean, modern, single-page academic homepage — static HTML/CSS/JS, no build step, free
to host on GitHub Pages. Live at **https://sekwaf.github.io/mywebsite/** once Pages is enabled.

```
mywebsite/
├── index.html          # the homepage (edit your content here)
├── cv.html             # printable CV page (Print → Save as PDF)
├── css/style.css       # all styling; theme colors live at the top in :root
├── js/main.js          # dark-mode toggle + nav highlighting
├── assets/
│   ├── profile.svg     # placeholder avatar — replace with your photo
│   └── favicon.svg     # browser-tab icon
└── .nojekyll           # tells GitHub Pages to serve files as-is
```

## Turn on free hosting (one time)

1. Commit and push these files to the `main` branch of `SekWaf/mywebsite`.
2. On GitHub: **Settings → Pages**.
3. Under *Build and deployment*, set **Source = Deploy from a branch**,
   **Branch = `main`**, folder **`/ (root)`**, then **Save**.
4. Wait ~1 minute. Your site is live at `https://sekwaf.github.io/mywebsite/`.

Every future `git push` to `main` republishes automatically.

## Customize it

All the visible content is in **`index.html`** — search for the text you want to change.
Key things to replace:

- **Name, title, affiliation** — top of `index.html` (the `.hero` section).
- **Photo** — drop your image in `assets/` and change the `src` on `.hero__photo`
  to e.g. `assets/photo.jpg` (a square image works best).
- **Links** — the `href="#"` placeholders on Scholar / GitHub / X, and your email.
- **About / News / Publications / Teaching / Projects / Contact** — each is a
  clearly-marked `<section>`.
- **CV** — edit `cv.html`, or replace the `CV` button's `href` with a PDF you upload.

### Change the accent color / fonts

Open `css/style.css`. The palette is defined once at the top:

```css
:root {
  --accent: #3b5bdb;   /* change this to re-theme the whole site */
  --maxw: 720px;       /* content width */
}
```

Dark-mode colors are in the `:root[data-theme="dark"]` block just below.

### Use a custom domain (optional)

Add a file named `CNAME` containing your domain (e.g. `www.example.com`), then set the
DNS records your registrar requires and configure the domain under Settings → Pages.

---

> ⚠️ **The content is placeholder/fictional.** Names, publications, awards, and courses were
> generated as a template. Replace everything with your real information before sharing the site.
