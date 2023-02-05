## Simple Logic Gates

You are familiar with the three basic logical operators: `AND`, `OR`, and `NOT`. Digital circuits to implement these and other logical functions are called gates. The system (a) shows the symbol notation used to represent the `AND`, `OR`, and `NOT` gates. The `NOT` gate is often referred to as the inverter. We have also included the truth table for each gate. A `truth table` is a list of all possible inputs combinations and their corresponding output. For example, if you treat a logical zero as representing false and logical 1 truth, you can see that the truth table for the `AND` gate represents the logical `AND` operation.

Even Though the three gates shown in system (a) are sufficient to implement any logical functions, it is convenient to implement certain other gates. System (b) shows three popularly used gates. The `NAND` gate is equivalent to and `AND` gate followed by a `NOT` gate. Similarly, the `NOR` gates are a combination of the `OR` and `NOT` gates. The exclusive-OR `(XOR)` gate generates a 1 output whenever the two inputs differ. This property makes it useful in certain applications such as parity generation.

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

