## Complex Eigenvalues:
Recall that we can find eigenspaces. IE: $$
A=\begin{bmatrix}
2 & 3 \\
3 & -6
\end{bmatrix}
$$ with $\lambda=3$.
Steps:
$$
\begin{align}
(A-\lambda I|0) \\
\begin{bmatrix}
-1 & 3 & | & 0 \\
0 & 0 & | & 0
\end{bmatrix} \\
\implies x_{1}=3x_{2} \\
\text{ so } \\
\left\{  t\begin{bmatrix}
3 \\ 1
\end{bmatrix} \forall t \in \mathbb{R}^{} \right\} \\

 =s pan(\begin{bmatrix}
3\\ 1
\end{bmatrix})
\end{align}
$$
are both ways of representing the eigenspace. 

How to actually find eigenvalues?
$$
\begin{align}
A\vec{v}=\lambda \vec{v} \\
A\vec{v}=\lambda I\vec{v} \\
(A-\lambda I)\vec{v} = \vec{0} \\
\end{align}
$$
This implies $A-\lambda I$ is not invertible. We are looking for values that makes this not invertible. This happens if and only if $\det(A-\lambda I) = 0$.

**$\lambda$ is an eigenvalue of $A \Leftrightarrow \lambda$ satisfies the characteristic equation $\det(A-\lambda I)= 0$.** Also remember, the eigenvalues are the diagonal values of any triangle matrix. 

We can see something interesting:
For example: Find the eigenvalues of $A=\begin{bmatrix}0&-1 \\ 1 & 0\end{bmatrix}$ and find the basis for the eigenspace corresponding to each eigenvalue.

we need to find $\lambda$ so that 
$$
\begin{align}

\det(\begin{bmatrix}
-\lambda & -1 \\
1 & -\lambda
\end{bmatrix} )= 0 \\
\implies \lambda^{2}+1 = 0 \\
\lambda = \pm i
\end{align}
$$
Complex eigenvalues still have eigenspaces:
$$
\begin{align}
\lambda= i \\
\begin{bmatrix}
-i & -1  & | & 0 \\
1 & -i & | & 0
\end{bmatrix}\xrightarrow {iR_{1}\to  R_{1}} \\
\begin{bmatrix}
1 & -i & | & 0 \\
1 & -i & | & 0
\end{bmatrix}\to  \begin{bmatrix}
1 & -i & | & 0 \\
0 & 0 & | & 0
\end{bmatrix} \\
\vec{x}=s\begin{pmatrix}
i \\ 1
\end{pmatrix} \implies \left\{ \begin{pmatrix}
i \\ 1
\end{pmatrix} \right\} \text{is a basis for }E_{i} \\
 \\
\lambda= -i: \\
\begin{bmatrix}
i & -1 & | & 0 \\
1 & i & | & 0
\end{bmatrix}\to   \\
\begin{bmatrix}
1 & i & | & 0 \\
0 & 0 & | & 0
\end{bmatrix} \\
\vec{x} = s \begin{pmatrix}
-i \\ 1
\end{pmatrix} \implies \left\{ \begin{pmatrix}
-1 \\ 1
\end{pmatrix}  \right\}\text{ is a basis for} E_{-i} \\
\end{align}
$$

We find that doing this rotation matrix preserves lines in the complex space, which we have to interpret with the scalar multiplication. 

Remember: The determinant of any triangle matrix is the product of the values along the diagonal

For example: find the eigenvalues of 
$$
A = \begin{bmatrix}
3 & 6 & -8 \\
0 & 0 & 6 \\
0 & 0 & 2
\end{bmatrix}
$$
As in the $2\times  2$ case, eigenvalues of $A$ are zeros of the characteristic polynomial, 
$$
\begin{align}
\det(A-\lambda I)=\det \begin{bmatrix}
3-\lambda & 6 & 8 \\
0 & -\lambda & 6 \\
0 & 0 & 2-\lambda
\end{bmatrix} \\
= (3-\lambda)(-\lambda)(2-\lambda)
\end{align}
$$

For each of the three solutions, $\lambda= 3, \lambda= 0, \lambda= 2$
We can find a basis by plugging in that lambda and then reducing the matrix. We get: 
$$
\left\{ 
\begin{bmatrix}
1 \\ 0 \\ 0\end{bmatrix},
\begin{bmatrix}
-2 \\ 1 \\ 0
\end{bmatrix},\begin{bmatrix}
-10 \\ 3 \\ 1
\end{bmatrix}\right\}
$$
 
## Eigenvalues and invertibility
Theorem: Suppose $A$ has a zero eigenvalue:
$$
\begin{align}
\implies &A\vec{x}=\vec{0} \text{ for some nontrivial }\vec{x} \\
\implies &\text{ A is not invertible }
\end{align}
$$

$A$ is invertible $\Leftrightarrow$ 0 is **not** an eigenvalue of A.

