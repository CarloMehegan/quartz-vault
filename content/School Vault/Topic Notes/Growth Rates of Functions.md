tags: #notes #topic  
creation date: [[2022-11-27 Sunday]] 23:45:07  
description::

## Growth Rates of Functions
We need a measure to compare the efficiency of algorithms, and use the following notations to compare growth rates.

##### Big-O notation
is used to compare the growth rates of two increasing functions. For two functions $f$ and $g$, $f(x) = O(g(x))$ says that $f(x)$ is big-O of $g(x)$, implying that the growth rate of $f(x)$ is **less than or equal to** the growth rate of $g(x)$.

For example, $x^2 + 2x = O(x^2)$

"A polynomial grows at the rate of its highest degree. Lower-order terms can be ignored. Constant factors are absorbed in the constant c in the big-O definition." *from the lecture notes page 24*

##### Common functions by increasing growth rates  
$1, \log n, n, n \log n, n^2, 2^n, n!$  
Rule of thumb: Constant < Polylog < Polynomial < Exponential

For example, more functions in order: $(\log n)^m, n^2 , n^2 \log n, n^3 , n^{\log n} , 2^n , (\log n)^n , n!, n^n , 2^{2^n} \neq 2^{2^{n+1}} = (2^{2^n} )^2$

##### Big-Omega
$f(x) = \Omega (g(x))$ implies that the growth rate of $f(x)$ is **greater than or equal to** the growth rate of $g(x)$.
$f(x) = \Omega (g(x))$ iff $g(x) = O(f(x))$
so basically the opposite?

##### Big-Theta
$f(x) = \Theta (g(x))$ implies that the growth rate of $f(x)$ is **equal to** the growth rate of $g(x)$.
$f(x) = \Theta (g(x))$ iff $f(x) = \Omega (g(x))$ and $f(x) = O(g(x))$

##### Little-o
$f(n) = o(g(n))$ iff for all $c$ there exists a $k$ such that $f(n) < cg(n)$ for $n \geq k$. Alternatively, $\lim_{n \rightarrow \infty} \frac {f(n)} {g(n)} = 0$.

##### Little-omega
$f(n) = \omega(g(n))$ iff for all $c$ there exists a $k$ such that $f(n) > cg(n)$ for $n \geq k$. Alternatively, $\lim_{n \rightarrow \infty} \frac {f(n)} {g(n)} = \infty$.


## References  
Textbook 3.2  
[[CSCI243 lectures.pdf]] Lecture 9, Growth rates of functions pgs 24-25
[[2022-10-19 CSCI243]] big-O  
[[2022-10-21 CSCI243]] big-omega, big-theta  
[[2022-10-24 CSCI243]] little-o, little-omega