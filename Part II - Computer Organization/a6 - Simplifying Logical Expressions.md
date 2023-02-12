## Simplifying Logical Expressions

The sum-of-products and product-of-sums logical expressions can be used to come up with a crudc implementation that uses only the `AND`, `OR`, and `NOT` gates. The implementation process is straightforward. We illustrate the process for sum-of-products expressions. In [Figure 2.3](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a4%20-%20Logic%20Functions.md) shows the brute force implementation of the sum-of-products expression we derived for the 3-input majority function. If we simplify the logical expression, we can get a more efficient implementation Figure 2.5.

Let us now focus on how we can simplify the logical expressions obtained from truth tables. Our focus is on sum-of-products expressions. There are three basic techniques:

| Method | Info |
|--------|------|
| __Algebric Manipulation__ | Uses Boolean laws to derive a simplified logical expressions |
| __Karnaugh Map__ | Uses a graphical form and is suitable for sumplifying logical expressions with a small number of variables |
| __Quice-McCluskey methods__ | A tabular method and is particularly suitable for simplifying logical expressions with a large number of variables. In addition, this method can be used to automate the simplification process. |

In this section, we discuss the first two methods (for details on the last method, see [_Fundamentals of Computer Organization and Design_](https://www.amazon.com.br/Fundamentals-Computer-Organization-Sivarama-Dandamudi/dp/1475778333) by __Dandamudi__)

### Algebric Manipulation

In this method, we use the Boolean algebra to manipulate logical expressions. We need Boolean identities to facilitate this manipulation. These are discussed next. Following this discussion, we show how the identities developed can be used to simplify logical expressions. 

Table 2.2 presents some basic Boolean laws. For most laws, there are two versions: an `and` version and an `or` version. If there is only one version, we list it under the `and` version. We can transform a law form the `and` version to the `or` version by replacing each $1$ with a $0$, $0$ with a $1$, $+$ with a $\cdot$, and $\cdot$ with a $+$. This relationship is called `duality`.

We can use the Boolean laws to simplify the logical expressions. We illustrate this method by looking at the sum-of-produts expression for the majority function. A straightforward simplification leads us to the following expression:

$$ Majority function = \bar{A}BC + A\bar{B}C + AB\bar{C} + ABC$$

Thus, the expression: $AB\bar{C} + ABC$ can be:

$$AB\bar{C} + ABC = AB$$

Thus, the Majority Function is:

$$Majority function = \bar{A}BC + A\bar{B}C + AB$$

---

#### Boolean Laws

| Name | `and` version | `or` version |
|------|---------------|--------------|
| Identity      | $x \cdot 1 = x$        | $x + 0 = x$ |
| Complement    | $x \cdot  \bar{x} = 0$ | $x + \bar{x} = 1$ |
| Commutative   | $x \cdot y = y \cdot x$| $x + y = y + x$ |
| Distribution  | $x \cdot (y + z) = (x \cdot y) + (x \cdot z)$ | $x + (y \cdot z) = (x + y) \cdot (x + z)$ |
| Idempotent | $x \cdot x = x$ | $x + x = x$ |
| Null | $x \cdot 0 = 0$ | $x + 1 = 1$ |
| Involution  | $\bar{\bar{x}} = x$ | $-$ |
| Absorption  | $x \cdot (x + y) = x$ | $x + (x \cdot y) = x$ |
| Associative | $x \cdot (y \cdot z) = (x \cdot y) \cdot z$ | $x + (y + z) = (x + y) + z$ |
| de Morgan | $\overline{x \cdot y} = \bar{x} + \bar{y}$ | $\overline{x + y} = \bar{x} \cdot \bar{y}$ |

> Table 2.2 - Boolean Laws
---

Do you know if this is the final simplified form? This is the hard part in applying algebraic manipulation (in addition to the inherent problem of which rule should be applied). This method difinitely requires good intuition, which often implies that one needs experience to know if the final form has been derived. In our example, the expression can be further simplified. We start be rewriting the original logical expression by repeating the term $A B C$ twice and then simplifying the expression as shown below. Knowing $Majority Function = F_{m}$:

$$ F_{m} = \bar{A}BC + A\bar{B}C + AB\bar{C} + ABC +\underbrace{ABC + ABC}_\text{added extra} $$

$$ F_{m} = \underbrace{\bar{A}BC + ABC}_\text{BC} + \underbrace{A\bar{B}C + ABC}_\text{AC} + \underbrace{AB\bar{C} + ABC}_\text{AB} $$

$$ F_{m} = BC + AC + AB $$

This is the final expression. In the next section, we show a simpler method to dirive this expression. Figure 2.5 shows an implementation of this logical expression.

We can see the benefits of implementing the simplified logical expressions by comparing this implementation with the one shown in Figure 2.3. The simplified version reduces not only the gate count but also the gate complexity.

### Karnaugh Map Method

> Figure 2.5 - An implementation of the simplified 3-input majority function

<img align="left" src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/An%20Implementation%20of%20the%20simplified%203-input%20majority%20function.png?raw=true" alt="An Implementation of the simplified 3-input majority function"/>

This a graphical method and is suitable for simplifying logical expressions with a small number of Boolean variables (typically six of less). It provides a straightforward method to derive minimal sum-of-products expressions. This method is preferred to the algebraic method as it takes the guesswork out of the simplification process. For example, in the previous majority function example, it was not straughtforward to guess that we have to duplicate the term $ABC$ twice in order to get the final logical expression.

<br clear="left">

> Figure 2.6 - Maps used for simplifying 2-, 3-, and 4-variable logical expressions using the Karnaugh map method

<img src="https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/static/Maps%20used%20for%20simplifying%202-,%203-,%20and%204-%20variable%20logical%20expressions%20using%20the%20Karnaugh%20map%20method.png?raw=true" alt="Maps used for simplifying 2-, 3-, and 4- variable logical expressions using the Karnaugh map method"/>

The Karnaugh map method uses maps to represent the logical function output. Figure 2.6 shows the maps used for 2-, 3-, and 4-variable logical expressions. Each cell in these maps represents a particular input combination. Each cell is filled with the output value of the function corresponding to the input combination represented by the cell. For example, the bottom left-hand cell represents the input combination $A=1$ and $B=0$ for the two-variable map (Figure 2.6a), $A=1$, $B-0$, and $C=0$ for the three-variable map (Figure 2.6b), and $A=1$, $B=0$, $C=0$, and $D=0$ for the four-variable map (Figure 2.6c).

The basic idea behind this method is to label cell such that the neighboring cells differ in only one input bit position. This is the reason why the cells are labeled 00, 01, 11, 10 (notice the chance in the order of the last two labels from the normal binary number order). What we are doing is labeling with a Hamming distance of $1$. Hamming distance is the number of bit position in which two binary numbers differ. This labeling is also called `gray code`. Why are we so interested in this gray code labeling? Simply because we can then eliminate a variable as the following holds:

$$ AB\bar{C}D + ABCD = ABD$$

