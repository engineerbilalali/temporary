# RISC-V Spike Playground
Bare metal RISC-V assembly task for Spike (no pk) <br>
- Author: Bilal Ali <br>
- Company: 10xEngineers Technologies (Pvt.) Ltd.

## Description

This project demonstrates a simple Fibonacci sequence generator in RISC-V assembly. <br>
The program computes the first 12 numbers of the Fibonacci sequence and stores them in a finite vector V of length N = 12. <br>
The Fibonacci sequence is defined as: <br>
- V(0) = 0 <br>
- V(1) = 1 <br>
- V(i) = V(i-1) + V(i-2), for i ≥ 2 <br>
### Key points: <br>
- The vector length N is defined as a constant using .equ. <br>
- Results are stored in memory (array V). <br>
- The program runs in a bare-metal environment on Spike, without pk. <br>
- Uses only simple loops and arithmetic instructions. <br>

See docs/BilalAli_Task4.pdf for detailed explanation and console output screenshots. <br>
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


