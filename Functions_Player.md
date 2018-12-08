---
menu: Player 
tab: false
parent: Functions.md
weight: 1
---

# Player Functions
<br/><br/>
All Below Functions only work being called on authority.
All Below Functions only work with players registered with the system.
<br/><br/>
### Set Player Move Badge
![Alt text](Image/Func_SetPlayerMoveBadge.png?raw=true "ManagerNode")
<br/><br/>
Set Player Move Badge Allows you to set if a player is able to move there badge 
on the character select system.
A good example of using this is when a player wants to lock in there character, you would disable 
there movement, but not input incase you wanted them to be able to back out or cancel.
<br/><br/>
### Get Player Move Badge
![Alt text](Image/Func_GetPlayerMoveBadge.png?raw=true "ManagerNode")
<br/><br/>
Get Player Move Badge returns a bool letting you know if this player is able to move there
badge.
<br/><br/>
### Set Player Input Badge
![Alt text](Image/Func_SetPlayerInputBadge.png?raw=true "ManagerNode")
<br/><br/>
Set Player Input Badge Enables or Disables if a player is able to send any input too the system at all,
this includes Moving, Interacting and canceling.
A good example of use for this is when you want to pause a player's ability to interact at all, say players
where taking turns picking there character.
<br/><br/>
### Get Player Input Badge
![Alt text](Image/Func_GetPlayerInputBadge.png?raw=true "ManagerNode")
<br/><br/>
Get Player Move Badge returns a bool letting you know if this player is able to send input to the 
character select system to move there badge or input / cancel.
<br/><br/>
### Get Player Input Badge
![Alt text](Image/Func_GetPlayerBadgeNumber.png?raw=true "ManagerNode")
<br/><br/>
Gets the Players assigned badge number, you can consider this the Player Order number, used for things
like Player 1, Player 2 etc, or you can use your own system.
<br/><br/>
### Set Player Character States
![Alt text](Image/Func_SetPlayerCharStates.png?raw=true "ManagerNode")
<br/><br/>
Allows you to a players character states, a good example of use of this would be if you wanted
to load a list of characters the player has unlocked.
<br/><br/>
### Get Player Character States
![Alt text](Image/Func_GetPlayerCharStates.png?raw=true "ManagerNode")
<br/><br/>
Gets the Players Character states.
<br/><br/>
