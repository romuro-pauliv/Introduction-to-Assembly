## Simple Logic Gates

You are familiar with the three basic logical operators: `AND`, `OR`, and `NOT`. Digital circuits to implement these and other logical functions are called gates. The [system (a)](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a3%20-%20Simple%20Logic%20Gates.md#basic-logic-gates-a) shows the symbol notation used to represent the `AND`, `OR`, and `NOT` gates. The `NOT` gate is often referred to as the inverter. We have also included the truth table for each gate. A `truth table` is a list of all possible inputs combinations and their corresponding output. For example, if you treat a logical zero as representing false and logical 1 truth, you can see that the truth table for the `AND` gate represents the logical `AND` operation.

Even Though the three gates shown in [system (a)](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a3%20-%20Simple%20Logic%20Gates.md#basic-logic-gates-a) are sufficient to implement any logical functions, it is convenient to implement certain other gates. [System (b)](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a3%20-%20Simple%20Logic%20Gates.md#some-additional-logic-gates-b) shows three popularly used gates. The `NAND` gate is equivalent to and `AND` gate followed by a `NOT` gate. Similarly, the `NOR` gates are a combination of the `OR` and `NOT` gates. The exclusive-OR `(XOR)` gate generates a 1 output whenever the two inputs differ. This property makes it useful in certain applications such as parity generation.

Logic gates are in turn built using transitors. One transistor is enough to implement a `NOT` gate. But we need three transistors to implement the `AND` and `OR` gates. It is interesting to note that, contrary to our intuition, implementing the `NAND` and `NOR` gates requires only two transistors. In this sense, transistors are the basic electronic components of digital hardware circuits. For example, the Pentium processor introduced in 1993 consists of about 3 million transistors. It is now possible to design chips with more that 100 million transistors.

#### Basic Logic Gates (A)

| Name | Logic Gate | Truth Table |
|------| -----------|-------------|
| `AND` | ![AND Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/AND%20gate.png?raw=true) | <table> <thead>  <tr> <th>A</th> <th>B</th> <th>F</th> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </tr> </thead> </table> |
| `OR` | ![OR Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/OR%20gate.png?raw=true) |<table> <thead>  <tr> <th>A</th> <th>B</th> <th>F</th> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </tr> </thead> </table>|
| `NOT` | ![NOT Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/NOT%20gate.png?raw=true) | <table> <thead>  <tr> <th>A</th> <th>F</th> <tbody> <tr> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td></tr></tbody> </tr> </thead> </table>|

#### Some Additional Logic Gates (B)

| Name | Logic Gate | Truth Table |
|------| -----------|-------------|
| `NAND` | ![NAND Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/NAND%20gate.png?raw=true) | <table> <thead>  <tr> <th>A</th> <th>B</th> <th>F</th> <tbody> <tr> <td>0</td> <td>0</td> <td>1</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> </tr> </tbody> </tr> </thead> </table> |
| `NOR` | ![NOR Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/NOR%20gate.png?raw=true) | <table> <thead>  <tr> <th>A</th> <th>B</th> <th>F</th> <tbody> <tr> <td>0</td> <td>0</td> <td>1</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> </tr> </tbody> </tr> </thead> </table> |
| `XOR` | ![XOR Gate](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/XOR%20gate.png?raw=true) | <table> <thead>  <tr> <th>A</th> <th>B</th> <th>F</th> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> </tr> </tbody> </tr> </thead> </table> |

There is a `propagation delay` associated with each gate. This delay represents the time required for the output to react to an input. The propagation delay depends on the complexity of the circuit and the technology used. Typical values for the TTL gates are in the range of a few nanoseconds (about 5 to 10 ns). A nanosecond (ns) is 10<sup>-9</sup> second.

In addition to propagation delay, other parameters should be taken into consideration in designing and building logic circuits. Two such parameters are fanin and fanout.

| Type | Info |
|------|------|
| `Fanin` | Specifies the maximum number of inputs a logic gate can have |
| `Fanout` | Refers to the driving capacity of an output. Fanout specifies the maximum number of gates that the output of a gate can drive |

A small set of independent logic gates (such as AND, NOT, NAND, etc.) are packaged into an integrated circuit `(IC)` chip, or **"chip"** for short. These ICs are called small-scale integrated `(SSI)` circuits and typically consist of about 1 to 10 gates. gates. Medium-scale integrated `(MSI)` circuits represent the next level of integration (typically between 10 and 100 gates). Both SSI and MSI were introduced in the late 1960s. `LSI` (large-scale integration), introduced in early 1970s, can integrate between 100 and 10,000 gates on a single chip. The final degree of integration, `VLSI` (very large scale integration), was introduced in the late 1970s and is used for complex chips such as microprocessors that require more than 10,000 gates.

| IC Types | Info | Gates |
|----------|------|-------|
| `SSI`    | Small-Scale Integration | 1 to 10 |
| `MSI`    | Medium-Scale Integration | 10 to 100 |
| `LSI`    | Large-Scale Integration | 100 to 10,000 |
| `VLSI`   | Very Large Scale Integration | more than 10,000 |
 
| < [Introduction](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a2%20-%20Introduction.md) | [Logic Functions](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a4%20-%20Logic%20Functions.md) > |
| -|-|