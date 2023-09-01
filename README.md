# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

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
### Program:
```
Developed by: VIKASH S
RegisterNumber: 212222240115
```
HALF ADDER
```
module exp3(A,B,C,S);
input A,B;
output S,C;
assign S=A^B;
assign C=A&B;
endmodule
```
FULL ADDER
 ```
module exp3_2(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=a^b^c;
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
### TRUTH TABLE:

HALF ADDER
![Screenshot 2023-09-01 092526](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/bf1dd111-4d1d-4e29-84c8-d44804301ad6)
FULL ADDER

![Screenshot 2023-09-01 092658](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/9f614dd9-ca40-4d03-b340-5dc9959450da)
### RTL:
HALF ADDER
![rtl 3](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/d1222031-0344-4448-adbf-e2f3dbcec0ab)

FULL ADDER

![rtl 2](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/9feb1267-36c1-4a9c-9fc8-eeaac21c47fb)



### Output:
HALF ADDER


![Screenshot 2023-09-01 093210](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/20415589-5c70-4769-b664-3b774cb249a0)

FULL ADDER
![exp3_2](https://github.com/vikashsenthil21/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/119433834/ac1bf998-e34c-461a-be2c-fb73f7549e1e)



### Result:
Thus the half adder and full adder circuits are designed and the truth tables is verified using quartus software.
