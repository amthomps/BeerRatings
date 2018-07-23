# BeerRatings
There's nothing quite like kicking back at the end of the day with a fun machine-learning side-project.  The goal of this project is to develop a model that can predict how well a new beer will rate with users of the Untappd app.  Untappd has amassed a database of tens of thousands of beers and allows users to login, find the name of the beer they're currently enjoying (or not enjoying as much), and give the beer a 1-5 rating and a free-form review.  Also included in the database are facts about the beer, including the type of beer, the brewery, the ABV, and the city and state.  

This project consists of two parts: collecting a sample of beer ratings and facts via web scraping, and machine learning model generation.

## Contents:
* **CollectData.ipynb:** Python code written in Jupyter Notebook format used in web scraping and writing csv's with raw data
* **Analysis.ipynb:** Python code written in Jupyter Notebook format used to read in raw data, generate machine learning models, and perform analyses
* **untappd2.csv** Data collected from Untappd beer rating pages
* **breweries.csv** Data collected form Untappd brewery pages  

### Collect Data: *CollectData.ipynb*
This python code uses requests and beautiful soup to extract data from the Untappd web pages.  A small sample of about 300 pages for specific beers is collected first.  Next, pages for the breweries represented in this data set are accessed and scraped for brewery-specific information.  Please note that accessing these pages requires a login, and you will need to edit the username and password if you intend to run this code.

### Predict Ratings: *Analysis.ipynb*
Using the data collected in *CollectData.ipynb*, this code creates a tidy pandas dataframe, cleans the data using some regex and filtering, and uses some exploratory analysis.  Two models are generated separately and their performance is compared.  The first is a logistic regression model and the second is a K-nearest neighbors model.  
