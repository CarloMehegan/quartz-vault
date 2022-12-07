tags: #notes #topic
creation date: [[2022-10-11 Tuesday]] 20:47:17
modification date: [[2022-10-11 Tuesday]] 20:47:17

## Summations
A summation is a sum of some terms. We use the Greek letter sigma, $\sum$.
Latex command: `\sum`

The sequence $a_m + a_{m+1} + ... + a_n$ can be written as $\sum^n_{j=m} a_j$.
Latex command: `\sum^n_{j=m} a_j`

##### Limits
$\sum ^{\infty} _{i=1} a_i = lim_{n \rightarrow \infty} \sum ^n _{i=1} a_i$

##### Law of Linearity
$\sum^n_{i=1} (ax_i + by_i) = a \sum^n_{i=1} x_i + b \sum^n_{i=1} y_i$
this law shows how factors can be taken outside of a sum and how elements added together within a sum can be split into two sums added together.

##### Double Summation
$\sum^n_{i=1} \sum^m_{j=1} (2i + 3^j)$
Think of double sums as two nested for loops.
Factors that do not depend on the summation index can be factored out.
$\sum^n_{i=1} \sum^m_{j=1} a_i b_j = \sum^n_{i=1} a_i \sum^m_{j=1} b_j$
These sums can be switched as long as the inner loop variable doesn't depend on the outer loop.
$\sum^n_{i=1} \sum^m_{j=1} a_{ij} = \sum^m_{j=1} \sum^n_{i=1} a_{ij}$

##### Useful Arithmetic Series
$x_i = a + id$

$\sum^n_{k=1} k = \frac 1 2 n(n+1)$

$\sum^n_{k=1} kd = \frac 1 2 d n(n+1)$

$\sum^n_{k=1} (a+kd) = \frac 1 2 (n+1)(2a + nd)$

##### Useful Geometric Series
$x^i = ar^i$

$\sum^n_{i=0} r^i = \frac {r^{n+1}-1}{r-1}$
(when $r = 1$, sums to $n+1$)

##### Sum of Squares
$\sum^n_{j=1} j^2 = \frac 1 6 n (n+1) (2n+1)$

##### Sum of Cubes
$\sum^n_{j=1} j^3 = \frac 1 4 n^2 (n+1)^2$

##### Differentiating Series
$\sum ^{\infty} _{k=0} kx^{k-1} = \frac 1 {(1-x)^2}$
for $|x| < 1$.

##### Harmonic Series
$\sum^n_{i=1} \frac 1 i$
The $n$th harmonic number of the harmonic series:
$H_n = \sum^n_{i=1} \frac 1 i < ln n +1$

##### Telescoping Series
For any sequence $a_0, a_1, ... , a_n$, $\sum^n_{k=1} (a_k - a_{k-1}) = a_n = a_0$.
For example, using telescoping, we can show that $\sum^{n-1}_{k=1} \frac 1 {k(k+1)} = 1 - \frac 1 n$.
Proofs are left as an exercise for the dipshit


## References
Textbook 2.4
[[2022-10-07 CSCI243]] summations
[[2022-10-10 CSCI243]] useful summations