#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=165 ]]
# Intent 
The Blackboard architectural pattern is useful for problems for which no deterministic solution strategies are known. In Blackboard several specialized subsystems assemble their knowledge to build a possibly partial or approximate solution.
# Structure
![[Pasted image 20260209003750.png]]
- ==Simple Form==: Control activates all knowledge sources sequentially.
- ==Complex Form==: Checks a set of applicable knowledge sources (with ***`execCondition()`***), chooses one, and executes it.
# Example
![[Pasted image 20260209004818.png]]
# Applicability
- When several transformations (“knowledge sources”) operate on a common data structure (“blackboard”). 
- When triggering the transformations is controlled by the contents of the data structure. 
- When the selection of the applicable transformation should be controlled