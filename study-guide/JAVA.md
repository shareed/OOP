# JAVA
## Syntax
#### 2 ypes of statements Statement ( a line of code)
- Expression
- Control flow or conditional, which can be divided into decision(uses boolean logic) and loop(repeat a statement) statements 

[More on Java Syntax...](https://github.com/STR-FRONT-END/Java/blob/main/BASICS.md)
_________________________________

## Data Types(divided into two groups)
##### Primitive (created by the programmer)
- [includes 8 data types:](../img/javadatatypes.png) byte, short, int, long(`15000000000L`), float(`5.75f`), double(`19.99d`), boolean and char (single character, `'A'` or `'c'`: ASCII values to display certain characters, `char a = 65, b = 66, c = 67;`)
- Primitive number types are divided into two groups:

**Integer**
- stores whole numbers, positive or negative without decimals
- types are `byte`, `short`, `int` and `long`

**Floating** 
- represents numbers with a fractional part, containing one or more decimals
- types are: `float` and `double`
##### Non-primitive (already defined in Java)
- Examples: Strings, Arrays, Classes, Interface, etc.
- called reference types because they refer to objects
##### Reference Data Types: used to access objects
[More on Data Types...](../java/DATATYPES.md)
_____________________________

## Conditional Statements
- if statement 
- if..else statement
- if...else if 
- nested if statement
- switch statement

[More on Java Conditionals....](../java/CONDITIONALS.md)
[More on Java Conditionals....](https://github.com/STR-FRONT-END/Java/blob/main/CONDITIONALS.md)
__________________

## Looping(control flow statements)
- allows us to execute a statement or group of statements multiple times
##### for loop
- used to repeatedly execute a block of code a specified number of times
##### while loop
- used to repeatedly execute a block of code until a specified condition is no longer satisfied
##### do-while loop
- used to repeatedly execute a block of code until a specified condition is no longer satisfied, will run at least once
##### enhance For Loop
-  mainly used to traverse collection of elements including arrays

[More on Java Loops](../java/LOOPING.md) 
_______________________

## Classes
- you write classes and work with objects
- a template/ blue print that describes the behaviours/states that a object of its type support(Java structure that you define)
- you instantiate objects from classes, making that object follow the class template
##### State
- properties like size, weight, propulsion, etc.
##### Behavior
- methods like communicate(), track(), walk(), fly() etc.
##### Main Method
`public static void main(String[] args)`
##### Access modifiers
-  helps to restrict the scope of a class, constructor, variable, method, or data member ([Default, Private, Protected, Public](../img/accessmodifiers2.md))
##### IS-A vs. HAS-A relationships
- An IS-A relationship represent a class that is a subclass of another.
- A HAS-A relationship is a class that has a field that references another class.

##### Class Constructors
- initializes the state of a class

##### Super keyword
- the keyword super is a way to refer to a parent class (from within the child class), example: `super.parentMethod();`

[More on Classes...](https://github.com/STR-FRONT-END/Java/blob/main/CLASSES.md)
[More on Classes andConstructors...](../README.md)
____________________________________

## Interfaces(Reference type)
- is like a contract between objects on how to communicate with each other
- the interface defines the methods, a deriving class(subclass) should use
- the implementation of the methods is totally up to the subclass
[More on Interfaces](../java/INTERFACE.md)
__________________________

## Abstract Classes
- a restricted class that cannot be used to create objects (to access it, it must be inherited from another class)
- Abstract method: can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from)
- Can have both abstract and regular methods

[More on Abstarct Classes...](../README.md)
___________________________________

## Abstract Classes VS Interfaces.
Below is a list of some differences between the two:

- A class can extend only one class (abstract or not) but can implement multiple interfaces
- Interface variables are implicitly public static final
- Abstract classes can declare any modifiers on instance variables
- Interfaces can (as of Java 8) provide default methods, but all others are public abstract
- Abstract classes can declare any modifiers on their methods
**If you wanted to develop and enforce a certain hierarchy of functionality where state and behavior was tracked, then you would use an abstract class**

**If you want a class to be free to implement functionality without constrained to a hierarchy, then an interface is a better approach**
## Exceptions
**An Exception is a specific subclass of Throwable and it represents all possible exceptions that may occur within your program**
- different errors can occur: coding errors made by the programmer, errors due to wrong input, or other unforeseeable things
### TRY and CATCH
- **try** statement allows you to define a block of code to be tested for errors while it is being executed
- **catch** statement allows you to define a block of code to be executed, if an error occurs in the try block
- **finally** statement lets you execute code, after try...catch, regardless of the result
- **throw** statement allows you to create a custom error
    -  used together with an exception type. There are many exception types available in Java: ArithmeticException, FileNotFoundException, ArrayIndexOutOfBoundsException, SecurityException, etc:

[More on Exceptions](../java/EXCEPTIONS.md)
________________________________________

## Collections
- **Collection:** interface implemented by all collections
- **Collections:** class with static methods used to manipulate the collection object
- **Ordering:** determines where an element is in a collection
- **Sorting:** determines an element's position based on its value; it can be alphabetical, numerical or other
- List, Set and Queue are interfaces that extend Collection
    - **List:** is an interface that specifies an order
    - **Set:** is an interface that specifies a collection that doesn't allow duplicate elements
    **Queue:** is a collection that maintains order

[More on Collections....](https://github.com/STR-FRONT-END/Java/blob/main/COLLECTIONS.md)
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
Local variables
- Local variables are declared in methods, constructors, or blocks.
- Local variables are created when the method, constructor or block is entered and the variable will be destroyed once it exits the method, constructor, or block.
- Access modifiers cannot be used for local variables.
- Local variables are visible only within the declared method, constructor, or block.
- Local variables are implemented at stack level internally.
- There is no default value for local variables, so local variables should be declared and an initial value should be assigned before the first use.
Class Variables (Static Variables)
Class variables also known as static variables are declared with the static keyword in a class, but outside a method, constructor or a block.

There would only be one copy of each class variable per class, regardless of how many objects are created from it.

Static variables are rarely used other than being declared as constants. Constants are variables that are declared as public/private, final, and static. Constant variables never change from their initial value.

Static variables are stored in the static memory. It is rare to use static variables other than declared final and used as either public or private constants.

Static variables are created when the program starts and destroyed when the program stops.

Visibility is similar to instance variables. However, most static variables are declared public since they must be available for users of the class.

Default values are same as instance variables. For numbers, the default value is 0; for Booleans, it is false; and for object references, it is null. Values can be assigned during the declaration or within the constructor. Additionally, values can be assigned in special static initializer blocks.

Static variables can be accessed by calling with the class name ClassName.VariableName.

When declaring class variables as public static final, then variable names (constants) are all in upper case. If the static variables are not public and final, the naming syntax is the same as instance and local variables.
Instance Variables (Non-static variables)
Instance variables are declared in a class, but outside a method, constructor or any block.

When a space is allocated for an object in the heap, a slot for each instance variable value is created.

Instance variables are created when an object is created with the use of the keyword 'new' and destroyed when the object is destroyed.

Instance variables hold values that must be referenced by more than one method, constructor or block, or essential parts of an object's state that must be present throughout the class.

Instance variables can be declared in class level before or after use.

Access modifiers can be given for instance variables.

The instance variables are visible for all methods, constructors and block in the class. Normally, it is recommended to make these variables private (access level). However, visibility for subclasses can be given for these variables with the use of access modifiers.

Instance variables have default values. For numbers, the default value is 0, for Booleans it is false, and for object references it is null. Values can be assigned during the declaration or within the constructor.

Instance variables can be accessed directly by calling the variable name inside the class. However, within static methods (when instance variables are given accessibility), they should be called using the fully qualified name. ObjectReference.VariableName.


____________________
- **Servlets** - services HTTP requests for the web server in order to create dynamic responses