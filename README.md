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

<img width="498" height="482" alt="full adder" src="https://github.com/user-attachments/assets/9fede916-d486-4abd-8745-7ca6071fbc8a" />
<img width="559" height="537" alt="full sub" src="https://github.com/user-attachments/assets/630c937f-3612-47d3-ad64-fb29ea257918" />


**Procedure**
~~~
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.
~~~

**Program:**
~~~
module fua(a,b,c,sum,cary);
input a,b,c;
output sum,cary;

assign sum  = a ^ b ^ c;
assign cary = (a & b) | (b & c) | (c & a);

endmodule

module fus(a,b,c,diff,bor);
input a,b,c;
output sum,cary;

assign sum  = a ^ b ^ c;
assign cary = (~a & b) | (b & c) | (~a & c);

endmodule
~~~

**RTL Schematic**
<img width="2556" height="1302" alt="fua 1" src="https://github.com/user-attachments/assets/602af564-8f2d-4926-b6c6-dab4a1817683" />
<img width="2560" height="1389" alt="fus 1" src="https://github.com/user-attachments/assets/2589a3b3-60d3-4570-9e79-7caf30bb2146" />

**Output Timing Waveform**
<img width="2553" height="1309" alt="fua 2" src="https://github.com/user-attachments/assets/16b43d29-56b4-457a-83ac-46683191a8a1" />
<img width="2536" height="1361" alt="fus 2" src="https://github.com/user-attachments/assets/c0717373-5a1e-4b30-8e87-6111f7261756" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



