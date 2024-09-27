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

1. **Data Collection:** 
   - Utilizes the [`nba_api`](https://github.com/swar/nba_api) to fetch historical player game logs and team opponent stats.
   - Uses web scraping (BeautifulSoup) to collect defensive statistics by position from [hashtagbasketball.com](https://hashtagbasketball.com/nba-defense-vs-position).
   - Scrapes an external source to import player minute projections for the current day’s games.

2. **Data Cleaning and Preprocessing:** 
   - Cleans and processes the scraped data by removing unnecessary ranks and converting columns to the appropriate data types.
   - Converts team names into standardized abbreviations for consistency.
   - Extracts relevant player game logs using the `nba_api` and filters the data to focus on players with substantial playing time.
   - Converts player stats to a per-minute basis to standardize comparisons across players with different playtimes.

3. **Feature Engineering:** 
   - Creates new features, such as per-minute statistics, to enhance the predictive power of the model.
   - Merges various data sources, including recent team performance, individual player stats, and defensive metrics.

4. **Modeling:** 
   - Prepares the processed data for modeling, applying statistical methods (e.g., linear regression, logistic regression) to predict key player performance metrics like points, rebounds, and assists.
   - Automates data collection and processing to provide daily predictions for player performance.

5. **Output and Results:** 
   - Outputs the cleaned and processed data as DataFrames for further analysis and use in the predictive models.
   - Displays the predicted statistics for players, providing valuable insights for sports analysis, fantasy sports, or sports betting.
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
- **Automation:** Implement automated data scraping to collect all necessary information, such as today's games, player teams, and positions, so users don't need to manually input this data.


## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/csmotherman/NBAPlayerStat.git
