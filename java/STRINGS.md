## Strings
- a sequence of characters that are treated as objects
- Java platform provides the `String` class to create and manipulate strings
- The String class has 11 constructors that allow you to provide the initial value of the string using different sources, such as an array of characters
- `String greeting = "Hello World";`
    - this string literal creates a string object with the value "Hello World"
- you can create String objects by using the new keyword and a constructor
[String Example](../img/string1.png)
**Note : The String class is immutable, so that once it is created a String object cannot be changed. If there is a necessity to make a lot of modifications to Strings of characters, then you should use String Buffer & String Builder Classes**

### String Length
Methods used to obtain information about an object are known as accessor methods. One accessor method that you can use with strings is the length() method, which returns the number of characters contained in the string object. 

### Concatenating Strings
The String class includes a method for concatenating two strings :
    - `string1.concat(string2);` returns a new string that is string1 with string2 added to it at the end
- You can also use the concat() method with string literals 
    -`"My Name is".concat("Zara");`  
    - Strings are most commonly concatenated with the "+" operator `"Hello," + " world" + "!`

### Some String Handling Methods 
- **char charAt(int index)**  - Returns the character at the specified index. 
- **int compareTo(Object o)** - Compares this String to another Object. 
- **String concat(String str)**  - Concatenates the specified string to the end of this string. 
- **boolean equals(Object anObject)** - Compares this string to the specified object. 
- **boolean equalsIgnoreCase(String anotherString)** - Compares this String to another String, ignoring case considerations. 