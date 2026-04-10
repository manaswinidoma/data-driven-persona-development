# Data-Driven Persona Development Using K-Means Clustering
**World Values Survey (WVS) Wave 7 — Australia & New Zealand**
*University of Technology Sydney | Industry Project*

---

## Overview
Built a Python ML pipeline to segment 2,870 survey respondents into 
empirically-grounded personas using K-Means clustering on World Values 
Survey data — moving beyond traditional assumption-based persona methods.

---

## Problem Statement
Traditional personas rely on designer assumptions and small focus groups, 
making them unverifiable and unreliable. This project replaces guesswork 
with a transparent, reproducible, data-driven approach.

---

## Dataset
- **Source:** World Values Survey (WVS) Wave 7 (2017–2022)
- **Countries:** Australia (n=1,477) & New Zealand (n=1,393)
- **Size:** 2,870 respondents × 572 variables
- **Themes:** Social values, trust, religion, politics, economics & more

---

## Methodology
1. **Feature Selection** — Reduced 572 → 290 variables using metadata 
   (removed technical, country-level, and composite variables)
2. **Missing Data Handling** — KNN Imputation (k=5); pre-imputation 
   transparency report generated
3. **Type-Aware Encoding** — Binary (0/1), Ordinal (ranked), 
   Nominal (label), Continuous (original)
4. **Standardisation** — StandardScaler (z-score normalisation)
5. **Clustering** — K-Means evaluated k=3 to k=7 using 4 metrics
6. **Validation** — Silhouette, Davies-Bouldin, Calinski-Harabasz, Elbow
7. **Profiling** — 4 personas across 10 WVS thematic domains

---

## Key Results
| Persona | Size | % | Profile |
|---------|------|---|---------|
| Persona 1 | 986 | 34.4% | Family-oriented, environmentally conscious, institution-skeptic |
| Persona 2 | 96  | 3.3%  | High trust, socially engaged, interpersonally connected |
| Persona 3 | 973 | 33.9% | Disengaged, low importance across life domains, anti-nationalist |
| Persona 4 | 815 | 28.4% | Traditionalist, religious, nationalist, corruption-aware |

- **Cluster Stability:** 97.8% across 100 random initialisations
- **Silhouette Score:** 0.138 (k=4)
- **Davies-Bouldin Index:** 1.02

---

## Tech Stack
- Python, scikit-learn, pandas, numpy, matplotlib
- Google Colab
- KNNImputer, KMeans, PCA, StandardScaler

---

## Output Files
| File | Description |
|------|-------------|
| `persona_assignments.csv` | All 2,870 respondents mapped to personas |
| `persona_summary.csv` | Persona names, sizes, percentages |
| `persona_profiles.json` | Detailed thematic profiles (10 domains) |
| `missing_data_report.csv` | Pre-imputation data quality report |
| `optimal_clusters.png` | Clustering metrics across k=3 to k=7 |
| `personas_visualization.png` | PCA scatter + audience distribution |

---

## How to Run
```bash
# 1. Clone the repo
git clone https://github.com/yourusername/wvs-persona-development.git

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your data files (see note below)
# Place WVS_Australia_NZ.xlsx and WVS_Metadata_Augmented.xlsx 
# in the root directory

# 4. Run the notebook
# Open Final_Analysis.ipynb in Google Colab or Jupyter
```

> **Note on Data:** WVS data is publicly available at 
> [worldvaluessurvey.org](https://www.worldvaluessurvey.org). 
> Download Wave 7 dataset and request access directly from WVS.

---

## Author
**Manaswini Doma**
Master of Information Technology | 
University of Technology Sydney
[LinkedIn](https://www.linkedin.com/in/domamanaswini/) | [GitHub](https://github.com/manaswinidoma/)
