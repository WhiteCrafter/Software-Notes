#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=170 ]]
# Intent 
Encapsulate a request as an object, thereby letting you parameterize clients with different requests, queue or log requests, and support undoable operations.
**A.K.A**: Action, Transaction

# Structure
![[Pasted image 20260209005749.png]]
# Example
![[Pasted image 20260209005758.png]]

![[Pasted image 20260209005814.png]]

![[Pasted image 20260209005822.png]]
# Applicability
- When objects should be parameterized by an action to perform, as MenuItem objects did above. 
- When requests should be specified, requested, and executed at different times. 
- When an undo should be supported. 
- When changes should be logged, so that they can be reapplied in case of a system crash. 
- When a system should be structured around high-level operations built on primitive operations (macro command).