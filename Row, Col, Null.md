
def: Suppose $A$ is a $n\times m$ matrix. The row space of $A$ is the subspace $row(A)$ or $\mathbb{R}^{m}$ spanned by the rows

The column space of $A$ is the subspace $row(A)$ or $\mathbb{R}^{m}$ spanned by the columns.

If we take a matrix

$$
A=\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix}
$$

row(A)

$$
= \begin{bmatrix}
\begin{pmatrix}
1 \\
2 \\
3
\end{pmatrix} & \begin{pmatrix}
4 \\
5 \\
6
\end{pmatrix}
\end{bmatrix}
$$

and col(a) = 
$$
\begin{bmatrix}
\begin{pmatrix}
1 \\
4
\end{pmatrix} & \begin{pmatrix}
2 \\ 5 
\end{pmatrix} & \begin{pmatrix}
3 \\ 6
\end{pmatrix}
\end{bmatrix}
$$

We can see that the dimension of the Row space is 2, so the column-space also has dimension 2.

A #consistent system has either 1 or infinitely many solutions. $\infty$ is if there is a free variable, or #inconsistent if there is an impossible row, ie $\begin{bmatrix}0&0&0&|&nonzero\end{bmatrix}$ 

col(A) tells us what $\vec{b}$ vectors yield consistent linear solutions. These are the possible outputs $A\vec{x}$. 

row(A) tells us the possible results of doing EROs on $A$. 

Null(A) = $\{ \vec{x}\in\mathbb{R}^{n}:A\vec{x}=\vec{0} \}$. 
Ex:
$$
A = \begin{bmatrix}
1 & -3 & -2 \\
-5 & 9 & 1
\end{bmatrix}\text{ and } \vec{u}=\begin{bmatrix}
5\\3\\-2
\end{bmatrix}
$$
Null(A):
$$
A\vec{u}=\begin{bmatrix}
1 & -3 & -2 \\
-5 & 9 & 1
\end{bmatrix}\begin{bmatrix}
5\\3\\-2
\end{bmatrix}=\begin{pmatrix}
0\\0 \\
\end{pmatrix}
$$
Theorem: The null space of an $m\times n$ matrix $A$ is a subspace of $\mathbb{R}^{n}$. 
proof: Note $A \vec{0} = \vec{0}$, so $\vec{0} \in nul l(A)$.
Suppose $\vec{v},\vec{u}\in n u ll(A)$. Note that $A(c\vec{u}+d\vec{v})=cA\vec{u}+dA\vec{v}=c_{0}0+d_{0}0=\vec{0}$, so $c\vec{u}+d\vec{v}\in \text{ null }(A)$

The idea behind the null space of a matrix is that it is precisely those vectors in the domain being sent to the $\vec{0}$ vector in the codomain. We have to find the solution set of $Ax=0$.

We do this by finding the null space of a reduced row echelon form of $A$, which has the same null space as $A$. That is, if  $B$ is the reduced row echelon form for $A$ , $Ax=0$ if and only if $Bx=0$ So, $N(B)=N(A)$ 

For example, take
$$
A=\begin{bmatrix}
1 & 4 & 0 & 2 & -1 \\
3 & 12 & 1 & 5 & 5 \\
2 & 8 & 1 & 3 & 2 \\
5 & 20 & 2 & 8 & 8
\end{bmatrix}
$$
We reduce to RREF, then find the free variables and write the result in a nice form $$
\begin{bmatrix}
x_{1}\\x_{2}\\x_{3}\\x_{4}\\x_{5}
\end{bmatrix}=
x_{1}\begin{bmatrix}
num\\num\\num\\num\\num
\end{bmatrix} + x_{2}\begin{bmatrix}
num\\num\\num\\num\\num
\end{bmatrix} \dots
$$
whatever, to use the free variables to define every variable. The vectors attached with these free variables is the Null space of A. 
in this example, we find the null space as
$$
\begin{bmatrix}
\begin{pmatrix}
-4\\1\\0\\0\\0
\end{pmatrix} & \begin{pmatrix}
-2\\0\\1\\1\\0
\end{pmatrix}
\end{bmatrix}
$$
so dim(null(A)) = 2.


Any two bases of a subspace contain the same number of vectors
Def: The *dimension* of a nonzero subspace $S$ of $\mathbb{R}^{n}$ is the number of nonzero vectors in a basis for $S$. We can write this as $dim(S)$. Special case: $dim{(\vec{0})}=0$.

Fact: Any set of $n$ *linearly independent* vectors forms a basis for $\mathbb{R}^{n}$.

## Rank nullity theorem:
#rank: dimension of the row or column space = $\text{\# of rows or columns}=$  # leading variables.
$rank=dim(row(A))=d i m(col(A))$
$\text{nullity = number of free variables}$
$\text{nullspace = linearly dependent columns }$

$\text{num vectors} =\text{ rank} + \text{ nulity }$
$\uparrow$ this is the Rank Nullity Theorem. Number of free leading variables + number of free variables = total number of variables. This fact seems obvious, but it is a very useful fact to have stated.
I f there are no free variables then null(A) = 0 and rank(A) = n.

Take an $n\times n$ matrix where $Rank(A)=n$
$$
\begin{align}
\Leftrightarrow \text{ nullity }(A)=0 \Leftrightarrow \text{ null A }=\{ \vec{0} \} \\
\Leftrightarrow \text{ The only solutino to  }A\vec{x}=\vec{0} \text{ is } \vec{x}=\vec{0} \\
\Leftrightarrow A \text{ is invertible }
\end{align}
$$
