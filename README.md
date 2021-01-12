# OOP(Object Oriented Programming)
**Object means a real-world entity such as a pen, chair, table, computer, watch, etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies the software development and maintenance by providing some concepts**

### OOP Concepts
- Object
- Classes
- Inheritance
- Polymorphism
- Abstraction
- Encapsulation

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
