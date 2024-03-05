## Orthonormal sets
A set of vectors in $\mathbb{R}^{n}$ is called an #orthogonal_set if all pairs of distinct vectors in the set are orthogonal, ie 
$$
\vec{v}_{i}\cdot \vec{v}_{j}=0 \, \forall i\neq j, \, i,j\in Z
$$
An orthogonal set of unit vectors is called an orthonormalset. That is
$$
\vec{v}_{i}\cdot \vec{v}_{j}=\begin{Bmatrix}
0 \text{ if } i\neq j \\
1 \text{ if } i = j
\end{Bmatrix}
$$
For example:
$$
\left\{ \vec{v}_{1}=\begin{pmatrix}
3 \\ 1 \\ 1 
\end{pmatrix}m \vec{v}_{2} = \begin{pmatrix}
-1 \\ 2 \\ 1
\end{pmatrix}, \vec{v}_{3} = \begin{pmatrix}
-\frac{1}{2} \\ -2 \\ \frac{7}{2}
\end{pmatrix} \right\}
$$
We can see that all pairs are orthonormal by computing the dot product between all of them.

We get an orthonormal set by making all of these unit vectors, ie 
$$
\vec{V}_{1} = \frac{v_{1}}{\left| v_{1} \right|},\text{ etc }
$$
This doesn't change the angle of any vector, so they are still orthonormal. 

Why do we care about orthonormal sets?
Suppose $\vec{v}_{1},\dots,\vec{v}_{k}$ is an orthogonal set and all $\vec{v}_{i}$ are nonzero, and consider the equation
$$
c_{1}\vec{v}_{1}+c_{2}\vec{v}_{2}+\dots+c_{k}\vec{v}_{k} = \vec{0}
$$
For any $j=1,\dots, k$ we can compute 
$$
\begin{align}
0 = \vec{v}_{j}\cdot 0 = c_{1}(\vec{v}_{j}\cdot v_{1}) + \dots + c_{j}(\vec{v}_{j}\cdot \vec{v}_{j})  \\
= \vec{v}_{j}\cdot \vec{v}_{j}
\end{align}
$$
Since $\vec{v}_{j}$ is nonzero, we have $c_{j} = 0$. Since our choice of $j$ was arbitrary, we know that $c_{1}=c_{2}=\dots=c_{k}$. All of the constants are zero, so this set is linearly independent. 

Theorem: if $\left\{ \vec{v}_{1},\dots,\vec{v}_{k} \right\}$ is an orthogonal set of nonzero vectors in $\mathbb{R}^{n}$, then they are linearly independent. 

We can use this to compute the constants. 
$$
\vec{w}=c_{1}\vec{v}_{1}+\dots+c_{k}\vec{v}_{k}
$$
taking dot products,
$$
\begin{align}
\vec{v}_{j}\cdot\vec{w} &= c_{1}(\vec{v}_{j}\cdot \vec{v}_{1}) + \dots + c_{k}(\vec{v}_{j}+\vec{v}_{k}) \\
 &= c_{j}(\vec{v}_{j}\cdot \vec{v}_{j})
\end{align}
$$
so $c_{j}=\frac{\vec{v}_{j}\cdot \vec{w}}{\vec{v}_{j}\cdot \vec{v}_{j}}$

For example: 
take two vectors in $\mathbb{R}^{2}$ which are linearly independent and orthogonal
$$
V = \left\{ \vec{v}_{1}=\begin{pmatrix}
2 \\ 2
\end{pmatrix} , \vec{v}_{2} = \begin{pmatrix}
1 \\ -1
\end{pmatrix}\right\}
$$
$W = \begin{pmatrix}-1 \\ 2\end{pmatrix}$ is a linear combination of $\vec{v}_{1},\vec{v}_{2}$
![[Pasted image 20240304113402.png]]

## Orthogonal transformations
Interesting examples:
$$
\begin{bmatrix}
\cos\theta & -\sin \theta \\
\sin \theta & \cos\theta 
\end{bmatrix}
$$
and 
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 0 & 1 \\
0 & 1 & 0
\end{bmatrix}
$$
This second one is a "permutation" if the identity matrix, ie just simple row operations have generated it.

Orthogonal matrices are #angle-preserving and #length-preserving.

we can write out these properties as such:
$$
\begin{align}
(Q\vec{x})\cdot(Q\vec{y}) \\
= (Q\vec{x})^{T}(Q\vec{y} \\
= \vec{x}^{T}Q^{T}Q\vec{y} \\
= \vec{x}^{T}y
\end{align}
$$

## Properties of orthogonal matrices
Let $Q$ be an orthogonal matrix.
- The rows of Q also (like the columns) form an orthonormal set
- $Q^{-1}$ is also an orthogonal matrix
- $\det Q=1\text{ or }-1$
- if $\lambda$ is an eigenvalue of $Q$, then $\left| \lambda \right|$ = 1
- The product of orthogonal matrices is orthogonal. 


See previous: [[Similarity and Diagonalization]]