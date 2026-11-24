# QSys 2027 website

Static landing page for **QSys 2027: IEEE International Conference on Quantum Computing and Communication Systems** (May 24-27, 2027, Dallas, USA; in conjunction with the 27th IEEE CCGrid 2027).

There is no build step, framework or server-side code. It is plain HTML, CSS and a few lines of JavaScript.

```
index.html            the whole page (all content lives here)
assets/css/style.css  styles (light + dark theme)
assets/js/main.js     mobile menu, theme toggle, active-section highlight
assets/img/favicon.svg
.nojekyll             tells GitHub Pages to serve files as-is
```

All paths are relative, so the folder works unchanged at any URL, including
`https://clouds.cis.unimelb.edu.au/qsys2027/`.

## Hosting

**On an existing web server (e.g. clouds.cis.unimelb.edu.au/qsys2027/)**

Copy the folder contents into the `qsys2027/` web directory, replacing the old `index.html`
(keep a backup of the old file first). You don't need to upload `README.md` or `.nojekyll`.

**On GitHub Pages**

Push to GitHub, then go to *Settings → Pages → Build and deployment*, choose *Deploy from a branch*,
pick the branch and `/ (root)`, and save.

**Preview locally**

Open `index.html` in a browser, or run `python3 -m http.server` in this folder and visit http://localhost:8000.

## Updating content

Everything is in `index.html`. Each section has an HTML comment explaining how to edit it.
Placeholders are shown on the page as grey dashed pills that read *To be announced*.

| What | Where in `index.html` | How |
|---|---|---|
| Important dates | `<section id="dates">` | Replace `<span class="tba">To be announced</span>` with `<time datetime="2027-01-31">January 31, 2027</time>`. For an extension, keep the old date wrapped in `<del>…</del>`. |
| Organising roles | `<section id="committee">` | Copy a `<li class="person">` block. Rename or delete the placeholder *Publicity Chairs* and *Publication Chair* groups. |
| Program Committee | `<div class="pc">` | Replace the placeholder with one `<li class="pc-member">` per member. |
| Venue / Registration / Travel | `<section id="attend">` | Replace *To be announced.* with a short summary once CCGrid 2027 publishes details; keep the CCGrid link. |
| Contact e-mail | footer | Replace the placeholder with a `mailto:` link. |

Fonts (Plus Jakarta Sans for headings, Inter for body text) load from Google Fonts. If they can't load,
the page falls back to the system font.
