# Global Earthquake & Tsunami Risk — Analytics Dashboard

An interactive multi-page analytics dashboard built in Tableau, exploring global seismic activity from 2000 to 2025 — with an AI-generated forecast extending to 2027.

The dashboard transforms raw earthquake data into a layered risk-assessment tool: from surface-level frequency counts to nuanced regional tsunami probability analysis.

---

## Dashboard Pages

### Page 1 — Risk Overview
| Chart | Type | Key Insight |
|-------|------|-------------|
| Magnitude vs Depth | Scatter plot | Shallow quakes (0–100 km) dominate; orange dots (tsunami) cluster at low depths |
| Risk Parameter Over Time | Dual-line chart | High-risk events are rare but consistent; low-risk events spike in 2011, 2015, 2022 |
| Regional Comparison | Bar + line (dual axis) | South region: only 3 events — but 100% tsunami rate |
| Depth × Magnitude Density | Heatmap | Hotspot: magnitude 6.4, depth 0–25 km |

### Page 2 — Deep Dive
| Chart | Type | Key Insight |
|-------|------|-------------|
| Significance by Tsunami | Box plot | Tsunami events have significantly higher significance scores |
| Global Distribution | Geographic map | Ring of Fire clearly visible; Pacific plate boundaries dominate |
| Annual Frequency + AI Forecast | Line + shaded area | Upward trend predicted through 2027 with confidence interval |
| Frequency by Magnitude | Stacked bar | Low-magnitude (6.4–6.7) events are far more common; tsunami ratio increases with magnitude |
| Risk by Magnitude Range | Packed bubble | Bubble size = frequency; colour intensity = tsunami risk sum |
| Top 10 Significant Events | Horizontal bar | Ranked by significance score with year and magnitude labels |

---

##  Interactive Controls

- **Magnitude Threshold slider** — filters the entire dashboard dynamically; set to any value to isolate high-magnitude events
- **Colour legends** — Tsunami (0/1) and Risk Level (High/Low) explained inline
- **Cross-sheet filtering** — selecting a region or year in one chart highlights related data across all sheets

---

##  AI Forecast

The **Annual Frequency forecast** uses Tableau's built-in exponential smoothing model trained on 2001–2021 data. The shaded confidence band shows prediction uncertainty — wider toward 2027 as expected for longer horizons.

```
Historical data:  2001 – 2021  (actual counts)
Forecast range:   2022 – 2027  (model prediction + 95% CI)
Trend:            General upward trajectory in event frequency
```

---

## Standout Findings

1. **The South region paradox** — fewest earthquakes (3 events) but 100% tsunami occurrence rate — a counterintuitive result that only becomes visible when frequency and probability are plotted together
2. **Shallow = dangerous** — the heatmap confirms that depth 0–25 km at magnitude 6.4 is the single most common seismic profile in the dataset
3. **High-risk events are consistent, not spiky** — unlike low-risk events which fluctuate year to year, high-risk events maintain a steady low baseline

---


## Repository Structure

```
analytics-dashboard-tableau/
├── dashboard.twb              ← Tableau workbook (open this)
├── docs/
│   └── Dashboard_Report.docx  ← Full analysis report with chart descriptions
└── README.md
```

---

## Tech Stack

- **Tool:** Tableau Desktop
- **Dataset:** Global Significant Earthquake Database, 2000–2025
- **Visualisation types:** Scatter, heatmap, bar/line, geographic map, box plot, packed bubble, stacked bar, horizontal bar
- **AI component:** Tableau exponential smoothing forecast

---

##  Author

**Manaeva Daria** · [mandariiii19](https://github.com/mandariiii19)  

