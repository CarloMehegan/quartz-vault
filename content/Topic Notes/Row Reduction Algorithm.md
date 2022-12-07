tags: #notes #topic
creation date: [[2022-09-05 Monday]] 22:38:08
modification date: [[2022-09-05 Monday]] 22:38:08

## Row Reduction Algorithm

The Row Reduction Algorithm consists of four steps used to produce a [[Matrix]] in [[Echelon Form]]. A fifth step produces a matrix in [[Reduced Echelon Form]].

1. Begin with the leftmost nonzero column. This is a [[Pivot Position|pivot column]]. The [[Pivot Position|pivot position]] is at the top.
2. Select a nonzero entry in the pivot column as a pivot. [[Elementary Row Operations|Interchange]] rows if necessary to move this entry into the pivot position.
3. Use [[Elementary Row Operations|replacement operations]] to create zeroes in all positions below the pivot.
4. Ignore the row containing the pivot position and all rows, if any, above it. Apply steps 1-3 to the submatrix that remains. Repeat the process until there are no more nonzero rows to modify.

These steps, called the **forward phase**, give us a matrix in echelon form.

5. Beginning with the rightmost pivot and working upward and to the left, create zeroes above each pivot. If a pivot is not 1, make it 1 by a scaling operation.

This final step, called the **backward phase**, leaves us with a matrix in reduced echelon form.

The purpose of the algorithm is to assist in finding the solution set of a [[Linear System]].
The row reduction algorithm leads directly to an explicit description of the solution of a linear system when the algorithm is applied to the augmented matrix of the system.

![[Pasted image 20220905231218.png]]
If this is the a linear system that has been changed into the equivalent reduced echelon form,

![[Pasted image 20220905231257.png]]
This is the associated system of equations.

![[Pasted image 20220905231359.png]]
This is what the solution set of the linear system looks like. We can see here that $x_3$ is a [[Free Variable]] and that $x_1, x_2$ are [[Basic Variable|Basic Variables]]. Each choice of $x_3$ determines a (different) solution of the system, and every solution of the system is determined by a choice of $x_3$.
This format for a solution set is called [[Parametric Description]].

## References
Textbook 1.2
[[2022-09-02 MATH211]]