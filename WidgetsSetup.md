---
menu: SettingUpTheWidgets 
tab: false
parent: Setup.md
weight: 2
---

# Setting up the Widgets

## Setting up the Character select Display Widget

We need to first start by creating our Primary foundation widget, this would be
our display system for showing the Character Select System.
<br/><br/>
![Alt text](Image/CreateDisplay.png?raw=true "ManagerNode")
<br/><br/>
Right click anywhere in the content browser and choose new blueprint,  if you type in CSP
this will filter in all the Character Select Plus classes, if you scroll down too the 
bottom a little, you should see the widgets.
We want to create a CSP_Display.

You will notice that if you open the widget up, it will be blank like any normal user created
widget. You can basically do anything you want in here, the system is built to be designer friendly.
However if you press compile you will notice the BP compiler will throw a fit asking for a UGridPanel 
called DisplayGrid.
<br/><br/>
![Alt text](Image/DisplayCompileFail.png?raw=true "ManagerNode")
<br/><br/>
This "DisplayGrid" is the container that will be displaying your Character Slots, it needs to be created by 
the user manually, this is very easy, this is called Widget binding.
<br/><br/>
![Alt text](Image/DisplayGridDrop.png?raw=true "ManagerNode")
<br/><br/>
Search your Pallete for a Grid Panel, the pallete is located in the top left corner of your UMG Widget.
Drag and drop this on too your root widget.(Note for designers, this does not have to be the root widget, can go
virtually anywhere and can even be the root its self!)

The next step is too rename the widget to DisplayGrid once you have done this, if you try and compile it should not
throw any errors!
<br/><br/>
![Alt text](Image/DisplayGridCompile.png?raw=true "ManagerNode")
<br/><br/>

## Setting up the Character Display Slot Widget

Now that we have setup the main display, we need to setup our Slots for displaying our character information.
Once again create another blueprint class from the content browser, but this time we want to choose a 
CSP_Slot as the class.
<br/><br/>
![Alt text](Image/SlotCreate.png?raw=true "ManagerNode")
<br/><br/>

Once again if we open this widget up and try to compile it we get a compiler error, it will throw an error asking for
a Image Widget called "CharacterIcon" this is the only required widget for the slot, it can go anywhere and be wrapped 
in anything.

Drag a image widget in too your canvas and name it "CharacterIcon", when you compile you should get no errors.
<br/><br/>
![Alt text](Image/SlotExample.png?raw=true "ManagerNode")
<br/><br/>
Here is an example of what it could look like for a basic slot.
<br/><br/>
(Note: will cover a full explination of how to setup a general type of slot to work correctly, with all UMG settings later on)

## Setting up the Badge Widget

Finally once again create another blueprint class, select CSP_Badge and create it, open the badge up and this will also request a
widget bind for Image called "BadgeIcon" add the Image too your canvas and name it "BadgeIcon", it will look something like this.
<br/><br/>
![Alt text](Image/BadgeIcon.png?raw=true "ManagerNode")
<br/><br/>

## Assigning our Slot & Badge class to our system

The system is setup so you may use different types of Slot & badge type Style classes, so we are going to assign these classes
to our display widget. Start by opening up your Display Widget you created.
Open trhe Graph tab on the top right, and in your variable details panel bottom left, find or search for class or CSP display 
this should bring up the Slot & badge class, this is where you can assign what widgets to use.
<br/><br/>
![Alt text](Image/DisplayClassAssign.png?raw=true "ManagerNode")
<br/><br/>

This now gives us all the basic widget setups, however this does not include styling & visual setup for things like 
slot states, Normal, Disabled, taken etc. Neither does this include setting badges up for players, but this is the 
bare minium we will cover these other things later on.