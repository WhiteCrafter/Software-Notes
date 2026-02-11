#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=191 ]]
# Intent 
Given a language, define a representation for its grammar along with an interpreter that uses the representation to interpret sentences in the language. A context provides values for variables or other information needed for interpretation.
# Structure
![[Pasted image 20260209011202.png]]

# Applicability
When there is a language to interpret, and phrases in the language can be represented in the language as abstract syntax trees. The interpreter pattern works best when 
- the grammar is simple. For complex grammars, the class hierarchy for the grammar becomes large and unmanageable. Tools such as parser generators are a better alternative in this case. 
- efficiency is not a critical concern. The most efficient interpreters do not interpret the input directly but first translate it into a more compact form that is faster to traverse. The translation can also be done by an interpreter. 

# Interpreter vs. Composite vs. Visitor
- Interpreter and composite share the same structure. One speaks of an interpreter, when sentences in a language are represented and evaluated. In particular, the method interpret() usually returns a value that is the result of evaluating and combining all sub-components. One does not normally consider a parts hierarchy as a sentence in a language to be interpreted. Thus, the interpreter can be viewed as a special case of composite. 
- Rather than placing the method interpret() into every subclass, one can collect them into a visitor.