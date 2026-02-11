#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page= 148]]
# Intent 
Without violating encapsulation, capture and externalize an objects´s internal state so that the object can be restored to this state later.
**A.K.A**: Token

# Structure
![[Pasted image 20260209002250.png]]

# Example
![[Pasted image 20260209002259.png]]

# Applicability
- When a snapshot (some portion of) an object's state must be saved so that it can be restored to that state later, and
- when a direct interface to obtaining the state would  expose implementation details and break the object's encapsulation.