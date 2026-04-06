# Steam Games Analysis
### COSC 301 Data Analysis Project

## Project Overview
Thousands of games launch on Steam annually. This high volume of releases has made visibility a critical challenge for developers. This project moves beyond the viral success stories to analyze the market health of the average Steam game and what developers can do to increase the likelihood of success of their game. 

Using a dataset of ~35,000 titles, we track the journey from raw marketplace data to actionable insights, identifying the "hidden rules" of pricing, platform support, and community engagement.

## Core Research Questions
1.  **Platform Usage:** How does cross-platform support (Mac/Linux) correlate with game ownership? 
2.  **Genre Velocity:** Which genres are currently dominating the market and how has their sentiment evolved?
3.  **Best Value:** Where do players find the highest "Playtime per Dollar" spent?
4.  **Hidden Gems:** Which games maintain 95%+ positive sentiment despite low marketing reach?
5.  **Cult Classics:** Which titles have managed to build exceptionally loyal fanbases (high playtime) despite modest player counts?

## Data Pipeline
*   **Data Processing:** Python (Pandas, NumPy)
*   **Storage:** SQLite3 (Local relational database)
*   **Visualization:** Matplotlib, Seaborn
*   **Source Data:** Steam Game Scraper (`games.json`)

## Workflow
1.  **Ingestion & Cleaning (`data_cleaning.ipynb`):**
    *   Parses raw JSON data acquired from the [Steam-Games-Scraper](https://github.com/FronkonGames/Steam-Games-Scraper).
    *   Handles missing values, dataframe form, and creates relational tables.
    *   Saves cleaned data into `steam_games.db`.
2.  **Analysis & Insights (`analysis.ipynb`):**
    *   Connects to the SQLite database to query cleaned data.
    *   Performs Exploratory Data Analysis (EDA) on market health (Dead/Ghost games).
    *   Computes complex correlations and categorical aggregations.
3.  **Export:**
    *   Generates targeted CSVs (e.g., `hidden_gems.csv`, `cult_classics.csv`) for further visualization or reporting.


## Setup & Usage
1.  **Data Gathering:** Gather the `games.json` file using the [Steam-Games-Scraper](https://github.com/FronkonGames/Steam-Games-Scraper).
2.  **Clean the Data:** Run all cells in `data_cleaning.ipynb` to generate `steam_games.db`.
3.  **Run Analysis:** Run `analysis.ipynb` to see visualizations and generate report CSVs.

