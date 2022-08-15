# Elevator-controller
A VLSI implementation of Elevator control based on Finite state machine using Verilog

Our Basic Logic is based on Mealy state machine. Here, we 

•	At any floor when input button is pressed to reach any desired floor the state will be changed.
•	According to this state the motor moves the elevator car upward or downward. 
•	As car reaches the desired floor, sensor generates an input to change the state. 
•	At this state output “01” for stop will be generated which will stop the car. 
•	According to next instruction (input) the same procedure repeats.
