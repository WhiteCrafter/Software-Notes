#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=70]]
# Intent
Compose a system as a hierarchically ordered set of layers. A layer is a set of software components with a  well-defined interface, which uses lower layers as a client and acts as server for upper layers.
# Example
![[Pasted image 20260208182221.png]]
## Opaque Layers
- In a layered architecture with opaque layers, each layer can only use the layer directly below it.
![[Pasted image 20260208182431.png]]
## Transparent Layers
- In a layered architecture with transparent layers, each layer can use **all the layers below** it.
![[Pasted image 20260208185018.png]]
## Other examples 
- microkernels (operating systems)
- protocol stacks (networking)
- business applications(3 layers: data base , application kernel, user interface)
In some systems usage of the next lower layer only is allowed another variation is that every layer export only a subset of components of the next lower layer besides its own components

# 3-Tier Architecture 
- A 3-tier architecture is a 3-layer architecture with some of the layers being on different machines.
  _ For example, the user interface layer runs on the client machine, the application and database layers on the server


# Structure of Layers
![[Pasted image 20260208180448.png]]
# Applicability 
- Clear structuring of a system in levels of abstraction or virtual machines,
- No restrictions on the structure within layers.
- Independent development, testing, and replacement of layers,
- Step-by-step development and step-by-step testing,
- reuse of lower layers in other configurations,
- To provide a simplified interface for a complex layer (or several), one can use a [[Facade]]