# Lunamisni PDF workspace

## Run locally

Open PowerShell in this folder and run:

```powershell
node generate-pages.mjs
node server.mjs
```

Then open [http://localhost:4173](http://localhost:4173). Stop the server with Ctrl+C. Node.js 18 or newer is recommended. PDF.js, pdf-lib and the AES-256 security engine are bundled in `vendor/`. PDF operations happen in the browser; files are not sent to a Lunamisni server.

## Design and layout

- Colors: deep navy `#0C172B`, cobalt `#4778F5`, mint `#59CFC1`, lilac `#A694FA`, and near-white surfaces.
- Fonts: Manrope headings and DM Sans body text, with system fallbacks.
- There are 13 individual tool pages, an All Tools index, an Edit PDFs in One Workspace page, and separate Privacy, Terms and About pages.
- Individual workspaces use an upload panel, centered preview, selectable page thumbnails when relevant, and a single Convert button that becomes Download result when processing succeeds.
- Layout adapts to mobile and desktop. Files are added locally; Merge PDF supports multiple files at once or repeated add-file steps.

## Current tool status

13 tools are enabled and locally verified. PDF to PDF/A has been removed as requested. The six tools removed at the user's request are OCR, Permanent Redact, Flatten Forms, Interactive Form Builder, Visual Crop and Repair.

See [TOOL-QA.md](TOOL-QA.md) for the operation checks and [SEO-BEYONDSEO.md](SEO-BEYONDSEO.md) for Blogger publishing and SEO setup.

## Third-party notices

The AES-256 browser engine is built from `@libpdf/core` and its dependencies. PDF.js and pdf-lib are also included. Include the upstream license notices when distributing the bundled dependencies; check `vendor/` and upstream packages for their respective license terms.
