<p align="center">
  <h1 align="center">Official ApexTab API Documentation</h3>
</p>

<hr>

## About
- Please note that We are offering this API to all of the users in the community who would to get creative with our data.

## Limitations
- There are no limitations to this API as long as it is not abused. We hold the right to refuse service to anyone who we believe is abusing this system.

<hr>

## Search by name

Request URL {GET} https://apextab.com/api/search.php


METHOD | **platform**:

- <i>**pc**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

METHOD | **search**:

- <i>**playername**</i> urlencode the playername<br>

Response data:

- <i>**aid**</i> is the Identifier assigned by ApexTab to the player<br>
- <i>**name**</i> is the current name of the player<br>
- <i>**platform**</i> is the platform of the player<br>
- <i>**avatar**</i> is the current avatar URL of the player<br>
- <i>**legend**</i> is the current selected legend of the player<br>
- <i>**level**</i> is the current level of the player<br>
- <i>**kills**</i> is the current total kills of the player<br>

Example: https://apextab.com/api/search.php?platform=pc&search=ball

Example response:
```
{  
   "results":[  
      {  
         "aid":"d3afc956ebceabefc2488f093f96182f",
         "name":"Ballabriggsx",
         "platform":"pc",
         "avatar":"https://apextab.com/cache/bf803897b5f71857f60f29d00cbdd883.png",
         "legend":"Lifeline",
         "level":"0",
         "kills":"97"
      },
      {  
         "aid":"f5337d769b7b29628f59d8c84ea45d9d",
         "name":"BallerInGame",
         "platform":"pc",
         "avatar":"https://apextab.com/cache/fc4c4cba183c2f81a94730be057cf07d.png",
         "legend":"Lifeline",
         "level":"28",
         "kills":"112"
      }
   ],
   "totalresults":2
}
```
<hr>

## Get player data by ID

Request URL {GET} https://apextab.com/api/player.php

METHOD | **aid**:

- <i>**aid**</i> is the ID that ApexTab assigns to every player.<br>

An example of a player ID is: <i>**f5337d769b7b29628f59d8c84ea45d9d**</i>

Example: https://apextab.com/api/player.php?aid=f5337d769b7b29628f59d8c84ea45d9d

Example response: 
```
{
  "playerfound": true,
  "aid": "f5337d769b7b29628f59d8c84ea45d9d",
  "name": "BallerInGame",
  "platform": "PC",
  "skillratio": 4,
  "visits": "1522",
  "avatar": "https://apextab.com/cache/fc4c4cba183c2f81a94730be057cf07d.png",
  "legend": "Lifeline",
  "level": "28",
  "kills": "112",
  "headshots": "178",
  "matches": "113",
  "kills_Bloodhound": "18",
  "kills_Gibraltar": "10",
  "kills_Lifeline": "9",
  "kills_Pathfinder": "4",
  "kills_Wraith": "2",
  "kills_Bangalore": "62",
  "kills_Caustic": "3",
  "kills_Mirage": "4",
  "headshots_Bloodhound": "38",
  "headshots_Gibraltar": "11",
  "headshots_Lifeline": "23",
  "headshots_Pathfinder": "31",
  "headshots_Wraith": "4",
  "headshots_Bangalore": "61",
  "headshots_Caustic": "4",
  "headshots_Mirage": "6",
  "matches_Bloodhound": "11",
  "matches_Gibraltar": "13",
  "matches_Lifeline": "10",
  "matches_Pathfinder": "15",
  "matches_Wraith": "11",
  "matches_Bangalore": "40",
  "matches_Caustic": "7",
  "matches_Mirage": "6",
  "globalrank": "24192",
  "utime": "1550669669"
}
```

<hr>

## Affiliation
- The ApexTab API is in no way shape or form affiliated with Electronic Arts and its partners. Any "Apex Legend" name, logos and/or images are registered trademarks of EA Games and/or Respawn.
