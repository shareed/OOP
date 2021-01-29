# Java Errors
- There are two types of errors:

1. Compile time errors
    - Compile time errors can be again classified into two types:
        1. Syntax Errors
            - Instead of declaring `int a;` you mistakenly declared it as `in a;` for which compiler will throw an error.
        2. Semantic Errors
            - You have declared a variable int a; and after some lines of code you again declare an integer as int a;. All these errors are highlighted when you compile the code

2. Runtime errors
    - A Runtime error is called an Exceptions error. It is any event that interrupts the normal flow of program execution.
    - arithmetic exception, Nullpointer exception, Divide by zero exception, etc.


# Exceptions
**An Exception is a specific subclass of Throwable and it represents all possible exceptions that may occur within your program and are out of developers control, they are events that occur during the execution of programs that disrupt the normal flow of instructions (e.g. divide by zero, array access out of bound, etc.)**

- an exception is an object that wraps an error event that occurred within a method and contains: 
    1. Information about the error including its type 
    2. The state of the program when the error occurred 
    3. Optionally, other custom information 


**Exceptions are further divided into checked and unchecked exceptions**

**Categories of Exceptions**

- Checked Exceptions
- Unchecked Exceptions
- Errors

### Checked Exceptions
**You must handle any checked exception in code by either using a try/catch/finally block or by rethrowing the exception using the throws keyword**
- The compiler enforces that you handle them explicitly. 
- Methods that generate checked exceptions must declare that they throw them. 
- Methods that invoke other methods that throw checked exceptions must either handle them (they can be reasonably expected to recover) or let them propagate by declaring that they throw them. 
[Example](../img/exception1.png)
**If you use FileReader class in your program to read data from a file, if the file specified in its constructor doesn't exist, then a FileNotFoundException occurs, and the compiler prompts the programmer to handle the exception**. 

### Unchecked Exceptions
- Errors and RuntimeExceptions(parent class of all unchecked exceptions) are unchecked — that is, the compiler does not enforce (check) that you handle them explicitly. 
- Methods do not have to declare that they throw them (in the method signatures). 
- It is assumed that the application cannot do anything to recover from these exceptions (at runtime). 
[Example](../img/exception2.png)
**If you have declared an array of size 5 in your program, and trying to call the 6th element of the array then an ArrayIndexOutOfBoundsException occurs.** 

### Errors
These are not exceptions at all, but problems that arise beyond the control of the user or the programmer. Errors are typically ignored in your code because you can rarely do anything about an error. 
**For example, if a stack overflow occurs, an error will arise. They are also ignored at the time of compilation.**
________________________

## [Exception Hierarchy](../img/exceptionhierarchy3.png)
 - All exception classes are subtypes of the [java.lang.Exception class](../img/exceptionhierarchy.png). 
### Throwable Class
- All exception classes are subclass of the Throwable class, they extend the Throwble class
- **The Exception class** represents the exceptions that can be handled by our program, and our program can be recovered from this exception using try and catch block
    - **A Runtime exception** is a sub-class of the exception class. The Exception of these type represents exception that occur at the run time and which cannot be tracked at the compile time. An excellent example of same is divide by zero exception, or null pointer exception, etc
    - **IO exception** is generated during input and output operations
    - **Interrupted exceptions** in Java, is generated during multiple threading.
- Other than the exception class there is another subclass of Throwable called Error. It defines the exception or the problems that are not expected to occur under normal circumstances by our program, example Memory error, Hardware error, JVM error, etc 

## [Catching Exceptions](../img/exceptioncatching.png)
**You must handle any checked exception in code by either using a try/catch/finally block or by rethrowing the exception using the throws keyword**
- A method catches an exception using a combination of the try and catch keywords
- A try/catch block is placed around the code that might generate an exception
- Code within a try/catch block is referred to as protected code

**[Catching Exceptions Example](../img/exceptioncatching2.png)** which has an array declared with 2 elements, the code tries to access the 3rd element of the array which throws an exception
- The code which is prone to exceptions is placed in the try block
- When an exception occurs, that exception occurred is handled by catch block associated with it
- Every try block should be immediately followed either by a catch block or finally block.
- A catch statement involves declaring the type of exception you are trying to catch
- If an exception occurs in protected code, the catch block (or blocks) that follows the try is checked
- If the type of exception that occurred is listed in a catch block, the exception is passed to the catch block much as an argument is passed into a method parameter.

### The [Throw/Throws](../img/throwthrows.png) Keyword
**If a method does not handle a checked exception, the method must declare it using the throws keyword.**
- The throws keyword appears at the end of a method's signature. 
- can throw an exception, either a newly instantiated one or an exception that you just caught, by using the throw keyword. 
- throws is used to postpone the handling of a checked exception
- throw is used to invoke an exception explicitly. 

### [Finally Block](../img/finally.png)
- The finally block follows a try block or a catch block
- A finally block of code always executes, irrespective of occurrence of an Exception.
- Using a finally block allows you to run any cleanup-type statements that you want to execute, no matter what happens in the protected code.
- A finally block appears at the end of the catch blocks and has the following syntax 
[Example](../img/finallyblockexample.png)
[Replit](https://repl.it/@shanreed1/exceptions2-1#Main.java)
___________________