# LoL_Ezreal_Eff2023
An analysis of champion Ezreal's effectiveness in the realm of 2023 League of Legends Esport. (Project for DSC80 at University of Califrnia San Diego))

```python
#load
league = pd.read_csv('2023_LoL_esports_match_data_from_OraclesElixir.csv')
league

```

    /var/folders/g0/6rfqkkms2jl55vm04r5k709r0000gn/T/ipykernel_726/2573673647.py:2: DtypeWarning:
    
    Columns (2) have mixed types. Specify dtype option on import or set low_memory=False.
    





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
    <tr>
      <th>129343</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>complete</td>
      <td>NaN</td>
      <td>NEXO</td>
      <td>2024</td>
      <td>Split 1</td>
      <td>0</td>
      <td>2023-11-13 20:32:25</td>
      <td>1</td>
      <td>13.21</td>
      <td>...</td>
      <td>152.0</td>
      <td>677.0</td>
      <td>736.0</td>
      <td>-2.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>129344</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>complete</td>
      <td>NaN</td>
      <td>NEXO</td>
      <td>2024</td>
      <td>Split 1</td>
      <td>0</td>
      <td>2023-11-13 20:32:25</td>
      <td>1</td>
      <td>13.21</td>
      <td>...</td>
      <td>143.0</td>
      <td>-956.0</td>
      <td>-16.0</td>
      <td>-11.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>129345</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>complete</td>
      <td>NaN</td>
      <td>NEXO</td>
      <td>2024</td>
      <td>Split 1</td>
      <td>0</td>
      <td>2023-11-13 20:32:25</td>
      <td>1</td>
      <td>13.21</td>
      <td>...</td>
      <td>11.0</td>
      <td>107.0</td>
      <td>497.0</td>
      <td>17.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>129346</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>complete</td>
      <td>NaN</td>
      <td>NEXO</td>
      <td>2024</td>
      <td>Split 1</td>
      <td>0</td>
      <td>2023-11-13 20:32:25</td>
      <td>1</td>
      <td>13.21</td>
      <td>...</td>
      <td>560.0</td>
      <td>-1386.0</td>
      <td>-2270.0</td>
      <td>-41.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>129347</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>complete</td>
      <td>NaN</td>
      <td>NEXO</td>
      <td>2024</td>
      <td>Split 1</td>
      <td>0</td>
      <td>2023-11-13 20:32:25</td>
      <td>1</td>
      <td>13.21</td>
      <td>...</td>
      <td>519.0</td>
      <td>1386.0</td>
      <td>2270.0</td>
      <td>41.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
<p>129348 rows × 123 columns</p>
</div>



First, let's look at what interesting columns are there


```python
print(league.columns.tolist())
```

    ['gameid', 'datacompleteness', 'url', 'league', 'year', 'split', 'playoffs', 'date', 'game', 'patch', 'participantid', 'side', 'position', 'playername', 'playerid', 'teamname', 'teamid', 'champion', 'ban1', 'ban2', 'ban3', 'ban4', 'ban5', 'gamelength', 'result', 'kills', 'deaths', 'assists', 'teamkills', 'teamdeaths', 'doublekills', 'triplekills', 'quadrakills', 'pentakills', 'firstblood', 'firstbloodkill', 'firstbloodassist', 'firstbloodvictim', 'team kpm', 'ckpm', 'firstdragon', 'dragons', 'opp_dragons', 'elementaldrakes', 'opp_elementaldrakes', 'infernals', 'mountains', 'clouds', 'oceans', 'chemtechs', 'hextechs', 'dragons (type unknown)', 'elders', 'opp_elders', 'firstherald', 'heralds', 'opp_heralds', 'firstbaron', 'barons', 'opp_barons', 'firsttower', 'towers', 'opp_towers', 'firstmidtower', 'firsttothreetowers', 'turretplates', 'opp_turretplates', 'inhibitors', 'opp_inhibitors', 'damagetochampions', 'dpm', 'damageshare', 'damagetakenperminute', 'damagemitigatedperminute', 'wardsplaced', 'wpm', 'wardskilled', 'wcpm', 'controlwardsbought', 'visionscore', 'vspm', 'totalgold', 'earnedgold', 'earned gpm', 'earnedgoldshare', 'goldspent', 'gspd', 'total cs', 'minionkills', 'monsterkills', 'monsterkillsownjungle', 'monsterkillsenemyjungle', 'cspm', 'goldat10', 'xpat10', 'csat10', 'opp_goldat10', 'opp_xpat10', 'opp_csat10', 'golddiffat10', 'xpdiffat10', 'csdiffat10', 'killsat10', 'assistsat10', 'deathsat10', 'opp_killsat10', 'opp_assistsat10', 'opp_deathsat10', 'goldat15', 'xpat15', 'csat15', 'opp_goldat15', 'opp_xpat15', 'opp_csat15', 'golddiffat15', 'xpdiffat15', 'csdiffat15', 'killsat15', 'assistsat15', 'deathsat15', 'opp_killsat15', 'opp_assistsat15', 'opp_deathsat15']


In a game boasting a vast roster of hundreds of unique champions, my attention zeroes in on a singular, emblematic figure – Ezreal. This choice is rooted in Ezreal's status as one of the game's earliest creations, making him a representative icon of the game itself.


```python
league["champion"].unique()
```




    array(['Jax', 'Poppy', 'Taliyah', 'Ezreal', 'Karma', 'Sejuani', 'Viego',
           'Syndra', 'Zeri', 'Yuumi', nan, "K'Sante", 'Xin Zhao', 'Ryze',
           'Lucian', 'Nami', 'Gwen', 'Vi', 'Irelia', 'Draven', 'Amumu',
           'Aatrox', 'Wukong', 'Varus', 'Renata Glasc', 'Camille', 'Yone',
           'Jhin', 'Akali', 'Twitch', 'Lulu', 'Fiora', 'Zac', 'Veigar',
           'Taric', 'LeBlanc', 'Xayah', 'Alistar', 'Mordekaiser', 'Vex',
           'Leona', 'Ziggs', 'Renekton', 'Sylas', 'Swain', 'Lux', 'Gragas',
           'Jayce', 'Kennen', 'Graves', 'Nautilus', 'Ekko', 'Ahri',
           'Heimerdinger', 'Ornn', 'Dr. Mundo', "Kog'Maw", 'Olaf', 'Galio',
           "Kai'Sa", 'Blitzcrank', 'Jarvan IV', 'Kassadin', 'Zilean',
           'Caitlyn', 'Trundle', 'Sett', 'Lillia', 'Sivir', 'Gangplank',
           'Azir', 'Maokai', 'Kindred', 'Kalista', 'Aphelios', 'Soraka',
           'Lissandra', 'Gnar', 'Ashe', 'Bard', 'Viktor', 'Malphite', 'Zoe',
           'Skarner', 'Nidalee', 'Sona', 'Lee Sin', 'Darius', 'Orianna',
           'Rakan', 'Nocturne', 'Elise', "Bel'Veth", 'Seraphine', 'Jinx',
           'Rell', 'Nasus', 'Corki', 'Tristana', 'Braum', 'Pyke',
           'Twisted Fate', 'Udyr', 'Zed', 'Brand', 'Senna', 'Nilah',
           'Cassiopeia', 'Karthus', 'Sion', 'Zyra', 'Samira', 'Miss Fortune',
           'Thresh', 'Tryndamere', 'Xerath', 'Tahm Kench', 'Morgana', 'Yasuo',
           'Kled', 'Malzahar', 'Garen', 'Volibear', 'Urgot', 'Vladimir',
           'Ivern', 'Warwick', 'Hecarim', 'Akshan', 'Pantheon', 'Kayn',
           'Diana', 'Rumble', "Vel'Koz", 'Vayne', 'Singed', 'Shen', 'Riven',
           "Rek'Sai", 'Illaoi', 'Qiyana', 'Katarina', 'Janna', 'Shyvana',
           'Yorick', "Kha'Zix", 'Rengar', "Cho'Gath", 'Anivia', 'Fizz',
           'Kayle', 'Talon', 'Nunu & Willump', 'Master Yi', 'Annie', 'Neeko',
           'Fiddlesticks', 'Aurelion Sol', 'Quinn', 'Evelynn', 'Milio',
           'Shaco', 'Naafiri', 'Briar'], dtype=object)



### Cleaning and EDA
#### Data Cleaning
First, only keep the relative columns for our analysis and combine neccessary columns for simplicity. We can cross out unneccessary stats, combine certain columns to one. And match the data type in each column. For instance, I have kept the basic information regarding the game, result, the players and the champions selected. I have also added a column "kda" which is the combination of $\frac{\text{kill} + \text{assist}}{\text{death}}$. I addition, I chose two other most genrealizable satistics, damageshare and csp as performance metrics for the champions



```python
df = league.copy()
df['patch'] = df['patch'].astype(str)
binary_columns = ['firstdragon', 'firstbaron', 'firstbloodassist', 'firstbloodkill']
df[binary_columns] = df[binary_columns].astype(bool)
threshold = 0.5 * len(df)
df.dropna(thresh=threshold, axis=1, inplace=True)
df["kda"] = (df["kills"] + df["assists"])/df["deaths"].replace(0, 1)
game_performance_metrics = df[["gameid",'result','game','participantid','side', 'position',
       'playername', 'playerid', 'teamname', 'teamid', 'champion', 'ban1',
       'ban2', 'ban3', 'ban4', 'ban5',"kda", "damageshare", "cspm"]]
game_performance_metrics
```




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
    <tr>
      <th>129343</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>8</td>
      <td>Red</td>
      <td>mid</td>
      <td>Tirex</td>
      <td>oe:player:ae97b9649e39ad901b680f74c3f56b3</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Ahri</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>9.000000</td>
      <td>0.304237</td>
      <td>9.6440</td>
    </tr>
    <tr>
      <th>129344</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Alonshot</td>
      <td>oe:player:1723bb9b9fe68aea988f0c7ec75fbe1</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Aphelios</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>3.500000</td>
      <td>0.187860</td>
      <td>9.5183</td>
    </tr>
    <tr>
      <th>129345</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>10</td>
      <td>Red</td>
      <td>sup</td>
      <td>Boohis</td>
      <td>oe:player:38408cb0943e6f27ccd6272bdc1f09b</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Rakan</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>12.000000</td>
      <td>0.068353</td>
      <td>1.8220</td>
    </tr>
    <tr>
      <th>129346</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Erfolg Esports</td>
      <td>oe:team:4103ef051074f24e9566d1b7443c3fb</td>
      <td>NaN</td>
      <td>Maokai</td>
      <td>Poppy</td>
      <td>Taliyah</td>
      <td>Milio</td>
      <td>Cassiopeia</td>
      <td>0.857143</td>
      <td>NaN</td>
      <td>33.6440</td>
    </tr>
    <tr>
      <th>129347</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>NaN</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>10.250000</td>
      <td>NaN</td>
      <td>37.6335</td>
    </tr>
  </tbody>
</table>
<p>129348 rows × 19 columns</p>
</div>



Below are games in which Ezreal is selected as the ADC


```python
ezreal_gameids = game_performance_metrics[game_performance_metrics['champion'] == 'Ezreal']['gameid'].unique()
ezrealdf =game_performance_metrics[game_performance_metrics['gameid'].isin(ezreal_gameids)]
ezrealdf

```




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
    <tr>
      <th>129331</th>
      <td>ESPORTSTMNT02_3250546</td>
      <td>1</td>
      <td>1</td>
      <td>8</td>
      <td>Red</td>
      <td>mid</td>
      <td>Nestor</td>
      <td>oe:player:0d5006f22fac8518abf748573730738</td>
      <td>Kawaii Kiwis</td>
      <td>oe:team:8eb9a212591f919a353abfac0c0a52a</td>
      <td>Ahri</td>
      <td>Jayce</td>
      <td>Orianna</td>
      <td>Rell</td>
      <td>Nautilus</td>
      <td>Leona</td>
      <td>10.000000</td>
      <td>0.371440</td>
      <td>8.7555</td>
    </tr>
    <tr>
      <th>129332</th>
      <td>ESPORTSTMNT02_3250546</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Kurilius</td>
      <td>oe:player:ed6b2c95feaa4fd78f2ed6cd24dedf4</td>
      <td>Kawaii Kiwis</td>
      <td>oe:team:8eb9a212591f919a353abfac0c0a52a</td>
      <td>Ezreal</td>
      <td>Jayce</td>
      <td>Orianna</td>
      <td>Rell</td>
      <td>Nautilus</td>
      <td>Leona</td>
      <td>2.000000</td>
      <td>0.257506</td>
      <td>9.1520</td>
    </tr>
    <tr>
      <th>129333</th>
      <td>ESPORTSTMNT02_3250546</td>
      <td>1</td>
      <td>1</td>
      <td>10</td>
      <td>Red</td>
      <td>sup</td>
      <td>Whyx</td>
      <td>oe:player:df3f37d87473767caaa78b04dffc663</td>
      <td>Kawaii Kiwis</td>
      <td>oe:team:8eb9a212591f919a353abfac0c0a52a</td>
      <td>Rakan</td>
      <td>Jayce</td>
      <td>Orianna</td>
      <td>Rell</td>
      <td>Nautilus</td>
      <td>Leona</td>
      <td>5.000000</td>
      <td>0.052344</td>
      <td>1.5529</td>
    </tr>
    <tr>
      <th>129334</th>
      <td>ESPORTSTMNT02_3250546</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Dango SB</td>
      <td>oe:team:6da30cd905c797eaea30aeb18bc091a</td>
      <td>NaN</td>
      <td>Gnar</td>
      <td>Caitlyn</td>
      <td>Akali</td>
      <td>Syndra</td>
      <td>Neeko</td>
      <td>0.785714</td>
      <td>NaN</td>
      <td>30.5286</td>
    </tr>
    <tr>
      <th>129335</th>
      <td>ESPORTSTMNT02_3250546</td>
      <td>1</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Kawaii Kiwis</td>
      <td>oe:team:8eb9a212591f919a353abfac0c0a52a</td>
      <td>NaN</td>
      <td>Jayce</td>
      <td>Orianna</td>
      <td>Rell</td>
      <td>Nautilus</td>
      <td>Leona</td>
      <td>8.750000</td>
      <td>NaN</td>
      <td>32.9405</td>
    </tr>
  </tbody>
</table>
<p>10980 rows × 19 columns</p>
</div>



#### Univariate Analysis
Now let's look at the three most interesting stats about Ezreal's performance: kda, damage share, and creep score per minute (cspm)


```python
import plotly.offline as pyo
```




    'cspm_distribution.html'




```python
fig_kda = px.box(ezrealdf, x='kda', title='KDA Distribution in Ezreal Games')
fig_kda.show()

fig_damageshare = px.box(ezrealdf, x='damageshare', title='Damageshare Distribution in Ezreal Games')
fig_damageshare.show()

fig_cspm = px.box(ezrealdf, x='cspm', title='CSPM Distribution in Ezreal Games')
fig_cspm.show()

```







#### Bivariate Analysis
Let's look the differnece of the three most important statistical metrics, kda, cspm, and damageshare between Ezreal and all other ADCs


```python
df = game_performance_metrics.copy()
bot_data = df[df['position'] == 'bot']

bot_data['Champion Type'] = bot_data['champion'].apply(lambda x: 'Ezreal' if x == 'Ezreal' else 'Other Champions')

fig_kda = px.box(bot_data, y='Champion Type', x='kda', 
                 title='KDA Box Plot: Ezreal vs Other Champions (Bot Position)')
fig_kda.show()

fig_damageshare = px.box(bot_data, y='Champion Type', x='damageshare', 
                         title='Damageshare Box Plot: Ezreal vs Other Champions (Bot Position)')
fig_damageshare.show()

fig_cspm = px.box(bot_data, y='Champion Type', x='cspm', 
                  title='CSPM Box Plot: Ezreal vs Other Champions (Bot Position)')
fig_cspm.show()
```

    /var/folders/g0/6rfqkkms2jl55vm04r5k709r0000gn/T/ipykernel_726/489161154.py:4: SettingWithCopyWarning:
    
    
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
    








#### Interesting Aggregates	
For a game that has no tide, the expected win rate would be 50$. Let's first see if that is the case for side choosing ezreal.


```python
ezreal_games = game_performance_metrics[game_performance_metrics['champion'] == 'Ezreal']
win_rate_ezreal = (ezreal_games[ezreal_games['result'] == 1].shape[0] / ezreal_games.shape[0]) * 100
print(f"Overall Win Rate for Ezreal: {win_rate_ezreal:.2f}%")
```

    Overall Win Rate for Ezreal: 45.79%


For intuitive calculation, I will add a column as "performancescore" which is the combination of the standardized version of the three statistics- kda, cspm, and damageshare - to the dataframe


```python
kda_standardized = (game_performance_metrics['kda'] - game_performance_metrics['kda'].mean()) / game_performance_metrics['kda'].std()
cspm_standardized = (game_performance_metrics['cspm'] - game_performance_metrics['cspm'].mean()) / game_performance_metrics['cspm'].std()
damageshare_standardized = (game_performance_metrics['damageshare'] - game_performance_metrics['damageshare'].mean()) / game_performance_metrics['damageshare'].std()
game_performance_metrics['performancescore'] = kda_standardized + cspm_standardized + damageshare_standardized

#updating ezreal_df
ezreal_gameids = game_performance_metrics[game_performance_metrics['champion'] == 'Ezreal']['gameid'].unique()
ezrealdf =game_performance_metrics[game_performance_metrics['gameid'].isin(ezreal_gameids)]

game_performance_metrics
```




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
      <td>0.254200</td>
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
      <td>-2.487362</td>
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
      <td>0.845127</td>
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
      <td>3.558888</td>
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
      <td>-2.515943</td>
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
    </tr>
    <tr>
      <th>129343</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>8</td>
      <td>Red</td>
      <td>mid</td>
      <td>Tirex</td>
      <td>oe:player:ae97b9649e39ad901b680f74c3f56b3</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Ahri</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>9.000000</td>
      <td>0.304237</td>
      <td>9.6440</td>
      <td>1.714837</td>
    </tr>
    <tr>
      <th>129344</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Alonshot</td>
      <td>oe:player:1723bb9b9fe68aea988f0c7ec75fbe1</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Aphelios</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>3.500000</td>
      <td>0.187860</td>
      <td>9.5183</td>
      <td>-0.509043</td>
    </tr>
    <tr>
      <th>129345</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>10</td>
      <td>Red</td>
      <td>sup</td>
      <td>Boohis</td>
      <td>oe:player:38408cb0943e6f27ccd6272bdc1f09b</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>Rakan</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>12.000000</td>
      <td>0.068353</td>
      <td>1.8220</td>
      <td>-0.999986</td>
    </tr>
    <tr>
      <th>129346</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>0</td>
      <td>1</td>
      <td>100</td>
      <td>Blue</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Erfolg Esports</td>
      <td>oe:team:4103ef051074f24e9566d1b7443c3fb</td>
      <td>NaN</td>
      <td>Maokai</td>
      <td>Poppy</td>
      <td>Taliyah</td>
      <td>Milio</td>
      <td>Cassiopeia</td>
      <td>0.857143</td>
      <td>NaN</td>
      <td>33.6440</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>129347</th>
      <td>ESPORTSTMNT02_3251457</td>
      <td>1</td>
      <td>1</td>
      <td>200</td>
      <td>Red</td>
      <td>team</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Universae Instituto FP</td>
      <td>oe:team:2d02ba0b874367692a25110f0e321f6</td>
      <td>NaN</td>
      <td>Rumble</td>
      <td>Ziggs</td>
      <td>Jarvan IV</td>
      <td>Orianna</td>
      <td>Syndra</td>
      <td>10.250000</td>
      <td>NaN</td>
      <td>37.6335</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>129348 rows × 20 columns</p>
</div>



It seems like the win rate is about 5 % lower than the expected value. But for its significance, we will wait till the last section in this report to find out.


### Assessment of Missingness

Let's look at all the columns with missing values.


```python
columns_with_missing_values = game_performance_metrics.columns[game_performance_metrics.isnull().any()].tolist()
columns_with_missing_values
```




    ['playername',
     'playerid',
     'teamid',
     'champion',
     'ban1',
     'ban2',
     'ban3',
     'ban4',
     'ban5',
     'damageshare',
     'cspm',
     'performancescore']




```python
ezreal_games.head(15)
```




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
      <td>12.00</td>
      <td>0.441215</td>
      <td>8.4992</td>
    </tr>
    <tr>
      <th>195</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Shade</td>
      <td>oe:player:1c749862591cbbc9e4609d7a10288f4</td>
      <td>Janus Esports</td>
      <td>oe:team:1ab54595dac94e054c4f3831f7ccb98</td>
      <td>Ezreal</td>
      <td>Heimerdinger</td>
      <td>Yuumi</td>
      <td>Nami</td>
      <td>Darius</td>
      <td>Camille</td>
      <td>5.00</td>
      <td>0.206674</td>
      <td>7.6786</td>
    </tr>
    <tr>
      <th>332</th>
      <td>ESPORTSTMNT03_3084449</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Nothing</td>
      <td>oe:player:f80a4ad87fee7c9fdc19b7769495fdb</td>
      <td>Leviatan Esports</td>
      <td>oe:team:294ae8f82e2061ab10ef6a3459bc02d</td>
      <td>Ezreal</td>
      <td>Yuumi</td>
      <td>Kassadin</td>
      <td>Wukong</td>
      <td>Fiora</td>
      <td>Sejuani</td>
      <td>11.00</td>
      <td>0.403989</td>
      <td>10.8476</td>
    </tr>
    <tr>
      <th>488</th>
      <td>ESPORTSTMNT03_3085482</td>
      <td>0</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Redstratos</td>
      <td>oe:player:17a67c112efdb928dbabbbe91904fa7</td>
      <td>War Legion Esports</td>
      <td>oe:team:35d8c122cd2fd58cdb1208f823023af</td>
      <td>Ezreal</td>
      <td>K'Sante</td>
      <td>Heimerdinger</td>
      <td>Varus</td>
      <td>Fiora</td>
      <td>Camille</td>
      <td>0.00</td>
      <td>0.315110</td>
      <td>8.4427</td>
    </tr>
    <tr>
      <th>1035</th>
      <td>ESPORTSTMNT06_2763150</td>
      <td>0</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>PiOk</td>
      <td>oe:player:956b4d2f499b1d362f693f82b8e652b</td>
      <td>beGenius ESC</td>
      <td>oe:team:607baf04091e515e195644cb08ec21c</td>
      <td>Ezreal</td>
      <td>Fiora</td>
      <td>Sejuani</td>
      <td>Maokai</td>
      <td>LeBlanc</td>
      <td>Camille</td>
      <td>2.25</td>
      <td>0.340613</td>
      <td>8.4928</td>
    </tr>
    <tr>
      <th>1088</th>
      <td>ESPORTSTMNT03_3084614</td>
      <td>0</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Legolas</td>
      <td>oe:player:5cfc41b7eccda649db08ead84343554</td>
      <td>BISONS ECLUB</td>
      <td>oe:team:b346309564f4fc7f30ac14403e93010</td>
      <td>Ezreal</td>
      <td>Yuumi</td>
      <td>Varus</td>
      <td>Zeri</td>
      <td>Vi</td>
      <td>Xin Zhao</td>
      <td>3.00</td>
      <td>0.258252</td>
      <td>8.6553</td>
    </tr>
    <tr>
      <th>1652</th>
      <td>ESPORTSTMNT04_2663089</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Zamulek</td>
      <td>oe:player:694ee794a9d3a8c3fbd658becb89769</td>
      <td>NNO Prime</td>
      <td>oe:team:2ae1a4c6fe17bf70dd4b5520d60f55b</td>
      <td>Ezreal</td>
      <td>Gangplank</td>
      <td>Ryze</td>
      <td>Nami</td>
      <td>Kalista</td>
      <td>Caitlyn</td>
      <td>6.00</td>
      <td>0.295003</td>
      <td>9.8522</td>
    </tr>
    <tr>
      <th>1808</th>
      <td>ESPORTSTMNT03_3088284</td>
      <td>0</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Fatorix</td>
      <td>oe:player:4f7a70e4a2d3a81289bd3efad09b915</td>
      <td>PÊEK Gaming</td>
      <td>oe:team:db4e98d03fec12b08cb7a80b739c446</td>
      <td>Ezreal</td>
      <td>Ryze</td>
      <td>K'Sante</td>
      <td>Heimerdinger</td>
      <td>Viego</td>
      <td>Vi</td>
      <td>0.25</td>
      <td>0.171218</td>
      <td>7.6832</td>
    </tr>
    <tr>
      <th>1875</th>
      <td>ESPORTSTMNT03_3088309</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Shakaa</td>
      <td>oe:player:7a5f74a5795c6a476c8c83032d5cae2</td>
      <td>Reven Esports</td>
      <td>oe:team:4054ca135a8ad4383af9b6bed4fabcf</td>
      <td>Ezreal</td>
      <td>Heimerdinger</td>
      <td>Nami</td>
      <td>NaN</td>
      <td>Sylas</td>
      <td>NaN</td>
      <td>16.00</td>
      <td>0.341537</td>
      <td>8.1604</td>
    </tr>
    <tr>
      <th>2115</th>
      <td>ESPORTSTMNT06_2767040</td>
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
      <td>Zac</td>
      <td>Ryze</td>
      <td>Maokai</td>
      <td>Nautilus</td>
      <td>Nami</td>
      <td>7.00</td>
      <td>0.253189</td>
      <td>9.7524</td>
    </tr>
    <tr>
      <th>2139</th>
      <td>ESPORTSTMNT03_3088407</td>
      <td>0</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>iso</td>
      <td>oe:player:3a631438d6f2eba0ef81c8cc070fe15</td>
      <td>Malvinas Gaming</td>
      <td>oe:team:d5772fdb1ae7fcc8046fa2e056a8715</td>
      <td>Ezreal</td>
      <td>Vi</td>
      <td>Sejuani</td>
      <td>Akali</td>
      <td>Yone</td>
      <td>LeBlanc</td>
      <td>1.00</td>
      <td>0.300295</td>
      <td>8.0296</td>
    </tr>
    <tr>
      <th>2367</th>
      <td>ESPORTSTMNT06_2768092</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Comp</td>
      <td>oe:player:5d531a4cf817202fc25eda63906e797</td>
      <td>KOI</td>
      <td>oe:team:5aef7c486046c4885a0baad37b027e8</td>
      <td>Ezreal</td>
      <td>Darius</td>
      <td>Varus</td>
      <td>Wukong</td>
      <td>Viktor</td>
      <td>Viego</td>
      <td>7.00</td>
      <td>0.414519</td>
      <td>11.4364</td>
    </tr>
    <tr>
      <th>2499</th>
      <td>ESPORTSTMNT06_2767108</td>
      <td>1</td>
      <td>1</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>Neon</td>
      <td>oe:player:af07c10f5578a1df16f311eeda3d0d8</td>
      <td>Team Vitality</td>
      <td>oe:team:e8d8ae992fe72acb7adc7bfcee31dbb</td>
      <td>Ezreal</td>
      <td>Maokai</td>
      <td>Zeri</td>
      <td>Azir</td>
      <td>Renata Glasc</td>
      <td>Braum</td>
      <td>11.00</td>
      <td>0.228812</td>
      <td>10.1413</td>
    </tr>
    <tr>
      <th>2511</th>
      <td>ESPORTSTMNT03_3088592</td>
      <td>0</td>
      <td>2</td>
      <td>4</td>
      <td>Blue</td>
      <td>bot</td>
      <td>ZombieHog</td>
      <td>oe:player:7a2798d7c31bb0cdb3401cd4e375f14</td>
      <td>Red Eye</td>
      <td>oe:team:ba218f9a2faccaad7d4a47facbf43fe</td>
      <td>Ezreal</td>
      <td>Zac</td>
      <td>Viego</td>
      <td>Sylas</td>
      <td>Yasuo</td>
      <td>Yone</td>
      <td>8.00</td>
      <td>0.274030</td>
      <td>8.7343</td>
    </tr>
    <tr>
      <th>2600</th>
      <td>ESPORTSTMNT03_3087612</td>
      <td>1</td>
      <td>1</td>
      <td>9</td>
      <td>Red</td>
      <td>bot</td>
      <td>Nothing</td>
      <td>oe:player:f80a4ad87fee7c9fdc19b7769495fdb</td>
      <td>Leviatan Esports</td>
      <td>oe:team:294ae8f82e2061ab10ef6a3459bc02d</td>
      <td>Ezreal</td>
      <td>Yuumi</td>
      <td>Lucian</td>
      <td>Akali</td>
      <td>Ornn</td>
      <td>Heimerdinger</td>
      <td>3.00</td>
      <td>0.458975</td>
      <td>10.6485</td>
    </tr>
  </tbody>
</table>
</div>



#### Missing by Design
We will analyze each missingness one by one\
Let's start by looking at the columns likely missing by design. These are typically columns with value that are missing at some fixed location, suggesting manual emptying of data in those spots

#### champion
Lets's look at the missingness in the games with the champion ezreal. Below is a simplified dataframe with only gameid and champions. As you can see, there are missing values spread throughout the dataframe. The diciotnary below returns the relative location in the missing value apears in each game.


```python
ezrealdf_simplified = ezrealdf[['gameid', 'champion']]
ezrealdf_simplified.head(25)
```




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
      <th>gameid</th>
      <th>champion</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Jax</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Poppy</td>
    </tr>
    <tr>
      <th>2</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Taliyah</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Ezreal</td>
    </tr>
    <tr>
      <th>4</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Karma</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Sejuani</td>
    </tr>
    <tr>
      <th>6</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Viego</td>
    </tr>
    <tr>
      <th>7</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Syndra</td>
    </tr>
    <tr>
      <th>8</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Zeri</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>Yuumi</td>
    </tr>
    <tr>
      <th>10</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>ESPORTSTMNT06_2753012</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>192</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>K'Sante</td>
    </tr>
    <tr>
      <th>193</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Kindred</td>
    </tr>
    <tr>
      <th>194</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Syndra</td>
    </tr>
    <tr>
      <th>195</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Ezreal</td>
    </tr>
    <tr>
      <th>196</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Renata Glasc</td>
    </tr>
    <tr>
      <th>197</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Gwen</td>
    </tr>
    <tr>
      <th>198</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Xin Zhao</td>
    </tr>
    <tr>
      <th>199</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Ryze</td>
    </tr>
    <tr>
      <th>200</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Zeri</td>
    </tr>
    <tr>
      <th>201</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>Lulu</td>
    </tr>
    <tr>
      <th>202</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>203</th>
      <td>ESPORTSTMNT03_3083359</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>324</th>
      <td>ESPORTSTMNT03_3084449</td>
      <td>Ornn</td>
    </tr>
  </tbody>
</table>
</div>



As shown above, missin values seems to only appears in relative spots of the gameid.


```python
missing_value_frequency = {}
for game_id in ezrealdf_simplified['gameid'].unique():
    game_rows = ezrealdf_simplified[ezrealdf_simplified['gameid'] == game_id]
    total_rows = len(game_rows)
    
    for index, row in game_rows.iterrows():
        if pd.isnull(row['champion']):
            relative_location = game_rows.index.get_loc(index) / total_rows
            
            relative_location = round(relative_location, 2)
            
            if relative_location not in missing_value_frequency:
                missing_value_frequency[relative_location] = 0
            missing_value_frequency[relative_location] += 1



missing_value_frequency    
```




    {0.83: 915, 0.92: 915}



As shown, values are only missing at two relative spots, thus making them missing by design. The same can be said for playername, damageshare, cspm, and performancescore.


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


#### Not Missing are Random.


```python
game_performance_metrics[game_performance_metrics["playerid"].isna()].head(8)
```




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




```python
game_performance_metrics[game_performance_metrics["teamid"].isna()].head(8)
```




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

#### Missing at Random
Code below checks the correlation of each missing column in relationship with all other columns. Is there are columns with extremely low p_value 0.05, the correctlated columns will be returned in a dicionary where the key is each column. And if the column is uncorrelated with any other columns, its value will be 'MCAR'


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



### Hypothesis Testing
Among the selective columns in the dataframe, the only strong indicator of Ezreal's attribution is game that is not missing is its win rate.\
Null hypothesis: Ezreal's win rate is similar to the average win rate \
Alternative hypothesis: Ezreal's win rate is way lower than the average win rate



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


As shown above, no matter how many tests conducted, the p_value is still smaller than the alpha level of 0.05. Thus, the win rate is statistically significant and we can reject the null hypothesis. This shows that the win rate for Ezreal is significantly lower than the average win rate.

