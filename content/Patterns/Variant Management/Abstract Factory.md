#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=141]]
# Intent 
Provide an interface for creating families of related or dependent objects without specifying their concrete classes.
**A.K.A** Kit
# Structure
![[Pasted image 20260208234954.png]]
# Example
![[Pasted image 20260208235005.png]]

![[Pasted image 20260208235021.png]]
# Applicability
- When a system should be independent of how its products are created, composed, and represented. 
- When a system should be configured with one of multiple families of products. 
- When a family of related product objects is designed to be used together, and there is a need to enforce this constraint. 
- When a class library of products should be provided, and just their interfaces should be revealed, not their implementations.
# Builder vs. Abstract Factory
Abstract Factory is similar to Builder in that it too may construct complex objects. The primary difference is that the Builder pattern focuses on constructing a complex object step by step. Abstract Factory´s emphasis is on families of product objects (either simple or complex). Builder returns the product as a final step, but as far as the Abstract Factory pattern is concerned, the product gets returned immediately.