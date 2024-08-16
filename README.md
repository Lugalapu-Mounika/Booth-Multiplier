# Booth-Multiplier
The BOOTH_FINAL module implements Booth's multiplication algorithm. It performs signed multiplication of two 8-bit numbers (M and Q) and produces a 16-bit signed result (Z). The module is implemented in Verilog and uses behavioral programming to simulate the Booth's algorithm.
**Module Description**
Inputs:

M: 8-bit signed multiplicand
Q: 8-bit signed multiplier
Output:

Z: 16-bit signed result of the multiplication
Registers:

temp: 2-bit temporary variable for storing intermediate results
Q1: 1-bit register to store the value of bit less than the LSB bit of Q
M1: 8-bit register to store the 2’s complement of M
**Behavioral Programming**
Initialize Z to 16-bit decimal 0.
Initialize Q1 to 1-bit decimal 0.
Compute the 2’s complement of M and store it in M1.
Loop through 8 iterations:
Concatenate Q[i] and Q1 to the temp variable.
Update Z based on the value of temp:
If temp is 10, add the 2’s complement of M to Z.
If temp is 01, add M to Z.
If neither condition is met, perform an arithmetic right shift on Z.
Update Q1 to the value of Q[i].
**Software Requirements & Tools**
Xilinx ISE 14.7
Description: Xilinx ISE (Integrated Synthesis Environment) is a discontinued software tool for synthesis and analysis of HDL designs. It is used for development of embedded firmware for Xilinx FPGA and CPLD integrated circuits.
**Getting Started**
Open Xilinx ISE 14.7.
Create a new project and add the BOOTH_FINAL Verilog module.
Compile the design and perform simulation to verify correctness.
