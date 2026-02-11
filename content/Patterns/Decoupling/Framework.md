#software/designpatterns/patern 
# Intent
Provide a (nearly) complete program that contains planed “empty spaces”, which can be extended to form a complete program. It contains the complete application’s logic, mostly the main program. The user can build subclasses from some classes, overwrite certain methods or implement pre-defined abstract methods. The framework is designed so that it calls the user-defined extensions correctly.

# Example
A drawing framework has a class Graphic and some subclasses *Line, Rectangle, Ellipse,* etc. The user may add new subclasses, e.g. *Square* or *Icon*, but he must define a ***draw*** method in this new subclass.
The framework ensures the correct creation, positioning, moving, saving, etc. of the objects of the new classes.

![[Pasted image 20260208230410.png]]
## Conventional System Structure
- Vendor provides libraries,
- Programmer writes main program and applicantion's logic
![[Pasted image 20260208230553.png]]
# Framework (principle)
A Framework follows the "Hollywood-Principle":
`"Don't call us - we'll call you".` The main program already exists and calls programmer-defined extensions.

# Applicability 
-  When a base version of the application should work without extensions.
- When extensions should be possible with consistent behavior(application's logic in framework).
- When a new implementation of the Application's Logic should be avoided
The patters **[[Factory Method]], [[Abstract Factory]], and [[Template Method]]**  are often used in Frameworks

 