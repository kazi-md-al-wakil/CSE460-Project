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

opcode operation description
000 RESET The ALU will be at the idle state (no operation state) and the
output C will retain the result of the last operation performed.


001 XNOR The ALU will perform bitwise XNOR operation on A, B. The
bitwise operation will be performed serially at the positive edge of
input clock i.e. during the first clock cycle, the operation will be
performed on the LSBs (A0, B0) storing the result in C0 and in the
next clock cycle the operation will be performed on A1, B1 updating C1 and finally, 
on A3 and B3 saving it to C3 as long as the opcode is active.

010 SUB
The ALU will SUBTRACT B from A.. The operation will be
performed serially at the positive edge of input clock i.e. during
the first clock cycle, the operation will be performed on the LSBs
(A0, B0) storing the result in C0 and in the next clock cycle the
operation will be performed on A1, B1 updating C1 and finally, on
A3 and B3 saving it to C3 as long as the opcode is active. During
SUB operation, the MSBs of both A and B should be treated as
sign bits i.e. A3 will be the sign bit for A and correspondingly B3
will be the sign bit for B. So, the subtraction will occur between
two signed binary numbers where the MSBs are the sign bits and
the remaining bits are the values of the operands.


011 NAND
The ALU will perform bitwise NAND operation on A, B. The
bitwise operation will be performed serially at the positive edge of
input clock i.e. during the first clock cycle, the operation will be
performed on the LSBs (A0, B0 ) storing the result in C0 and in the next clock cycle the operation will be performed on A1, B1
updating C1 and finally, on A3 and B3 saving it to C3 as long as the opcode is active.


100 ADD
The ALU will perform ADD operation on A, B. The operation will
be performed serially at the positive edge of input clock i.e. during
the first clock cycle, the operation will be performed on the LSBs
(A0, B0) storing the result in C0 and in the next clock cycle theoperation will be performed on A1, B1 updating C1 and finally, on
A3 and B3 saving it to C3 as long as the opcode is active.
