# 🐍 Python OOP: Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program
~~~
from abc import ABC, abstractmethod
import math
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, l, w):
        self.l = l
        self.w = w
    def calculate_area(self):
        return self.l * self.w
class Circle(Shape):
    def __init__(self, r):
        self.r = r
    def calculate_area(self):
        return math.pi * self.r**2
print("Rectangle area:", Rectangle(5, 3).calculate_area())
print("Circle area:", Circle(4).calculate_area())
~~~
## Output
<img width="1262" height="608" alt="image" src="https://github.com/user-attachments/assets/62a12298-13c8-4b37-aa4d-fa24401b14a3" />

## Result
The code is executed successfully.
