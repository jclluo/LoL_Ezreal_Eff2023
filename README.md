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
Let's see the stats of kda, damage share, and cspm: 
<iframe src="kda_distribution.html" width=800 height=600 frameBorder=0></iframe>
For kda, the median sits at about 1.3 and 50% of kda scattered from 0 to 7,5, This means that usually, Ezrael can kill at least one enemy without getting slayed. Sometimes it can even reach about 7 enemies.
<iframe src="damageshare_distribution.html" width=800 height=600 frameBorder=0></iframe>
For damage share, the median sits at around 0.19 and 50% scattered within 0.26 to 0.12. For an ADC, Ezreal usually can not cover one fifth of the damage for the team, making it a bit lower than expected.

<iframe src="cspm_distribution.html" width=800 height=600 frameBorder=0></iframe>
Last for cspm. From the boxplot, there are a lot of outliers. This suggest a very high inconsistency in creep score. Thus, further analysis with other BOT heroes are needed.



#### Bivariate Analysis
Let's look the differnece of the three most important statistical metrics, kda, cspm, and damageshare between Ezreal and all other ADCs
<iframe src="bivariate_kda_box_plot_ezreal_vs_others.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="bivariate_damageshare_box_plot_ezreal_vs_others.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="bivariate_cspm_box_plot_ezreal_vs_others.html" width=800 height=600 frameBorder=0></iframe>
As shown from the plot, the kda between Ezreal and other BOT champtions are minimal wiht simialr center points and sitributions. But for damage share, Ezreal depict likely of of a higher damage share than other champions. And for CSPM, though the overal distribution seems similar, other BOT champions depict a lot more outliers, suggesting a differetn playstyle that does not require creep score.

#### Interesting Aggregates
As mentioned above, winning is the most important vector for any single champion. So first, let's see the overall win rate for Ezreal:
```python
ezreal_games = game_performance_metrics[game_performance_metrics['champion'] == 'Ezreal']
win_rate_ezreal = (ezreal_games[ezreal_games['result'] == 1].shape[0] / ezreal_games.shape[0]) * 100
print(f"Overall Win Rate for Ezreal: {win_rate_ezreal:.2f}%")
```

    Overall Win Rate for Ezreal: 45.79%

For a sample size that is encompasing over 1000 games, the observed statistics seems extremely low. Thus, this is a important statistics to consider later.

In addition, I have also added a new column called "performancescore" which takes the average of standardized statistics from kda, damageshare, and cspm. Thus this is a good standardized indicator of whether the champion's competency. And due to its standardized property. The mean is located at 0 and 68% if data falls within -1 and 1. Below is the pivot table between performancescore and result.
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th>result</th>
      <th>performancescore</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>-1.05122</td>
    </tr>
    <tr>
      <td>1</td>
      <td>0.18380</td>
    </tr>
  </tbody>
</table>

As shown above, the average performancescore when Ezreal loses is extremely below the mean while the average performancescore when Ezreal wins is higher than the mean. This dramatic difference suggest this can also be a good indicator of Ezreal's overall competence along side win rate.


## Assessment of Missingness
#### Missing by Design
In this dataframe, there are many columns that missing by design. These are rows when there are no entry of players and thus all the related columns are also missing. In total, the columns that are missing by design are ['champion', 'playername', 'damageshare', 'cspm', 'performancescore']. Below is a code snippet showning the following columns only has missingness at two relative spots in terms of per game, which are intensionally left in blank for substitution, suggesting missing by design:
```python
testing = ['playername',
 'playerid',
 'teamid',
 'ban1',
 'ban2',
 'ban3',
 'ban4',
 'ban5',
 'damageshare',
 'cspm',
 'performancescore']

def relative_loc(col):
    df = game_performance_metrics[['gameid', col]]
    missing_value_frequency = {}
    for game_id in df['gameid'].unique():
        game_rows = df[df['gameid'] == game_id]
        total_rows = len(game_rows)

        for index, row in game_rows.iterrows():
            if pd.isnull(row[col]):
                relative_location = game_rows.index.get_loc(index) / total_rows
                
                relative_location = round(relative_location, 2)
                
                if relative_location not in missing_value_frequency:
                    missing_value_frequency[relative_location] = 0
                missing_value_frequency[relative_location] += 1
    
    print(f"the reltiave location for {col} is shown as {missing_value_frequency}")

for i in testing:
    relative_loc(i)

print("thus the remaining columns that need to be analyze are [playerid, teamid, ban1, ban2, ban3, ban4, ban5]")
```

    the reltiave location for playername is shown as {0.83: 10779, 0.92: 10779, 0.17: 2, 0.33: 1, 0.58: 3, 0.0: 1, 0.08: 1, 0.67: 2, 0.25: 3}
    the reltiave location for playerid is shown as {0.83: 10779, 0.92: 10779, 0.25: 91, 0.67: 101, 0.17: 61, 0.33: 88, 0.75: 98, 0.08: 89, 0.42: 113, 0.0: 102, 0.58: 65, 0.5: 100}
    the reltiave location for teamid is shown as {0.0: 94, 0.08: 94, 0.17: 94, 0.25: 94, 0.33: 94, 0.83: 94, 0.42: 125, 0.5: 125, 0.58: 125, 0.67: 125, 0.75: 125, 0.92: 125}
    the reltiave location for ban1 is shown as {0.0: 882, 0.08: 882, 0.17: 882, 0.25: 882, 0.33: 882, 0.83: 882, 0.42: 878, 0.5: 878, 0.58: 878, 0.67: 878, 0.75: 878, 0.92: 878}
    the reltiave location for ban2 is shown as {0.0: 874, 0.08: 874, 0.17: 874, 0.25: 874, 0.33: 874, 0.83: 874, 0.42: 869, 0.5: 869, 0.58: 869, 0.67: 869, 0.75: 869, 0.92: 869}
    the reltiave location for ban3 is shown as {0.42: 895, 0.5: 895, 0.58: 895, 0.67: 895, 0.75: 895, 0.92: 895, 0.0: 900, 0.08: 900, 0.17: 900, 0.25: 900, 0.33: 900, 0.83: 900}
    the reltiave location for ban4 is shown as {0.0: 889, 0.08: 889, 0.17: 889, 0.25: 889, 0.33: 889, 0.83: 889, 0.42: 885, 0.5: 885, 0.58: 885, 0.67: 885, 0.75: 885, 0.92: 885}
    the reltiave location for ban5 is shown as {0.42: 914, 0.5: 914, 0.58: 914, 0.67: 914, 0.75: 914, 0.92: 914, 0.0: 912, 0.08: 912, 0.17: 912, 0.25: 912, 0.33: 912, 0.83: 912}
    the reltiave location for damageshare is shown as {0.83: 10779, 0.92: 10779}
    the reltiave location for cspm is shown as {0.83: 1624, 0.92: 1624}
    the reltiave location for performancescore is shown as {0.83: 10779, 0.92: 10779}
    thus the remaining columns that need to be analyze are [playerid, teamid, ban1, ban2, ban3, ban4, ban5]

#### Not Missing By Random
The remainng columsn are [playerid, teamid, ban1, ban2, ban3, ban4, ban5]. Let's see the two filtered dataframe when playerid has only missing values and when teamid has only missing values:
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
      <th>performancescore</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>10</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>1</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Klanik Esport</td>
      <td>oe:team:0ade5e44c23039bca133eee58ec1b83</td>
      <td>NaN</td>
      <td>Sylas</td>
      <td>Caitlyn</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>7.285714</td>
      <td>NaN</td>
      <td>29.5406</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>0</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>MS Company</td>
      <td>oe:team:14ad76b8d9e647d4b29c3d26ecd29c9</td>
      <td>NaN</td>
      <td>Galio</td>
      <td>Lucian</td>
      <td>Fiora</td>
      <td>Viktor</td>
      <td>Azir</td>
      <td>1.923077</td>
      <td>NaN</td>
      <td>28.1623</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>22</th>
      <td>ESPORTSTMNT06_2754023</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>beGenius ESC</td>
      <td>oe:team:607baf04091e515e195644cb08ec21c</td>
      <td>NaN</td>
      <td>Fiora</td>
      <td>Kindred</td>
      <td>Sejuani</td>
      <td>Nautilus</td>
      <td>Leona</td>
      <td>4.000000</td>
      <td>NaN</td>
      <td>32.9064</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>23</th>
      <td>ESPORTSTMNT06_2754023</td>
      <td>1</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>ViV Esport</td>
      <td>oe:team:2d9e95ecefb34c32ff1a997ebe372f9</td>
      <td>NaN</td>
      <td>Heimerdinger</td>
      <td>Wukong</td>
      <td>Akali</td>
      <td>Syndra</td>
      <td>Sylas</td>
      <td>2.200000</td>
      <td>NaN</td>
      <td>33.5714</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>34</th>
      <td>ESPORTSTMNT06_2755035</td>
      <td>1</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Team du Sud</td>
      <td>oe:team:1dc6411295a36bd29c29b1096ba859d</td>
      <td>NaN</td>
      <td>Zac</td>
      <td>Sylas</td>
      <td>Sejuani</td>
      <td>Jarvan IV</td>
      <td>Ornn</td>
      <td>9.714286</td>
      <td>NaN</td>
      <td>33.5455</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>35</th>
      <td>ESPORTSTMNT06_2755035</td>
      <td>0</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Akroma</td>
      <td>oe:team:e05fc2a9f99e906ea564a672d75f839</td>
      <td>NaN</td>
      <td>Zeri</td>
      <td>Nami</td>
      <td>Caitlyn</td>
      <td>Fiora</td>
      <td>Heimerdinger</td>
      <td>0.850000</td>
      <td>NaN</td>
      <td>29.4242</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>46</th>
      <td>ESPORTSTMNT06_2754033</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Atletec</td>
      <td>oe:team:e0ec1fed6e0949a0aef5f506ccb76ce</td>
      <td>NaN</td>
      <td>Zilean</td>
      <td>Rek'Sai</td>
      <td>Riven</td>
      <td>Senna</td>
      <td>Kalista</td>
      <td>1.428571</td>
      <td>NaN</td>
      <td>29.6343</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>47</th>
      <td>ESPORTSTMNT06_2754033</td>
      <td>1</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Joblife</td>
      <td>oe:team:7380b73561abdd86c2391e9481acd4b</td>
      <td>NaN</td>
      <td>Nami</td>
      <td>Syndra</td>
      <td>Yuumi</td>
      <td>Renata Glasc</td>
      <td>Caitlyn</td>
      <td>7.142857</td>
      <td>NaN</td>
      <td>32.0827</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>

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
      <th>performancescore</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>37356</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>Blue</td>
      <td>top</td>
      <td>Abaddon</td>
      <td>oe:player:a9e2d00e60f059e223d82301a50182c</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Sion</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>0.750000</td>
      <td>0.239479</td>
      <td>6.5698</td>
      <td>-0.791752</td>
    </tr>
    <tr>
      <th>37357</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>2</td>
      <td>Blue</td>
      <td>jng</td>
      <td>Annataqui</td>
      <td>oe:player:fac747e9c68a89da88dad294bf5ed51</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Wukong</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>1.000000</td>
      <td>0.176369</td>
      <td>4.8939</td>
      <td>-1.575292</td>
    </tr>
    <tr>
      <th>37358</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>3</td>
      <td>Blue</td>
      <td>mid</td>
      <td>Overload</td>
      <td>oe:player:b6fe055bfad88e328abe3fbbf21a33c</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Gragas</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>1.500000</td>
      <td>0.239830</td>
      <td>7.8771</td>
      <td>-0.512334</td>
    </tr>
    <tr>
      <th>37359</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Snoopy</td>
      <td>oe:player:c59f2a6c6e7227a313b6d215f5fb153</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Ezreal</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>1.250000</td>
      <td>0.284399</td>
      <td>8.7151</td>
      <td>-0.009010</td>
    </tr>
    <tr>
      <th>37360</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>5</td>
      <td>Blue</td>
      <td>sup</td>
      <td>khaN</td>
      <td>oe:player:2eb2a12f1608b0150cc7050b061bc83</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Karma</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>2.000000</td>
      <td>0.059923</td>
      <td>0.3687</td>
      <td>-3.073881</td>
    </tr>
    <tr>
      <th>37366</th>
      <td>ESPORTSTMNT03_3125447</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Sylas</td>
      <td>Gwen</td>
      <td>Jax</td>
      <td>1.166667</td>
      <td>NaN</td>
      <td>28.4246</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>37433</th>
      <td>ESPORTSTMNT03_3123485</td>
      <td>0</td>
      <td>2</td>
      <td>6</td>
      <td>Red</td>
      <td>top</td>
      <td>Abaddon</td>
      <td>oe:player:a9e2d00e60f059e223d82301a50182c</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Renekton</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Caitlyn</td>
      <td>Gwen</td>
      <td>Ahri</td>
      <td>1.333333</td>
      <td>0.178047</td>
      <td>7.4474</td>
      <td>-1.226692</td>
    </tr>
    <tr>
      <th>37434</th>
      <td>ESPORTSTMNT03_3123485</td>
      <td>0</td>
      <td>2</td>
      <td>7</td>
      <td>Red</td>
      <td>jng</td>
      <td>Annataqui</td>
      <td>oe:player:fac747e9c68a89da88dad294bf5ed51</td>
      <td>unknown team</td>
      <td>NaN</td>
      <td>Wukong</td>
      <td>Fiora</td>
      <td>Olaf</td>
      <td>Caitlyn</td>
      <td>Gwen</td>
      <td>Ahri</td>
      <td>2.000000</td>
      <td>0.152891</td>
      <td>5.2252</td>
      <td>-1.599513</td>
    </tr>
  </tbody>
</table>
</div>

As seem above, playerid is highly related to playername, suggesting it to be at least missing at Random. And for teamid, there is no apparent correlation and thus further analysis is needed. There is unlikely to be not missing at random columns. Bans are like chess games: In this time period before the start of the games, the coaches of each side decide what champion to ban depending on the previous champion that the opposing coach chose before (For instance, the coach at the red side will ban after the coach bans at the blue side). This implies that bans are dependent on each other: each ban is the best response to the previous ban except the first one, for which coaches will ban the champion that is too powerful that they have to prioritize first.


#### Missing at Random & Missing Completely at Random
Through a series of calculation, I have analyze the missingness of all other columns. Code below checks the correlation of each missing column in relationship with all other columns. Is there are columns with extremely low p_value 0.05, the correctlated columns will be returned in a dicionary where the key is each column. And if the column is uncorrelated with any other columns, its value will be 'MCAR'
```python
from scipy.stats import ks_2samp 
def test_mcar_vs_mar(df, col_x, columns_to_check):
    results = {}
    for col in columns_to_check:
        if col != col_x:
            data_missing = df[df[col_x].isnull()]
            data_not_missing = df[df[col_x].notnull()]

            if len(data_missing[col].dropna()) > 0 and len(data_not_missing[col].dropna()) > 0:
                stat, p_value = ks_2samp(data_missing[col].dropna(), data_not_missing[col].dropna())
                results[col] = p_value
    return results

def assess_all_columns(df, columns_to_test):
    all_results = {}
    for col_x in columns_to_test:
        results = test_mcar_vs_mar(df, col_x, columns_to_test)
        significant_columns = [col for col, p_val in results.items() if p_val < 0.05]

        if significant_columns:
            all_results[col_x] = significant_columns
        else:
            all_results[col_x] = "MCAR"

    return all_results

columns_to_test = ['playerid', 'teamid', 'ban1', 'ban2', 'ban3', 'ban4', 'ban5']
missingness_assessment = assess_all_columns(game_performance_metrics, columns_to_test)
missingnessresult = missingness_assessment
missingnessresult
```




    {'playerid': 'MCAR',
     'teamid': ['playerid', 'ban1', 'ban2', 'ban3', 'ban4', 'ban5'],
     'ban1': ['playerid', 'teamid', 'ban2', 'ban5'],
     'ban2': ['playerid', 'teamid', 'ban1', 'ban3', 'ban4', 'ban5'],
     'ban3': ['playerid', 'teamid', 'ban1', 'ban2', 'ban4', 'ban5'],
     'ban4': ['playerid', 'teamid', 'ban1', 'ban2', 'ban3'],
     'ban5': ['playerid', 'teamid', 'ban1', 'ban2', 'ban3', 'ban4']}



Here is a more straighforward view each columns's missingness:


```python
for col, result in missingnessresult.items():
    print(col, result)
```

    playerid MCAR
    teamid ['playerid', 'ban1', 'ban2', 'ban3', 'ban4', 'ban5']
    ban1 ['playerid', 'teamid', 'ban2', 'ban5']
    ban2 ['playerid', 'teamid', 'ban1', 'ban3', 'ban4', 'ban5']
    ban3 ['playerid', 'teamid', 'ban1', 'ban2', 'ban4', 'ban5']
    ban4 ['playerid', 'teamid', 'ban1', 'ban2', 'ban3']
    ban5 ['playerid', 'teamid', 'ban1', 'ban2', 'ban3', 'ban4']



```python
classification_dict = {'MD' : ['champion', 'playername', 'damageshare', 'cspm','performancescore'], 'NMAR':[], 'MAR': [], 'MCAR': []}
for col, result in missingnessresult.items():
    if result == "MCAR":
        classification_dict['MCAR'].append(col)
    else:
        classification_dict['MAR'].extend(result)
classification_dict['MAR'] = list(set(classification_dict['MAR']))
print(classification_dict)

flattened_data = [(key, val) for key, values in classification_dict.items() for val in values]
classification_df = pd.DataFrame(flattened_data, columns=['Classification', 'Column'])
classification_df = classification_df.drop(index=7)
classification_df.set_index("Column")

```

    {'MD': ['champion', 'playername', 'damageshare', 'cspm', 'performancescore'], 'NMAR': [], 'MAR': ['ban2', 'teamid', 'playerid', 'ban1', 'ban3', 'ban5', 'ban4'], 'MCAR': ['playerid']}





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Classification</th>
    </tr>
    <tr>
      <th>Column</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>champion</th>
      <td>MD</td>
    </tr>
    <tr>
      <th>playername</th>
      <td>MD</td>
    </tr>
    <tr>
      <th>damageshare</th>
      <td>MD</td>
    </tr>
    <tr>
      <th>cspm</th>
      <td>MD</td>
    </tr>
    <tr>
      <th>performancescore</th>
      <td>MD</td>
    </tr>
    <tr>
      <th>ban2</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>teamid</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>ban1</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>ban3</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>ban5</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>ban4</th>
      <td>MAR</td>
    </tr>
    <tr>
      <th>playerid</th>
      <td>MCAR</td>
    </tr>
  </tbody>
</table>
</div>

#### One MAR Example: ban2
Let's see the distribution of ban2 when ban1 is missing and when it is not

<iframe src="pie1.html" width=800 height=600 frameBorder=0></iframe>
<iframe src="pie2.html" width=800 height=600 frameBorder=0></iframe>

As shown above. When ban1 is  missing, about 98.7% of ban2 is missing. But when ban1 is not missing, around 0.0303% of ban2 is missing. This dramatic difference the strong correlation between ban1 and ban2, showing how the missingness of ban2 is very dependent on ban1, suggesting its missingness as missing at random.

## Hypothesis Testing
Due to missiness in performancescore. It unfortuantly cannot be used to conduct the following hypothesis testing. As a result, I will be using win rate as my test statistic.\

Among the selective columns in the dataframe, the only strong indicator of Ezreal's attribution is game that is not missing is its win rate.\
Null hypothesis: Ezreal's win rate is similar to the average win rate \
Alternative hypothesis: Ezreal's win rate is way lower than the average win rate\
Below is a code snippet showing the result of running the hypothesis test through multiple iterations:
```python
Observed = win_rate_ezreal * 0.01 #calcualted in the previous section
average_win = game_performance_metrics['result'].mean()  #proving the averaging win rate is 0.5
totalezgames = ezrealdf.groupby("gameid").count().shape[0]
iteration = [1000, 5000, 10000, 20000, 50000]


def hypothesis_testin(n):
    arr = []
    for _ in range(n):
        sample = np.random.multinomial(totalezgames, [average_win, 1-average_win])
        teststat = sample[0]/totalezgames
        arr.append(teststat)
    p_val = sum(np.array(arr) < Observed) / n
    result = f"Over {n} iterations, the p-value is {p_val}"
    df = pd.DataFrame({'Win Rate': np.array(arr)})
    fig = px.histogram(df, x='Win Rate', title=f'Win Rate Distribution for {n} iterations', 
                   color_discrete_sequence=['#636EFA'])

    fig.add_shape(type='line',
              line=dict( color='#EF553B'),
              x0=Observed, x1=Observed, y0=0, y1=1, xref='x', yref='paper')
    
    
    fig.show()


    return result

results = [hypothesis_testin(n) for n in iteration]
for res in results:
    print(res)

```
    Over 1000 iterations, the p-value is 0.005
    Over 5000 iterations, the p-value is 0.0048
    Over 10000 iterations, the p-value is 0.0066
    Over 20000 iterations, the p-value is 0.0053
    Over 50000 iterations, the p-value is 0.00532

Here is the distribution over 50000 iteation. The red line indicate where the observed statistics is.
<iframe src="win_rate_dist_50000.html" width=800 height=600 frameBorder=0></iframe>




As shown above, no matter how many tests conducted, the p_value is still smaller than the alpha level of 0.05. Thus, the win rate is statistically significant and we can reject the null hypothesis. This shows that the win rate for Ezreal is significantly lower than the average win rate. 

In conclusion, the result of the hypothesis test provides strong evidence of Ezreal's incompetence in winning in pro scene. However, this can not be generalized to a biger population. The play style betweem the most competivie esport and regular, lower intensity games are completely different. Thus, Ezreal players can still enjoy the game playing this signature hero of the franchise.



