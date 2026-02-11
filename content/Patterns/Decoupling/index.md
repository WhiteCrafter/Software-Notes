---
	title: 	Decoupling
---
#software/designpatterns/category
# Decoupling
Decoupling Patterns divide a software system into several independent parts in such a way that they can be built, changed, and replaced independently as well as reused and recombined in unforeseen combinations. An important advantage of decoupling is local change, i.e., a system consisting of decoupled parts can be adapted and extended by modifying or adding a single or only a few parts, instead of modifying everything.

- Module
- Abstract Datatype
	- [[Repository]]
		- Client/Server
	- Manager
	- [[Iterator]]
	- Collection
		- Set
		- Bag
		- Sequence
		   . . . 
	-  . . . 
- [[Layers]]
	- Sandwich
	- [[Facade]]
	- [[Mediator]]
	- [[Bridge]]
	- [[Adapter]](Wrapper)
	- Facet( Extension Object)
	- [[Proxy]]
		- **Decorator** *see in proxy [[Proxy#Decorator| -->]]*
		- **Buffer Proxy**
		- **Logging (Counting) Proxy**
		- **Firewall**
		- Synchronization Proxy
		- **Remote Access Proxy**
- [[Pipeline]]
- Event Notification
	- Event Handler (Catch and Throw)
	- Callback
	- Event Loop
	- [[Event Channel]]
	- Propagator
		- Strict Propagator with/without failure
		- Lazy Propagator
		- Adaptive Propagator
		- [[Observer]] !
- [[Framework]]

