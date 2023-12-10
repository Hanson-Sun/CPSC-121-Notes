# Weak Induction Proofs

## Goals

1. Convert sequences to and from explicit formulas that describe the sequence.
2. Convert sums to and from summation/$\Sigma$ notation.
3. Convert products to and from product/$\Pi$ notation.
4. Manipulate formulas in summation/product notation by adjusting their bounds, merging or splitting summations/products, and factoring out values.
5. Identify the base, induction hypothesis and step in an induction proof.

6. Establish properties of self-referential structures using inductive proofs that naturally build on those self-references.
7. Formally prove properties of the non-negative integers (or a subset) that have appropriate self-referential structure using weak induction.
8. Recognize the differences between a proof with an IH of P(n-1) for a proof with an IH of P(n).

# Intro

## Sequences
- A function whose domain is either all the integers between two given integers or all the integers greater than or equal to a given integer
- $a_1, a_2, a_3, ..., a_n$
  - $a$ is a term, and the subscript is called the index

## Summation Notation
$$\sum^n_{k = m}a_k = a_m + a_{m+1} + a_{m+2} + ... + a_{m+n}$$

### Telescoping sum
- the middle terms cancel out, leaving only the first and last terms.

## Product Notation
$$\prod^n_{k = m}a_k = a_m \cdot a_{m+1}\cdot a_{m+2}\cdot \cdot \cdot a_{m+n}$$

## Factorial and “n Choose r” Notation
### Factorials
$$n! = n \cdot (n-1) \cdot (n-2) \cdot \cdot \cdot 3 \cdot 2 \cdot 1$$
or recursively,
$$n! = \begin{cases}
    1 & n = 0 \\
    n(n-1) & n \ge 1.
\end{cases}$$
Note: the zero factorial is defined as $0! = 1$

### Combinations
$n, r \in \mathbb{Z}, 0 \le r \le n$, the symbol
$${n \choose r}$$
"n choose r" is the number of distinct groups $r$ that can be chosen from $n$. We define
$${n \choose r} = \frac{n!}{r!(n-r)!}.$$


# Weak Induction
 Observe patterns in a few terms of a sequence $\implies$ arrive at a generalized formula that is representative of the whole sequence. Think domino effect.

## Principle of Mathematical Induction
Let $P(n)$ be a property that is defined for integers $n$, and let $a$ be a fixed integer. Suppose the following two statements are true:
1. $P(a)$ is true
2. For every integer $k \ge a$, if $P(k)$ is true then $P(k+1)$ is true.
Then the following statement is true
$$\forall n \in \mathbb{Z}, n \ge a \implies P(n)$$

**Imporant:** induction only shows that that the formula works for **integers**, it is **insufficient** to use induction for real numbers.

## Summary of Proof Process
1. rewrite and state $P(n)$ clearly
2. Show that $P(1)$ is true, or whatever first value
3. Show that for every integer $k \ge 1$, if $P(k)$ is true then $P(k+1)$ is also true (inductive hypothesis)
   - Suppose that $P(k)$ is true for a particular but arbitrarily chosen integer $k \ge 1$ ...

4. Show that both sides are equal
   - In general, $P(k) + \text{ last term} = P(k+1)$

5. Conclude and state $P(n)$ is true
   - Since we have proved both the basis step and the inductive step, we conclude that the theorem is true.

Induction proves sequences that have a **closed form** (that can be written as a simple formula without ... or summation).



## Worksheet
> prove using induction that $\forall n \in \mathbb{Z}, n \ge 4 \implies 2^n < n!$
>
> for $n = 4, 2^4 < n!$
> 
> assume true for $n = k$ and prove for $n = k + 1$
> $$2^{k + 1} = 2^k * 2 < (k + 1)! = (k+1)k!$$
> we know that $2^k < n!$, moreover, we also know that $2 < k + 1$, therefore
> $$2^{k + 1} < (k + 1)!$$
> it works now!!


> Prove that for every value of $a \not = 0, 1$, 
> $$\sum^t_{i = 0}a^i = \frac{a^{t + 1} - 1}{a-1}$$
> For $t = 1$,
> $$1 + a = \frac{a^2 - 1}{a - 1} = a + 1$$ 
> Assume this is true for t = k, then we try to show for $k+1$
> $$\sum^{k+1}_{i = 0}a^i = \sum^{k}_{i = 0}a^i + a^{k+1}$$
> $$= \frac{a^{k + 1} - 1}{a-1} + a^{k+1} = \frac{a^{k + 1} - 1 + a^{k+2} - a^{k+1}}{a-1} = \frac{a^{k+2} - 1}{a-1}$$
> we won! Therefore, the proposition is true!

> Prove that for every $n \ge 1$
> $$\sum^n_{t = 1}\frac{1}{i^2} \le 2 - \frac{1}{n}$$
> for $n = 1$
> $$1 = 2 - 1$$
> Assume the proposition is true for $n = k$, we then show for $k+1$
> $$\sum^{k + 1}_{t = 1}\frac{1}{i^2} \le 2 - \frac{1}{k+1}$$
> $$\sum^{k}_{t = 1}\frac{1}{i^2} + \frac{1}{(k + 1)^2}\le 2 - \frac{1}{k+1}$$
> $$2 - \frac{1}{k} + \frac{1}{(k + 1)^2}\le 2 - \frac{1}{k+1}$$
> We need to use the fact that $\frac{1}{(k + 1)^2} < \frac{1}{k(k+1)}$
> $$2 - \frac{1}{k} + \frac{1}{k(k + 1)}\le 2 - \frac{1}{k+1}$$
> $$2 - \frac{1}{k} + \frac{1}{k} - \frac{1}{(k + 1)}\le 2 - \frac{1}{k+1}$$
> $$2 - \frac{1}{(k + 1)}\le 2 - \frac{1}{k+1}$$
> ohhhh its true af!!



