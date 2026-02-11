#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=22]]
# Intent 
Represents part-whole hierarchies (aggregates). Composite lets clients treat individual objects and composites of objects uniformly.
## Motivation
Part-whole hierarchies occur whenever complex objects are modeled, e.g. file systems, graphics applications, word processing, CAD, CIM, ... . In these applications, primitive objects are combined into groups which may again be combined to form still larger groups. Often, client programs wish to treat primitive and composite objects (aggregates) uniformly. The composite pattern factors out the common aspects of both primitives and aggregates into a common superclass.
# Structure
![[Pasted image 20260208235352.png]]
# Example
![[Pasted image 20260208235345.png]]

# Implementation
1. It is often useful to maintain a parent reference in each component (simplifies traversal). 
   Of course, the parent reference must point to the true parent. This invariant can be maintained by the ***add*** and ***remove*** operation for composites.
   Sharing components causes multiple parents (ambiguity)
   ![[Pasted image 20260208235505.png]]
2. Maximize the Component Interface 
   The component Interface should define as many common methods of containers and leaves as possible, to ensure transparency.
   When container methods are defined for all components:
   ***getChild*** should return nothing for leaves -this can be the default implementation in component.
   ***addChild*** and ***removeChild*** should fail for leaves(return an error or generate and exception).
3. Storing children
   arrays. lists, hashtables - choice depends on efficiency. 
   For fixed set of children, use explicit variables(and specialized ***add/remove/getChild*** operations).
   Children may also have to be maintained in a specific order(for instance, for layout managers).

   