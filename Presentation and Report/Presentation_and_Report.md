## Title
Predicting Olympic Medal Success: A Data Driven Country Level Analysis

## Abstract

In this project, we tried to figure out what makes some countries do better than others in the Olympics. We used data from the 1960, including things like GDP, population size, whether a country hosted the Olympics, and a country's regime status. We combined data from different sources, cleaned it up, and turned it into a format we could use to build prediction models.
After preparing the data we used four different models to predict how many medals each country might win: Poisson Regression, Linear Regression, Random Forest, and XGBoost. We looked at both country level averages and specific years to see what patterns we could find.
We found that GDP and population were the strongest predictors for winning medals in the Summer Olympics. The more a country participated, the better it did too. Hosting the Olympics and political regime type didn’t really seem to matter once we included the economic data. Winter Olympics were harder to predict, but participation still made a difference there.
Overall, our best performing models were Random Forest for the Summer Games and XGBoost for the Winter Games (on country level data). Our project shows that data science can be a useful way to understand what drives success in international sports competitions, especially when we have access to long term, country level data.

## Related Work
Here are the main papers we looked at that helped us understand what affects Olympic success:

- **Bernard & Busse (2004):**
  - Found that both GDP and population are strong predictors of Olympic medal counts.
  - Hosting the Olympics and being part of the former Soviet bloc also gave countries a boost.
  - This paper helped us choose our main features (GDP, population, host, regime).

- **Rewilak (2021):**
  - Showed that GDP per capita isn't always a good predictor once you control for country specific traits.
  - Population and hosting were more consistent factors.
  - This made us consider that GDP might not be as important as we first thought.

- **Hoffmann, Ramasamy & Ging (2002):**
  - Focused on ASEAN countries and why they didn’t do well in the 2000 Olympics.
  - Found that low GNP and small populations were the main reasons.
  - Also said that getting richer isn’t enough, you need real support for sports.
  - Made us think about missing variables that might not be in our dataset.

- **Xun Bian:**
  - Used linear and Cobb Douglas models with Olympic data from 1988 to 2000.
  - Found that GDP, population, host advantage, and socialist background all matter.
  - Talked about diminishing returns—more money/population doesn’t always mean more medals.

- **Winfree & Fort (Team Payroll vs. Performance):**
  - Looked at North American sports leagues like the NBA and NFL.
  - Found that teams with higher payrolls usually perform better, especially where salary caps are looser.
  - Not directly about the Olympics, but showed how money can lead to success in sports generally.
 ## Data

We used several datasets in this project, which we combined and cleaned to build our final dataset for modeling:

- **Sources:**
  - Athlete-level Olympic data from [Kaggle’s athlete_events dataset].
  - GDP and population data from the World Bank (API_SP.POP.TOTL and CountriesGDP 1960–2020).
  - Hosting info and event metadata from olympic_hosts.csv.
  - Regime data (communist countries) was created manually using Wikipedia.

- **Size and Structure:**
  - Athlete data: ~69,000 rows, 15 columns (one row per athlete-event-year).
  - GDP and population: Country-level data from 1960–2020.
  - Final dataset: Aggregated to country-year level with features like population, GDP, medals, regime, and hosting status.

- **Preprocessing Steps:**
  - Cleaned and standardized country names (e.g., "USA" vs "United States").
  - Dropped rows where GDP or population were missing.
  - Aggregated medal counts per country and year.
  - Created binary variables:  
    - `host` = 1 if country hosted that year  
    - `regime` = 1 if communist that year  
  - Log-transformed GDP and population to reduce skew.
  - Standardized (z-score) numerical variables.
  - Filtered to only include countries with complete data across required features.

- **Challenges:**
  - A lot of inconsistencies in country names (especially over time).
  - Missing values for GDP/population caused some countries or years to be dropped.
  - Defining the “regime” variable was tricky and required external manual sources.
  - Winter Olympic data was harder to model due to smaller and more uneven participation.

Overall, we ended up with a clean dataset that we used to build regression models and analyze which features best predict Olympic medal success.
