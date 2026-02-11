#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=156 ]]
# Intent 
Use sharing to support large numbers of fine-grained objects efficiently.
# Structure
![[Pasted image 20260209002705.png]]
# Example
![[Pasted image 20260209002717.png]]
- The characters themselves can be represented by a character code (intrinsic state). 
- The information about font, size, and position can be externalized (extrinsic state) and placed into the row or column object, or subsequences of characters. Font and size need not be stored in every character object but can be looked up in their container. The position of each character can be computed from the position of the container, as necessary
# Applicability
The Flyweight pattern’s effectiveness depends heavily on how and where it is used. Apply the Flyweight pattern when all the following are true: 
- An application uses many objects. 
- Storage costs are high because of the sheer quantity of objects. 
- Most object state can be made extrinsic and applies to many objects at once, or intrinsic state is heavy-weight and can be reused. 
- Many groups of objects may be replaced by relatively few shared objects once extrinsic state is removed. 
- The application doesn’t depend on the identity of flyweights.