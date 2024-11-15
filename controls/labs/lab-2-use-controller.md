## You Turn the Wheel

### Objective

In this lab we will create a robot program that reads driver input and moves a robot part at a speed proportional to a joystick input.

### Hardware

The hardware required for this lab is:

* A Laptop with Driver Station installed and means to connect to RoboRIO
* A joystick or controller
* A functional robot with a subsystem you can move

The setup should be as follows:

* Plug the joystick or controller into a USB port on the Driver Station laptop.
* Put a new battery in the robot.
* Confer with mentors or veteran students to determine a system to move. Good examples may be an arm, an elevator, or a tank drive robot's drive.
  * **IMPORTANT!** You must avoid running any motors that are linked mechanically from running against each other.

### Software

What we need to do to accomplish the objective:

* Create an Timeslice Robot template project or open your lab 1 project.
* Insert code to read the joystick value.
* Insert code to use the joystick value to command the motor controller(s).
* Test our code.

#### Create an Timedslice template project

If you don't have a project, see Lab 1 on how to create one. If you still have your Lab 1 project, you can use that.

#### Write Code to Read the Joystick

The first step is to read the input value from a joystick on the joystick or controller.

What method or methods should our code to do this go in? Think about it or discuss with your group.

What code will you need to add? Here are some tips:

* You will need to create a variable representing the joystick or controller. You should be using the class `XboxController`.
  * The first joystick you plug in should be joystick 0.
* You will need to call a method on the `XboxController` object to get the value from the joystick. Check out the javadocs [here](https://first.wpi.edu/FRC/roborio/release/docs/java/edu/wpi/first/wpilibj/Joystick.html) and try to figure out what you need to call.
  * Decide which joystick and axis you will read from.

**QUESTION TIME!**
* What range of values do you expect to get for the joystick input?
* Assuming you picked the Y axis of one of the sticks, what value would you expect for pushing the joystick fully up?

#### Write Code to Command the Motor Controller

How can you command the motor controller using your joystick input? Try scaling it down to 10-20% speed to start when controlling it manually.
  
#### Testing

When you test your code for the first time, always do it "on blocks". No moving part of the robot should be touching the floor or anything else.

### Post Lab Questions

* What happens if you only move the joystick slightly? Could this be bad for the robot? Discuss with a mentor.
  * How can we prevent this?
* How would you change your code if I wanted the motor to spin at half speed proportional to the joystick input? The opposite of the joystick input?
