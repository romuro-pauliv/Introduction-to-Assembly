Assembly language is directly influenced by the instruction set and architecture of the processor. In this repository, we focus on the assembly language for the **Intel 32-bit processors** like the Pentium. The assembly language code must be processed by a program in order to generate the machine language code. Assembler is the program that translates the assembly language code into the machine language.

`NASM` (Netwide Assembler), `MASM` (Microsoft Assembler), and `TASM` (Borland Turbo Assembler) are some of the popular assemblers for the Intel processors. In this book, we use the `NASM` assembler. There are two main reasons for this selection: 
- It is a **free assembler**
- `NASM` supports a variety of formats including the formats used by Microsoft Windows, Linux and a host of others.

Are you curious as to how the assembly language instructions look like? Here are some examples:

```Assembly
inc result
mov class_size,     45
and mask1,          128
add marks,          10
```

The first instruction increments the variable `result`. This assembly language instruction is equivalent to

```C
result++;
```
in C. The second instruction initializes `class_size` to 45. The equivalent statement in C is

```C
class_size = 45;
```
The third instruction performs the bitwise and operation on `mask1` and can be expressed in C as

```C
mask1 = mask1 & 128;
```

The last instruction updates `marks` by adding 10. In C, this is equivalent to
```C
marks = marks + 10;
```
These examples illustrate several points:

1. Assembly language instructions are cryptic.
2. Assembly language operations are expressed by using mnemonics (like `and` and `inc`).
3. Assembly language instructions are low level. For example, we cannot write the the following in the assembly language:

```Assembly
add     marks, value
```
This instruction is invalid because two variables, `marks` and `value`, are not allowed in a single instruction.

We appreciate the readability of the assembly language instructions by looking at the equivalent machine language instructions. Here are some machine languages examples:

| Assembly language | Operation | Machine language (in hex) |
|-------------------|-----------|---------------------------|
| `nop`             | No operation   | 90                   |
| `inc result`      | Increment      | FF060A00             |
| `mov class_size, 45`| Copy         | C7060C002D00         |
| `and mask, 128` | Logical and      | 80260E0080           |
| `add marks, 10` | Integer addition | 83060F000A           |

It is obvious from these examples that understanding the code of a program in the machine language is almost impossible. Since there is a one-to-one correspondence between the instructions of the assembly language and the machine language, it is fairly straightforward to translate instructions from the assembly language to the machine language. As a result, only a masochist would consider programming in a machine language. However, life was not so easy for some of the early progranmiers. When microprocessors were first introduced, some programming was in fact done in machine language!

| < [Introduction](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20I%20-%20Overview/a2%20-%20Introduction.md) | [Advantages of High-Level Languagess]() > |
| -|-|
