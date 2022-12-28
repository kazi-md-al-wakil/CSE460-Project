# CSE460-Project
Project:
Design a 4-bit ALU capable of performing 4 different arithmetic or logical operations using
Quartus, implement it using Verilog HDL, and verify it using a timing diagram.

Specifications:
The ALU takes two four-bit inputs: A, B, and a three-bit operation code (opcode). Based on
the opcode, it performs five different operations on A and B and produces a four-bit output, C.
Depending on the result of a particular operation, the ALU also produces three flags: carry,
zero and sign flag. Fig. 1 illustrates the block diagram of the ALU.

The following table shows the details of the flags followed by an operation.
Flags Description
Zero Flag (ZF) ZF is set to 1 when the output C is 0.
Sign Flag (SF) SF is set to 1 when the MSB of the output C is 1.
Carry Flag (CF) CF is set to 1 when output carry/borrow is 1.

<h3>Example</h3>
<img src="https://github.com/kazi-md-al-wakil/CSE460-Project/blob/master/Example%201.jpg" margin-left= Auto>
<img src="https://github.com/kazi-md-al-wakil/CSE460-Project/blob/master/Example%202.jpg";>
<h3>Opcode operation description</h3>
<img src="https://github.com/kazi-md-al-wakil/CSE460-Project/blob/master/Op%20Code%20Distribuiton.jpg";>
