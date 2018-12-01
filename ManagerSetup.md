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
<br/><br/>
A ideal place to do this would be the game mode.

##### Creating your Character Select Manager Settings
Right click anywhere in the content browser that is not on an asset under misscellaneous you should see 
a data asset choose this class.
<br/><br/>
![Alt text](Image/CreateDataAsset.png?raw=true "ManagerNode")
<br/><br/>
Next you will see a Data picker window open, search and find CSP_DisplaySettings then click select.
This will then create a data asset in your content browser, you will now be able to select this from the
drop down class list in the function Setup Character Select Manager.
<br/><br/>
![Alt text](Image/DataAssetPick.png?raw=true "ManagerNode")
<br/><br/>
More details on Display Settings class later on.
## Setting up the Manager Component
The display Settings is a data asset that helps to define how your Character Select system will act
and how the rules for it will be defined. First we need to create a data asset for the display class.

The Manager component is a communcation system that is used to communicate with the character
Select System, allowing you to register players and send input.

The Manager is used Primarily internally for multiplayer support.
<br/><br/>
![Alt text](Image/ManagerComponent.png?raw=true "ManagerNode")

Use the Add Component drop down button(big green button top left) in your player controller 
too add a CSP Manager.

## Registering the Player

To register a player to be able to interact with the character select widget
you must call a function from the Manager Component called RegisterPlayer.

Note: if a player tries to send an action to the Character Select System 
with out first registering, the input will fail and you will recieve an error 
in your log.


<br/><br/>
![Alt text](Image/RegisterController.png?raw=true "ManagerNode")


Multiplayer note: When registering your system make sure to do this on the server
side.