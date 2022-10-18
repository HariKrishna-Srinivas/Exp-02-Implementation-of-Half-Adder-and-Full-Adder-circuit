# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
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
### 
Program:
~~~
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:M.Harikrishna.
RegisterNumber: 212221230059

Half Adder:

module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

Full Adder:

module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule

Output:
Half Adder:
RTL:
![image](https://user-images.githubusercontent.com/94882905/196326419-6b3e3c36-c65c-47cd-9530-beee5ee86d7c.png)

TIMING DIAGRAM:

![image](https://user-images.githubusercontent.com/94882905/196326516-cf79befb-5d32-442d-a32f-260258df1dee.png)

TRUTH TABLE:

![image](https://user-images.githubusercontent.com/94882905/196326570-d803ad57-7cbb-4c61-bd13-9d4c19c5dded.png)

Full Adder:

RTL:

![image](https://user-images.githubusercontent.com/94882905/196326790-3d4a1719-d01f-4eaa-ab91-0eed161a4da5.png)

TIMING DIAGRAM:

![image](https://user-images.githubusercontent.com/94882905/196326866-39417eda-5c45-4dbc-ab1d-1773be9b6baf.png)

TRUTH TABLE:

![image](https://user-images.githubusercontent.com/94882905/196326952-3ef0af12-820f-4f32-b666-b6917b6d64c0.png)

Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.

