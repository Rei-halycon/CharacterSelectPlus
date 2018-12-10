---
menu: CharacterLayerStates 
tab: false
parent: Info.md
weight: 1
---

# The Layer State System
<br/><br/>
### The Layers

>Layer 4 | Development Character States, an extra layer used to override everything.
<br/><br/>
Layer 3 | Global Character States, Useful for banning, gamemode etc.
<br/><br/>
Layer 2 | Live Character States, that can be set by the Authority, apply to everyone.
<br/><br/>
Layer 1 | Player Character States, these only apply too the player.
<br/><br/>
>Layer 0 | everything is assumed to be available for selection.
<br/><br/>

### Priority 
<br/><br/>
By default the system assumes everything is avalaible, and respects the layering order, what this 
means is that the highest layer is the final state, layers do not have to contain data they can 
be empty, this just assumes that the character for that layer is avalaible. 

The system will ignore any empty layers that it checks after it has found a state, this means that if 
you have a character in say the global character state set to disable, then the development character 
state which is empty will not return it as avalaible.  