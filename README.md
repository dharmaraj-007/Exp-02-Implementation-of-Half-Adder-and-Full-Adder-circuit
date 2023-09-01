# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Components Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
### Theory
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

### Program:
```

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Dharmaraj S
RegisterNumber: 212222240025
```
```
HALFADDER:

module HalfAdder(A,B,sum,carry);
input A,B;
output sum,carry;
assign sum= A^B;
assign carry = A&B;
endmodule
```
```
FULLADDER:

module FullAdder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum= A^B^Cin;
assign carry = (A&B)|((A^B)&Cin);
endmodule
```
### RTL diagram:
## HALFADDER
![halfadder rtl](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/e155a801-584d-4a15-9b91-8f1ecca8ef00)

## FULLADDER
![fulladder rtl](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/90cd7962-ca35-4edf-9beb-1bb734795666)

### Truth table:
## HALFADDER
![halfadder tt](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/c1aa8dce-da04-4922-a2cd-488306bbc1ae)

## FULLADDER
![fulladder tt](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/d0c37dc4-2410-4693-98d7-823b6ff39a3c)

### Output waveform:
## HALFADDER
![halfadder wave](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/325cc8a1-c722-413b-9eb6-062416238f3f)

## FULLADDER
![fulladder wave](https://github.com/dharmaraj-007/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119560386/be9cd3b0-159d-4c87-8c04-2281b36db04b)
 

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
