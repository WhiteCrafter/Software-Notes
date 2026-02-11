#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=161 ]]
# Intent 
Ensure a class has only one instance and provide a global point of access to it.
## Motivation
The class itself is responsible for keeping track of its sole instance. The class can ensure that no other instance can be created (by intercepting requests to create new objects), and it can provide a way to access the instance.
# Structure
![[Pasted image 20260209002848.png]]

# Applicability
- When there must be exactly once instance of a class, and it must be accessible to clients from a well-known access point.
- When it is impractical or impossible to determine which part of an application creates the first instance. 
- When the sole instance should be extensible by subclassing, and clients should be able to use an extended instance without modifying their code