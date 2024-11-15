# Quick Java Basics

We aren't going to teach a full Java course but need to go over a few things about how Java works. If you want to take a full java course ask a mentor and we can point you towards resources!

### Classes and Objects

### Variables

Variables are pieces of data that hold a value. In Java every variable has a specific type. Types are either "primitive" or a class (more on classes below).

Examples of commonly use primitive variables:

* `boolean` - true or false, nothing else.
* `int` - An interger, or whole number.
* `double` - A number with a decimal part, like `3.14159`

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

* Pick your favorite animal that you would create a class of.
* List some attributes or information that describe your animal. 
   * Examples are height, weight, age, health, location, canSwim, canFly, etc.
   * For each attribute, think of a good variable name and correct variable type to represent it.
* Begin to think of actions this animal can take as they relate to the attributes you have chosen. 
   * Think what how these attributes might change as certain actions occur.
   * For example, what happens to your animal as it gets older? (age increases?)
   * For each action, think of an easy to understand method name and correct method return type to represent it (eg int, double, etc)
