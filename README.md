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

1)TRUTH TABLE FOR FULL ADDER

<img width="342" height="220" alt="image" src="https://github.com/user-attachments/assets/94d06711-afb8-4270-8d33-793de4d6e870" />

2)TRUTH TABLE FOR SUBTRACTOR

<img width="755" height="405" alt="image" src="https://github.com/user-attachments/assets/fbb1b727-071e-49ab-be75-d073320bd2b0" />





**Procedure**

1)Type the program in Quartus software.

2)Compile and run the program.

3)Generate the RTL schematic and save the logic diagram.

4)Create nodes for inputs and outputs to generate the timing diagram.

5)For different input combinations generate the timing diagram.


**Program:**

PROGRAM FOR FULLADDER:

```
module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```

PROGRAM FOR FULLSUBTRACTOR:

```
module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
endmodule
```

Developed by:DHAMODHARAN S RegisterNumber:25009463

**RTL Schematic**

1)FULLADDER

<img width="1159" height="589" alt="image" src="https://github.com/user-attachments/assets/dedd7cae-f126-455c-a0b5-40e7dcd52382" />

2)FULL SUBTRACTOR

<img width="1162" height="588" alt="image" src="https://github.com/user-attachments/assets/4e93a8ce-54ba-4657-b4eb-d707a9292b2b" />






**Output Timing Waveform**

1)FULLADDER

<img width="1167" height="597" alt="image" src="https://github.com/user-attachments/assets/48868fa0-8bb4-4cae-8246-c975e6a9474f" />

2)FULL SUBTRACTOR

<img width="1152" height="592" alt="image" src="https://github.com/user-attachments/assets/c1dea09f-7926-4696-b62d-8ae3ff887b34" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



