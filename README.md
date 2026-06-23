# 🔬 FTIR Analysis Tool

[![GitHub Pages](https://img.shields.io/badge/Live%20Tool-GitHub%20Pages-brightgreen?logo=github)](https://siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Plotly.js](https://img.shields.io/badge/Plotly.js-v3.6.0-purple)](https://plotly.com/javascript/)
[![No dependencies](https://img.shields.io/badge/Dependencies-None-orange)](#)

A fully self-contained, offline FTIR spectral analysis tool for plastic identification — delivered as a **single HTML file**. No installation, no internet connection, and no IT involvement required.

> **▶ Open the live tool:**
> ### [siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html](https://siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html)

---

## ✨ Features

| Feature | Detail |
|---|---|
| **JCAMP-DX upload** | Load `.dx` / `.jdx` spectra directly from your instrument |
| **Built-in reference library** | 20 plastics (conventional + bioplastics) — tick to activate, no files needed |
| **HQI matching** | Mean-centered cosine similarity, ranked results table |
| **Interactive plot** | Zoom, pan, hover — powered by Plotly.js (bundled inline) |
| **Adjustable match region** | Focus HQI on any wavenumber range |
| **CO₂ auto-exclusion** | Atmospheric band 2280–2400 cm⁻¹ always masked |
| **CSV export** | Download the full match results table |
| **Fully offline** | Works with zero internet after first page load |

---

## 🚀 Quick Start

### Option 1 — No download (browser)
Click the link above. Works instantly.

### Option 2 — Fully offline
1. Download [`FTIR_Analysis_Tool.html`](FTIR_Analysis_Tool.html)
2. Double-click → opens in any modern browser
3. No installation, no internet, no IT ticket needed

### Typical workflow

```
1. Reference spectra   →  Upload .dx files  OR  tick built-in plastics
2. Unknown spectrum    →  Upload unknown .dx file
3. Results            →  HQI table updates automatically
4. Export             →  Download CSV
```

---

## 📊 How HQI Matching Works

The **Hit Quality Index (HQI)** is computed via mean-centered cosine similarity:

1. Both spectra are interpolated onto a shared wavenumber grid
2. CO₂ atmospheric band (2280–2400 cm⁻¹) is masked
3. Mean-centering removes baseline offset
4. Cosine similarity is computed → multiplied by 100 = HQI %

**HQI ≥ 70 %** generally indicates a strong candidate match.

> 💡 Narrow the matching range to the fingerprint region (400–1800 cm⁻¹) for best polymer discrimination.

---

## 🗂️ Built-in Reference Library

All references are **Gaussian band models** parameterised from published literature wavenumbers — no proprietary spectral library data is included.

### Conventional Plastics
| ID | Material |
|---|---|
| PE | Polyethylene |
| PP | Polypropylene (iPP) |
| PS | Polystyrene |
| PVC | Polyvinyl Chloride |
| PET | Polyethylene Terephthalate |
| PC | Polycarbonate |
| PMMA | Acrylic / Plexiglas |
| ABS | Acrylonitrile-Butadiene-Styrene |
| PUR | Polyurethane |
| PA6 | Nylon 6 |

### Bioplastics & Biodegradable Polymers
| ID | Material |
|---|---|
| PLA | Polylactic Acid |
| PBAT | Polybutylene Adipate-Terephthalate |
| PBS | Polybutylene Succinate |
| PBSA | Polybutylene Succinate-co-Adipate |
| PHB | Polyhydroxybutyrate (PHA) |
| PHBV | Poly(3-HB-co-3-HV) |
| PCL | Polycaprolactone |
| TPS | Thermoplastic Starch |
| CA | Cellulose Acetate |
| PVOH | Polyvinyl Alcohol |

---

## 📁 Repository

```
ftir-analysis-tool/
├── FTIR_Analysis_Tool.html   # Complete self-contained application (~4.7 MB)
├── LICENSE                   # MIT License
└── README.md
```

---

## 🛠️ Built With

- [Plotly.js v3.6.0](https://plotly.com/javascript/) — interactive spectral visualisation, bundled inline (MIT)
- Vanilla HTML + CSS + JavaScript — no frameworks, no build tools, no bundler

---

## 📋 Requirements

| | |
|---|---|
| **Browser** | Chrome, Edge, Firefox, Safari (any modern version) |
| **Internet** | Not required after first load |
| **Installation** | None |
| **OS** | Windows, macOS, Linux |
| **Input format** | JCAMP-DX (`.dx` / `.jdx`) |

---

## 📄 License

MIT — see [LICENSE](LICENSE).

Reference spectral data is derived from publicly available literature wavenumber values modelled as Gaussian absorption bands. No data from proprietary commercial spectral libraries (OMNIC, Bio-Rad KnowItAll, Wiley, etc.) is included.

---

*Built for offline use in laboratory and corporate environments — share the link or the HTML file with colleagues, no setup required.*
