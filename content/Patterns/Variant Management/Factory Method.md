#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=128]]
# Intent 
Define an interface for creating an object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses. Alternatively, the factory method decides which subclass to instantiate.
**A.K.A** Virtual Constructor
# Structure
![[Pasted image 20260208233417.png]]
# Example
Assume, Archi is a framework for planning buildings. It contains a class Building, which contains a ***construct*** method. This method is an interactive program to create a plan for a new building. 
It is allowed for users to implement subclasses of Building. These subclasses must implement the abstract methods ***createWall, createRoom, createDoor, createWindow***. 
Problem: How does the user tell the name of the subclasses to the Framework?

![[Pasted image 20260208233533.png]]

Solution 1: Pass the class name School as character string and transform it to the corresponding class. 
	in Java: ***`Class.forName(String name)`***
```java
construct() { 
	String className = fetchClassName() 
	// fetchClassName reads from a manifest 
	// or uses a parameter, or asks interactively 
	bldg = Class.forName(className).newInstance(); 
	//above is deprecated because of exceptions. Better: 
	Class.forName(className).getDeclaredConstructor().newInstance() 
	bldg.construct(); 
	... 
}
```

Solution 2: Subclasses of Building are pre-determined in the Framework; parameterize ***`construct()`*** accordingly.
```java
construct (BuildingType t) { 
	switch (t) { 
		case SCHOOL: bldg = (Building) new School(); break; 
		case BANK: bldg = (Building) new Bank(); break; 
		case HOME: bldg = (Building) new Home(); break; 
	} 
	bldg.construct(); 
}
```
Disadvantage:  subclasses are fixed

[[Framework| See Framework ->]]
# Applicability
- When a class can´t anticipate the class of objects it must create. 
- When a class wants its subclasses to specify the objects it creates. 
- When classes delegate responsibility to one of several helper subclasses, and you want to localize the knowledge of which helper subclass is the delegate. 
*Factory Method* is *Template Method* applied to object creation (some confusion in terminology: in Factory Method, the primitive operations are called factory methods. In Template Method, the primitive operations are called just that.