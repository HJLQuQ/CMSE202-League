# CMSE202-League

This repository is centered around answering the question: Can we predict the winner of League of Legends Tournament?


Data Cleaning and Aquisition: Anirudh Agaram

  Data was obtained from Oracle Elixir (https://oracleselixir.com/tools/downloads). The dataset that showed team data from 2022 was used. 
  Only complete team data was filtered from the dataset. Once the complete team data remained, league, side, position, teamname, result, kills, assists,
       teamkills, doublekills, team kpm, dragons, elementaldrakes,
       dragons (type unknown), 'irstbaron, barons, towers,
       firstmidtower, firsttothreetowers, inhibitors, earnedgold,
       earned gpm, gspd, golddiffat10, golddiffat15, and xpdiffat15 remained in the dataset. The filtering was done by making the dataset into a correlation matrix and finding the features that correlated highest with the result of the match (win/loss).
