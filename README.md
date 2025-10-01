# RISC-V Spike Playground
Bare metal RISC-V assembly task for Spike (no pk) <br>
- Author: Bilal Ali <br>
- Company: 10xEngineers Technologies (Pvt.) Ltd.

## Description

This task explains the RISC-V calling convention rules regarding:<br>
- Caller-saved registers<br>
- Callee-saved registers<br>
The rules are defined in the RISC-V ABI Specification (topics 1.1 and 2.1).<br>
When functions call each other, registers may get overwritten. To prevent losing important data, the ABI defines which side (caller or callee) is responsible for saving/restoring registers.<br>
### Caller-Saved Registers
Registers: t0–t6 (temporaries), a0–a7 (argument/return values)
Rule: The caller must assume these registers will be overwritten by the callee.
Use case: When the caller needs the value after the function call, it must save it to the stack before calling another function.
### Callee-Saved Registers
Registers: s0–s11 (saved registers), plus ra (return address), sp (stack pointer), gp, tp
Rule: The callee must preserve their values. If the callee wants to use them, it must save them on entry and restore them before returning.
Use case: Caller can rely on these registers remaining unchanged across function calls.

See `docs/BilalAli_Task2.pdf` for details and console output screenshots.
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



