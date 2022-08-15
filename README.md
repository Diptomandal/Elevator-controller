# Elevator-controller
A VLSI implementation of Elevator control based on Finite state machine using Verilog

Our Basic Logic is based on Mealy state machine. Here, we 

•	At any floor when input button is pressed to reach any desired floor the state will be changed.
•	According to this state the motor moves the elevator car upward or downward. 
•	As car reaches the desired floor, sensor generates an input to change the state. 
•	At this state output “01” for stop will be generated which will stop the car. 
•	According to next instruction (input) the same procedure repeats.

This Ecosystem has been designed for 40 floors. Digital designs can be best described using Finite State Machine (FSM). . It has been used to model the design in which the floors are represented by parameters S00, S01, S02…..S39, S40 representing states as ground floor, first floor, second….. Fortieth floor respectively. Upward /downward motion as well as opening and closing of the lift door is controlled by motors for which the sensors represented by variables Up/Down and Door respectively have been used in the Verilog code. 
The controller contains a Reset button that is used to bring the elevator immediately to last state (current floor) when the reset input is high, also enabling reset opens the door i.e. Door =1 , and stop the motion of lift, i.e. Up = 0 and Down = 0; also Stop = 1;
The basic Logic consists of starting an initial state of lift. I.e. basically keeping lift at ground floor at rest.
Then with positive edge of clock or positive edge of reset (to stop immediately) our lift will work
If reset is pressed, then lift will remain at last state i.e. last floor, opening all the doors and stopping the motion of lift.
If reset is not pressed, then our lift will work for normal conditions, so now user will input any query (request). Now we will have three conditions:
first if our goto floor or requested floor is greater than our current floor(goto>cf) 
second, if our goto floor is less than requested floor (goto<cf)
third, if our goto floor is equal to our requested floor(goto = cf)
Depending upon all three conditions our lift will go up/down or remain stopped wherever it is and update floors as per logic given in code.
Also after updating temp current floor, we update our result in our output result, y.
