tags: #notes #topic
creation date: [[2022-09-19 Monday]] 22:39:35
modification date: [[2022-09-19 Monday]] 22:39:35

## Proof Methods
A **proof** is a sequence of statements, where each statement is given a condition or conclusion obtained by previous statements by some [[Rules of Inference]].

##### Difference between an [[Argument]] and a Proof
![[Pasted image 20220922231642.png]]

Both arguments and proofs involve introducing evidence and applying logic to determine the truth of a premise. But they have a number of important differences:

Arguments are defined as “a reason or set of reasons given with the aim of persuading others that an action or idea is right or wrong;” while proofs are defined as “evidence or argument establishing or helping to establish a fact or the truth of a statement.” [Quora](https://www.quora.com/Whats-the-difference-between-an-argument-and-proof)

The following are different methods of proof

##### Direct Proof
To prove "if $p$ then $q$," assume that $p$ is true and show that $q$ is true.

##### Proof by Contraposition
To prove "if $p$ then $q$," assume $q$ is false and show that $p$ is false.

This method is based on the tautology $p \rightarrow q \equiv \neg q \rightarrow \neg p$.

##### Proof by Contradiction
To prove $p$, assume $p$ is false and show there is $r$ such that $r$ is true and $\neg r$ is true, a contradiction

Or according to the textbook
Assume both $p$ and $\neg q$ are true and show a contradiction
Idk man 

Or the internet
Assume p is false

Or
Assume q is false

- [ ] i gotta figure this out

##### Proof by Cases
When we are unable to prove a theorem with a single argument that holds for all possible cases, we may need to construct our proof for each of the possible cases, one by one.

This method relies on the rule of inference:
$(p_1 \vee p_2 \vee ... \vee p_n) \rightarrow q$
$\equiv (p_1 \rightarrow q) \wedge (p_2 \rightarrow q) \wedge ... \wedge (p_n \rightarrow q)$

##### Existence Proof
To prove there exists an object of a certain type, we can simply construct one. This is the **constructive existence proof**.

It is also possible to give a **nonconstructive existence proof**. Sometimes a nonconstructive existence proof uses proof by contradiction.

##### Proof by Induction
To prove that $P(n)$ is true for all $n \geq 1$, prove that
1. P(1) is true, and
2. $\forall k (P(k) \rightarrow P(k+1))$ is true.

We can split induction into 2 steps: the base case and the inductive step. We can also split the inductive step into 2 steps in order to understand exactly what we need to show for it.
1. The base case
   Proving $P(1)$
2. The inductive hypothesis (IH)
   What we assume
3. The inductive step (IS)
   Showing how we go from $n$ to $n+1$
   

## References
Textbook 1.7
[[2022-09-14 CSCI243]] direct proof, proof by contraposition
[[2022-09-16 CSCI243]] proof by contraposition, by contradiction, by cases
[[2022-09-19 CSCI243]] proof by cases, by existence, by induction
[[2022-09-21 CSCI243]] more induction examples (trominoes)
[[2022-09-23 CSCI243]] last induction example (hats)

For examples, see HW #2,
[[CSCI243 HW2.pdf]]
or the textbook,
or pages 10 through 13 in the lecture notes (lecture 4 and 5)