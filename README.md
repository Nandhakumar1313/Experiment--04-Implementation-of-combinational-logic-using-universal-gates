# Experiment--02-Implementation-of-combinational-logic
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
Hardware-PCs,Cyclone II,USB flasher

Software-Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy


1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B


## Procedure

Create a project with required entities.

Create a module along with respective file name.

Run the respective programs for the given boolean equations.

Run the module and get the respective RTL outputs.

Create university program(VWF) for getting timing diagram.

Give the respective inputs for timing diagram and obtain the results.

## Program:
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

```
Developed by:G.R.Nandhakumar
Reg No:212222100029
```
## F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
```
module f1(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule
```
## F2=xy’z+x’y’z+w’xy+wx’y+wxy
```
module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```
## Output:
## RTL realization:
## For F1
![de1](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/706d09cd-5d77-48a4-880c-7b62b533e007)

## Timing Diagram For F1
![243156755-804e2710-e610-4bd2-b14e-8b208082f604](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/31390ff1-baa7-4758-bcf3-4f10d32f15aa)


## For F2
![kk](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/195be91e-8b01-4239-ba00-0115fe2bb07e)

## Timing Diagram For F2
![243156766-f47bcd88-719f-4785-9f29-681bb9757ca5](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/a9ca8281-5ebc-422e-b6d4-e59f07434f84)



## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
