# RISC-V Spike Playground
Bare metal RISC-V assembly task for Spike (no pk) <br>
- Author: Bilal Ali <br>
- Company: 10xEngineers Technologies (Pvt.) Ltd.

## Description

This project demonstrates the computation of **absolute sums of triplets** in RISC-V assembly. <br>
The program takes an input vector `A` of length `3*N` and produces another vector `B` of length `N`, where each element of `B` is the absolute value of the sum of three consecutive elements of `A`. <br>

### Example: <br>
- Suppose `N = 4` <br>
- A = [2, -3, 5, 1, 1, 1, -2, -2, -2, 4, 4, -8] <br>
- Then: <br>
  - B[0] = |2 + (-3) + 5| = |4| = 4 <br>
  - B[1] = |1 + 1 + 1| = |3| = 3 <br>
  - B[2] = |-2 + (-2) + (-2)| = |-6| = 6 <br>
  - B[3] = |4 + 4 + (-8)| = |0| = 0 <br>
- Final result: B = [4, 3, 6, 0] <br>
### Key points: <br>
- The vector length `N` is defined using `.equ`. <br>
- The main program calls a helper function `res_triplet`, which computes the absolute value of the sum of three consecutive elements. <br>
- A separate function `abs` is implemented to handle absolute values. <br>
- Register `a0` is used to return values from functions, following the RISC-V calling convention. <br>
- The program runs in a bare-metal environment on Spike (no pk). <br>

See docs/BilalAli_Task6.pdf for detailed explanation and console output screenshots. <br>

## Structure

.<br>
├── Makefile<br>
├── README.md<br>
└── src<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── example.c<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── lib.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── macro.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── main.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── regs.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── riscv.ld<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── startup.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── syscalls.s<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── trap.s<br>


## Usage

To build and and run:

`make run`


