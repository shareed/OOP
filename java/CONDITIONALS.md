## Conditional Statements
**Decision Making Structures**
- have one or more conditions to be evaluated or tested by the program, along with a statement or statements that are to be executed if the condition is determined to be true, and optionally, other statements to be executed if the condition is determined to be false. 

Java programming language provides following types of decision making statements. 

- if statement
- if..else statement
- nested if statement
- switch statement

### IF Statement
`if(Boolean_expression) {// Statements will execute if the Boolean expression is true}`
- consists of a Boolean expression followed by one or more statements
- if the Boolean expression evaluates to true then the block of code inside the if statement will be executed
- if not, the first set of code after the end of the if statement (after the closing curly brace) will be executed.

### IF..ELSE Statement
```
    if(Boolean_expression) {
        // Executes when the Boolean expression is true
    }else {
        // Executes when the Boolean expression is false
    }
```
-  can be followed by an optional else statement, which executes when the Boolean expression is 


### IF..ELSE IF Statement
**An if statement can be followed by an optional else if...else statement, which is very useful to test various conditions using single if...else if statement.**
```
    if(Boolean_expression 1) {
        // Executes when the Boolean expression 1 is true
    }else if(Boolean_expression 2) {
        // Executes when the Boolean expression 2 is true
    }else if(Boolean_expression 3) {
        // Executes when the Boolean expression 3 is true
    }else {
        // Executes when the none of the above condition is true.
    }
```

- `if` can have zero or one else's and it must come after any else if's.
- `if` can have zero to many else if's and they must come before the else.
- once an else if succeeds, none of the remaining else if's or else's will be tested.

### Nested IF Statement
**It is always legal to nest if-else statements which means you can use one if or else if statement inside another if or else if statement.**

```
    if(Boolean_expression 1) {
        // Executes when the Boolean expression 1 is true
    if(Boolean_expression 2) {
        // Executes when the Boolean expression 2 is true
    }
    }
```

### SWITCH Statement
```
switch(expression) {
   case value :
      // Statements
      break; // optional
   
   case value :
      // Statements
      break; // optional
   
   // You can have any number of case statements.
   default : // Optional
      // Statements
}
```
- allows a variable to be tested for equality against a list of values
- each value is called a case, and the variable being switched on is checked for each case.

##### Rules for [SWITCH Statement](../img/switch.png)
- The variable used in a switch statement can only be integers, convertable integers (byte, short, char), strings and enums.
- You can have any number of case statements within a switch. Each case is followed by the value to be compared to and a colon.
- The value for a case must be the same data type as the variable in the switch and it must be a constant or a literal.
- When the variable being switched on is equal to a case, the statements following that case will execute until a break statement is reached.
- When a break statement is reached, the switch terminates, and the flow of control jumps to the next line following the switch statement.
- Not every case needs to contain a break. If no break appears, the flow of control will fall through to subsequent cases until a break is reached.
- A switch statement can have an optional default case, which must appear at the end of the switch. The default case can be used for performing a task when none of the cases is true. No break is needed in the default case.