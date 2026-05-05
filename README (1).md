# 🚗 EIC Vehicle Insurance Analytics Dashboard

> **"The Sad Tale of EIC"** — A deep-dive into the financial collapse of Ethiopia's largest motor insurer through data.

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![License](https://img.shields.io/badge/License-CC%20BY%204.0-green?style=for-the-badge)
![Data Source](https://img.shields.io/badge/Data-Mendeley%20Data-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

---

## 📖 Background

**EIC (Ethiopian Insurance Corporation)** was one of the most prominent motor insurers in Ethiopia during **2014–2018**. Despite its size and market position, the company suffered consistent insurance losses and **closed operations in 2019**.

This project analyses their complete vehicle insurance portfolio using Power BI to uncover the financial patterns, risk trends, and underwriting failures that led to EIC's collapse.

---

## 📊 Dashboard Preview

### Main Report Page
The main dashboard surfaces all key performance indicators across the full portfolio — premiums, claims, policy counts, and segment breakdowns.

| KPI | Value |
|-----|-------|
| 📋 Open Policies | **130K** |
| 💰 Total Premium | **₹ 1 Billion** |
| 📉 Total Claims | **₹ 3 Billion** |
| ⚠️ Premium-to-Claims Ratio | **39%** |
| 📌 Average Premium | **₹ 8K** |
| 🔴 Average Claim | **₹ 20K** |
| 🔢 Claim Count | **10K** |

> **Critical Signal:** A P:C ratio of 39% means EIC paid out **₹2.56 in claims for every ₹1 collected in premium** — a structurally loss-making portfolio.

---

## 🗂️ Dataset

| Field | Details |
|-------|---------|
| **Source** | Ethiopian Insurance Corporation |
| **Published** | 19 July 2023 |
| **Version** | 1 |
| **DOI** | [10.17632/34nfrk36dt.1](https://doi.org/10.17632/34nfrk36dt.1) |
| **Contributor** | Edossa Terefe (Hawassa University) |
| **License** | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| **Category** | Applied Statistics / Machine Learning |
| **Period** | 2014 – 2018 |

📥 **[Download the Dataset on Mendeley Data](https://data.mendeley.com/datasets/34nfrk36dt/1)**

---

## 📁 Repository Structure

```
eic-insurance-analytics/
│
├── 📊 report-template-with-data.pbix   # Power BI dashboard (main file)
├── 📄 README.md                         # This file
├── 📂 data/
│   └── (download from Mendeley link above and place here)
├── 📂 screenshots/
│   ├── dashboard-main.png               # Main report page
│   └── dashboard-intro.png              # The Sad Tale of EIC intro page
└── 📂 docs/
    └── EIC_Insurance_Analytics_Report.docx  # 15-page analytical report
```

---

## 🔑 Key Variables

| Column | Description |
|--------|-------------|
| `SEX` | Policyholder gender (0, 1, 2) |
| `TYPE_VEHICLE` | Vehicle category (Motor-cycle, Truck, Automobile, Bus, etc.) |
| `MAKE` | Vehicle manufacturer / brand (TOYOTA, ISUZU, NL, BIS, etc.) |
| `USAGE` | How the vehicle is used (Private, Taxi, Commercial, Ambulance, etc.) |
| `CLAIM_PAID` | Total claim amount paid out per policy |
| `Year` | Policy year (2014–2018) via calendar table |

---

## 📈 Dashboard Pages

### Page 1 — `The Sad Tale of EIC` (Intro)
- **Treemap**: Portfolio volume by vehicle type — Motor-cycle and Trucks dominate
- **Gauge**: Total claims (₹9bn) vs open policies (508K) — visual proof of the loss scale
- Narrative context on EIC's history and collapse

### Page 2 — `Report` (Main Analytics)
- **KPI Cards**: Open policies · Total premium · Total claims · P:C ratio · Avg premium · Avg claims · Claim count
- **Bar Chart** (`Who are buying our policies?`): Policy count by vehicle type across years
- **Ribbon Chart** (`Total claims by year and usage`): 2014–2018 claims trend split by USAGE category
- **Scatter Chart** (`Premium vs Claim`): Each vehicle MAKE plotted on average premium vs average claims axes
- **Donut Chart** (`Open policies by SEX`): Gender split — Female 49.43% · Male 42.24% · Unknown 8.33%
- **Pivot Table**: Premium-to-claims ratio by USAGE × Year — the core profitability matrix
- **Slicer**: Year filter (2014, 2015, 2016, 2017, 2018)

---

## 🔍 Key Findings

### 1. Catastrophic Loss Ratio
The overall premium-to-claims ratio of **39%** means total claims (₹3bn) were nearly **3× total premiums** (₹1bn), with the broader portfolio reaching ₹9bn in total claims against 508K policies.

### 2. High-Risk Usage Categories (2016 snapshot)
| Usage | P:C Ratio |
|-------|-----------|
| Others | 1259% |
| Agricultural Own Farm | 219% |
| Special Construction | 170% |
| **Taxi** | **133%** |
| Agricultural Any Farm | 101% |
| Car Hires | 84% |
| Private | 66% |
| Ambulance | 56% |
| **Fare Paying Passengers** | **38%** |
| **Total** | **39%** |

> Taxi and Fare Paying Passengers — the highest-volume commercial segments — were significantly under-priced relative to actual claims.

### 3. Volume vs Risk Mismatch
Motor-cycles had the **highest policy count** (27.7K) but trucks and automobiles generated disproportionately large claim values, as seen in the treemap.

### 4. Gender Distribution is Nearly Equal
Female (SEX=1): 49.43% of policies | Male (SEX=0): 42.24% | Unknown: 8.33%

---

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop** — dashboard development
- **DAX** — calculated measures (P:C ratio, averages, counts)
- **Power Query** — data transformation
- **Python / R** *(optional)* — for extended ML analysis using the raw dataset

---

## 🚀 Getting Started

### Prerequisites
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)

### Steps

```bash
# 1. Clone this repository
git clone https://github.com/YOUR_USERNAME/eic-insurance-analytics.git
cd eic-insurance-analytics

# 2. Download the dataset from Mendeley
# https://data.mendeley.com/datasets/34nfrk36dt/1
# Place the downloaded file(s) in the /data folder

# 3. Open the Power BI file
# Double-click report-template-with-data.pbix
# Or open Power BI Desktop → File → Open → select the .pbix file

# 4. Refresh data if prompted
# Home → Refresh
```

---

## 📚 Citation

If you use this dataset or analysis in your work, please cite:

```bibtex
@dataset{terefe_2023_eic,
  author    = {Edossa Terefe},
  title     = {Vehicle Insurance data},
  year      = {2023},
  publisher = {Mendeley Data},
  version   = {1},
  doi       = {10.17632/34nfrk36dt.1},
  url       = {https://data.mendeley.com/datasets/34nfrk36dt/1}
}
```

---

## 📄 License

- **Dataset**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
- **Code & Dashboard**: [MIT License](LICENSE)

You are free to share and adapt the material for any purpose, provided appropriate credit is given.

---

## 🤝 Contributing

Contributions are welcome! If you'd like to:
- Add machine learning models on the raw dataset
- Extend the Power BI report with additional visuals
- Translate findings into another language

Please open an issue or submit a pull request.

---

## ⭐ Acknowledgements

- **Edossa Terefe** (Hawassa University) for publishing the dataset
- **Ethiopian Insurance Corporation** — the source of the underlying records




<img width="732" height="495" alt="image" src="https://github.com/user-attachments/assets/dd49630e-1717-41de-a9ec-80c3a3de487d" />

- **Mendeley Data** for hosting the dataset under open access terms

---

*"EIC's story is a textbook case of premium inadequacy — pricing risk at a fraction of its actual cost across a portfolio of 500K+ policies over five years."*
