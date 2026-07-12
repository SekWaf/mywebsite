# Academic personal website

A clean, single-page academic homepage in an elegant **editorial / literary serif** style —
one self-contained static HTML file, no build step, free to host on GitHub Pages.
Live at **https://sekwaf.github.io/mywebsite/**.

```
mywebsite/
├── index.html          # the whole site — content + styling inline in one file
├── assets/
│   ├── profile.jpg     # your portrait
│   └── favicon.svg     # browser-tab icon
├── .nojekyll           # tells GitHub Pages to serve files as-is
└── .gitignore          # keeps local /previews (alternate style drafts) out of the repo
```

> The homepage is fully self-contained: all CSS lives in the `<style>` block at the top of
> `index.html`, and there is no external CSS/JS. Edit that one file and everything updates.

## Hosting (already on)

GitHub Pages is enabled: **Settings → Pages → Deploy from a branch → `main` / `(root)`**.
Every `git push` to `main` republishes automatically after ~1 minute.

## Customize it

All visible content is in **`index.html`** — search for the text you want to change.

- **Name, title, affiliation** — the `<header class="hero">` block near the top of `<body>`.
- **Photo** — replace `assets/profile.jpg` with your own (portrait orientation works well;
  the frame is a circle). If you rename it, update the `src` on `<img class="portrait">`.
- **Links** — the GitHub and X buttons (in the hero and Contact) point at your accounts.
- **About / Contact** — each is a clearly-marked `<section>` in the `<body>`.

### Change the colors / fonts

Open `index.html` and edit the palette at the top of the `<style>` block:

```css
:root{
  --paper:#faf7f2;   /* page background            */
  --ink:#26241f;     /* main text                  */
  --gold:#9a7b2e;    /* accent (links, flourishes) */
  --measure:660px;   /* reading column width        */
  --serif:Georgia,"Iowan Old Style","Times New Roman","Songti SC",serif;
}
```

### Try a different style

Alternate design drafts (classic serif sidebar, dark tech, bold Swiss modern) live in a
local `previews/` folder that is git-ignored. To switch, copy one over `index.html` and fix
the asset paths (`../assets/` → `assets/`, `../cv.html` → `cv.html`).

### Use a custom domain (optional)

Add a file named `CNAME` containing your domain (e.g. `www.example.com`), set the DNS records
your registrar requires, then configure the domain under Settings → Pages.

---

> ⚠️ **The content is placeholder/fictional.** Names, publications, awards, and courses were
> generated as a template. Replace everything with your real information before sharing the site.
