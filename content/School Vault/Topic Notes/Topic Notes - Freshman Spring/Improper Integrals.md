Tags: #flashcards #notes #MATH112
Created: Monday, Mar 28

# Improper Integrals
they look like this

$\int_{a}^{\infty}f(x)dx$,  $\int_{-\infty}^{b}f(x)dx$


---
##### Definition: Improper Integrals of Type I
a. If $\int_{a}^{b}f(x)dx$ exists for every $b \geq a$, then we define 
$$\int_{a}^{\infty}f(x)dx = \lim_{b \to \infty}\int_{a}^{b}f(x)dx$$
provided that this limit exists as a finite number
ex. $\int_{0}^{\infty}sinxdx → DNE$
ex. $\int_{1}^{\infty}\frac 1 {x^2}dx = 1$

b. If $\int_{a}^{b}f(x)dx$ exists for every $a \geq b$, then we define
$$\int_{-\infty}^{b}f(x)dx = \lim_{a \to -\infty}\int_{a}^{b}f(x)dx$$
provided that this limit exists as a finite number

---
##### Definition: Divergent vs. Convergent
The improper integrals $\int_{a}^{\infty}f(x)dx$,  $\int_{-\infty}^{b}f(x)dx$ are called <mark style="background: #ABF7F7A6;">convergent if the limits exist</mark> , and <mark style="background: #ABF7F7A6;">divergent if the limits do not exist</mark> 

$$
\int_{-a}^{a}f(x)dx = 2\int_{ 0 }^{a}f(x)dx
$$

---

##### Definition: $\int^\infty_1 \frac 1 {x^p} dx$
if p > 1, convergent
if p < 1, divergent
if p = 1, divergent
this is why the $\frac 1 {x^2}$ example earlier exists, but $\int^\infty_1 \frac 1 {x} dx$ does not
if p > 1, $\int^\infty_1 \frac 1 {x^p} dx = \frac 1 {p-1}$

---
##### Definition: Bounding functions
If we know $\int^\infty_1 f(x) dx$ converges/diverges and f(x) bounds g(x), we can compare with $\int^\infty_1 g(x) dx$
Bounding here means that the bounded function is between the top function and the x axis

---
##### Definition: Comparison Theorem
Suppose f and g are continuous and that f(x) is greater than or equal to g(x) is greater than or equal to 0 for all x greater than or equal to a.

a. If $\int^\infty_1 f(x) dx$ converges, then $\int^\infty_1 g(x) dx$ also converges.
b. If $\int^\infty_1 g(x) dx$ diverges, then $\int^\infty_1 f(x) dx$ also diverges

b is the contrapositive of a

---
##### Example: Comparison Theorem
$\int^\infty_1 \frac 1 {x^3+1} dx$

we don't know how to find the antideriv. of this to see if it converges or diverges
instead replace $x^3+1$ with just $x^3$. we can find this antideriv and it bounds the original function
we find that the new function converges, so by part a we can say the original function converges as well.

---
##### Definition: Improper Integrals Type II
Discontinuous integrals

ex. $\int^1_0 \frac 1 {\sqrt x} dx$ can't plug in 0 here

im bored of writing

---






### Flashcards
- 


### Related Topics
- 

### Intangibles (to be rewritten)
- 