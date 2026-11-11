# Lunamisni PDF tool verification

Checked in the local browser at `http://localhost:4173` with the supplied local sample PDFs. Each enabled operation returned a downloadable result. These are functional checks with small sample files, not a compatibility or security certification.

## Enabled and verified

- Merge PDF — added a second file in a separate selection and confirmed both PDFs remained in the list; conversion produced a combined PDF.
- Split PDF — displayed three page tiles, extracted a selected page, and produced a PDF download.
- Compress PDF — processed the sample and produced output. The sample was already small, so it did not shrink further.
- Rotate PDF Pages — applied a rotation to selected pages and produced a PDF.
- Organize Pages — selected pages moved to the front in custom click order while all other PDF pages remained after them.
- PDF to Markdown — selected a page and produced a Markdown download.
- Compare PDFs — compared two files and produced a Markdown report.
- Metadata Sanitizer — produced a metadata-cleared PDF.
- Bates Numbering — numbered selected pages and produced a PDF.
- N-Up / Booklet — placed selected pages on a sheet and produced a PDF.
- E-Sign PDF — verified drawn signatures and uploaded signature images, adjustable ink color, selected-page signing and downloadable output.
- Protect PDF — created an AES-256 protected PDF with a test password; the result was then opened in Unlock PDF.
- Unlock PDF — removed protection from the test output with the correct password and produced a PDF.

## Removed at the user's request

Local OCR, Permanent Redact PDF, Flatten PDF Forms, Interactive Form Builder, Visual Crop PDF, Repair PDF and PDF to PDF/A.

## Behavior notes

- Page tiles are available for Split, Rotate, Organize, PDF to Markdown, Bates Numbering, N-Up and E-Sign.
- Leaving pages unselected applies the operation to all pages, except Organize, which keeps the original order.
- Organize puts selected pages first in click order, then appends all unselected pages in their original order.
- Changing settings or page selections after conversion restores the Convert action. In Edit PDFs in One Workspace, switching tools carries the latest PDF result forward.
- PDF drop handling is shared across the entire workspace; signature images have a separate upload control.
- The rotation tool shows a live preview of the selected page and angle.
- Rotation supports arbitrary angles; angles other than 0°, 90°, 180° and 270° rasterize selected pages.
- Compare PDFs compares extracted text; it does not highlight visual differences.
- Compression may preserve selectable text or rasterize pages when that produces a smaller result.
