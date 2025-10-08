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

full adder

![Screenshot 2025-04-22 210616](https://github.com/user-attachments/assets/cb470266-ed7a-41ba-82f9-731c291e687b)

full subtractor

![Screenshot 2025-04-22 210628](https://github.com/user-attachments/assets/dc341a31-2a58-4b56-9cb1-ee62d0a9a300)

**Procedure**

Full Adder: Open Quartus II and create a new project. Use schematic design entry to draw the full adder circuit. The circuit consists of XOR, AND, and OR gates. Compile the design, verify its functionality through simulation. Implement the design on the target device and program it.

Full Subtractor: Follow the same steps as for the full adder. Draw the full subtractor circuit using schematic design. The circuit includes XOR, AND, OR gates to perform subtraction. Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**
```
//expt4a-full adder
module ex4a(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule


//exp-4b-full subtractor
module ex4b(df, bo, a, b, bin);
    output df;
    output bo;
    input a;
    input b;
    input bin;
	wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=(~a&b);
	 assign w3=(~w1&bin);
	 assign df=w1^bin;
	 assign bo=w2|w3;

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Yaazhini.S
RegisterNumber:212224230308
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



