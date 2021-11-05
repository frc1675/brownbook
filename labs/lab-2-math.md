# Lab 2: The Math class, conditional statements, and operators

### Relevant Definitions
**Variable**

A symbol that represents a value of a defined type. The types you are already familiar with include:
 * int: used for whole numbers (-1, 0, 1, 2, 3 etc)
 * double: used for decimal values (1.5, 4.0, etc)
 * boolean: used for true / false situations (true, false)
 * String: represents a sequence of characters, always in quotes (“HelloWorld”)
 * Variables are declared as follows (the following are generic names; variable names have no impact on how a program works):
```java 
int x = 1;
double y = 3.5;
boolean z = false;
String word = “test”;
```
**Math Library**

Java provides a library of math functions available in every Java program.

Examples: ```Math.abs(); Math.sqrt(); Math.pi();```

**Operators**

Special symbols recognized by Java that perform operations on the two values on either side of them. We will go over two kinds: mathematical operators and conditional operators.

**Conditional Statements**

A line of code that Java will evaluate as true or false. The most common use of a conditional statement is in an if or if-else statement.

### Setup

1. Copy the “HelloWorld” folder to C:\dev from the previous exercise.
2. Rename the folder to be “MathExercise".
3. From the desktop open Visual Studio code.
4. Select “File” --> “Open Folder” and then choose C:\dev\MathExercise.
5. Open the file Main.java.
6. Remove old code from previous exercise from main().
7. Press the “Run” button just above the main method to make sure it works.

### Exercise #1

**Background Info**

Up until this point, we've thought of programs as following one path which is each instruction from the top to the bottom. If statements and their variations allow us to break this flow a little bit. The basic structure of an if statement is:
``` java
if (/*conditional statement 1*/) {
    //path 1
} else if (/*conditional statement 2*/) {
    //path 2
} else {
    //path 3
}
```
The ```else if``` and ```else``` parts are optional, and you can write an unlimited number of ```else if``` clauses. For the most part, we'll be using if-else statements. If what's in the parentheses is true, only the path inside the first brackets will happen. Otherwise, if what's in the parentheses is false, only the code in the second brackets will run.

The most basic conditional statement is simply a boolean value. However, we'll never write ```if (true) {```, because that defeats the whole purpose of the multiple paths our code could take! The ```else``` segment could never happen. To make more nuanced programs, we need to use conditional operators. They can be split into two kinds, those that operate on numbers and those that operate on booleans.

**Numeric:**

* == : equal
* < : less than
* /> : greater than
* <= : less than or equal to
* />= : greater than or equal to

**Boolean:**

* && : AND
* || : OR
* ! : NOT

The numeric operators are pretty self-explanatory, and function just like they do in algebra.

AND takes in two booleans and is true only if both are true; otherwise it's false. OR is only false if both booleans are false; otherwise it's true. NOT is a special operator, in that it only takes in one boolean. All it does is reverse a true to a false, and vice versa.

Ok, on to the actual exercise. 

1. Modify the HelloWorld program to have one double variable named “number”.
2. Assign any decimal value to the “number” variable.
3. Update your program to print “number is greater 0” if “number” is above 0. It should print “number is less than or equal to 0” otherwise.
4. Run your program to see the result.
5. Change the value of “number” to run both paths through the code.

### Exercise #2

1. Modify the MathExercise program to have two double variables and assign them any values.
2. Write a program that prints "Both positive" if the first double AND the second double are greater than 0. Otherwise, it should print "Not both positive".
3. Change the values of the variables so that you get the other result.

### Exercise #3

1. Modify the MathExercise program to have one double variable named “number” and assign it a value.
2. Define a second double variable named “range” and give it value.
3. Write a program that prints the message “number is within range” if “number” is less than “range” and greater than “-range”. It prints the message “number is out of range” for all other cases.
4. Run your program to see the result.
5. Change the value of “number” to run both paths through the code.

### Bonus Exercise

As alluded to before, there is something in Java called the Math class that lets you perform mathematical operations. Then all start with "Math.", and a common one is "Math.abs()". To review, the absolute value function leaves positive numbers unchanged and makes negative numbers positive. 

1. Try to rewrite the conditional statement in this program with Math.abs(). 
2. Hint: The input to the function goes inside the parentheses.

### Exercise #4

The second kind of operators are mathematical operators, which output numbers instead of booleans. There are five common ones:

* \+ : addition
* \- : subtraction
* \* : multiplication
* / : division
* % : modulus

The first four work just like in algebra (except for division in some cases). Modulus is probably a new one, and all it is is the remainder of division. For example, ```10 % 8``` is the remainder of ```10 / 8```, 2.

The strange behavior of the division operator happens when the numbers on both sides are ints. In that case, Java rounds the answer down, so ```7 / 3``` is 2. If one or both numbers are doubles, the answer comes out as you would expect.

1. Back in your MathExercise program, declare two ints or doubles, but instead of using one number as a declaration, use an expression with one or more operators. 
2. Print both of them out, but see if you can predict what will print before you press run.
3. These operators also work inside of System.out.println. Add five more print statements, one for each of the operators, and add your variables. 
4. Again, see if you can correctly predict what will print before seeing it.
