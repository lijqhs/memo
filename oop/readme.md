# OOP / Design Pattern

- [SOLID Principles](solid.md)
- [Drawbacks of Inheritance](drawbacks-of-inheritance.md)
- [Class-based programming vs Prototype-based programming](class-vs-prototype.md)

## Design Patterns

- Creational patterns
  - [Factory Method](creational-factory-method.md): Define an interface for creating a single object, but let subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses.
  - [Abstract Factory](creational-abstract-factory.md): Provide an interface for creating families of related or dependent objects without specifying their concrete classes.
  - [Builder](creational-builder.md): Separate the construction of a complex object from its representation, allowing the same construction process to create various representations.
  - [Prototype](creational-prototype.md): Specify the kinds of objects to create using a prototypical instance, and create new objects from the 'skeleton' of an existing object, thus boosting performance and keeping memory footprints to a minimum.
  - [Singleton](creational-singleton.md): Ensure a class has only one instance, and provide a global point of access to it.
- Structural patterns
  - [Adapter](structural-adapter.md): Convert the interface of a class into another interface clients expect. An adapter lets classes work together that could not otherwise because of incompatible interfaces.
  - [Bridge](structural-bridge.md): Decouple an abstraction from its implementation allowing the two to vary independently.
  - [Composite](structural-composite.md): Compose objects into tree structures to represent part-whole hierarchies. Composite lets clients treat individual objects and compositions of objects uniformly.
  - [Decorator](structural-decorator.md): Attach additional responsibilities to an object dynamically keeping the same interface. Decorators provide a flexible alternative to subclassing for extending functionality.
  - [Facade](structural-facade.md): Provide a unified interface to a set of interfaces in a subsystem. Facade defines a higher-level interface that makes the subsystem easier to use.
  - [Flyweight](structural-flyweight.md): Use sharing to support large numbers of similar objects efficiently.
  - [Proxy](structural-proxy.md): Provide a surrogate or placeholder for another object to control access to it.
- Behavioral patterns
  - [Chain of Responsibility](behavioral-chain-of-responsibility.md): Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.
  - [Command](behavioral-command.md): Encapsulate a request as an object, thereby allowing for the parameterization of clients with different requests, and the queuing or logging of requests. It also allows for the support of undoable operations.
  - [Iterator](behavioral-iterator.md): Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation.
  - [Mediator](behavioral-mediator.md): Define an object that encapsulates how a set of objects interact. Mediator promotes loose coupling by keeping objects from referring to each other explicitly, and it allows their interaction to vary independently.
  - [Memento](behavioral-memento.md): Without violating encapsulation, capture and externalize an object's internal state allowing the object to be restored to this state later.
  - [Observer](behavioral-observer.md): Define a one-to-many dependency between objects where a state change in one object results in all its dependents being notified and updated automatically.
  - [State](behavioral-state.md): Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.
  - [Strategy](behavioral-strategy.md): Define a family of algorithms, encapsulate each one, and make them interchangeable. Strategy lets the algorithm vary independently from clients that use it.
  - [Template Method](behavioral-template-method.md): Define the skeleton of an algorithm in an operation, deferring some steps to subclasses. Template method lets subclasses redefine certain steps of an algorithm without changing the algorithm's structure.
  - [Visitor](behavioral-visitor.md): Represent an operation to be performed on instances of a set of classes. Visitor lets a new operation be defined without changing the classes of the elements on which it operates.

### References

- https://en.wikipedia.org/wiki/Software_design_pattern
- https://refactoring.guru/
