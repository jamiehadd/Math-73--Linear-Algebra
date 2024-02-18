
## Inner and outer products
The alternate view of producing linear combinations is the dot product. 
If we imagine for example
$$
a = \begin{pmatrix}
1 & 2  \\
0 & 7  \\
1 & 3
\end{pmatrix} \text{ and }  b = \begin{pmatrix}
-1 & 5 & 2 & -2 \\
2 & -2 & 0 & -3
\end{pmatrix}
$$ Compute AB!
we take the dot product between $(1,2)$ and $(-1,2)$ or $(5,-2)$, etc.
To compute the $i,j^{th}$  entry of a product, you need the $i$th entry of A and the $j$th entry of B. 

The 3,4 entry is done by taking the dot product between the the third row of a and the 4th column of B.  The output of $ab$ is a $3\times 4$ matrix. a is a $3\times 2$ matrix and b is a $2 \times 4$ matrix. We are able to multiply them because $2=2$. In general, we can only multiply an $M\times N \text{ and }  N \times R$  matrix if $M=J$, and the output will be a $N\times K$ matrix. The dot product is the inner representation of matrix multiplication. We will later get into the difference between the #inner_product and the #outer_product view of matrix multiplication. 

The outer product takes the left matrix as scalar multiples of each entry at the top of the right matrix, then down etc, + a new matrix for the second left of the matrix as scaler multiples, and so on. This explanation is bad, but just look at the numbers and you'll understand. 

copying the AB again for easy reference:
$$
a = \begin{pmatrix}
1 & 2  \\
0 & 7  \\
1 & 3
\end{pmatrix} \text{ and }  b = \begin{pmatrix}
-1 & 5 & 2 & -2 \\
2 & -2 & 0 & -3
\end{pmatrix}
$$
using the AB before, we can write as
$$
\begin{pmatrix}
-1 & 5 & 2 & -2 \\
0 & 0 & 0 & 0 \\
-1 & 5 & 2 & -2
\end{pmatrix} + \begin{pmatrix}
4 & -4 & 0 & -6 \\
14 & -14  & 0 & 21 \\
6 & -6 & 0 & -9
\end{pmatrix} \xleftarrow {\text{ Outer product expansion }}
$$
The way we multiply is by taking columns of A and rows of B
$$
\sum_{i=1}^{n}\vec{a}_{i}\vec{b}_{i}
$$ 
## Transpose
Taking a matrix $A$
$$
\begin{align}
(A^{t})^{t}&\mapsto A \\
(kA)^{t} &\mapsto k(A^{t})  \\
(A+B)^{t} &\mapsto A^{t}+B^{t} \\
(AB)^{t} &\mapsto B^{t}A^{t}  \\
\text{ this next one only exists if A is a } &\square_{\text{ square }} \text{ matrix, as a time a must have similar dimenisions } \\


(a^{r})^{t}&\mapsto (A^{t})^{r}
\end{align}
$$

A matrix $A$ is symmetric if $A^{t} \mapsto A$ (if when it is transposed the matrix outputs the same thing). This means that $A\text{ is } \square \text{ and } A$ is symmetric about the diagonal.

If $A$ is square, then $A+A^{t}$ is symmetric. For any matrix $A$, both $AA^{T}$ and $A^{T}A$ are symmetric. 

We can prove properties of these operations in common now that we have basic rules.
$$\text{ Properties of matrix addition and scalar multiplication }
\begin{align}
A+B&=B+A \\
(A+B)+C&=A+(B+C) \\
A+0&=A \\
A+(-A) &= 0 \\
c(A+B)&=cA+cB \\
(c+d)A&=cA+dA \\
c(dA)&=(cd)A \\
1A&=A
\end{align}
$$
$$
\text{ Properties of matrix multiplication   }
\begin{align}
A(BC)&=(AB)C \\
A(B+C)&=AB+AC \\
(A+B)C&=(AC+BC) \\
k(AB)&=(kA)B=A(KB) \\
I_{m}A&=A=AI_{n} \text{ if A is }M\times N
\end{align}
$$

Practice
$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
=\begin{bmatrix}
1 & 2 \\
3 & 4
\end{bmatrix}
$$
The identity matrixes preserve others during multiplications. 
## Matrix algebra
many of the same operations and objects generalize from vectors to matrices!

Def: if $A_{1},A_{2}\dots A_{k}$ are matrices of the same size and $c_{1},c_{2}\dots,c_{k}$ are scalars, than we may form the linear combination $c_{1}A_{1}+c_{2}A_{2}+\dots+c_{k}A_{k}$ 

The span of the set of matrices is the set of all linear combinations of them.

Def: the matrices $A_{1},A_{2},\dots A_{k}$ are #linearly_independentif the only solution to the equation $c_{1}A_{1}+c_{2}A_{2}+\dots c_{k}A_{k} = 0$ is the trivial solution, $c_{1}=c_{2}=\dots=c_{k}=0$
We can write this in an interesting way using matrixes. instead of having everything of one equation in one matrix, we have equations across matrixes
IE $$
c_{1}\begin{bmatrix}
1 & 2 \\
-1 & 1
\end{bmatrix}+ c_{2}\begin{bmatrix}
1 & 2 \\
-1 & 0
\end{bmatrix} = \begin{bmatrix}
0 & 0 \\
0 & 0
\end{bmatrix}
$$
forms the four equations
$$
\begin{align}
c_{1}+c_{2}=0 \\
-c_{1}-c_{2}=0 \\
2c_{1}+2c_{2}=0 \\
c_{1}=0
\end{align}

$$
Next time, we will talk about the identity matrix and inverse matrixes. 


## inverse matrixes
What if we multiply $a\vec{x}=\vec{b}$
and want to undo the transformation? 
Def: If A is an $n\times n$matrix, an #inverse_matrix of A is an $n\times n$ matrix with the property that 
$A^{-1}A = I$, and $AA^{-1}=I$ , where $I$ is the identity matrix. It can be proven that if an inverse matrix exists, there is only one. 
Ex:
$$
\begin{align}
A=\begin{bmatrix}
1 & -1 \\
3 & 0  
\end{bmatrix}
 \\
A^{-1}=\begin{bmatrix}
0 & \frac{1}{3} \\
-1 & \frac{1}{3}
\end{bmatrix}
\end{align}
$$
Is this true? Lets check
$$
\begin{align}
I \stackrel{?}{=} \begin{bmatrix}
1 & -1 \\
3 & 0  
\end{bmatrix}\begin{bmatrix}
0 & \frac{1}{3} \\
-1 & \frac{1}{3}
\end{bmatrix} \\
= \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix} \\
I \stackrel{?}{=} \begin{bmatrix}
0 & \frac{1}{3} \\
-1 & \frac{1}{3}
\end{bmatrix} \begin{bmatrix}
1 & -1 \\
3 & 0  
\end{bmatrix}\\
= \begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
\end{align}
$$

Since we have checked both ways, this is the correct inverse matrix for A. Why did we do two equations instead of applying a communitive property of matrixes?**Because there is no commutative property of matrixes! AB $\neq$ BA, so we have to check that each is $I$**. 

What is the inverse of $A^{-1}$? A! This follows from the fact that $$
(A^{T})^{-1}=(A^{-1})^{T}
$$ for all nonnegative integer n.

If A is invertible:
$$
\begin{align}
A^{-1^{-1}} &= A \\
\text{ if } c \neq 0,\text{ then } (cA)^{-1} &= \frac{1}{c}A^{-1} \\
\text{ If B is invrtable and the same size as A, then } (AB)^{-1}&=B^{-1}A^{-1} \\
(A^{T})^{-1}&=(A^{-1})^{T} \\
(A^{n})^{-1}&=(A^{-1})^{n} \\
\end{align}
$$
Lets try some exercises:
$$
\begin{align}
\left( \frac{1}{c}A^{-1} \right) = \frac{1}{c}c^{A^{-1}A}=I \\ \\

(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B \\
=B^{-1}IB = B^{-1}B = I
\end{align}
$$


We can have a matrix that breaks rules though, $$
\begin{bmatrix}
0 & 0 \\
0 & 0
\end{bmatrix}
$$
that transforms every matrix into the all zeros vector. This looses all information if we were to multiply it, so there is no way to send back. 

see next: [[Inverse of a Matrix]]
see previously: [[Matrix operations]]
