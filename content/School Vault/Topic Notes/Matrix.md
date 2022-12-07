tags: #notes #topic
creation date: [[2022-08-31 Wednesday]] 22:05:57
modification date: [[2022-08-31 Wednesday]] 22:05:57

1.1

## Matrix
[[Linear System|Linear Systems]] can be recorded compactly in an array called a [[Matrix]].

![[Pasted image 20220831220839.png]]

Given a [[Linear System|linear system]], a **coefficient matrix** can be created by aligning the coefficients of each variable by columns.

An augmented matrix is created by adding a column to the end of a coefficient matrix containing the constants from the right side of each equation.

The **size** of the matrix refers to how many rows and columns it has. The coefficient matrix pictured above is called a 3x3 matrix, and the augmented matrix is a 3x4 matrix.

##### Usage
Our goal is to simplify the matrix to have 1 nonzero number in each column representing each variable; this will give us our solution set.
The idea is to transform the matrix into an equivalent system (one with the same solution set) that is easy to solve.
The simplest procedure (for now?) is to transform the matrix into a **triangular matrix**, then isolate the variables from there.

![[Pasted image 20220901213831.png]]

A triangular matrix has leading zeroes following each row as seen above, making the coefficient part of the matrix (not including last column) triangular, not counting the zeroes. This terminology will be "replaced by a precise term in the next section" (pg 6).

In order to transform the given matrix into a triangular one, there are **3 elementary row operations** that can be used.

[[Elementary Row Operations]]
1. Replacement
	Replace one row by the sum of itself and a multiple of another row, or, add to one row a multiple of another row.
	$R_i = R_i + \alpha * R_j, \alpha \neq 0$
2. Interchange
	Interchange two rows.
	$R_i \leftrightarrow R_j$
3. Scalar/Scaling
	Multiply all entries in a row by a nonzero constant.
	$\alpha * R_i, \alpha \neq 0$

These row operations preserve the solution set for the matrix. Two matrices are called **row equivalent** if a sequence of elementary row operations can transform one into the other. These operations are also reversible.

Once the matrix is in triangular form, elementary row operations can continue to be used in order to simplify the matrix and find the solutions.

![[63913CFB-2B6D-47CB-BC2F-D98C078C39B9.jpeg]]

**The goal is a matrix like the one above, with a 1 in each variable column.** The constants column now shows the answers. In this case, $x_1 = 1, x_2 = 0, x_3 = -1$, and the solution set is $(1, 0, -1)$. This answer can be confirmed by plugging the solution into the left side of the original system and confirming that the left and right side are equal.


##### Equality
If the augmented matrices of two [[Linear System|linear systems]] are row equivalent, then the two systems have the same solution set.


##### Using row operations on an augmented matrix to determine the nature of the solution set for a linear system
aka, is the system consistent or inconsistent?, aka, does the system have one existing solution, multiple solutions or no solutions?

In the case of the triangular matrix seen in the second image on this page, we already know $x_3$. We could substitute $x_3 = -1$ into equation 2 and find $x_2$ , and the same with equation 1. So, a solution exists, and the system is consistent. (We can go farther and say since $x_3$ has only one possible value, so does $x_2$ and $x_1$, making the solution unique).

![[729502CA-8E64-4BE4-8993-A46FEE3845F3.jpeg]]

In the case of a triangular matrix like the one above, we find that 0 = 15. This means that there are no values of $x_1, x_2, x_3$ that satisfy this linear system, and the original linear system that comes from these row operations is inconsistent.


## References
[[2022-08-31 MATH211]]
Textbook 1.1 page 4-8
Class notes August 31 (https://blackboard.wm.edu/webapps/blackboard/execute/content/file?cmd=view&content_id=_1966303_1&course_id=_24295_1)