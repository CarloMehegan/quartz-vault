tags: #notes #topic
creation date: [[2022-09-19 Monday]] 21:51:08
modification date: [[2022-09-19 Monday]] 21:51:08

## Rules of Inference
Used to simplify/validate [[Argument|Arguments]].
These are relatively simple valid argument forms that can be used as building blocks to construct more complicated valid argument forms.

##### Modus Ponens
The [[Tautology]] $(p \wedge (p \rightarrow q)) \rightarrow q$ is the basis for modus ponens, aka the law of detachment.
Latin for "mode that affirms."

$p$
$p \rightarrow q$
$\_\_\_\_$
$q$

##### Modus Tollens
The tautology $(\neg q \wedge (p \rightarrow q)) \rightarrow \neg p$ is the basis for modus tollens.
"Inverse" of modus ponens

$\neg q$
$p \rightarrow q$
$\_\_\_\_$
$\neg p$

##### Hypothetical Syllogism
example: 
"all ferraris are red"
"all red cars get tickets"
so
"all ferraris get tickets"

$p \rightarrow q$
$q \rightarrow r$
$\_\_\_\_$
$p \rightarrow r$

##### Disjunctive Syllogism
If $p \vee q$ is true, and $p$ is false, then $q$ must be true

$p \vee q$
$\neg p$
$\_\_\_\_$
$q$

##### Addition
If $p$ for sure, then $p \vee$ anything

$p$
$\_\_\_\_$
$p \vee q$

##### Simplification
If $p \wedge q$ is true, then p must be true

$p \wedge q$
$\_\_\_\_$
$p$

##### Conjunction
if $p$ and $q$ are both true separately, can be combined into compound proposition $p \wedge q$

$p$
$q$
$\_\_\_\_$
$p \wedge q$

##### Resolution
In one statement, $p$ or $q$ evaluates to true
In another statement, $\neg p$ or $r$ evaluates to true
Because these statements are both true, either $q$ or $r$ have to be true. 
If $q$ and $r$ were both false, then both statements could not evaluate to true, as $p$ and $\neg p$ cannot both be true at the same.
We can drop $p$ from consideration altogether and combine the statements into $q \vee r$.

$p \vee q$
$\neg p \vee r$
$\_\_\_\_$
$q \vee r$


## Rules of Inference for Quantified Statements
##### Universal Instantiation
$\forall x P(x)$
$\_\_\_\_$
$P(c)$ for any specific number c

##### Universal Generalization
$P(c)$ for an arbitrary number c
$\_\_\_\_$
$\forall x P(x)$

##### Existential Instantiation
$\exists x P(x)$
$\_\_\_\_$
$P(c)$ for some number c

##### Existential Generalization
$P(c)$ for some number c
$\_\_\_\_$
$\exists x P(x)$

##### Universal Modus Ponens
$\forall x (P(x) \rightarrow Q(x))$
$P(a)$, where a is a particular element in the domain
$\_\_\_\_$
$Q(a)$

##### Universal Modus Tollens
$\forall x (P(x) \rightarrow Q(x))$
$\neg Q(a)$, where a is a particular element in the domain
$\_\_\_\_$
$\neg P(a)$



## References
Textbook 1.6
[[2022-09-12 CSCI243]]
