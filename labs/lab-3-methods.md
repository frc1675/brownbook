# Organizing Your Code With Methods

### Definitions

* **Method**
   *  A named section of a program that performs a specific task.
   * Methods often return output when provided input. The example below computes the addition of two numbers, a and b. 
     ```java
     double add(double a, double b) {
        return a + b;
     }
     ```
   * They have the following general form: ```[return type] [name]([argument type] [argument name])```. A method can have any number of arguments separated by commas, including 0.
   * Therefore, the above example has a return type of double, a name of add, an argument type of double two doubles, and argument names a and b.
   * Methods can also return ```void``` (which means nothing) and in this case do not require a ```return``` statement.
   * Use methods to organize your code by grouping related code together.
   * Use methods to reduce duplication of code for operations that must be performed many times.
   * You are already familiar with methods through your experience with ```System.out.println()``` and ```Math.abs()```.
   
### Exercise #1

* Below is a Java program designed to print out where each member of the team goes to school:
```java
public final class Main {
    private Main() {
    }
    
    public static void printNameAndSchool(String fName, String lName, String school){
        // Add your code here.
    }

    public static void main(String[] args) {
        String firstName  = "John";
        String lastName = "Smith";
        String school = "King";
        System.out.println(firstName+" "+lastName+" goes to "+school);

        firstName  = "Jane";
        lastName = "Smith";
        school = "MSL";
        System.out.println(firstName+" "+lastName+" goes to "+school);
    }
}
```
* Create a new folder called MethodExercise in C:\dev that has a Main.java file.
* Copy the above code into that file and Run to see the output.
* Modify the names and schools to match your group and add new code if needed for additional members.
* Complete the method: 
   * ```printNameAndSchool(String first, String last, String school)``` that returns nothing (```void```)
   * It should print the statement "**fName** **lName** goes to **school**" where fName, lName, and school are the values of the input variables.
* Update your main method to call ```printNameAndSchool()``` instead of printing each statement itself.
   * Hint: In your ```main()``` method you should have only as many lines of code as you have members in your group.
   * Check with a mentor when complete to see if you can simplify your code even more.
   * The program should have the exact same output as when you didn't use a method.

### Exercise #2

* Add two new methods to your code:
   * ```public static int mean(int a, int b)```
   * ```public static double mean(double a, double b)```
   * Each method should compute the average of two numbers.
* From your ```main()``` method call each of your new functions and print the result:
   * Example: ```System.out.println(mean(1,2));``` and ```System.out.println(mean(1.0,2.0);```
* Run your program! Why do you get different results?

### Exercise #3

* Add two new methods to your code:
   * ```public static int min(int a, int b)```
      * This method should compute the minimum of two numbers a, b (**Hint**: Use conditionals!)
   * ```public static int max(int a, int b)```
      * This method should compute the maximum of two numbers a, b (**Hint**: Also use conditionals!)
* From your ```main()``` method call each of your new functions and print the result:
   * Example: ```System.out.println(min(1,5));``` and ```System.out.println(max(1,5);```
* Run your program! Do your results make sense? Try different values to test it more.

### Bonus Exercise

* Create a new file named `Methods.java` and copy the following code into the file:
  
 ```java
 public final class Methods {

  public static double checkIfNumberIsGreater(double x, double y) {
    System.out.println("---------Cool Number Thing----------\n");
    // Fill in your method here
    
    // Think back to if/else statements. Call someone over if you need help.
    
    // Create code to check if x is greater than y, and if true, 
    // add 2 to x (x = x + 2), then print out "x is greater than y"
    
    // Then create code that adds 1 to y if it is greater than x,
    // and then print out "x is NOT greater than y"
    
    double z = 0;
    // Then set z equal to the sum of x and y
    System.out.println("The sum of x and y is: " + z + "\n");
    return z; 
  }

  public static void main(String... args) {
    double a = 9.4;
    double b = 8.7;

    // Replace this line with a call to checkIfNumberIsGreater() and pass a and b as parameters.
    // Then save the result in a double named c.

    a += c;
    b = b + (2.5 * c);

    // Call the method checkIfNumberIsGreater() here and pass a and b as parameters again.
  }
}
```
