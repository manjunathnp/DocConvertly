# DocConvertly v1.0.0

Convert and edit documents privately in your browser.

**12 document tools** · **No account** · **Files stay on your device** · **One HTML file**

DocConvertly is a collection of document conversion and PDF editing tools that runs locally in a browser tab. Documents are processed on the user’s device and returned as downloadable files.

## Download and run

1. Download [docconvertly-v1.0.0.html](https://github.com/manjunathnp/DocConvertly/releases/download/v1.0.0/docconvertly-v1.0.0.html) from the [v1.0.0 release](https://github.com/manjunathnp/DocConvertly/releases/tag/v1.0.0).
2. Open the downloaded HTML file in your browser.
3. Choose a tool, select your files, and download the results.

The logo, favicon, styles, and application code are embedded in the HTML. No asset folder, installation, or local server is needed. An internet connection is required to load the document-processing libraries from cdnjs; this is not a fully offline application.

## Features

- Local, browser-based document processing
- No account, backend, analytics, or conversion server
- Drag-and-drop file selection
- Multiple-file workflows with reorder controls
- Job-specific conversion settings
- Light and dark themes
- Individual downloads and ZIP bundles
- Responsive layouts for desktop, tablet, and mobile
- Keyboard-accessible controls and reduced-motion support

## Included tools

| Tool | What it does |
| --- | --- |
| Images to PDF | Combines supported images into one PDF or separate PDF files. |
| PDF to images | Renders selected PDF pages as images. |
| Convert images | Converts and resizes supported image formats. |
| Word to PDF | Partially converts DOCX text and basic structure to PDF. |
| PDF to Word | Partially extracts readable PDF text into a DOCX document. |
| PDF to text | Extracts text from PDFs that contain a text layer. |
| Merge PDF | Combines multiple PDFs in the selected order. |
| Split PDF | Extracts page ranges or separates pages into individual files. |
| Compress PDF | Re-renders pages to reduce file size when possible. |
| Edit PDF pages | Reorders, rotates, and removes PDF pages. |
| Watermark PDF | Places configurable text watermarks on PDF pages. |
| Page numbers | Adds page numbers with configurable position, style, and starting number. |

Word to PDF and PDF to Word are clearly marked **Partial** in the interface because browser-only Office conversion cannot preserve every layout feature.

## Privacy

DocConvertly reads and processes selected documents inside the current browser tab. Document contents are not sent to a conversion service, and original files are not modified.

The application loads its processing libraries from cdnjs. Those library requests do not contain document contents. Generated results remain in tab memory until they are downloaded, replaced, or lost when the page is closed or reloaded.

## Limitations

- Word conversions do not preserve complex layouts, images, columns, exact fonts, headers, footers, or precise spacing.
- PDF text extraction requires an existing text layer; OCR is not included.
- Password-protected PDFs must be unlocked before use.
- Compression rasterizes pages and can remove selectable or searchable text.
- A document that is already efficiently compressed may not become smaller.
- Browser memory can limit large batches, complex documents, and high-resolution rendering before the stated per-file size limit is reached.
- Inputs, settings, and results are not persisted across page reloads or closed tabs.

## Browser support

DocConvertly is designed for current desktop and mobile browsers with JavaScript, the File API, canvas, Web Workers, and Blob downloads available. Behavior can vary with browser memory limits and download policies.

## Dependencies

| Library | Version | Purpose |
| --- | --- | --- |
| [pdf-lib](https://github.com/Hopding/pdf-lib) | 1.17.1 | PDF creation and editing |
| [PDF.js](https://github.com/mozilla/pdf.js) | 3.11.174 | PDF rendering and text extraction |
| [JSZip](https://github.com/Stuk/jszip) | 3.10.1 | ZIP archives and DOCX package handling |
| [Mammoth](https://github.com/mwilliamson/mammoth.js) | 1.6.0 | DOCX text and structure conversion |

## Quality assurance

The application has browser-based coverage for:

- All twelve conversion engines with synthetic PDF, PNG, and DOCX inputs
- Responsive geometry from 320 px to 1440 px
- Empty, unsupported, and corrupt files
- Keyboard and pointer interaction
- File ordering and directional controls
- Dark theme presentation
- Long Unicode filenames
- Duplicate conversion attempts
- Navigation while file loading or conversion is still pending
- Recovery after a failed conversion

QA scripts and screenshots are kept locally and are not included in the repository. Coverage does not establish compatibility with every browser, document layout, or file size.

## Project files

The repository contains exactly two files:

| Path | Description |
| --- | --- |
| `docconvertly-v1.0.0.html` | Single-file application with embedded logo and favicon |
| `README.md` | Download instructions and project documentation |

## Release v1.0.0

- Initial public release with twelve document tools.
- Embedded branding so the downloaded HTML displays its logo without companion files.
- Two-file distribution: the application and this README.

## Licence

DocConvertly identifies its application source as MIT licensed. The included third-party libraries and brand marks retain their respective licences and rights.

## Developer

**Manjunath N P**

[Website](https://manjunathnp.in) · [LinkedIn](https://linkedin.com/in/manjunathnp) · [GitHub](https://github.com/manjunathnp)
