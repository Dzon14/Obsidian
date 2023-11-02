---
tags: [prog]
---
# Matlab
High-level language and interactive environment for scientific computing
- algorithm development
- visualization of results
- data analysis
- numerical computations
- modeling and simulation of engineering problems

## Relevant for NumAna course: [[ODE solvers]]

## Matlab help system
![[Pasted image 20230323152018.png]]

## Scalar functions
![[Pasted image 20230323152400.png]]

## Vectors
are 1 x n or n x 1 matrices (scalars are 1 x 1 matrices).
**Indexing:** 1- first index; end - last index
For ex:
```python
v = [1 2 3]
w = [1; 2; 3;]
t = [1, 2, 3] // ?
```

#### Special vectors
![[Pasted image 20230323152815.png]]

## Matrices
**Entering data:**
```python
A = [1,2,3;4,5,6;7,8,9];
```
Where the first row ends at ;
"whos" gives info about the matrix.

#### Special matrices
![[Pasted image 20230323153102.png]]

#### Matrix operators
![[Pasted image 20230323153150.png]]

#### Matrix functions
![[Pasted image 20230323153215.png]]

#### Submatrix operations
![[Pasted image 20230323154128.png|500]]

## Relational and Logical Operators

**Relational operators:**
![[Pasted image 20230323154240.png|400]]
**Logical operators:**
![[Pasted image 20230323154259.png]]


## Graphics - 3D plots
```python
[X,Y] = meshgrid(-1:0.05:1, -1:0.05:1);
Z = cos(pi*X).*sin(pi*Y);
surf(X,Y,Z)
mesh(X,Y,Z)
```
![[Pasted image 20230323154501.png|450]]

## Conditional control - if, else, switch

#### If
Syntax:
![[Pasted image 20230323154607.png|400]]

**Example:**
![[Pasted image 20230323154632.png|400]]

#### switch
- in case of many possible known values switch statements are easier to read than if statements;
- I not possible for inequality between switch and case values

**Syntax:**
![[Pasted image 20230323154725.png]]
**Example:**
![[Pasted image 20230323154746.png]]

#### Loops
**For:**
for variable = matrix
```python
n = 1;
for i=2:5
n = n*i
end
```
(computation of 5)

**while:**
```python
n=1;  i=2;
while i <= 5
n=n*i; i=i+1;
end
```

- For both loops *continue* can be used to skip remaining states in the body of the loop. 
- *break* can be used to early exit from a loop. In a nested loop, break exists from the inner loop only.

## M-files: Scripts and Functions
- *Scripts* do not accept input arguments or return output arguments: operate on data in the workspace
- *Functions* can accept input arguments and return output arguments: internal variables are local to the function.

#### Functions example
![[Pasted image 20230323155512.png|500]]
- inline(expr) can be used to construct a fucntion from the Matlab expression contained in the string expr. Here input argument is automatically determined and function can be accessed as usual. 
 ![[Pasted image 20230323155833.png|300]]




