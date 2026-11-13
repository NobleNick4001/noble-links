# noble-links

Public Noble link pages on GitHub Pages. The truck QR page is `wd/` (`/noble-links/wd/`). Brochure QR landing is `wd-brochure/`.

## Resync the product brochures

The public list at `wd-brochure/brochures/` is the sales-app catalog. Titles and files live in one file: `wd-brochure/brochures/brochures.json`. The page only reads that file. PDFs stay on the sales-app site; do not copy them into this repo.

1. Open the `GROUPS` array in `js/pages/brochures.js` on the `main` branch of [Noble-Windows-and-Doors-](https://github.com/NobleNick4001/Noble-Windows-and-Doors-) (raw: `https://raw.githubusercontent.com/NobleNick4001/Noble-Windows-and-Doors-/main/js/pages/brochures.js`).
2. Replace `groups` in `brochures.json` with those groups, in the same order. Keep each group's `id` and `name`, and each item's `label`. Set `file` to the PDF filename only (`brochures/milgard-v250-style-line.pdf` in the app becomes `milgard-v250-style-line.pdf`).
3. Leave `pdfBase` as `https://noblenick4001.github.io/Noble-Windows-and-Doors-/brochures/`. Each box links to `pdfBase` + `file`, opened in a new tab.
4. Before publishing, request every brochure URL and confirm it returns HTTP 200.
