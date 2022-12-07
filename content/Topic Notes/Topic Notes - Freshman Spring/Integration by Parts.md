Tags: #flashcards #notes #MATH112
Created: Monday, Feb 14

# 7.1 Integration by Parts

### In-Class Notes Monday, Feb 14

Problem: how to integrate $\int f(x)g(x)dx$?
Does not equal $\int f(x)dx * \int g(x)dx$

Recall product rule for derivatives
$[f(x)g(x)]' = f'(x)g(x) + f(x)g'(x)$
Integration by parts is taking this idea, but backwards

Integrate both sides
$\int [f(x)g(x)]dx' = \int [f'(x)g(x) + f(x)g'(x)]dx$
FTC
$f(x)g(x) = \int [f'(x)g(x)dx + f(x)g'(x)]$
Simplify
$\int f'(x)g(x)dx = f(x)g(x) - \int f(x)g'(x)dx$

Set u = f(x) and v = g(x), du = f'(x)dx, dv = g'(x)dx
$\int vdu = uv - \int udv$
OR
$\int udv = uv - \int vdu$
Looking for this pattern
dv: a function we know how to integrate
u: a function we know how to differentiate ^15d17c


1. Ex. $\int xsin(x)dx$
Pick a function u and a function dv
Then differentiate to find du and integrate to find v
u = x
dv = sinxdx
then
du = dx
v = -cosx

$\int udv = uv - \int vdu$
$\int xsinxdx = x(-cosx) - \int (-cosx)dx$
Is this easier to evaluate?
Yes it's easier to integrate -cos than xsin
$\int xsinxdx = -x(cosx) + \int (cosx)dx$
$\int xsinxdx = -x(cosx) + sinx + C$
don't forget C

What if we chose u = sinx?
dv = xdx
du = cosxdx
v = $\frac 1 2 x^2$
$\int xsinxdx = \frac 1 2 x^2sinx - \int \frac 1 2 x^2(-cosx)dx$
This isn't wrong, but it's more difficult than the other way
At this point when you realize it's more complicated, just try the other function as u

2. Ex. $\int x^2 ln(x)dx$
u = ln(x) because we don't know how to integrate ln(x)
dv = $x^2dx$
du = $\frac 1 x$
v = $\frac 1 3 x^3$

$= \frac 1 3 x^3 ln(x) - \int \frac 1 3 x^3 (\frac 1 x)dx$
$= \frac 1 3 x^3 ln(x) - \frac 1 3 \int x^2 dx$
$= \frac 1 3 x^3 ln(x) - \frac 1 3 (\frac 1 3 x^3) + C$

3. What is $\int ln(x)dx$ anyways?
Use integration by parts to calculate
u = ln(x)
dv = dx
du = $\frac 1 x dx$
v = x

$= x *ln(x) - \int x \frac 1 x dx$
$= x ln(x) - x + C$

The integral of ln(x) =
$\int ln(x)dx = xln(x) - x + C$

4. $\int tan^{-1}(x)dx$
u = $tan^{-1}(x)$
dv = dx
du = $\frac 1 {x^2 + 1}dx$
v = x
$= xtan^{-1}(x) - \int \frac x {x^2 + 1}dx$

u-substitution
u = $x^2 + 1$
du = $2xdx$
$= xtan^{-1}(x) - \frac 1 2 \int \frac 1 u du$
$= xtan^{-1}(x) - \frac 1 2 ln(|u|) + C$
$= xtan^{-1}(x) - \frac 1 2 ln(x^2 + 1) + C$

5. Integration by parts for definite integrals:
$\int_a^b f'(x)g(x)dx = f(x)g(x)|_a^b - \int_a^b f(x)g'(x)dx$

6. $\int_0^1 tan^{-1}(x)dx$
$= xtan^{-1}(x)|_0^1 - \int_0^1 \frac x {x^2 + 1}dx$
...
$= \frac \pi 4 - ln(2)$

7. $\int e^x sin(x) dx$
sidenote how do we know this will be good for integration by parts?
-> two very different types of functions being multiplied together

u = e^x
dv = sin(x)dx
du = e^xdx
v = -cos(x)

$=-e^xcosx + \int e^x cosxdx$
it's still complicated, but the other way will also be complicated
-> do integration by parts again!

u = e^x
dv = cosxdx
du = e^xdx
v = sinx

$= -e^x cosx + e^x sinx - \int e^xsinxdx$
still difficult!
now there's a minus sign, we can try to bring terms to the other side (minus sign is important bc otherwise they'd cancel out)

$2\int e^x sinxdx = -e^x cosx + e^x sinx + C$
final solution
$\int e^x sinxdx = \frac 1 2 [-e^x cosx + e^x sinx] + C$


---


### In class notes Wednesday, Feb 16
With integration by parts, how to decide what u should be?
General heuristic: pick u in the following order
1. Logarithmic ($ln(x), log_3(x)$)
2. Inverse Trig ($tan^{-1}, sin^{-1}$)
3. Algebraic ($x^2, \sqrt x, 3x+5$)
4. Trig ($sin(x), cos(x), tan(x)$)
5. Exponential ($e^x, 2^x$)
aka, LIATE

##### Examples
1. LIATE doesn't always work

$\int x^3 e^{x^2}dx$
By LIATE, would set u to $x^3$
$du = 3x^2dx$
Still complicated
However
set $u = x^2$ (weird bc it's only part of the function)
$du = 2xdx$
$dv = x e^{x^2}dx$
$v = \frac 1 2 e^{x^2}$
turn the integral into $\frac 1 2 \int 2x^3 e^{x^2}dx$
...$\frac 1 2 \int ue^{u}du$
Do by parts from here

2. Using LIATE I'm not gonna write it all out
Remember the formula
$\int_a^b f'(x)g(x)dx = f(x)g(x)|_a^b - \int_a^b f(x)g'(x)dx$
Don't forget!!
Final example of 7.1 onto next section



---

### Detailed Definitions
*Integration by Parts for indefinite integrals:*

$\int f'(x)g(x)dx = f(x)g(x)- \int f(x)g'(x)dx$
Set u = f(x) and v = g(x), du = f'(x)dx, dv = g'(x)dx
$\int vdu = uv - \int udv$
OR
$\int udv = uv - \int vdu$
Looking for this pattern
dv: a function we know how to integrate
u: a function we know how to differentiate


*Integration by Parts for definite integrals:*

$\int_a^b f'(x)g(x)dx = f(x)g(x)|_a^b - \int_a^b f(x)g'(x)dx$
Set u = f(x) and v = g(x), du = f'(x)dx, dv = g'(x)dx
$\int_a^b vdu = uv|_a^b - \int_a^b udv$
OR
$\int_a^b udv = uv|_a^b - \int_a^b vdu$


---
### Flashcards
- 


### Related Topics
- Next: 7.2 [[Trigonometric Integrals]]

### Intangibles (to be rewritten)
- 