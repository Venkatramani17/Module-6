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
```
from abc import ABC
class Shape(ABC):
    def calculate_area(self):
        pass
class Rectangle(Shape):
    length = 5
    breadth =3 
    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
  radius = 4
  def calculate_area(self):
      return 3.14 * self.radius * self.radius
rec=Rectangle()
cir=Circle()
print("Area of a rectangle:", rec.calculate_area())
print("Area of a circle:", cir.calculate_area())

```
## Output
![Screenshot (207)](https://github.com/user-attachments/assets/6fbcf00e-2d2f-426c-8ce0-06bf921648aa)

## Result
Thus ,the program excuted successfully.

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program
```
class R:
    def __init__(self, l, w):
        self.__l = l
        self.__w = w
    def display(self):
        print(self.__l)
        print(self.__w)
rect = R(5,3)
rect.display()
```
## Output
![Screenshot (211)](https://github.com/user-attachments/assets/979c8dfb-5056-4bd6-8480-68c5df630b75)

## Result
Thus ,the program executed successfully.

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
       def type(self):
           print("fish")
class Shark(Fish):
    def type(self):
        print("shark")
f=Fish()
f.type()
s=Shark()
s.type()
```
## OUTPUT
![Screenshot (208)](https://github.com/user-attachments/assets/5f4834ae-d14f-4e6e-8961-5be4aeb33361)

## RESULT
Thus,the program excuted successfully.

# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A : 
   def __init__(self,a): 
      self.a=a 
def  lt (self,o): 
   if self.a < o.a : 
      return "ob1 is less than ob2" 
   else: 
      return "ob2 is less than ob1" 
ob1 = A(2) 
ob2 = A(3) 
print(ob1<ob2)
```

## Output
![image](https://github.com/user-attachments/assets/44d05dd9-9676-43ad-9d88-f2e92ca09c68)

## Result
 Thus, the program has been successfully executed. 

 # # 🐍 Python OOP: Polymorphism with Classes

## 🎯 AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

## 🧠 ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

## 💻 Program
```
class Beans():
def type(self):
print("Vegetable")
def color(self):
print("Green")
class Mango():
def type(self):
print("Fruit")
def color(self):
print("Yellow")
def func(obj):
obj.type()
obj.color()
obj_beans = Beans()
obj_mango = Mango()
func(obj_beans)
func(obj_mango)
```
## Output
![Screenshot (210)](https://github.com/user-attachments/assets/0f138b56-47e7-484f-b876-54200f75895c)

## Result
Thus,the program excuted successfully.
