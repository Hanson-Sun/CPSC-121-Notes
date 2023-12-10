# Indirect Proofs

## Goals:
- How to apply contrapositive on a proof.
- How to apply contradiction on a proof.

- Devise and attempt multiple different, appropriate proof strategies.
- Check why indirect proofs are valid.
- Practice indirect proofs and identify common strategies used on those proofs

## Method of Proof by Contradiction
Because the negation of a statement and the original statement cannot be both true, if we show the negation is a contradiction, the original statement must be true. The method of contradiction is as follow:

1. Suppose the statement to br proved is false. That means, suppose the negation of the statement is true.
2. Show that this supposition leads logically to a contradiction

3. Conclude that the statement to be proved is true


### Use cases

There are no exact cases where proof by induction should be used, however, where are some general cases where it might be easier than direct proofs
- to show there is no objects that satisfy a property
- to show a certain object doesn't have a property


## Argument by Contrapositions
Because the contrapositive is logically equivalent with the original statement, proving the contrapositive is the same as proving the original statement. The general steps of an argument by contraposition is as follows:
1. Express the statement to be proved in the form 
   $$\forall x \in D, P(x) \implies Q(x)$$ 
   (this can be done mentally)
2. Rewrite the statement in contrapositive form 
   $$\exist x \in D, \lnot Q(x) \implies \lnot P(x)$$ 
   (this step may also be done mentally)

3. Prove the contrapositive by a direct proof.
   a. suppose $x$ is a particular but arbitrarily element of $D$ such that $Q(x)$ is false (the hypothesis is true)
   b. Show that $P(x)$ is false (the conclusion is true)

### Use cases
Like before, argument by contraposition also has no direct use cases. However, there are some situations where it might be easier than using direct proofs.
- contraposition CANNOT be used for simple statements with not contrapositive (there must be an implication!), ie "$\sqrt{2}$ is irrational" cannot be proved with contraposition.
- contraposition may be useful if $Q(x)$ is easier to prove than $P(x)$ -- it is easier to work with mathematically. "If the Square of an Integer Is Even, Then the Integer Is Even"
- easier if the negation of the statement is complex

## Relation between Proof by Contradiction and Proof by Contraposition
Contraposition:
Suppose $x \in D$, such that $\lnot Q(x)$ --- steps ---> $\lnot P(x)$
- the conclusion is simply known

Contradiction:
Suppose $\exist x \in D$ such that $P(x) \land \lnot Q(x)$ ---- steps ----> Contradiction: $P(x) \land \lnot P(x)$
- the conclusion from the proof may not be obvious

The steps are quite similar, but the context and goal is different. Don't mix these up! 

## Proof as a Problem Solving Tool
There is no clearcut difference, just think about it :sob:. Just practice doing more proofs fr!!!!!!

## Worksheet
> 1. if $n^3 + 5$ is off, then $n$ is even
>
> Contrapositive $Odd(n) \implies Even(n^3 + 5)$
> assume n is odd
> $$n = 2x + 1$$
> $$n^3 + 5 = (odd) + odd = even$$

>2. if the sum of two real numbers is smaller than 50, then at least one of those numbers is smaller than 25
>
> Contrapositive: none of those numbers is smaller than 25, the sum of two real numbers is larger than 50.
> $$a + b, \,\, a \land b > 25$$
> $$a + b > 25 + 25 = 50$$

> 3. given a positive integer n, if $2^n - 1$ is a prime, then n is also a prime
>
> Contrapositive: $\lnot Prime(n) \implies \lnot Prime(2^n - 1)$$
> assume n is not a prime, so
> $$n = k * m$$
> $$2^{k*m} - 1 = (2^k - 1) (2^{m (k-1)} + 2^{m (k-2)} + ... + 2^m + 1)$$
> since it can be written as a product of two number, it is not prime!


