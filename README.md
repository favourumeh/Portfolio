# Favour Umeh Portfolio
This portfolio highlights some of the Data Engineering and Data Science projects that I have undergone in 2021

## Project 1 (Data Engineering): [Basketball Reference Data Pipeline](https://github.com/favourumeh/DATA-PIPELINE)
- Created a data pipeline that can scrape and clean tabular statistical data from BasketballReference.com and store it in a local MySQL server and/or Excel workbook. 
- The data in question is per-game statistics from the national Basketball Association (NBA) and it will be used to undergo regression and classifcation projects (see projects 2 and 3)
- The NBA is the top professional basketball league in North America. It was founded in 1947 and is currently home to the best basketball players in the world. 
- The figure below shows the cleaning and transformative action undergone on the raw data

![](/Images/Cleaning_Actions.png)

## Project 2 (Data Science): [Predicting Turnovers](https://github.com/favourumeh/Multiple_Linear_Regression---Predicting-Turnovers-)
 - In this project two multiple linear regression models were created to predict the turnovers committed by an NBA player per 36 minutes (TOV)           
 - Ultimately it was found that Two-point attempts per36(2PA), Free throw Attempts per36(FTA) and Assists per36(AST) were the only factors from the dataset that had a notable effect on the TOV:
 
      - **R2 = 0.46** . This is low because the model does not factor a player's skill which is the primary predictor of TOV. The R2 suggests that there is a significant variance in skill level amongst players  
        
      - **RMSE = 0.529** . The value of this error is roughly 25% of the mean TOV observed. 

- The models created can be used to assists NBA coaches in player development because the model acts as a predictor of a player's expected TOV. A player vastly outperforming their expected TOV (i.e. commits less TOV than expected) could indicate good ball retention skills which would mean that they require more on-ball possessions. It can also be used to pinpoint players who need more training in ball retention. 
- The figure below shows displays the use of correlation plots for feature selection
![](/Images/Correlation%20plot.png)

## Project 3 (Data Science): [Identifying the position of an NBA player](https://github.com/favourumeh/Identifying-Player-Position)
![](https://github.com/favourumeh/Identifying-Player-Position/blob/main/KNN/final%20images/tuning_k.png)
![](https://github.com/favourumeh/Identifying-Player-Position/blob/main/Evaluation%20images/Confusion%20matrices%20for%20all%20non-ensemble%20models%20for%20evaluation%20data.png)
![](https://github.com/favourumeh/Identifying-Player-Position/blob/main/Evaluation%20images/Confusion%20matrices%20for%20all%20ensemble%20models%20for%20evaluation%20data.png)
