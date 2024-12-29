# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER

![Screenshot 2024-12-03 082725](https://github.com/user-attachments/assets/2e1c0097-4033-419b-b4b8-c6e592c201c4)

FULL SUBTRACTOR

![Screenshot 2024-12-03 082801](https://github.com/user-attachments/assets/31f7d926-59ff-4f88-b0f0-18346278d037)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
FULL ADDER
module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule
```
```
FULL SUSTRACTOR
module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule
```

Developed by:Divya Sri 
RegisterNumber:24901155
*/

**RTL Schematic**
FULL ADDER

![exp4](https://github.com/user-attachments/assets/9b078ba0-cc8a-4f2a-bdc4-0d5386b321c7)

FULL SUBTRACTOR

![exp4a](https://github.com/user-attachments/assets/15a7a8bb-1b71-4f1b-9ab5-29671739dc8b)


**Output Timing Waveform**
FULL ADDER

![exp4 (2)](https://github.com/user-attachments/assets/aac7da72-5d65-481d-9060-4120efd4dd72)

FULL SUBTRACTOR

![exp4a (2)](https://github.com/user-attachments/assets/69ed8424-495f-4f8d-9b7b-769e630221f1)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



