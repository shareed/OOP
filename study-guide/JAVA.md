# JAVA
## Syntax
#### Statement ( a line of code)
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

## Interfaces
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

## Exceptions
- different errors can occur: coding errors made by the programmer, errors due to wrong input, or other unforeseeable things
### TRY and CATCH
- **try** statement allows you to define a block of code to be tested for errors while it is being executed
- **catch** statement allows you to define a block of code to be executed, if an error occurs in the try block
- **finally** statement lets you execute code, after try...catch, regardless of the result
- **throw** statement allows you to create a custom error
    - - used together with an exception type. There are many exception types available in Java: ArithmeticException, FileNotFoundException, ArrayIndexOutOfBoundsException, SecurityException, etc:

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
Local Variables
Class Variables (Static Variables)
Instance Variables (Non-static variables)



____________________
- **Servlets** - services HTTP requests for the web server in order to create dynamic responses