#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=204 ]]
# Intent 
Provide a unified interface to a set of interfaces in a subsystem. Facade defines a higher-level interface that makes the subsystem easier to use.
# Structure
![[Pasted image 20260209015825.png]]


# Applicability
- When you want to provide a simple interface to a complex subsystem. A facade can provide a simple default view of the subsystem that is good enough for most clients. 
- When there are many dependencies between clients and the implementation classes of an abstraction. The introduction of a facade decouples the subsystem from clients and other subsystems, thereby promoting subsystem independence and portability. 
- When you want to layer your subsystems. The facade is used to define an entry point to each subsystem level.