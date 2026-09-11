# Alpine Updraft AI Data Center

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)
[![Format: IEEEtran](https://img.shields.io/badge/LaTeX-IEEEtran-blue.svg)](paper.tex)
[![Status: Open Research](https://img.shields.io/badge/Status-Open%20Research-green.svg)](#)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22698911.svg)](https://doi.org/10.5281/zenodo.22698911)

> **Thermodynamische und techno-ökonomische Bewertung unterirdischer Naturzug-Schrägschächte zur passiven Kühlung und Energierückgewinnung in Hyperscale-KI-Rechenzentren**  
> **Autor:** Chu Duc Kien ([mailiekien@icloud.com](mailto:mailiekien@icloud.com))  
> **Preprint:** [doi:10.5281/zenodo.22698911](https://doi.org/10.5281/zenodo.22698911) (Concept-DOI, zeigt immer auf die aktuelle Version) · v2: [doi:10.5281/zenodo.22707524](https://doi.org/10.5281/zenodo.22707524) · v1 (überholt): [doi:10.5281/zenodo.22698912](https://doi.org/10.5281/zenodo.22698912)

> **Revision v2 (September 2026):** Eine unabhängige Nachrechnung hat drei Fehler in der Erstfassung aufgedeckt: Die Turbinenleistung (2,25 MW) war aus der eigenen Druckverlustbilanz nicht herleitbar (korrekt ≈ 1,4 MW), die Schachtgeometrie war intern inkonsistent, und der Kapitalwert (+162,3 Mio. €) ließ sich aus der angegebenen Formel nicht reproduzieren (korrekt ≈ −49 Mio. € im Basisszenario). Das Fazit lautet jetzt: **thermodynamisch robust, im Basisszenario wirtschaftlich nicht tragfähig, positiv erst bei hohen Wasser-/Strompreisen.** Details im Revisionsvermerk am Ende von `paper.tex`.

> **Status-Hinweis:** Dies ist eine unabhängige, nicht begutachtete Vorab-Veröffentlichung (Preprint) auf Zenodo. Es handelt sich um ein Konzeptpapier mit techno-ökonomischer Modellierung, nicht um eine peer-reviewte Publikation in einem Fachjournal. Rückmeldungen und fachliche Prüfung sind ausdrücklich erwünscht.

---

## 📌 Executive Summary

Modern AI clusters (Nvidia H100 / H200 / B200) require datacenter power capacities in the hundreds of megawatts. Heat dissipation from Direct Liquid Cooling (DLC) at 55–65 °C creates a severe environmental bottleneck: conventional dry cooling demands megawatts of parasitic fan power, while evaporative cooling consumes billions of liters of fresh water per year.

This repository presents an open infrastructure research paper proposing the coupling of a **100 MW AI datacenter** with a **1,500m inclined underground mountain shaft** (3,000m tunnel at 30° slope) in alpine geology.

```mermaid
graph TD
    A["100 MW AI Cluster (DLC Waste Heat 90 MWth @ 60°C)"] --> B["Base Liquid-to-Air Heat Exchanger"]
    B -->|Heat Differential ΔT = 20K| C["1,500m Vertical Inclined Mountain Shaft"]
    C -->|Thermosiphon Airflow ~4,480 kg/s| D["Base Axial Turbines"]
    D -->|+1.4 MWel Electricity Generation| E["Net Grid / Facility Power"]
    C -->|Peak Summit Exhaust| F["Zero-Water Passive Dry Cooling (PUE ~1.016)"]
```

---

## 🚀 Key Performance Indicators (KPIs)

| Metric | Industry Standard (100 MW) | Alpine Updraft Shaft | Impact |
|---|---|---|---|
| **PUE (Power Usage Effectiveness)** | 1.15 – 1.25 | **~1.016** (1.03 without turbine credit) | Eliminates ~4 MW fan power |
| **WUE (Water Usage Effectiveness)** | 1.5 – 2.0 L/kWh (~1.58B L/yr) | **0.0 L/kWh** | **100% Zero Water Consumption** |
| **Energy Recovery** | 0.0 MW | **+1.41 MWel Net** | Recovers power via base turbines (~41 % of static draft available to turbine) |
| **Annual OPEX Savings** | Baseline | **~€9.43 Million / year** | Fan power + Water + Maintenance + Turbine |
| **50-Year Net Present Value (NPV50, r = 6 %)** | Baseline | **−€49.3 Million** (base case) | Does **not** amortize €198M net CapEx at €0.10/kWh and €2.50/m³; positive only at water ≥ €5/m³ or combined high energy/water prices |

---

## 📁 Repository Structure

```
├── paper.tex              # Complete IEEEtran LaTeX paper (ready to compile)
├── paper_konzept.md       # Comprehensive German markdown summary & analysis
├── README.md              # Project overview & quickstart
├── CITATION.cff           # Citation metadata for academic references
├── LICENSE                # Open Research License (MIT & CC-BY-4.0)
└── promo/
    ├── HACKER_NEWS_POST.md    # Launch strategy & submission text for Hacker News
    └── TWITTER_THREAD.md      # Launch copy & thread structure for X/Twitter
```

---

## 🛠️ How to Compile the LaTeX Paper

You can compile [`paper.tex`](paper.tex) locally using TeX Live / MacTeX, or online via Overleaf:

```bash
# Using pdflatex
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex

# Or using Tectonic
tectonic paper.tex
```

---

## 📖 Citation

If you use this research, formulas, or concepts in your work, please cite it using BibTeX:

```bibtex
@techreport{alpine_updraft_datacenter_2026,
  title={Thermodynamische und techno-oekonomische Bewertung unterirdischer Naturzug-Schraegschaechte zur passiven Kuehlung und Energierueckgewinnung in Hyperscale-KI-Rechenzentren},
  author={Chu, Duc Kien},
  year={2026},
  institution={Independent Research},
  note={Preprint, Revision v2},
  doi={10.5281/zenodo.22698911},
  url={https://doi.org/10.5281/zenodo.22698911}
}
```

---

## 📜 License

Distributed under the [MIT License](LICENSE) and [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/).

---

## 🤖 Methodik-Hinweis

Die technischen Berechnungen (Thermodynamik, CapEx/OPEX-Modellierung) wurden mit KI-gestützten Recherche- und Rechenwerkzeugen erstellt und vom Autor konzeptionell geprüft. Eine unabhängige fachliche Validierung durch Experten aus Verfahrenstechnik/Bauingenieurwesen steht noch aus — Feedback ist willkommen.
