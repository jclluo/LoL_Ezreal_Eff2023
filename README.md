# LoL_Ezreal_Eff2023
An analysis of champion Ezreal's effectiveness in the realm of 2023 League of Legends Esport. (Project for DSC80 at University of Califrnia San Diego))

## Introduction
League of Legends is a competitive MOBA (Multiplayer Online Battle Arena) game where 5 players on each team try and cooperatively destroy the enemy's base to win. In this game, there are five roles corresponding to different lanes on the map called summoner's rift: top, jungle, mid, bottom, and support(pic). A total of more than 160 champions can be chosen for each player depending on the lane they are playing. 

For today, we are discussing one of the champions in the bot lane: Ezreal. Because of his versatility, it is very challenging for enemies to kill him, but the tradeoff for his versatility is his damage output and his strength in the early and late game. It is very hard for Ezreal to gain priority and dominate the opponent early in the game while it is also very difficult for him to close the game out when the game goes beyond the 35 minute mark. He often can deal a lot of poke damage before a skirmish begins but lack the necessary skills to deal the fatal blow.

In the competitive scene, Ezreal has always been a controversial champion to pick: In fact, in the recent season 13 Worlds tournament where players from all over the world gather to play for the highest honor, Ezreal was only picked for 5 times out of more than 100 games, with a 0 percent winrate overall. Many esports casters from over the world do not trust the champion in the professionsal scene as the lack of priority that Ezreal can bring in the game often is the reason of teams' losses.

Is he being overlooked or is he actually incompetent of winning at this level of competition? In this report, we will be taking analyzing Ezreal's performance in 2023's League of Legend's esport scene. We will be examing "2023 Lol esport match data" dataest from Oracles Elixir which has 129348 rows and 123 columns. To fulfill or needs, we only need to extract neccessary columns: ```["gameid",'result','game','participantid','side', 'position',
       'playername', 'playerid', 'teamname', 'teamid', 'champion', 'ban1',
       'ban2', 'ban3', 'ban4', 'ban5',"kda", "damageshare", "cspm"]```
    
## Cleaning and EDA
#### Data Cleaning
To begin


## Assessment of Missingness



## Hypothesis Testing
Among the selective columns in the dataframe, the only strong indicator of Ezreal's attribution is game that is not missing is its win rate.\
Null hypothesis: Ezreal's win rate is similar to the average win rate \
Alternative hypothesis: Ezreal's win rate is way lower than the average win rate



