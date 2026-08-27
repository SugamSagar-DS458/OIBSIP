# Unemployment Analysis in India 📊

Exploratory data analysis of unemployment trends in India, built as part of the Oasis Internship Data Science track (Task 2). The notebook cleans the raw dataset, then explores regional, monthly, and time-series unemployment patterns — including a direct comparison of key labor indicators before and after the COVID-19 pandemic.

## Overview

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

> The dataset is a commonly used public dataset from Kaggle's "Unemployment in India" collection.

## Key Analyses & Visualizations

- **Region-wise average unemployment rate** — bar chart ranking all regions.
- **Month-wise unemployment trend** — line chart of average unemployment rate across the year.
- **Time-series for top 3 regions** — unemployment rate over time for the three regions with the highest averages.
- **Top 10 states by unemployment** — bar chart highlighting the most affected states.
- **Correlation heatmap** — relationship between unemployment rate, employment, and labour participation rate.
- **Pre-COVID vs. post-COVID comparison** — mean values of key indicators split at the March 2020 cutoff, showing the pandemic's impact on the labor market.

## Screenshots

<p align="center">
  <img src="assets/screenshot-1.png" alt="Region-wise unemployment rate bar chart" width="700"/>
</p>

<p align="center">
  <img src="assets/screenshot-2.png" alt="Correlation heatmap" width="700"/>
</p>

> Add your screenshot images to an `assets/` folder in the repo root and update the file names/paths above to match.

## Demo

<p align="center">
  <img src="assets/demo.gif" alt="Notebook walkthrough demo" width="700"/>
</p>

GitHub does not natively play `.mp4` files inline in a README, so for video demos either:

- Convert the clip to a `.gif` (e.g. using [ezgif.com](https://ezgif.com) or `ffmpeg`) and embed it like the image above, **or**
- Upload the `.mp4` directly by dragging it into a GitHub issue/PR comment or the repo's file editor — GitHub will host it and give you a link you can paste here, **or**
- Host the video externally (YouTube, Loom, etc.) and link a thumbnail:

```markdown
[![Watch the demo](assets/video-thumbnail.png)](https://your-video-link-here.com)
```

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
└── assets/        # Screenshots, GIFs, and demo media used in this README
```

## Findings

- Unemployment rates vary significantly by region, with certain states consistently reporting much higher averages than others.
- Seasonal patterns are visible in the month-wise trend.
- Employment and labour participation rate show a meaningful relationship with the unemployment rate, as seen in the correlation heatmap.
- The post-COVID period shows a marked shift in unemployment, employment, and labour participation compared to the pre-COVID period, reflecting the pandemic's disruption of the Indian labor market.

## Acknowledgements

Task completed as part of the **Oasis Infobyte Data Science Internship**.
