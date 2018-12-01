---
menu: LoadingDisplay 
tab: false
parent: Setup.md
weight: 3
---
# Loading the Display
In this section we will cover how to load your character data and populate your
character select widget.


## Populating the display with data

To propergate information through the system this is very easily achieved, we do this by sending a payload of data
which is an array of Wrappers that hold all relative information about a character for the system, lets take a look
at the structure.
#### CharacterData Structure
<br/><br/>
![Alt text](Image/CharDataStruct.png?raw=true "ManagerNode")
<br/><br/>
Name: This will be the display name that might be diplayed on the Display widget if you desire.
Identifier: This is how you keep track of characters, this could be a String, or a string containing a Id number like an
int, or even reference to a data table, anything you really want that you can convert too a string.
Icon: The display icon for the slot, this can be Image, Material or Material instance. 

Advanced features:
 coming soon..

#### Load Character Select Node

Its very simple to load the character select, all you need to do is create an array of these structures with your character
data populated inside them, so it would be helpful to make your self some form of helper function, something that takes in 
the type you are using to store your character data and outputs a CSP_CharacterData Structure.
<br/><br/>
![Alt text](Image/LoadCharacterSelect.png?raw=true "ManagerNode")
<br/><br/>

Once you fire this function to populate your Character Select Display, It will also cause all players who are registered for input
to have there badges be created and are given input & movement access too the system, ofcourse if you dont want that you can call functions
afterwards to disable/hide there badges.