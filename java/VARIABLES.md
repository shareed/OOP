### Memory
- A computer's memory is broken up into bytes – 8 bits, or binary digits
- 8 bits makes a byte, 1024 bytes makes a kilobyte, 1024 kilobytes makes a megabyte, etc
- Every byte of memory has an address, which is where the computer knows to look for a particular value

### Variables
**Understand the idea of a variable, and how memory is used by computer programs**
- If a variable occupies more than one byte, typically the computer will know to access the variable through the address of the first byte reserved
- If any other variables are created, the computer knows to reserve memory after the initial address plus the number of bytes reserved for the variable stored there
- Computer programs use variables in the same way a math equation does – they're a store for a value of some kind, but the particular value can be changed. Some languages separate those values into groups, like integers, alphanumeric characters, or decimal numbers, called typing
- a variable is given a fixed amount of memory space that it is allowed to occupy
    - in Java, an integer variable is allowed 4 bytes – 32 bits – of memory
        1. the range of integer values that variable could store is limited to what can be expressed with 32 binary digits
        2. the amount of memory reserved is always going to be 4 bytes, even if the actual value stored doesn't require that much space
____________________


### Arrays
- an array is simply a series of reserved memory spaces for a fixed number of variables
**Example** If I have an array of 5 integers, and each integer is reserved 4 bytes of memory, my array is a chain of 20 reserved bytes of memory. 
- I can place values into this array at any point using an index. Array indices are always wrapped by brackets, because, under the hood, an array is accessed by the first memory address reserved for the first index. 
- Accessing the value in another index is simply a matter of accessing the address at…the array's first address, plus the desired index multiplied by the number of bytes reserved for each variable. 
- So if my array starts at address 2, and each integer is reserved 4 bytes, then accessing array index 3 is as simple as accessing memory address 2 + (4 * 3), or memory address 14. 
- Array values are thus said to be memory adjacent, which makes accessing the values of an array just about as fast as anything can possibly be
- we say that an accessing an array by index is done in O(1) time.No matter how big the array is, accessing the value at any index only requires one step
- copying each value will require iterating over the entire length of the old array, which is an O(n) task. So for an O(1 + N + 1) algorithm, remember that we can just say it's an O(N) task
_______________________

### Strings
- a series of alphanumeric characters, like a word or a sentence
- In most languages, these are implemented as arrays of characters, where each character is allowed a certain number of bytes for its encoding. Some languages also require the last character of a string to be a special invisible character, in case the string is shorter than the amount of reserved space, which prevents garbage data from being accidentally interpreted as part of the string. But because this is a language-specific trait, we're not going to factor it into our algorithms

**[Example:](../img/algo.png) An algorithm that determines if a given String is a palindrome. A palindrome is a series of characters that are the same when read forward or backward, like “racecar”. Generally, you ignore spaces with palindromes, but for simplicity we'll assume our input phrase has no spaces or special characters.**
- For input, we work with a string variable named “phrase”.
- For our output, we return a boolean value that will be either “true” or “false”.
- To run this algorithm, we create two new variables: “length” will be a value that stores the length of the input phrase, and “c” will be a value that stores 0, at least initially. This will be our “counter” or “cursor” variable, which refers to an index of the phrase string.
- Then we use a loop to iterate over each character in the input phrase
    - we're comparing the first character to the last character, the second character to the second-from-last character, etc.
    - We only need to iterate over half the characters in the phrase string to determine if the phrase is a palindrome.
    - So we use a while-loop, which only runs while the condition in parenthesis is true – in this case, while the value of c is less than or equal to half the length of the input phrase.
    - For every iteration of the loop, we check if the character at index “c” is not equal to the character at index “length” minus one minus “c”.
    - As “c” increments by 1 with each loop iteration, the characters compared converge toward the center of the input phrase. So, when we compare the two characters, if they're not equal then we know the phrase cannot be a palindrome, and we return false.- Returning a value always ends the algorithm immediately, and most languages only allow you to return one value.
    - If the characters actually do match, the value of c is incremented, and the loop continues.
    - If every character in the first half of the phrase matches every character in the second half in reverse order, the word is a palindrome and the loop will exit when “c” is greater than half the length of the phrase.
    - When the loop exits this way, the word must be a palindrome, and so the value “true” is returned.
- The act of creating variables, returning values, and checking conditions are all O(1) operations – they're just a single step or statement.
- Each iteration of a loop can also be said to be O(1). But our loop iterates over characters in the input phrase, and the longer the input phrase is, the more loop iterations our algorithm will have.
- At first glance, we could try saying this algorithm is O(1 + 1 + n/2 + 1), where n is the number of characters in the input phrase.But we know that we discard coefficients and smaller scaling factors, so this algorithm is really just O(n).
____________________________________-

### List
- By increasing the size so much at once, the number of times the list has to increase in size is reduced
- insertion time is **amortized out**, as the list increases in size, the time spent copying arrays over is less than the actual number of elements O(1)
_______________________________

### Linked List 
- to guarantee that inserting or deleting an element from your data structure is actually O(1)
- you only ever need to perform 3 steps to insert: get the address of the node that will come after your inserted node, set your new node to point to that address, and then update the address of the previous node's neighbor variable to point to your new node
- Deleting is even easier – just set the “next” address of the previous node to the address of the node that comes after the one you're removing.
- this is really only that fast if you're inserting or removing at the head of a linked list, and the tail of a doubly-linked list.Inserting or removing from somewhere in the middle of the list would first require searching to that position, which makes the overall operation O(n).
- has variables that contain the memory address of the next or prior node in the sequence
- the first node in the list, called the head
- to retrieve a value from the list, you check the head. If the head doesn't contain the value you want, then you get the address of the next node from the head, and check that one. If that node doesn't have the value you want, you get the address of the next node, and check that one, and so on
-  searching for an element in a linked list is O(n), because we have to traverse multiple nodes to find what we're looking for

**[Example:](../img/algo2.png)** write an algorithm that removes all duplicate values from the linked list(you're not allowed to create any kind of buffer to memorize values you have already seen). The only input we need for this is the head of the linked list, which is a node. This algorithm won't have any output, it just removes items from the list that it's given. Because the list is singly-linked, we can only move forward through the list's nodes, not backwards.
- create a variable that refers to the current node. This will start as the head node
- for each node we'll need to check every node that comes after the current one to see if they have duplicate values.
- use a runner, a second variable that runs through the rest of the list repeatedly, starting at whatever the current node is, and stopping at the last node.
- while the current node is not the end of the list, we'll create a runner. 
    - The runner starts at the same node as the current one. While that runner is not at the end of the list, we'll check if the data of the node after the runner matches the data at the current node. 
    - If it does, we remove that node by linking the runner to the node that comes after the next one. That is, if the runner is at node 1, it compares the data of node 2 to the data of node 1. 
    - If the two data match, then node 3 is linked to node 1, cutting node 2 out of the list. 
    - Otherwise, if there's no match, the runner is moved to the next node. 
    - This loop will run until the runner is at the end of the list. When it ends, the current node is moved to the next node in the list after the head, and the process continues. 
- When the algorithm finishes, The loop will have checked every node, and removed every duplicate of each node that came after the first occurrence. 
- This algorithm iterates over the list once with the “current” pointer, but the “runner” pointer also iterates over each node, each iteration containing one less node than the one before it.
- This will run in O(n^2) time – a rather complex algorithm, but the best we can do without being able to track what numbers we've encountered as we iterate through.

**How do we know it's O(n^2)? [Let's plot it out.](../img/bigo5.png)**
- linked list with 4 nodes, like a chain 
- Beneath that, is the number of iterations the first loop will run – one for each node, so 4
- For each iteration, check if the runner visited the corresponding node
- In the first iteration, the runner starts at the head, and checks the data of each node after that, until the runner exits the list – when the runner is null
- Then on the next iteration, the current pointer will be at the second node, and the runner visits that node and every one thereafter
- This continues on, and we notice that our checkboxes form the shape of a half-filled in square. We know the area of a square is x^2, and half that is of course x^2/2.
- Our nested loops therefore run O(n^2/2) times, but with Big-O notation we ignore coefficients, so that simplifies to O(n^2).

**In practice, linked lists aren't used as much as other data structures. Plain lists or arrays are better for just storing elements, and there are other data structures that are just as fast at inserts and deletes, and faster at searching. But linked lists still have their place, and you should understand how to use them.**
________________________

### TREES and GRAPHS
#### Graphs
- a series of nodes that each may or may not have child nodes
- These nodes may direct to each other in a circular fashion, and they may be bi-directional, i.e.nodes A and B both have each other as child nodes
- It’s also possible to have isolated subgraphs – that is, collections of nodes that are part of the same graph, but no connection exists between them.
- you will use them to emulate real life data structures, you could use them for mapping out the web of friend relationships on social media, or to represent intersections from a street map. 
- whatever data you are representing with a graph, you’re most often going to be using the graph in searches. When searching a graph, there are two common approaches: breadth-first search, and depth-first search.
- Both searches start at the head or root node. 

##### Depth-first search
- you progress through each branch completely before moving on to the next branch
- This is best used when you are searching for a specific node, or when you want to guarantee that you check every one
- A depth-first search uses this [algorithm](../img/dfs.png).

  - need some way of tracking whether a node has been visited already or not. Without this, you would search one branch all the way down to the lowest level child node, then loop back up to its parent, and then search the child node again in an infinite loop
    - this algorithm is recursive – that is, it calls itself with new data every time it runs, until it is done
    - Here’s a visualization of a [DFS](../img/dfs1.png) in action
        - start at A, our root node, and we are searching for ‘E’. A isn’t our target, so we mark A as visited and start searching the children
        - The first child we visit is C, which doesn’t match the value we’re looking for.
        - We mark C as visited, and search its children
        - F isn’t our target, so its marked as visited, but F also has no children, so the for each loop is skipped.This search returns null.
        - Now the loop that was started when we searched C can continue, and we search G. G doesn’t match, so we search its child H. H doesn’t match so we search its child D. 
        - D doesn’t match, and D has no children – note that the links are unidirectional – so we return null and back up to H. No more children, so H’s loop finishes and we back up to G, then to C, then to A. C has no children that haven’t been visited so we go back to A
        - A has another child, D… but D has been visited, so we move to E
        - Finally, E matches our value and we return E
        - No more searching needed

**A depth-first search covers searches through every available child node before moving to a neighbor and can be written recursively or iteratively with a stack**

##### Breadth-first search
- you explore each neighbor before moving on to any children
- This is useful when you’re trying to find a path from A to B. 
- A breadth-first search uses this [algorithm](../img/bfs.png).
    - example of an iterative BFS algorithm. 
    - Starting with the first node, the current node is added to a queue
    - Then the next item in the queue is removed and checked for a match
    - If it doesn't match, its children are added to the back of the queue for later checking.

- Here we have the same graph as shown before, but we're going to search it for E with our [BFS algorithm](../img/bfs1.png).
    - A is added to the queue, then removed and checke
    - A doesn't match, so we add C, D, E, and B to the queue going left to right
    - The next item to get pulled from the queue is C, which doesn't match, so its children F and G are added to the back of the queue
    - D is then removed and checked, and has no match or children to queue up
    - Then we check E, and there's a match so the algorithm returns that node and quits
- a breadth-first search visits every neighbor of a node before visiting any children
- a breadth-first search uses a queue to track which nodes it still needs to visit.You typically use a BFS to find a route from one node to another


#### Trees
**So graphs can be useful structures, but they're more useful when they have some structure and rules.That's where trees come in**

- are a subtype of graph, but do not contain any cycles, where node connections loop back into each other.
- A node with no children is called a leaf node.Oftentimes, a tree will be restricted as to how many children each node can have.A tree that only allows two children – the most common type of tree – is called a binary tree.Binary trees are used often because if they are sorted, they can be easy to search through.A sorted binary tree is called a binary search tree, and it requires that for every node, all lefthand children must be less than or equal to the node, and that node must be less than all righthand children.This is an example of a binary search tree, but this is not.The second tree fails because each node requires that all lefthand children be less than it, and this is not true for the root node – 15 is not less than 10.Furthermore, the rule also states that all righthand children of a node must be greater than that node, and 9 is not greater than 10.Searching a binary search tree can happen in LogN time, because the tree is sorted.Every time you check a node, you know if the current node is less than or greater than your target, and you can cut the remaining number of nodes in half each time.The same goes for inserting, because you can quickly find where an item should be inserted to maintain the sorted property.A binary search tree is said to be balanced when the size of each subtree for a node is roughly the same size as all other subtrees of neighbor nodes in the same level.This doesn't have to be exact, just close enough that the search complexity remains close to LogN.A complete binary tree is a tree where every level is filled.The last level of the tree is allowed to remain partially filled, so long as it is filled left-to-right.A full binary tree is one where every level has exactly 0 or 2 children.A perfect binary tree is both full and complete.When traversing a tree and not performing a search, there are three ways of doing so: In-order traversal, pre-order, and post-order.You should know how to implement all of them, but thankfully they're all rather simple.An in-order traversal visits the left child before the current node, then the right child.This is true for every node, and the recursive algorithm looks like this.In a binary search tree, in-order traversal will visit every element in ascending order.Pre-order traversal visits the current node before exploring the left and right child, and post-order visits the node after the left and right child.When implemented recursively, these algorithms are easy to differentiate and remember.Trees – particularly binary search trees – have a lot of uses in algorithm design.They are also used behind the scenes to implement some advanced and efficient data structures.Graphs make for a great approximation of real-life structures, like internet connectivity routes, or for pathfinding in video games..
__________________________

  