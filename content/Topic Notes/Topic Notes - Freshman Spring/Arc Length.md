Tags: #flashcards #notes #MATH112
Created: Monday, Mar 21

# 9.1 Arc Length
In-class notes done on paper

### Synopsis
Goal: compute the distance travelled along a curve, from a to b

Think of the curve as small line segments to piece together
First, approximate short distances along the curve with straight lines. Break up $[a,b]$ into n intervals of width $\Delta x$. For each of these points, connect with a straight line
Think of these straight lines as the hypotenuses of triangles
Using triangle magic, arc length L is
$$
L \approx \sum_{i=1}^{n} \sqrt {1 + (\frac {\Delta y} {\Delta x})^2 } \Delta x
$$
or,
$$
L = \int_{a}^{b} \sqrt {1 + (\frac {dy} {dx})^2 } d x
$$
aka
$$
L = \int_{a}^{b} \sqrt {1 + f'(x)^2 } d x
$$
so yeah just plug that in do some calculus and simplify it


---
### Flashcards
- 


### Related Topics
- 

### Intangibles (to be rewritten)
- 