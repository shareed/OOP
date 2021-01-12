## Looping Constructs
**A loop statement allows us to execute a statement or group of statements multiple times**

**Types Of Loops in Java:** 
- While loop
- For loop
- Do..While loop

### While Loop
**A while loop statement in Java programming language repeatedly executes a target statement as long as a given condition is true**
- `while(Boolean_expression) {// Statements}`
- statement(s) may be a single statement or a block of statements
- the condition may be any expression, and true is any non zero value. 
- if the boolean_expression result is true, then the actions inside the loop will be executed. This will continue as long as the expression result is true.
- when the condition becomes false, program control passes to the line immediately following the loop.
[While Loop Example](../img/whileloop.png)

### For Loop
- `for(initialization; Boolean_expression; update) {// Statements}`
- a repetition control structure that allows you to efficiently write a loop that needs to be executed a specific number of times
- useful when you know how many times a task is to be repeated.
##### Steps
1. **initialization** 
    - is executed first, and only once
    - allows you to declare and initialize any loop control variables and this step ends with a semi colon (;)
2. **Boolean expression**
    - if it is true, the body of the loop is executed, if it is false, the body of the loop will not be executed and control jumps to the next statement past the for loop.
3. **update statement** 
    - after the body of the for loop gets executed, the control jumps back up to the update statement
    - allows you to update any loop control variables
    - can be left blank with a semicolon at the end.
4. **Boolean expression**
    - is now evaluated again. If it is true, the loop executes and the process repeats (body of loop, then update step, then Boolean expression)
    - After the Boolean expression is false, the for loop terminates

[For Loop Example](../img/forloop.png)


### Do..While Loop
**A do...while loop is similar to a while loop, except that a do...while loop is guaranteed to execute at least one time.** 

- `do {// Statements}while(Boolean_expression);`
- the Boolean expression appears at the end of the loop, so the statements in the loop execute once before the Boolean is tested
- if the Boolean expression is true, the control jumps back up to do statement, and the statements in the loop execute again
- This process repeats until the Boolean expression is false.

[Do...While Loop Example](../img/dowhileloop.png)

### Enhanced For Loop
As of Java 5, the enhanced for loop was introduced. This is mainly used to traverse collection of elements including arrays. 
- `for(declaration : expression) {// Statements}`
    1. **Declaration** − The newly declared block variable, is of a type compatible with the elements of the array you are accessing. The variable will be available within the for block and its value would be the same as the current array element.
    2. **Expression** − This evaluates to the array you need to loop through. The expression can be an array variable or method call that returns an array.

[Enhanced For Loop Example](../img/enhancedforloop.png)