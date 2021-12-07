# CSCI2000U-Final-Project
# The State and Growth of Esports Tournaments (1998-2021)

## Authors
- Andre Alix
- Daniel Batchellor
- Luis Octavo

## Introduction
E-Sports has experienced massive interest among young viewers and this report aims to find common patterns and trends of the current gaming landscape. This report explores the rapid growth of a subset of the gaming industry.

Datasets used:
- Esports Earnings 1998 to 2021 by Ran.Kirsh (https://www.kaggle.com/rankirsh)
- eSports Earnings by Jack Daoud (https://www.kaggle.com/jackdaoud)
- eSports Earnings 1998-2020 by Webbery (https://www.kaggle.com/webbery)

## Analysis
The summarized report aims to answer a few questions.
- How big is the professional Esports industry in specific games / genres with regards to tournament prize pools.
- What are the games that has the most prize pool allocation.
- What is the distribution of professional players based on their nationalities

A fairly common question is how big the professional scene has grown over the years. A metric we can use to determine this is by getting all the player count for each genre. Afterwards, we can go into a game by game basis.

There are 11 genres that the Esports envelops (abbreviation legends as follows):
1) Battle Royale = BR <br>
2) Collectible Card Game = CCG<br>
3) Fighting Game = FG<br>
4) First-Person Shooter = FPS<br>
5) Multiplayer Online Battle Areana = MOBA<br>
6) Puzzle Game = PG<br>
7) Racing = Ra<br>
8) Role-Playing Game = RPG<br>
9) Sports = Sp<br>
10) Strategy = St<br>
11) Third-Person Shooter = TPS<br>

We then check what is the distrubution of prize money throughout the two decades: <br>
![Imgur](https://i.imgur.com/Zp5bJiT.png)

From the data in the graph, we can see that MOBA, FPS and BR top the charts in terms of tournament prize money. The gap between the top genres to the remaining ones is gigantic approaching differences of at least 100M. The bottom 3 includes RPG, TPS and Puzzle Games which barely competes with the other genres.

Looking further, we can check which games bring the most tournament money overall. <br>
![Imgur](https://i.imgur.com/YycLsUm.png)

Based on our findings, Dota 2 tops the charts accounting around 276 million in prize money throughout its tournament lifespan followed by Counter-Strike: Global Offensive and Fortnite with 125 million and 108 million respectively.

Up next is to determine the amount of professional players per game. Which is graphed below: <br>
![Imgur](https://i.imgur.com/HGdT8So.png)

Counter-Strike: Global Offensive tops the charts in the amount of professional players competing followed by League of Legends and Fortnite. 

With data from graph 2 and 3, we can determine that Dota 2 has the highest amount of tournament earnings while only being 5th in terms of amount of professional players. Counter-Strike: Global Offensive is the most competitive among the games having over 14000 professional players competing.

With regards to professional players, we can also look on how nationality plays a part in terms of amount winnings. <br>
![Imgur](https://i.imgur.com/ulOnfEO.png)

Based on our findings, the top countries with the most earnings are United States, China (PRC) and South Korea. More than half of the top 20 consists only of these 3 countries. The three countries mentioned are the leaders in different genres, South Korea leads in the MOBA genre followed closely by China. The United States excels in FPS and BR. All of these genres have lucrative price pools which makes sense considering the prize share on all genres.


## Conclusion
Through our analysis we have learned that the Esports market is being dominated by the top few games. The majority of the earnings, players and tournaments are being held for the most popular games while the other games are getting much less support. We can also see that similar games seem to hold similar results. Through our analysis we find that the FPS and MOBA genre's are dominating the esports industry as 5 of the most popular titles such as "Counter-Strike: Global Offensive", "League of Legends" and "Dota 2" have larger success drawing in player and prize support. The large monopoly that these games had on the industry was surprising to us. While we knew that these games were very popular we did not expect these games to have such a large share on the industry. The fact that top 5 games held the majority of the prize support is very suprising considering the amount of title's there were in the database.

A shortcoming to point out is the lack of a broader scope in terms of Esports in general. Getting a generalized view on the scene would help greatly in further investigations such as player count, viewer counts / engagement, etc. With only the tournament data in hand, we are limited to questions related to solely game tournaments.

Overall we are satisfied with our analysis of the dataset and feel that we can confidently say that the Esports industry is growing. However the top titles have far more influence and larger support than other titles. We can see that games in specific genre's generally have  a better chance in becoming popular eSports titles than others. We believe the data we collect would be useful to understand the current economic enviorment of the eSports industry as well as an understanding of the current landscape of competitve gaming.

For a more in-depth look at the report plus the methodology in determining the results, visit the full report in the notebook. Instructions are added below.

## Acknowledgements
This project was submitted as the final course project for CSCI 2000U “Scientific 
Data Analysis” during Fall 2021. The authors certify that the work in this 
repository is original and that all appropriate resources are rightfully cited.

## Notebook Report Instructions
In order for the report to run, please follow the instructions below.
1. Check required Files (must be in the same directory):
- Final_Project.ipynb
- Top_Countries.csv
- highest_earning_players.csv
- GeneralEsportData.csv

2. Open Final_Project.ipynb and run the notebook one cell at a time. Wait for each cell to initialize their output.
