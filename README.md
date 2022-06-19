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

-------------------------------------------

## Single-Responsibility Principle


**Single-responsibility Principle (SRP) states:**

> A class should have one and only one reason to change, meaning that a class should have only one job.

### Example: [Single Responsibility Principle](https://github.com/heykarimoff/solid.python/blob/master/1.srp.py)

**The result of this simple action is that now:**

1. It is easier to localize errors. Any error in execution will point out to a smaller section of your code, 
accelerating your debug phase.
2. Any part of the code is reusable in other section of your code.
3. Moreover and, often overlooked, is that it is easier to create testing for each function of your code. 
Side note on testing: You should write tests before you actually write the script. But, this is often ignored in favour 
of creating some nice result to be shown to the stakeholders instead.
4. Lower coupling – Less functionality in a single class will have fewer dependencies.

**Goal:**

`This principle aims to separate behaviours so that if bugs arise as a result of your change, it won’t affect other 
unrelated behaviours.`

-------------------------------------------
## Open-Closed Principle

**Open-closed Principle (OCP) states:**

> Objects or entities should be open for extension but closed for modification. 
> 
> This means that a class should be extendable without modifying the class itself.

### Example: [Open-Closed Principle](https://github.com/heykarimoff/solid.python/blob/master/2.ocp.py)

**Goal:**

`This principle aims to extend a Class’s behaviour without changing the existing behaviour of that Class. This is to 
avoid causing bugs wherever the Class is being used.`

-------------------------------------------
## Liskov Substitution Principle

**Liskov Substitution Principle states:**

> A subclass must be substitutable for its super-class.
> 
> The aim of this principle is to ascertain that a subclass can assume the place of its super-class without errors.
> 
> If the code finds itself checking the type of class then, it must have violated this principle.

### Example: [Liskov Substitution Principle](https://github.com/heykarimoff/solid.python/blob/master/3.lsp.py)


When a **child** Class cannot perform the same actions as its **parent** Class, this can cause bugs.

If you have a Class and create another Class from it, it becomes a **parent** and the new Class becomes a **child**. 
The **child** Class should be able to do everything the **parent** Class can do. This process is called **Inheritance**.

The **child** Class should be able to process the same requests and deliver the same result as the **parent** Class or 
it could deliver a result that is of the same type.

**Goal:**

`This principle aims to enforce consistency so that the parent Class or its child Class can be used in the same way without any errors.
`

-------------------------------------------
## The Interface Segregation Principle


**Interface segregation principle states:**

> A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to 
> depend on methods they do not use.
> 
> **_Many client-specific interfaces are better than one general-purpose interface_**

### Example: [Interface Segregation Principle](https://github.com/heykarimoff/solid.python/blob/master/4.isp.py)

**Goal:**

`This principle aims at splitting a set of actions into smaller sets so that a Class executes ONLY the set of actions it requires.
`

-------------------------------------------
## Dependency Inversion Principle

**Dependency inversion principle states:**

> High-level modules should not depend on low-level modules. Both should depend on the abstraction.
> 
>Abstractions should not depend on details. Details should depend on abstractions.

### Example: [Dependency Inversion Principle](https://github.com/heykarimoff/solid.python/blob/master/5.dip.py)

Firstly, let’s define the terms used here more simply

**High-level Module(or Class):** Class that executes an action with a tool.

**Low-level Module (or Class):** The tool that is needed to execute the action

**Abstraction:** Represents an interface that connects the two Classes.

**Details:** How the tool works

This principle says a Class should not be fused with the tool it uses to execute an action. Rather, it should be fused to the interface that will allow the tool to connect to the Class.

It also says that both the Class and the interface should not know how the tool works. However, the tool needs to meet the specification of the interface.


**Goal:**

`This principle aims at reducing the dependency of a high-level Class on the low-level Class by introducing an interface.
`

### References:

1. https://towardsdatascience.com/solid-coding-in-python-1281392a6a94
2. https://medium.com/backticks-tildes/the-s-o-l-i-d-principles-in-pictures-b34ce2f1e898
3. https://gist.github.com/dmmeteo/f630fa04c7a79d3c132b9e9e5d037bfd
4. https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/
5. https://github.com/heykarimoff/solid.python
