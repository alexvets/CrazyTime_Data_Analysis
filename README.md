# Analysis of the online gambling game CrazyTime

### Project Overview

This data analysis project aims to provide insights into the gambling game CrazyTime. By analyzing the data:
* We seek to find pattern in the number of players during the day
* What time of the day should a gambler play
* Make data-driven recommendations on what betting strategy should a gambler follow
* Realize that on average the owner of the game wins


### Data Sources


  * **Origin:** https://casinoscores.com/crazy-time/
  * **Collection Method:** Web scraping .json files, with Python Selenium package.
  
 
  * **Collection Dates:**
    - 2024-12-01T10:22:57.476Z to 2024-12-06T15:05:11.980Z
    - 2024-12-17T19:17:15.991Z to 2024-12-19T15:14:06.419Z
  
  #### Data Files
  * **Raw Data:** WholeStats.csv
  * **Clean Data:** CleanData.csv  

### Tools
- **Python :** Data collection,data storage, data cleaning, data analysis and data visualisation.
   - **Packages:** Selenium, Sqlite3, Pandas, Numpy
- **DB Browser for SQlite :** Data analysis and data visualisation. 


### Data Cleaning/Preparation

In the initial data preparation phase, we performed the following tasks:

1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis

EDA involved exploring the CleanData.csv file to answer questions,such as:
- If there is any pattern in the number of players during the day.
- What time of the day should a gambler play?
- What are the best positions in  the CashHunt table, that a gambler should choose?
- what are the best betting strategies?
- If the owner of the game wins on average.

### Data Analysis

#### Results/Findings
The analysis results are summarized as follows:

1. One can see that there is great traffic between 14:30 - 17:30 GMT and low traffic during midnight hours. See NumberOfPlayers_plot.png .
2. 
