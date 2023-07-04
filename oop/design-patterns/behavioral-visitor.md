# Visitor

![analogy](https://refactoring.guru/images/patterns/content/visitor/visitor-comic-1.png)

The Visitor pattern is a behavioral pattern that separates an algorithm from an object structure on which it operates. The pattern allows you to add new operations or algorithms to an object structure without modifying the structure itself. The pattern achieves this by defining a separate object called a visitor, which can traverse an object structure and apply a specific operation to each element of the structure.

The main idea behind the Visitor pattern is to provide a way to separate the concerns of an algorithm from the object structure it operates on. This allows you to add new operations or algorithms to an object structure without modifying the structure itself.

## Example

Here's an example of the Visitor pattern in Python:

```python
# Element interface
class Element:
    def accept(self, visitor):
        pass

# Concrete element classes
class ConcreteElementA(Element):
    def accept(self, visitor):
        visitor.visit_concrete_element_a(self)

    def operation_a(self):
        pass

class ConcreteElementB(Element):
    def accept(self, visitor):
        visitor.visit_concrete_element_b(self)

    def operation_b(self):
        pass

# Visitor interface
class Visitor:
    def visit_concrete_element_a(self, element):
        pass

    def visit_concrete_element_b(self, element):
        pass

# Concrete visitor class
class ConcreteVisitor(Visitor):
    def visit_concrete_element_a(self, element):
        print("ConcreteVisitor visiting ConcreteElementA.")
        element.operation_a()

    def visit_concrete_element_b(self, element):
        print("ConcreteVisitor visiting ConcreteElementB.")
        element.operation_b()

# Object structure class
class ObjectStructure:
    def __init__(self):
        self._elements = []

    def attach(self, element):
        self._elements.append(element)

    def detach(self, element):
        self._elements.remove(element)

    def accept(self, visitor):
        for element in self._elements:
            element.accept(visitor)

# Client code
def client_code():
    object_structure = ObjectStructure()
    object_structure.attach(ConcreteElementA())
    object_structure.attach(ConcreteElementB())

    visitor = ConcreteVisitor()
    object_structure.accept(visitor)

# Usage
client_code()
```

In this example, we have an `Element` interface that defines the common interface for all the concrete element classes. The `Element` object represents an element of the object structure that can be visited by a visitor.

The `ConcreteElementA` and `ConcreteElementB` classes are concrete element classes that implement the `Element` interface. Each `ConcreteElement` object represents an element of the object structure that can be visited by a visitor.

The `Visitor` interface defines the common interface for all the concrete visitor classes. The `Visitor` object represents an algorithm that can be applied to each element of the object structure.

The `ConcreteVisitor` class is a concrete visitor class that implements the `Visitor` interface. The `ConcreteVisitor` object represents a specific algorithm that can be applied to each element of the object structure.

The `ObjectStructure` class represents the object structure that can be visited by a visitor. The `ObjectStructure` object maintains a list of elements and allows visitors to visit each element in the list.

When we create an `ObjectStructure` object, add some `ConcreteElement` objects to it, create a `ConcreteVisitor` object, and apply the visitor to the object structure using the `accept` method, we get the output:

```
ConcreteVisitor visiting ConcreteElementA.
ConcreteVisitor visiting ConcreteElementB.
```

As you can see, the `ConcreteVisitor` object visits each `ConcreteElement` object in the `ObjectStructure` and applies the algorithm defined in the `visit_concrete_element_a` and `visit_concrete_element_b` methods. This example demonstrates how the Visitor pattern can be used to separate an algorithm from an object structure on which it operates.

## Reference

- https://refactoring.guru/design-patterns/visitor
