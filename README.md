# Marcella Tambuscio — Quarto academic website

**Design:** Coastal Networks, hybrid palette (sand / aqua / slate blue / charcoal).  
**Intended URL:** <https://mtambuscio.github.io>. This source folder is **not published** merely by downloading it.

## What's in the project

- `_quarto.yml` — Quarto site configuration and navbar (GitHub in CV only)
- `index.qmd` — homepage with original SVG abstract network hero
- `research.qmd` — **Relational Worlds**: Computational Humanities first, then Computational Social Science
- `projects/` — three current project pages plus text-only selected earlier research themes
- `talks.qmd` — chronologically organized talks (including invited talks), plus selected posters; slide links to be added once PDFs are available
- `publications.qmd` — publication list drafted from the supplied CV
- `cv.qmd` — **public-summary** CV and academic service (including HNR), omitting the personal phone number, personal leave data and the original CV file; GitHub link lives here rather than the main menu
- `visualizations/` — future embedding instructions and placeholder page
- `styles.css` — palette, fonts, layouts, responsive styling
- `assets/network-*.svg` — **abstract illustrations**; not analytical network outputs
- `assets/logo-moon-mt.svg` — editable network-crescent **MT monogram**, included in top navigation
- `assets/favicon.svg` — simplified small-size variant

## Preview locally (macOS + VS Code)

1. Install Quarto: <https://quarto.org/docs/get-started/>.
2. Install the **Quarto** extension in VS Code.
3. Unzip the archive and open the `mtambuscio-quarto` directory in VS Code.
4. In its Terminal run:

   ```bash
   quarto --version
   quarto render
   quarto preview
   ```

5. Edit `.qmd` files for the text, `styles.css` for styling, or `assets/network-hero.svg` for the abstract network.

Notes: Font files are **not** bundled. The site requests Libre Baskerville and Source Sans 3 from Google Fonts, with local fallback fonts if unavailable. No JavaScript build pipeline or R/Python environment is required to render the site.

## Publish on GitHub Pages

1. Create a **public**, empty repository named **`mtambuscio.github.io`** on GitHub.
2. Open Terminal in this folder. Replace the URL only if the username or repository changes:

   ```bash
   git init
   git add .
   git commit -m "Start academic website"
   git branch -M main
   git remote add origin https://github.com/mtambuscio/mtambuscio.github.io.git
   git push -u origin main
   ```

3. Publish the rendered site to the `gh-pages` branch:

   ```bash
   quarto publish gh-pages
   ```

4. **For a `username.github.io` user site**, open GitHub **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch → `gh-pages` → `/ (root)` → Save** if GitHub has not selected the branch automatically. The default for a user site can remain `main`, which is not the intended publishing branch here.
5. When active, the site will be visible at <https://mtambuscio.github.io/>.

Official docs: <https://quarto.org/docs/publishing/github-pages.html>.

## Updating after publication

After editing, run:

```bash
git add .
git commit -m "Update site"
git push
quarto publish gh-pages
```

## Data and privacy checklist before publishing

- [ ] Review biography and academic role wording.
- [ ] Supply **exact Google Scholar and LinkedIn profile URLs** to enable those links; none have been guessed or invented.
- [ ] Add selected public slide PDFs to `files/slides/`, then add links in `talks.qmd`; do not publish unreviewed slides.
- [ ] Check 2027 scheduled talk details once finalized.
- [ ] Verify bibliographic entries, dates, DOI links and full metadata (the accepted 2026 paper was listed under 2025 in the original CV).
- [ ] Check project descriptions with collaborators/funders.
- [ ] **Do not upload the original CV PDF** as it contains a personal mobile phone number and leave information. Add a reviewed public copy to `files/` later if desired.
- [ ] Confirm public licensing/data permissions before sharing project networks or real figures.
- [ ] Replace the current project-thumbnail SVG illustrations with actual figures if desired; they are explicitly marked decorative.
- [ ] Test on a mobile device and check links.

This package includes no Google Analytics and no third-party tracking by design. Google Fonts requests are external; you can replace font imports with system fallbacks if preferred.

## Adding presentation slides

Create a directory `files/slides/` and copy reviewed/public presentation PDFs there, e.g. `files/slides/hnr2026-filtering-emperor.pdf`. In `talks.qmd` append inside the corresponding talk-entry: 

```html
<a class="text-link" href="files/slides/hnr2026-filtering-emperor.pdf">Slides (PDF) →</a>
```

No slide links were added yet because the PDFs were not provided. Slides are **optional**; the talks list remains useful without them.

## Brand files

`assets/logo-moon-mt.svg` is a hand-built vector interpretation of the agreed *minimal network crescent with MT in its opening*. All lines, node positions, letter placement and colours are editable in SVG. The favicon is intentionally simplified for small browser tabs.
