### OOP(Object Oriented Programming)
**Object means a real-world entity such as a pen, chair, table, computer, watch, etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies the software development and maintenance by providing some concepts**
- use of self-contained code (objects) to develop applications
- Procedural programming is about writing procedures or functions that perform operations on the data.

### OOP Concepts
- Object
- Classes

**[Object-Oriented Programming System](./img/oopsystem.png)**

**Advantages of OOPs over Procedure Oriented Programming**
- makes development and maintenance easier whereas in a procedure-oriented programming language it is not easy to manage if code grows as project size increases. 
- provides data hiding whereas in a procedure-oriented programming language a global data can be accessed from anywhere.**
__________________
### Objects
**Any entity that has state and behavior is known as an object. For example a chair, pen, table, keyboard, bike, etc. It can be physical or logical.**

- can be defined as an instance of a class
- contains an address and takes up some space in memory
- can communicate without knowing the details of each other's data or code
- the type of message accepted and the type of response returned by the objects are necessary 

**Example: A dog is an object because it has states like color, name, breed, etc. as well as behaviors like wagging the tail, barking, eating, etc**
_________________________

### Class
**A class, in the context of Java, are templates that are used to create objects, and to define object data types and methods. Core properties include the data types and methods that may be used by the object**

- can be defined as a blueprint from which you can create an individual object
- does not consume any space
- When you are declaring a class in java, you are just creating a new data type

**[Class Example](./img/class.png)**
_______________________

### Constructor
**In Java, a constructor is a block of code similar to the method. It is called when an instance of the object is created, and memory is allocated for the object.**

- a special type of method which is used to initialize the object
- constructs the values at the time of object creation
- java compiler creates a default constructor if your class doesn't have any, so it is not necessary to write a constructor

**When is a constructor called?**
- When an object is created, compiler makes sure that constructors for all of its subobjects (its member and inherited objects) are called
- If members have default constructors or constructor without parameter then these constructors are called automatically, otherwise parameterized constructors can be called using initializer list. 

**Rules to remember while creating a constructor**
- There are three rules defined for the constructor:
    - name must be the same as its class name
    - must have no explicit return type
    - cannot be abstract, static, final, and synchronized

**Types of constructors**
- [Default Constructor](./img/defaultconstructorcompiler.png), if there is no constructor in the class, the compiler adds a default constructor
    -  a no-args constructor that the Java compiler inserts on your behalf
    - contains a default call to super(); which is the default behavior
    - if you implement any constructor then you no longer receive a default constructor

    **[Default Constructor Example](./img/defaultconstructor.png)**(invokes the no-argument constructor to create a new Bicycle object called yourBike)
 
- Parameterized Constructor, has a specific number of parameters
    - used to provide different values to the distinct objects, you can provide the same values also

    **[Parameterized Constructor Example](./img/parameterizedconstructor.png)**


### Constructor Overloading
In Java, a constructor is just like a method but without return type. It can also be overloaded like Java methods. 

- having more than one constructor with different parameter lists
- They are arranged in a way that each constructor performs a different task. 
- They are differentiated by the compiler by the number of parameters in the list and their types. 

**[Constructor Overloading Example](./img/constructoroverloading.png)**
____________________

### Constructor vs Method
#### Constructor 
- used to initialize the state of an object 
- must not have a return type 
- is invoked implicitly 
- The Java compiler provides a default constructor if you don't have any constructor in a class 
- The constructor name must be same as the class name 
#### Method
- used to expose the behavior of an object 
- must have a return type 
- invoked explicitly
- name may or may not be same as class name
- Methods used to obtain information about an object are known as accessor methods.
_______________________

### Access Modifiers
*There are two types of modifiers in java: access modifiers and non-access modifiers.* 
- [access modifiers](/img/accessmodifiers.png) specifies accessibility (scope) of a data member, method, constructor or class, there are 4 types of java access modifiers:
    - private
    - default
    - protected
    - public

- There are many non-access modifiers such as static, abstract, synchronized, native, volatile, transient etc.
- If you are overriding any method, overridden method (i.e. declared in subclass) must not be more restrictive [access modifiers method overriding example](/img/accessmodifiersmethodoverriding.png)

__________________________________

### Abstract Class
**A restricted class that cannot be used to create objects (to access it, it must be inherited from another class)**
- achieves security - hide certain details and only show the important details of an object
- must be declared with an abstract keyword
- can have abstract and non-abstract methods
- cannot be instantiated, can only have references of abstract class type `Animal myObj = new Animal(); // will generate an error if the class is abstract`
- To access the abstract class, it must be inherited from another class
- can have constructors and static methods also
- can have final methods which will force the subclass not to change the body of the method

#### Abstract Method
A method which is declared as abstract and does not have implementation is known as an abstract method. 

`abstract void printStatus();  //no method body and abstract` 
 
[Abstract class with abstract method example](../img/abstractclassmethod.png)
[Abstarct class Replit](https://repl.it/@shanreed1/abstractclass#Main.java)

[Java Enums:](/img/enum.png)
Enums were introduced in Java 5.0. Enums restrict a variable to have one of only a few predefined values. The values in this enumerated list are called enums.

With the use of enums it is possible to reduce the number of bugs in your code.

For example, if we consider an application for a fresh juice shop, it would be possible to restrict the glass size to small, medium and large. This would make sure that it would not allow anyone to order any size other than the small, medium or large.
