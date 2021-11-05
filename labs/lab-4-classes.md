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
NEW FILE
```java
  // Inside main, call the methods on the myCar object
  public static void main(String[] args) {
    Car myCar = new Car("CRV", 100000, 0);     // Create a myCar object and call the constructor
    myCar.fullThrottle();      // Call the fullThrottle() method
    myCar.setSpeed(70);        // Call the setSpeed() method
    myCar.getSpeed();          // Call the getSpeed() method
  }
}
```
  
### Exercise #1

* Pick your favorite animal that you will create a class of.
* Don't code anything yet, just open a Notepad to write down your notes.
* List attributes or information that describe your animal. 
   * Examples are height, weight, age, health, location, canSwim, canFly, etc.
   * For each attribute, think of a good variable name and correct variable type to represent it.
* Begin to think of actions this animal can take as they relate to the attributes you have chosen. 
   * Think what how these attributes might change as certain actions occur.
   * For example, what happens to your animal as it gets older?
   * For each action, think of a good method name and correct method return type to represent it (eg int, double, etc)
   
### Exercise #2

* Now lets code up your group's favorite animal.
* Create a new folder in C:\dev named "ClassExercise"
* Create a new file in that folder named <your-animal-here>.java where <your-animal-here> is the name of your specific animal.
* Use VSCode to File -> Open Folder to open "ClassExercise" and begin to edit your java file.
* Copy the following block of code into the file and replace "Animal" with <your-animal-here>
```java
public final class Animal {
    // list your variables here along with their appropriate types
    public int age;
 
    //Constructor
    public Animal(int a) {
       age = a;
    }

    // list your methods here along with their appropriate return types
    // and create a template for them without populating them with code yet
    public int growOlder(int years) {
        age = age + years;
        return age;
    }
    
    // For every variable you add to your class add a new line to print
    public void toString() {
        System.out.println("Age = " + age);
    }
}
```
NEW FILE
```java
 public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal(); //call to constructor
        myAnimal.toString();
        myAnimal.growOlder(10);
        myAnimal.toString();
    }
}
```
* Make sure you can "Run" your code to confirm it can build and run before moving to next step.
* Pick five variables (attributes) and five methods (actions) that are related to each other and add them to your class.
* Discuss with a mentor the methods you have chosen to get ideas for how you might implement them.
* As you implement each one, call it from your main method and call myAnimal.toString() after each to see how your animal changes with each call.

