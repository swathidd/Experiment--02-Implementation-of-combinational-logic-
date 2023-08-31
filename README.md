## Developed by:D.SWATHI
## RegisterNumber: 212222230154
# Experiment-02 Implementation of combinational logic
Implementation of combinational logic gates
 ## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required
Hardware – PCs, Cyclone II , USB flasher
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. ###Using NAND gates NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
## Logic Diagram
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'
## Procedure
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations. 
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.
## Program
```
module ex02(A,B,C,D,F1);
 input A,B,C,D; output F1;
 wire x1,x2,x3,x4,x5;
 assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
 assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1=x1|x2|x3|x4|x5;
endmodule
``` 

## Output
## RTL
![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/57f4d145-ab6a-4c06-8c4d-07391f5ac0a5)

## Timing Diagram
![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/48e3a2a1-49f0-4365-b36a-b929b0ba5455)

## Result
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
