## Deriving Logical Expressions

We can a logical expressions from a truth table in one of two forms: _sum-of-products_ `(SOP)` and _product-of-sums_ `(POS)` forms. 

> In `sum-of-products` form, we specify the combination of inputs for which the output should be 1.

> In `product-of-sums` form, we specify the combinations of inputs for which output should be 0.

### Sum-of-Products Form

In this form, each input combination for which the output is 1 is expressed as an `and` term. This is the _product term_ as we use <span>&#183;</span> to represent the `AND` operation. These product terms are `OR` together. That is why it is called sum-of-products as we use + for the `OR` operation to get the final logical expression. In deriving the products terms, we write the variable if its value is 1 or its complement if 0. 

Let us look at the 3-input majority function. The truth table is given in this [Table](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/39c520f700e69428264b5063be441e9605645763/Part%20II%20-%20Computer%20Organization/a4%20-%20Logic%20Functions.md?plain=1#L7). There are four 1 output in this function. So, our logical expression will have four products terms. The first product term we write is for row 4 with a 1 output. Since A has a value of 0, we use its complement in the product term while using B and C as they have 1 as their value in this row. Thus, the product term for this row is A'B C. The product term for row 6 is A B' C. Product terms for rows 7 and 8 are A B C' and A B C, respectively. `ORing` these four product term gives the logical expression as __A' B C + A B' C + A B C' + A B C__. 

### Products-of-Sum Form

This is the dual form of the sum-of-products form. We assentially complement what we have done to obtain the sum-of-products expression. Here we look for rows that have a 0 output. Each such row input variable combination is expressed as an `OR` term. In this `OR` term, we use the variable if its value in the row being considered is 0 or its complement if 1. We `AND` these sum terms to majority function is __(A + B + C)(A + B + C')(A + B' + C)(A' + B + C)__.

This logical expression and the sum-of-products expressions derived before represent the same truth table. Thus, despite their appearence, these two logical expressions are logically equivalent. We can prove this logical equivalence by using algebric manipulation method decribed in the next section.

| < [Logic Functions](https://github.com/romuro-pauliv/Introduction-to-Assembly/blob/main/Part%20II%20-%20Computer%20Organization/a4%20-%20Logic%20Functions.md) | [Simplifying Logical Expressions]() > |
| -|-|