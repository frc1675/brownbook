# Creating Objects in Code

### Definitions

* Classes:
  * collection of variables and methods organized to represent an object
  * an object is an abstract "thing" implemented in your program to achieve a specific purpose
  * objects must be created via a call to "new": ```MyClass myObj = new MyClass();```
  * objects can be used to represent objects from the real world. See the "Car" object implementation below:
  
```
public class Car {
 
  // Create a fullThrottle() method
  public void fullThrottle() {
    System.out.println("The car is going as fast as it can!");
  }

  // Create a speed() method and add a parameter
  public void speed(int maxSpeed) {
    System.out.println("Max speed is: " + maxSpeed);
  }

  // Inside main, call the methods on the myCar object
  public static void main(String[] args) {
    Car myCar = new Car();     // Create a myCar object
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.speed(200);          // Call the speed() method
  }
}
```
  
### Exercise #1:

* Pick your favorite animal that you will create an object/class for.
* Don't code anything yet, just open a Notepad to write down your notes.
* List attributes or information that describe your animal (in some cases these might be generic to all animals). 
   * Examples are height, weight, age, health, location, canSwim, canFly etc. Think of as many as you can.
   * For each attribute think of a good variable name and correct variable type to represent it (eg int, double, String, boolean).
* Begin to think of actions this animal can take as they relate to the attributes you have chosen. 
   * Think what how these attributes might change as certain actions occur.
   * For example, what happens to your animal as it gets older?
   * For each action, think of a good method name and correct method return type to represent it (eg int, double, etc)
   
### Exercise #2:

* Now lets code up your group's favorite animal.
* Create a new folder in C:\dev named "ClassExercise"
* Create a new file in that folder named <your-animal-here>.java where <your-animal-here> is the name of your specific animal.
* Use VSCode to File -> Open Folder to open "ClassExercise" and begin to edit your java file.
* Copy the following block of code into the file and replace "Animal" with <your-animal-here>
```
public final class Animal {
    // list your variables here along with their appropriate types
    public int age = 0;
 
    public Animal() {
    }

    // list your methods here along with their appropriate return types
    // and create a template for them without populating them with code yet
    public int growOlder(int years) {
        age = age + years;
        return age;
    }
    
    // For every variable you add to your class add a new line to print
    public void print() {
        System.out.println("Age = "+age);
    }
   

    public static void main(String... args) {
        Animal myAnimal = new Animal();
        myAnimal.print();
        myAnimal.growOlder(10);
        myAnimal.print();
    }
}
```
* Make sure you can "Run" your code to confirm it can build and run before moving to next step.
* Pick five variables (attributes) and five methods (actions) that are related to each other and add them to your class.
* Discuss with a mentor the methods you have chosen to get ideas for how you might implement them.
* As you implement each one, call it from your main method and call myAnimal.print() after each to see how your animal changes with each call.

