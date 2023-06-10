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
Program :
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming
HALF ADDER:

module expfour(a,b,c,d,f);

input a,b,c,d;

output f;

wire f1,f2,f3;

assign f1 = (~c&~b&~a);

assign f2 = (~d&~c&~a);

assign f3 = (c&~(~b)&~a);

assign f= f1&~f2&~f3;

endmodule


FULL ADDER:

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



Developed by: Pavithra.Y
RegisterNumber:  212222050043
*/
Logic symbol
![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/7634eb53-3d14-4a6c-aa65-9cc9a4292181)

RTL REALIZATION
### Output:
HALF ADDER:
![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/8538b0ba-b941-4c20-a35b-a06f04739efa)

FULL ADDER:
![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/c229cc67-8773-45f2-8849-7c52f3af3f95)

### RTL TIMING DIAGRAM
HALF ADDER:
![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/656d7fac-703e-432e-a1a1-e10bfad11b47)

FULL ADDER:
![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/c4592dd3-54f8-415d-847a-94119c5bc679)

###TRUTH TABLE:

HALF ADDER:

![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/7b49b05e-71fb-43a2-8a26-f1f73784337e)

FULL ADDER:

![image](https://github.com/pavithra2200891/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/128951583/0f37ad7e-e6d8-402a-a7d6-d7383099e429)

### Result:thus the given logic functions are implementing using NAND AND nor gates and their operations are verified using VERILOG programming
