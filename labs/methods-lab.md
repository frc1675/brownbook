# Organize your code! Use methods

### Definitions:

* **Methods**: a named section of a program that performs a specific task.
   * Methods often return output when provided input, the example below computes the addition of two input numbers a and b. 
     ```
     float add(float a, floatb) {
        return a + b;
     }
     ```
   * They have the following general form: "return type" "name"("arguement type" "arguement name")
   * Therefore the above example has a return type of float, a name of add, arguement type of float and arguement name of a and b.
   * Methods can also return ```void``` (which means nothing) and in this case do not require a ```return``` statement.
   * Use methods to organize your code by grouping related code together.
   * Use methods to reduce duplication of code for operations that must be performed many times.
   * You are already familiar with methods through your experience with ```System.out.println()``` and ```Math.abs()```
   
### Exercise #1:

* Below is a Java program designed to print out where each member of your group goes to school:
```
public final class Main {
    private Main() {
    }
    
    void printNameAndSchool(String first, String last, String school){
        // Add your function code here.
    }

    public static void main(String... args) {
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
   * ```void printNameAndSchool(String first, String last, String school)``` that returns nothing (```void```)
   * It should print the statement "**first** **last** goes to **school**" where first, last and school are the values of the input variables.
* Update your main method to call ```printNameAndSchool()``` instead of printing each statement itself.
   * Hint: When complete your ```main()``` method should have only as many lines of code as you have members in your group.
   * Check with a mentor when complete to see if you can simplify your code even more.
   * The program should still generate the same print statements when run.
