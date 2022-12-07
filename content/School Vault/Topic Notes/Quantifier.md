tags: #notes #topic
creation date: [[2022-09-19 Monday]] 19:57:37
modification date: [[2022-09-19 Monday]] 19:57:37

## Quantifier
Quantification expresses the extent to which a [[Predicate]] is true over a range of elements. We will focus on two specific quantifiers.

##### Universal quantifier
The universal quantification of P(x) is the statement
	"P(x) for all values of x in the domain"
The notation $\forall x P(x)$ denotes this universal quantification.

$\forall$ is called the universal quantifier. $\forall x P(x)$ can be read as "for all $xP(x)$."

An element for which P(x) is false is called a counterexample of $\forall x P(x)$.


##### Existential quantifier
The existential quantification of P(x) is the proposition
	"There exists an element x in the domain such that P(x)"
The notation $\exists x P(x)$ denotes this existential quantification

$\exists$ is called the existential quantifier. $\exists x P(x)$ can be read as "There exists an x such that P(x)" or "There is at least one x such that P(x)," or "For some x P(x)."

Without specifying a domain, the statement $\exists x P(x)$ has no meaning.


##### Precedence
Quantifiers have higher precedence than all logical operators from propositional calculus.


##### Logical Equivalences Involving Quantifiers
Distribution
$\forall (P(x) \wedge Q(x)) \equiv \forall x P(x) \wedge \forall x Q(x)$

De Morgan's Law with Quantifiers
$\neg \forall x P(x) \equiv \exists x \neg P (x)$
$\neg \exists x Q(x) \equiv \forall x \neg Q(x)$

In a sequence of quantifiers, apply De Morgan's law from outside to inside
$\neg \forall x \forall y P(x,y)$
$\equiv \exists x \neg(\forall y P(x,y))$
$\equiv \exists x \exists y \neg P (x, y)$


##### Nested Quantifiers
think of nested quantifiers as loops
see page 58 of textbook


## References
textbook pg 58

[[2022-09-09 CSCI243]] logical laws, predicates, and quantifiers
see fleeting note for more examples