# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
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
```c

module expf1(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~b & d) | (~a & b & d) | (a & b &~c));
endmodule
```

COMBINATION 2 USING NOR OPERATION
 ```c
module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((x & y) | (~y & z) | (w & y));
endmodule  

*/
```

## Output:

## COMBINATION 1:

## RTL

![image](https://user-images.githubusercontent.com/120367796/232848801-86390348-2137-4160-ad35-32cbe67e217b.png)


## Timing Diagram

![image](https://user-images.githubusercontent.com/120367796/232850850-495f5c2b-3c41-4465-aea8-b8fbcb11a359.png)


## Truth Table

![image](https://user-images.githubusercontent.com/120367796/232851058-4fa42e69-9788-4279-a4d6-777d3ebfcbec.png)



## COMBINATION 2:

## RTL realization:

![image](https://user-images.githubusercontent.com/120367796/232849906-b82da722-4159-45b7-b6df-3f97bbf42099.png)

## Timing Diagram:

![image](https://user-images.githubusercontent.com/120367796/232851281-0b64ed5e-b3f9-486c-aebb-5e389f81124c.png)


## Truth Table:

![image](https://user-images.githubusercontent.com/120367796/232851457-a0d4ef6d-bef6-4fcd-9833-458c789d5053.png)


## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
