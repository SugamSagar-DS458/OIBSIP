# Unemployment Analysis in India 📊

## Overview

Exploratory data analysis of unemployment trends in India, built as part of the Oasis Internship Data Science track (Task 2). The notebook cleans the raw dataset, then explores regional, monthly, and time-series unemployment patterns — including a direct comparison of key labor indicators before and after the COVID-19 pandemic.

The `Task2.ipynb` notebook walks through a complete mini-EDA workflow:

1. **Data loading & cleaning** — load the CSV, inspect shape/dtypes, strip stray whitespace from column names, drop rows with missing values, and parse the `Date` column into proper datetime format.
2. **Exploratory analysis** — visualize how unemployment varies by region, by month, and over time for the most affected regions.
3. **Correlation analysis** — examine the relationship between unemployment rate, employment, and labour participation rate.
4. **Pre-COVID vs. post-COVID comparison** — split the data at March 31, 2020 and compare mean values of key indicators across the two periods.

## Dataset

The notebook expects a CSV named `Unemployment in India.csv` with (at least) the following columns:

| Column | Description |
|---|---|
| `Region` | Indian state/region |
| `Date` | Date of the observation |
| `Estimated Unemployment Rate (%)` | Unemployment rate for that region/date |
| `Estimated Employed` | Number of people employed |
| `Estimated Labour Participation Rate (%)` | Labour participation rate |

---

## Key Analyses & Visualizations

- **Region-wise average unemployment rate** — bar chart ranking all regions.
- **Month-wise unemployment trend** — line chart of average unemployment rate across the year.
- **Time-series for top 3 regions** — unemployment rate over time for the three regions with the highest averages.
- **Top 10 states by unemployment** — bar chart highlighting the most affected states.
- **Correlation heatmap** — relationship between unemployment rate, employment, and labour participation rate.
- **Pre-COVID vs. post-COVID comparison** — mean values of key indicators split at the March 2020 cutoff, showing the pandemic's impact on the labor market.

## Screenshots

### Average unemploymenmt rate by region
[Average unemploymenmt rate by region](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screenshot%202026-08-27%20164711.png)

### Average unemploymenmt rate by month
[Average unemploymenmt rate by month](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screenshot%202026-08-27%20164728.png)

### Unemploymenmt rate for top 3 region
[Unemploymenmt rate for top 3 region](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screenshot%202026-08-27%20164741.png)

### Highest average unemploymenmt rate of top 10 region
[Highest average unemploymenmt rate of top 10 region](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screenshot%202026-08-27%20164755.png)

### Correlation Heatmap of Key Economic Indicators
[Correlation Heatmap of Key Economic Indicators](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screenshot%202026-08-27%20164809.png)

## Demo

[Short video of walkthrough my project](https://github.com/SugamSagar-DS458/OIBSIP/blob/main/DataScience-Task2-UnemploymentInIndia/Screen%20Recording%202026-08-27%20115710.mp4)

## Requirements

- Python 3.8+
- pandas
- matplotlib
- seaborn
- jupyter

Install dependencies:

```bash
pip install pandas matplotlib seaborn jupyter
```

## Usage

1. Clone this repository.
2. Place `Unemployment in India.csv` in a location of your choice and update the file path in the first cell of `Task2.ipynb`.
3. Launch Jupyter and run all cells:

```bash
jupyter notebook Task2.ipynb
```

## Repository Structure

```
.
├── Task2.ipynb    # Main analysis notebook
├── README.md      # Project documentation
 # Screenshots, and demo video used in this README
```

## Findings

- Unemployment rates vary significantly by region, with certain states consistently reporting much higher averages than others.
- Seasonal patterns are visible in the month-wise trend.
- Employment and labour participation rate show a meaningful relationship with the unemployment rate, as seen in the correlation heatmap.
- The post-COVID period shows a marked shift in unemployment, employment, and labour participation compared to the pre-COVID period, reflecting the pandemic's disruption of the Indian labor market.

## Acknowledgements

Task completed as part of the **Oasis Infobyte Data Science Internship**.
