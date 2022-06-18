# Solid-principle object-oriented designs

**SOLID** is a set of object-oriented design principles aimed at making code more maintainable and flexible. 
They were coined by Robert "Uncle Bob" Martin in the year 2000 in his paper Design Principles and Design Patterns. 
The SOLID principles apply to any object-oriented language, but I'm going to concentrate on what they mean in a Python 
application in this post.

The SOLID principles are:

* The Single-Responsibility Principle (SRP)
* The Open-Closed Principle (OCP)
* The Liskov Substitution Principle (LSP)
* The Interface Segregation Principle (ISP)
* The Dependency inversion Principle (DIP)

### Single-Responsibility Principle
**Single-responsibility Principle (SRP) states:**

> A class should have one and only one reason to change, meaning that a class should have only one job.

### Open-Closed Principle
**Open-closed Principle (OCP) states:**

> Objects or entities should be open for extension but closed for modification. 
> 
> This means that a class should be extendable without modifying the class itself.

### Liskov Substitution Principle
**Liskov Substitution Principle states:**

> A subclass must be substitutable for its super-class.
> 
> The aim of this principle is to ascertain that a subclass can assume the place of its super-class without errors.
> 
> If the code finds itself checking the type of class then, it must have violated this principle.
> 

### The Interface Segregation Principle
**Interface segregation principle states:**

> A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to 
> depend on methods they do not use.

### Dependency Inversion Principle
**Dependency inversion principle states:**

> Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the 
low-level module, but they should depend on abstractions.
