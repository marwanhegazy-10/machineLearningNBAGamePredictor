# RimPredictor: Machine Learning NBA Game Predictor

This repository provides tools for scraping, processing, and analyzing NBA game data from [Basketball Reference](https://www.basketball-reference.com). It includes functionalities to scrape game schedules, box scores, and player statistics, as well as a machine learning pipeline for predicting game outcomes.

## Features

- **Web Scraping**: Uses [Playwright](https://playwright.dev/) and [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) to scrape game schedules, standings, and box scores.
- **Data Processing**: Cleans and organizes scraped data into structured formats, leveraging [Pandas](https://pandas.pydata.org/) for data manipulation.
- **Machine Learning**: Implements a feature selection and prediction pipeline using [scikit-learn](https://scikit-learn.org/).
- **Rolling Averages**: Calculates rolling averages for teams to capture recent performance trends.
- **Backtesting**: Validates prediction models using historical data.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/marwanhegazy-10/rimPredictor.git
   cd rimPredictor
   ```

2. Install Playwright browsers:
   ```bash
   playwright install
   ```

## Usage

### 1. Scraping Data
Run the scraping functions to download NBA schedules, standings, and box scores.

#### Example:
```python
from scraper import scrape_season

# Scrape data for a specific season
await scrape_season(2022)
```

### 2. Data Cleaning and Processing
Process the scraped HTML files into a structured DataFrame.

#### Example:
```python
from data_processor import process_box_scores

# Process all box scores
df = process_box_scores()
```

### 3. Rolling Averages
Calculate rolling averages for teams to include recent performance trends.

#### Example:
```python
from rolling_averages import calculate_rolling_averages

# Calculate rolling averages
df_rolling = calculate_rolling_averages(df)
```

### 4. Predicting Game Outcomes
Use the machine learning pipeline to predict game outcomes based on historical data.

#### Example:
```python
from predictor import backtest

# Train and test the model
predictions = backtest(df, model, predictors)
```

## Key Results

- **Prediction Accuracy**: Achieved a prediction accuracy of ~63% using ridge regression and selected features.
- **Home Advantage Insights**: Found that home teams win about 57% of games.

## Data Workflow

1. Scrape NBA schedules and game data.
2. Process and clean the scraped data.
3. Transform the data into rolling averages and features.
4. Train a machine learning model to predict game outcomes.

## Requirements

- Python 3.8+
- Pandas
- BeautifulSoup
- Playwright
- scikit-learn

## Directory Structure

```
.
├── data/                   # Raw and processed data
│   ├── standings/          # Scraped standings data
│   ├── scores/             # Scraped box score data
├── notebooks/              # Jupyter notebooks for analysis
├── scraper.py              # Scripts for web scraping
├── data_processor.py       # Scripts for data cleaning and processing
├── rolling_averages.py     # Rolling average calculations
├── predictor.py            # Machine learning pipeline
└── README.md               # Project documentation
```

## Acknowledgments

- Data sourced from [Basketball Reference](https://www.basketball-reference.com).
- Machine learning powered by [scikit-learn](https://scikit-learn.org/).
- This project was developed with guidance and resources from Dataquest.
