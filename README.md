# ----------------------------------------
# What is OOP?
# ----------------------------------------
# OOP stands for Object Oriented Programming.
# To map code with real-world scenarios, we use *objects*.
# Before making an object, we must first define a *class* (a blueprint).
# Even strings, lists, and numbers are objects in Python!

# ----------------------------------------
# Basic Class & Object
# ----------------------------------------
class Student:
    name = "Abdullah Mateeb"

# Create an instance (object) of Student
s1 = Student()
print(s1.name)  # Accessing class attribute through object


# ----------------------------------------
# Another Example: Car Factory
# ----------------------------------------
class Car:
    colour = "Blue"
    brand = "Bugatti"

car1 = Car()
print(car1.colour)
print(car1.brand)


# ----------------------------------------
# What is a Constructor?
# ----------------------------------------
# A constructor is a special method called __init__.
# It runs automatically when an object is created.

class Student1:
    uni_name = "UBIT"  # Class attribute shared among all objects

    def __init__(self, fullname, age):
        self.name = fullname      # Instance attribute
        self.age = age            # Instance attribute
        print("Adding a student to the database...")

# Creating objects (instances)
s3 = Student1("Abd", 20)
print(s3.name)
print(s3.age)

s4 = Student1("Ahmed", 20)
print(s4.name)
print(s4.age)

# Accessing class attribute
print(s3.uni_name)
print(s4.uni_name)


# ----------------------------------------
# What are Methods?
# ----------------------------------------
# Methods are functions defined inside a class, and they belong to objects.

class Student2:
    university_name = "UBIT"

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def welcome(self):
        print("Welcome to UBIT,", self.name)

    def get_age(self):
        return self.age

s1 = Student2("M. Abdullah", 20)
s1.welcome()
print(s1.get_age())


# ----------------------------------------
# Practice: Calculating Average Marks
# ----------------------------------------
class Student3:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def get_average(self):
        total = sum(self.marks)
        avg = total / len(self.marks)
        print("Hi", self.name, ", your average score is:", avg)

s1 = Student3("Abdullah", [99, 23, 100])
s1.get_average()


# ----------------------------------------
# Static Method
# ----------------------------------------
# Static methods are utility functions tied to a class but not to a particular object.
# We use @staticmethod decorator to define them.

class MathUtils:
    @staticmethod
    def add(x, y):
        return x + y

print("Sum is:", MathUtils.add(5, 3))


# ----------------------------------------
# Four Pillars of OOP
# ----------------------------------------
# 1. Abstraction
# 2. Encapsulation
# 3. Inheritance
# 4. Polymorphism

# Example: Abstraction — Hiding internal working and exposing only necessary features

class Car:
    def __init__(self):
        self.acc = False
        self.brk = False
        self.clutch = False

    def start(self):
        self.acc = True
        self.clutch = True
        print("Car started...")

car1 = Car()
car1.start()


