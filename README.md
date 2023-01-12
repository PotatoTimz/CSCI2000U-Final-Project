# CSCI 2000U - Scientific Data Analysis
## Final Project - Proposal
**Date:** December 06, 2021.
### Project Group 20

#### List of Group Members & Contributions: 
Andre Alix: Introduction, Description of data, Data Reformating, 4.1, 4.2, 4.3, Conclusion

Daniel Batchellor: Data Cleaning, 4.5

Luis Octavo: Data Reformatting, 4.4, 4.6, Potential Data Science, Conclusion, readme

## Introduction: 

The video game industry has grown tremendously in the past few decades. It has become the fourth largest entertainment sector supassing both the Movie and Music industries. Due to its growing popularity multiple sub-genres have spawned to capitlize on the growing trend. The Esports industry is a form of competition between players. Similar to sports this takes the form of organized competititons between multiple players either in a team or individually. 

![Imgur](https://i.imgur.com/ODnSkNM.png)

Source: https://businesstech.co.za/news/lifestyle/88472/the-biggest-entertainment-markets-in-the-world/ 
 
Our group decided it would be interesting to do a report on this topic because of our interest in the video game industry. Esports is a rising subsection and we would like to see its current trends. Since we have the general knowledge of the industry as a whole it would be easier to make conclusions based on our findings. 

The goal of this report is to understand the current Esports climate. We will be trying to find patterns between the most successful games in the industry and take a look at the overall scope of the industry. This will be done through visualizing data collected about the numerous Esports titles collected in our datasets.

## Description of Data:

### Dataset Name: Esports Earnings 1998-2021
###### Link: https://www.kaggle.com/rankirsh/esports-earnings

The dataset contains information about various Esports titles and total cash prizes between 1998 to 2021. It organizes the data on a game title basis and contains information about the game (platform, genre, etc) and information about its esports infrastructure (players, total earnings).

Information found in the datasets were found through:

   *  Data found on website [EsportsEarnings.com](https://EsportsEarnings.com)
   *  Data found in [Rushikesh's original dataset](https://www.kaggle.com/rushikeshhiray/esport-earnings) 
   *  [EsportsEarnings.com](https://EsportsEarnings.com) is a website that contains stats about esports prize distribution. This includes filters to divide the earnings by player, country, game, etc.
   
(https://www.kaggle.com/rushikeshhiray/esport-earnings) also uses data from [EsportsEarnings.com](https://EsportsEarnings.com)

#### Data Attributes
Each data attribute is recorded in a per game basis. 

   * __Game__: Name of the game.
   * __ReleaseDate__: Date which the game was released.
   * __Genre__: Genre of the game.
   * __TotalEarnings__: Total prizepool allocated in tournament. *(Some values have values beyond two decimal places because of exchange rate)*
   * __OnlineEarnings__: Total prizepool for tournaments that took place in an online setting.
   * __TotalPlayers__: Amount of players that have recieved some prize *(money)*
   * __TotalTournaments__: Total tournaments that have recorded data 
  
### Dataset Name: Esports Earnings
###### Link: https://www.kaggle.com/jackdaoud/esports-earnings-for-players-teams-by-game

The dataset contains information about Esports players and contains information about their total earnings, the game they play professionally, etc. Organizes the information on a player by player basis and helps us determine information on the game that the given player is known for.

Information found in the dataset were found through:

   *  Data found on website [EsportsEarnings.com](https://EsportsEarnings.com)
   *  Data found in [Rushikesh's original dataset](https://www.kaggle.com/rushikeshhiray/esport-earnings) 
   *  Data found on [Tableau story on Esports.](https://public.tableau.com/app/profile/jack.daoud/viz/eSportsReport/Story)

#### Data Attributes
Each data attributes is recorded on a player basis.

   *  __Playerid__: player id found on [EsportsEarnings.com](https://EsportsEarnings.com)
   * __NameFirst__: First name of given player.
   * __NameLast__: Last name of given player.
   * __CurrentHandle__: In game name.
   * __CountryCode__: Country of origin of player (given in abbreviation. 
   * __TotalUSDPrize__: Total prizepool of player in USD.
   * __Game__: Main game player competes in.
   * __Genre__: Genre of player's main game.
   
   
### Dataset Name: Esports Earnings 1998-2020
###### Link: https://www.kaggle.com/webbery/esports-earnings-19982020

The dataset contains information about a country's tournament success in Esports. Contains information about given countries total earnings, etc. 

Information found in dataset were found through:

   *  data found on website [EsportsEarnings.com](https://EsportsEarnings.com)

#### Data Attributes
Each data attributes is recorded on a country basis. 

   * __Year__: The year the data was collected for
   * __Country__: The country the data is based on
   * __Total Prize Money (Year)__: Total prize money country has obtained in the according to given year
   * __Number of Players__: Numbers of players that represent the given country
  
### 3.1 Data Cleaning

Before we start to work with the data we must clean up our dataframe many games on the database may have one or two tournaments off shoots or events with small amounts of prize money. We have decided to ommit these cases as they may skew our data.

We would like to remove games that:
- Do not have at least 5 "TotalTournaments" held
- Has a recorded "TotalEarnings" of less than $2000
- That have less than 5 "TotalPlayers"

Doing this will help remove games that have little to no relevence to the broader Esports market giving us a much more accurate data through the removal of potential outliers.

Removing all of these games will be important to keeping our data consistent and remove possible outliers that may skew the data. 

Before cleaning the dataset we had about 540 different games. After removing possible outliers we are left with 265 games cutting out about half of the games that we started with. Though this may seem high it is important that we remove games that have little relevance and can skew our data. 

### 3.2 Data Reformating:

Since we will want to work with statistics it would be a good idea to convert all columns storing numeric values into float type variables within the dataframe. This way all the data we are working with remains consistant.
### 3.3 Pre-Processing: 
We would like to devide our data by genre as we predict that it may answer some of the questions we are lookign to answer.

### 4.1 Exploring Genres

To understand the current state of the Esports industry we would like to examine the different genres of the gaming industry. Understanding the popularity of each of the genres in relation with each other. 

We will create two different charts totaling earnings and player count by genre. This will help us determine the popularity of each genre.
The names of of the given genres are pretty long. Because of this we will abbreviate each of the genres in the dataset according to the legends below

#### Abbreviation Legends
    1)Battle Royale = BR
    2)Collectible Card Game = CCG
    3)Fighting Game = FG
    4)First-Person Shooter = FPS
    5)Multiplayer Online Battle Areana = MOBA
    6)Puzzle Game = PG
    7)Racing = Ra
    8)Role-Playing Game = RPG
    9)Sports = Sp
    10)Strategy = St
    11)Third-Person Shooter = TPS
    
![Imgur](https://i.imgur.com/Md3XH7A.png)
*Clearer image for graph can be found at https://i.imgur.com/Md3XH7A.png*

![Imgur](https://i.imgur.com/WZ8pDmG.png)
*Clearer image for graph can be found at https://i.imgur.com/WZ8pDmG.png*

Based on the two graphs we can see that the genres that tend to have the largest amount of earnings seem to be similar to the games with highest player count. The top 3 games with the highest earnings are MOBA, FPS and BR. Each of these genres in terms of total prize distribution is in the hundred millions while the games below it are in the ten millions and below. Granted these are just the prize support we do not know how much money is being generated through third party sources (sponsors, streaming rights, investments, etc). The lowest prize support for any given genre is puzzle games which has a total prize distribution in the 50,000 range. Looking at the total player per genre we see that similar to earnings the top 3 games are FPS, MOBA and FG. FG being the only genre that did not make the top 3 in total earnings. At a glance the two charts seem similar. You can see that the games that tend to have a larger prize distribution also have a larger amount of professional players. The two games that break this trend being FPS and FG. FPS has the largest player count totaling over 40,000 players however the genre only has the second highest prize distribution with about 275,000,000 prize distribution. Comparatively MOBA's have about 17,000 players (less than half of fps) but has the highest total distribtion totaling almost 400000000. This biggest outlier while comparng the two lists of data is the FG genre. The genre has the third largest player base of about 13000 and the sixth largest prize support of about 23000000. This is a huge outlier considering the BR genre have a similar playerbase count but a much larger prize support 173000000, which is over seven times the amount as the fighting game genre. Other than a few outliers it seems to be a clear correlation between the player count of a game and its total earnings.

### 4.2 Comparing data about top 10 games.

In this section of the analysis we will go through the front runners in terms of total player base and earnings and see if there is some sort of correlation between the two.

Finding the top 10 games in terms of overall playerbase: This will show us the total amount of players to have been recorded to earn money from tournaments.

![Imgur](https://i.imgur.com/FPKKoth.png)
*Clearer image for graph can be found at https://i.imgur.com/FPKKoth.png*

Finding the top 10 games in terms of total prizepool: This will show us the total prizepool that has distributed between the competitive life span of a game.

![Imgur](https://i.imgur.com/1D8qLa9.png)
*Clearer image for graph can be found at https://i.imgur.com/1D8qLa9.png*

Here we display graphs to better display the total earnings and total player base that each of the top 10 games.

![Imgur](https://i.imgur.com/daycx5I.png)
*Clearer image for graph can be found at https://i.imgur.com/daycx5I.png*

When we look at the games that have the highest total playerbase we can see that the top 2 games have a much larger playercount than the rest of the list. Counter-Strike: Global Offensive and League of Legends have the two largest player bases. When looking at the playercounts for the top 3 games we can see that CS:GO (1st) has over 14000 players, League of Lengends (2nd) has less than half having about 7000 players and Fortnite (3rd) having just as large of a drop with 4000 players. The graph slightly skews right showing that player count is not well distributed between the top 10 games. However other than the top 2 games the next 8 games (Fortnite - Super Smash Bros. Ultimate) do not have as large of a drop off.

One suprising thing to note is that games like Super Smash Bros. Ultimate and Heartstone are 1v1 games which makes their large total playerbase more impressive considering how each match will consist of less players. The other games on this list tend to be team games (Counter-Strike, League, Fortnite) which consist of teams of 3-6 players. Because of this some notable games may not appear on this list such as Starcraft 2, Street Fighter V, etc due to their 1v1 nature

![Imgur](https://i.imgur.com/RAu0S82.png)
*Clearer image for graph can be found at https://i.imgur.com/RAu0S82.png*

When analysing the top 10 games by earnings we see that Dota 2 (which had the 5th largest playerbase) has the highest total earnings. This is suprising considering that Counter-Strike has about 400% more players than Dota 2, however we can see that Dota 2 has more than double Counter-Strikes total prize distributions. Other than a few of the placements however many of the games in the top earnings also appear in the top player count.

Looking at the earnings we can see that their is a larger spread in distribution between the top 4 games and the other 6. Looking at the top player bases we can see that other than the top 2 the other games steadly drop in players. Looking at the total Earnings we see much larger skew right. Adding the the earnings of rank 5-10 games would total less than the overall earnings of Dota 2. This shows the large difference in total earnings between the top games and the lower top games.

We can conclude that their is some correlation between a games playercount and total earnings however their are deffinitly some notable outliers to this trend that can be further investigated.

### 4.3 Analysing the Distributions between game genres
Now that we see that we have an understanding of the most popular genres and top games in the industry we would like to see if their is some correlation between the two. We believe that it is likely the the top games should line up with the popular genres. Seeing that the top genres (FPS, MOBA and BR) have a larger share over the industry it is likely that we will see these 3 genres appear a few times when looking at the top 10 games.

We are calculating the total sum of players and earnings by genre only using the top 10 games:

![Imgur](https://i.imgur.com/ndu8pp3.png)
*Clearer image for graph can be found at https://i.imgur.com/ndu8pp3.png*

![Imgur](https://i.imgur.com/3B63NtB.png)
*Clearer image for graph can be found at https://i.imgur.com/3B63NtB.png*

![Imgur](https://i.imgur.com/gqZ1Ana.png)
*Clearer image for graph can be found at https://i.imgur.com/gqZ1Ana.png*

Looking at the pie graphs we see the three largest genres in the top 10 games match the results we see in the top genres. MOBA, FPS and BR clearly dominate the the top 10 games taking well over 75% of the distribution combined. Another point to note is that the next 3 most popular genres found earlier Strategy, CCG and Fighting have also appeared in the top 10 genres.

Another similarity in the results of these pie graphs and our graphs from 4.1 are the domination of FPS in the total player count category and the MOBA in the total earnings category. We see that FPS games in the top 10 account for about half of the player count of the top 10 games. Which is a similar result to the what was observed earlier in the genres total player count. Similarly MOBA accounts for just under 50% of the total earnings which again is similar to the result observed in the genre total earnings chart.

Through this result we can see clear correlation between the top 10 genres and games. This further emphsises the point that the largest Esports titles clearly dominate the market. These games make up a very large portion of the industry and is integral for its success 

### 4.4 Analysis between the top 5 games and the rest

In our last analysis we found that their is large similarity between the charts found in our top 10 games and top genres chart. This shows that the top games most likely had a large impact on the genre chart skewing the results through the top games.

In this section we would like to anylise the top 5 games in terms of earnings and check its total weight compared to the rest of the dataset. Given our prior data we believe it is likely for the top 5 games to make a up a large portion of our data which will be proven through this analysis.

Creating dataframes that containg the top 5 games in terms of "TotalEarnings" and the rest of the games:

Sums the total value for the top 5 games and the rest of the games and uses creates a pie chart to compare the two:

![Imgur](https://i.imgur.com/abDtSAl.png)
*Clearer image for graph can be found at https://i.imgur.com/abDtSAl.png*

Looking at this distribution we can see that our assumptions were correct. We see that the top 5 game's prize disribution were larger than the rest of the total prize distributions combined. These results is no suprised concidering the distribution seen in the previous analysis. The top 5 Esports titles are much more popular in terms of financial support that the other Esports titles. Even amongst the top 5 there is reason to believe that they may still be some large jumps in prizepools between these games. The raise of the industry can show that many of the larger games have become much more popular than others.

### 4.5: Determing Relation Popular game and Release Date

We are using the TotalPlayers, TotalTournaments, and TotalEarnings in order to sort and figure out whether age helps determine the popularity of a game.

![Imgur](https://i.imgur.com/lmR758n.png)
*Clearer image for graph can be found at https://i.imgur.com/lmR758n.png*

We sorted by The total amount of players to see the most popular games by looking for the games with the most amount of players. This will give us the opinion of the people competing in the games to see what games they prefer. It looks like games that are newer releases in the 2010s are more present in esports than older releases before 2010s when it comes to the total amount of players.

![Imgur](https://i.imgur.com/cY3IWNJ.png)
*Clearer image for graph can be found at https://i.imgur.com/cY3IWNJ.png*

We sorted by The total amount of tournaments held to see the most popular games by looking for games with the highest amount of tournments held. This will give us the opinion on what the fans want to see when it comes to games. It looks like games that are newer releases in the 2010s and 2000s are more present in esports than older releases before 2000s when it comes to the total amount of tournaments.
![Imgur](https://i.imgur.com/g2Ia1tq.png)
*Clearer image for graph can be found at https://i.imgur.com/g2Ia1tq.png*

We sorted by the total amount of earnings to see the most popular games by looking for the games with the highest total earnings. This will give us the opinion of the organizers and sponsors in what games tournaments they want to support. It looks like games that are newer releases in the 2010s are more present in esports than older releases before 2010s when it comes to the total amount of earnings.

With this data it can be said that the newer the game (around the 2010s) the more popular it is with the esports community. So according to the data the age of the games does affect the popularity of the games in the esports community, the newer the games the more popular it is.

### 4.6 An analysis of the top players and countries

In this analysis we will be looking into the highest earnings players and countries to see if their are any correlation between these and the popular games that we have found in our previous analysis.

It is likely that games like Dota 2 which have a large amount of earnings will likely be popular in the most succesful countries and players.

Looking into the top earning players in the world and the top earning countries (using the new data set):

![Imgur](https://i.imgur.com/p8PVVZc.png)
*Clearer image for graph can be found at https://i.imgur.com/p8PVVZc.png*

![Imgur](https://i.imgur.com/y5LMGpe.png)
*Clearer image for graph can be found at https://i.imgur.com/y5LMGpe.png*
Source: [EsportsEarnings.com](https://EsportsEarnings.com)
​
Up next is to find the distribution of the players' nationalities with relation to their accumulated winnings.
​
Based on our findings, the top countries with the most earnings are United States, China (PRC) and South Korea. More than half of the top 20 consists only of these 3 countries. 
​
The share of the top 20 by continent is as follows:
- Americas - 3 countries
- Eurasia - 9 countries
- Asia - 7 countries
- Oceania - 1 country

## Potential Data Science 

The datasets used in this final report has potential for further analysis.

Datasets involving prize pool data:<br>
Tournament prize pools has diminished in value of significance for latter half of the decade. However, the metric is still useful in terms of the monetary capacity of the game or genre.
- Which games have higher return on investment with regards to potential prize money and game popularity.
- Can be used as a factor in determining team investment decisions.
- Determining competition in a specific game or genre (how many professionals are competiting, has it reached its saturation point, etc.)

Datasets involving player counts:<br>
Data can be used for scouting players, using nationality, games and genres as possible factors for consideration.
- Which players wins the most on tournaments? Does the nationality have a factor?
- Which genres of games are a specific nationality good at?
- Which countries excel at what game and does it correlate to all games of the same genre?

## Conclusion

Through our analysis we have learned that the eSports market is being dominated by the top few games. The majority of the earnings, players and tournaments are being held for the most popular games while the other games are getting much less support. We can also see that similar games seem to hold similar results. Through our analysis we find that the FPS and MOBA genre's are dominating the esports industry as 5 of the most popular titles such as "Counter-Strike: Global Offensive", "League of Legends" and "Dota 2" have larger success drawing in player and prize support. The large monopoly that these games had on the industry was surprising to us. While we knew that these games were very popular we did not expect these games to have such a large share on the industry. The fact that top 5 games held the majority of the prize support is very suprising considering the amount of title's there were in the database.

One specific point we believe this report was lacking was a more in-depth analysis on tournaments. Other than the total amount being held for each game we had very little info on the specifics for each tournament. Being able to see the prize support for the largest tournaments and which games they were being held for would have been great way to analyze the larger gaps in prize support. For example a game like "Super Smash Bros. Melee" has the fourth largest amount of total tournaments. However is no where to be seen in the top prize support per title category. Being able to see specific details for each tournament would allow us to find potential outliers that are skewing the prize support data. One example being Dota 2's "The International 2021" which have some of the largest prize supports in Esports history, having over $40M of prize support. Which is larger than the majority of most titles total earnings. 

Another shortcoming to point out is the lack of a broader scope in terms of Esports in general. Getting a generalized view on the scene would help greatly in further investigations such as player count, viewer counts / engagement, etc. With only the tournament data in hand, we are limited to questions related to solely game tournaments.

Overall we are satisfied with our analysis of the dataset and feel that we can confidently say that the Esports industry is growing. However the top titles have far more influence and larger support than other titles. We can see that games in specific genre's generally have  a better chance in becoming popular eSports titles than others. We believe the data we collect would be useful to understand the current economic enviorment of the eSports industry as well as an understanding of the current landscape of competitve gaming.

##### All methods for obtaing this data can be found in the .ipynb file

## References

The biggest entertainment markets in the world (2015, May 31). Businesstech. https://businesstech.co.za/news/lifestyle/88472/the-biggest-entertainment-markets-in-the-world/ <br>
eSports: Should You Start a Startup? (2020, Oct 23). tableau. https://public.tableau.com/app/profile/jack.daoud/viz/eSportsReport/Story

## Notebook Report Instructions
In order for the report to run, please follow the instructions below.
1. Check required Files (must be in the same directory):
- Final_Project.ipynb
- Top_Countries.csv
- highest_earning_players.csv
- GeneralEsportData.csv

2. Open Final_Project.ipynb and run the notebook one cell at a time. Wait for each cell to initialize their output.

## Acknowledgements
This project was submitted as the final course project for CSCI 2000U “Scientific 
Data Analysis” during Fall 2021. The authors certify that the work in this 
repository is original and that all appropriate resources are rightfully cited.
