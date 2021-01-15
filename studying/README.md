## I. Object Oriented Programming terminology (35%)


**Objects**
**Any entity that has state and behavior is known as an object. For example a chair, pen, table, keyboard, bike, etc. It can be physical or logical.** 

**Classes**
**A class, in the context of Java, are templates that are used to create objects, and to define object data types and methods. Core properties include the data types and methods that may be used by the object**

**Four Concepts of OOP**

**1. Inheritance**
**Reuseing the common logic and extract the unique logic into a separate class**
- classes inheriting from other classes creating the IS-A relationship which is also known as a parent-child relationship
- a child class reuses all fields and methods of the parent class (common part) and can implement its own (unique part)
- each class adds only what is necessary for it while reusing common logic with the parent classes
- Automobile(parent), car, truck, motocysle(child) example
                
**2. Polymorphism**
**Objects having the ability to take on many forms**
- have more than one IS-A relationship
- define one interface and have multiple implementations
Example: I am a person, mother, sister, daughter, coder, dancer
        
**3. Encapsulation**
**Coding in a way that protects data from being accessed and manipulated by outside code**
- so in java the data of one class is hidden from any other classes and can only be accessed through functions in the class 
- thus, the binding between the private state and public methods is made
Example: Lets say we have 
    - a **Book Class** with 
    - two private variables **read** **unread**
    - two public methods **nextPage** and **previousPage**
    - other classes can call the **nextPage** and **previousPage** methods, which can access **read** and **unread** variables
    - other classes can not directly access the **read** and  **unread** variables

**4. Abstraction**
**Only displaying the essential details to the user**
-  A pilot flying an airplane turns on the light for everybody to to put their seat belt on, he has no idea how pressing the button from the cockpit makes all the seatbealt lights come on he just knows he needs to press the btton to get it done
- can be achieved by sing interfaces and abstract classes
    
**Encapsulation and abstraction can help us develop and maintain a big codebase**

- **Method overriding,** on the other hand, occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.
- **Method Overloading:** When there are multiple functions with same name but different parameters then these functions are said to be overloaded. Functions can be overloaded by change in number of arguments or/and change in type of arguments.
___________________________

II.  JAVA basic & advanced (45%)
**Syntax**
**Data Types**
**Conditional Statements**
**Loops**
**Classes**
**Interfaces**
- an interface can be defined as a contract between objects on how to communicate with each other
- an interface defines the methods, a deriving class(subclass) should use. But the implementation of the methods is totally up to the subclass

**Abstract Classes**
**Exceptions**
**Collections**
_________
 **A Java program it can be defined as a collection of objects that communicate by invoking each other's methods**
 - **Object** - has states(Instance Variables) and behaviours(methods)
 - **Class** - a template/ blue print that describes the behaviours/states that a object of its type support
 - **Method** - where the logic is written, data is manipulated and all the actions are executed
 - **Instance Variables** - Each object has its unique set of instance variables. An object's state is created by the values assigned to these instance variables.
 - **main() method** - where processing starts and is a mandatory part of every Java program
 - **Identifiers** Names used for classes, variables and methods are called identifiers
    - should begin with a letter (A to Z or a to z), currency character ($) or an underscore (_)
    - After the first character identifiers can have any combination of characters
_____________________
**Java Modifiers:**
- used to modify classes, methods

**Access Modifiers:** default, public, protected, private

**Non-access Modifiers:** final, abstract, strictfp

_____________
**Java Variables:**
Local Variables
Class Variables (Static Variables)
Instance Variables (Non-static variables)