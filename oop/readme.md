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
  - Flyweight
  - Proxy
- Behavioral patterns
  - Chain of Responsibility
  - Command
  - Iterator
  - Mediator
  - Memento
  - Observer
  - State
  - Strategy
  - Template Method
  - Visitor
