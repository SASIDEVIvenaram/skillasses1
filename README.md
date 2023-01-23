# Design a 4 bit binary to BCD converter using verilog

## AIM:
To design a 4 bit binary to BCD converter using verilog programming in quartus.
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime.

## THEORY:
BCD code plays an important role in digital circuits. The BCD stands for Binary Coded Decimal Number. In BCD code, each digit of the decimal number is represented as its equivalent binary number. So, the LSB and MSB of the decimal numbers are represented as its binary numbers.In the 4 bit binary to BCD code converter, the input is 4- bit binary so there is 16 possible combinations. From 10 to 15 decimal numbers, since we cannot represent these numbers by 4 bit BCD code, so we need 8 bit to represent such 2 digit decimal number.But the first 3 bits are zero. Therefore, we can ignore the first 3 bit and we are going to use remaining 5 bits to represent such number in BCD code. 

## PROGRAM:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: SASIDEVI.V
RegisterNumber: 22008940 
```
```
module bcd(input [3:0] bin_in, output reg [3:0] bcd_out);
   always @* begin
     case (bin_in)
       4'b0000: bcd_out = 4'b0000;
       4'b0001: bcd_out = 4'b0001;
       4'b0010: bcd_out = 4'b0010;
       4'b0011: bcd_out = 4'b0011;
       4'b0100: bcd_out = 4'b0100;
       4'b0101: bcd_out = 4'b0101;
       4'b0110: bcd_out = 4'b0110;
       4'b0111: bcd_out = 4'b0111;
       4'b1000: bcd_out = 4'b1000;
       4'b1001: bcd_out = 4'b1001;
       default: bcd_out = 4'bxxxx;
     endcase
   end
endmodule
```
## OUTPUT:

## TRUTHTABLE :
![](/truth.png)
## LOGIC DIAGRAM:
![](/logic.webp)
## TIMING DIAGRAM:
![](/RTL.png)
## RESULT:
Thus,to design a 4 bit binary to BCD converter is implemented successfullly in Quartus using Verilog programming.

