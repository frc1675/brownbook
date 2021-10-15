# Lab 2: Basic Java math

### Definitions:

* **Operators**: Special characters recognized by Java that perform some sort of action.

### Common operators

There are five basic math operators in Java:
* **\+** \-\-\- addition
* **\-** \-\-\- subtraction
* **\*** \-\-\- multiplication
* **/** \-\-\- division
* **%** \-\-\- modulus

The first four work the same as they do in math class, for the most part. The exception is division of ints. If you use division and both numbers are ints, the result will be rounded down to the nearest integer. For example, ```9 / 5``` is 1, not 1.8.

An easy way to think of modulus is taking the remainder of division. For example, ```7 % 5``` is the remainder of ```7 / 5```, 2.

### Exercise #1
Go back to your Hello World program and take a look at your int and double variables. Instead of declaring (creating) them with one value, come up with an expression that uses an operator to declare the same value. Then run your program to make sure that it has the expected behavior.
### Bonus exercise
Use an expression with two or more operators to initailize the variables. Java has an order of operations, just like math class, so you can also use parentheses to order things.

### Exercise #2
Add some extra print statements to your Hello World program so that you add, subtract, multiply, divide, and do the modulus of your int and double variables together. See if you can reason why you got the numbers that you did.

### Important note
Java has another use of the \+ operator when it comes to Strings, called concatenation. Concatenation is simply creating a new String that is two or smaller ones in order, so it makes sense to use a plus sign. 

These two lines will print the exact same thing, but one uses concatenation:
```java
System.out.prinln("Hello World");
System.out.println("Hello" + " " + "World");
