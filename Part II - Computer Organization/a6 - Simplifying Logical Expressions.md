## Simplifying Logical Expressions

The sum-of-products and product-of-sums logical expressions can be used to come up with a crudc implementation that uses only the `AND`, `OR`, and `NOT` gates. The implementation process is straightforward. We illustrate the process for sum-of-products expressions. This [Figure](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/561e2bae861064c79f404cee20d5f676624aceff/Part%20II%20-%20Computer%20Organization/a4%20-%20Logic%20Functions.md?plain=1#L15) this figure shows the brute force implementation of the sum-of-products expression we derived for the 3-input majority function. If we simplify the logical expression, we can get a more efficient implementation (See this [Figure]()).

Let us now focus on how we can simplify the logical expressions obtained from truth tables. Our focus is on sum-of-products expressions. There are three basic techniques:

| Method | Info |
|--------|------|
| __Algebric Manipulation__ | Uses Boolean laws to derive a simplified logical expressions |
| __Karnaugh Map__ | Uses a graphical form and is suitable for sumplifying logical expressions with a small number of variables |
| __Quice-McCluskey methods__ | A tabular method and is particularly suitable for simplifying logical expressions with a large number of variables. In addition, this method can be used to automate the simplification process. |

In this section, we discuss the first two methods (for details on the last method, see [_Fundamentals of Computer Organization and Design_](https://www.amazon.com.br/Fundamentals-Computer-Organization-Sivarama-Dandamudi/dp/1475778333) by __Dandamudi__)

### Algebric Manipulation

In this method, we use the Boolean algebra to manipulate logical expressions. We need Boolean identities to facilitate this manipulation. These are discussed next. Following this discussion, we show how the identities developed can be used to simplify logical expressions. 

This [Table](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a6%20-%20Simplifying%20Logical%20Expressions.md#boolean-laws) presents some basic Boolean laws. For most laws, there are two versions: an `and` version and an `or` version. If there is only one version, we list it under the `and` version. We can transform a law form the `and` version to the `or` version by replacing each 1 with a 0, 0 with a 1, + with a <span>&#183;</span>, and <span>&#183;</span> with a +. This relationship is called `duality`.

We can use the Boolean laws to simplify the logical expressions. We illustrate this method by looking at the sum-of-produts expression for the majority function. A straightforward simplification leads us to the following expression:

$$ Majority function = A'BC + AB'C + ABC' + ABC$$

Thus, the expression: $$ ABC' + ABC $$ can be:

$$ ABC' + ABC = AB$$

Thus, the Majority Function is:

$$ Majority function = A'BC + AB'C + AB $$

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

---

Do you know if this is the final simplified form? This is the hard part in applying algebraic manipulation (in addition to the inherent problem of which rule should be applied). This method difinitely requires good intuition, which often implies that one needs experience to know if the final form has been derived. In our example, the expression can be further simplified. 