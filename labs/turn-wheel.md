## As the Wheel Turns

### Objective

In this lab we will create our first robot program and make a wheel turn using a motor controller.

### Hardware

The hardware required for this lab is:

* A Laptop with Driver Station installed and means to connect to RoboRIO
* RoboRIO
* PD Board and Main Breaker
* 1 motor controller
* 1 motor
* 1 wheel
* 1 battery

The setup should be as follows:

* The PD Board and Main Breaker should be wired to power the RoboRIO and the motor controller with the battery.
* The motor controller should be wired to power the motor and to communicate with the roboRIO (CAN or PWM).
* The wheel should be connected to the output shaft of the motor in some way. The wheel will turn whenever the motor turns.

You're in luck! Every past 1675 robot that still has its electronics has all these things. 
Let's go a little more in-depth on some of the aspects of the hardware setup.

#### Driver Station

You will need a computer with Driver Station installed to start the robot. We won't be using any human input in this lab so the program is all you need.

#### RoboRIO

![roboRIO](https://andymark-weblinc.netdna-ssl.com/product_images/ni-roborio/5cd03254fe93c67e8e620dea/zoom.jpg?c=1557148244)

The RoboRIO is the "brain" of the robot. It will run our code, take input signals, and send output signals.
One key output is sending commands to motor controllers, over either PWM or CAN.

#### PD Board and Main Breaker

![PD Board](https://media.screensteps.com/image_assets/assets/000/289/904/original/47968888-bef1-41ab-b81e-35e33bdd749c.png)
![Main Breaker](https://media.screensteps.com/image_assets/assets/000/289/920/original/3A6C33C3-2EB6-4689-837C-F117C800F6F0.png)

The PD (Power Distribution) board connects to the battery (via the Main Breaker) and distributes power to the robot. The Main Breaker black switch is used to turn the robot on, and red button to turn it off. The electrical team will handle this for the most part but using CAN we can get some info about power usage of various channels if we need.

#### Motor Controller

![SparkMax](https://media.screensteps.com/image_assets/assets/002/146/978/original/MAX_HERO__64533.1542227940.png)

This is a motor controller. It takes power in from the PD board (+ and -), outputs power to the motor (+ and -), and has signal wires.
The output wires going to the motor will apply some voltage to the motor depending on how we command it.
In FRC motor controllers work using the CAN (Controller Area Network) Bus, or using PWM (Pulse-Width Modulation) signals.
The two methods use different wiring and different code.
Typically 1675 uses communication over the CAN bus now.

##### CAN Bus

-insert CAN connection picture here-

The CAN Bus is 2 wires that all the CAN Bus devices on the robot chain together and enter the roboRIO at one point.
Each CAN Device has its own "CAN ID" used to refer to it in code.

#### Motor

-insert CIM picture here-

This is a motor. This motor is a CIM, but we use many different kids of motors (determined by the rules and the design team).
Most motors we will use work the same way. The two power wires connect to the outputs of the motor controller.
When the motor controller applies voltage to the motor, the motor will turn proportional to the voltage given.
How fast the motor spins is determined by both the applied voltage and the motor specifications.
Each motor requires its own dedicated motor controller.

#### Wheel

The wheel will turn when the motor turns. How fast it spins depends on how it is conected to the motor. 
The design team determines what the ratio from the motor to the wheel will be.

### Software

To program the robot you will need Eclipse with the FRC development plugins installed and CTRE library for motor controllers. For help, see [Setting up your development environment (robot)](../basics/robot-dev-setup.md).

What we need to do to accomplish the objective:

* Create an IterativeRobot template project
* Understand how IterativeRobot works
* Insert code to make the motor controller turn the wheel
* Test our code

#### Create an IterativeRobot template project

To create the template project

* Select File > New > Other... . 
* In the New window select WPILib Robot Java Development > Robot Java Project.
* Give your project a name.
* In the package field, put `org.usfirst.frc.team1675.robot` . This may already be filled in.
* Select the Iterative Robot radio button.
* Ignore the Simulation World field and click Finish

If successful you will have a new project in Eclipse and in that project will be a Robot.java file with a lot of template code and comments.

#### Understand How IterativeRobot Works

In FRC, if a robot is turned on, it is in one of 3 modes: Disabled, Teleoperated, or Autonomous. In Disabled mode all outputs are disabled. In Autonomous all input from the Driver Station is disabled. In the IterativeRobot framework your code can be called in one of 3 ways: init, periodic, and continuous. Each mode has its own version of a method for these ways. (ex. `autonomousInit`, `disabledPeriodic`, `teleopContinuous`).

* init
  * `autonomousInit`, `teleopInit`, `disabledInit`
  * Runs once when the robot enters the given mode.
    * For example, `autonomousInit` runs once whenever the robot enters autonomous mode.
* periodic
  * `autonomousPeriodic`, `teleopPeriodic`, `disabledPeriodic`
  * Runs every so often when the robot is in the given mode.
    * Typically the period is 20ms as the robot runs at 50Hz. 1s/50Hz = 20ms
    * For example, `disabledPeriodic` runs every 20ms when the robot is in disabled mode.
* continuous
  * `autonomousContinuous`, `teleopContinuous`, `disabledContinuous`
  * Runs as often as possible when other things aren't running in the given mode
    * For example, `teleopContinuous` runs as often as possible when the robot is in teleop mode.
  * We typically do not use continuous methods.
* There is one more important method, `robotInit`, that runs once, ever, whenever the robot code starts.

**QUESTION TIME!** 
* Can you think of some reasons why it is important for our code to be as fast and efficient as possible?
* Can you think of some guidelines on how our code should be written in each of these methods?
  * Are there certain java keywords we should avoid using?
  
On 1675 we typically use Command-Based programming to program our competition robots, but it is important to understand how IterativeRobot works first.

#### Write Code

For this lab, make the wheel spin at 50% speed forward any time the robot is in teleop mode.

What method or methods should our code to do this go in? Think about it or discuss with your group.

What code will you need to add? Here are some tips:

* You will need to create a variable representing the motor controller. For a TalonSRX using CAN the class is `CANTalon`.
  * The channel/ID to declare it with is determined by the wiring. A veteran member or mentor can help you determine this.
* You will need to call a method on the motor controller object to set its speed. Check out the javadocs [here](http://www.ctr-electronics.com/downloads/api/java/html/index.html) and try to figure out what you need to call. You will be in "Percent Voltage Bus" mode.
  * An argument of `0.5` will set the motor to 50% speed forward.
  
#### Testing

When you test your code for the first time, always do it "on blocks". No moving part of the robot should be touching the floor or anything else. For this lab you can leave the robot on blocks as we are only turning one wheel.

### Post Lab Questions

* How could I make the wheel go forward at 100%? Backward at 25%?
* What if I wanted the wheel to turn in autonomous mode?
