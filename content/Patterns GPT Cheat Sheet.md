# Design Patterns – with Examples & Structures

> Source: Software Engineering lecture slides  
> Each pattern includes **intent, example (if shown), structure**, and **PDF+page links**

---

## Creational Patterns

### Singleton
**Intent:** Ensure exactly one instance of a class.

**Example (slides):**
- Logger
- Configuration manager

**Structure:**
- private constructor
- static instance
- public `getInstance()`

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=5|p.5]], [[Chap3.3DesignPatternTurorial.pdf#page=6|p.6]]

---

### Factory Method
**Intent:** Defer object creation to subclasses.

**Example:**
- Creator calls `createProduct()`
- ConcreteCreator decides which Product to instantiate

**Structure:**
- Product (interface)
- ConcreteProduct
- Creator (factory method)
- ConcreteCreator

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=8|p.8]], [[Chap3.3DesignPatternTurorial.pdf#page=9|p.9]]

---

### Abstract Factory
**Intent:** Create families of related objects.

**Example:**
- GUI widget families (Windows / Mac)

**Structure:**
- AbstractFactory
- ConcreteFactory
- AbstractProduct
- ConcreteProduct

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=11|p.11]], [[Chap3.3DesignPatternTurorial.pdf#page=12|p.12]]

---

### Builder
**Intent:** Separate construction from representation.

**Example:**
- Document / complex object builder

**Structure:**
- Builder
- ConcreteBuilder
- Director
- Product

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=14|p.14]]

---

### Prototype
**Intent:** Create objects by cloning.

**Structure:**
- Prototype interface
- `clone()`

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=16|p.16]]

---

## Structural Patterns

### Adapter
**Intent:** Convert incompatible interfaces.

**Example:**
- Legacy class wrapped by Adapter

**Structure:**
- Target
- Adapter
- Adaptee

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=18|p.18]]

---

### Bridge
**Intent:** Separate abstraction from implementation.

**Example:**
- Shape + DrawingAPI

**Structure:**
- Abstraction
- RefinedAbstraction
- Implementor
- ConcreteImplementor

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=20|p.20]]

---

### Composite
**Intent:** Treat objects and compositions uniformly.

**Example:**
- File system (File / Directory)

**Structure:**
- Component
- Leaf
- Composite

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=22|p.22]]

---

### Decorator
**Intent:** Add responsibilities dynamically.

**Example:**
- Java I/O streams

**Structure:**
- Component
- ConcreteComponent
- Decorator
- ConcreteDecorator

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=24|p.24]], [[Chap3.3DesignPatternTurorial.pdf#page=25|p.25]]

---

### Facade
**Intent:** Simplify subsystem usage.

**Structure:**
- Facade
- Subsystem classes

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=27|p.27]]

---

### Flyweight
**Intent:** Share intrinsic state.

**Example:**
- Characters in text editor

**Structure:**
- Flyweight
- ConcreteFlyweight
- FlyweightFactory

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=28|p.28]]

---

### Proxy
**Intent:** Control access to another object.

**Structure:**
- Subject
- RealSubject
- Proxy

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=29|p.29]]

---

## Behavioral Patterns

### Strategy
**Intent:** Interchangeable algorithms.

**Example:**
- Different sorting algorithms

**Structure:**
- Strategy
- ConcreteStrategy
- Context

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=32|p.32]]

---

### Observer
**Intent:** Automatic notification.

**Example:**
- GUI listeners

**Structure:**
- Subject
- Observer
- ConcreteSubject
- ConcreteObserver

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=34|p.34]]

---

### Command
**Intent:** Encapsulate requests.

**Example:**
- Menu actions, undo/redo

**Structure:**
- Command
- ConcreteCommand
- Invoker
- Receiver

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=36|p.36]]

---

### State
**Intent:** Behavior depends on internal state.

**Example:**
- Object state machine

**Structure:**
- State
- ConcreteState
- Context

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=38|p.38]], [[Chap2.2Additional-UML-Diagrams.pdf#page=3|state UML]]

---

### Template Method
**Intent:** Define algorithm skeleton.

**Structure:**
- AbstractClass
- TemplateMethod
- Primitive operations

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=41|p.41]]

---

### Iterator
**Intent:** Traverse collections.

**Structure:**
- Iterator
- Aggregate

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=42|p.42]]

---

### Mediator
**Intent:** Centralize communication.

**Example:**
- Dialog coordination

**Structure:**
- Mediator
- Colleagues

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=43|p.43]]

---

### Memento
**Intent:** Save and restore state.

**Example:**
- Undo operation

**Structure:**
- Originator
- Memento
- Caretaker

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=44|p.44]]

---

### Visitor
**Intent:** Add operations without modifying classes.

**Structure:**
- Visitor
- ConcreteVisitor
- Element
- ConcreteElement

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=45|p.45]]

---

### Chain of Responsibility
**Intent:** Pass request along handler chain.

**Example:**
- Logging chain

**Structure:**
- Handler
- ConcreteHandler
- next handler reference

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=47|p.47]]

---

### Interpreter
**Intent:** Interpret grammar.

**Example:**
- Expression evaluator

**Structure:**
- AbstractExpression
- TerminalExpression
- NonTerminalExpression

**References:**  
[[Chap3.3DesignPatternTurorial.pdf#page=48|p.48]]

---

## Architectural / Pattern-Oriented (non-GoF)

### Model–View–Controller (MVC)
**Structure:**
- Model
- View
- Controller

**References:**  
[[Chap3.1Design.pdf#page=12|MVC]], [[Chap8.1ProcessModels.pdf#page=6|UI]]

---

### Layers
**Structure:**
- Presentation
- Business logic
- Data

**References:**  
[[Chap3.2ArchitecturalStyles.pdf#page=8|Layers]]

---

### Pipes and Filters
**Structure:**
- Filters
- Pipes

**Example:**
- Image processing pipeline

**References:**  
[[Chap3.2ArchitecturalStyles.pdf#page=11|Pipes & Filters]]

---

### Client–Server
**Structure:**
- Client
- Server

**References:**  
[[Chap3.2ArchitecturalStyles.pdf#page=5|Client–Server]]

---

### Peer-to-Peer
**Structure:**
- Symmetric peers

**References:**  
[[Chap3.2ArchitecturalStyles.pdf#page=6|Peer-to-Peer]]

---

### Blackboard
**Structure:**
- Blackboard
- Knowledge sources
- Control component

**References:**  
[[Chap3.2ArchitecturalStyles.pdf#page=14|Blackboard]]

---
