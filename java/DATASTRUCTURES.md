# DataStructures
**When programmers need to organize their data, they use data structures. These are standardized patterns of code designed to organize one or more variables**
## Array
**An array is a linear collection of variables of uniform size, and in typed languages, uniform type**
- An object which contains elements of a similar data type
- It is a data structure where we store similar elements
- We can store only a fixed set of elements in a Java array.
- index-based, the first element of the array is stored at the 0 index.
- Typically, arrays store sequential pieces of data near one
another in memory and thus searching through arrays is a quick operation to perform

**Advantages**
- Code Optimization: It makes the code optimized, we can retrieve or sort the data efficiently.
- Random access: We can get any data located at an index position
**Disadvantages**
- Size Limit: We can store only the fixed size of elements in the array. It doesn't grow its size at runtime. To solve this problem, collection framework is used in Java which grows automatically. 
**An array reserves a certain amount of adjacent bytes in memory - enough to fit a predetermined number of variables, this guarantee makes searching through an array very fast, because at the lowest level, the computer always knows where to look for the next variable, and it never has to look far. The guarantee also allows arrays to allow access to their contents by an index.**
**Types of Array**
- Single Dimensional Array
- Multidimensional Array
[Example](../img/array.png)
_________________________

## List/Vector
**What if you don’t care about memory adjacency, and you want a collection that can grow or even shrink as needed?Well in that case, you would use a List, sometimes called a Vector**
- A list is like an array, but provides support for adding/removing elements via methods. Generally, a
List/Vector is an implementation of an array behind the scenes
- when a the array in a vector or list gets full, it automatically creates a new array that is larger - often double the size of the previous array - and copies the contents of the old array into the new one.When an element is removed from a vector or a list, the elements after the now-empty position are usually shifted down to close the gap
- these features are a tradeoff of performance for flexibility
________________________

## Stacks
- Stacks are similar to Lists, but they enforce a procedure for accessing their elements
- LIFO(Last In First Out)

____________________________________________

## Queue
- A Queue is like a stack but typically enforces a FIFO procedure for adding/removing elements
- The Queue interface is available in java.util package and extends the Collection interface
- The queue collection is used to hold the elements about to be processed and provides various operations like the insertion, removal etc. It is an ordered list of objects with its use limited to insert elements at the end of the list and deleting elements from the start of list i.e. it follows the FIFO or the First-In-First-Out principle.
- LinkedList, ArrayBlockingQueue and PriorityQueue are the most frequently used implementations. 
__________________

## Link List
- A Linked List is linear like a list
- has no index, and are not an wrapper for an array
- it is composed of nodes
- Each node keeps track of another node and this forms a link or chain of elements 
- Adding/Removing elements to the middle of a linked list is a slow process, because you have to search
through several nodes (down the chain) until you find your point of inserting/deleting the node.
- A singly-linked list is a uni-directional link of nodes. Each node only knows about the node in front of it.
- A doubly-linked list is bi-directional. Each node knows about the node in front of it and behind it. 
______________________________

## Maps/Dictionary
- A map is a collection of key/value pairs. One node is considered a key and it points to another which is
considered the value. Together they form a pair, similar to how a dictionary associates a word (key) to
its definition (value)
___________________________

## Collection Interface
**The Collection interface is the foundation upon which the collections framework is built. It declares the core methods that all collections will have. A collections framework is a unified architecture for representing and manipulating collections. All collections frameworks contain the following:**

- **Interfaces** − These are abstract data types that represent collections. Interfaces allow collections to be manipulated independently of the details of their representation. In object-oriented languages, interfaces generally form a hierarchy.
- **Implementations, i.e., Classes** − These are the concrete implementations of the collection interfaces. In essence, they are reusable data structures.
- **Algorithms** − These are the methods that perform useful computations, such as searching and sorting, on objects that implement collection interfaces. The algorithms are said to be polymorphic: that is, the same method can be used on many different implementations of the appropriate collection interface.
**In addition to collections, the framework defines several map interfaces and classes. Maps store key/value pairs. Although maps are not collections in the proper use of the term, but they are fully integrated with collections**
________________________________________

## The List Interface
**The List interface extends Collection and declares the behavior of a collection that stores a sequence of elements.**
- Elements can be inserted or accessed by their position in the list, using a zero-based index.
- A list may contain duplicate elements.
- In addition to the methods defined by Collection, List defines some of its own, which are summarized in the following table.
- Several of the list methods will throw an UnsupportedOperationException if the collection cannot be modified, and a ClassCastException is generated when one object is incompatible with another. 
___________________________

## ArrayList
**ArrayList is a part of collection framework and is present in java.util package. It provides us dynamic arrays in Java. Though, it may be slower than standard arrays but can be helpful in programs where lots of manipulation in the array is needed.**

- ArrayList inherits AbstractList class and implements List interface.
- ArrayList is initialized by a size, however the size can increase if collection grows or shrunk if objects are removed from the collection.
- Java ArrayList allows us to randomly access the list.
- ArrayList can not be used for primitive types, like int, char, etc. We need a wrapper class for such cases.
**Code to create a generic integer ArrayList**
    `ArrayList<Integer> arrli = new ArrayList<Integer>();`
___________________________

## The Set Interface
- A Set is a Collection that cannot contain duplicate elements. It models the mathematical set abstraction.
- The Set interface contains only methods inherited from Collection and adds the restriction that duplicate elements are prohibited.
- Set also adds a stronger contract on the behavior of the equals and hashCode operations, allowing Set instances to be compared meaningfully even if their implementation types differ.
_________________________

## The Map Interface
**The Map interface maps unique keys to values. A key is an object that you use to retrieve a value at a later date.**

- Given a key and a value, you can store the value in a Map object. After the value is stored, you can retrieve it by using its key.
- Several methods throw a NoSuchElementException when no items exist in the invoking map.
- A ClassCastException is thrown when an object is incompatible with the elements in a map.
- A NullPointerException is thrown if an attempt is made to use a null object and null is not allowed in the map.
- An UnsupportedOperationException is thrown when an attempt is made to change an unmodifiable map.
_____________________
[List, Set and Map Example](../img/collectionsexamples.png)


