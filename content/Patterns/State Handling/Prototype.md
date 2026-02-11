#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=152 ]]
# Intent 
Specify the kinds of objects to create using a prototypical instance and create new objects by copying this prototype.
# Structure
![[Pasted image 20260209002512.png]]

# Applicability
The Prototype pattern is used when a system should be independent of how its products are created, composed, and represented; and
- when the classes to instantiate are specified at run-time, for example, by dynamic loading; or 
- to avoid building a class hierarchy of factories that parallels the class hierarchy of products; or
- when instances of a class can have one of only a few different combinations of state. It may be more convenient to install a corresponding number of prototypes and clone them rather than instantiating the class, each time with the appropriate state.

# Prototype vs. Factory Method
- Use Prototype, when creating an object needs much more time than creating a copy. 
- Don´t use Prototype when the prototypical objects are too big or too numerous and thus use up too much memory.