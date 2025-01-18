# Analysis of the online gambling game CrazyTime

### Project Overview

This data analysis project aims to provide insights into the gambling game CrazyTime. By analyzing the data:
* We seek to find patterns in the number of players during the day.
* What time of the day should a gambler play?
* What are the best positions in  the CashHunt table, that a gambler should choose?
* Make data-driven recommendations on what betting strategy should a gambler follow.
* Realize that on average the owner of the game has profit.


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
- What are the best betting strategies?
- If the owner of the game wins on average.

### Data Analysis

#### Results/Findings
The analysis results are summarized as follows:

1. One can see that there is great traffic between 14:30 - 17:30 GMT and low traffic during midnight hours. See NumberOfPlayers_plot.png .
2. Assuming that on average a gambler plays for 2 hours continuously, a suitable 2-hour session is during 8:35-10:35 GMT, when average multiplier is 8.4 . That means, if a gambler bets 1€ to each one of 8 possible results, the gambler on average will have 0.4€ profit for every result in this two hour period. On the other hand, between 12:00 and 16:00 definitely should not a gambler play, because on average the multiplier is very low. See 2-hour_Sessions.png.
3. We recommend positions (1,3) and (9,3) in CashHunt Table, because on average have the biggest multiplier. See CashHunt_Table_HeatMap.png.
4. On every possible result, we bet 1€. The top 5 strategies are :
   - Bet only CashHunt. Suppose that a result is CashHunt. The probability in the next 8 results the result is CashHunt, with multiplier at least 8, is 0.54.
   - Bet only 10. Suppose that a result is 10. The probability in the next 8 results the result is 10, with multiplier at least 10, is also 0.54.
   - Bet both on 10 and CashHunt. Suppose that a result is 10 or CashHunt. The probability in the next 4 results the result is either CashHunt or 10 with multiplier above 8, is 0.53.
   - Bet both on Coinflip and CashHunt. Suppose that a result is Coinflip or CashHunt. The probability in the next 4 results the result is either CashHunt or Coinflip with multiplier above 8, is 0.50.
   - Bet on three results, (10,Coinflip,CashHunt). Suppose that a result is one of these three. The probability in the next 2 results, the result is one of them with multiplier above 8, is 0.5.
See all possible betting strategies in the Strategies folder.
5. The average multiplier is 7.29. That means, on average, the owner of the game in each round has at least profit = 9% of the total amount that is bet from all gamblers in the corresponding round. Also, you can see from 2-hour_Sessions.png that most of the time average multiplier is below 8. That means, most of the time the owner gains money. Sometimes, when average multiplier is above 8, owner "rewards" gamblers by giving some money back. 


### Future plans:
1. Collect data for at least one month.
2. Calculate again the strategies, but with different ammount of betting on each possible result, and of course with more data. This will be deduced by doing some optimization.
3. Try to make predictions when a huge multiplier is gonna happen.
