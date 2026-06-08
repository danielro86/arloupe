# arLoupe — Marketing Site

Static multi-language marketing site for arLoupe (Bewelltech Inc.). No build step, no
dependencies — plain HTML/CSS. Fonts load from Google Fonts and photography from Unsplash
over the network, so the pages need an internet connection to render fully.

## Languages

| Language | Location | Home page |
|----------|----------|-----------|
| English (default) | `/` (root) | `index.html` |
| 简体中文 (Simplified) | `/zh-CN/` | `zh-CN/index.html` |
| 繁體中文 (Traditional) | `/zh-TW/` | `zh-TW/index.html` |

Each language has the same five pages: **Home, Products, About Us, Find a Dealer, Contact.**
The header language switcher (EN · 简 · 繁) links the three versions together, and the
mobile hamburger menu mirrors it. All links are relative, so the site works from any
sub-path or domain root.

## Structure

```
.
├── index.html                Home (EN)
├── About Us.html
├── Products.html
├── Find a Dealer.html
├── Contact.html
├── assets/
│   ├── arloupe-logo.png       Logo (nav + footer)
│   └── world-map-real.png     Find-a-Dealer hero world map
├── zh-CN/                     Simplified Chinese (same 5 pages)
└── zh-TW/                     Traditional Chinese (same 5 pages)
```

## Deploy

Drop the contents of this folder into the root of your repository. The site is fully
static, so any static host works:

**GitHub Pages**
1. Commit these files to your repo (root, or a `/docs` folder).
2. Settings → Pages → Source: your branch, folder `/ (root)` (or `/docs`).
3. The site goes live at `https://<user>.github.io/<repo>/`.

The included empty `.nojekyll` file tells GitHub Pages to serve all files and folders
as-is (no Jekyll processing).

## Notes

- File names contain spaces (e.g. `Find a Dealer.html`); browsers encode these as `%20`
  automatically and all internal links account for it. Keep the names as-is.
- To swap any photo, replace the relevant Unsplash URL in the page's HTML.
- The Find-a-Dealer world map is a single image (`assets/world-map-real.png`); the
  glowing dealer nodes and the highlighted HQ are baked into that image.
