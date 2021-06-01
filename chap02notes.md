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
| $A ∩ U = A$ $A∪∅=A$ | Identity laws |
|-|-|
| $A ∪ U = U$  $A∩∅=∅$ | Domination laws |
| $A ∪ A = A$ $A∩A=A$ | Idempotent laws |
| $\bar{(\bar{A})} = A$ | Complementation law |
| $A ∪ B = B ∪ A$ $A∩B=B∩A$ | Commutative laws |
| $A ∪ (B ∪ C) = (A ∪ B) ∪ C$ $A∩(B∩C) = (A∩B)∩C$ | Associative laws |
| $A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C)$ $A∩(B∪C) = (A∩B)∪(A∩C)$ | Distributive laws |
| $\bar{A ∩ B} = \bar{A} ∪ \bar{B}$ $\bar{A∪B}=\bar{A} ∩ \bar{B}$ | De Morgan’s laws |
| $A ∪ (A ∩ B) = A$ $A∩(A∪B) = A$ | Absorption laws |
| $A ∪ \bar{A} = U$ $A∩\bar{A}=∅$ | Complement laws |

Notice how DeMorgan's law is very similar.

