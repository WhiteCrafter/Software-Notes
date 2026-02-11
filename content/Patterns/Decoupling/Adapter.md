#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=89]]
# Intent
Convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn't otherwise because of incompatible interfes
**A.K.A** Wrapper
# Structure
![[Pasted image 20260208221006.png]]
![[Pasted image 20260208221011.png]]
# Example
![[Pasted image 20260208223341.png]]
# Applicability
- When an existing class should be used, and its interface  does not match the one you need.
- When a  reusable class should be created that cooperates with unrelated or unforeseen class should be created that cooperates with unrelated or unforeseen classes that don't need necessarily have compatible interfaces.
- (object adapter only) When several existing subclasses should be used, but it's impractical to adapt their interface by subclassing every one. An object adapter can adapt the interface of its parent class.

 