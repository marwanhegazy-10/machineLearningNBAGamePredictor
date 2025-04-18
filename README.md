# RimPredictor: Machine Learning NBA Game Predictor

**RimPredictor** is a comprehensive NBA game prediction tool that leverages machine learning. This repository provides tools for scraping, processing, and analyzing NBA game data from [Basketball Reference](https://www.basketball-reference.com). It includes functionalities to scrape game schedules, box scores, and player statistics, as well as a machine learning pipeline for predicting game outcomes.

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
# Use the `get_data.ipynb` notebook to scrape data
```

### 2. Data Cleaning and Processing
Process the scraped HTML files into a structured DataFrame.

#### Example:
```python
# Use the `parse_data.ipynb` notebook to clean and process data
```

### 3. Predicting Game Outcomes
Use the machine learning pipeline to predict game outcomes based on historical data.

#### Example:
```python
# Use the `predict.ipynb` notebook to train and test the model
```

## Key Results

- **Prediction Accuracy**: Achieved a prediction accuracy of ~63% using ridge regression and selected features.
- **Home Advantage Insights**: Found that home teams win about 57% of games.

## Directory Structure

```
.
├── README.md               # Project documentation
├── get_data.ipynb          # Notebook for scraping NBA data
├── parse_data.ipynb        # Notebook for cleaning and processing data
├── predict.ipynb           # Notebook for training and predicting game outcomes
```

## Requirements

- Python 3.8+
- Pandas
- BeautifulSoup
- Playwright
- scikit-learn

## Acknowledgments

- Data sourced from [Basketball Reference](https://www.basketball-reference.com).
- Machine learning powered by [scikit-learn](https://scikit-learn.org/).
- This project was developed with guidance and resources from Dataquest.
