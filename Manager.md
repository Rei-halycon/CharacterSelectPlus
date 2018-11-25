---
menu: SettingUpTheSystem 
tab: true
---

# Setting up the System

## Setting up the Manager
<br/><br/>
The manager node(as seen below) Is a function you can call anywhere, the first thing you
do when setting up this system is to call Setup Character Select Manager, this spawns the
background handling system, there should only ever be one of these.

Multiplayer Note: If your game is not standalone(SinglePlayer) make sure to spawn this
from your Authoritative client(dedicated server, listen server)
<br/><br/>
![Alt text](Image/ManagerNode.png?raw=true "ManagerNode")

A ideal place to do this would be the game mode.

## Setting up the Manager Component

The Manager component is a communcation system that is used to communicate with the character
Select System, allowing you to register players and send input.

The Manager is used Primarily internally for multiplayer support.
<br/><br/>
![Alt text](Image/ManagerComponent.png?raw=true "ManagerNode")

Use the Add Component drop down button(big green button top left) in your player controller 
too add a CSP Manager.