# Predicting Olympic Medal Success: A Data-Driven Country-Level Analysis

## Overview

This project explores what makes some countries more successful than others in the Olympic Games, focusing on the impact of economic and demographic factors like GDP, population size, and hosting status. Using data from 1960 onward, we built a cleaned and merged country-level dataset and applied regression and machine learning models (Poisson, Linear, Random Forest, XGBoost) to predict Olympic medal counts. Our work compares different modeling approaches and studies from the literature to highlight which features matter most.

## Group Members

- Maxim Lisiansky (206529018)
- Noam Ben Moshe (318962693)
- Roy Kremer (207577099)
- Romi Richter (212876551)
- Avraham Elbaz (209885359)

## Project Files

- `Workshop_Olympics.ipynb` — Main Jupyter notebook containing all code, data cleaning, exploration, modeling, and results.
- `report.tex` / `report.pdf` — Final report written in LaTeX (and exported PDF) summarizing the project, results, and discussion.
- `EX1_Group_A.pdf` — Assignment 1, initial project statement, datasets, and literature review.
- `EX2_Group_A.pdf` — Assignment 2, project contributions, novelty, and detailed discussion of related work.
- `data/` — Folder containing all raw and processed datasets (e.g., `athlete_events.csv`, `CountriesGDP1960-2020.csv`, `API_SP.POP.TOTL_DS2_en_csv_v2_131993.csv`, `olympic_hosts.csv`).
- Additional scripts, outputs, or figures as generated in the notebook.

## Data Sources

- [120 Years of Olympic History: Athletes and Results](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results)
- [World Bank GDP Data](https://databank.worldbank.org/source/world-development-indicators#)
- [World Bank Population Data](https://databank.worldbank.org/source/world-development-indicators#)
- Manual sources for regime data (Wikipedia) and Olympic hosts.

## How to Run

1. Open `Workshop_Olympics.ipynb` in Jupyter or Google Colab.
2. Place all relevant CSV data files in the same directory or in a `data/` subfolder.
3. Run the cells in order for data cleaning, analysis, and results reproduction.
4. The LaTeX report (`report.tex`) can be compiled using any standard LaTeX editor.

## Main Results

- **GDP, population, and participation (number of Games attended)** are the strongest predictors of medal counts.
- **Hosting** and **regime** status were not significant predictors after accounting for economic and demographic variables.
- **Random Forest** performed best for Summer Olympics; **XGBoost** gave best (though less stable) results for Winter Olympics.
- Results are consistent with and compared to the main findings of the literature.

## References

- Bernard & Busse (2004), "Who Wins the Olympic Games: Economic Resources and Medal Totals"
- Johan Rewilak (2021), "The (Non) Determinants of Olympic Success"
- Hoffmann, Ramasamy & Ging (2002), "Olympic Success and ASEAN Countries: Economic Analysis and Policy Implications"
- Xun Bian (2005), "Predicting Olympic Medal Counts: The Effects of Economic Development on Olympic Performance"
- Winfree & Fort, "Team Payroll Versus Performance in Professional Sports"
- See EX1_Group_A.pdf and EX2_Group_A.pdf for additional paper summaries and discussion.

## Acknowledgments

Thanks to the data providers and authors whose work informed our project. See references above for key studies.

