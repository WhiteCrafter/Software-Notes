#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=83]]
# Intent 
Decouple an abstraction from its implementation so that the tow can vary independently

**A.K.A** Handle/Body

# Structure
![[Pasted image 20260208215835.png]]
# Example
![[Pasted image 20260208215857.png]]
![[Pasted image 20260208215910.png]]
# Applicability
- When a permanent binding between abstraction and its implementation should be avoided
- When both abstraction and implementation should be extensible by subclassing
- When changes in the implementation should have no impact  on clients.
- When the implementation should be hidden completely from clients (C++: representation visible in class interface)
- When a Large number of classes should be avoided (see example)
- When an implementation should be shared  among multiple objects
- (two-levels with subclassing on both levels)
