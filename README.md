# Portfolio site - deploy notes

Static site, no build step, no dependencies. Entry point is `index.html`.

## Files
- `index.html` - the homepage (GitHub Pages serves this at the domain root)
- `facade-viewer.html`, `web-maps.html`, `railroad-corridor.html`, `court-exhibits.html` - the four case-study pages
- `styles.css` - cartographic GIS-professional theme
- `contours.svg` - topographic contour motif used in the hero
- `DevinClark_Resume.pdf` - linked by the "Download resume" button
- `img/` - card and case-study images

## Deploy to GitHub Pages (repo: dmc-maps/portfolio)
1. Put every file in this folder (including `img/`) at the root of the `dmc-maps/portfolio` repo.
2. Keep the `CNAME` file in the repo (it holds `portfolio.digitalmappingconsultants.com`).
3. Commit and push (GitHub Desktop: review changes, commit, push).
4. Repo Settings, then Pages: Source `main` branch, `/root`. The custom-domain DNS check passes once propagation finishes, then tick "Enforce HTTPS" once it is no longer grayed out.
5. Live at https://portfolio.digitalmappingconsultants.com

The entry must stay named `index.html` so the domain root serves the homepage. The case pages keep their project names.

## DNS (already configured)
DNS for digitalmappingconsultants.com is hosted at WordPress.com (nameservers ns1/ns2/ns3.wordpress.com), not Hover. A CNAME `portfolio -> dmc-maps.github.io` is set there. To put the facade demo on its own subdomain later, add another CNAME the same way at WordPress.com.

## Preview locally
A launch config named `portfolio` serves this folder on port 5050. Or run:
```
python -m http.server 5050
```
then open http://localhost:5050

## Style rules kept
Plain hyphens only (no em or en dashes), no decorative accents, one primary accent, understated. Keep it that way when you edit.
