# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
module expfour(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3;
assign f1 = (~c&~b&~a);
assign f2 = (~d&~c&~a);
assign f3 = (c&~(~b)&~a);
assign f= f1&~f2&~f3;
endmodule
PROGRAM 2:
module expfourtwo(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3,f4;
assign f1 = c&(~b)&a;
assign f2 = d&(~c)&a;
assign f3 = c&(~b)&a;
assign f4 = ~(f1|f2|f3);
not(f,f4);
endmodule
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Pavithra.Y
RegisterNumber:  212222050043
*/
Logic symbol & Truthtable
PROGRAM 1
![TRUTH TABLE PROGRAM 1](https://user-images.githubusercontent.com/128951583/233091090-b712f9b1-43e8-4e99-9959-e2fd5002affa.jpg)
PROGRAM 2
![TRUTH TABLE PROGRAM 2](https://user-images.githubusercontent.com/128951583/233091234-9c1dd2c0-c4af-45ea-b9b6-61d5392dd633.jpg)



RTL REALIZATION
### Output:
PROGRAM 1
![RTL PROGRAM 1](https://user-images.githubusercontent.com/128951583/233091447-a456d043-f8a7-4647-9097-640dbc52e4ad.jpg)
PROGRAM 2
![RTL PROGRAM 2](https://user-images.githubusercontent.com/128951583/233091565-5b7ee09a-04fc-4105-a152-55cc44b2479c.jpg)


### RTL
### TIMING DIAGRAM
PROGRAM 1
![TIMING DIAGRAM PROGRAM 1](https://user-images.githubusercontent.com/128951583/233091752-15ead1b4-232b-48cd-92e1-f341b550a3ec.jpg)
PROGRAM 2
![TIMING DIAGRAM PROGRAM 2](https://user-images.githubusercontent.com/128951583/233091835-6c082524-f616-4507-a3d6-cd55867370be.jpg)



### Result:thus the given logic functions are implementing using NAND AND nor gates and their operations are verified using VERILOG programming
