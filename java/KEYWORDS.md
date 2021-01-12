## Keywords
### Usage of "this" keyword 
**In java, this is a reference variable that refers to the current object.**
**6 usage of java this keyword**
1. `this` can be used to refer current class instance variable.
2. `this` can be used to invoke current class method (implicitly)
3. `this()` can be used to invoke current class constructor.
4. `this` can be passed as an argument in the method call.
5. `this` can be passed as argument in the constructor call.
6. `this` can be used to return the current class instance from the method.


**["this" : to refer current class instance variable](../img/this1.png)**
- The this keyword can be used to refer current class instance variable. If there is ambiguity between the instance variables and parameters, this keyword resolves the problem of ambiguity. 

**["this" : to invoke current class method](../img/this2.png)**
- You may invoke the method of the current class by using the this keyword. If you don't use the this keyword, compiler automatically adds this keyword while invoking the method. 

**["this" : to invoke current class constructor](../img/this3.png)**
- The this() constructor call can be used to invoke the current class constructor. It is used to reuse the constructor. In other words, it is used for constructor chaining. 


### Usage of the "new" keyword
When you are declaring a class in java, you are just creating a new data type. A class provides the blueprint for objects. You can create an object from a class. 

1. **Declaration**, you must declare a variable of the class type. This variable does not define an object `Student anil`

2. **Instantiation and Initialization**, you must acquire an actual, physical copy of the object and assign it to that variable
    - You can do this using the new operator. The new operator instantiates a class by dynamically allocating(i.e, allocation at run time) memory for a new object and returning a reference to that memory
    - This reference is then stored in the variable. Thus, in Java, all class objects must be dynamically allocated. 
    - The new operator is also followed by a call to a class constructor, which initializes the new object. A constructor defines what occurs when an object of a class is created. Constructors are an important part of all classes and have many significant attributes.
    - Let us say that we have a class called Student and we need to instantiate this class `Student anil = new Student();`

### Usage of "super" keyword
**The super keyword is a reference variable which is used to refer immediate parent class object.**
- Whenever you create the instance of subclass, an instance of parent class is created implicitly which is referred by super reference variable.
- can be used to refer immediate [parent class instance variable](../img/super1.png)
    -  access the data member or field of parent class. It is used if parent class and child class have same fields.
- can be used to invoke immediate [parent class method](../img/super2.png)
    -  invoke parent class method. It should be used if subclass contains the same method as parent class. In other words, it is used if method is overridden. 
- `super()` can be used to invoke immediate [parent class constructor](../img/super3.png)
    - `super()` has to be in the first line within the subclass constructor


### Static Keyword
- used for memory management mainly
- can apply  with variables, methods, blocks and nested class
- belongs to the class than an instance of the class. 

The static can be:
- Variable (also known as a class variable)
- Method (also known as a class method)
- Block
- Nested class

**Static variable**
`static String college ="ITS";`
- can be used to refer to the common property of all objects (which is not unique for each object), for example, the company name of employees, college name of students, etc.
- gets memory only once in the class area at the time of class loading.
- makes your program memory efficient (i.e., it saves memory). 
[Static Keyword Example](../img/static1.png)
[Static Keyword Example Diagram](../img/static2.png)


### Final Keyword
- used to restrict the user
- can be used in many context
- Final can be:
    - [variable: stops value change](../img/final1.png)
    - [method: stops method overidding](../img/final2.png)
    - [class: stops inheritance](../img/final3.png)
The final keyword can be applied with the variables, a final variable that have no value it is called blank final variable or uninitialized final variable. It can be initialized in the constructor only. The blank final variable can be static also which will be initialized in the static block only.