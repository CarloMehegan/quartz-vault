tags: #notes #topic
creation date: [[2022-09-05 Monday]] 22:03:05
modification date: [[2022-09-05 Monday]] 22:03:05

1.2

## Echelon Form

A rectangular [[Matrix]] is in echelon form is if has the following three properties:
1. All nonzero rows are above any rows of all zeroes. (Zero rows at the bottom)
2. Each leading entry of a row is in a column to the right of the leading entry of the row above it. (Negative diagonal, or "steplike" pattern)
3. All entries in a column below a leading entry are zeroes.

"Property 3 is a simple consequence of Property 2, but we include it for emphasis" (page 14)

Also called Row Echelon Form

A matrix in this form is called an Echelon Matrix.

![[Pasted image 20220905222054.png]]

A method to row reduce a matrix into an echelon matrix is in the [[Row Reduction Algorithm]]. Echelon Form matrices can be further reduced into [[Reduced Echelon Form]] matrices using the Row Reduction Algorithm. Reducing a matrix to these forms is done in order to find the solution set of their corresponding [[Linear System]].

All nonzero matrices can be row reduced into more than one matrix in echelon form using [[Elementary Row Operations]].


## References
Textbook 1.2
[[2022-09-02 MATH211]]