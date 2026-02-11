#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=31  ]]
# Intent 
Define a family of algorithms, encapsulate each one, and make them interchangeable. Algorithms can vary independent of clients that use them.
**A.K.A** Policy
## Motivation
Sometimes algorithms need to vary, depending on size of data, performance required, or type of data.

# Structure
![[Pasted image 20260209001000.png]]
# How to use 
![[Pasted image 20260209001013.png]]

# Example

# Applicability
- When several classes differ only in their behavior. Strategies can configure a class with one of many behaviors. 
- When different variants of algorithms are needed, e.g. reflecting different space/time/quality tradeoffs. 
- When algorithm-specific data structures can be hidden. 
- Switchless programming: When a class defines many behaviors as multiple conditional statements or switches. Move related branches into their own strategy class. Then the code for every single case is contained in a single class, which results in a cleaner design. Also, the classes for the cases can be worked on independently
  ![[Pasted image 20260209001101.png]]
- Alternative to ==strategy==: subclass the class Context: One can subclass Context directly to obtain different behaviors. 
- This results in many classes that only differ in behavior and the behavior is fixed for each class. 
- ==Strategy==, on the other hand, factors out only the behavior, and allows dynamic change of behavior