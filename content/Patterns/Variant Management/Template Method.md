#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=124 |chap 3.3 - page 124 ]]
# Intent 
Define the skeleton of an algorithm in an operation, deferring some steps to subclasses. Template Method lets subclasses redefine certain steps of an algorithm without changing the algorithm´s structure.
# Structure
![[Pasted image 20260208233137.png]]
# Example
![[Pasted image 20260208233147.png]]

# Applicability
- To implement the invariant parts of an algorithm once and leave it up to subclasses to implement the behavior that can vary. 
- When common behavior among subclasses should be factored and localized in a common class to avoid code duplication. 
- To control subclasses extensions. For example, define a template method that calls “hook” operations at specific points, thereby permitting extensions only at those points.