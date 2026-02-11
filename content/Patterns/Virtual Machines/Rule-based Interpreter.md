#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=195 ]]
# Intent 
Solve a Problem using a set of rules. A rule consists of a condition part and an action part. If the condition evaluated on a set of data elements in the working space returns true, then the action part can be executed. The action part replaces or removes data elements which have been selected in the condition part, or adds new data elements.
**A.K.A**: Rule-Based (Expert-) System

# Structure
![[Pasted image 20260209011934.png]]
# Selecting Rules
If more than one rule can be applied, the selection of a rule is done by the the following steps: 
1. A rule may only be applied once to a given data element in the working space. 
2. If several rule-data element combinations are applicable, then select those that operate on the youngest data elements.
3. Select the rules with the highest “specificity”, i.e., those whose conditions need the most elements of the working space. 
4. Select a rule a) in order of specification or b) randomly.
# Applicability
- When the solution of the problem is best formulated as a set of condition-action-rules (for example, diagnosis problems, matching problems). 
- When the action part only executes simple operations on the data elements (no loops, no recursion, no procedure calls to modify the working space).