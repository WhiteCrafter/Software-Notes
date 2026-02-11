#software/designpatterns/patern 
[[Chap3.3DesignPatternTurorial.pdf#page=184 ]]
# Intent 
Regulate a physical (continuous) process.
- [[#Open-Loop System]]
- Closed-Loop System
	- Feedback Control System
	- Feedback-Loop System

# Terminology
**Process Variables**: Properties of the process that can be measured; several specific kinds are often distinguished. 
**Controlled variable**: Process variable whose value the system is intended to control
**Input variables**: Process variable that measures an input to the process 
**Manipulated variable**: Process variable whose value can be changed by the controller 
**Set point**: The desired value for a controlled variable

# Open-Loop System
System in which information about process variables is not used to adjust the system.

![[Pasted image 20260209010508.png]]
## Example Heating:
- Constant burner
- use a timer to turn burner off and on at fixed intervals
# Closed - Loop System
System in which information about process variables is used to manipulate a process variable to compensate for variations in process variables and operating conditions
## Feedback Control System

The controlled variable is measured, and the result is used to manipulate one or more of the process variables.

![[Pasted image 20260209010704.png]]

### Example Heating:

use a thermostat, burner is turned off and on as necessary to maintain the desired temperature (the set point)

## Feedforward Control System
Some of the process variables are measured, and anticipated disturbances are compensated for without waiting for changes in the controlled variable to be visible.

![[Pasted image 20260209010826.png]]
### Example Heating:
measure the outside temperature (i.e., before the heating process), select a timer interval dependent on this temperature