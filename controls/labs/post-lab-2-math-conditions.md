# Lab 2: The Math class, conditional statements, and operators

### Vocabulary
**Variable**

A symbol that represents a value of a defined type. The types you are already familiar with include:
 * int: used for whole numbers (-1, 0, 1, 2, 3 etc)
 * double: used for decimal values (1.5, 4.0, etc)
 * boolean: true or false
 * String: represents a sequence of characters, always in quotes (“HelloWorld”)
 * Variables are declared as follows. Variable names have no impact on how a program works.
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

### Conditionals

Up until this point, we've thought of programs as following one path, which is each instruction from the top to the bottom. If statements and their variants allow us to break this flow a little bit. The basic structure of an if statement is:
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

**Numeric**

* `==` : equal
* `<` : less than
* `>` : greater than
* `<=` : less than or equal to
* `>=`: greater than or equal to

**Boolean**

* `&&` : AND
* `||` : OR
* `!` : NOT

The numeric operators are pretty self-explanatory, and function just like they do in algebra.

AND takes in two booleans and is true only if both are true; otherwise it's false. OR is only false if both booleans are false; otherwise it's true. NOT is a special operator, in that it only takes in one boolean. All it does is reverse a true to a false, and vice versa.

### Math Operators

The second kind of operators are mathematical operators, which output numbers instead of booleans. There are five common ones:

* `+` : addition
* `-` : subtraction
* `*` : multiplication
* `/` : division
* `%` : modulus

The first four work just like in algebra (except for division in some cases). Modulus is probably a new one, and all it is is the remainder of division. For example, ```10 % 8``` is the remainder of ```10 / 8```, 2.

The strange behavior of the division operator happens when the numbers on both sides are ints. In that case, Java rounds the answer down, so ```7 / 3``` is 2. If one or both numbers are doubles, the answer comes out as you would expect.