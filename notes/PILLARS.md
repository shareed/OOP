# Object Oriented Programming Pillars(Java)
- Inheritance
    - a mechanism in which one object acquires all the properties and behaviors of a parent object
- Polymorphism
    - The ability of an object to take on many forms
- Encapsulation
    - A process of wrapping code and data together into a single unit, for example, a capsule which is mixed of several medicines
- Abstraction
____________________

## Inheritance

- you can create new classes that are built upon existing classes
- when you inherit from an existing class, you can reuse methods and fields of the parent class
- you can add new methods and fields in your current class also
- represents the IS-A relationship which is also known as a parent-child relationship

**Advantages of Inheritance**
- Method Overriding (so runtime polymorphism can be achieved).
- Code Reusability.

**Terms used in Inheritance**
- **Class:** a class is a group of objects which have common properties
    - a template or blueprint from which objects are created.

- **Sub Class/Child Class:** a class which inherits the other class
    - also called a derived class, extended class, or child class

- **Super Class/Parent Class:** the class from where a subclass inherits the features
    - also called a base class or a parent class

- **Reusability:** a mechanism which facilitates you to reuse the fields and methods of the existing class when you create a new class
    - you can use the same fields and methods already defined in the previous class

**Syntax**
-  **extends** keyword indicates that you are making a new class that derives from an existing class
    - `class Subclass-name extends Superclass-name{}`

**[Inheritance Example](../img/inheritance.png)**
___________________________

### Types Of Inheritance In Java
**On the basis of class, there can be three types of inheritance in java: single, multilevel and hierarchical.(multiple and hybrid inheritance is supported through interface only)**

**[Single Inheritance Example](../img/singleinheritance.png)**
**[Multilevel Inheritance Example](../img/multilevelinheritance.png)**
**[Hierarchical Inheritance Example](../img/hierarchicalinheritance.png)**

##### Why [multiple inheritance](../img/multipleinheritance.png) is not supported in Java?
To reduce the complexity and simplify the language, multiple inheritance is not supported in java. 

Consider a scenario where A, B, and C are three classes. The C class inherits A and B classes. If A and B classes have the same method and you call it from child class object, there will be ambiguity to call the method of A or B class.

Since compile-time errors are better than runtime errors, Java renders compile-time error if you inherit 2 classes. So whether you have same method or different, there will be compile time error.
_______________________________

## Polymorphism
**The ability of an object to take on many forms. The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.**

- any Java object that can pass more than one IS-A test is considered to be polymorphic
- all Java objects are polymorphic since any object will pass the IS-A test for their own type and for the class Object

### Method Overloading 
**If a class has multiple methods having same name but different in parameters, it is known as Method Overloading.**

If we have to perform only one operation, having same name of the methods increases the readability of the program. 

**Suppose you have to perform addition of the given numbers but there can be any number of arguments, if you write the method such as a(int,int) for two parameters, and b(int,int,int) for three parameters then it may be difficult for you as well as other programmers to understand the behavior of the method because its name differs**

##### Different ways to overload a method?
- [By changing number of arguments](../img/methodoverloading1.png)
    -  creating static methods so that we don't need to create instance for calling methods
    -  two methods, first add() method performs addition of two numbers and second add method performs addition of three numbers.
- [By changing the data type](../img/methodoverloading2.png)
    - created two methods that differs in data type
    - first add method receives two integer arguments and second add method receives two double arguments. 

**Note : Method overloading is not possible by changing the return type of the method**

- You can have any number of [main methods](../img/overloadingmain.png) in a class by method overloading. But JVM calls main() method which receives string array as arguments only. 
____________________

### Method Overriding
**If subclass (child class) has the same method as declared in the parent class, it is known as method overriding in Java.**
- if a subclass provides the specific implementation of the method that has been declared by one of its parent class, it is known as method overriding.

#### Usage and Rules for Method Overriding
**Usage:** 
- used to provide the specific implementation of a method which is already provided by its superclass.
- used for runtime polymorphism

**Rules:** 
- must have the same name as in the parent class
- must have the same parameter as in the parent class
- must be an IS-A relationship (inheritance)

**[Method Overriding Example](../img/methodoverriding.png)**
    -  defines a disp() method in the subclass as defined in the parent class but it has some specific implementation
    - the name and parameter list of the methods are the same, and there is IS-A relationship between the classes

##### Static method cannot be overridden

- static methods are bound with class whereas instance method is bound with an object
- static belongs to the class area, and an instance belongs to the heap area 

### Method Overloading vs Method Overriding
**Method Overloading** 
- used to increase the readability of the program 
- performed within class
- parameter must be different
- is the example of compile time polymorphism. 
- can't be performed by changing return type of the method only
- return type can be same or different in method overloading

**Method Overriding** 
- used to provide the specific implementation of the method that is already provided by its super class
- occurs in two classes that have IS-A (inheritance) relationship
- parameter must be same
- is the example of run time polymorphism. 
- return type must be same or covariant

**[Method Overiding Replit](https://repl.it/@shanreed1/methodoverriding)**

__________________________

## Encapsulation
**A process of wrapping code and data together into a single unit, for example, a capsule which is mixed of several medicines.**

- you can create a fully encapsulated class in Java by making all the data members of the class private
- then you can use setter and getter methods to set and get the data in it 
**The Java Bean class is the example of a fully encapsulated class**

**Advantages of Encapsulation**
- By providing only a setter or getter method, you can make the class read-only or write-only(you can skip the getter or setter methods but they provide you the control over the data
    - Suppose you want to set the value of id which should be greater than 100 only, you can write the logic inside the setter method. You can write the logic not to store the negative numbers in the setter methods.
- It is a way to achieve data hiding in Java because other class will not be able to access the data through the private data members.
- The encapsulate class is easy to test. So, it is better for unit testing.

**[Encapsulation Class Example](../img/encapsulationclass.png)**
- a class called Student that has only one field with its setter and getter methods

**[Encapsulation Read Only Class Example](../img/encapsulationreadonlyclass.png)**
-  it has only a getter to access the college name. If the user tries to change the value of the college name, a compile-time error is rendered. 


**[Encapsulation Write Only Class Example](../img/encapsulationwriteonlyclass.png)**
-  it has only setters to change the value of the college name and cannot read the college name. Even if tried to access outside of this class a compile-time error is displayed only because the variable is declared as private. 

**[Encapusulation Replit](https://repl.it/@shanreed1/encapsulation#Main.java)**

