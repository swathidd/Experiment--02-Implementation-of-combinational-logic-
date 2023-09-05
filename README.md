## Developed by:D.SWATHI
## RegisterNumber: 212222230154
# Experiment-02 Implementation of combinational logic
## AIM
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime

## Theory
Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
Sum = A’B+AB’ =A ⊕ B Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin
## Procedure
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.
## Program
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

1. HALF ADDER
module adder (a,b,sum,carry);
input a,b;
output sum,carry;
assign sum = (a^b);
assign carry = (a&b);
endmodule

2. FULL ADDER
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum= a^b^cin;
assign carry = (a&b)|((a^b)&cin);
endmodule
``` 

## RTL
![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/f1f61304-aaa1-48d8-889e-24967bed81f4)

![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/b0e1a37d-18d1-4b08-aeda-6a766fb9cadb)


## Output
![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/13e8ad8e-b9ad-41a4-8931-204cb1eaf786)

![image](https://github.com/swathidd/Experiment--02-Implementation-of-combinational-logic-/assets/121300272/6303f7ba-72b6-482c-93e9-79ae9484c5c7)


## Result
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
