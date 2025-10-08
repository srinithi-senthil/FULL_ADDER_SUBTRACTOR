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
<img width="1161" height="659" alt="image" src="https://github.com/user-attachments/assets/1d4a5dbe-3d08-44d4-9f0f-0a77ed1ec742" />
<img width="1124" height="646" alt="image" src="https://github.com/user-attachments/assets/7ad43ec8-1036-49bc-ae4e-b705fc04c70d" />

**Procedure**


```
Write the detailed procedure here

**Program:**
```module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

```
```
module fullsubtractor(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
full adder

![Screenshot 2025-04-22 210003](https://github.com/user-attachments/assets/746f29ad-ebf7-4979-8727-e7048774e797)

full subtractor

![Screenshot 2025-04-22 210017](https://github.com/user-attachments/assets/6b650132-5622-4515-9da4-e5530d54a03d)

**Output Timing Waveform**

full adder

![Screenshot 2025-04-22 210043](https://github.com/user-attachments/assets/07260fd2-dc60-47a5-8ea4-66a5ef2513de)

full subtractor

![Screenshot 2025-04-22 210103](https://github.com/user-attachments/assets/ad9beebc-c915-4ff9-aeaf-78a234b67815)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



