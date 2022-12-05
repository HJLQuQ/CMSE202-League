# CMSE202-League

This repository is centered around answering the question: Can we predict the winner of League of Legends Tournament?


Data Cleaning and Aquisition: Anirudh Agaram

  Data was obtained from Oracle Elixir (https://oracleselixir.com/tools/downloads). The dataset that showed team data from 2022 was used. 
  Only complete team data was filtered from the dataset. Once the complete team data remained, league, side, position, teamname, result, kills, assists,
       teamkills, doublekills, team kpm, dragons, elementaldrakes,
       dragons (type unknown), 'irstbaron, barons, towers,
       firstmidtower, firsttothreetowers, inhibitors, earnedgold,
       earned gpm, gspd, golddiffat10, golddiffat15, and xpdiffat15 remained in the dataset. The filtering was done by making the dataset into a correlation matrix and finding the features that correlated highest with the result of the match (win/loss).


Decision Tree Classifier : Haizhou Wang

Firstly, I chose to use decision trees for prediction for several reasons：
1. decision trees have very easy to understand decision rules
2. decision trees can handle non-linear features
3. the interactions between variables are taken into account

The prediction model based on the decision tree can reach 97.386% accuracy

In the final distribution of importance, it can be seen that the number of towers plays a crucial role in winning or losing a match, followed by earnded gmp, team death and team kills

Linear and Logistic Regression: Zhoufan Yu

1. Using the regional statistics data from Oracle Elixir in year 2022, we applied the Logistic regression classifier to predict the winning ratio of each team in their own regions. The predicted probabilities that are greater than 80 are considered winning. The training error of the model is: 0.0171, and test error is: 0.0224.

2. Using the statistics data in the group stage (https://gol.gg/teams/list/season-ALL/split-ALL/tournament-World%20Championship%202022/), we were able to build the linear regression model to predict the group stage winning ratio. The model MSE is 0.0127

3. Eventually, the results of knockout stage can be predicted by using the weighted winning ratio, which is consist of 70% weights of the group stage and 30% weights of the regional winning ratio. 

Multiple regression: Jeremy Bouford

This part contains an OLS multiple regression on the variable 'towers'. This is, as observed from other analysis, the variable that tells us the most about who will win the match. It fits the data with an adjusted R-squared of 0.913 and all of the predictors have a significance level below 0.05.

This is of importance because we can use this model to see what other aspects of the game lead to teams destroying opposing teams towers which is ultimately how a team wins the match.


