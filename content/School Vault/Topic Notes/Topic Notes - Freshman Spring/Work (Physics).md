Tags: #flashcards #notes #MATH112

# 6.4 - Work

### Synopsis
If we apply a constant force $F$ to move an object a distance $d$, then the work done is $W=Fd$. And force is $F=ma$, where $m$ is the mass of the object and $a$ is acceleration

### In-Class Examples (Feb. 9, 2022 - Feb. 11)
1. Constant force
What is the work done in lifting a book of mass 12kg to a height of 0.7m?

force is force of gravity: $F = mg$ (g is the acceleration of gravity, = $9.8m/s^2$)

$F = (12)(9.8) = 117.6N$ (N = newtons, $1N = 1kgm/s^2$)

$W = (117.6)(0.7) = 82J$ (J = joules, $1J = 1N*m = 1kgm^2/s^2$)

2. What if force isn't constant?
Push a box across the ground from a to b with force F(x)
This is a continuous function
Can break up $[a,b]$ into $n$ intervals and approximate the Work on each small interval
$W_{i} = F(x_{i}^{*})\Delta x$
$= \int_{a }^{b}F(x)dx$

3. Hooke's Law
Find work done stretching a spring from 16cm to 21cm fiven thaht it naturally rests at 10cm and takes 30N to hold it at 13cm.

Hooke's Law: F(x) = kx
k is "spring constant" and x is distance past resting state

30N to hold at 13cm aka 3cm past resting state or 0.03m
$30 = F(0.03)$
$30 = k * (0.03)$
$k = 1000$ (k is the spring constant)
$F(x) = 1000 x$ (x is in meters and F is in Newtons)

$W = \int_{0.06}^{0.11}1000xdx$ (stretching from 6cm past resting state to 11cm past resting state)
$= 500x^2 from 0.06 to 0.11$
$= 4.25 J$

4. Gravity
50lb cable 25ft long hanging vertically from the ledge of a building. How much work does it take to lift the cable up to the top of the ledge?
It takes less and less force to pull the remainder of the cable up as the process goes on
Idea: break up into $n$ small pieces (think of links in a chain) of thickness $\Delta x = \frac {25} n ft$ .
The weight of each piece is $\frac {50} n lb$.
In terms of $\Delta x$, each piece weighs $2\Delta x$
To lift the $i$th piece, $W_i = F*d = 2\Delta x * x_i^*$ (pretend its an approx. equals sign)
($x_i^*$ is how far up each "chain" will need to travel)
$W =\sum_{i=1}^n 2\Delta x * x_i^* = \sum_{i=1}^n (2x_i^*)\Delta x$
$W = \int_{0}^{25}2xdx$
$= 25^2 ft*lb$
Ends with a really simple integral, but it's difficult to visualize and flesh out

5. Pump water
Find work needed to pump water out of a full cylindrical tank with given dimensions out of a spout 2m above the tank.
Height of tank 8m
Radius of tank 3m

Idea: cut up into n slices. Taking horizontal slices of water, each point in the slice needs to move up the same distance to the top of the tank. Find the work done on each slice.
Think of the origin in the coordinate plane as the top of the tank going down to the bottom of the tank at $y = 8$
$\Delta y = \frac 8 n$
Force on $i$th slice: $F_i = m*g$ (g is gravity)
Mass (of slice) = density (of water) * volume (of slice in tank) = $1000kg/m^3 * \pi (3)^2 \Delta y$
$F = 1000 \pi (3)^2 \Delta y * 9.8$


6. Pump water out of a sphere
Pumping water out a full spherical tank
Radius of tank 3m
Through a spout above the tank
Spout of 1m above the tank
Break up into small pieces; "That's our main idea of calculus"

Put x=0 at the middle of the tank x increasing as you go up like usual (and not like the other examples)

Make horizontal slices to make circles but need to find the radius of these circles to find volume of each slice

$V = \pi r^2 \Delta y$

Use [[Trigonometry|triangle magic]] to find radius
Base of triangle is y
Height is r
Hypotenuse is radius of the sphere

We put x=0 at the center of the sphere so that the base would be y and the triangle magic would be pretty

$r^2 + y^2 = 3^2$
$r = \sqrt{9-y^2}$
$V = \pi (9-y^2) \Delta y$

$F = mg = pVg = \pi pg (9-y^2) \Delta y$ (p is the density of water $1000 kg/m^3$ and g is gravity $9.8m/s^2$)

Then the water has to travel $4 - y$ to get to the top of the spout

$d = 4 - y$

$W = \pi pg (9-y^2)(4 - y) \Delta y$ (for a slice at y)

$W = \int_{-3}^{3} \pi pg (9-y^2)(4 - y)dy$

7. What if we only pumped out water until the height of the water remaining was 2/3 the original height? (Continuation from last example)
The limits of integration are the only part that would change

$W = \int_{1}^{3} \pi pg (9-y^2)(4 - y)dy$

8. What if tank was only filled to 1/3 its height to begin with, and then we pump all of that water out?
The limits of integration are the only part that would change

$W = \int_{-3}^{-1} \pi pg (9-y^2)(4 - y)dy$



### Detailed Definition
*Theorem 1:*
$$
\displaystyle \int_{-a }^{a}f(x)dx = 2\int_{ 0 }^{a}f(x)dx
$$


---
### Flashcards
- 


### Related Topics
- [[Integration]]