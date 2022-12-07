tags: #notes #topic
creation date: [[2022-10-10 Monday]] 19:59:15
modification date: [[2022-10-10 Monday]] 19:59:15

Table of Contents
- [[#Sets|Sets]]
			- [[#Set|Set]]
			- [[#Elements|Elements]]
			- [[#Special sets|Special sets]]
			- [[#Empty sets|Empty sets]]
			- [[#Subsets|Subsets]]
			- [[#Cardinality|Cardinality]]
			- [[#Power Set|Power Set]]
			- [[#Cartesian Product|Cartesian Product]]
			- [[#Quantifiers and Truth Sets|Quantifiers and Truth Sets]]
- [[#Set Operations|Set Operations]]
			- [[#Union|Union]]
			- [[#Intersection|Intersection]]
			- [[#Difference|Difference]]
			- [[#Complement|Complement]]
- [[#Set Identities|Set Identities]]
			- [[#Identity Law|Identity Law]]
			- [[#Domination Law|Domination Law]]
			- [[#Idempotent Law|Idempotent Law]]
			- [[#Complementation Law|Complementation Law]]
			- [[#Absorption Law|Absorption Law]]
			- [[#Complement Law|Complement Law]]
			- [[#Commutative Law|Commutative Law]]
			- [[#Associative Law|Associative Law]]
			- [[#Distributive Law|Distributive Law]]
			- [[#De Morgan's Law|De Morgan's Law]]
			- [[#Membership Table|Membership Table]]
- [[#References|References]]


## Sets

##### Set
A set is an **unordered** collection of elements.
Uppercase letters are used to name sets and lowercase letters to name set elements. For example, $S = \{1, 2, 3\}$, or $A \{x | x$ is an even integer$\}$.


##### Elements
Sets are made up of elements.
The symbol $\in$, or "in," is used to show that an element is in a set.
$x \in Y$ means element $x$ belongs in set $Y$.
Latex command:`\in`


##### Special sets
There are a few special sets of numbers used often
$\mathbb{R}$ - the set of real numbers
$\mathbb{N}$ - the set of natural numbers
$\mathbb{Z}$ - the set of integers
$\mathbb{Q}$ - the set of rational numbers
The superscript $^+$, such as $\mathbb{R}^+$ indicates positive numbers
The superscript $^*$,  such as $\mathbb{R}^*$ indicates the set doesn't include zero
Latex command: `\mathbb{R}`


##### Empty sets
The empty set is a set that contains no elements, denoted by $\emptyset$ or $\{\}$.
Note that $\emptyset \neq \{\emptyset\}$.
Latex command: `\emptyset`


##### Subsets
Set $A$ is a subset of set $B$ if every element of $A$ is also an element of $B$.
The symbol $\subset$ denotes "proper subset"
The symbol $\subseteq$ denotes "subset or equal to"
If $A$ is a subset of $B$, and $B$ is a subset of $A$, then $A = B$.
If $A \subseteq B$, and $A\neq B$, then $A$ is a proper subset of $B$.
![[Pasted image 20220926111757.png]]
These Venn diagrams represent different subset relationships between sets $A$ and $B$.
1. Set $A$ and its elements in $U$, the universal set
2. Set $A$ as a subset of $B$
3. Set $A$ and $B$, not overlapping, not subsets
4. Set $A$ and $B$, overlapping but not subsets
Latex commands: `\subset`, `\subseteq`


##### Cardinality
Sets may be finite or infinite, depending on whether the number of elements it contains is finite or infinite.
The cardinality of a finite set $S$  is the number of elements in the set, and is denoted by $|S|$.
For example, $S = \{a, b\}$, $|S| = 2$.


##### Power Set
For a given set $S$, the power set of $S$ is the set of all subsets of $S$. This is denoted as $P(S)$ and will be equal to $2^{|S|}$.
With every new element, the number of possible subsets doubles.
![[Pasted image 20220928205239.png]]
This graphic uses a tree to visualize the number of subsets and how they are created. Note that **$\emptyset$ is a subset of every set**.


##### Cartesian Product
The Cartesian product of two sets $A$ and $B$ is the set of all **ordered** pairs from $A$ and $B$, denoted as $A \times B$.
For example, $A = \{a, b\}, B = \{1, 2,3\}$
$A \times B$
$= \{(a,b)|a \in A \wedge b \in B\}$
$= \{ (a, 1),  (a, 2),  (a, 3),  (b, 1),  (b, 2),  (b, 3) \}$
Note that $B \times A \neq A \times B$.
$B \times A$
$= \{ (1, a),  (1, b),  (2, a),  (2, b),  (3, a),  (3, b) \}$
Sets are unordered, however, the Cartesian product is the set of all **ordered** pairs of elements. Finite ordered lists of elements such as these pairs are called **tuples**.
Note that $|A \times B| = |A||B|$.
A subset of $A \times B$ is called a **relation** from $A$ to $B$. Functions are special relations.
Latex command: `\times`


##### Quantifiers and Truth Sets
Quantifiers can be used with sets. It can be useful to restrict a quantifier to a particular set. For example, $\forall x \in S(P(x))$, or $\forall x \in S \exists y \in F(P(x,y))$.
The truth set of a predicate $P(x)$ is defined as $\{x \in D |P(x)\}$.


## Set Operations
##### Union
$A \cup B = \{x|x \in A \vee x \in B\}$, $\bigcup^n_{i=1} A_i = A_1 \cup A_2 \cup ... \cup A_n$
"Or"
![[Pasted image 20220928111203.png]]

##### Intersection
$A \cap B = \{x|x \in A \wedge x \in B\}$, $\bigcap^n_{i=1} A_i = A_1 \cap A_2 \cap ... \cap A_n$
"And"
![[Pasted image 20220928111550.png]]

##### Difference
$A - B = \{x|x \in A \wedge x \notin B\}$
and, $|A - B| = |A| - |A \cap B|$
"Subtraction"
![[Pasted image 20220928112156.png]]

##### Complement
With respect to a universal set $U$: 
$\bar A = U - A = \{x|x \notin A\}$
note, represented by $\bar A$
Latex command: `\bar A`
"Inverse"
![[Pasted image 20220928112527.png]]


## Set Identities
Set identities are used to simplift or manipulate an expression that involves sets.
##### Identity Law
$A \cup \emptyset = A, A \cap U = A$

##### Domination Law
$A \cup U = U, A \cap \emptyset = \emptyset$

##### Idempotent Law
$A \cup A = A, A \cap A = A$

##### Complementation Law
$\bar {\bar {A}} = A$

##### Absorption Law
$A \cup (A \cap B) = A, A \cap (A \cup B) = A$
![[Pasted image 20220928113436.png]]

##### Complement Law
$A \cup \bar A = U$
$A \cap \bar A = \emptyset$

##### Commutative Law
$A \cup B = B \cup A$
$A \cap B = B \cap A$

##### Associative Law
$A \cup (B \cup C) = (A \cup B) \cup C)$
$A \cap (B \cap C) = (A \cap B) \cap C)$

##### Distributive Law
$A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
$A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$

##### De Morgan's Law
![[Pasted image 20220928113859.png]]
(Multi-character bars can't be displayed in Mathjax)


##### Membership Table
One way of proving the equality of two set expressions is to use a membership table, similar to a [[Truth Table]].
![[Pasted image 20220928114317.png]]
The table above proves De Morgan's Law of sets.

The preferred way of proving the equality of two set expressions is to use the definition of equal sets and the above set identities.


## References
Textbook 2.1 - Sets and 2.2 - Set Operations
Lecture notes page 15 lecture 6

[[2022-09-23 CSCI243]] finishing proof methods, introducing sets
[[2022-09-26 CSCI243]] cardinality, power set, cartesian product
[[2022-09-28 CSCI243]] relation, set operations, set identities, membership table, trevtutor videos

TrevTutor
- [[2022-09-28 CSCI243#Vid 1 - TrevTutor Intro to Set Theory|Intro to Set Theory]]
- [[2022-09-28 CSCI243#Vid 2 - TrevTutor Cartesian Products and Ordered Pairs|Cartesian Products and Ordered Pairs]]
- [[2022-09-28 CSCI243#Vid 3 - TrevTutor Subsets and Power Sets|Subsets and Power Sets]]