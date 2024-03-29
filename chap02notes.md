# Chapter 2: Sets, Functions, and Matrices
## Math 275 | Summer 2021
---

## Sets
* A set is an unordered collection of distinct objects.
* A set contains elements.
* $a ∈ A$ means a is an element of A.
* There are multiple methods for describing set:

### Roster Method
* This method lists all the elements of a set using curly brackets.
* $\{a, b, c, d\}$ means a set that has four elements: a, b, c, and d.
* Set that represents vowels of English Vowels: $V = \{a, e, i, o, u\}$
* You can also use ellipses, so that $\{1, 2, ..., 99\}$ is equal to the set of positive integers less than 100.

### Set Builder Notation
* Has all the properties of that set in the brackets
* General Form: $\{x ∣ x \text{ has property } P\}$, means the set of x, so that x has Property P
* Pretty easy to read
* $O=\{x ∈ Z^+ ∣x\text{ is odd and }x<10\}$, means all positive integers that are and are less 10.

#### Common Sets
* $\mathbf{N}$, natural numbers, which are positive integers and 0.
* $\mathbf{Z}$, all integers, plus or minus, makes it set of positive or negative integers
* $\mathbf{Q}$, set of all rational numbers
* $\mathbf{R}$, set of all real numbers
* $\mathbf{C}$, set of all complex numbers

### Interval Notation
* Describing sets with () and [], and their combinations for interval.
* Self explanatory

### Set Equality
* A set is equal to another set iff they have the same elements.
* **Order doesn't matter in a set**, so that $\{3, 4\}$ is the same as $\{4, 3\}$.
* Duplication does not matter in a set, so that $\{3, 3, 4, 4 ,4, 5\}$ equals $\{3, 4, 5\}$.

### Universal Set and Empty Set
* The universal set $U$ is the set containing everything currently under consideration.
* The empty set is a set with no elements, denoted by $\emptyset$, or $\{\}$.
* Note that $\emptyset$ **IS NOT THE SAME** as $\{\emptyset\}$.
* One is the empty set, another is a set that has the empty set.
* From the book:
>The empty set can be thought of as an empty folder and the set consisting of just the empty set can be thought of as a folder with exactly one folder inside, namely, the empty folder.

### Subsets
* Kinda like the name implies, they are sets within sets.
* Set A is a **subset** of set B, iff every element of A is also an element of B.
  * This means B must be at least the same size of A, or bigger.
* The notation $A ⊆ B$ is used to indicate that A is a subset of B
* {1, 2} is a subset of {1, 2, 3}.
  * {1} and {2} are also subsets of both.
* $\emptyset$ is **always** a subset of ANY set.
* A set is always a subset of *itself*.
  *  Basically, $A ⊆ A$ always.

#### Proper Subsets
* If we have two sets A and B, and $A⊆B$,but $A ≠B$ ,then we say A is a proper subset of B.
* Is denoted with $A ⊂ B$

### Power Sets
* The power set is the set of all subsets of a set.
* Denoted by $2^A$ or $P(A)$.
* If $A = \{a,b\}$ then $P(A) = \{ø, \{a\},\{b\},\{a,b\}\}$
* Notice that the power set is NOT the set of each individual element, rather it is the set of all subsets.
  * Basically make sure to have brackets around everything in the power set.

### Set Cardinality and Size of Sets
* If there are exactly n distinct elements in S where n is a nonnegative integer, we say that S is finite. Otherwise it is infinite.
* The cardinality of a finite set A, denoted by |A|, is the number of (distinct) elements of A.
1. $|ø|=0$ Empty set has no elements.
1. $|\{1,2,3\}| = 3$
2. $|\{ø\}| = 1$ Set of empty set has 1 element.
3. $|\{ {1,2,3} \}| = 1$

Notice how that subsets count as one set.

### Cartesian Products

The Cartesian Product of sets A and B (denoted with $A \times B$), represents the set of all ordered pairs (a, b), where $a ∈ A$ and $b ∈ B$.

For example:

What is the Cartesian product of $A = \{1, 2\}$ and $B = \{a, b, c\}$?

$A × B = \{(1,a),(1,b),(1,c),(2,a),(2,b),(2,c)\}$

Note that the Cartesian product is NOT commutative, i.e. A x B does not equal B x A.


## Set Operations
Basically, operations you can do on sets.

### Union
Let A and B be sets. The union of the sets A and B, denoted by $A ∪ B$, is the set that contains those elements that are either in A or in B, or in both.

The union of the sets $\{1,3,5\}$ and $\{1,2,3\}$ is the set $\{1,2,3,5\}$; that is, $\{1,3,5\} ∪ \{1,2,3\} = \{1,2,3,5\}$.

Basically adding all elements in both sets to one set.

### Intersection
Let A and B be sets. The intersection of the sets A and B, denoted by $A ∩ B$, is the set containing those elements in both A and B.

The intersection of the sets $\{1,3,5\}$ and $\{1,2,3\}$ is the set $\{1,3\}$; that is, $\{1,3,5\} ∩ \{1,2,3\} = \{1,3\}$.

Two sets are called disjoint if their intersection is the empty set.

### Difference
The difference of A and B, denoted by $A − B$, is the set containing those elements that are in A but not in B. The difference of A and B is also called the complement of B with respect to A.

Basically, subtract elements that are in B from A.

### Complement
Let U be the universal set. The complement of the set A, denoted by $\bar{A}$, is the complement of A with respect to U. Therefore, the complement of the set A is $U − A$.

## Set Identities
| Identity                                                                       | Name                |
| ------------------------------------------------------------------------------ | ------------------- |
| $A ∩ U = A$<br> $A∪∅=A$                                                        | Identity laws       |
| $A ∪ U = U$<br> $A∩∅=∅$                                                        | Domination laws     |
| $A ∪ A = A$<br> $A∩A=A$                                                        | Idempotent laws     |
| $\overline{(\bar{A})} = A$                                                     | Complementation law |
| $A ∪ B = B ∪ A$<br> $A∩B=B∩A$                                                  | Commutative laws    |
| $A ∪ (B ∪ C) = (A ∪ B) ∪ C$ <br> $A∩(B∩C) = (A∩B)∩C$                           | Associative laws    |
| $A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)$ <br> $A∩(B∪C) = (A∩B)∪(A∩C)$                 | Distributive laws   |
| $\overline{A ∩ B} = \bar{A} ∪ \bar{B}$ <br> $\overline{A∪B}=\bar{A} ∩ \bar{B}$ | De Morgan’s laws    |
| $A ∪ (A ∩ B) = A$ <br> $A∩(A∪B) = A$                                           | Absorption laws     |
| $A ∪ \bar{A} = U$<br> $A∩\bar{A}=∅$                                            | Complement laws     |

Notice how DeMorgan's law is very similar.

## Functions

* Also called mappings and transformations
* For x, there can only be one y. 

### Injective
* Also called one to one.
* Each x points to a different y.

### Surjective
* Means every y, has a corresponding x value.
* $y = x^2$ is NOT surjective, because when $y=-1$, there is no x.
* Also called onto.

### Bijective
* Both injective and surjective
* Also called one-to-one correspondence

### Inverse of Functions
* A function has an inverse, if when you switch x and y, the new equation is also a function.
* Basically, **iff** the original function is a bijection.

### Floor and Ceil
The floor function, denoted $f(x)= ⎣x⎦$ is the largest integer less than or equal to x. The ceiling function, denoted $f(x)= ⎡x⎤$ is the smallest integer greater than or equal to x.

* Basically for floor, look at the ones decimal place for the answer.
  * As it lowers it to that integer.
* For ceil, add 1 to the ones decimal place for answer.
  * As it increases it to that integer.

Example:
* floor(1/2) = floor(0.5), since ones place is 0, answer is 0.
* ceil(1/2) = ceil(.5), since ones place is 0, we add 1 to get 1, for the answer.
* It's pretty self explanatory from the names, themselves. Floor lowers, ceils increases.
* Floor or ceil of that integer is itself.


## Sequences & Summations
* Sequences are ordered lists of elements (usually numbers).
* Summations are when you add all the elements in the sequence.

#### Empty String
From the book:
>Sequences of the form a1, a2, ... , an are often used in computer science. These finite se- quences are also called strings. This string is also denoted by a1a2 ... an... The length of a string is the number of terms in this string. The empty string, denoted by $\lambda$, is the string that has no terms `[think null character in C-strings]`. The empty string has length zero. The string abcd is a string of length four.

### Arithmetic Regression
Arithmetic regression has form:
$$a,a + d,a + 2d,...,a + nd,...$$ 

### Geometric Progression
Geometric progression is a sequence in the form of:
$$a,ar,ar^2,...,ar^n,...$$

Summing these terms gives us a geomettic series:
$\sum_{k=0}^{n}{ar^k} = \dfrac{ar^{n+1} - a}{r-1}, r ≠ 0$


### Recurrence Relation
* A recurrence relation for the sequence $a_n$ is an equation that expresses an in terms of one or more of the previous terms of the sequence.
* Think of the Fibonacci Sequence: $f_n = f_{n−1} + f_{n−2}$.
  * Current element defined by sum of two last elements.
* The initial conditions of a recurrence relation define it. That is a recurrence relation together with its initial conditions determines a unique solution.
* A **closed formula** for a sequence, defines in terms of its initial conditions only, and can give you the term at any n, regardless of whether you know its previous terms.

### Product Notation
* Just like sigma, but you multiply instead of add, and you use big pi, rather than big sigma:
$\prod_{i=a}^{b} f(i)$

### On Cardinality and Countability of Infinite Sets
* The sets A and B have the same cardinality if and only if there is a one-to-one correspondence from A to B.
* The set of positive even integers is countably infinite
* The set of (positive and negative) integers is countably infinite
* The set of positive rational numbers is countably infinite
* The set of real numbers is uncountably infinite.

A set is countably infinite if its elements can be put in one-to-one correspondence with the set of natural numbers, otherwise uncountbaly infinite.

## Matrices
* Rectangular of numbers

### Zero-One Matrix
* A matrix all of whose entries are either 0 or 1 is called a zero–one matrix:

$\begin{bmatrix}
1 & 0 & 1\\
0 & 1 & 0
\end{bmatrix}$

* These 1's and 0's can represent computer bits, and we can treat them as truth values.
  * **1 IS TRUE**
  * **0 IS FALSE**
* Because we are treating them as truth values, we can use the Boolean operations $∧$ (and) and $∨$ (or).
  * $1 ∧ 1 \equiv 1$
  * $1 ∧ 0 \equiv 0$
  * $1 ∨ 1 \equiv 1$
  * etc, basically just T and F, but with 1 and 0
* Using these properties, we can define new operations for zero-one matrices

### Join
* The join of two matrices is defined for two zero-one matrices of equal dimensions.
* The join of two matrices A, B, results in a new matrix with equal dimensions, with the *(i, j)*th entry corresponding to $A_{ij} ∨ B_{ij}$.
* Basically you look at the entry of the same location for two matrices, and you do OR on them.

Example:

$\mathbf{A} = \begin{bmatrix} 1 & 0 & 1\\ 0 & 1 & 0 \end{bmatrix}$
$\mathbf{B} = \begin{bmatrix} 0 & 1 & 0\\ 1 & 1 & 0 \end{bmatrix}$<br>

$\mathbf{A} ∨ \mathbf{B} = \begin{bmatrix} 1∨0 & 0∨1 & 1∨0\\ 0∨1 & 1∨1 & 0∨0 \end{bmatrix} = \begin{bmatrix} 1 & 1 & 1\\ 1 & 1 & 0 \end{bmatrix}$

  
### Meet
* The meet is similar to join except it uses $∧$ (and) instead of $∨$.
* The meet of two matrices is defined for two zero-one matrices of equal dimensions.
* The join of two matrices A, B, results in a new matrix with equal dimensions, with the *(i, j)*th entry corresponding to $A_{ij} ∧ B_{ij}$.
* Basically you look at the entry of the same location for two matrices, and you do AND on them.

Example, same matrices as above, but meet instead of join:

$\mathbf{A} ∧ \mathbf{B} = \begin{bmatrix} 1∧0 & 0∧1 & 1∧0\\ 0∧1 & 1∧1 & 0∧0 \end{bmatrix} = \begin{bmatrix} 0 & 0 & 0\\ 0 & 1 & 0 \end{bmatrix}$

### Boolean Product
* Denoted with: $⊙$
* The boolean product of two zero-one matrices is defined for matrices that you can do regular matrix multiplication with.
  * This means if you take the boolean product of $\mathbf{A} ⊙ \mathbf{B}$, you should be able to do regular matrix multiplication with them.
  * That is number of columns of A should equal number rows of B. (Inner dimensions match)
* You basically do matrix multiplication, but instead of addition you use $∨$, and multiplication you use $∧$.
* Also like matrix multiplication, the boolean product is NOT COMMUTATIVE.

Example:

$\mathbf{A} = \begin{bmatrix} 1 & 0\\ 0 & 1\\ 1 & 0 \end{bmatrix}$ 
$\mathbf{B} = \begin{bmatrix} 1 & 1 & 0\\ 0 & 1 & 1 \end{bmatrix}$<br>

$\mathbf{A} ⊙ \mathbf{B} = \begin{bmatrix}(1∧1)∨(0∧0) & (1∧1)∨(0∧1) & (1∧0)∨(0∧1)\\ (0∧1)∨(1∧0) & (0∧1)∨(1∧1) & (0∧0)∨(1∧1)\\ 1∧1)∨(0∧0) & (1∧1)∨(0∧1) & (1∧0)∨(0∧1)\end{bmatrix} = \begin{bmatrix} 1∨0 & 1∨0 & 0∨0\\ 0∨0 & 0∨1 & 0∨1\\ 1∨0 & 1∨0 & 0∨0\end{bmatrix} =$ 
$$\begin{bmatrix} 1 & 1 & 0\\ 0 & 1 & 1\\ 1 & 1 & 0\end{bmatrix}$$