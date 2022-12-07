Tags: #flashcards #notes #MATH112
Created: Friday, Feb 11

# Subject

### In-class notes (Feb. 11, 2022)
1. 
Recall: if you have n numbers $y_1,y_2,...y_n$, their average is $\frac{y_1,y_2,...y_n}{n}$

What if you have infinitely many numbers?
-> How do meteorologists compute average temperature when the temperature is continuously changing?

Break up the interval into $n$ intervals of width $\Delta x = \frac {b-a}{n}$
Take value $f(x_i^*)$ on each interval, average the values taken one from each interval

$\frac {1} {n} = \frac {\Delta x}  {b-a} = \frac {1} {b-a} \Delta x$

........I started coughing and missed this part......

$\frac 1 {b-a} \int_{a}^{b} f(x)dx$
-> Average value of f(x) on $[a,b]$

2. $f_{avg}$
If f(x) is continuous on $[a,b]$, then $\int_{a}^{b} f(x)dx$ is area under f(x) between a and b, which is equal to area of the rectangle: $f_{avg} (b-a)$  and  $f_{avg} = \frac 1 {b-a} \int_{a}^{b} f(x)dx$
The idea of the rectangle is that the width is the interval a,b, and the area of the function above the rectangle cancel out the empty area within the rectangle. The height of the rectangle has to be $f_{avg}$ for this to happen.

3. Example
Find average value of $f(x) = 1+x^2 on [-1, 2]$

$f_{avg} = \frac 1 {2-(-1)} \int_{-1}^{2} (1+x^2)dx$
$... = 2$

4. MVT
Recall [[Mean Value Theorem]] for derivatives
If f is cont. on $[a,b]$ and f is diff. on $(a,b)$, then there is a c in $(a,b)$ such that
$f'(c) = \frac {f(b)-f(a)} {b-a}$

[[Mean Value Theorem]] for Integrals:
If f is continusoud on $[a,b]$ and there exists a c in $(a,b)$ such that
$f(c) = \frac 1 {b-a} \int_{a}^{b} f(x)dx$







### Detailed Definition
Average value of f(x) on $[a,b]$:

$\frac 1 {b-a} \int_{a}^{b} f(x)dx$



---
### Flashcards
- 


### Related Topics
- 

### Intangibles (to be rewritten)
- 