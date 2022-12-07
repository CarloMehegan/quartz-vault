Tags: #flashcards #notes #MATH112

# Volumes
###### Unit 6.2

### Synopsis
- Finding volume of solid obtained by revolving region enclosed by two curves about... x-axis, y-axis, etc.
- Find an formula for the area of a cross section, then [[Integration|Integrate]] using the area of the cross-section (bounds are where the functions intersect)

### Example 1
Volume of solid obtained by revolving region enclosed by $f(x) = \sqrt x$ and $g(x) = \frac 1 3 x$ 

About the x-axis.
- Area of cross-section/"washer": $\pi R(x)^2 - \pi r(x)^2$
- R(x) = the radius of the outer edge of the washer
- r(x) = the radius of the inner edge of the washer
- Integrate using area of cross-section (bounds are 0, 9, where curves intersect)

About the y-axis...
- The difference is instead of integrating with respect to x, integrate with respect to y
Area of cross-section/"washer": $\pi R(y)^2 - \pi r(y)^2$
- To get R(y), or to get f(x) in respect to y, just solve for y
- $3y = x, y^2 = x$
- $V = \int_{0 }^{3} \pi (3y)^2 - \pi (y^2)^2dy$

About the line y =4...
- now it looks like a sideways funnel
- use vertical cross-sections again, now we get bigger washers
- typically, take vertical/horizontal cross-sections depending on what axis you are revolving about; **typically, cross-sections are perpendicular to that axis**
- $R(x) = 4 - \frac 1 3 x$
- $r(x) = 4 - \sqrt x$
- $V = \int_{0 }^{3} \pi (4 - \frac 1 3 x)^2 - \pi (4 - \sqrt x)^2dx$

### Example 2
Find volume of a rectangular pyramid
- cross-section = a right triangle
- fix x, area of slice is $\frac 1 2 bh$
- biggest height is z = 2, biggest base is y = 4, both go down to zero
- height of cross-section triangle = $\frac 2 5 (5 - x) = h$
	- found using the "left face" of the pyramid and trig magic
	- similar triangles in left face $\frac 2 5 = \frac h {5-x}$
- base of cross-section triangle = $\frac 4 5 (5 - x) = b$
	- found using "bottom face" of the pyramid and trig magic
- area of cross-section triangle = half base * height
- integrate



### Detailed Definition
*Theorem 1:*
$$
\displaystyle \int_{0 }^{9}\pi R(x)^2 - \pi r(x)^2 dx
= V
$$
bounds are where the curves intersect

### Flashcards
- 


### Related Topics
- 