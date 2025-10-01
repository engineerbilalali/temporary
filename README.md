# RISC-V Spike Playground
Bare metal RISC-V assembly task for Spike (no pk) <br>
- Author: Bilal Ali <br>
- Company: 10xEngineers Technologies (Pvt.) Ltd.

## Description

This project demonstrates how to check **coprimality** of integer pairs using RISC-V assembly. <br>
The program takes as input a vector `D` of size `3*M`, where each triplet `(xi, yi, ci)` represents: <br>
- `xi` and `yi`: a pair of positive integers <br>
- `ci`: initially `0`, later updated as follows: <br>
  - `ci = 2` if `(xi, yi)` are coprime (gcd = 1) <br>
  - `ci = 1` otherwise <br>

### Example: <br>
Input vector: <br>
`D = (3,5,0, 6,18,0, 15,45,0, 13,10,0, 24,3,0, 24,35,0)` <br>

Output vector after execution: <br>
`D = (3,5,2, 6,18,1, 15,45,1, 13,10,2, 24,3,1, 24,35,2)` <br>

### Key points: <br>
- The number of pairs `M` is defined as a constant using `.equ`. <br>
- A helper function `check_coprime` is implemented, which: <br>
  - Calls the `gcd` function. <br>
  - Updates `ci = 2` if gcd = 1, else `ci = 1`. <br>
- The Euclidean algorithm is used in `gcd` (same as implemented in earlier tasks). <br>
- Functions follow the RISC-V ABI calling convention (`a0-a7` for args/returns, `s` registers saved across calls). <br>
- The program runs in a bare-metal environment on Spike, without pk. <br>

See docs/BilalAli_Assessment1.pdf for detailed explanation and console output screenshots. <br>

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


 
