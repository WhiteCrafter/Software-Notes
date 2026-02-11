#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=135 ]]
# Intent 
Separate the construction of a complex object from its representation so that the same construction process can create different representations.
# Structure
![[Pasted image 20260208234439.png]]
# Example
![[Pasted image 20260208234445.png]]

# Applicability
- When the algorithm for creating a complex object should be independent of the parts that make up the object and how they´re assembled. 
- When the construction process must allow different representations for the object that's constructed.
# Collaborations
- The client creates the Director object and configures it with the desired Builder object. 
- Director notifies the builder whenever a part of the product should be built. 
- Builder handles requests from the director and adds parts to the product.
- The client retrieves the product from the builder.

# Builder vs Factory Method
Builder separates the construction algorithm and the interface for building the individual parts (Director and Builder classes). Thus, it is possible to vary the construction algorithm dynamically
