## Why Program in Assembly Language?

The previous section gives enough reasons to discourage you from programming in the assembly language. However, there are two main reasons why programming is still done in assembly language:

- Efficiency
- Accessbility to system hardware

### Efficiency

Efficiency refers to how "good" a program is in achieving a given objective. Here we consider two objectives based on space **space-efficiency** and time **time-efficiency**.

### Space-efficiency

Space-efficiency refers to the memory requirements of a program, that is, the size of the executable code. Program A is said to be more space-efficient if it takes less memory space than program B to perform the same task. Very often, programs written in the assembly language tend to be more compact than those written in a high-level language.

### Time-efficiency

Time-efficiency refers to the time taken to execute a program. Obviously a program that runs faster is said to be better from the time-efficiency point of view. If we craft assembly language programs carefully, they tend to run faster than their high-level language counterparts.

---

As an aside, we can also define a third objective: how fast a program can be developed (i.e. write code and debug). This objective is related to the programmer productivity, and assembly language loses the battle to high-level languages as discussed in the last section.

The superiority of assembly language in generating compact code is becoming increasingly less important for several reasons. First, the savings in space pertain only to the program code and not to its data space. Thus, depending on the application, the savings in space obtained by converting an application program from some high-level language to the assembly language may not be substantial. Second, the cost of memory has been decreasing and memory capacity has been increasing. Thus, the size of a program is not a major hurdle anymore. Finally, compilers are becoming "smarter" in generating code that is both space- and time-efficient. However, there are systems such as embedded controllers and handheld devices in which space-efficiency is important.

One of the main reasons for writing programs in an assembly language is to generate code
that is time-efficient. The superiority of assembly language programs in producing efficient code is a direct manifestation of _specificity_.

That is, assembly language programs contain only the code that is necessary to perform the given task. Even here, a "smart" compiler can optimize the code that can compete well with its equivalent written in the assembly language. Although the gap is narrowing with improvements in compiler technology, assembly language still retains its advantage for now. 

The other main reason for writing assembly language programs is to have **direct control over system hardware**. High-level languages, on purpose, provide a restricted (abstract) view of the underlying hardware. Because of this, it is almost impossible to perform certain tasks that require access to the system hardware. For example, writing a device driver for a new scanner on the market almost certainly requires programming in assembly language. Since assembly language does not impose any restrictions, you can have direct control over the system hardware. If you are developing system software, you cannot avoid writing assembly language programs.

| < [Advantages of High-Level Languages](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20I%20-%20Overview/a4%20-%20Advantages%20of%20High-Level%20Languages.md) | [Typical Applications]() > |
| -|-|