# boxscore.md

# BoxScore
##### [nba_api/live/nba/endpoints/boxscore.py](https://github.com/swar/nba_api/blob/master/nba_api/live/nba/endpoints/boxscore.py)

##### Endpoint URL
>[https://cdn.nba.com/static/json/liveData/boxscore/boxscore_{game_id}.json](https://cdn.nba.com/static/json/liveData/boxscore/boxscore_{game_id}.json)

##### Valid URL
>[https://cdn.nba.com/static/json/liveData/boxscore/boxscore_0022000181.json](https://cdn.nba.com/static/json/liveData/boxscore/boxscore_0022000181.json)

## Parameters
API Parameter Name | Python Parameter Variable | Pattern | Required | Nullable
------------ | ------------ | :-----------: | :---: | :---:
[_**GameID**_](https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/library/parameters.md#GameID) | game_id | `^\d{10}$` | `Y` |  |

## DataSets
#### Arena `Arena`
```text
["arenaId", "arenaName", "arenaCity", "arenaState", "arenaCountry", "arenaTimezone"}
```
#### AwayTeam `away_team`
```text
["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "players"["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"]
```
#### AwayTeamStats `away_team_stats`
```text
["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"]
```
#### AwayTeamPlayerStats `away_team_player_stats`
```
["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"]
```
#### Game `game`
```text
["gameId", "gameTimeLocal", "gameTimeUTC", "gameTimeHome", "gameTimeAway", "gameEt", "duration", "gameCode", "gameStatusText", "gameStatus", "regulationPeriods", "period", "gameClock", "attendance", "sellout", "arena""arenaId", "arenaName", "arenaCity", "arenaState", "arenaCountry", "arenaTimezone", "officials"["personId", "name", "nameI", "firstName", "familyName", "jerseyNum", "assignment"], "homeTeam" ["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "players"["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"], "awayTeam"["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "players"["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"]]
```
#### HomeTeam `home_team`
```text
["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "players"["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"]
```
#### HomeTeamStats `home_team_stats`
```text
["teamId", "teamName", "teamCity", "teamTricode", "score", "inBonus", "timeoutsRemaining", "periods"["period", "periodType", "score"], "statistics""assists", "assistsTurnoverRatio", "benchPoints", "biggestLead", "biggestLeadScore", "biggestScoringRun", "biggestScoringRunScore", "blocks", "blocksReceived", "fastBreakPointsAttempted", "fastBreakPointsMade", "fastBreakPointsPercentage", "fieldGoalsAttempted", "fieldGoalsEffectiveAdjusted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTeam", "foulsTechnical", "foulsTeamTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "leadChanges", "minutes", "minutesCalculated", "points", "pointsAgainst", "pointsFastBreak", "pointsFromTurnovers", "pointsInThePaint", "pointsInThePaintAttempted", "pointsInThePaintMade", "pointsInThePaintPercentage", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsPersonal", "reboundsTeam", "reboundsTeamDefensive", "reboundsTeamOffensive", "reboundsTotal", "secondChancePointsAttempted", "secondChancePointsMade", "secondChancePointsPercentage", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "timeLeading", "timesTied", "trueShootingAttempts", "trueShootingPercentage", "turnovers", "turnoversTeam", "turnoversTotal", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage"]
```
#### HomeTeamPlayerStats `home_team_player_stats`
```
["status", "notPlayingReason", "notPlayingDescription", "order", "personId", "jerseyNum", "starter", "oncourt", "played", "statistics""assists", "blocks", "blocksReceived", "fieldGoalsAttempted", "fieldGoalsMade", "fieldGoalsPercentage", "foulsOffensive", "foulsDrawn", "foulsPersonal", "foulsTechnical", "freeThrowsAttempted", "freeThrowsMade", "freeThrowsPercentage", "minus", "minutes", "minutesCalculated", "plus", "plusMinusPoints", "points", "pointsFastBreak", "pointsInThePaint", "pointsSecondChance", "reboundsDefensive", "reboundsOffensive", "reboundsTotal", "steals", "threePointersAttempted", "threePointersMade", "threePointersPercentage", "turnovers", "twoPointersAttempted", "twoPointersMade", "twoPointersPercentage", "name", "nameI", "firstName", "familyName"]
```
#### Officials `officials`
```text
["personId", "name", "nameI", "firstName", "familyName", "jerseyNum", "assignment"]
```



## JSON
```json
{
   "meta":{
      "version":1,
      "code":200,
      "request":"http://nba.cloud/games/0022000180/boxscore?Format=json",
      "time":"2021-01-15 23:51:25.282704"
   },
   "game":{
      "gameId":"0022000180",
      "gameTimeLocal":"2021-01-15T19:30:00-05:00",
      "gameTimeUTC":"2021-01-16T00:30:00Z",
      "gameTimeHome":"2021-01-15T19:30:00-05:00",
      "gameTimeAway":"2021-01-15T19:30:00-05:00",
      "gameEt":"2021-01-15T19:30:00-05:00",
      "duration":125,
      "gameCode":"20210115/ORLBOS",
      "gameStatusText":"Final",
      "gameStatus":3,
      "regulationPeriods":4,
      "period":4,
      "gameClock":"PT00M00.00S",
      "attendance":0,
      "sellout":"0",
      "arena":{
         "arenaId":17,
         "arenaName":"TD Garden",
         "arenaCity":"Boston",
         "arenaState":"MA",
         "arenaCountry":"US",
         "arenaTimezone":"America/New_York"
      },
      "officials":[
         {
            "personId":201638,
            "name":"Brent Barnaky",
            "nameI":"B. Barnaky",
            "firstName":"Brent",
            "familyName":"Barnaky",
            "jerseyNum":"36",
            "assignment":"OFFICIAL1"
         }
      ],
      "homeTeam":{
         "teamId":1610612738,
         "teamName":"Celtics",
         "teamCity":"Boston",
         "teamTricode":"BOS",
         "score":124,
         "inBonus":"1",
         "timeoutsRemaining":2,
         "periods":[
            {
               "period":1,
               "periodType":"REGULAR",
               "score":34
            }
         ],
         "players":[
            {
               "status":"ACTIVE",
               "order":1,
               "personId":1627759,
               "jerseyNum":"7",
               "position":"SF",
               "starter":"1",
               "oncourt":"0",
               "played":"1",
               "statistics":{
                  "assists":8,
                  "blocks":0,
                  "blocksReceived":0,
                  "fieldGoalsAttempted":12,
                  "fieldGoalsMade":6,
                  "fieldGoalsPercentage":0.5,
                  "foulsOffensive":0,
                  "foulsDrawn":4,
                  "foulsPersonal":1,
                  "foulsTechnical":0,
                  "freeThrowsAttempted":7,
                  "freeThrowsMade":7,
                  "freeThrowsPercentage":1.0,
                  "minus":50.0,
                  "minutes":"PT25M01.00S",
                  "minutesCalculated":"PT25M",
                  "plus":65.0,
                  "plusMinusPoints":15.0,
                  "points":21,
                  "pointsFastBreak":0,
                  "pointsInThePaint":6,
                  "pointsSecondChance":0,
                  "reboundsDefensive":2,
                  "reboundsOffensive":0,
                  "reboundsTotal":2,
                  "steals":1,
                  "threePointersAttempted":5,
                  "threePointersMade":2,
                  "threePointersPercentage":0.4,
                  "turnovers":2,
                  "twoPointersAttempted":7,
                  "twoPointersMade":4,
                  "twoPointersPercentage":0.5714285714285711
               },
               "name":"Jaylen Brown",
               "nameI":"J. Brown",
               "firstName":"Jaylen",
               "familyName":"Brown"
            }
         ],
         "statistics":{
            "assists":25,
            "assistsTurnoverRatio":2.27272727272727,
            "benchPoints":66,
            "biggestLead":29,
            "biggestLeadScore":"72-101",
            "biggestScoringRun":13,
            "biggestScoringRunScore":"72-101",
            "blocks":4,
            "blocksReceived":1,
            "fastBreakPointsAttempted":9,
            "fastBreakPointsMade":5,
            "fastBreakPointsPercentage":0.555555555555556,
            "fieldGoalsAttempted":88,
            "fieldGoalsEffectiveAdjusted":0.607954545454545,
            "fieldGoalsMade":45,
            "fieldGoalsPercentage":0.511363636363636,
            "foulsOffensive":0,
            "foulsDrawn":16,
            "foulsPersonal":18,
            "foulsTeam":18,
            "foulsTechnical":0,
            "foulsTeamTechnical":0,
            "freeThrowsAttempted":19,
            "freeThrowsMade":17,
            "freeThrowsPercentage":0.894736842105263,
            "leadChanges":4,
            "minutes":"PT240M00.00S",
            "minutesCalculated":"PT240M",
            "points":124,
            "pointsAgainst":97,
            "pointsFastBreak":13,
            "pointsFromTurnovers":16,
            "pointsInThePaint":48,
            "pointsInThePaintAttempted":36,
            "pointsInThePaintMade":24,
            "pointsInThePaintPercentage":0.666666666666666,
            "pointsSecondChance":11,
            "reboundsDefensive":39,
            "reboundsOffensive":6,
            "reboundsPersonal":45,
            "reboundsTeam":6,
            "reboundsTeamDefensive":2,
            "reboundsTeamOffensive":4,
            "reboundsTotal":51,
            "secondChancePointsAttempted":6,
            "secondChancePointsMade":4,
            "secondChancePointsPercentage":0.666666666666666,
            "steals":7,
            "threePointersAttempted":42,
            "threePointersMade":17,
            "threePointersPercentage":0.40476190476190504,
            "timeLeading":"PT47M16.00S",
            "timesTied":0,
            "trueShootingAttempts":96.36,
            "trueShootingPercentage":0.6434205064342051,
            "turnovers":10,
            "turnoversTeam":1,
            "turnoversTotal":11,
            "twoPointersAttempted":46,
            "twoPointersMade":28,
            "twoPointersPercentage":0.608695652173913
         }
      },
      "awayTeam":{
         "teamId":1610612753,
         "teamName":"Magic",
         "teamCity":"Orlando",
         "teamTricode":"ORL",
         "score":97,
         "inBonus":"1",
         "timeoutsRemaining":2,
         "periods":[
            {
               "period":1,
               "periodType":"REGULAR",
               "score":28
            }
         ],
         "players":[
            {
               "status":"ACTIVE",
               "order":1,
               "personId":203516,
               "jerseyNum":"11",
               "position":"SF",
               "starter":"1",
               "oncourt":"0",
               "played":"1",
               "statistics":{
                  "assists":0,
                  "blocks":0,
                  "blocksReceived":0,
                  "fieldGoalsAttempted":4,
                  "fieldGoalsMade":1,
                  "fieldGoalsPercentage":0.25,
                  "foulsOffensive":0,
                  "foulsDrawn":0,
                  "foulsPersonal":3,
                  "foulsTechnical":0,
                  "freeThrowsAttempted":0,
                  "freeThrowsMade":0,
                  "freeThrowsPercentage":0.0,
                  "minus":41.0,
                  "minutes":"PT14M34.00S",
                  "minutesCalculated":"PT14M",
                  "plus":36.0,
                  "plusMinusPoints":-5.0,
                  "points":2,
                  "pointsFastBreak":0,
                  "pointsInThePaint":2,
                  "pointsSecondChance":0,
                  "reboundsDefensive":1,
                  "reboundsOffensive":0,
                  "reboundsTotal":1,
                  "steals":0,
                  "threePointersAttempted":2,
                  "threePointersMade":0,
                  "threePointersPercentage":0.0,
                  "turnovers":0,
                  "twoPointersAttempted":2,
                  "twoPointersMade":1,
                  "twoPointersPercentage":0.5
               },
               "name":"James Ennis III",
               "nameI":"J. Ennis III",
               "firstName":"James",
               "familyName":"Ennis III"
            }
         ],
         "statistics":{
            "assists":14,
            "assistsTurnoverRatio":1.07692307692308,
            "benchPoints":33,
            "biggestLead":1,
            "biggestLeadScore":"4-3",
            "biggestScoringRun":13,
            "biggestScoringRunScore":"72-101",
            "blocks":1,
            "blocksReceived":4,
            "fastBreakPointsAttempted":7,
            "fastBreakPointsMade":2,
            "fastBreakPointsPercentage":0.28571428571428603,
            "fieldGoalsAttempted":94,
            "fieldGoalsEffectiveAdjusted":0.441489361702128,
            "fieldGoalsMade":38,
            "fieldGoalsPercentage":0.404255319148936,
            "foulsOffensive":2,
            "foulsDrawn":18,
            "foulsPersonal":16,
            "foulsTeam":14,
            "foulsTechnical":1,
            "foulsTeamTechnical":0,
            "freeThrowsAttempted":22,
            "freeThrowsMade":14,
            "freeThrowsPercentage":0.636363636363636,
            "leadChanges":4,
            "minutes":"PT240M00.00S",
            "minutesCalculated":"PT240M",
            "points":97,
            "pointsAgainst":124,
            "pointsFastBreak":8,
            "pointsFromTurnovers":10,
            "pointsInThePaint":52,
            "pointsInThePaintAttempted":47,
            "pointsInThePaintMade":26,
            "pointsInThePaintPercentage":0.553191489361702,
            "pointsSecondChance":20,
            "reboundsDefensive":31,
            "reboundsOffensive":15,
            "reboundsPersonal":46,
            "reboundsTeam":12,
            "reboundsTeamDefensive":4,
            "reboundsTeamOffensive":8,
            "reboundsTotal":58,
            "secondChancePointsAttempted":16,
            "secondChancePointsMade":9,
            "secondChancePointsPercentage":0.5625,
            "steals":5,
            "threePointersAttempted":28,
            "threePointersMade":7,
            "threePointersPercentage":0.25,
            "timeLeading":"PT00M30.00S",
            "timesTied":0,
            "trueShootingAttempts":103.68,
            "trueShootingPercentage":0.46778549382716,
            "turnovers":11,
            "turnoversTeam":2,
            "turnoversTotal":13,
            "twoPointersAttempted":66,
            "twoPointersMade":31,
            "twoPointersPercentage":0.46969696969696995
         }
      }
   }
}
```

Last validated 2020-08-16

---

# playbyplay.md

# PlayByPlay
##### [nba_api/live/nba/endpoints/playbyplay.py](https://github.com/swar/nba_api/blob/master/nba_api/live/nba/endpoints/playbyplay.py)

##### Endpoint URL
>>[https://cdn.nba.com/static/json/liveData/playbyplay/playbyplay_{game_id}.json](playbyplay/playbyplay_{game_id}.json)

##### Valid URL
>>[https://cdn.nba.com/static/json/liveData/playbyplay/playbyplay_0022000180.json](https://cdn.nba.com/static/json/liveData/playbyplay/playbyplay_0022000180.json)

## Parameters
API Parameter Name | Python Parameter Variable | Pattern | Required | Nullable
------------ | ------------ | :-----------: | :---: | :---:
[_**GameID**_](https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/library/parameters.md#GameID) | game_id | `^\d{10}$` | `Y` |  |

## Data Sets
#### Actions `actions`
```text
["actionNumber", "actionType", "assistPersonId", "assistPlayerNameInitial", "assistTotal", "blockPersonId", "blockPlayerName", "clock", "description", "descriptor", "edited", "foulDrawnPersonId", "foulDrawnPlayerName", "foulPersonalTotal", "foulTechnicalTotal", "isFieldGoal", "jumpBallLostPersonId", "jumpBallLostPlayerName", "jumpBallRecoverdPersonId", "jumpBallRecoveredName", "jumpBallWonPersonId", "jumpBallWonPlayerName", "officialId", "orderNumber", "period", "periodType", "personId", "personIdsFilter"[], "playerName", "playerNameI", "pointsTotal", "possession", "qualifiers"[], "reboundDefensiveTotal", "reboundOffensiveTotal", "reboundTotal", "scoreAway", "scoreHome", "shotActionNumber", "shotDistance", "shotResult", "side", "stealPersonId", "stealPlayerName", "subType", "teamId", "teamTricode", "timeActual", "turnoverTotal", "value", "x", "xLegacy", "y", "yLegacy"]
```
## About `Actions` Data Set
This is intended to be a comprehensive list of all possible `actions` available. Note that not all keys appear on every `action` as it depends on the `actionType`
Key | Class | Sample | Description | AlwaysPresent |
------------ | ------------ | :-----------: | :------------------: | :---------:
`actionNumber`|`<class 'int'>`| `4` | `actionNumber is guaranteed to be sequential but not consectutive ([2, 5, 6, 7, 9, 10])` | `Yes` |
`actionType`|`<class 'str'>`| `"period"` | `-` | `Yes` |
`assistPersonId`|`<class 'int'>`| `1627759` | `-` | `No` |
`assistPlayerNameInitial`|`<class 'str'>`| `J. Brown` | `-` | `No` |
`assistTotal`|`<class 'int'>`| `3` | `-` | `No` |
`blockPersonId`|`<class 'int'>`| `1627759` | `-` | `No` |
`blockPlayerName`|`<class 'str'>`| `J. Brown` | `-` | `No` |
`clock`|`<class 'str'>`| `PT03M59.00S` | `clock is the Period Time in which the play occurred` | `Yes` |
`description`|`<class 'str'>`| `J. Brown 14' pullup Jump Shot (2 PTS)` | `description of the action` | `No` |
`descriptor`|`<class 'str'>`| `pullup` | `a key phrase with regards to the play. Examples: ("heldball","technical","pullup","bad pass","driving finger roll"` )  | `No` |
`edited`|`<class 'str'>`| `2021-01-16T02:01:02Z` | `The time in which the play was edited` | `No` |
`foulDrawnPersonId`|`<class 'int'>`| `1627759` | `-` | `No` |
`foulDrawnPlayerName`|`<class 'str'>`| `Brown` | `-` | `No` |
`foulPersonalTotal`|`<class 'int'>`| `1` | `-` | `No` |
`foulTechnicalTotal`|`<class 'int'>`| `0` | `-` | `No` |
`isFieldGoal`|`<class 'int'>`| `0` | `0 | 1` | `Yes` |
`jumpBallLostPersonId`|`<class 'int'>`| `203935` | `-` | `No` |
`jumpBallLostPlayerName`|`<class 'str'>`| `Smart` | `-` | `No` |
`jumpBallRecoverdPersonId`|`<class 'int'>`| `203932` | `-` | `No` |
`jumpBallRecoveredName`|`<class 'str'>`| `A. Gordon` | `-` | `No` |
`jumpBallWonPersonId`|`<class 'int'>`| `203920` | `-` | `No` |
`jumpBallWonPlayerName`|`<class 'str'>`| `Birch` | `-` | `No` |
`officialId`|`<class 'int'>`| `-` | `-` | `No` |
`orderNumber`|`<class 'int'>`| `4560000` | `unknown consecutive number` | `Yes` |
`period`|`<class 'int'>`| `3` | `-` | `Yes` |
`periodType`|`<class 'str'>`| `-` | `-` | `Yes` |
`personId`|`<class 'int'>`| `1629109` | `-` | `Yes` |
`personIdsFilter`|`<class 'list'>`| `[203932, 203920, 203935]` | `players involved in the play. In this case ti was a jump ball (recovered, won, lost)` | `Yes` |
`playerName`|`<class 'str'>`| `Clark` | `-` | `No` |
`playerNameI`|`<class 'str'>`| `G. Clark` | `-` | `No` |
`pointsTotal`|`<class 'int'>`| `6` | `-` | `No` |
`possession`|`<class 'int'>`| `1610612753` | `The teamId who has possession` | `Yes` |
`qualifiers`|`<class 'list'>`| `["pointsinthepaint"]` | `-` | `yes` |
`reboundDefensiveTotal`|`<class 'int'>`| `6` | `-` | `No` |
`reboundOffensiveTotal`|`<class 'int'>`| `2` | `-` | `No` |
`reboundTotal`|`<class 'int'>`| `8` | `-` | `No` |
`scoreAway`|`<class 'str'>`| `68` | `-` | `Yes` |
`scoreHome`|`<class 'str'>`| `83` | `-` | `Yes` |
`shotActionNumber`|`<class 'int'>`| `10` | `shotActionNumber is guaranteed to be sequential but not consectutive ([10, 14, 18, 38])` |
`shotDistance`|`<class 'float'>`| `4.44` | `-` | `No` |
`shotResult`|`<class 'str'>`| `"Made" | "Missed"` | `-` | `No` |
`side`|`<class 'str'>`| `null | "left" | "right"` | `-` | `Yes` |
`stealPersonId`|`<class 'int'>`| `1629750` | `-` | `No` |
`stealPlayerName`|`<class 'str'>`| `Green` | `-` | `No` |
`subType`|`<class 'str'>`| `"request` | `subType of the actonType` | `No` |
`teamId`|`<class 'int'>`| `1610612738` | `-` | `No` |
`teamTricode`|`<class 'str'>`| `BOS` | `-` | `No` |
`timeActual`|`<class 'str'>`| `2021-01-16T02:14:17.3Z` | `The time in which the play occurred` | `Yes` |
`turnoverTotal`|`<class 'int'>`| `1` | `-` | `No` |
`value`|`<class 'str'>`| `"Corrected to Offensive Foul on C. Anthony"` | `Was found to be present on an actionType of "instantreplay" and subType of "challenge" with a descriptor of "overturned"` | `No` |
`x`|`<class 'float'>`| `90.22667542706965` | `-` | `Yes` |
`xLegacy`|`<class 'int'>`| `-20` | `-` | `Yes`  |
`y`|`<class 'float'>`| `45.90226715686275` | `-` | `Yes`  |
`yLegacy`|`<class 'int'>`| `39` | `-` | `Yes` |


## JSON
```json
{
   "meta":{
      "version":1,
      "code":200,
      "request":"http://nba.cloud/games/0022000180/playbyplay?Format=json",
      "time":"2021-01-15 23:48:58.906160"
   },
   "game":{
      "gameId":"0022000180",
      "actions":[
         {
            "actionNumber":2,
            "actionType":"period",
            "assistPersonId":1627759,
            "assistPlayerNameInitial":"J. Brown",
            "assistTotal":1,
            "blockPersonId":1630202,
            "blockPlayerName":"Pritchard",
            "clock":"PT10M53.00S",
            "description":"N. Vucevic 14' turnaround Hook (2 PTS) (A. Gordon 1 AST)",
            "descriptor":"turnaround",
            "edited":"2021-01-16T00:42:13Z",
            "foulDrawnPersonId":201952,
            "foulDrawnPlayerName":"Teague",
            "foulPersonalTotal":1,
            "foulTechnicalTotal":0,
            "isFieldGoal":1,
            "jumpBallLostPersonId":1628407,
            "jumpBallLostPlayerName":"Bacon",
            "jumpBallRecoverdPersonId":1630202,
            "jumpBallRecoveredName":"P. Pritchard",
            "jumpBallWonPersonId":202684,
            "jumpBallWonPlayerName":"Thompson",
            "officialId":202041,
            "orderNumber":20000,
            "period":1,
            "periodType":"REGULAR",
            "personId":202696,
            "personIdsFilter":[
               1630175,
               201952
            ],
            "playerName":"Williams",
            "playerNameI":"G. Williams",
            "pointsTotal":8,
            "possession":1610612753,
            "qualifiers":[
               "pointsinthepaint"
            ],
            "reboundDefensiveTotal":4,
            "reboundOffensiveTotal":3,
            "reboundTotal":7,
            "scoreAway":"68",
            "scoreHome":"72",
            "shotActionNumber":40,
            "shotDistance":10.64,
            "shotResult":"Missed",
            "side":"right",
            "stealPersonId":"202696",
            "stealPlayerName":"Vucevic",
            "subType":"out",
            "teamId":1610612738,
            "teamTricode":"BOS",
            "timeActual":"2021-01-16T01:16:36.7Z",
            "turnoverTotal":2,
            "value":"Corrected to Offensive Foul on C. Anthony",
            "x":80.81471747700394,
            "xLegacy":-63,
            "y":37.31234681372549,
            "yLegacy":128
         }
      ]
   }
}
```

Last validated 2020-08-16

---

# scoreboard.md

# ScoreBoard
##### [nba_api/live/nba/endpoints/scoreboard.py](https://github.com/swar/nba_api/blob/master/nba_api/live/nba/endpoints/scoreboard.py)

##### Endpoint URL
>[https://cdn.nba.com/static/json/liveData/scoreboard/todaysScoreboard_00.json](https://cdn.nba.com/static/json/liveData/scoreboard/todaysScoreboard_00.json)

## Parameters
`None`

## Properties
#### GameDate `game_date`
```text
#returns a string
scoreboard.ScoreBoard().game_date
```

#### Games `games`
```text
#returns all games as dictionary
scoreboard.ScoreBoard().games.get_dict()

#returns all games as json
scoreboard.ScoreBoard().games.get_json()
```


## JSON
```json
{
   "meta":{
      "version":1,
      "request":"https://nba-prod-us-east-1-mediaops-stats.s3.amazonaws.com/NBA/liveData/scoreboard/todaysScoreboard_00.json",
      "time":"2021-01-16 11:11:39.1139",
      "code":200
   },
   "scoreboard":{
      "gameDate":"2021-01-15",
      "leagueId":"00",
      "leagueName":"National Basketball Association",
      "games":[
         {
            "gameId":"0022000181",
            "gameCode":"20210115/NYKCLE",
            "gameStatus":3,
            "gameStatusText":"Final",
            "period":4,
            "gameClock":"",
            "gameTimeUTC":"2021-01-16T00:30:00Z",
            "gameEt":"2021-01-15T19:30:00Z",
            "regulationPeriods":4,
            "seriesGameNumber":"",
            "seriesText":"",
            "homeTeam":{
               "teamId":1610612739,
               "teamName":"Cavaliers",
               "teamCity":"Cleveland",
               "teamTricode":"CLE",
               "wins":6,
               "losses":7,
               "score":106,
               "inBonus":"None",
               "timeoutsRemaining":1,
               "periods":[
                  {
                     "period":1,
                     "periodType":"REGULAR",
                     "score":28
                  }
               ]
            },
            "awayTeam":{
               "teamId":1610612752,
               "teamName":"Knicks",
               "teamCity":"New York",
               "teamTricode":"NYK",
               "wins":5,
               "losses":8,
               "score":103,
               "inBonus":"None",
               "timeoutsRemaining":0,
               "periods":[
                  {
                     "period":1,
                     "periodType":"REGULAR",
                     "score":25
                  }
               ]
            },
            "gameLeaders":{
               "homeLeaders":{
                  "personId":203083,
                  "name":"Andre Drummond",
                  "jerseyNum":"3",
                  "position":"C",
                  "teamTricode":"CLE",
                  "playerSlug":"None",
                  "points":33,
                  "rebounds":23,
                  "assists":3
               },
               "awayLeaders":{
                  "personId":203944,
                  "name":"Julius Randle",
                  "jerseyNum":"30",
                  "position":"F-C",
                  "teamTricode":"NYK",
                  "playerSlug":"None",
                  "points":28,
                  "rebounds":6,
                  "assists":6
               }
            },
            "pbOdds":{
               "team":"None",
               "odds":0.0,
               "suspended":1
            }
         }
      ]
   }
}
```

Last validated 2020-08-16