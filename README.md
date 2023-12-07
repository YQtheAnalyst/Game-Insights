# Exploratory Data Analysis: Steam Games
This project is under continuous updating! My next plan is to build an interactive dashboard for players to see the most popular games according to different genres!
## Technologies
1. Python

Pandas

Numpy

MatPlotLib

## Abstract
Steam is a video game digital distribution service and storefront developed by Valve Corporation. This dataset is from [Kaggle dataset](https://www.kaggle.com/datasets/nikdavis/steam-store-games) containing more than 27k Steam games and information including game names, genres, playtime, ratings, price, etc.

As an enthusiastic game player, I am interested in learning about the insights of existing Steam games, including the following questions:

- Which are the most popular games?

- What kind of genres do players like playing most?

To solve these problems, I utilized Python to do exploratory data analysis to answer the questions. 

## Exploratory Data Analysis

### The most popular games

I can define the "popularity of games" based on many performance metrics, such as the number of players, number of ratings, positive rate, and playtime. Let's see each performance metric one by one.

- Number of Players

The raw dataset has one categorical column which classifies the numbers of owners, and 6 games are owned by more than 20 million gamers, which are Dota 2, Counter-Strike: Global Offensive, Playerunknown's Battlegrounds, Team Fortress 2, Warframe, and Unturned.

[picture1]

- Number of Ratings

By adding the positive ratings and negative ratings, I obtained the total ratings of the games. The list of top 6 games is a little bit different from the last one which adds Grand Theft Auto V and Garry's Mod.

[pic2]

- Positive rate

Many games have a high positive rate. However, I cannot only utilize positive rates to define the most popular games as some games have small numbers of ratings. For example, the games "Room of Pandora" and "2048", have 4 total ratings and all of them are positive, which leads to a 100% positive rate.

Therefore, I set the threshold of the number of owners as 20k and the positive rate larger than 0.8. Here is what I got:

[pic3]

The top three games with positive rates are Portal 2, Factorio, and Rimworld!

- Playtime

Given the columns of `average playtime` and `median playtime`, I found the games with the most average playtime are The Abbey of Crime Extensum, The Banner Sage: Factions, and The Secret of Tremendous Corporation. However, I have doubts about this list.

Therefore, I explore further on playtime variables. I built the new column `playtime indicator` which equals `average_playtime - median_playtime`. The larger the differences, the more portion of players invest a considerable amount of time in the game. Here is the game list which has the most differences: Dota2, Final Fantasy XIV Online and Counter-Strike-Global Offensive. This list aligns with the previous list well!

[pic4]

### The most popular genres

From the analysis, the most popular genres are: Action, Adeventure, and Casual. One thing worth noticing is that "Indie" appears lots of times in the top genres. Indie games are getting more and more popular among developers!

[pic5]

## Results

I am going to give a list of the most popular games among players which have large players basement and positive rate! If you are new to games, you can pick your first game from this list! Based on the results of exploratory data analysis, the most popular games include Dota 2, Counter-Strike: Global Offensive, Playerunknown's Battlegrounds, Team Fortress 2, Warframe, Unturned, Portal 2, Factorio, Rimworld, and Fantasy XIV Online.