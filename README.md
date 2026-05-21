# XPT Converter

A simple, private, browser-based tool to convert **SAS Transport (`.xpt`) files** into **CSV** or **Excel (`.xlsx`)** formats.

Upload one or many `.xpt` files, then download each as CSV or Excel with a single click. Everything runs entirely in your browser — your data never leaves your computer.

🔗 **Live app:** `https://<your-username>.github.io/xpt-converter/`

---

## Features

- **Drag & drop** one or multiple `.xpt` files (or browse to select).
- **Two export options per file** — download as **CSV** or **Excel**, whichever you need.
- **Bulk convert** — turn every uploaded file into CSV or Excel in one click.
- **100% private** — files are parsed locally in your browser. Nothing is uploaded to any server.
- **Multi-dataset support** — `.xpt` files containing multiple members export each one as its own sheet (Excel) or its own file (CSV).
- **No installation** — it's a single HTML file. Just open it in any modern browser.

---

## How to use

1. Open the [live app](https://<your-username>.github.io/xpt-converter/) (or open `index.html` locally).
2. Drag your `.xpt` file(s) onto the drop zone, or click to browse.
3. For each file, click **Download CSV** or **Download Excel**.
4. The converted file saves straight to your computer.

---

## Supported formats

- **Input:** SAS Transport V5 / V6 (`.xpt`), including CDISC SDTM and ADaM datasets.
- **Output:** `.csv` and `.xlsx` (Excel).

---

## How it works

The app reads the raw `.xpt` binary directly in the browser and parses the SAS Transport structure (library, member, NAMESTR, and OBS records). Numeric values stored in IBM hexadecimal floating-point format are decoded back to standard numbers, and the resulting tables are exported using the [SheetJS](https://sheetjs.com/) library for Excel and a built-in writer for CSV.

Because all processing happens client-side, there is no backend, no build step, and no data ever transmitted over the network.

---

## Running locally

No setup required — just download `index.html` and double-click it to open in your browser. An internet connection is needed only so the page can load the Excel export library from a CDN.

---

## Tech stack

- HTML, CSS, and vanilla JavaScript (no framework)
- [SheetJS (xlsx)](https://sheetjs.com/) for Excel export
- Custom in-browser SAS Transport (XPT) parser

---

## Author

Built by **Vishwa**.

---

## License

Free to use and share.
