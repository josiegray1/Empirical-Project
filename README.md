# Empirical-Project
# Project Notebooks Overview

## 1. Box Office Scraping Notebook
**Libraries used**: Selenium, BeautifulSoup, Pandas
- Scraped a list of all-time worldwide box office movies from The Numbers.
- Downloaded the appropriate Chrome driver for Selenium: [ChromeDriver Downloads](https://chromedriver.chromium.org/downloads).
- Used Selenium to load dynamic page content and BeautifulSoup to parse and extract movie information (rank, year, title, worldwide gross).
- Scraped data from pages and saved it to `box_office.csv`.
- Cleaned `box_office.csv` and saved it as `worldwide_box_office_movies.csv`.

## 2. Success Metrics Notebook
**Libraries used**: Pandas, Matplotlib, Seaborn
- Downloaded pre-made CSV files containing movie awards data (BAFTA, Golden Globes, Oscars) from Kaggle:
  - [Kaggle Golden Globes Dataset](https://www.kaggle.com/datasets/)
  - [Kaggle Oscars Dataset](https://www.kaggle.com/datasets/)
- Cleaned and merged the datasets into `combined_awards.csv`.
- Created new columns for the number of nominations and wins for each movie.
- Downloaded Rotten Tomatoes ratings data from Mendeley.
- Cleaned and merged Rotten Tomatoes data with the awards data to create `final_combined_dataset.csv`.
- Categorized movies into groups: "Won Best Picture", "Won Award", "Nominated for Awards", "No Awards".
- Merged this data with box office data (`worldwide_box_office_movies.csv`) and created `success_metrics.csv` for analysis.
- Visualized data using Matplotlib and Seaborn.

## 3. Star Actors Notebook
**Libraries used**: BeautifulSoup, Pandas, Time, Requests, Collections.Counter, Ast, Re
- Scraped actor data from popular films on Letterboxd.
- Identified the most frequently appearing actors and selected the top ones.
- Scraped the list of highest-paid actors from Forbes.
- Merged actor data into a CSV file called `100_actors.csv`.
- Combined this data with cast/crew information and success metrics to create a dataset with star actors and their influence on movie success.
- Created binary variables for movies with and without star actors.
- Visualized the data with plots.

## 4. Budget vs Actors Notebook
**Libraries used**: Selenium, BeautifulSoup, Pandas
- Scraped production budget data from The Numbers.
- Used Selenium to automate page loading and BeautifulSoup to parse each HTML page.
- Extracted rank, release date, title, and production budget data.
- Stored the data in a CSV file called `production_budgets_movies.csv`.
- Ran a regression analysis on audience ratings, star presence, and budget, and visualized the results.

## 5. Genres Success Notebook
**Libraries used**: Pandas, Matplotlib
- Downloaded the `title.basics.tsv` dataset from IMDb.
- Cleaned and saved the data as `genres.csv`.
- Merged this data with `success_metrics.csv` for a comprehensive analysis.
- Categorized movies by genre and created visualizations to explore genre success.

## 6. Clichés Notebook
**Libraries used**: Requests, BeautifulSoup, TQDM, OS, Regex
- Scraped movie script links from IMSDb.
- Used BeautifulSoup to find links to full movie scripts, and then parsed the scripts for common clichés.
- Saved the scripts in a folder called `MovieScripts` within the "Empirical Project" directory.
- Defined a list of common clichés using regular expressions and scanned each script for these patterns.
- Results were saved in a CSV file (`cliches.csv`) showing the cliché name, script file, and match count.
- Cleaned the CSV file and saved it to `cliches_cleaned.csv`.
- Joined `cliches_cleaned.csv` with `success_metrics.csv` to create `cliches_success.csv`.
