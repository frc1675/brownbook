## Lab 3: As the Wheel Turns

### Objective

In this lab we will create our first robot program and make a wheel turn using a motor controller.

### Hardware

The hardware required for this lab is:

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

#### RoboRIO

-insert roboRIO picture here-

The RoboRIO is the "brain" of the robot. It will run our code, take input signals, and send output signals.
One key output is sending commands to motor controllers, over either PWM or CAN.

#### PD Board and Main Breaker

-insert PD Board picture here-

The PD (Power Distribution) board connects to the battery and distributes power to the robot. 
The electrical team will handle this for the most part but using CAN we can get some info about power usage of various channels if we need.

#### Motor Controller

-insert Talon SRX picture here-

This is a motor controller. It takes power in from the PD board (+ and -), outputs power to the motor (+ and -), and has signal wires.
The output wires going to the motor will apply some voltage to the motor depending on how we command it.
In FRC motor controllers work using the CAN (Controller Area Network) Bus, or using PWM (Pulse-Width Modulation) signals.
The two methods use different wiring and different code.
Typically 1675 uses Talon SRXs over the CAN bus now.

##### CAN Bus

-insert CAN connection picture here-

The CAN Bus is 2 wires that all the CAN Bus devices on the robot chain together and enter the roboRIO at one point.
Each CAN Device has its own "CAN ID" used to refer to it in code.

##### PWM

-insert PWM connection pricture here-

Sometimes we will connect a motor controller to the RoboRIO using a PWM cable. These cables are made of 3 wires. 
Red is power (+), Black is ground (-) and White is signal. 
Each motor controller requires a direct connection to the roboRIO.
One end connects to the motor controller and the other goes to one of the PWM channels on the RoboRIO. 
Make sure to double check the orientation of the wire when plugging in.

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


