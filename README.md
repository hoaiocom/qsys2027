# QSys 2027 website

Landing page for **QSys 2027: IEEE International Conference on Quantum Computing and Communication Systems**, May 24-27, 2027, Dallas–Fort Worth, Texas, USA (in conjunction with the 27th IEEE CCGrid 2027).

It is a plain static site: no build step, no framework, no server-side code.

```
index.html     all page content
assets/css/    styles
assets/js/     menu, theme toggle (optional; the page works without it)
assets/img/    logo and venue photos
```

## Self-hosting

All paths are relative, so the folder works at any URL.

**Any web server** (Apache, Nginx, a university web directory, etc.)

Copy `index.html` and the `assets/` folder into the web directory, for example `public_html/qsys2027/`. Nothing else is needed.

**GitHub Pages**

In the repository, go to *Settings → Pages*, set *Source* to *Deploy from a branch*, select `main` and `/ (root)`, then save. The site appears at `https://<user>.github.io/<repo>/` within a minute or two.

**Local preview**

Open `index.html` in a browser, or run:

```bash
python3 -m http.server 8000
```

and visit <http://localhost:8000>.

## Editing

Everything is in `index.html`. Each section has an HTML comment explaining how to edit it, and placeholders appear on the page as grey "To be announced" pills.

- **Important dates:** edit the rows in `<section id="dates">`. Dates are written as `<time datetime="2027-01-31">January 31, 2027</time>`; three rows currently link to CCGrid 2027 ("Same as CCGrid 2027").
- **Committee:** copy a `<li class="person">` block (organising team) or a `<li class="pc-member">` block (Program Committee).
- **Venue, registration, travel:** replace "To be announced." once CCGrid 2027 publishes details.

## Credits

Venue photos by Carol M. Highsmith, Library of Congress (public domain), via Wikimedia Commons. Fonts: Plus Jakarta Sans and Inter (Google Fonts).
