## Introduction

A user's view of a computer system depends on the degree of abstraction provided by the underlying software. Figure 1.1 shows a hierarchy of levels at which one can interact with a computer system. Moving to the top of the hierarchy shields the user from the lower-level details. At the highest level, the user interaction is limited to the interface provided by application software such as spreadsheet, word processor, and so on. The user is expected to have only a rudimentary knowledge of how the system operates. Problem solving at this level, for example, involves composing a letter using the word processor software.

> Fig. 1.1 - A user's view of a computer system

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20I%20-%20Overview/static/A%20user's%20view%20of%20a%20computer%20system.png?raw=true" alt="A user's view of a computer system">

At the next level, problem solving is done in one of the high-level languages such as C and Java. A user interacting with the system at this level should have detailed knowledge of software development. Typically, these users are application programmers. Level 4 users are knowledgeable about the application and the high-level language that they would use to write the application software. They may not, however, know internal details of the system unless they also happen to be involved in developing system software such as device drivers, assemblers, linkers, and so on.

Both levels 4 and 5 are system `independent`, that is, independent of a particular processor used in the system. For example, an application program written in C can be executed on a system with an Intel processor or a PowerPC processor without modifying the source code. All we have to do is recompile the program with a C compiler native to the target system. In contrast, software development done at all levels below level 4 is system dependent.

Assembly language programming is referred to as low-level programming because each assembly language instruction performs a much lower-level task compared to an instruction in a high-level language. As a consequence, to perform the same task, assembly language code tends to be much larger than the equivalent high-level language code.

Assembly language instructions are native to the processor used in the system. For example, a program written in the Intel assembly language cannot be executed on the PowerPC processor. Programming in the assembly language also requires knowledge about system internal details such as the processor architecture, memory organization, and so on.

Machine language is a close relative of the assembly language. Typically, there is a one-to-one correspondence between the assembly language and machine language instructions. The processor understands only the machine language, whose instructions consist of strings of 1s and 0s. We say more on these two languages in the next section.

Even though assembly language is considered a low-level language, programming in assembly language will not expose you to all the nuts and bolts of the system. Our operating system hides several of the low-level details so that the assembly language programmer can breathe easy. For example, if we want to read input from the keyboard, we can rely on the services provided by the operating system.

Well, ultimately there has to be something to execute the machine language instructions. This is the system hardware, which consists of digital logic circuits and the associated support electronics. A detailed discussion of this topic is beyond the scope of this repository. On `computer organization` discuss this topic in detail.

| < [Overview](https://github.com/romuro-pauliv/Introduction-to-Assembly/tree/main) | [What Is Assembly Language?](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20I%20-%20Overview/a3%20-%20%20What%20Is%20Assembly%20Language.md) > |
| -|-|
