# LoL_Ezreal_Eff2023
An analysis of champion Ezreal's effectiveness in the realm of 2023 League of Legends Esport. (Project for DSC80 at University of Califrnia San Diego))

## Introduction
League of Legends is a competitive MOBA (Multiplayer Online Battle Arena) game where 5 players on each team try and cooperatively destroy the enemy's base to win. In this game, there are five roles corresponding to different lanes on the map called summoner's rift: top, jungle, mid, bottom, and support(pic). A total of more than 160 champions can be chosen for each player depending on the lane they are playing. 

For today, we are discussing one of the champions in the bot lane: Ezreal. Because of his versatility, it is very challenging for enemies to kill him, but the tradeoff for his versatility is his damage output and his strength in the early and late game. It is very hard for Ezreal to gain priority and dominate the opponent early in the game while it is also very difficult for him to close the game out when the game goes beyond the 35 minute mark. He often can deal a lot of poke damage before a skirmish begins but lack the necessary skills to deal the fatal blow.

In the competitive scene, Ezreal has always been a controversial champion to pick: In fact, in the recent season 13 Worlds tournament where players from all over the world gather to play for the highest honor, Ezreal was only picked for 5 times out of more than 100 games, with a 0 percent winrate overall. Many esports casters from over the world do not trust the champion in the professionsal scene as the lack of priority that Ezreal can bring in the game often is the reason of teams' losses.

Is he being overlooked or is he actually incompetent of winning at this level of competition? In this report, we will be taking analyzing Ezreal's performance in 2023's League of Legend's esport scene. We will be examing "2023 Lol esport match data" dataest from Oracles Elixir which has 129348 rows and 123 columns. 


<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gameid</th>
      <th>datacompleteness</th>
      <th>url</th>
      <th>league</th>
      <th>year</th>
      <th>split</th>
      <th>playoffs</th>
      <th>date</th>
      <th>game</th>
      <th>patch</th>
      <th>...</th>
      <th>opp_csat15</th>
      <th>golddiffat15</th>
      <th>xpdiffat15</th>
      <th>csdiffat15</th>
      <th>killsat15</th>
      <th>assistsat15</th>
      <th>deathsat15</th>
      <th>opp_killsat15</th>
      <th>opp_assistsat15</th>
      <th>opp_deathsat15</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>complete</td>
      <td>NaN</td>
      <td>LFL2</td>
      <td>2023</td>
      <td>Spring</td>
      <td>0</td>
      <td>2023-01-10 17:07:16</td>
      <td>1</td>
      <td>13.01</td>
      <td>...</td>
      <td>131.0</td>
      <td>322.0</td>
      <td>263.0</td>
      <td>12.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>complete</td>
      <td>NaN</td>
      <td>LFL2</td>
      <td>2023</td>
      <td>Spring</td>
      <td>0</td>
      <td>2023-01-10 17:07:16</td>
      <td>1</td>
      <td>13.01</td>
      <td>...</td>
      <td>117.0</td>
      <td>-357.0</td>
      <td>-1323.0</td>
      <td>-43.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>complete</td>
      <td>NaN</td>
      <td>LFL2</td>
      <td>2023</td>
      <td>Spring</td>
      <td>0</td>
      <td>2023-01-10 17:07:16</td>
      <td>1</td>
      <td>13.01</td>
      <td>...</td>
      <td>162.0</td>
      <td>-479.0</td>
      <td>-324.0</td>
      <td>-26.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>complete</td>
      <td>NaN</td>
      <td>LFL2</td>
      <td>2023</td>
      <td>Spring</td>
      <td>0</td>
      <td>2023-01-10 17:07:16</td>
      <td>1</td>
      <td>13.01</td>
      <td>...</td>
      <td>122.0</td>
      <td>200.0</td>
      <td>292.0</td>
      <td>20.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>complete</td>
      <td>NaN</td>
      <td>LFL2</td>
      <td>2023</td>
      <td>Spring</td>
      <td>0</td>
      <td>2023-01-10 17:07:16</td>
      <td>1</td>
      <td>13.01</td>
      <td>...</td>
      <td>3.0</td>
      <td>-216.0</td>
      <td>-579.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
  </tbody>
</table>
<p>129348 rows × 123 columns</p>
</div>


To fulfill or needs, we only need to extract neccessary columns: ```["gameid",'result','game','participantid','side', 'position',
       'playername', 'playerid', 'teamname', 'teamid', 'champion', 'ban1',
       'ban2', 'ban3', 'ban4', 'ban5', 'kill', 'assit', 'death', 'damageshare', 'cspm']``` The first fiew gives overall information regrading the team, player, game, and champions selected. While as latter few gives detail statistics regarding the champion's performance. 
#### kill, death & assits       
'kill', 'death', 'assits' all together formed one of the most important metric in the game, the kda, which reflects the player's ability of eliminating the enemy without letting the enemy to do the same to you. 
#### damageshare
'damageshare' shows the player's proportion of overall damage, indicating the player's, and the champion's, potency to deal damage to the enemy. 
#### cspm    
'cspm' is also know as creep score per minute. For each wave, there are about 6-7 minions, meaning that on average in professional play, players are able to have somewhere around 10 cs per minute. This indicates how suppresive of a champion you are in lane and how fast you are at farming gold.
#### result
For a competitive esport game, nothing is more important than winning. Even if you have the highest kills, damage, creep score, if you can not lead your game to victory, it will mean nothing. Thus, 'result' columns records a binomial distribution where 0 when the team loses and 1 when the team wins. Though simple, this is the most important indicator for every single player and champion.

## Cleaning and EDA
#### Data Cleaning
To begin with, I have eliminated all the irrelavant columns and gather the columns kills, deaths, and assits and formulate them into a new column, kda, which records the quanty of kills and assits per life. As a result, the dataframe is crop to keeping the following column:```["gameid",'result','game','participantid','side', 'position',
       'playername', 'playerid', 'teamname', 'teamid', 'champion', 'ban1',
       'ban2', 'ban3', 'ban4', 'ban5',"kda", "damageshare", "cspm"]```


<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gameid</th>
      <th>result</th>
      <th>game</th>
      <th>participantid</th>
      <th>side</th>
      <th>position</th>
      <th>playername</th>
      <th>playerid</th>
      <th>teamname</th>
      <th>teamid</th>
      <th>champion</th>
      <th>ban1</th>
      <th>ban2</th>
      <th>ban3</th>
      <th>ban4</th>
      <th>ban5</th>
      <th>kda</th>
      <th>damageshare</th>
      <th>cspm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>Blue</td>
      <td>top</td>
      <td>Wylenz</td>
      <td>oe:player:60aff1184bec1d2b2efdae84f5b6e3e</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Jax</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>10.000000</td>
      <td>0.150027</td>
      <td>9.1654</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>Blue</td>
      <td>jng</td>
      <td>Julbu</td>
      <td>oe:player:fd78e127e45463dcfc2ea3836af0335</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Poppy</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>3.000000</td>
      <td>0.065324</td>
      <td>3.6524</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>3</td>
      <td>Blue</td>
      <td>mid</td>
      <td>Sintax</td>
      <td>oe:player:baf7147fedeec5de54ca1f240952a3f</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Taliyah</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>6.500000</td>
      <td>0.283899</td>
      <td>7.7412</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Axelent</td>
      <td>oe:player:8204ca38dc1c42012b5d53131271eb1</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Ezreal</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>12.000000</td>
      <td>0.441215</td>
      <td>8.4992</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>Blue</td>
      <td>sup</td>
      <td>Wixo</td>
      <td>oe:player:bb97cd2e43cb0855f6485e6f9e93ea2</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Karma</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>5.000000</td>
      <td>0.059536</td>
      <td>0.4824</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
  </tbody>
</table>
<p>129348 rows × 19 columns</p>
</div>

As it is about the champion Ezreal, we have also created a subset dataframe that only contains data of the champion.

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gameid</th>
      <th>result</th>
      <th>game</th>
      <th>participantid</th>
      <th>side</th>
      <th>position</th>
      <th>playername</th>
      <th>playerid</th>
      <th>teamname</th>
      <th>teamid</th>
      <th>champion</th>
      <th>ban1</th>
      <th>ban2</th>
      <th>ban3</th>
      <th>ban4</th>
      <th>ban5</th>
      <th>kda</th>
      <th>damageshare</th>
      <th>cspm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>Blue</td>
      <td>top</td>
      <td>Wylenz</td>
      <td>oe:player:60aff1184bec1d2b2efdae84f5b6e3e</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Jax</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>10.000000</td>
      <td>0.150027</td>
      <td>9.1654</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>Blue</td>
      <td>jng</td>
      <td>Julbu</td>
      <td>oe:player:fd78e127e45463dcfc2ea3836af0335</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Poppy</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>3.000000</td>
      <td>0.065324</td>
      <td>3.6524</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>3</td>
      <td>Blue</td>
      <td>mid</td>
      <td>Sintax</td>
      <td>oe:player:baf7147fedeec5de54ca1f240952a3f</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Taliyah</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>6.500000</td>
      <td>0.283899</td>
      <td>7.7412</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Axelent</td>
      <td>oe:player:8204ca38dc1c42012b5d53131271eb1</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Ezreal</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>12.000000</td>
      <td>0.441215</td>
      <td>8.4992</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>5</td>
      <td>Blue</td>
      <td>sup</td>
      <td>Wixo</td>
      <td>oe:player:bb97cd2e43cb0855f6485e6f9e93ea2</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>Karma</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>5.000000</td>
      <td>0.059536</td>
      <td>0.4824</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
  </tbody>
</table>
<p>10980 rows × 19 columns</p>
</div>


#### Univariate Analysis
Let's see the stats of kdaa, damage share, and cspm:
[[kda](kda_distribution.html)]




#### Bivariate Analysis


#### Interesting Aggregates


## Assessment of Missingness



## Hypothesis Testing
Among the selective columns in the dataframe, the only strong indicator of Ezreal's attribution is game that is not missing is its win rate.\
Null hypothesis: Ezreal's win rate is similar to the average win rate \
Alternative hypothesis: Ezreal's win rate is way lower than the average win rate



