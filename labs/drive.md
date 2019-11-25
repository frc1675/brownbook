## Your Robot Driver's License Test

### Objective

In this lab we will create a robot program that reads driver input and drives a robot with "tank drive".

### Hardware

The hardware required for this lab is:

* A Laptop with Driver Station installed and means to connect to RoboRIO
* A joystick or controller (we typically use XBox 360 controllers)
* A functioning old 1675 robot

The setup should be as follows:

* Plug the joystick or controller into a USB port on the Driver Station
* The robot should be functional
* A veteran student or mentor should confirm that they have good code to put back into the robot when done

### Software

What we need to do to accomplish the objective:

* Create an IterativeRobot template project
* Write code to read the Y axis of both sticks on the controller
* Write code to be able to command all motor controllers that control wheel motors
* Determine an algorithm to turn your joystick inputs into commands to the motor controllers
* Write code to express that algorithm

#### Create an IterativeRobot template project

If you don't have a project, see Lab 3 on how to create one.

#### Write Code to Read the Joysticks

The first step is to read the input value from both control sticks' Y-axis.

This should be relatively easy - refer to your Lab 4 project if you need help.

#### Write Code to Command the Motor Controllers

We will now be working with more than 1 motor controller. A veteran student or mentor can help you figure out how many motor controllers and what channels or CAN IDs they have. Take a good look inside the robot with your mentor or veteran while determining this. Try to understand the relationship between the motors, controllers, wheels, and drivetrain.

#### Determine a Control Algorithm

"Algorithm" is just a fancy way to say "a set of steps to take every time". Before we write code to control the rob0ot, we need to determine our control algorithm. A good rule of thumb is that if you can explain it out loud or write it down, you can figure out how to implement it in your program.

Look at the robot and where the wheels are situated. What will happen in they spin foward or backward all at the same time? Half of them? One of them? Try drawing it out on the board or a sheet of paper. 

The algorithm you should aim to implement first is "tank drive". Imagine driving a military tank. Pushing forward on the left stick should make the left wheels go forward, and vice versa. Pushing both sticks forward the same amoutn should have the robot driving forward in a relatively straight line.

Once you can describe your algorithm to take in the two control stick inputs and turn them into motor controller commands, we can move back to coding.

#### Write Code to Express That Algorithm

Try writing the code that expresses your algorithm above. Don't be afraid to take it one step at a time and try different things with the robot. Make sure the robot is ON BLOCKS before testing any code that you don't know the behavior of.

**QUESTION TIME!**
* Did some wheels turn the opposite direction you thought they would? Why might that be?
* How did you fix the above problem? Try looking in the javadocs for the motor controller (see Lab 3). Are there any methods that can help your solution or make it cleaner?
  
#### Testing

When you test your code for the first time, always do it "on blocks". No moving part of the robot should be touching the floor or anything else. For this lab, once you are confident that the robot will be controllable, put it on the ground and drive it around!

#### Reload Code

**IMPORTANT!**
Make sure a veteran student or mentor loads the correct code back into the robot before the end of the night. We don't want people to go to a demo or something with random drive code and nothing else in the robot.

### Post Lab Questions

* Did you implement any code to resolve the post-lab question from Lab 4?
* Try to drive the robot at half-speed or 3/4 speed straight forward. It can be pretty difficult. Can you think of a way to make it easier?
* Can you come up with any other control algorithms using the control sticks? Feel free to be creative.

