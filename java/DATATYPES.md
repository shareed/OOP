## [Data Types](https://github.com/STR-FRONT-END/Java/blob/main/DATATYPES.md)
- Each variable specifies its own type
Data types are divided into two groups
#### Primitive (created by the programmer)
- specifies the size and type of variable values, and it has no additional methods
- always a value and starts with a lowercase letter
- size depends on the data type
- [includes 8 data types:](../img/javadatatypes.png) byte, short, int, long(`15000000000L`), float(`5.75f`), double(`19.99d`), boolean and char (single character, `'A'` or `'c'`: ASCII values to display certain characters, `char a = 65, b = 66, c = 67;`)
##### Numbers
Primitive number types are divided into two groups:

**Integer**
- stores whole numbers, positive or negative without decimals
- types are `byte`, `short`, `int` and `long`. Which type you should use, depends on the numeric value.

**Floating** 
- represents numbers with a fractional part, containing one or more decimals
- types are: `float` and `double`
- precision of a floating point value indicates how many digits the value can have after the decimal point( precision of float is only six or seven decimal digits, while double variables have a precision of about 15 digits)
- can also be a scientific number with an "e" to indicate the power of 10(35e3f, or 12E4d)

***The most used for numbers are int (for whole numbers) and double (for floating point numbers), but you can use other to save memory. For example, The byte data type can store whole numbers from -128 to 127. This can be used instead of int or other integer types to save memory when you are certain that the value will be within -128 and 127***


#### Non-primitive (already defined in Java)

- Examples: Strings, Arrays, Classes, Interface, etc.
- called reference types because they refer to objects
- can be null
- come with methods to perform certain operations
- starts with an uppercase letter
- all the same size
#### Reference Data Types: used to access objects
_____________________________