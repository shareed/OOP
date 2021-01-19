# JAVA basic & advanced
## [Syntax](https://github.com/STR-FRONT-END/Java/blob/main/BASICS.md)
#### Statement ( a line of code)
- Expression
- Control flow or conditional, which can be divided into decision(uses boolean logic) and loop(repeat a statement) statements 
_________________________________
## [Data Types](https://github.com/STR-FRONT-END/Java/blob/main/DATATYPES.md)
Divided into two groups
#### Primitive (created by the programmer)
- [includes 8 data types:](../img/javadatatypes.png) byte, short, int, long(`15000000000L`), float(`5.75f`), double(`19.99d`), boolean and char (single character, `'A'` or `'c'`: ASCII values to display certain characters, `char a = 65, b = 66, c = 67;`)
- Primitive number types are divided into two groups:
**Integer**
- stores whole numbers, positive or negative without decimals
- types are `byte`, `short`, `int` and `long`
**Floating** 
- represents numbers with a fractional part, containing one or more decimals
- types are: `float` and `double`


#### Non-primitive (already defined in Java)

- Examples: Strings, Arrays, Classes, Interface, etc.
- called reference types because they refer to objects
- can be null
- come with methods to perform certain operations
- starts with an uppercase letter
- all the same size
#### Reference Data Types: used to access objects
_____________________________
## [Conditional Statements](../java/CONDITIONALS.md)
### Decision making structures
- one or more conditions to be evaluated or tested by the program, along with a statement or statements that are to be executed if the condition is determined to be true, and optionally, other statements to be executed if the condition is determined to be false
### Decision making statements
- if statement 
    - Boolean expression followed by one or more statements
    - If the Boolean expression evaluates to true then the block of code inside the if statement will be executed
- if..else statement
    - if statement followed by an optional else statement, which executes when the Boolean expression is false
    - if statement can have zero or one else's
- if...else if 
    - if statement followed by an optional else if...else statement
    - if statement can have zero to many else if's
    - if using a else statement it must come last
    - if else if succeeds, none of the remaining else if's or else's will be tested.
- nested if statement
    - using one if or else if statement inside another if or else if statement
- switch statement
    -  allows a variable to be tested for equality against a list of values
    - each value is called a case
    - the variable being switched on is checked for each case
    - the variable used in a switch statement can only be integers, convertable integers (byte, short, char), strings and enums.
    - value for a case must be the same data type as the variable in the switch and it must be a constant or a literal
    - not every case needs to contain a break
    - no break is needed in the default case
__________________

## [Looping](../java/LOOPING.md) (control flow statements)
- allows us to execute a statement or group of statements multiple times
### for loop
- used to repeatedly execute a block of code a specified number of times
### while loop
- used to repeatedly execute a block of code until a specified condition is no longer satisfied
### do-while loop
- used to repeatedly execute a block of code until a specified condition is no longer satisfied, will run at least once
### Enhance For Loop
-  mainly used to traverse collection of elements including arrays
_______________________

## Classes
## Interfaces
- is like a contract between objects on how to communicate with each other
- the interface defines the methods, a deriving class(subclass) should use. But the implementation of the methods is totally up to the subclass

## Abstract Classes
## Exceptions
## Collections
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