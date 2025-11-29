Name: Ansh Raj
Course: BCA ( AI & DS ) 
Section: A
Roll No.: 2501060133
Sr No.: 54
Subject: Problem solving with python
Assignment No.: 3
Question (a): Diffentiate between Method overriding and Method overloading with an example.
-->Method Overriding: Method overriding in python is an object-oriented concept in which a child (derived) class provides it's own implementation of a method that is already defined in it's parent(base) class, using the same method name and parameters.
-->Method Overloading: Method overloading in Python is a concept in which a single method name is used to perform different operations based on the number or type of arguments passed, even though Python does not support traditional method overloading like some other languages.
Difference: Method overloading and method overriding are both important object-oriented concepts in Python, but they differ in purpose and implementation.
Method overloading refers to using the same method name to perform different operations based on the number or type of arguments passed. Python does not support traditional method overloading like Java, so it is achieved using default values or variable-length arguments (*args) within the same class. The method behavior changes depending on how it is called, and inheritance is not required. It is considered a form of compile-time polymorphism conceptually.
Example:
class Calculator:
    def add(self, a, b=0, c=0):
        return a + b + c

calc = Calculator()

print(calc.add(5))        # One argument
print(calc.add(5, 3))     # Two arguments
print(calc.add(5, 3, 2))  # Three arguments

On the other hand, method overriding occurs when a child class redefines a method that already exists in a parent class, using the same method name and parameters. It requires inheritance and allows the child class to provide its own specific behavior for that method. The method to be executed is decided at runtime, making it an example of runtime polymorphism. In short, method overloading changes how a method is used, while method overriding changes how a method behaves.
Example:
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):
        print("Dog barks")

dog = Dog()
dog.sound()

Question (b): Describe the role and types of constructors in Python with a suitable example.
Answer: A constructor in Python is a special method of a class that is automatically called when an object of the class is created. The main role of a constructor is to initialize the data members (variables) of the object and prepare it for use. In Python, the constructor method is named __init__. It helps in setting initial values for object attributes, performing setup tasks, and ensuring that each object starts in a valid state.
--> Default constructor: A default constructor is a constructor that does not accept any parameters (except self). It is used to initialize objects with default values.
Example:
class Student:
    def __init__(self):
        self.name = "Unknown"
        self.age = 0

    def display(self):
        print(self.name, self.age)

s = Student()
s.display()
--> Parameterized constructor: A parameterized constructor accepts arguments along with self. It allows different objects to be initialized with different values at the time of object creation.
Example: 
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display(self):
        print(self.name, self.age)

s1 = Student("Ansh", 18)
s2 = Student("Rahul", 20)

s1.display()
s2.display()
