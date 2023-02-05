## Introduction

A computer system has three main components: a central processing unit `(CPU)` or processor, a `memory unit`, and input/output `(I/O)` devices. These three components are interconnected by a `system bus`. The term bus is used to represent a group of **electrical signals** or the wires that carry these signals. Figure 2.1 shows details of how they are interconnected and what actually constitutes the system bus. As shown in this figure, the three major components of the system bus are the address bus, data bus, and control bus.

The width of address bus determines the memory addressing capacity of the processor. The width of data bus indicates the size of the data transferred between the processor and memory or I/O device. For example, the 8086 processor had a 20-bit address bus and a 16-bit data bus. The amount of physical memory that this processor can address is 2<sup>20</sup> bytes, or 1 MB, and each data transfer involves 16 bits. The Pentium processor, for example, has 32 address lines and 64 data lines. Thus, it can address up to 2<sup>32</sup> bytes, or a 4 GB memory.

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Simplified%20block%20diagram%20of%20a%20computer%20system.png?raw=true" alt="drawing" width="400"/>


| < [Digital Logic Circuits](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a1%20-%20Digital%20Logic%20Circuits.md) | [Simple Logic Gates]() > |
| -|-|

