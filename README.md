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
![de](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/69c68c37-dc65-4252-991d-ea124ba65620)

## For F2
![kk](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/195be91e-8b01-4239-ba00-0115fe2bb07e)

## Timing Diagram For F2
![237874331-0fa16d6e-e4ff-43e2-be8e-bc2d1d6d8b3f](https://github.com/Nandhakumar1313/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120230694/37ab8b95-e837-4b49-982f-4894aba68829)


## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
