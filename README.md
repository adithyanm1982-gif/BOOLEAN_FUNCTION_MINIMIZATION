# BOOLEAN_FUNCTION_MINIMIZATION

## AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Equipment Required:

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

## Procedure

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


## Program:

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: ADITHYA NM

RegisterNumber: 212225040011
```
module Exp2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash;
wire f11,f12,f13,f21,f22,f23;
not (adash,a);
not (bdash,b);
not (cdash,c);
not (ddash,d);
not (ydash,y);
//f1 value
and (f11,bdash,ddash);
and (f12,adash,b,d);
and (f13,a,b,cdash);
or (f1,f11,f12,f13);
//f2 value
and (f21,ydash,z);
and (f22,x,y);
and (f23,w,y);
or (f2,f21,f22,f23);
endmodule
```


## RTL realization
<img width="1920" height="1080" alt="de1" src="https://github.com/user-attachments/assets/67a888c7-2d37-46b2-8ab6-fcd92cc66db9" />

## Output:

## RTL
<img width="1920" height="1080" alt="de2" src="https://github.com/user-attachments/assets/4cd88a6d-db5a-43bd-9eff-c359a4dd3d47" />

## Timing Diagram
<img width="1920" height="1080" alt="de3" src="https://github.com/user-attachments/assets/1b78bb43-a59c-4ef4-96c7-d8f7d8a22d5b" />

## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

