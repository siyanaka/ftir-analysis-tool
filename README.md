# 🔬 FTIR Analysis Tool

A fully self-contained, offline FTIR spectral analysis tool delivered as a **single HTML file** — no installation, no internet connection, and no IT involvement required.

> **Live tool:** [Open in browser](https://siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html)

---

## ✨ Features

- **Instant spectral matching** — upload your FTIR spectrum and get ranked matches against a built-in reference library using cosine similarity (HQI scoring)
- **Built-in reference library** — covers conventional plastics (PE, PP, PS, PVC, PET, Nylon, and more) and bioplastics/biodegradable polymers (PLA, PBAT, PBS, PHB, and more)
- **Interactive plot** — zoom, pan, and hover over spectral overlays powered by Plotly.js
- **Adjustable matching region** — define custom wavenumber ranges to focus the HQI calculation
- **CO₂ band exclusion** — atmospheric CO₂ band (2280–2400 cm⁻¹) is automatically excluded from all calculations
- **Fully offline** — all libraries are bundled inline; works with no internet after the first load
- **Zero dependencies** — open by double-clicking; no Python, Node.js, or any software needed

---

## 🚀 How to Use

### Option 1 — Use the live link
Click the link above. The tool loads directly in your browser.

### Option 2 — Run locally (fully offline)
1. Download `FTIR_Analysis_Tool.html` from this repo
2. Double-click the file — it opens in your browser
3. No installation or internet connection needed

### Uploading your spectrum
- Supported format: **CSV** with two columns — wavenumber (cm⁻¹) and absorbance/transmittance
- The tool auto-detects column order
- Multiple spectra can be uploaded and compared simultaneously

---

## 📊 How Matching Works

The tool calculates a **Hit Quality Index (HQI)** using mean-centered cosine similarity between your uploaded spectrum and each reference material. Scores range from 0–100%, where higher means a better match.

- Spectra are interpolated onto a common wavenumber grid before comparison
- The CO₂ atmospheric band (2280–2400 cm⁻¹) is always excluded
- Matching wavenumber range is user-adjustable in the HQI panel

---

## 📁 File Structure

```
ftir-analysis-tool/
└── FTIR_Analysis_Tool.html   # The entire application (self-contained)
```

---

## 🛠️ Built With

- [Plotly.js](https://plotly.com/javascript/) — interactive spectral visualization (bundled inline)
- Vanilla HTML, CSS, and JavaScript — no frameworks or build tools

---

## 📋 Requirements

| Requirement | Detail |
|---|---|
| Browser | Any modern browser (Chrome, Edge, Firefox, Safari) |
| Internet | Not required after first load |
| Installation | None |
| OS | Windows, macOS, Linux |

---

## 🗂️ Reference Library

### Conventional Plastics
PE, PP, PS, PVC, PET, PES, PC, Nylon 6, Nylon 6,6, PMMA, ABS, PU, PTFE, EVA, Cellophane

### Bioplastics & Biodegradable Polymers
PLA, PBAT, PBS, PBSA, PHA, PHB, PHBV, PCL, TPS, CA, PEF, Bio-PE, Bio-PP, Bio-PET

---

## 📄 License

This project is for internal research and analytical use.

---

*Built for offline use in corporate and laboratory environments — share the link or the file with colleagues, no setup required.*
