# Olympic Medal Prediction Project — Group A

## Overview

This repository contains our data science project exploring which country-level features best predict Olympic medal success. We use a combination of historical Olympic data, GDP, population, and hosting/regime features to model medal counts with regression and machine learning approaches.

## Group Members

- Maxim Lisiansky (206529018)
- Noam Ben Moshe (318962693)
- Roy Kremer (207577099)
- Romi Richter (212876551)
- Avraham Elbaz (209885359)

## Folder Contents

- `Workshop_Olympics.ipynb` — Main Jupyter notebook containing the full analysis, including data loading, cleaning, feature engineering, exploratory analysis, modeling, and results.
- `report.tex` / `report.pdf` — Final project report in LaTeX (and PDF) summarizing motivation, data, methodology, results, and conclusions.
- `athlete_events.csv` — Athlete- and event-level Olympic data (Kaggle).
- `CountriesGDP1960-2020.csv` — Country GDP data from the World Bank.
- `API_SP.POP.TOTL_DS2_en_csv_v2_131993.csv` — Country population data from the World Bank.
- `olympic_hosts.csv` — List of host countries and cities for each Olympic Games.
- `EX1_Group_A.pdf` — Assignment 1, literature review and data exploration.
- `EX2_Group_A.pdf` — Assignment 2, discussion of project contribution and novelty.
- Any additional scripts, figures, or processed files generated during analysis.

## How to Use

1. **Data Preparation:**
    - Make sure all the `.csv` data files are present in the same folder as `Workshop_Olympics.ipynb`.
2. **Analysis:**
    - Open `Workshop_Olympics.ipynb` in Jupyter Notebook or Google Colab.
    - Run all cells in order to perform data cleaning, exploration, modeling, and evaluation.
3. **Report:**
    - Compile `report.tex` using any standard LaTeX editor to generate the PDF report.

## Data Sources

- [120 Years of Olympic History: Athletes and Results (Kaggle)](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results)
- [World Bank: GDP and Population Data](https://databank.worldbank.org/source/world-development-indicators)
- [Olympic Hosts and Event Metadata] (custom-compiled, see notebook)
- Regime information constructed manually using Wikipedia and historical records

## Main Results

- **GDP, population, and participation** (number of Games attended) are the most reliable predictors of Olympic medal counts.
- **Hosting** the Olympics and **regime type** were not significant predictors after controlling for economic/demographic variables.
- **Random Forest** performed best for the Summer Games; **XGBoost** had the best (but less stable) performance for the Winter Games.

## References

- See `report.tex`, `EX1_Group_A.pdf`, and `EX2_Group_A.pdf` for a detailed bibliography and related work summary.

## Acknowledgments

Thanks to the data providers and prior researchers whose work is referenced throughout this project.

---

