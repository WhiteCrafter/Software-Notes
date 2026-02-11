#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=176 ]]
# Intent 
Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.
# Structure
![[Pasted image 20260209005913.png]]
# Example
![[Pasted image 20260209005917.png]]
# Applicability
- When more than one object my handle a request, and the handler is not known a priori. The handler should be ascertained automatically. 
- When a request should be issued to one of several objects without specifying the receiver explicitly. 
- When the set of objects that can handle a request should be specified dynamically