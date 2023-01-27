DEVELOPED BY: J.B.VINIYA
REGISTER NUMBER: 22008831



AIM:To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.


Equipments Required:Hardware – PCs, Cyclone II , USB flasher   Software – Quartus prime


Theory:Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.


Half Subtractor Full Subtractor

Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

![santhosh1](https://user-images.githubusercontent.com/121683551/213453722-f363fbe7-3471-4bbc-86a1-1e22d57dc3a8.png)

Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y


Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 

![santhosh2](https://user-images.githubusercontent.com/121683551/213453856-ca03507c-c06e-4914-a55d-52a3c2f9bd21.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

Procedure
Write the detailed procedure here

Program:
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. HALF SUBTRACTOR:

module HalfSub(a,b,difference,borrow);

input a,b;

output difference,borrow;

assign difference=(a^b);

assign borrow=(~a&b);

endmodule

FULL SUBTRACTOR:

module FullSub(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign borrow=(~a&(b^c)|(b&c));

assign difference=(a^b^c);

endmodule

LOGIC GATES:

![33](https://user-images.githubusercontent.com/121683551/213455104-ce62b8d0-4cb7-43b7-b9a7-7a19aef5ae53.png)

Output:
Truthtable:

HALF SUBTRACTOR

![SANTHOSH4](https://user-images.githubusercontent.com/121683551/213455253-89089712-34bd-4d4b-8bf2-7c52b5ba608d.png)

FULL SUBTRACTOR

![SANTHOSH5](https://user-images.githubusercontent.com/121683551/213455376-7cd4eb6e-3bb5-44de-a8ac-50c43dd1405c.png)


RTL realization
HALF SUBTRACTOR

![SANTHOSH6](https://user-images.githubusercontent.com/121683551/213455480-da83d429-2d09-4ba7-8ffd-e85d0bbab809.png)


FULL SUBRRAVTOR

![SANTHOSH7](https://user-images.githubusercontent.com/121683551/213455608-86fae1e4-364e-476b-9e44-913f498a0cd2.png)


Timing diagram
HALF SUBTRACTOR

![SANTHOSH8](https://user-images.githubusercontent.com/121683551/213455710-bbed6c56-5abe-439c-a648-b959515aff2c.png)


FULL SUBTRASCTOR

![SANTHOSH9](https://user-images.githubusercontent.com/121683551/213455774-f79d5073-8bbd-4893-9c87-d7f4e1e40c5b.png)


RESULTS
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
