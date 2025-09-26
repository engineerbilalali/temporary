# RISC-V Spike Playground
Bare metal RISC-V assembly task for Spike (no pk) <br>
- Author: Bilal Ali <br>
- Company: 10xEngineers Technologies (Pvt.) Ltd.

## Description

This project demonstrates a simple **Euclidean Algorithm** implementation in RISC-V assembly to compute the Greatest Common Divisor (GCD) of two numbers.  
It runs in a bare-metal environment on **Spike** without `pk`, using minimal I/O support functions.  

Algorithm steps:  
- Compare two numbers.  
- Subtract the smaller from the larger.  
- Repeat until both numbers are equal (the GCD).

See `docs/BilalAli_FinalAssessment.pdf` for details and console output screenshots.
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



