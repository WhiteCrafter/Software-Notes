#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=94]]

# Intent 
provide a surrogate or placeholder for another object to control access to it
**A.K.A** Surrogate
# Structure
![[Pasted image 20260208224107.png]]
# Example
![[Pasted image 20260208224906.png]]
# Applicability
Proxy is applicable whenever there is a need for a more versatile or sophisticated reference to an object than a simple pointer. Here are several common situations in which the proxy pattern is applicable:
1. A **logging proxy** (counting proxy) counts the number of references to the real object so that it can be freed automatically when there are no more references. It also can log access information.
2. A **remote access proxy** provides a local representative for an object in a different address space.
3. A **buffer proxy** (cache proxy) loads a persistent object in memory when it was first dereferenced. It can hold a buffer with several objects, which can be moved between background and main memory on demand.
4. A **virtual proxy** creates expensive objects on demand. (delayed load, delayed creation).
5. A **firewall** (protection proxy) controls the access to the original object. Firewalls are useful when objects should have different access rights.
6. A **decorator** adds additional responsibilities to an object dynamically (maybe in cascades)
## Decorator 
![[Pasted image 20260208225132.png]]
### Structure
![[Pasted image 20260208225210.png]]