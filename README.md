# Olympics Data EDA (R)

An exploratory data analysis of the Summer Olympics (1984–2020) in R: scraping historical results and country GDP data, cleaning and merging it, and exploring medal trends, age distributions, and economic correlates through an interactive Shiny dashboard.

## What it does

- **Scraping** (`src/data_scraping_and_preprocessing.R`, `src/tokyo_olympic.R`) — pulls per-Games results tables from [Olympedia](http://www.olympedia.org) for each Summer Olympics from Los Angeles 1984 through Tokyo 2020, and country-level GDP data (`src/gdp_scrapping.R`) to analyze alongside medal counts.
- **Analysis & plots** (`src/plots.R`) — medal distribution, athlete age distribution, and GDP-vs-performance exploration across editions.
- **Interactive dashboard** (`src/Olympic_Shiny_app.R`) — a Shiny app for exploring medal and age distributions per Games, filterable by event.

## Data

Scraped tables are cached as `.Rdata` files under `data/Olympics_scraped_data/` (one per Games year) and `data/Rshiny_data/` (pre-joined data for the Shiny app), so the dashboard runs without re-scraping.

## Getting started

```r
# From the repo root, in R/RStudio:
install.packages(c("shiny", "ggplot2", "GGally", "patchwork", "dplyr", "plotly", "shinythemes"))
shiny::runApp("src/Olympic_Shiny_app.R")
```

## Report

`Project_Report.pdf` and `Group_5_PPT.pptx` contain the full writeup and presentation of findings.

## Status

Academic group project (R / EDA coursework). Shared here as-is for reference.
