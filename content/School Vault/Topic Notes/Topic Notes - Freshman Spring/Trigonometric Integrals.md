Tags: \#flashcards/calc2 #notes #MATH112
Created: Wednesday, Feb 16
(disabled flashcard tag)
# 7.2 Trigonometric Integrals

### In-class notes Wednesday, Feb 16
Trig Identity
$sin^2x + cos^2x = 1$

ex.
$cos^3x = cos^2x * cosx$
$cos^3x = (1-sin^2x) cosx$
$\int cos^3xdx = \int (1-sin^2x) cosxdx$
u = sinx
du = cosxdx
$\int cos^3xdx = \int (1-u^2) du$
$\int cos^3xdx = u - \frac 1 3 u^3 + C$
$\int cos^3xdx = sinx - \frac 1 3 sin^3x + C$

ex 2 i wont write it all out but its $\int sin^7x cos^5xdx$
u substitution is like figuring out how to remove the du from the equation in this situation its cosx so you are working only in terms of u which is sinx here

This technique works well when the power on sinx or cosx is odd
Take the one with the odd power, take off one power, use that as du, use trig identity for the leftover even power to get in terms of the other function

What if powers on sinx and cosx are both even?
First use double-angle identities!

Double angle identities
$cos^2x = \frac {1 + cos2x} 2$
$sin^2x = \frac {1-cos2x} 2$

So,
$\int cos^2xdx = \int \frac {1 + cos2x} 2 dx$
$\int cos^2xdx = \frac 1 2 \int (1 + cos2x)dx$
Do u = 2x du = 2 u substitution
Or just know that the antiderivative would be $\frac 1 2 sin2x$ for cos2x
$\int cos^2xdx = \frac 1 2 (x + \frac 1 2 sin2x) + C$

Next example $\int cos^2x sin^2xdx$
Use the double angle identities on both take out a 1/4 it's like a difference of squares $cos^22x = \frac {1+cos4x} 2$ whateverrr I got lost


More circle identities
Take $sin^2x + cos^2x = 1$ and divide everything by $cos^2x$
Becomes
$tan^2x + 1 = sec^2x$
Divide by $sin^2x$ and it becomes
$1 + cot^2x = csc^2x$

Can't remember trig derivatives? Remember quotient rule to find them
derivative of tan = sec squared
derivative of sec = sectan

ex $\int tan^6xsec^4xdx$
want to set 
$u = tanx$
$du = sec^2xdx$
Use the circle identity to replace one of the sec^2x with tan^2x + 1
Etc not gonna write it all do u sub and stuff

u=tanx substitution works well when power on secx is even


### In-class notes Friday, Feb 18

To integrate $\int tan^mxsec^nxdx$
If m is even, use $u = tanx, du = sec^2xdx$
and circle identity $tan^2x + 1 = sec^2x$

If n is odd, use $u = secx, du = secxtanxdx$
and circle identity $tan^2x = sec^2x - 1$

If m is odd and n is even, the solution is more ambiguous
Typically need to do integration by parts at some point




Recall: $\int tanxdx = ln(|secx|) + C$
What is $\int secxdx$?
u = secx + tanx
du = $(secxtanx + sec^2x) dx = secx (tanx+secx)dx$
$\frac 1 {secx + tanx}du = secxdx$
so, $\int secxdx = \int \frac 1 u du$
$= ln(|u|) + C$
Now we know: $\int secxdx = ln(|secx + tanx|) + C$

ex.
$\int sec^3xdx$
[[Integration by Parts#^15d17c|by parts]]: $u = secx, dv = sec^2xdx$
	 	$du = secxtanxdx, v = tanx$

$\int sec^3xdx = secxtanx - \int secxtan^2xdx$
...
$\int sec^3xdx = secxtanx - \int sec^3xdx + \int secx dx$
$2\int sec^3xdx = secxtanx + \int secx dx$
$2\int sec^3xdx = secxtanx + ln(|secx+tanx|)+ C$




Same ideas as before for these trig function
$\int cot^mxcsc^nxdx$
...
$[cotx]' = -csc^2x$
$[cscx]' = -cotxcscx$





### In-class Notes Monday, Feb 21

Let a > 0 be constant
Use right triangle with sides a and x
For integrals involving

1. $\sqrt {a^2 - x^2}$

hyp is a
opp is x
adj is 1. (as in the thing labelled 1 above)

2. $\sqrt {a^2 + x^2}$

hyp is 2.
opp is x
adj is a

3. $\sqrt {x^2 - a^2}$

hyp is x
opp is 3.
adj is a

1. Substitution to make for $\sqrt {a^2 - x^2}$
Use $x = a sin(\theta)$
$cos^2\theta = 1 - sin^2\theta$
$a^2 - a^2sin^2\theta =a^2cos^2 \theta$
$= acos\theta$

2. Substitution to make for $\sqrt {a^2 + x^2}$
...
$= atan\theta$

3. Substitution to make for $\sqrt {x^2 - a^2}$
$= asec\theta$

Don't need to memorize these just set up a triangle to get these expressions to show up


Example 1
$\int \frac {dx} {\sqrt {x^2 + 9}}$
sidenote this is the same as
$\int \frac {1} {\sqrt {x^2 + 9}}dx$

sum of squares on the bottom $x^2 + 3^2$
make a triangle
I have to stop writing this out in obsidian its too tedious this sucks

triangle:
hyp is $\sqrt{x^2 + 9}$
adj is 3
opp is x

want to use substitution 
$tan\theta = \frac x 3$ or  $x = 3tan\theta$
and $dx = 3sec^2 \theta d\theta$

now in terms of theta it looks like

$\int \frac {1} {\sqrt {(3tan\theta)^2 + 9}}3sec^2 \theta d\theta$
simplify...
$\int \frac {3sec^2 \theta} {(3sec\theta)} d\theta$
$\int sec\theta d \theta$
$= ln(|sec\theta| + tan\theta) + C$ (we found this last class)

We can use the triangle to simplify by substituting sec and tan

$= ln(|\frac {\sqrt {x^2 + 9} } 3 + \frac x 3|) + C$


Example 2








---

### Detailed Definitions
Trig (circle) identity
$sin^2x + cos^2x = 1$

Double angle identities
$cos^2x = \frac {1 + cos2x} 2$
$sin^2x = \frac {1-cos2x} 2$

Don't need to memorize double angle identities, but do need to know circle identity


---

### Flashcards
- Trig (circle) identity :: $sin^2x + cos^2x = 1$
<!--SR:!2022-09-01,1,230-->


### Related Topics
- Next: [[Trigonometric Substitution]]

### Intangibles (to be rewritten)
- 