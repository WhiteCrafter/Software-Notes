#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=102|Chap 3.3  -  page102]]
# Intent 
Provide a structure for systems that operate on date flows. Every operation step is encapsulated in a filter component. Data is transmitted via pipes. To build new systems create a new combination of filters.
**A.K.A**: Data Flow, Pipes and Filters

# Structure  
![[Pasted image 20260208225438.png]]
# Example: Compiler
![[Pasted image 20260208225451.png]]
# Applicability
- When a system operates on, or transforms, data flows and a system of a single component is not customizable. 
- When in future development some components will be replaced or the operational order will be changed. 
- When smaller components can be reused in other systems.
- When some components should run in parallel or quasi parallel

