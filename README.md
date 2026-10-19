# Korash Assani — personal website

A static website for GitHub Pages, written in HTML and CSS. No build step is needed.

## Publish the complete website

1. Extract the ZIP on your computer.
2. Open the extracted folder. Upload its **contents** into the root of your existing `korashassani.github.io` repository. Keep the `assets` folder intact. Do not upload the ZIP itself or put everything inside another folder.
3. Replace the existing HTML pages and `styles.css` when prompted.
4. Commit the changes and wait for the GitHub Pages deployment to finish.
5. Open your website. All pages use `styles.css?v=20261019-2` to request the new stylesheet instead of an old cached copy.

Keep your existing GitHub Pages publishing settings and repository URL.

## Files

- `index.html`: homepage, biography, and selected research.
- `research.html`: research themes, figures, and paper links.
- `publications.html`: first-author and selected collaborative papers.
- `teaching.html`: teaching and mentorship.
- `cv.html`: CV information and download link.
- `contact.html`: email and professional links.
- `styles.css`: shared colors, typography, layout, and responsive styles.
- `assets/`: images, research figures, and existing CV PDFs.
- `homepage-preview.html`: a readable copy of the homepage, using the same stylesheet and assets. It needs those files alongside it.
- `.prettierrc.json`: optional formatting settings, for consistent future edits.
- `.nojekyll`: tells GitHub Pages to serve these static files directly.

## Preview locally

Open `index.html` in a browser after extracting the complete folder. Alternatively, run:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Editing

The source uses two-space indentation and descriptive section comments. Edit text in the relevant HTML page. Shared navigation and footer markup are repeated in each page, so update all pages when changing them.

To change colors, edit the CSS custom properties under `:root` in `styles.css`.

When you change the stylesheet again, update its version query in every HTML page, for example `styles.css?v=20261020-1`. This helps returning visitors receive the new styling.

To format files consistently (optional):

```sh
npx prettier@3.6.2 --write "*.html" styles.css README.md .prettierrc.json
```

## CV

The CV PDF is carried over from the previous website. Replace `assets/Korash_Assani_CV.pdf` with your updated version, then revise the note on `cv.html`.

## Image credits

- Cosmic Cliffs: NASA, ESA, CSA, STScI. https://esawebb.org/images/weic2205a/
- Portrait: supplied by Korash Assani.
- Cosmic-ray schematic: Assani et al. (2026), Figure 4. https://arxiv.org/abs/2607.09407
- Extinction schematic and beta curves: Assani et al. (2025), Figures 6 and 4. https://arxiv.org/abs/2504.02136
- Iron jet channel maps: Assani et al. (2024), Figure 6. https://arxiv.org/abs/2404.18334

Figures are cropped from the papers with axes and labels preserved. The extinction schematic includes material adapted in the paper from van Dishoeck et al. (2011).
