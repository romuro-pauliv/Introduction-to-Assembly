## Introduction

A computer system has three main components: a central processing unit `(CPU)` or processor, a `memory unit`, and input/output `(I/O)` devices. These three components are interconnected by a `system bus`. The term bus is used to represent a group of **electrical signals** or the wires that carry these signals. Figure 2.1 shows details of how they are interconnected and what actually constitutes the system bus. As shown in this figure, the three major components of the system bus are the address bus, data bus, and control bus.

The width of address bus determines the memory addressing capacity of the processor. The width of data bus indicates the size of the data transferred between the processor and memory or I/O device. For example, the 8086 processor had a 20-bit address bus and a 16-bit data bus. The amount of physical memory that this processor can address is 2<sup>20</sup> bytes, or 1 MB, and each data transfer involves 16 bits. The Pentium processor, for example, has 32 address lines and 64 data lines. Thus, it can address up to 2<sup>32</sup> bytes, or a 4 GB memory.

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Simplified%20block%20diagram%20of%20a%20computer%20system.png?raw=true" alt="drawing" width="450"/>

Furthermore, each data transfer can move 64 bits. In comparison, the Intel 64-bit processor Itanium uses 64 address lines and 128 data lines.

The control bus consists of a set of control signals. Typical control signals include memory read, memory write, I/O read, I/O write, interrupt, interrupt acknowledge, bus request, and bus grant. These control signals indicate the type of action taking place on the system bus. For example, when the processor is writing data into the memory, the memory write signal is asserted. Similarly, when the processor is reading from an I/O device, the I/O read signal is asserted.

The system memory, also called `main memory` or `primary memory`, is used to store both program instructions and data. I/O devices such as the keyboard and display are used to provide user interface. I/O devices are also used to interface with secondary storage devices such as disks.

| < [Digital Logic Circuits](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a1%20-%20Digital%20Logic%20Circuits.md) | [Simple Logic Gates]() > |
| -|-|

