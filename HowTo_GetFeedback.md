---
menu: GetFeedbackFromWidget 
tab: false
parent: HowTo.md
weight: 2
---
# How to get feedback from the widget

The system uses a EventDispatcher[Delegate] to give the server feedback on what the users are reqesting to do.
This means that you can set the EventDpisatcher bind up to where ever you want to give you full
flexability.
When ever a user attempts some sort of input it will fire the function you are bond too
with a payload of information about what is going on, you can then decide from there what you
choose to do.
### Creating the Function to bind too
The signature for the function is as follows:
<br/><br/>
(a signature is the type of paramaters a function uses, they must be in the correct order)
```
StateWrapper[FCPS_StateWrapper] - struct
Action[ECSP_Action] - Enum
Controller[AController] - Controller
```
![Alt text](Image/Feedback_Sig1.png?raw=true "ManagerNode")
![Alt text](Image/Feedback.png?raw=true "ManagerNode")
<br/><br/>
### Binding
To bind our created function too the widgets feedback system is pretty easy.
Search for the BindDisplayFeedback function, drag off the red input pin and search
for create event.
<br/><br/>
Once you have the create event pin on the graph if your function is setup with the 
correct signature you should be able too see it in the drop down menu for create
event, select it.
<br/><br/>
Now when ever i use trys to interact or cancel this function will fire and give you a 
payload of information for you to use.
note: only bind feedback on authority.
<br/><br/>
![Alt text](Image/BindFeedback.png?raw=true "ManagerNode")