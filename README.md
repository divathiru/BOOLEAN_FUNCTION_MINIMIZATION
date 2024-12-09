# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

Implementing Boolean functions in Verilog HDL (Hardware Description Language) involves
translating the simplified Boolean expressions into Verilog code to describe the behavior of digital
circuits. The basic building blocks in Verilog is module. The module represent a combinational
circuit. Use logical operators (&, |, ~, ^) to implement Boolean functions directly. Use built-in gate
primitives for basic functions. Use University program VWF to verify the functionality of your Verilog
modules. Create waveform and check outputs against expected results

**Logic Diagram**



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: RegisterNumber:K.Thirumurugan :24005998

module boolean_function_minimization(a, b, c, d, w, x, y, z, f1, f2);
input a, b, c, d, w, x, y, z;
output f1, f2;
wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
assign x1 = (~a) & (~b) & (~c) & (~d);
assign x2 = (a) & (~c) & (~d);
assign x3 = (~b) & (c) & (~d);
assign x4 = (~a) & (b) & (c) & (d);
assign x5 = (b) & (~c) & (d);
assign f1 = x1 | x2 | x3 | x4 | x5;
assign x6 = (x) & (~y) & (z);
assign x7 = (~x) & (~y) & (z);
assign x8 = (~w) & (x) & (y);
assign x9 = (w) & (~x) & (y);
assign x10 = (w) & (x) & (y);
assign f2 = x6 | x7 | x8 | x9 | x10;
endmodule


**Output:**


**RTL** REALIZATION:
![Screenshot 2024-12-05 173834](https://github.com/user-attachments/assets/a06e579e-e661-49c8-a158-302b74c6b295)
truth table
F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D:
'''
![Screenshot 2024-12-05 173916](https://github.com/user-attachments/assets/a587f6e0-712e-4640-aba3-5601138dd056)
'''
F2=xy’z+x’y’z+w’xy+wx’y+wxy
'''
![Screenshot 2024-12-05 173934](https://github.com/user-attachments/assets/37caf1e5-10e7-4fff-8352-957eaedb9198)
'''


**Timing Diagram**

![Screenshot 2024-12-05 173950](https://github.com/user-attachments/assets/1603ae7f-68e2-4d96-9f64-d388c46184b8)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

