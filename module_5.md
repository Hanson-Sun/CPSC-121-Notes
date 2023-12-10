# Sets and Predicate Logic

## Goals
1. Use truth tables to establish or refute the validity of a rule of inference.
2. Given a rule of inference and propositional logic statements that correspond to the rule's premises, apply the rule to infer a new statement implied by the original statements.
   
3. Determine whether or not a propositional logic proof is valid, and explain why it is valid or invalid.
4. Explore the consequences of a set of propositional logic statements by application of equivalence and inference rules, especially in order to massage statements into a desired form.
5. Devise and attempt multiple different, appropriate strategies for proving a propositional logic statement follows from a list of premises.


## Definitions 

**Predicate**: a sentence that contains a finite number of variables and becomes 
a statement when specific values are substituted for the variables. 
- **domain** of a predicate variable:  the set of **all values** that may be **substituted** in place of the variable.

**Truth Set**: all values in the domain $D$ for a predicate $P(x)$ that makes $P(x)$ true. 
- $\{x \in D | P(x)\}$

**Quantifer**: words that refer to quantities (some, all) -- tells how many elements are true in a predicate.

**Method of Exhaustion**: showing the truth of a predicate by checking all the possibilities in the domain.

**Counterexample**: a value of $x$ that makes $P(x)$ false.

## Predicates and Quantified Statements
Imagine a mathematical statement that expresses a logic relationship with variables. There are a finite amount of variables that can be substituted with specific values to become a logic statement. In general, we can denote a predicate as $P(x)$ where $x \in D$ and $\exists$ some truth set such that $\{x \in D | P(x)\}$.
> **Example**: Let P(x) be the predicate $x^2 > x$ with $D = \R$. Find specific values of $P(x)$\
> $P(1)$ is false because $1^2 = 1$\
> $P(2)$ is true because $2^2 > 2$

## Universal Quantifier $\forall$
Read as "for every", "for each", "for any", "given any", "for all". Quantifies EVERY element in the set. Let $Q(x)$ be a predicate and $D$ the domain of $x$, a universal statement is of the form
$$\forall x \in D, Q(x)$$
It is true **if, and only if** $Q(x)$ is true for each individual $x, x \in D$. Conversely, it is false **if, and only if** $Q(x)$ is false for at least one $x, x\in D$ (counter example).

## Existential Quantifier $\exists$
Read as "there exists". Quantifies that ONE specific element exists in the set. Let $Q(x)$ be a predicate and $D$ the domain of $x$, an existential statement is a statement of the form
$$\exists x \in D, Q(x)$$
It is true **if, and only if**, Q(x) 
is true for **at least one** $x, x\in D$. It is false **if, and only if**, $Q(x)$ is false for all $x, x \in D$.

## Translating between Informal and Formal Language
Helps with understanding or something, just think about it to translate.
> Example 1:

> Example 2:

### Trailing Quantifiers
Rearrange sentence such that the quantifers are at the end of the sentence.

> Example:

## Universal Conditional Statements
Apply conditionals on quantified amounts within a set.
$$\forall x \in S, P(x) \implies Q(x)$$
> More examples i dont want to write

### Vacuously true universal conditional statements
Consider the universal conditional statement
$$\forall x, P(x) \implies Q(x)$$
This statement indicates that $P(x) \implies Q(x)$ is true for ALL values of $x$, even those that make $P(x)$ false. If $P(x)$ (the hypothesis) is false, no matter what $Q(x)$ is, the statement overall is still **vacuously** true.

## Equivalent Forms of Universal and Existential Statements

Consider the conditional statement
$$\forall x \in U, P(x) \implies Q(x)$$
Can be written in the form
$$\forall x \in D, Q(x)$$
where $D \subset U$ such that $\forall x \in D, P(x)$ (D is subset of U such that every value of D makes P(x) true). Conversely, the statement
$$\forall x \in D, Q(x)$$
can be written as
$$\forall x, x\in D \implies Q(x)$$

## Bound Variables and Scope
Imagine scope in programming functions. In a universal statement
$$\forall x \in D, P(x)$$
$x$ is bounded by the quantifier $\forall$ and its scope is confined by when the statement starts and ends (like local params in a function).

## Implicit Quantification
Let $P(x)$ and $Q(x)$ be predicates and suppose the common domain of $x$ is $D$
- The notation $P(x) \implies Q(x)$ means $\forall x, P(x) \implies Q(x)$
  - every element in the truth sat $P(x)$ is in the truth set of $Q(x)$ (imagine subset)
- The notation $P(x) \iff Q(x)$ means $\forall x, P(x) \implies Q(x)$
  - the truth set of $P(x)$ and $Q(x)$ are the same. (imagine same set)

They arent used with $\exist$ because of the vacuous truth makes it really useless!

> Examples: 

## Negations of Quantified Statements

Suppose we have the universal quantifier statement
$$\forall x \in D, Q(x)$$
then we can say the negation of the statement (theres one in D that gives false Q(x))
$$\boxed{\lnot (\forall x \in D, Q(x)) \equiv \exists x \in D, \lnot Q(x)}$$

Similarly, suppose we have the existential quantifier statement 
$$\exists x \in D, Q(x)$$
Then the negation of the statement (all elements in D produce not Q(x)) is
$$\boxed{\exists x \in D, Q(x) \equiv \forall x \in D, \lnot Q(x)}$$

> Examples: dont wanna do them

## Negations of Universal Conditional Statements
Consider the universal conditional statement
$$\forall x \in D, P(x) \implies Q(x)$$
then by definition, we know the negation is
$$\exists x \in D, \lnot (P(x) \implies Q(x)) \equiv \exists x \in D, \lnot (\lnot P(x) \lor Q(x)) $$
Hence we can say, 
$$\boxed{\lnot (\forall x \in D, P(x) \implies Q(x)) \equiv \exists x \in D, P(x) \land  \lnot Q(x)}$$

> Example 1:
>

> Example 2:
>

## Relating $\forall, \exists, \land, \lor$
The negations of quantifying statements seems similar to De Morgan's law. This is not a coincidence, we can generalize quantifying statements with $\land$ and $\lor$.

If $Q(x)$ is a predicate and the domain of $D$ is the set $\{x_0, x_1, ..., x_n\}$, then we can say
$$\boxed{\forall x \in D, Q(x) \equiv Q(x_0) \land Q(x_1) \land Q(x_2)\land ... \land Q(x_n)}$$

Similarly, for the existential quantifier
$$\boxed{\exists x \in D, Q(x) \equiv Q(x_0) \lor Q(x_1) \lor Q(x_2)\lor ... \lor Q(x_n)}$$

## Variations of Universal Conditional Statements

Consider a statement of the form $\forall x \in D, P(x) \implies Q(x)$
1. its **contrapositive** is $\forall x \in D, \lnot Q(x) \implies  \lnot P(x)$
2. its **converse** is $\forall x \in D, Q(x) \implies P(x)$
3. its **inverse** is  $\forall x \in D, \lnot P(x) \implies \lnot Q(x)$
   
The equivalence between the original statement and its variants are the same as those of conditionals. That is, it is **equivalent with its contrapositive**, and **not equivalent** with its **converse and inverse**.

## Necessary and Sufficient Conditions

As with conditional statements, necessary and sufficient conditions can also be extended to universal conditional statements.
- "$\forall x, r(x)$ is a **sufficient** condition for $s(x)$" means "$\forall x, r(x) \implies s(x)$"
- "$\forall x, r(x)$ is a **necessary** condition for $s(x)$" means "$\forall x, \lnot r(x) \implies \lnot s(x)$" or "$\forall x, s(x) \implies r(x)$"
- "$\forall x, r(x)$ only if $s(x)$" means "$\forall x, \lnot s(x) \implies \lnot r(x)$" or "$\forall x, r(x) \implies s(x)$"

> Examples: bro i dont want those

## Statements with Multiple Quantifiers

When a statement contains more than one kind of quantifier, we imagine the actions suggested by the quantifiers as being performed in the **order in which** the quantifiers occur.
$$\forall x \in D, \exists y \in E, P(x, y)$$
- for every $x$ in $D$, there exists a corresponding value $y$ in $E$, such that $P(x, y)$ is true.
- notice how each quantifying statement is chained together

> EXAMPLES: WTF SOBSOBSOBSOB

## Negation of Statements with Multiple Quantifiers
We can find the negation of multiple quantifier statements with the rules to negate single quantifier statements ([Negations of Quantified Statements](#negations-of-quantified-statements)).

Consider the statement $\forall x \in D, \exists y \in E, P(x, y)$, the negation of this statement can be written as
$$\begin{align*}
    \lnot (\forall x \in D, \exists y \in E, P(x, y)) &\equiv  \exists x \in D, \lnot (\exists y \in E, P(x, y)) \\
    & \equiv \exists x \in D, \forall y \in E, \lnot P(x, y). \\
\end{align*}$$
Similarly, for the flipped statements $\exists x \in D, \forall y \in E, P(x, y)$, the negation can be written as 
$$\begin{align*}
    \lnot (\exists x \in D, \forall y \in E, P(x, y)) &\equiv  \forall x \in D, \lnot (\forall y \in E, P(x, y) )\\
    & \equiv \forall x \in D, \exists y \in E, \lnot P(x, y). \\
\end{align*}$$

In summary,
- $\boxed{\lnot (\forall x \in D, \exists y \in E, P(x, y)) \equiv \exists x \in D, \forall y \in E, \lnot P(x, y)}$
- $\boxed{\lnot (\exists x \in D, \forall y \in E, P(x, y)) \equiv \forall x \in D, \exists y \in E, \lnot P(x, y)}$

> examples: bro this is gonna be so long

## Order of Quantifiers
In a statement containing both $\forall$ and $\exists$, **changing the order** of the quantifiers can **significantly change** the meaning of the statement. ORDER MATTERS FOR DIFFERENT QUANTIFIERS.
$$\boxed{\forall x \in D, \exists y \in E, P(x,y) \not \equiv \exists y \in E, \forall x \in D, P(x,y)}$$
> Example:
> $\forall$ person x, $\exists$ a person y that x loves y \
> $\exists$ a person y such that $\forall$ person x, x loves y
>
> those be different u know !!

However, the order does **not** matter for **same** quantifiers.
$$\boxed{\forall x \in D, \forall y \in E, P(x, y) \equiv \forall y \in E, \forall x \in D, P(x, y)}$$
or 
$$\boxed{\exists x \in D, \exists y \in E, P(x, y) \equiv \exists y \in E, \exists x \in D, P(x, y)}$$

> more examples ig:

## Formal Logic Notation
This method writes statements fully symbolically without any random english words. There are two key facts to know about formal logic notation
$$\boxed{\begin{align*}
    \forall x \in D, P(x) &\equiv \forall x (x \in D \implies P(x))\\
    \exists x \in E, P(x) &\equiv \exist x (x \in E \land P(x))
\end{align*}}$$
To understand those representations, its imperative to look at the truth set of $P(x)$ that produces the correct result. Note that the one with $\forall$ considers vacuous truth: if no elements $x \in D$ then the statement is still true. However, if no element $\exists$ in $E$, the whole statement is false. 

> Example: oh no no no no no no i wont do it

# Sets
A collection if definite and separate objects (every element in a set is unique)
  - $A = \{1 ,2 ,3 ,4, 5 \}$ 
  - $A$ is a set and $1,2,3,4,5$ are elements
## Set Membership and Subsets

### $\subseteq$ is used of subsets
  - $A \subseteq B \iff (\forall x, x\in A \implies x \in B)$
  - Negation: $A \not \subseteq B \iff \exist x, x \in A \land x \not \in B$
  - every element in $A$ is in the set $B$, $A$ and $B$ can be the same.

We can also say that all of $B$ is contained in $A$

### $A \sub B$, $A$ a proper subset of $B$
  - $A \subseteq B$ , and
  - there is at least one element in B that is not in A
  - sets A and B are not the same

Similarly, this means all of $B$ is strictly contained in $A$

### $\in$ vs $\subseteq$
- $\in$ acts on elements of a set
  - $x \in A$ if the *element* $x$ is in the *set* $A$

- $\subseteq$ acts on two different sets
  - $A \subseteq B$, if all the elements of $A$ are in the set $B$

## Set operations
- they consume mutliple sets and produce a set as an output

### Union $\cup$
- $A \cup B$, set of all elements in $A$ **or** $B$
- $\forall x, x \in A \lor x \in B$

### Intersection $\cap$
- $A \cap B$, set of all elements in $A$ **and** $B$
- $\forall x, x \in A \land x \in B$

### Difference $-$
- $A - B$, set of all elements in $A$ but **not** in $B$
- $\forall x, x \in A \land \lnot x \in B$

### Complement $c$
- $A^c$, set of all elements in $U$ (everything) that are not in $A$
- this is similar to the negation $\forall x, x \not \in A$

## Important sets in Math
- Integers
  - $\mathbb{Z} = \{\dots -2, -1,0,1,2 \dots\}$

- Positive Integers
  - $\mathbb{Z} ^+ = \{x \in \mathbb{Z}, x > 0\}$

- Non-zero integers
  - $\mathbb{Z}^* = \{x \in \mathbb{Z}, x \not = 0 \}$
- Natural Numbers
    - $\mathbb{N}_0 = \{0, 1, 2, 3 , \dots\}$
    - $\mathbb{N}_1 = \{1, 2, 3, \dots\}$
- Irrational Numbers
   - $\overline{\mathbb{Q}} = \{x \in \mathbb{R}, x \not \in \mathbb{Q}\}$
- Rational numbers
  - $\mathbb{Q} = \{\frac{a}{b} \; | \; a \in \mathbb{Z} \land b \in \mathbb{Z}\}$
- Real numbers
  - $\mathbb{R} = \{\dots\}$
- Empty set
 - $\{ \; \} \text{ or } \emptyset$

- Universal Set: everything!
  - $\mathbb{U}$

- Power set 
  - given a set $A$, the powerset of $A$ is the set of all possible subsets of $A$
  - $\mathbb{P}(\{x,y\}) = \{\emptyset, \{x\}, \{y\}, \{x, y\}\}$
  - $\forall x \in \mathbb{P}(A), x \subseteq A$
  - the powerset of U is all of the possible sets that can exist

## Counting with Quantifiers
### **At least** $n$ items with property $P$:
$$\boxed{\exists x_1 \in D,\exists x_1 \in D,...\exists x_n \in D,P(x_1)\land P(x_2) \land ... \land P(x_n) \land (x_1 \not = x_2) \land ... }$$ 

### **At most** $n$ items with property $P$:
$$\exist x_1 \in D, ..., \exist x_n \in D, \forall y \in D, (x_1 \not = y) \land ... \land (x_n \not = y) \implies P(x) \lor ... \lor P(n) \land \lnot P(y)$$
Alternatively, it can also be:
$$\boxed{\forall x_1 \in D, ..., \forall x_{n+1} \in D, (P(x_1) \land...\land P(x_{n+1})) \implies ((x_1 = x_2) \lor ... \lor (x_{n+1} = ...))}$$
At most means: if there are at most $n$ items, then if $n+1$ items are true, then there must be one repeat.

### **Exactly** $n$ items with property $P$:

At most $n$ **and** at least $n$ 
$$\exist x_1 \in D, ..., \exist x_n \in D, \forall y \in D, (x_1 \not = y) \land ... \land (x_n \not = y) \implies P(x) \land ... \land P(n) \land \lnot P(y) $$



## CONCLUSION
 BRUH BRUH BRUH
# Worksheet





