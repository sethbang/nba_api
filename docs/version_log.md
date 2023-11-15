# NBA API Change Log

## About Versioning

- The NBA API uses [Semantic Versioning 2.0.0](https://semver.org/)
- Dates are [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) compliant and formatted as `YYYY-MM-DD`

### Types of changes

- `Added` (new features)
- `Changed` (changes in existing functionality)
- `Deprecated` (soon-to-be removed functionality)
- `Removed` (removed functionality).
- `Fixed` (bug fixes)
- `Security` (vulnerabilities)
- `Contributor` (notes on updates to the project)

# Version History

## v1.4.0
### Added
- In-Season Tournament Standings[ISTStandings](https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/endpoints/iststandings.md). @shufinskiy #396
- [EventMsgType](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/library/eventmsgtype.py) now contains INSTANT_REPLAY (18). @usharerose #384 
 
### Changed
- All NBA player and team static data current as of 2023.11.09 #398

### Deprecated
- [EventMsgType](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/library/eventmsgtype.py) UNKNOWN (18) has been deprecated and will be removed in a future release. #400

### Fixed
- The [playbyplay][https://github.com/rsforbes/nba_api/blob/master/src/nba_api/stats/library/playbyplayregex.py] regex for TURNOVER was updated to account for a space within the description provided by the NBA. #401

### Security
- Set minimum requirement for [certifi](https://pypi.org/project/certifi/) to 2023.7.22 per [CVE-2022-23491](https://www.cve.org/CVERecord?id=CVE-2023-37920) / [CWE-296](https://cwe.mitre.org/data/definitions/296.html) #384
- Bumped urllib3 from 2.0.6 to 2.0.7 @dependabot #388

### Developer Notes
- [Black](https://github.com/psf/black) has been implemented project wide and will be required for all PRs. #399
- DevContainer Changes #402
  - The VSCode DevContainer was updated to pin Debian-11 due to changes in Debian 12 that have impacted Python development. 
  - Poetry Shell now includes reference to the project.
  - the ms-python.flake and ms-python.vscode-pylance extensions are now included

## v1.3.1

Date: 2023.10.07

### Security
- Set minimum requirement for [requests](https://pypi.org/project/requests/) to 2.31 per [CVE-2023-32681](https://www.cve.org/CVERecord?id=CVE-2023-32681) / [CWE-200](https://cwe.mitre.org/data/definitions/200.html) 
- Set minimum requirement for [certifi](https://pypi.org/project/certifi/) to 2022.12.07 per [CVE-2022-23491](https://www.cve.org/CVERecord?id=CVE-2022-23491) / [CWE-345](https://cwe.mitre.org/data/definitions/345.html) 

## v1.3.0

Date: 2023-10-04

### Added

#### Endpoints
Eleven new endpoints were added to this release. A massive thank you to @shufinskiy.
- [BoxScoreAdvancedv3](docs/nba_api/stats/endpoints/boxscoreadvancedv3.md)
- [BoxScoreDefensivev2](docs/nba_api/stats/endpoints/boxscoredefensivev2.md)
- [BoxScoreFourFactorsv3](docs/nba_api/stats/endpoints/boxscorefourfactorsv3.md)
- [BoxScoreHustlev2](docs/nba_api/stats/endpoints/boxscorehustlev2.md)
- [BoxScoreMatchupsv3](docs/nba_api/stats/endpoints/boxscorematchupsv3.md)
- [BoxScoreMiscv3](docs/nba_api/stats/endpoints/boxscoremiscv3.md)
- [BoxScorePlayerTrackV3](docs/nba_api/stats/endpoints/boxscoreplayertrackv3.md)
- [BoxScoreScoringV3](docs/nba_api/stats/endpoints/boxscorescoringv3.md)
- [BoxScoreTraditionalv3](docs/nba_api/stats/endpoints/boxscoretraditionalv3.md)
- [BoxScoreUsagev3](docs/nba_api/stats/endpoints/boxscoreusagev3.md)
- [PlaybyPlayv3](docs/nba_api/stats/endpoints/playbyplayv3.md)

### Changed

#### NBA JSON schema 
Until recently, the NBA JSON schema followed a tabular strucutre exposing `headers` and `resultSet`. The NBA is now using a nested JSON schema. In addition, the data labels are no longer uppercase (e.g., `PCT_OREB`), are now camelcase and, in many cases, more descriptive (e.g., `percentageReboundsOffensive`).

#### Other
- All NBA player and team data has been updated to the date of this release.
- Corrected an invalid Slack within the text body to match the link present in the Slack shield.
- Updated NBA team data to include the Nuggets 2023 championship (#350)

## Known Issues
Due to the change in the NBA schema, the following methods will currently return and empty dataframe `{}`
- `.get_normalized_dict()`
- `.get_normalized_json()`
- `.get_headers_from_data_sets()`
All other calls are expected to work as expected.

### Removed
The following eleven endpoints have been deprecated by the NBA and subsequently removed from the library
- BoxScoreDefensive --> [BoxScoreDefensivev2](docs/nba_api/stats/endpoints/boxscoredefensivev2.md)
- BoxScoreMatchups --> [BoxScoreMatchupsv3](docs/nba_api/stats/endpoints/boxscorematchupsv3.md)
- LeagueHustleStatsPlayerLeaders --> unknown
- LeagueHustleStatsTeamLeaders --> unknown
- PlayerDashboardByOpponent --> unknown
- TeamDashboardByClutch --> unknown
- TeamDashboardByGameSplits --> unknown
- TeamDashboardByLastNGames --> unknown
- TeamDashboardByOpponent --> unknown
- TeamDashboardByTeamPerformance --> unknown
- TeamDashboardByYearOverYear --> unknown


### Security
- [urllib3](https://github.com/urllib3/urllib3) from 1.26.15 to 1.26.17. (#373) - @dependabot
- [certifi](https://github.com/certifi/python-certifi) from 2022.12.7 to 2023.7.22 (#360) - @dependabot

### Developer Tools
Updated dev container to dynamically set the python path for Poetry. (#369)

## v1.2.1

Date: 2023-06-13

### Security
- [requests](https://github.com/psf/requests) bumped from 2.28.2 to 2.31.0 via #344 - @dependabot

### Fixed

- Reverted alexfayad@5076fae050ec7d655af300cde7674756c4381943. Change broke materialized url and test. Original URL was found to be valid.
- Resolved bad url in documentation #322 - @alexfayad
- Fixed typo in causing src/nba_api/stats/endpoints/playerindex.py to fail #340 - @shufinskiy 
- Fixed expired Slack URL #347


### Developer Tools
- Support for VS Code Dev Containers (including auto-format via [black](https://github.com/psf/black))


## v1.2.0

Date: 2023-03-23

### Added

- Python: Support for 3.11 #331

- New Endpoint:
  - [PlayerIndex](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/endpoints/playerindex.py) via #326 - @shufinskiy
  - [VideoDetailsAsset](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/endpoints/videodetailsasset.py) via #325 - @OnerInce 

- Jupyter Notebooks (Binary Classification - Home Team Win-Loss Modeling) #329  - @TheResearchLab
  - [Home Team Win-Loss: Data Prep](https://github.com/swar/nba_api/blob/master/docs/examples/Home%20Team%20Win-Loss%20Modeling/Home%20Team%20Win-Loss%20Data%20Prep.ipynb)
  - [Home Team Win-Loss: Modeling](https://github.com/swar/nba_api/blob/master/docs/examples/Home%20Team%20Win-Loss%20Modeling/Home%20Team%20Win-Loss%20Modeling.ipynb)
  - Player Static Data: Updated as of 2023.03.23 #322

### Changed

- Removed Python max version release dependency to allow for all go-forward versions. Bugs with later Python versions can be addressed as needed. #331 

### Fixed

- Documentation: corrected parameter order on commonteamroster.md [PR#317](https://github.com/swar/nba_api/pull/317) - @JohannPally
- Corrected Hawks home state from Atlanta to Georgia #332
- Bug #327: Corrected a missing comma in `src/nba_api/stats/endpoints/__init__.py` #333

### Developer Tools

- Resolved CircleCI build where Poetry and CircleCI Docker images conflicted in how output is managed. #331 

## v1.1.14

Date: 2022-11-16

### Fixed

- Fixed a team turnover regular expression when working with PlayByPlay data.
- Endpoints
  - Fixed [PlayerGameLogs](https://github.com/FarhanSajid1/nba_api/blob/master/src/nba_api/stats/endpoints/playergamelogs.py) parameter OppTeamID --> OpponentTeamID ([#311](https://github.com/swar/nba_api/pull/311) - [FarhanSajid1](https://github.com/FarhanSajid1)

### Added

- [Poetry](https://python-poetry.org/): Python dependency management and packaging made easy
- Updated CONTRIBUTING.md on how to Contribute Code Using Poetry
- [Snyk](https://snyk.io/) for Security Scanning
- Exclusion to `.gitignore` for `.dccache` files created by Snyk CLI
- Introduced .flake8, resolve a number of style guide issues, added exclusions with future TODOs

### Changed

- Minimum Version for NumPy has been set to v1.22.22 due to a security vulnerability in [NumPy v1.21.6](https://security.snyk.io/package/pip/numpy/1.21.6)

### Removed

- Support for Python 3.7 due to a security vulnerability in [NumPy v1.21.6](https://security.snyk.io/package/pip/numpy/1.21.6)

### Security

- Upgraded NumPy from v1.21.6 to v1.22.2 due to three vulnerabilies:
  - [NULL Pointer Dereference](https://security.snyk.io/vuln/SNYK-PYTHON-NUMPY-2321964)
  - [Buffer Overflow](https://security.snyk.io/vuln/SNYK-PYTHON-NUMPY-2321966)
  - [Denial of Service (DOS)](https://security.snyk.io/vuln/SNYK-PYTHON-NUMPY-2321970)
- Integrated [DeepSource](https://deepsource.io/) for code security scanning

## v1.1.13

Date: 2022-10-16

### Fixed

Fix team_index_championship_year [#286](https://github.com/swar/nba_api/pull/286)

- add championship years to data-updater template
- re-add team_index_championship_year to static data
- add Bucks 2021 championship and GSW 2022

## v1.1.12

Date: 2022-10-11

### Added

- 2022-10-08 [Player Data]([https://github.com/swar/nba_api/blob/master/nba_api/stats/library/data.py](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/library/data.py))
- Endpoints
  - [VideoEventsAsset](https://github.com/swar/nba_api/blob/master/src/nba_api/stats/endpoints/videoeventsasset.py) ([#259](https://github.com/swar/nba_api/pull/259) - [prateekjaipuria](https://github.com/prateekjaipuria))
- [`CONTRIBUTING.MD`](https://github.com/swar/nba_api/blob/master/CONTRIBUTING.md)
- [`CHANGELOG.MD`](https://github.com/swar/nba_api/blob/master/CHANGELOG.md)
- GitHub issue template for bugs
- CircleCI build support for Python 3.10
- pyproject.toml ([PEP 621](https://peps.python.org/pep-0621/))

### Changed

- CircleCI
  - [Migrated to next-gen Convenience Images](https://circleci.com/docs/next-gen-migration-guide/)
  - [Config to Version 2.1](https://discuss.circleci.com/t/circleci-2-1-config-overview/26057)
  - Moved `flake8` and `pytest` into Commands
  - Parameterized docker images
- README.md
  - Link to [NBA.com Terms of Use](https://www.nba.com/termsofuse)
  - Getting started samples at the top
  - Other edits for improving the reading structure
- Project Structure
  - Source code moved from flat-layout to src-layout
  - Tests were divided into Unit/Integration

### Removed

- Support for Python 3.4, 3.5, and 3.6
- Setup.py file in favor of pyproject.toml ([PEP 621](https://peps.python.org/pep-0621/))

### Fixed

- [Issue #249](https://github.com/swar/nba_api/issues/249): `./nba_api/stats/endpoints/_base.py` requires `numpy` to format data for `get_data_frame`. `numpy` was not in the list of requirements, but is required.
- [Issue #278](https://github.com/swar/nba_api/issues/278): Fixed `playbyplayregex`, and included updated unit tests, where
  - The NBA removed a space that represented `distance` when `distance` was not included in the made/missed shot.
  - Jump Ball contained a single space in the description (regex now also supports multiple spaces empty description).
  - Team fouls no longer included Player/Referee, just the Team Name & Foul.


# `v1.1.11`
#### `2021-11-08`
`Live NBA Stats`
- Adding missing live functionality [#231](https://github.com/swar/nba_api/pull/231)

# `v1.1.10`
#### `2021-10-31`
`stats.nba.com`
- Added handling of multiple level column names [#212](https://github.com/swar/nba_api/pull/212)
- Finding team by championship years [#219](https://github.com/swar/nba_api/pull/219)
- Updated Static Player and Team Data [#225](https://github.com/swar/nba_api/pull/225)
- Added `previous_season` attribute for Season Parameter [#226](https://github.com/swar/nba_api/pull/226)

`Live NBA Stats`
- Randy added some Live NBA endpoints [#184](https://github.com/swar/nba_api/pull/184/files)

Endpoints were unable to be tested due to outdated analyzer.

# `v1.1.9`
#### `2020-08-18`
`stats.nba.com`
* Fixed bug where LeagueDashOppPtShot was missing in tests and __init__.py [#152](https://github.com/swar/nba_api/pull/152)
* Adding endpoints [#102](https://github.com/swar/nba_api/issues/102)
  * AllTimeLeadersGrids
  * BoxScoreSimilarityScore
  * CumeStatsPlayer
  * CumeStatsPlayerGames
  * CumeStatsTeam
  * CumeStatsTeamGames
  * DraftBoard
  * GameRotation
  * GLAlumBoxScoreSimilarityScore
  * LeagueHustleStatsPlayer [#144](https://github.com/swar/nba_api/issues/144)
  * LeagueHustleStatsPlayerLeaders [#144](https://github.com/swar/nba_api/issues/144)
  * LeagueHustleStatsTeam [#144](https://github.com/swar/nba_api/issues/144), [#147](https://github.com/swar/nba_api/issues/147)
  * LeagueHustleStatsTeamLeaders [#144](https://github.com/swar/nba_api/issues/144)
  * LeagueLineupViz
  * LeagueStandingsV3
  * MatchupsRollup
  * PlayerCareerByCollege
  * PlayerCareerByCollegeRollup
  * PlayerEstimatedMetrics
  * ShotChartLeagueWide
  * TeamEstimatedMetrics

`Tools`
* Various Changes for New Endpoints including Threading


# `v1.1.8`
#### `2020-01-27`
`stats.nba.com`
* Updating Headers for New Requirements [#126](https://github.com/swar/nba_api/pull/126)
* Updates to Static Players Data 
* Added Proxy List Support
* Adding endpoint [#102](https://github.com/swar/nba_api/issues/102)
  * TeamGameLogs

`Tools`
* Added Parameter Overrides for Bad Parameter Analysis [#99](https://github.com/swar/nba_api/issues/99)


# `v1.1.7`
#### `2020-01-27`
##### SCRAPPED


# `v1.1.6`
#### `2020-01-27`
##### SCRAPPED

# `v1.1.5`
#### `2019-11-09`
`stats.nba.com`
* Bug fix to PlayByPlay Regex [#89](https://github.com/swar/nba_api/pull/89)
* Updates to Static Players Data with 2019 Draft [#91](https://github.com/swar/nba_api/issues/91)
* Updating Headers to Include Referer [#94](https://github.com/swar/nba_api/issues/94)
* Adding endpoint [#79](https://github.com/swar/nba_api/issues/79)
  * PlayerGameLogs


# `v1.1.4`
#### `2019-04-28`
`stats.nba.com`
* Updates to PlayByPlay Regex [#70](https://github.com/swar/nba_api/pull/70)

`Scripts`
* Added Script for Static Player Updater

`Tests`
* Updates to PlayByPlay Tests with Yesterday's Games [#70](https://github.com/swar/nba_api/pull/70)

`Tools`
* Added Static Player Data Updater Tool [#67](https://github.com/swar/nba_api/pull/67) 


# `v1.1.3`
#### `2019-04-21`
`stats.nba.com`
* Added PlayByPlay Regex for Ejections [#64](https://github.com/swar/nba_api/pull/64)
* Adding Active Status to Static Player List [#66](https://github.com/swar/nba_api/pull/66)
* Removing `tools` from the PyPi upload


# `v1.1.2`
#### `2019-04-15`
`stats.nba.com`
* Updating PlayByPlay Regex. [#59](https://github.com/swar/nba_api/pull/59)
* Adding endpoint [#60](https://github.com/swar/nba_api/pull/60)
  * SynergyPlayTypes


# `v1.1.1`
#### `2019-04-07`
`stats.nba.com`
* Adding proxy, header, and timeout support for every request. [#49](https://github.com/swar/nba_api/issues/49)
  * [Example](https://github.com/swar/nba_api/blob/master/docs/nba_api/stats/examples.md)
* Fixing auto-complete tabs for IDEs on endpoints. [#45](https://github.com/swar/nba_api/pull/45)
* Laid out foundation for future url generation without requesting.
* Adding endpoints [#54](https://github.com/swar/nba_api/issues/54)
  * AssistLeaders
  * AssistTracker
  * BoxScoreDefensive
  * BoxScoreMatchups
  * FantasyWidget
  * FranchiseLeaders
  * FranchisePlayers
  * LeaguePlayerOnDetails
  * LeagueSeasonMatchups
  * TeamAndPlayersVsPlayers
  * WinProbabilityPBP

`Tools`
* Updating analysis for site updates


# `v1.0.7`
#### 2018-12-11
`stats.nba.com`
* PlayersVsPlayers no longer valid.
* Adding TwoWay to parameters

`Documentation`
* Updating Endpoint docs with Python variables for [#19](https://github.com/swar/nba_api/issues/19).

`Endpoint Documentation Generator`
* Updating Endpoint docs with Python variables for [#19](https://github.com/swar/nba_api/issues/19).


# `v1.0.6`
#### 2018-10-11
* Accidentally distributed with DEBUG Mode enabled in `v1.0.5`.


# `v1.0.5`
#### 2018-10-10
* Adding `last_validated_date` to analysis json.

`stats.nba.com`
* Adding _LeagueDashPtStats_ endpoint
* Adding PtMeasureType to parameters
* Updating `missing_parameter_regex` for `Season Year` bug.
* Switching default values in `parameters.py`
  * `LastNGames` from `10` -> `0`
  * `Period` from `1` -> `0`
  * `StartPeriod` from `1` -> `0`
  * `EndPeriod` from `1` -> `0`


# `v1.0.4`
#### 2018-09-25
* Updating description on PyPi 


# `v1.0.3`
#### 2018-09-25
`stats.nba.com`
* Fixed a bug in `find_team_name_by_id()` in static/teams. 


# `v1.0.2`
#### 2018-09-17
`stats.nba.com`
* Added `__all__` to the following file: `nba_api/nba_api/stats/static/__init__.py`


# `v1.0.1`
#### 2018-09-17
`stats.nba.com`
* Added `__init__.py` to the following directory: `nba_api/nba_api/stats/static`


# `v1.0.0`
#### 2018-09-16
* The initial release of `nba_api`.
