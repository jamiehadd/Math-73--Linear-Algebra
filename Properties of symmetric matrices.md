
"Spectral" $\implies$ eigen stuff

Symmetric matrices have nice spectral properties. For instance:

If we  have a real and symmetric matrix, the eigenvalues are real. 

Before: For any matrix, eigenvectors associated to distinct eigenvalues are linearly independent.
Now: For a symmetric matrix, eigenvectors associated to distinct eigenvalues are orthogonal. 

## Orthogonal Diagonalization 
A matrix is #orthogonally_diagonalizable if there is an orthogonal matrix $Q$ and a diagonal matrix $D$ such that $Q^{T}AQ=D$.

The spectral theorem: Suppose A is a real, $n\times n$ matrix. Then A is symmetric if and only $A$ is orthogonally diagonalizable. We have the nice property that $Q^{-1}=Q^{T}$.

Proof: Suppose $Q^{T}AQ=D$ Since $Q$ is orthogonal, we have $QDQ^{T}=QQ^{T}AQQ^{T}=A$. Now, $A^{T}=(QDQ^{T})^{T}=QD^{T}Q^{T}=QDQ^{T}=A$ Thus $A^{T}=A$ so $A$ is symmetric. 

$A$ is symmetric implies that $A$ is orthogonally diagonalizable. Thus, we have the set $\text{ symmetric } \subseteq \text{ orthogonally diagonalizable }$.
We also have orthogonally diagonalizable matrix is symmetric, so we have $\text{ OD }\subseteq \text{ Sym }$
Thus, $\text{ Orthogonally diagonalizable matrices }\Leftrightarrow \text{ symmetric }$
The power of diagonalization is that we can easily find the eigendata or determinants etc.

For example:
take the symmetric matrix of all real components
$$
A=\begin{bmatrix}
3 & -2 & 4 \\
-2 & 6 & 2 \\
4 & 2 & 3 \\
\end{bmatrix}
$$
The characteristic polynomial is $(\lambda-7)^{2}(\lambda+2)$ so the eigenvalues are $7,7,2$. The eigenspaces are

$$
E_{-2}=span\left\{ \begin{pmatrix}
-2 \\ -1 \\ 2
\end{pmatrix} \right\} 
E_{7}=s pan\left\{ \begin{pmatrix}
1 \\ 0 \\ 1
\end{pmatrix}, \begin{pmatrix}
-1 \\ 2\\ 0
\end{pmatrix} \right\} 
$$
We can apply Gram Schmidt to get the orthogonal basis for $E_{7}$ (they aren't yet orthogonal). 
We then normalize and get
$$
Q=\begin{bmatrix}
\frac{1}{\sqrt{ 2 }} & -\frac{\sqrt{ 2 }}{6} & -\frac{2}{3} \\
0 & \frac{2\sqrt{ 2 }}{3} & -\frac{1}{3} \\
\frac{1}{\sqrt{ 2 }} & \frac{\sqrt{ 2 }}{6} & \frac{2}{3}
\end{bmatrix}
$$
and 
$$
D=\begin{bmatrix}
7 & 0 & 0 \\
0 & 7 & 0 \\
0 & 0 & -2
\end{bmatrix}
$$
The judicious reader can check that $Q^{T}AQ=D$. 

