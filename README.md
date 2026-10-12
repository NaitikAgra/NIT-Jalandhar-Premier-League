# NIT-Jalandhar-Premier-League
Build a small web auction for the NIT Jalandhar Premier League (JPL).
Players are already loaded. Do not build a screen to add or edit players. Four team managers bid. One auctioneer
accepts or rejects. An accepted bid removes the player from the auction and adds them to that team.
Roles
Role What they can do
Auctioneer Start the auction for one player, see bids, accept one bid or reject the round
Team manager There are exactly 4. Each can place a bid on the player currently up for auction
Anyone else Can only view the auction and the team rosters
Use a simple login, or a role picker on the first screen. Do not build signup, password reset, or real authentication.
Player data
Preload at least 12 players. Each player has:
◆ Name
◆ Skill: batting, bowling, or both
◆ Base price
◆ Status: available, in auction, or sold
What to build
1. Auction board. Show players still available. Show the player currently in auction, their base price, and the bids
so far.
2. Bid. A team manager enters an amount. The amount must be greater than the base price and greater than the
current highest bid. A team cannot bid twice in a row if it already holds the highest bid.
3. Auctioneer actions. Accept the highest bid, or reject the round. Accept assigns the player to that team, removes
the player from the available list, and shows them on that team's roster. Reject leaves the player available.
4. Rosters. Each team has a name, a budget, and a list of players bought with the price paid. Buying a player
reduces that team's remaining budget. A bid higher than the remaining budget is rejected.
5. Responsive UI. The board, the bid box, and the rosters must be usable on a phone and on a desktop.
Out of scope
Do not build player upload, payments, notifications, chat, or a timer. One auction at a time is enough.
Suggested build order
1. Data model and preloaded players and teams.
2. API for list players, place bid, accept, reject, and list rosters.
3. Auctioneer screen and team-manager screen.
4. Budget check and error messages.
5. Tests for bid rules and for accept moving the player onto the roster.

Data to store
◆ Team: id, name, total budget, remaining budget
◆ Player: id, name, skill, base price, status, sold price, team id
◆ Bid: id, player id, team id, amount, time
Use a database or a JSON file. Either is fine if the data survives a server restart.
Frontend framework and backend language are your choice. Follow normal project structure, handle errors with a
clear message, and keep the code readable.
