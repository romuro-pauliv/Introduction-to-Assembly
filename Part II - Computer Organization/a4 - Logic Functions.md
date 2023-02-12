## Logic Functions

Logic functions can be specified in a variety of ways. In a sense their expression is similar to problem specification in software development. A logical function can be specified verbally. For example, a majority function can be specified as: Output should be 1 whenever the majority of the inputs is 1. Similarly, an even-parity function can be specified as: Output (parity bit) is 1 whenever there is an odd number of Is in the input. The major problem with verbal specification is the imprecision and the scope for ambiguity.

We can make this specification precise by using a truth table. In the truth table method, for each possible input combination, we specify the output value. The truth table method makes sense for logical functions as the alphabet consists of only 0 and 1. The truth tables for the 3-input majority and even-parity functions are shown in table below.

| Majority Function | Even-Parity Function |
|-------------------|----------------------|
| <table> <thead> <tr> <th>A</th> <th>B</th> <th>C</th> <th>F<sub>1</sub></th> </tr> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </thead> </table>| <table> <thead> <tr> <th>A</th> <th>B</th> <th>C</th> <th>F<sub>2</sub></th> </tr> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </thead> </table> |

The advantage of the truth table method is that it is precise. This is important if you are interfacing with a client who does not understand other more concise forms of logic function expression. The main problem with the truth table method is that it is cumbersome as the number of rows grows exponentially with the number of logical variables. Imagine writing a truth table for a 10-variable function—it requires 2 <sup>20</sup> = 1024 rows!

We can also use logical expressions to specify a logical function. Logical expressions use the dot, +, and overbar to represent the `AND`, `OR`, and `NOT` operations, respectively. For example, the output of the `AND`gate in figure below is written as F = A <span>&#183;</span> B. Assuming that single letters are used for logical variables, we often omit the dot and write the previous `AND` function as F = A B. Similarly, the `OR` function is written as F = A + B. The output of the `NOT` gate is expressed as F = <span>&Amacr;</span>. Some authors use a prime to represent the `NOT` operation as in F = A' mainly because of problems with typesetting the overbar (how it happend here on GitHub).

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Logical%20circuit%20to%20implement%20the%203-input%20majority%20function.png?raw=true" width=400 alt="Logical circuit to implement the 3-input majority function"/>

The logical expressions for our 3-input majority and even-parity functions are shown below:

- 3-inputs majority function = A B + B C + A C, 
- 3-inputs even-parity function = A' B' C + A' B C' + A B' C' + A B C.

An advantage of this form of specification is that it is compact while it retains the precision of the truth table method. Another major advantage is that logical expressions can be manipulated to come up with an efficient design. We say more on this topic later.

The final form of specification uses a graphical notation. Figure above shows the logical circuit to implement the 3-input majority function. As with the last two methods, it is also precise but is more useful for hardware engineers to implement logical functions.

A logic circuit designer may use all the three forms during the design of a logic circuit. A simple circuit design involves the following steps:

- First we have to obtain the truth table from the input specifications.
- Then we derive a logical expression from the truth table.
- We do not want to implement the logical expression derived in the last step as it often contains some redundancy, leading to an inefficient design. For this reason, we simplify the logical expression.
- In the final step, we implement the simplified logical expression. To express the implementation, we use the graphical notation.

The following sections give more details on these steps.

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Logic%20circuit%20for%20the%203-input%20majority%20function%20using%20the%20bubble%20notation.png?raw=true" width=400 alt="Logical circuit to implement the 3-input majority function"/>

#### Bubble Notation

In large circuits, drawing inverters can be avoided by following what is known as the `bubble` notation. The use of bubble notation simplifies the circuit diagrams.

<br clear="left">
<br>
<br>

| < [Simple Logic Gates](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a3%20-%20Simple%20Logic%20Gates.md) | [Deriving Logical Expressions](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a5%20-%20Deriving%20Logical%20Expressions.md) > |
| -|-|