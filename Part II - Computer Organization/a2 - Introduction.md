## Introduction

A computer system has three main components: a central processing unit `(CPU)` or processor, a `memory unit`, and input/output `(I/O)` devices. These three components are interconnected by a `system bus`. The term bus is used to represent a group of **electrical signals** or the wires that carry these signals. Figure below shows details of how they are interconnected and what actually constitutes the system bus. As shown in this figure, the three major components of the system bus are the address bus, data bus, and control bus.

The width of address bus determines the memory addressing capacity of the processor. The width of data bus indicates the size of the data transferred between the processor and memory or I/O device. For example, the 8086 processor had a 20-bit address bus and a 16-bit data bus. The amount of physical memory that this processor can address is 2<sup>20</sup> bytes, or 1 MB, and each data transfer involves 16 bits. The Pentium processor, for example, has 32 address lines and 64 data lines. Thus, it can address up to 2<sup>32</sup> bytes, or a 4 GB memory.

> Figure 2.1 - Sumplified block diagram of a computer system

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Simplified%20block%20diagram%20of%20a%20computer%20system.png?raw=true" alt="drawing" width="450"/>

Furthermore, each data transfer can move 64 bits. In comparison, the Intel 64-bit processor Itanium uses 64 address lines and 128 data lines.

The control bus consists of a set of control signals. Typical control signals include memory read, memory write, I/O read, I/O write, interrupt, interrupt acknowledge, bus request, and bus grant. These control signals indicate the type of action taking place on the system bus. For example, when the processor is writing data into the memory, the memory write signal is asserted. Similarly, when the processor is reading from an I/O device, the I/O read signal is asserted.

The system memory, also called `main memory` or `primary memory`, is used to store both program instructions and data. I/O devices such as the keyboard and display are used to provide user interface. I/O devices are also used to interface with secondary storage devices such as disks.

The system bus is the communication medium for data transfers. Such data transfers are called bus `transactions`. Some examples of bus transactions are memory read, memory write, I/O read, I/O write, and interrupt. Depending on the processor and the type of bus used, there may be other types of transactions. For example, the Pentium processor supports a burst mode of data transfer in which up to four 64 bits of data can be 
transferred in a burst cycle.

Every bus transaction involves a `master` and a `slave`. The master is the initiator of the transaction and the slave is the target of the transaction. For example, when the processor wants to read data from the memory, it initiates a bus transaction, also called a bus cycle, in which the processor is the bus master and memory is the slave. The processor usually acts as the master of the system bus, while components like memory are usually slaves. Some components may act as slaves for some transactions and as masters for other transactions.

When there is more than one master device, which is typically the case, the device requesting the use of the bus sends a `bus request` signal to the bus arbiter using the bus request control line. If the bus arbiter grants the request, it notifies the requesting device by sending a signal on the `bus grant` control line. The granted device, which acts as the master, can then use the bus for data transfer. The bus-request-grant procedure is called `bus protocol`. Different buses use different bus
protocols. In some protocols, permission to use the bus is granted for only one bus cycle; in others, permission is granted until the bus master relinquishes the bus.

The hardware that is responsible for executing machine language instructions can be built
using a few basic building blocks. These building blocks are called logic gates. These logic gates implement the familiar logical operations such as `AND`, `OR`, `NOT`, and so on, in hardware. The purpose of this chapter is to provide the basics of the digital hardware. The next two chapters introduce memory organization and architecture of the Intel IA-32 processors.

Our discussion of digital logic circuits is divided into three parts. The first part deals with the basics of digital logic gates. Then we look at two higher levels of abstractions—combinational and sequential circuits. In combinational circuits, the output of the circuit depends solely on the current inputs applied to the circuit. The adder is an example of a combinational circuit. The output of an adder depends only on the current inputs. On the other hand, the output of a sequential circuit depends not only on the current inputs but also on the past inputs. That is, output depends both on the current inputs as well as on how it got to the current state. For example, in a binary counter, the output depends on the current value. The next value is obtained by incrementing the current value (in a way, the current state represents a snapshot of the past inputs). That is, we cannot say what the output of a counter will be unless we know its current state. Thus, the counter is a sequential circuit. We review both combinational and sequential circuits in this chapter.

| < [Digital Logic Circuits](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a1%20-%20Digital%20Logic%20Circuits.md) | [Simple Logic Gates](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a3%20-%20Simple%20Logic%20Gates.md) > |
| -|-|

