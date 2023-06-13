# Factory Method

> "Define an interface for creating an object, but let subclasses decide which class to instantiate. The Factory method lets a class defer instantiation it uses to subclasses." (Gang Of Four)

The Factory Method design pattern is a creational design pattern that provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created. In other words, it encapsulates object creation and delegates it to subclasses, rather than instantiating objects directly in the superclass.

The Factory Method pattern is useful when you have a superclass that doesn't know what type of objects it needs to create, but it knows the type of objects it wants to use. The factory method can be used to create these objects without the superclass having to know exactly what type of object it needs to create.

## Pros and Cons

Pros:

- Encapsulates object creation: The Factory Method pattern encapsulates the object creation process in a separate class or method, which makes it easier to modify or extend the creation process without affecting the rest of the code.
- Provides flexibility and extensibility: By delegating object creation to subclasses, the Factory Method pattern allows for more flexibility and extensibility in the creation of objects, making it easier to add new types of objects in the future.
- Promotes loose coupling: The Factory Method pattern promotes loose coupling between classes by allowing them to communicate through interfaces rather than concrete implementations, which makes the code more modular and easier to maintain.
- Single Responsibility Principle. You can move the product creation code into one place in the program, making the code easier to support.
- Open/Closed Principle. You can introduce new types of products into the program without breaking existing client code.

Cons:

- Increased complexity: The Factory Method pattern can increase the complexity of the code by introducing additional classes and methods, which can be difficult to manage in large applications.
- Overhead: The Factory Method pattern can introduce additional overhead by requiring the creation of additional classes and methods, which can affect performance in applications with many objects.
- Requires more code: The Factory Method pattern requires the creation of additional classes and methods, which can result in more code that needs to be written and maintained.
- May not be necessary for simple applications: For simple applications with only a few types of objects, the Factory Method pattern may introduce unnecessary complexity and overhead.

## Reference
- https://en.wikipedia.org/wiki/Factory_method_pattern
- https://refactoring.guru/design-patterns/factory-method
- https://refactoring.guru/design-patterns/factory-method/python/example
