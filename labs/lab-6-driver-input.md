## You Turn the Wheel

### Objective

In this lab we will create a robot program that reads driver input and turns a wheel at a speed proportional to a joystick input.

### Hardware

The hardware required for this lab is:

* A Laptop with Driver Station installed and means to connect to RoboRIO
* A joystick or controller
* RoboRIO
* PD Board and Main Breaker
* 1 motor controller
* 1 motor
* 1 wheel
* 1 battery

The setup should be as follows:

* Plug the joystick or controller into a USB port on the Driver Station laptop.
* The PD Board and Main Breaker should be wired to power the RoboRIO and the motor controller with the battery.
* The motor controller should be wired to power the motor and to communicate with the roboRIO (CAN or PWM).
* The wheel should be connected to the output shaft of the motor in some way. The wheel will turn whenever the motor turns.

If you completed [As the Wheel Turns](turn-wheel.md), the only new element is the joystick or controller.

### Software

What we need to do to accomplish the objective:

* Create an IterativeRobot template project or open your [As the Wheel Turns](turn-wheel.md) project.
* Insert code to read the joystick value.
* Insert code to use the joystick value to command the motor controller.
* Test our code.

#### Create an IterativeRobot template project

If you don't have a project, see Lab 3 on how to create one. If you still have your Lab 3 project, you can use that.

#### Write Code to Read the Joystick

The first step is to read the input value from a joystick on the joystick or controller.

What method or methods should our code to do this go in? Think about it or discuss with your group.

What code will you need to add? Here are some tips:

* You will need to create a variable representing the joystick or controller. No matter what the device is, you should be using the class `Joystick`.
  * The first joystick you plug in should be joystick 0.
* You will need to call a method on the `Joystick` object to get the value from the joystick. Check out the javadocs [here](http://first.wpi.edu/FRC/roborio/release/docs/java/) and try to figure out what you need to call.
  * Decide which joystick and axis you will read from. 
  * If you are using an XBox 360 controller, our [`XBoxControllerMap` class](https://github.com/frc1675/frc1675-2016/blob/master/src/org/usfirst/frc/team1675/robot/XBoxControllerMap.java) can help you figure out what axis to use.
    * Don't worry about including that file, just use it to pick the number you need.

**QUESTION TIME!**
* What range of values do you expect to get for the joystick input?
* Assuming you picked the Y axis of one of the sticks, what value would you expect for pushing the joystick fully up?

#### Write Code to Command the Motor Controller

Think back to the post-lab questions in [As the Wheel Turns](turn-wheel.md) (If you haven't done it yet, go read it).

How can you command the motor controller using your joystick input?
  
#### Testing

When you test your code for the first time, always do it "on blocks". No moving part of the robot should be touching the floor or anything else. For this lab you can leave the robot on blocks as we are only turning one wheel.

### Post Lab Questions

* What happens if you only move the joystick slightly? Could this be bad for the robot? Discuss with a mentor.
  * How can we prevent this?
* How would you change your code if I wanted the motor to spin at half speed proportional to the joystick input? The opposite of the joystick input?
