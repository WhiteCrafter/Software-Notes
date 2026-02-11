#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=10 ]]
# Intent 
Define a one-to-many dependency relationship between objects so that when one object changes its state, all its dependents are notified and updated automatically.
**A.K.A**: Dependents, Publish-Subscribe, Subject-Observer, Listener
## Motivation
When partitioning a system into a set of cooperating classes, consistency between related objects must be maintained.
It is not desirable to couple the classes tightly (every class knowing which other classes to update and how), because then the classes can’t be reused individually.
In the MVC example, the spreadsheet view and the bar chart view don’t know about each other, so they can be reused independently. A change to the spreadsheet is immediately reflected in the bar chart and vice versa
# Structure
![[Pasted image 20260209021111.png]]
## Colaborations
![[Pasted image 20260209021123.png]]
# Example

![[Pasted image 20260209021057.png]]
# Applicability
- When a change to an object requires changing others, and you don’t know how many or which ones. 
- When an object needs to notify others but can’t make assumptions about these objects. 
- When an abstraction has two aspects, one depending on the other. Encapsulating these aspects in separate objects allows independent reuse
# Consciences
- Subjects and observers can be reused independently. 
- Observers can be added/removed without modifying the subject or other observers. 
- Abstract coupling between subject and observer is achieved via the notify interface. Subject and observers can therefore belong to different layers in the USES-hierarchy, without introducing cycles (Subject does not use Observer in the sense of the USES-relation, because the subject's integrity does not depend on the presence or correct operation of observers).
- Automatic broadcast of changes. 
- Observers can decide whether to ignore a notification. 
- Cost of an update may be hidden
	- A single notification may cascade to many observers and their dependent objects.
	- Notify provides no hint on what changed. Additional protocol may be necessary to help observers detect what changed (Subject does not use Observer).
# Implementation
1. Observing more than one subject: Send subject as parameter in ***`notify(Subject s)`***.
2. Triggering update:
	-  part of ***`setState()`***,
	- clients call ***`notify()`*** explicitly. 
3. Deleting an observer: first unsubscribe it at its subjects.
4. Subject must be self-consistent before notification. When a subject subclass calls inherited operations, it may unintentionally trigger a notify from the superclass before the subclass object is completely consistent.
5. Update protocols: pull and push model
	- Pull model: Observer fetches all data from subject directly (may be inefficient)
	- Push model: Subject passes change data to observers in ***`notify()`*** (may reduce reusability)
6. Use Change Manager between subject and its observers: 
	- maintains a mapping of subjects to observers,
	- updates all dependent observers at the request of a subject,
	- avoids multiple updates and infinite recursion,
	- encapsulates complex update semantics.
	- ![[Pasted image 20260209021548.png]]