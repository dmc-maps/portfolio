# Portfolio site - deploy notes

A single static page (`portfolio.html` + `styles.css` + `contours.svg`). No build step, no dependencies. It loads instantly and hosts anywhere.

## Files
- `portfolio.html` - the page (named by project, not index.html)
- `styles.css` - cartographic GIS-professional theme
- `contours.svg` - topographic contour motif used in the hero background
- `DevinClark_Resume.pdf` - linked by the "Download resume" button

## Before you publish (10 minutes)
1. **Confirm the resume PDF is here.** The "Download resume" button points to `DevinClark_Resume.pdf` in this folder. (Regenerate from `../resume/` any time.)
2. **Fill in the four project links.** Each card has an "Add demo link / case summary / sample map" placeholder. Replace `href="#"` with a real URL once each demo or writeup is live (see `../github/github-plan.md`).
3. **Optional: add a screenshot to each card.** A single clean image per project lifts this a lot. Put images in an `img/` folder and add an `<img>` at the top of each `.card`.

## Publish to GitHub Pages (free)
1. Create a repo (suggested name: `portfolio` or `devin-clark`).
2. Add these files to the repo root and push.
3. Repo Settings, then Pages, then Source: `main` branch, `/root`. Save.
4. GitHub Pages serves `index.html` at a directory root. Since this page is `portfolio.html`, either link to `https://<username>.github.io/<repo>/portfolio.html`, or copy `portfolio.html` to `index.html` in the repo for a clean root URL. (Keep `portfolio.html` as your working filename either way.)
5. Live in about a minute.

## Custom domain (optional)
You already have `demo.digitalmappingconsultants.com` pending in Hover. You can point a subdomain (for example `devin.digitalmappingconsultants.com`) at GitHub Pages with a CNAME record, then set it under Settings, Pages, Custom domain. A clean personal URL on your own domain reads more senior than a github.io link.

## Preview locally
A launch config named `portfolio` serves this folder on port 5050. Or run:
```
python -m http.server 5050
```
then open http://localhost:5050/portfolio.html

## Style rules kept
Plain hyphens only (no em or en dashes), one primary accent, understated. Keep it that way when you edit.
