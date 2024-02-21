Recall: We saw the relationship between $\det(A)$ and the linear transformation encoded by the matrix $A$.

We can move from here to the page rank algorithm, which will motivate us to compute a vector $\vec{r}$ such that 
$$
A\vec{r}=\vec{r}
$$
This vector is an eigenvector, we'll get there soon. 

Back in the early stages of the internet, we needed a way for a search algorithm to rank internet pages. We'll measure the "importance" of webpages (nodes) by measuring the fraction of time that a random person traversing the links between nodes will land on that node. At each node, randomly pick an edge to traverse, then go along it. 

We can let matrixes represent this process:
![[Pasted image 20240221113304.png|300]]
$$
\begin{bmatrix}
0 & 0 & 1 & \frac{1}{2} \\
\frac{1}{3} & 0 & 0 & 0 \\
\frac{1}{3} & \frac{1}{2} & 0 & \frac{1}{2} \\
\frac{1}{3} &  \frac{1}{2} & 0 & 0
\end{bmatrix}
$$
This matrix represents the traverser's *transition* between nodes. 
Note that the diagonals are all zero, as we wont allow staying on a page. 

We can query for the probability of being on node 2, for example, with 
$$
\begin{bmatrix}
0\\0\\ \frac{1}{2} \\ \frac{1}{2}
\end{bmatrix}
=
\begin{bmatrix}
0 & 0 & 1 & \frac{1}{2} \\
\frac{1}{3} & 0 & 0 & 0 \\
\frac{1}{3} & \frac{1}{2} & 0 & \frac{1}{2} \\
\frac{1}{3} &  \frac{1}{2} & 0 & 0
\end{bmatrix}\begin{bmatrix}
0\\1\\0\\0
\end{bmatrix}
$$
This is representing the transition between node 2 and any other node.

Measuring the fraction of time that the surfer has been at node i tells us how important node i is relative to other nodes. Each additional step has little effect on the fraction.

(sidenote: for the curious, it might be interesting to look up "Markov chain", or "Markov process")

let $\vec{r}$ be the vector of fractions. Note that $\vec{r}=r_{1}\vec{e}_{1}+r_{2}\vec{e}_{2}+\dots+r_{n}\vec{e}_{n}$
One little step has no change on the fraction, so we have $A\vec{r}\approx \vec{r}$ . Going forever makes this even closer.

This can be written as
$$
\begin{align}
A\vec{r}=\vec{r}=I\vec{r} \\
\implies A\vec{r}-I\vec{r}=\vec{0} \\

\implies (A-I)\vec{r}=0
\end{align}
$$
Vectors that point in the same direction after transformation by $A$ are called #eigen_vectors of $A$; the amount by which an eigenvector is scaled is its #eigen_value.

For example: 
$$
\begin{align}
A=\begin{bmatrix}
2 & -2 \\
0 & 1
\end{bmatrix}\\
X = \begin{bmatrix}
1 & 1 & 3 & -1 \\
0 & -1 & 1 & -2
\end{bmatrix}
\end{align}
$$
$A\vec{x}_{1}=2\begin{pmatrix}1\\0\end{pmatrix}$
$A\vec{x}_{2}=2\begin{pmatrix}5\\-1\end{pmatrix}$
$A\vec{x}_{3}=\begin{pmatrix}3\\1\end{pmatrix}$
$A\vec{x}_{1}=2\begin{pmatrix}4\\-2\end{pmatrix}$

We can see that $\vec{x}_{2} \text{ and } \vec{x}_{4}$ are both scaled and rotated
$\vec{x}_{1}$ is the same
$\vec{x}_{3}$ is scaled but in the same direction.

## Calculating Eigenvectors:
For example: 
$$
A=\begin{bmatrix}
1 & 6 \\
5 & 2
\end{bmatrix}
$$
Show that $\lambda=7$ is an eigenvalue and find its corresponding eigenvector.

$7$ is an eigenvalue $\Leftrightarrow$ $A\vec{x}=7\vec{x}$
We can solve for $\vec{x}$:
$$
\begin{align}
A\vec{x}-7\vec{x}&=\vec{0} \\
(A-7I)\vec{x}&=\vec{0}  \\
\left( \begin{bmatrix}
1 & 6\\5 & 2
\end{bmatrix} - \begin{bmatrix}
7 & 0\\0 & 7
\end{bmatrix} \right) \vec{x} &= 0 \\
\implies \begin{bmatrix}
-6 & 6\\5 & -5
\end{bmatrix}\vec{x}&=\vec{0} \\
\begin{bmatrix}
-6 & 6 & | & 0 \\
5 & -5 & | & 0
\end{bmatrix} &\to   \begin{bmatrix}
1 & -1 & | & 0 \\
0 & 0 & | & 0
\end{bmatrix} \\
\implies \text{ solutions satisfy }x_{1}&=x_{2} \\
 \text{ so every vector in the form } &\\
\vec{x}=s\begin{pmatrix}
1\\1
\end{pmatrix}\\\text{ is an eigenvector of A corresponding to }\lambda= 7
\end{align}
$$


