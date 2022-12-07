tags: #notes #topic
creation date: [[2022-10-11 Tuesday]] 20:09:25
modification date: [[2022-10-11 Tuesday]] 20:09:25

Table of Contents
- [[#Functions|Functions]]
			- [[#Injective|Injective]]
			- [[#Surjective|Surjective]]
			- [[#Bijective|Bijective]]
			- [[#Common functions|Common functions]]
- [[#References|References]]


## Functions
A function $f : A \rightarrow B$ is a mapping of each element in set $A$ to some element in set $B$.
$A$ is called the **domain** of $f$ and $B$ is called the **codomain** of $f$.

The set $\{f(a)|a \in A\}$ is a subset of $B$ and is called the **range** of $f$.

To generalize to multi-variables, function $f: A_1 \times A_2 \times ... \times A_n \rightarrow B$ is a mapping of each ordered $n$-tuple to some element in $B$.

##### Injective
or, **one-to-one**
A function $f$ is injective iff $f (a) = f (b) \rightarrow a = b, \forall a, b \in A$
This means that there are no cases where different values in $A$ are mapped to the same value $B$.

##### Surjective
or, **onto**
A function $f$ is surjective iff $\forall b \in B \exists a \in A : b = f(a)$
This means that the range of $f$ coincides with its codomain, aka all elements of A map to an element of B.

##### Bijective
A function is bijective when it is both injective and surjective.

##### Common functions
- Ceilings and floors
- Modulo
- Polynomials
- Exponentials
- Logarithms
- Factorials
- Logarithms





## References
Textbook 2.3
[[2022-09-30 CSCI243]] properties of functions
[[2022-10-03 CSCI243]] common computer science functions
[[2022-10-05 CSCI243]] more common functions, starting sequences and sums