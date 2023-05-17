# Duck Typing

Duck typing is a concept in dynamic programming languages like Python, where the type of an object is determined not by its class name, but by its behavior or the methods and attributes it defines. The term "duck typing" comes from the phrase "if it looks like a duck, swims like a duck, and quacks like a duck, then it probably is a duck."

In Python, duck typing means that an object's suitability for a given task is determined by the presence of specific methods or attributes, rather than its type. For example, if an object has a `get()` method, we can treat it as a dictionary, even if it's not actually an instance of the `dict` class.

Here's an example of duck typing in Python:

```python
def print_area(shape):
    print(shape.area())

class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle:
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

rectangle = Rectangle(2, 4)
circle = Circle(3)

print_area(rectangle) # prints 8
print_area(circle) # prints 28.26
```

In this example, we define two classes, `Rectangle` and `Circle`, that both have an `area()` method. We then define a function `print_area()` that takes an object as an argument and calls its `area()` method.

By passing a `Rectangle` object and a `Circle` object to `print_area()`, we can see that duck typing is at work - the function works with both objects even though they are of different types, because they both implement the necessary `area()` method.

Duck typing can be a powerful tool for writing flexible and extensible code, as it allows you to work with objects based on their behavior rather than their type. However, it requires careful design and testing to ensure that your code works as intended with different types of objects.
