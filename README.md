# Experiment--02-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure

Step 1: Create a project with required entities.
Step 2: Create a module along with respective file name.
Step 3: Run the respective programs for the given boolean equations.
Step 4: Run the module and get the respective RTL outputs.
Step 5: Create university program(VWF) for getting timing diagram.
Step 6: Give the respective inputs for timing diagram and obtain the results.


## Program:
```
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: JAYABHARATHI.S
RegisterNumber: 212222100013 
/*

COMBINATION 1 USING NAND OPERATION

module expf1(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~b & d) | (~a & b & d) | (a & b &~c));
endmodule


COMBINATION 2 USING NOR OPERATION

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((x & y) | (~y & z) | (w & y));
endmodule  


```

## Output:

## COMBINATION 1:

## RTL

![de](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/159559a8-d80f-4860-ab85-e87621be7730)


## Timing Diagram

![de3](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/d269b150-c1cd-4ee9-a659-ec6216c26d81)



## Truth Table

![de5](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/8112c0d7-6726-4740-b606-d437e4d26c96)




## COMBINATION 2:

## RTL realization:

![de2](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/ae111975-bc3b-4825-8918-b0ce4dfb5714)



## Timing Diagram:
![de4](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/9dcb79b0-6eec-4340-a04e-e862c66e12e5)




## Truth Table:
![de6](https://github.com/Jayabharathi3/Experiment--04-Implementation-of-combinational-logic-using-universal-gates/assets/120367796/a12d26ec-edd9-4a5e-9943-a15dfcebf49e)



## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
