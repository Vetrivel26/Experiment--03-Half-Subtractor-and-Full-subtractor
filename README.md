# Experiment--03-Half-Subtractor-and-Full-subtractor

## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
~~~
1.Use module projname(input,output) to start the Verilog programmming.
2.Assign inputs and outputs using the word input and output respectively.
3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4.Use each output to represnt onre for differnce and the other for borrow.
5.End the verilog program using keyword endmodule.
~~~

## Program:
~~~
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: vetrivel s
RegisterNumber:  212221240060

Half Subtractor :

module ex03(A,B,Diff,Borrow);
input A,B;
output Diff,Borrow;
wire X;
xor(Diff,A,B);
not(X,A);
and(Borrow,X,B);
endmodule

Full Subtractor:

module ex03(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
assign Diff = A^B^C;
assign Borrow = ~A & (B^C) | B & C;
endmodule
*/
~~~
## Output:
HALF SUBTRACTOR

## Truthtable
![T1](https://user-images.githubusercontent.com/95363138/167686175-7321f4fc-3db1-4fbb-9ff1-9348b7cb738d.png)
##  RTL realization
![d3](https://user-images.githubusercontent.com/95363138/167686265-cf2711bf-18f1-4ac7-b57a-5f5c0f45317b.png)
## Timing diagram 
![d 3 1](https://user-images.githubusercontent.com/95363138/167686286-1d85a121-0b9f-476c-b1bb-6ea0ca293508.png)
## Truthtable
![T2](https://user-images.githubusercontent.com/95363138/167686450-c791d60c-8384-416b-8b43-27260d58b811.png)
## RTL realization
![d2](https://user-images.githubusercontent.com/95363138/167686508-72149dcb-2f53-4e8e-bcad-ee13f0aa04ac.png)
## Timing diagram
![d3 2](https://user-images.githubusercontent.com/95363138/167686652-b03c70a8-d64f-4260-839d-926a914a73d3.png)
## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
