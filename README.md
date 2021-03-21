# STOR-538-Project-2

The primary goal of this project is to design models for prediction of three variables – Spread, Total, and OREB. Below you can find clear definitions of these three outcome variables. It is imperative that you follow these specifications. Your group will be making predictions of the three variables for all NBA games between April 10 and April 30, inclusively. Your predictions should be saved in the dataset called Predictions. Here you will find missing values where future predictions will be placed. This completed file should be submitted along with a paper summarizing your methodology. You will not only be graded by your methodology, but also by your predictive accuracy. The variables, Spread, Total, and OREB will all be evaluated by root mean squared error (RMSE). For each of the variables, the top 6 groups will get 3 points, the middle 6 groups will get 2 points, the bottom 5 groups will get 1 point. All three variables are numeric. If you don’t submit numeric predictions, you will get 0 points.

Spread=Home Points−Away Points

Total=Home Points+Away Points

OREB=Home OREB+Away OREB

To build adequare predictive models, historical data is needed for training and testing. The dataset games contains important information about every game in the NBA since 2004. I would advise only using a subset of the data from recent years. The dataset games_details contains player level data for the games. This dataset is a massive dataset. The previous two datasets are organized using TEAM_ID. The dataset teams links TEAM_ID to each team’s NICKNAME and CITY. This will be extremely important when you go to inputting your predictions into the Predictions file.

The data you are given involves basic box score information. Because of this, you are required to engineer new variables and use outside data. This is highly recommended to gain a competitive edge in the sports betting market. For the engineering of new variables, consider creating differences and ratios between the stats for the home and away teams. Also, it may be useful to create variables that represent past information such as moving averages or lagged variables. These are just two basic examples. For the use of outside data, explore research for what other variables could be important for predicting these three variables. If you take the time to get data from games in the 2021, this data will be considered outside data.

For ideas on data engineering and more examples of outside data consider the following:

Nathan Lauga’s Kaggle
Advanced Stats on NBA.com
Injury Data from Kaggle
Injuries from Basketball Reference
Webscraping from Basketball Reference
R Package: nbastatR
Information Using nbastatR -Installation for nbastatR
Your study should be summarized in a paper of 3 to 7 pages. The paper and predictions should be submitted on Sakai before 5:00PM on the due date. Each group should have their own paper and predictions, but both need to be submitted by every member of the group. Also, each group member needs to assess the contribution value of the other members of the team on a scale from 0 (Bad) to 3 (Excellent). When you submit your paper on Sakai, you should write the full names of the other group members and the value of their contribution. Your individual value will be determined by the average score of the other members in your group gave you.

On the first page, you should title your paper and give the names of the team members who contributed. The content of the paper should be organized in the following 4 subsections:

1) Data Information
In this section, you should discuss three things.

First, you should explain the steps taken to get the datasets cleaned and joined. How did you handle missing data? What did you do to identify outliers and how did you handle these instances? Were there any games intentionally removed and what were the reasons?

Second, you should discuss any variables engineered and defend the reason. You are required to create/engineer at least one variable that doesn’t exist in any dataset in repository. You should be able to explain why you think the variable you created would help in predicting any of the three outcome variables.

Third, you should discuss all outside data you joined into your dataset to hopefully improve prediction. You are required to utilize at least one variable that is not currently contained in any of the given datasets. This could be division (yes or no), injuries, attendance, advanced stats, or any data from 2021, etc. For all data you bring into your predictive models from outside sources, you should site the source and/or defend the reason for incorporating the data into your model.

2) Methodology for Spread
You should clearly describe your group’s best predictive model for Spread and the steps you took to get there. Discuss what variables were useful and useless for predicting spread. Since Spread is a numeric variable, I highly recommend a basic linear regression as a baseline with stepwise algorithms or regularization for variable selection. To ensure you are seeking the best model for prediction, I highly advise considering many different types of models (neural nets, regression trees, time series, etc.), utilizing cross-validation, and adding interaction/polynomial terms. In this part, you should chronologically write about everything your group did to find the best model. Challenge yourselves to a thorough investigation from multiple angles and organize your process professionally for an audience with basic understanding in statistics and the sport. You are not required to present tables or figures, but these can be used to defend why the model you are calling the “best” is actually best.

3) Methodology for Total
You should clearly describe your group’s best predictive model for Total and the steps you took to get there. Discuss what variables were useful and useless for predicting spread. Total is a numeric variable but could be highly skewed, I highly recommend nonlinear transformations or a poisson regression with stepwise algorithms or regularization for variable selection. To ensure you are seeking the best model for prediction, I highly advise considering many different types of models (neural nets, regression trees, time series, etc.), utilizing cross-validation, and adding interaction/polynomial terms. There should also be out-of-sample testing for consideration in model selection and potential regularization. In this part, you should chronologically write about everything your group did to find the best model. Challenge yourselves to a thorough investigation from multiple angles and organize your process professionally for an audience with basic understanding in statistics and the sport. You are not required to present tables or figures, but these can be used to defend why the model you are calling the “best” is actually best.

4) Methodology for OREB
Your methodology for OREB can be extremely similar to your methodology for Total since they are both count variables. Your methodology can be similar but the optimal model for OREB may contain different variables than the optimal model for Total, and this should be discussed. The problem with OREB is that the variable is not currently given on the game and team level in games. This variable is contained on the player level in the massive dataset games_details. For additional help on cleaning the data and obtaining the OREB variable for each of the games in the data, check out this R Script. In this R file, I go through the process of aggregating the offensive rebounds for both the home team and the away team, and then I merge that information into the original data to create an OREB variable.
