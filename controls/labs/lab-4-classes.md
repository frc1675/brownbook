# Creating Objects in Code

### Definitions

* **Object**
  * You can think of an object as a variable that is a collection of other variables.
  * In a computer science class, the definition you would get is that objects are made of states and behaviors.
  * The variables are the objects state and its methods are behaviors.
  * Another way to think about it is that an object is an abstract "thing" implemented in your program to achieve a specific purpose.
  * Objects must be created with the new keyword, as in ```MyClass myObj = new MyClass();```.
  * Objects can be used to represent objects in the real world.

* **Class**
  * A blueprint for an object.
  * Each class has its own file. You've already used used classes in the three previous labs, Main.java.
  * You know if a file is a class if it starts with ```public class [name] {```.

* **Constructor**
  * Most classes have one special method, the constructor. This method is called whenever a new object of that type is created.
  * The constructor is special because it has no return type and must have the same name as the class. It looks like ```public [name]([arguments]) {```.
  * The following is an example of a class with a constructor:

NEW FILE Car.java
```java
public class Car {
  String model;
  int miles;
  int speed
  
  //Constructor
  public Car(String mo, int mi, int s) {
    model = mo;
    miles = mi;
    speed = s;
  }
 
  // fullThrottle() method
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  // setSpeed() method 
  public void setSpeed(int s) {
    speed = s;
  }
  
  // getSpeed() method
  public void getSpeed() {
    System.out.println("The car is going " + speed + " miles per hour.");
  }
```
NEW FILE Main.java
```java
public class Main {
  // Inside main, call the methods on the myCar object
  public static void main(String[] args) {
    Car myCar = new Car("CRV", 100000, 0);     // Create a myCar object and call the constructor
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.setSpeed(70);        // Call the setSpeed() method
    myCar.getSpeed();          // Call the getSpeed() method
  }
}
```
  
### Brainstorming #1

* Pick your favorite animal that you will create a class of.
* Don't code anything yet, just jot down some potential ideas.
* List some attributes or information that describe your animal. 
   * Examples are height, weight, age, health, location, canSwim, canFly, etc.
   * For each attribute, think of a good variable name and correct variable type to represent it.
* Begin to think of actions this animal can take as they relate to the attributes you have chosen. 
   * Think what how these attributes might change as certain actions occur.
   * For example, what happens to your animal as it gets older? (age increases?)
   * For each action, think of an easy to understand method name and correct method return type to represent it (eg int, double, etc)
   
### Exercise #1

* Now lets code up your animal!
* Create a new folder in C:\dev named "ClassExercise"
* Create a new file in that folder named `Animal.java` but replace `Animal` with the name of your specific animal.
* At the top of VSCode, select File -> Open Folder to open "ClassExercise" and begin to edit your java file.
* Copy the following block of code into the file but replace "Animal" with the name of your chosen animal similar to below:

 NEW FILE Axolotl.java
 ```java
public class Axolotl {
    // list the variables you chose while brainstorming along with their appropriate types
    int age;
    // int somethingCool;
    // double anotherExampleVariable;
    // boolean underwater;
 
    // constructor method (called automatically when an Axolotl is created)
    public Axolotl(int a) {
       // set the Axolotl's age to the value of parameter "a"
       age = a;
    }

    // write your methods here along with their appropriate return types
    public void growOlder(int years) {
        age = age + years;
    }
    
    // For every variable you add to your class, add a method to print out that value
    public void printAge() {
        System.out.println("Age = " + age);
    }
}
```
Within "ClassExercise", create a new file named `Main.java` and populate it with the following code:

Be sure to change this code to interact with your animal class too!
```java
public class Main {
    public static void main(String[] args) {
        Axolotl ancientJerry = new Axolotl(10000); // Instantiates a new Axolotl within the variable "ancientJerry" and sets its initial age to 10000

        // test out some of the methods you created for your animal:
        ancientJerry.printAge(); // displays the age of ancientJerry
        ancientJerry.growOlder(100); // call to one of the Axolotl class methods to increase age
        ancientJerry.printAge(); // displays the new age of ancientJerry

        // feel free to create more objects using the class:
        Axolotl jerryJunior = new Axolotl(5);  
        jerryJunior.growOlder(100); // jerryJunior is growing up!!
        jerryJunior.printAge();

        ancientJerry.growOlder(-10100);  
        ancientJerry.printAge();
        System.out.println("Ancient Jerry has finally died :[");
    }
}
```
* Make sure you can "Run" your code to confirm it can build and run before moving to next step.
* Pick five variables (attributes) and five methods (actions) that are related to each other and add them to your class.
* Discuss with a mentor the methods you have chosen to get ideas for how you might implement them.
* As you implement each one, call it from your main method and call `ancientJerry.printAge()` to see how your animal changes with each call.
