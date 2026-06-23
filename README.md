# Exploring Global Health and Development Trends, 1900–2019

This project explores long-term patterns in income per person, fertility rate and life expectancy across countries from 1900 to 2019.

The aim is to understand how these three indicators changed over time, and how they relate to each other at the country level. This is an exploratory data analysis project, so the findings are descriptive rather than causal.


## Dataset

The project uses `life_expectancy_and_income.csv`, a country-year dataset with 22,080 records across 184 countries from 1900 to 2019.

The dataset contains five columns:

1. `country`: country name

2. `year`: year of observation

3. `fertility_rate`: average number of children per woman

4. `income_per_person`: income per person

5. `life_expectancy`: average life expectancy

The averages used in this project are unweighted country-level averages. This means each country is given equal weight, regardless of population size.


## Questions

This project focuses on five questions:

1. How did average country-level life expectancy, fertility rate and income per person change from 1900 to 2019?

2. Are higher-income countries generally associated with higher life expectancy?

3. Are higher-income countries generally associated with lower fertility rates?

4. How are fertility rate and life expectancy related?

5. Which countries recorded the largest life expectancy gains between 1900 and 2019?


## Tools

Python with pandas, NumPy and matplotlib in Jupyter Notebook.


## Analysis

The notebook starts with basic data inspection, including the shape of the dataset, column names, data types and summary statistics.

It then checks for missing values, duplicate country-year records, year coverage and the number of records per country. I also reviewed unusually low life expectancy values, since some early historical records contain extreme values.

For the main analysis, I first looked at long-term trends in average country-level life expectancy, fertility rate and income per person. I then used scatter plots and correlations to explore the relationships between income, life expectancy and fertility rate in 2019.

Because income per person is highly skewed, I used a log-transformed income variable for the relationship analysis.

The final part of the notebook compares country-level changes between 1900 and 2019, focusing especially on recorded life expectancy gains.


## Key Findings

1. Average country-level life expectancy increased from around 33.6 years in 1900 to around 73.2 years in 2019.

2. Average country-level fertility rate declined from around 5.9 in 1900 to around 2.7 in 2019.

3. Income per person increased over time, but the values were highly skewed. For this reason, log income was used in the relationship analysis.

4. In 2019, log income and life expectancy had a strong positive correlation of approximately 0.84.

5. In 2019, log income and fertility rate had a strong negative correlation of approximately -0.78.

6. Fertility rate and life expectancy also had a strong negative correlation in 2019, at approximately -0.78.

7. Some countries recorded life expectancy gains of more than 50 years between 1900 and 2019.


## Limitations

1. This project is exploratory and does not establish causal relationships.

2. The averages are unweighted country-level averages and do not account for population size.

3. Income per person does not capture inequality within countries.

4. The dataset does not include other relevant factors such as healthcare access, education, conflict, governance, child mortality or urbanisation.

5. Historical data, especially from the early 20th century, may include estimates and should be interpreted carefully.

6. Country-level averages can hide large differences within countries.


## Running the Notebook

The analysis is in `notebooks/global_health_development_analysis.ipynb`, using the CSV file in `data/life_expectancy_and_income.csv`.

To run it locally, install the packages in `requirements.txt` and open the notebook in Jupyter.

