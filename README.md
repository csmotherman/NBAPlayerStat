# NBA Player Stat Prediction

This project involves building a predictive model for NBA player statistics using historical game logs and real-time data. The model leverages APIs, web scraping, and various data processing techniques to analyze player performance and provide daily projections for points, rebounds, and assists. 

## Table of Contents
- [Project Overview](#project-overview)
- [Data Collection](#data-collection)
- [Data Cleaning and Processing](#data-cleaning-and-processing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Installation](#installation)
- [Usage](#usage)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
The goal of this project is to predict NBA player performance in upcoming games by using a combination of historical game logs, player stats, and defensive metrics. This tool is useful for daily fantasy sports analysis, sports betting, and general NBA analytics.

## Data Collection
- Uses [`nba_api`](https://github.com/swar/nba_api) to retrieve player game logs and team opponent stats.
- Scrapes data from [hashtagbasketball.com](https://hashtagbasketball.com/nba-defense-vs-position) to collect defense versus position metrics.
- Imports player minute projections from an external source using web scraping with BeautifulSoup.

## Data Cleaning and Processing
- Cleans defense vs. position stats by removing ranks and converting columns to appropriate data types.
- Converts team names to standard abbreviations for consistency.
- Processes player game logs to extract relevant data and handle missing or unusual entries.
  
## Feature Engineering
- Converts player stats to a per-minute basis for more accurate performance comparisons.
- Combines various data sources, such as recent team performance and individual player minutes, to enhance predictive power.

## Modeling
- Applies predictive models (e.g., Linear Regression, Logistic Regression, etc.) to forecast player stats like points, rebounds, and assists.
- Utilizes Python libraries such as Pandas, NumPy, and Scikit-learn for data analysis and modeling.
## Usage
1. **Data Collection:** Run the script to collect and clean data using the NBA API and web scraping.
2. **Data Analysis:** Use the pre-defined functions to process and analyze player performance.
3. **Modeling:** Apply predictive models to generate forecasts for player stats in upcoming games.
4. **Results:** Review the results and predictions, which are outputted as a DataFrame.

> **Note:** Ensure you have an active internet connection to fetch data via the NBA API and web scraping.

## Future Improvements
- **Error Handling:** Implement robust error checking for API requests and data processing steps.
- **Modularity:** Refactor code into separate functions and modules for better maintainability.
- **Visualization:** Add visualizations (e.g., player performance charts) to enhance data analysis.
- **User Interface:** Develop a simple front-end interface to allow users to input custom player or team data for predictions.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/csmotherman/NBAPlayerStat.git
