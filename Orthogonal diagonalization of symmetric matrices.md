
 The great Spectral Theorem glues together diagonalization and orthogonality. 

First, an interesting observation.

Diagonalize the matrix 
$$
\begin{bmatrix}
2 & -1 \\
-1 & 2 
\end{bmatrix}
$$
We can first find the eigenvalues of the matrix.
Thus, $(2-\lambda)(2-\lambda)-(-1)(-1)=0$
$$
\begin{align}
4 - 4\lambda+ \lambda^{2} -1 = 0, \\
\lambda^{2} - 4 \lambda+ 3 = 0, \\
\lambda_{1}=1 \\
\lambda_{2} = 3
\end{align}
$$
This gives us a diagonal matrix $D$ = $\begin{bmatrix}3 & 0 \\ 0 & 1 \end{bmatrix}$
This matrix has the eigenvectors 
$$
\begin{pmatrix}
1 \\ -1 \\ 
\end{pmatrix} \text{ and } \begin{pmatrix}
1 \\ 1\\
\end{pmatrix}
$$
Which we can normalize and turn into a matrix $P$
$$
P = \begin{bmatrix}
\frac{1}{\sqrt{ 2 }} & \frac{1}{\sqrt{ 2 }}  \\
-\frac{1}{\sqrt{ 2 }}  & \frac{1}{\sqrt{ 2 }} 
\end{bmatrix}
$$
We have an orthonormal set of vectors. Because they must be linearly independent, we can find $P^{-1}$. 

$$
\begin{bmatrix}
\frac{1}{\sqrt{ 2 }} & \frac{1}{\sqrt{ 2 }}   & | & 1 & 0\\
-\frac{1}{\sqrt{ 2 }}  & \frac{1}{\sqrt{ 2 }}  & | & 0 & 1\\
\end{bmatrix}
$$
We can now simplify to get the inverse
$R_{2}\to R_{2}+R_{1}, R_{1}\to R_{1}-\frac{1}{2}R_{2},R_{1} \text{ and } R_{2}\to \times \sqrt{ 2 }$ 
$$
P^{-1}=\begin{bmatrix}
\frac{1}{2} & -\frac{1}{2} \\
\frac{1}{2} & \frac{1}{2}
\end{bmatrix}
$$
**We can see that this is $P^{T}$.**
$D=P^{T}AP=P^{-1}AP$
Is this a fluke?

A real symmetric matrix implies that all eigenvalues are real.
A symmetric matrix with distinct eigenvalues implies that eigenvectors are orthogonal.

Instead of just having an invertible matrix of eigenvectors, we have an orthogonal matrix. 

A matrix is #orthogonally_diagonalizable if there is an orthogonal matrix $Q$ and a diagonal matrix $D$ such that $Q^{-1}=Q^{T}$, meaning that $Q^{T}AQ=D = Q^{-1}AQ$.

The spectral theorem: Suppose $A$ is a real, $n\times n$ matrix. Then $A$ is symmetric *if and only if* $A$ is orthogonally diagonalizable.
Proof:
Suppose $Q^{T}AQ=D$. Since $Q$ is orthogonal, we have $QDQ^{T}=QQ^{T}AQQ^{T}=A$. 
Now, $A^{T}=(QDQ^{T})^{T}=QD^{T}Q^{T}=QDQ^{T}=A$. We can now do the forwards direction.  


Lets use this:
To orthogonally diagonalize a matrix, find the eigenvalues and then eigenvectors. Make an orthogonal basis by subtracting off projections if there are repeated eigenvalues, otherwise they are already orthogonal. Then normalize the matrix.




Side note: I didn't notate the previous lecture. Essentially:
We can take any matrix and find an orthonormal basis for it. Take any vector, then for the next vector in the matrix subtract off the projection of that vector onto the first, then for the next subtract off projections onto the already existing vectors, etc. This will make an orthogonal matrix. If each time your normalize the vector, then it becomes an orthonormal basis. 


See previous: [[Orthogonal Complement]]
