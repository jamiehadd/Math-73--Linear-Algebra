*Theorem*: if A is an invertible matrix, its inverse is unique.
*Proof*: By way of contradiction, suppose A has two inverses: $A'\text{ and } A''$
This means that $A'A=I=AA'$ and $A''A=I=A A''$. 
Well now show that $A'=A''$. 
$$
A'=A'I=A'(AA'')=(A'A)A''=IA''=A'' 
$$
Thus we have shown that there can only be 1 inverse. I still feel iffy about this proof that there can only exist one inverse of a function, but sure. 

## How can we compute the inverse?
For a $2\times 2$ matrix, if $A=\begin{bmatrix}a & b \\c & d\end{bmatrix}$and A is invertible, then $A^{-1}=\frac{1}{ad-bc}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}$
**General case intuition**: If $A$ is invertible, and $B$ is the inverse of $A$, then $AB=I$
We can think of this as a set of linear systems. We can use the matrix-column representation of systems to decouple this system.
$$
A\left[ \vec{b}_{1} ,\vec{b}_{2},\dots,\vec{b}_{n}\right]  = I = \left[ \vec{e}_{1},\vec{e}_{2},\dots,\vec{e}_{} \right]
$$
$\vec{e}_{1}\dots \vec{e}_{n}$ represents the identity matrix.
$$\begin{align}
A\vec{b}_{1} \text{ can be solved with } [A|\vec{e}_{1}] \\
A\vec{b}_{2}\text{ can be solved with } [A|\vec{e}_{2}] \\
A\vec{b}_{n} \text{ can be solved with } [A|\vec{e}_{n}]
\end{align}
$$
note: Solving the system $[A|\vec{b}]$ uses the same sequence of ERO's for any $\vec{b}$! The form of $A$ determines what sequence of EROs are necessary!

for each $A\vec{b}_{n}$ we turn the matrix into $\left[ RREF(A)|\vec{b}_{n} \right]$
Since there is only one inverse matrix, this will be $\left[ I|\vec{b}_{1} \right]$
We can stack together all of these vectors back, which is performing $\left[ A|I \right]\to[I|B]$. To summarize: in order to compute the inverse, we use the eros defined by a and act them on b and end up with a matrix B that will make the identity. 

Rigorously, what is going on here?
Each ERO is multiplying the matrix A and multiplying it by a particular matrix. #ERO **is really multiplication by elementary matrices**
#elementary_matrices: Any matrix that can be obtained by performing an ERO on an identity matrix. 
$$
\begin{align}
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix} \text{ swaps rows }  \\
\begin{bmatrix}
1 & 0 \\
0 & -3
\end{bmatrix} \text{scales by -3} \\

\begin{bmatrix}
1 & 1 \\
0 & 1
\end{bmatrix}\text{ does }r_{1}\to r_{1}+r_{2} 
\end{align}
$$
We can see this is due to swapping the identity, ie
$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}\xrightarrow {R_{1}\leftrightarrow R_{2}} \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$
What does this look like for a 3x3 matrix
$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}\xrightarrow {R_{1}\leftrightarrow R_{3}}\begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{bmatrix}
$$

We can undo ERO's by using their inverse matrixes.
For row swapping EROs, the inverse is itself
$$
\begin{align}
E=\begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{bmatrix},E^{-1=}\begin{bmatrix}
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0
\end{bmatrix}
 \\
E=\begin{bmatrix}
1 & 0 & 0 \\
0 & -7 & 0 \\
0 & 0 & 1
\end{bmatrix}, E^{-1} = \begin{bmatrix}
1 & 0 & 0\\
0 & -\frac{1}{7} & 0 \\
0 & 0 & 1
\end{bmatrix}
\end{align}
$$


see previous: [[Matrix Algebra and Inverse]]
