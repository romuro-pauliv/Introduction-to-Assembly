## Logic Functions

Logic functions can be specified in a variety of ways. In a sense their expression is similar to problem specification in software development. A logical function can be specified verbally. For example, a majority function can be specified as: Output should be 1 whenever the majority of the inputs is 1. Similarly, an even-parity function can be specified as: Output (parity bit) is 1 whenever there is an odd number of Is in the input. The major problem with verbal specification is the imprecision and the scope for ambiguity.

We can make this specification precise by using a truth table. In the truth table method, for each possible input combination, we specify the output value. The truth table method makes sense for logical functions as the alphabet consists of only 0 and 1. The truth tables for the 3-input majority and even-parity functions are shown in table below.

| Majority Function | Even-Parity Function |
|-------------------|----------------------|
| <table> <thead> <tr> <th>A</th> <th>B</th> <th>C</th> <th>F<sub>1</sub></th> </tr> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </thead> </table>| <table> <thead> <tr> <th>A</th> <th>B</th> <th>C</th> <th>F<sub>2</sub></th> </tr> <tbody> <tr> <td>0</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>0</td> <td>1</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>0</td> <td>0</td> </tr> <tr> <td>0</td> <td>1</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>0</td> <td>0</td> <td>0</td> </tr> <tr> <td>1</td> <td>0</td> <td>1</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>0</td> <td>1</td> </tr> <tr> <td>1</td> <td>1</td> <td>1</td> <td>1</td> </tr> </tbody> </thead> </table> |

The advantage of the truth table method is that it is precise. This is important if you are interfacing with a client who does not understand other more concise forms of logic function expression. The main problem with the truth table method is that it is cumbersome as the number of rows grows exponentially with the number of logical variables. Imagine writing a truth table for a 10-variable function—it requires 2 <sup>20</sup> = 1024 rows!

We can also use logical expressions to specify a logical function. Logical expressions use the dot, +, and overbar to represent the `AND`, `OR`, and `NOT` operations, respectively. For example, the output of the `AND`gate in figure below is written as F = A <span>&#183;</span> B. Assuming that single letters are used for logical variables, we often omit the dot and write the previous `AND` function as F = A B. Similarly, the `OR` function is written as F = A + B. The output of the `NOT` gate is expressed as F = <span style="text-decoration:overline">A</span>. 