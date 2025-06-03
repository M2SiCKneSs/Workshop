# Predicting Olympic Medal Success: A Data-Driven Country-Level Analysis

## Overview

This repository contains all files related to our group project exploring what drives Olympic medal success at the country level. We analyze a range of economic, demographic, and event features using data science and machine learning.

## Group Members

- Maxim Lisiansky (206529018)
- Noam Ben Moshe (318962693)
- Roy Kremer (207577099)
- Romi Richter (212876551)
- Avraham Elbaz (209885359)

## Folder Contents

- **Final Report.pdf** — The complete written report describing our methodology, data, results, discussion, and conclusions.
- **Workshop.pptx** — The final presentation summarizing the project motivation, data, modeling, results, and conclusions.
- **Workshop_Olympics.ipynb** — The main Jupyter notebook with all code for data loading, cleaning, analysis, modeling, and result generation.
- **athlete_events.csv** — Athlete- and event-level Olympic data (Kaggle).
- **CountriesGDP1960-2020.csv** — Country GDP data from the World Bank.
- **API_SP.POP.TOTL_DS2_en_csv_v2_131993.csv** — Country population data from the World Bank.
- **olympic_hosts.csv** — List of Olympic host countries and cities for each Games.
- **EX1_Group_A.pdf** (optional) — Literature review and initial data exploration.
- **EX2_Group_A.pdf** (optional) — Detailed project contribution and novelty.

## How to Use

1. **Explore the Code and Data:**
    - Open `Workshop_Olympics.ipynb` in Jupyter Notebook or Google Colab.
    - Ensure all `.csv` data files are in the same directory as the notebook.
    - Run the notebook cells for data preprocessing, feature engineering, modeling, and visualization.

2. **Read the Report and Presentation:**
    - Open `Final Report.pdf` for the full description of the project, including related work, data, methodology, results, and future directions.
    - View `Workshop.pptx` for a concise, visual summary suitable for presentation.

## Data Sources

- [120 Years of Olympic History: Athletes and Results (Kaggle)](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results)
- [World Bank: GDP and Population Data](https://databank.worldbank.org/source/world-development-indicators)
- Olympic host information (custom-compiled, see notebook)
- Regime/communist country data constructed using Wikipedia and historical sources.

## Main Findings

- **GDP, population, and participation (number of Games attended)** are the most important predictors of Olympic medal counts at the country level.
- **Hosting** the Olympics and **political regime** status were not significant predictors after controlling for other features.
- **Random Forest** performed best for the Summer Olympics; **XGBoost** had the best performance for Winter Olympics (less stable).
- Country-level models work better for Summer than for Winter Games, and more granular features may improve predictions.

## Reproducibility

- All code is provided in the notebook, with fixed random seeds and documented preprocessing steps.
- Results can be fully reproduced by running the notebook with the supplied data files.

## References

- See `Final Report.pdf` and `EX1_Group_A.pdf`/`EX2_Group_A.pdf` for complete literature references and related work.

## Contact

For any questions about the project, please contact any of the group members listed above.

---

