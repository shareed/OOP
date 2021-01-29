# Abstraction
**A process of hiding the implementation details and showing only functionality to the user**

- shows only essential things to the user and hides the internal details
- lets you focus on what the object does instead of how it does it
________________________________________________

**Generalization**
**The process of extracting shared characteristics from two or more classes, and combining them into a generalized superclass. Shared characteristics can be attributes, associations, or methods.**

[Generalization Example](../img/generalization.png)
    - The classes Piece of Luggage  and Piece of Cargo partially share the same attributes
    - From a domain perspective, the two classes are also very similar
    - During generalization, the shared characteristics  are combined and used to create a new superclass Freight
    - Piece of Luggage and Piece of Cargo become subclasses of the class Freight
    - Therefore the properties that are common to the classes Piece of Luggage and Piece of Cargo are placed in the superclass Freight - Identification, Weight and ID-Number are those properties. 

**Specialization**
**Creating new subclasses from an existing class. If it turns out that certain attributes, associations, or methods only apply to some of the objects of the class, a subclass can be created.**
- [Specialization Example](../img/specialization.png)
    - if there is a property that is only applicable to a specific subclass, such as Degree of  Hazardousness, that property is placed in the class Piece of Cargo where-in this class also has all the properties of the Freight class with the concept of Generalization. 

### Ways to achieve abstraction?
- Abstract class (0 to 100%)
- Interface (100%)
__________________________________
### Abstract Class
- must be declared with an abstract keyword
- can have abstract and non-abstract methods
- cannot be instantiated, can only have references of abstract class type
- can have constructors and static methods also
- can have final methods which will force the subclass not to change the body of the method

#### Abstract Method
A method which is declared as abstract and does not have implementation is known as an abstract method. 

`abstract void printStatus();  //no method body and abstract` 
 
[Abstract class with abstract method example](../img/abstractclassmethod.png)
[Abstarct class Replit](https://repl.it/@shanreed1/abstractclass#Main.java)
[Abstract Class vs Interface](/img/abstractclassinterface.png)