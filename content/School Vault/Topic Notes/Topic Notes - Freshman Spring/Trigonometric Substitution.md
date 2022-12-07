Tags: #flashcards #notes #MATH112
Created: Friday, Feb 18

# 7.3 Trigonometric Substitution

### In-Class Notes Friday, Feb 18

We have seen
$\int_0^R \sqrt {R^2-x^2}dx = \frac 1 4 \pi R^2$
We find this by looking at this as a picture, a circle with radius R, and just a fourth of the circle in quadrant 1, compute area with one fourth of the area of a circle
But how do we evaluate this using FTC?

To evaluate $\int \sqrt {R^2-x^2}dx$
Consider the right triangle

angle theta
hypotenuse of R
opp. side of x
adj side of a
$a^2 + x^2 = R^2$
$a = \sqrt {R^2 - x^2}$

Then $sin\theta = \frac x R$
And $cos\theta = \frac {\sqrt {R^2 - x^2}} R$ or $\sqrt {R^2 - x^2} = Rcos\theta$

Want to substitute one of these trig functions into the integral
We'd need to compute in terms of theta then, so we need to first solve for x

$x = Rsin\theta$, $dx = Rcos\theta d\theta$

$\int \sqrt {R^2-x^2}dx = \int (Rcos\theta)(Rcos\theta d\theta)$
					$= R^2 \int cos^2\theta d\theta$
					$= R^2 \int \frac 1 2 (1 + cos2\theta) d\theta$
					$= \frac {R^2} 2 [\theta + \frac 1 2 sin2\theta] + C$
					
$\int \sqrt {R^2-x^2}dx = \frac {R^2} 2 [\theta + \frac 1 2 sin2\theta] + C$
$\int \sqrt {R^2-x^2}dx = \frac {R^2} 2 [sin^{-1}(\frac x R) + \frac 1 2 sin(2sin^{-1}(\frac x R))] + C$
...solve definite integral...bounds 0 to R...
$= \frac 1 4 \pi R^2$
Which we knew before from area but now we know from FTC

---

When will this be useful? When do we use this trig substitution?


Use triangle for Trig Substitution (sometimes called inverse substitution)
a > 0 is a constant (in our example it was R)

For integrals involving
1. $\sqrt{a^2 - x^2}$
TODO: excalidraw? triangle
hyp is a
opp is x
adj is $\sqrt{a^2 - x^2}$

Use $x = asin\theta$
At some point may need circle identity,
$1 - sin^2\theta = cos^2\theta => a^2 - a^2 sin^2\theta = a^2cos^2\theta$
... $=> \sqrt{a^2 - x^2} = acos\theta$

Also works:
hyps is a
opp is
adj is x
a = costheta also works

















### Detailed Definition
*Theorem 1:*
$$
\int_{-a}^{a}f(x)dx = 2\int_{ 0 }^{a}f(x)dx
$$


---
### Flashcards
- 


### Related Topics
- 

### Intangibles (to be rewritten)
- 