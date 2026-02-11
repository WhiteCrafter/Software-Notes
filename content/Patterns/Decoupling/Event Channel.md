#software/designpatterns/category 
[[Chap3.3DesignPatternTurorial.pdf#page=104]]
# Intent
Decouple participants of a system completely so that they can work independently, and do not know anything about the existence or number of other participants. Interactions are transmitted as events.
# Structure
![[Pasted image 20260208225958.png]]
The participants register at the event channel about which events they want to be informed. When a participant sends an event to the event channel, it resends this event to registered participants. 
# Example
![[Pasted image 20260208230015.png]]
When the editor saves a file, it generates an event which causes the compiler to start and the class browser to update its display of classes.