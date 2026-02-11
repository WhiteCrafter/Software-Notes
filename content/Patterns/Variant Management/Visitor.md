#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=118]]
# Intent 
Represent an operation to be performed on the elements of an object structure. Visitor lets you define a new operation without changing the classes of the elements on which it operates.
# Structure
![[Pasted image 20260208232355.png]]
# Example
![[Pasted image 20260208232359.png]]
![[Pasted image 20260208232410.png]]
## Example for an abstract syntax tree
![[Pasted image 20260208232428.png]]
# Applicability
- When an object structure contains many classes of objects with differing interfaces, and operations on these objects that depend on their concrete classes should be performed.
- When many distinct and unrelated operations need to be performed on objects in an object structure, and “polluting” their classes with these operations should be avoided. 
- When classes defining the object structure rarely change, but often new operations over the structure are defined
- When several developers wish to extend the object structure simultaneously with several sets of operations