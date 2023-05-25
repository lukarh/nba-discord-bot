
# NBA Discord Bot

[The NBA Discord Bot](https://github.com/lukarh/NBA-Discord-Bot) is a [Discord](https://discord.com/) [Bot](https://discord.com/developers/docs/intro) developed by me, Lukar! It began as a fun little project for personal use on my own Discord Server since I typically host NBA Watch Parties there and wanted a way for everyone to easily access NBA stats / schedule without having to go to an application or different website. Plus, it's a cool little feature to have on the server for interactivity and engagement purposes, especially with the fake virtual betting feature of the bot (personally not a fan of sports-betting, but people find it appealing so it was a fun little feature to work on for friends to use). Also, I'm a huge NBA Fan/nerd and I enjoy learning how to work with code and data, so I thought to endeavor on this cool little project. A much more fleshed out and popular version of the NBA Discord Bot that the public uses can be found [here](https://github.com/NBABot-Development-Team/NBABot). File Structure is inspired by [Under Ctrl](https://www.youtube.com/watch?v=JEEcbVjLyr0) and the assets directory was inspired by the [NBA Discord Bot](https://github.com/NBABot-Development-Team/NBABot). 

## Code Development
- Coding Language: JavaScript
- Code Editor: [Visual Studio Code (VSCode)](https://code.visualstudio.com/)
- Relies on NBA Live API Endpoints:  
  -  https://cdn.nba.com/static/json/staticData/scheduleLeagueV2_1.json
  -  https://cdn.nba.com/static/json/liveData/odds/odds_todaysGames.json
  -  https://cdn.nba.com/static/json/liveData/boxscore/boxscore_{gameID}.json
  -  https://cdn.nba.com/static/json/liveData/scoreboard/todaysScoreboard_00.json

### File Structure
- **src/assets/..:** Contains .json mappings of names to emojis, colors, ids, tricodes, etc.
- **src/commands/{commandName}Folder/{commandName}.js:** Contains the logic for available bot commands that users can use and categorizes them
- **src/events/..:** Contains the logic that allows for the bot to listen and respond to specific events that occur in the Discord Server with the bot
- **src/handlers/..:** Contains the logic that handles all the events in the events folder
- **src/utils/..** Contains the logic for various functions that need to be reused throughout the directory

## Current Features on Version 1.0.1

- Automatic Features
  - sendDailyScoreMessage.js: Sends a msg for every game to the NBA Live Games Channel every 24 hours

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/857d7334-529c-49b5-8727-f685fb727fed)
  - updateGameMessage.js: Updates the NBA Live Games Channel with scores every minute

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/29d7f0a0-b6fb-4050-8a0b-79cbb84aa810)
- User Commands
  - **/available-game-bets**: Shows the user a list of the betting status for available NBA games.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/5d8b770d-be02-446e-aa61-7549216b35b5)
  - **/bet-east** [team-name] [amount] [game-id]: Allows the user to bet on an Eastern Conference Team to win a specific game.
  - **/bet-west** [team-name] [amount] [game-id]: Allows the user to bet on a Western Conference Team to win a specific game.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/d3dc3d89-7b32-4c56-8b1b-ae91f0c2d434)

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/813920b0-1596-4562-a05b-2bdaf8e2eab7)
  - **/bet-help**: Shows a list of available game bet commands

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/f77fbc22-5eab-4d0e-a7d8-26cc2da75a70)

  - **/balance** [optional-user]: Checks the balance of a current user or themselves

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/3344966e-e3af-4f32-aa15-ce2efac163af)
  - **/cancel-bet** [game-id]: Cancels a bet a user has made for a specific game if permitted.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/47c87879-8e50-40aa-8909-10958662669d)

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/8a239e51-093d-4d16-93d6-abe7510da8c7)
  - **/daily**: Allows the user to collect free daily money.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/e178c21c-bc9d-49cf-874c-8246776f3a88)
  - **/edit-bet** [amount] [game-id]: Edits a bet a user has made for a specific game if it permits.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/9a0086f3-768a-491c-b264-cb4463ab967a)

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/683788a0-d1af-451e-b0fe-b3addecc55b3)
  - **/signup**: Allows the user sign-up to create a profile to make virtual bets on games.

![image](https://github.com/lukarh/NBA-Discord-Bot/assets/65103724/1681a79d-89b2-4517-8d34-eda3cec33b6f)

## Change Log
1.0.0 - Initial Release of NBA Discord Bot. Bot can be ran locally when the user is online with their computer.

1.0.1 - Simplified / Reorganized code in utils.

1.1.0 - Introduced new betting feature, claim-bet feature yet to be implemented.

## Available Local Scripts

In the project directory, you can run:

### `node src/index.js`

Runs the bot/file locally, but does not restart the bot automatically when any saved file changes are made in the directory

### `nodemon`

Runs the bot locally and restarts the bot automatically when any saved file changes are made in the directory. This works because package.json has already defined "main": src/index.js

## Not Included 
- .env
  - TOKEN (Access to Bot)
  - GUILD_ID (Server ID)
  - CLIENT_ID 
  - NBA_GAME_CHANNEL_ID (Channel ID to update Game Scores Channel with)
 
- config.json