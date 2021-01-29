# Interface
- a reference type that is similar to class but is just a collection of abstract methods, constants, default methods, static methods, and nested types. Method bodies exist only for default methods and static methods.
- a class implements an interface, thereby inheriting the abstract methods of the interface
- a class describes the attributes and behaviors of an object but an interface contains behaviors that a class implements
- Unless the class that implements the interface is abstract, all the methods of the interface need to be defined in the class.

##### Similarities between an interface and a class
- An interface can contain any number of methods.
- An interface is written in a file with a .java extension, with the name of the interface matching the name of the file.
- The byte code of an interface appears in a .class file.
- Interfaces appear in packages, and their corresponding bytecode file must be in a directory structure that matches the package name.

##### Differences between an interface and a class
- You cannot instantiate an interface.
- An interface does not contain any constructors.
- All of the methods in an interface are abstract.
- An interface cannot contain instance fields. The only fields that can appear in an interface must be declared both static and final.
- An interface is not extended by a class, it is implemented by a class.
- An interface can extend multiple interfaces.

### Declaring Interfaces
- `interface Animal{public void eat();}`

### Implementing Interfaces
**When a class implements an interface it agrees to perform the specific behaviors of the interface. If a class does not perform all the behaviors of the interface, the class must declare itself as abstract**

A class uses the implements keyword to implement an interface. The implements keyword appears in the class declaration following the extends portion of the declaration.
```
    public class MammalInt implements Animal {

        public void eat() {
            System.out.println("Mammal eats");
        }
    }
```
- A class can implement more than one interface at a time.
- A class can extend only one class, but implement many interfaces.
- An interface can extend another interface, in a similar way as a class can extend another class.

### Extending Interface
**An interface can extend another interface in the same way that a class can extend another class. The extends keyword is used to extend an interface, and the child interface inherits the methods of the parent interface**

[Extending Interface Example](../img/interface1.png)
- Hockey interface has four methods, but it inherits two from Sports
- Thus, a class that implements Hockey needs to implement all six methods
- Similarly, a class that implements Football needs to define the three methods from Football and the two methods from Sports. 


### Extending Multiple Interfaces
Interfaces are not classes, and can extend more than one parent interface.

The extends keyword is used once, and the parent interfaces are declared in a comma-separated list.
`public interface Hockey extends Sports, Event`
_____________________
Abstract Classes VS Interfaces.
Below is a list of some differences between the two:

- A class can extend only one class (abstract or not) but can implement multiple interfaces
- Interface variables are implicitly public static final
- Abstract classes can declare any modifiers on instance variables
- Interfaces can (as of Java 8) provide default methods, but all others are public abstract
- Abstract classes can declare any modifiers on their methods
**If you wanted to develop and enforce a certain hierarchy of functionality where state and behavior was tracked, then you would use an abstract class**

**If you want a class to be free to implement functionality without constrained to a hierarchy, then an interface is a better approach**