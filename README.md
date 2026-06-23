# 🔬 FTIR Analysis Tool

A fully self-contained, offline FTIR spectral analysis tool for plastic identification — delivered as a **single HTML file**. No installation, no internet connection, and no IT involvement required.

> **▶ Open the live tool:** [siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html](https://siyanaka.github.io/ftir-analysis-tool/FTIR_Analysis_Tool.html)

---

## ✨ Features

- **JCAMP-DX support** — upload `.dx` / `.jdx` spectra directly from your instrument
- **Instant spectral matching** — HQI scores via mean-centered cosine similarity against a built-in reference library
- **Built-in simulated references** — tick any plastic from the panel; no `.dx` files needed for common materials
- **Interactive plot** — zoom, pan, and hover over overlaid spectra powered by Plotly.js
- **Adjustable matching region** — focus HQI on any wavenumber range
- **CO₂ band auto-exclusion** — atmospheric band (2280–2400 cm⁻¹) is always removed from calculations
- **Export results** — download match table as CSV
- **Fully offline** — Plotly.js is bundled inline; works with no internet after the first load
- **Zero dependencies** — open by double-clicking; no Python, Node.js, or any software needed

---

## 🚀 How to Use

### Option 1 — Live (browser, no download)
Click the link above. The tool loads instantly in your browser.

### Option 2 — Fully offline
1. Download `FTIR_Analysis_Tool.html` from this repo
2. Double-click the file — it opens in any browser
3. No installation or internet required

### Workflow

| Step | Action |
|---|---|
| **Reference** | Upload your own `.dx` database files **or** tick Built-in Reference Plastics |
| **Unknown** | Upload the unknown spectrum `.dx` file |
| **Analyse** | HQI table and spectral overlay update automatically |
| **Export** | Download the match results as CSV |

---

## 📊 How Matching Works

Matching uses **mean-centered cosine similarity** (Hit Quality Index, HQI):

1. Both spectra are interpolated onto a shared wavenumber grid
2. The CO₂ atmospheric band (2280–2400 cm⁻¹) is masked out
3. Mean-centering removes baseline offset effects
4. Cosine similarity is computed; result × 100 = HQI %

Higher HQI = closer match. Scores above ~70% generally indicate a strong candidate.

> The matching wavenumber range is user-adjustable in the HQI panel — narrow it to the fingerprint region (400–1800 cm⁻¹) for best discrimination.

---

## 🗂️ Built-in Reference Library

All references are modelled as Gaussian absorption bands using published literature wavenumbers — no proprietary spectral library data is included.

### Conventional Plastics
| Abbreviation | Material |
|---|---|
| PE | Polyethylene |
| PP | Polypropylene (iPP) |
| PS | Polystyrene |
| PVC | Polyvinyl Chloride |
| PET | Polyethylene Terephthalate |
| PC | Polycarbonate |
| PMMA | Acrylic (Plexiglas) |
| ABS | Acrylonitrile-Butadiene-Styrene |
| PUR | Polyurethane |
| PA6 | Nylon 6 |

### Bioplastics & Biodegradable Polymers
| Abbreviation | Material |
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

## 📁 Repository Structure

```
ftir-analysis-tool/
├── FTIR_Analysis_Tool.html   # Complete self-contained application
├── LICENSE                   # MIT License
└── README.md
```

---

## 🛠️ Built With

- [Plotly.js](https://plotly.com/javascript/) (v3.6.0) — interactive spectral visualisation, bundled inline
- Vanilla HTML, CSS, and JavaScript — no frameworks, no build tools

---

## 📋 Requirements

| Requirement | Detail |
|---|---|
| Browser | Chrome, Edge, Firefox, or Safari (any modern version) |
| Internet | Not required after first load |
| Installation | None |
| OS | Windows, macOS, Linux |
| File format | JCAMP-DX (`.dx` / `.jdx`) |

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

Reference spectral data is derived from publicly available literature values. No proprietary commercial spectral library data (e.g. OMNIC, Bio-Rad KnowItAll, Wiley) is included.

---

*Built for offline use in laboratory and corporate environments. Share the link or the file — no setup required.*
