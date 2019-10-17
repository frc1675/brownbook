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
* Don't code anything yet, just open a Notepad to write down the following.
* List attributes or information that describe your animal (in some cases these might be generic to all animals). Examples are height, weight, age, health, location, canSwim, canFly etc. Think of as many as you can.
* For each attribute think of a good variable name and correct variable type to represent it (eg int, double, String, boolean).
* Begin to think of actions this animal can take as they relate to the attributes you have chosen. Think what how these attributes might change as certain actions occur.
   * For example, what happens to your animal as it gets older?
* For each action, think of a good method name and correct method return type to represent it (eg int, double, etc)
