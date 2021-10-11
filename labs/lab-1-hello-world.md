# Lab 1: Hello World

## Relevant Definitions:
* **Program**:
  * A sequence of code statements executed in order starting the main method
* **Statement**:
  * A single executable action of a program, in Java statements are usually one per line and always end in a semicolon ; (!! Very important)
* **Variable**: 
  * a symbol that represents a value of a defined type.
  * Types include:
    * int: used for whole numbers (0,1,2,3,etc)
    * double: used for decimal values (1.5,1.5e-64,etc)
    * boolean: used for true / false situations (true, false)
    * String: represents a sequence of characters, always in quotes (“HelloWorld”)
   * Variables are declared and given values as follows (x is a generic name, you can choose whatever):
```  
   int x = 1675;
   double y = 16.75;
   boolean z = true;
   String a = "frc1675-UPS";
```
* **System Library**:
  * Java provides a library of standard functions available for all developers
  * This is done to speed up development by providing standard and stable solutions to common programming problems
  * One common programming actions is to print to the screen
    * This can be done via the following line: System.out.println(x);
* **Comment**:
  * Special characters used to disable a line of code, in Java use // at the beginning of a line to comment it

## Setup:
* Create a folder called “HelloWorld” folder to C:\dev
* From the desktop open Visual Studio code for 2020 robot development
* Select “File” >> “Open Folder…” and then choose C:\dev\HelloWorld as the folder
* Create a new called file Main.java
* Copy the contents below into the new file
```
class Main {
    public static void main(String[] args) {
        System.out.println("Hello World!"); // Display the string.
    }
}
```
* Press the “Run” button just above with the main method
* Confirm “HelloWorld” is printed in the console output

## Exercise #1:
* Modify the HelloWorld program to have one variable of each type mentioned above
* Print the value of each variable out to the console window
* Reorder your print statements and note the effect, how does it relate to the definition of a program above?
* Comment out two of your print statements and rerun your program, what did you observe?


## Exercise #2:
* Comment out all of your previous code from Exercise #1
* Write a program that will print the following face using various strings (no copy and pasting!!)

```
                   __ooooooooo__
              oOOOOOOOOOOOOOOOOOOOOOo
          oOOOOOOOOOOOOOOOOOOOOOOOOOOOOOo
       oOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOo
     oOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOo
   oOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOo
  oOOOOOOOOOOO*  *OOOOOOOOOOOOOO*  *OOOOOOOOOOOOo
 oOOOOOOOOOOO      OOOOOOOOOOOO      OOOOOOOOOOOOo
 oOOOOOOOOOOOOo  oOOOOOOOOOOOOOOo  oOOOOOOOOOOOOOo
oOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOo
oOOOO     OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO     OOOOo
oOOOOOO OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO OOOOOOo
 *OOOOO  OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO  OOOOO*
 *OOOOOO  *OOOOOOOOOOOOOOOOOOOOOOOOOOOOO*  OOOOOO*
  *OOOOOO  *OOOOOOOOOOOOOOOOOOOOOOOOOOO*  OOOOOO*
   *OOOOOOo  *OOOOOOOOOOOOOOOOOOOOOOO*  oOOOOOO*
     *OOOOOOOo  *OOOOOOOOOOOOOOOOO*  oOOOOOOO*
       *OOOOOOOOo  *OOOOOOOOOOO*  oOOOOOOOO*      
          *OOOOOOOOo           oOOOOOOOO*      
              *OOOOOOOOOOOOOOOOOOOOO*          
                   ""ooooooooo""
```
* Come up with your own ASCII artistic design to print out!
