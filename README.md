# PRD4-Prototype
PRD4 Prototype of Shadows Over Suburbia 
Full Project Here: https://github.com/mstrykul1336/Shadows-Over-Suburbia-Prototype-
Play: https://mstrykul1336.github.io/PRD4-Prototype/
Tasks:
Fix attack system and get it working.
Fix health UI to display properly 
Make it so players leave the lobby (because winning and voting both rely on the playerList from photon and I don't want to go in and try to change that. It's easier to just force the player out of the game so that it doesn't count them. Eventually they'll get to drop a death note though so at least they'll contribute something if they die.)
Implement chat box with being able to disable it for spectating players (if that's the way I go) and disable the chat box at night cycle.
Make sure voting runs smoothly (I think currently it needs time for votes to be counted before immediately voting out a player and needs to check if someone has equal votes). I think I also want to change it so voting doesn't happen on the first day cycle. Just start the game and give the players 30ish seconds to read their role and get used to their abilities. Then go to night cycle, then when day happens again, voting will start. 
Add in basics for character names, assigning characters at random and debugging in what abilities you get as that character.
Add in debug for what abilities you get as each role. 
Backlog:
Add shop and coin system. (This will require I add items too)
Add options to menu screen.
Add in neutral character side for OldMan character. 

What was done: 
- Fixed health UI, now players have separate health UI and can't see other health. (Still buggy)

- Removed RoleAssigner script and moved its contents to Game manager. This was to fix a problem with player controllers not receiving role information, therefore everyone was given the same health. Now health works properly per role, so each role accurately has the health they're supposed to. 

- Fixed attacking so now everyone has a separate attack UI, drop downs properly fill with players, and players can attack up to one other player. Drop-down makes sure not to include yourself. It still seems a little buggy though.

- Added a day counter at the top so you can see what day you're on. 

- Added a 30 second intermission for day 0, then it goes directly to night cycle. No voting needed if you don't know who to vote for! Voting starts at normal on day 1. 

- Voting now accounts for extra time to collect votes (30 seconds) and if there is a tie. If there is a tie, it will restart voting. It also makes sure players can only vote once. 

- The shop has arrived! Spend that hard earned gold on some items (currently just one for proof of concept)! Items will run out after a certain number of purchases! Don't read the fine print about items not currently doing anything. Walk by the shopkeeper and hit F to open the shop! Hit it again to close it.

- Want to admire those items you just bought? Hit I and open up that inventory of yours!

- I want to still add characters but I feel that's more of a formal element. Not required for the game loop. I will be adding these in vertical slice. 

- Abilities exist now! Just...in the debug, but they get assigned! Not all abilities are thought of yet tho so they're not all there.
- It tries to force the player out of the lobby, but sometimes it works and other times it doesn't. I think it has to do with who is the master client, even though I have it set to change master client to someone else if the master client was killed. 
