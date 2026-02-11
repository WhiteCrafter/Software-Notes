---
aliases:
  - Robust Iterator
  - Enumeration
---
#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=63]]
# Intent 
Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation.
**Also Known As:** Robust Iterator  Enumeration

# Structure
![[Pasted image 20260208175323.png]]
# Example
![[Pasted image 20260208175348.png]]

## Example Application

![[Pasted image 20260208175809.png]]
## Implementation in Java(1)
![[Pasted image 20260208175830.png]]![[Pasted image 20260208175852.png]]

# Applicability
- To access and aggregate object's contents without exposing its internal representation.
- To support multiple traversals of aggregate objects (a "robust" iterator allows multiple traversals)
- To provide a uniform interface for traversing different aggregate structures( that is, to support polymorphic iteration).