# TimeValue — Future & Present Value Calculator

A single-file, offline-first HTML tool for calculating the **Future Value (FV)** and **Present Value (PV)** of money using standard time-value-of-money compounding formulas. Built with plain HTML/CSS/JS plus embedded SheetJS (Excel import) and jsPDF (PDF export) libraries — no server, no build step, no internet connection required after download.

## Features

- **FV / PV modes** — toggle between calculating Future Value or Present Value using the compound interest formula `FV = PV × (1 + r)ⁿ`
- **Interactive inputs** — principal amount, interest rate, and time period, each with a number field and a synced slider
- **Live formula box** — shows the formula worked out with your actual numbers as you type
- **Result card** — highlighted gradient card displaying the final calculated value
- **Growth chart** — canvas-based, animated compounding curve with:
  - Mouse-wheel zoom and click-drag pan
  - Touch pinch-to-zoom and drag-to-pan on mobile
  - Multiple scenario overlays for side-by-side comparison
- **Scenario comparison** — save multiple input sets and plot them together on the same chart
- **Excel import** — drag-and-drop or upload an `.xlsx` file (via SheetJS) to pull in data
- **PDF export** — generates a `timevalue-report.pdf` summarizing all saved scenarios (via jsPDF)
- **Fully offline** — works with no network connection; indicated by the "offline" status pill in the header
- **Responsive layout** — collapses to a single column below 920px width

## Tech Stack

- Vanilla HTML, CSS, and JavaScript (no framework, no build tools)
- [SheetJS (xlsx.js)](https://sheetjs.com/) — bundled inline for Excel file parsing
- [jsPDF](https://github.com/parallax/jsPDF) — bundled inline for PDF report generation
- HTML5 Canvas — custom chart rendering engine with zoom/pan support

## Usage

1. Open `timevalue-calculator.html` in any modern browser (Chrome, Edge, Firefox, Safari).
2. Choose **Future Value** or **Present Value** mode from the toggle at the top.
3. Enter your principal, interest rate, and time period (or drag the sliders).
4. View the live result and growth chart update instantly.
5. Optionally:
   - Click **Add Scenario** to save the current inputs and compare multiple curves.
   - Drag an `.xlsx` file onto the dropzone to import data.
   - Click **Export PDF** to download a report of all saved scenarios.

No installation, server, or internet connection is required — just open the file.

## File Structure

This is intentionally a **single self-contained HTML file** — all CSS, JavaScript, and third-party libraries (SheetJS, jsPDF) are embedded inline. This makes it fully portable: copy the one file anywhere and it works.

## Browser Support

Works in all modern browsers with Canvas, `<input type="range">`, and ES5+ JavaScript support. Touch gestures (pinch-zoom, drag-pan) are supported on mobile browsers.

## License

This project is licensed under the MIT License.
