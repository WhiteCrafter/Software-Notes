#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=207 ]]
# Intent 
Provide a surrogate for another object that shares the same interface but does nothing. The Null Object encapsulates the implementation decisions of how to “do nothing” and hides those details from its collaborators.
## Motivation
Avoid cluttering up code with tests for null values like 
```
if (thisCall.callingParty != null) 
	thisCall.callingParty.action() 21
```
# Structure
![[Pasted image 20260209015940.png]]
# Example
![[Pasted image 20260209015946.png]]
# Applicability
- When an object requires collaborators and one or more of them should do nothing. 
- When clients should be able to ignore the difference between a collaborator which provides real behavior and that which does nothing. 
- When the do-nothing behavior should be reused so that various clients which need this behavior will consistently work the same way