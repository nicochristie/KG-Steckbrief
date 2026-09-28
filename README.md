# KG-Steckbrief

A fillable, single-page "Steckbrief" (profile sheet) parents fill out when running for the Kita's Elternbeirat. Five switchable designs, works in any browser, no server needed.

**Live page:** enable GitHub Pages first (see below), then it's at
`https://nicochristie.github.io/KG-Steckbrief/`

## Repo layout
- `index.html` — the whole site: one self-contained HTML file (fonts load from Google Fonts CDN, PDF export loads html2canvas/jsPDF from cdnjs; everything else is inline).
- `original/Steckbriefleer.docx` — the old Word template this replaces. Kept for reference only, not linked from the page.
- `.nojekyll` — tells GitHub Pages to serve files as-is instead of running them through Jekyll.

## Turning on GitHub Pages
Repo → **Settings → Pages** → under "Build and deployment", set **Source: Deploy from a branch**, **Branch: master**, folder **/ (root)** → Save. The site is live at the URL above a minute or two later, and republishes automatically on every push to `master`.

## Before sharing the link with parents
- **Recipient e-mail:** open `index.html`, find `const MAIL_AN = '';` near the top of the `<script>`, and fill in the address the finished PDFs should be sent to. Leave it empty and parents type in an address themselves.
- **Required fields:** the `PFLICHT` list right below it controls which fields must be filled in before the PDF/e-mail buttons unlock.
- The repo is public (required for free GitHub Pages), so don't put anything in it beyond this template — no filled-in parent data ever goes into the repo; it only ever lives in each parent's own browser and PDF download.
