### Exercise

Find a basis for $P_{1}$ the set of *all* polynomials
Every polynomial is a linear combination of monomials, $a_{0}+a_{1}x+a_{2}x^{2}+a_{3}x^{3}\dots a_{n}x^{n}$
So $B=\left\{ 1,x,x^{2},x^{3},\dots,x^{n} \right\}$ is a spanning set for $P$. It is linearly independent and also infinitely long ... cool.

Lets write a proof by contradiction that the set of al monomials is linearly independent:
Suppose there is some finite set of $B$ with $n$ vectors that is linearly *dependent* $\left\{ x^{P_{1}},x^{P_{2}},\dots,x^{Pn} \right\}$ where $P_{1}<p_{2}<p_{3}\dots<p_{n}$. Then there are some scalars (not all zero), $c_{1},c_{2},\dots,c_{n}$ so that $c_{1}x^{P_{1}}+c_{2}x^{P_{2}}+\dots+x^{P_{n}} = 0$
This polynomial is $0$ for all values of $x$. *BUT* the fundamental theorem of algebra says that a nonzero polynomial can have at most $n$ roots. Thus, the polynomial would have to be the zero polynomial with $c_{1}=c_{2}=\dots=c_{n}=0$. This is a contradiction, $\implies$ any finite set of $B$ is linearly independent $\implies$ $B$ is linearly independent.


## Dimension
Def: 
1) A vector is #finite_dimensional if it has a basis consisting of finitely many vectors
2) A vector space is #inifinite_dimensional if it has no finite basis
3) The vector space ${\vec{0}}$ is #zero_dimensional

## Coordinates
Lets move to something that is more concrete. Lets say we have a finite basis $B=\left\{ \vec{b}_{1},\dots,\vec{b}_{n} \right\}$ for the vector space $V$.then any $\vec{v}\in V$ can be written uniquely as a linear combination of $\vec{v}=c_{1}\vec{b}_{1}+\dots+c_{n}\vec{b}_{n}$

The unique coefficient $c_{1},\dots,c_{n}$ are called the #coordinates of $\vec{v}$ relative to the basis $\beta$, (or #b-coordinates). The entries in the coordinate vector are the coordinates of this combination. We can see this easily with the x y plane - to specify a point $(2\vec{x},3\vec{y})$ we just write out $(2,3)$. If instead we had a rotated representation, we would still be specifying points with the coefficients scaling each vector. 

Take the vector space represented by $\begin{bmatrix}a\\b\\b\\c \end{bmatrix}$ 
We have a basis
$$
\beta=\left\{ \begin{bmatrix}
\begin{pmatrix}
1 \\ 0 \\ 0 \\0
\end{pmatrix}, & \begin{pmatrix}
0 \\ 1 \\ 1 \\ 0
\end{pmatrix}, & \begin{pmatrix}
0 \\ 0 \\ 0 \\1
\end{pmatrix}
\end{bmatrix} \right\}
$$
We can specify coordinates of a point $\begin{bmatrix}2 \\-7 \\ -7 \\ 8\end{bmatrix}$ with  $\begin{bmatrix}2\\-7\\8\end{bmatrix}$, because those coordinates multiplied by the basis makes the point. We can make any basis and choose any coordinates to form that coordinate as long as $\beta$ is a basis for $V$.

What are the coordinates of 
$$
\begin{bmatrix}
2 & -7 \\
-7 & 8
\end{bmatrix}
$$
in the basis 
$$
\beta=\left\{ \begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
\begin{bmatrix}
0 & 1 \\
1 & 0  \\
\end{bmatrix},
\begin{bmatrix}
0 & 0 \\
0 & 1
\end{bmatrix}
\right\}
$$
The same, $\begin{bmatrix}2\\-7\\8\end{bmatrix}$!

### Some facts about coordinates
if $B$ is a basis, then
$\left[ \alpha_{1}\vec{u}_{1} + \alpha_{2} \vec{u}_{2} + \dots \alpha _{n} \vec{u}_{n} \right]=\alpha_{1}[\vec{u}_{1}]+\dots+\alpha_{k}[\vec{u}_{k}]$
This follows from the fact that 
$[\vec{u}+\vec{v}]_{\beta}=[\vec{u}]+[\vec{v}]$, and $[\alpha \vec{u}]_{\beta} = \alpha[\vec{u}]_{\beta}$

We can use coordinate vectors to check the linear independence of vector spaces that are not $\mathbb{R}^{n}$. 
$$
\begin{align}
\left\{ \vec{u}_{1},\dots,\vec{u}_{n} \right\}\text{ is linearly independent }  \\
\Leftrightarrow\left\{ [\vec{u}_{1}]_{b},\dots,[\vec{u}_{n}]_{b} \right\} \text{ is linearly independent in }\mathbb{R}^{n}
\end{align}
$$
(make a careful note of the difference between $k$ and $n$ in the above).

## Changing the basis
The choice of basis is important. How do we switch between bases?

In $\mathbb{R}^{2}:$
$B= \left\{ \begin{bmatrix}\begin{pmatrix}1\\0\end{pmatrix},\begin{pmatrix}1\\1\end{pmatrix}\end{bmatrix} \right\}$
          $\vec{u},\vec{v}$
We can represent the point $[5,-1]_{b}$ as coordinates $\begin{bmatrix}4\\-1\end{bmatrix}$ in the standard basis.

What if we want to change to a different basis?
$$
C=\left\{ \begin{bmatrix}
\begin{pmatrix}
0\\1
\end{pmatrix}, & \begin{pmatrix}
2 \\ 3
\end{pmatrix}
\end{bmatrix} \right\}
$$
We can represent x now as the solution to

$$
\begin{bmatrix}
4 \\ -1
\end{bmatrix} = c_{1}\begin{pmatrix}
0\\1
\end{pmatrix}+c_{2}\begin{pmatrix}
2\\3
\end{pmatrix}
$$
We can write this out as
$$
\begin{bmatrix}
4\\-1
\end{bmatrix}=\begin{bmatrix}
2c_{2}\\c_{1}+3c_{2}
\end{bmatrix}
$$
Or, in a slightly nicer and simultaneously grosser way,
$$
\begin{bmatrix}
4\\-1
\end{bmatrix}=\begin{bmatrix}
0 & 2 \\
1 & 3
\end{bmatrix}\begin{bmatrix}
c_{1} \\ c_{2}
\end{bmatrix}
$$
We can see that $c_{2}=2$, meaning $c_{1}=-7$.

However, this was a long process (find coordinates in the standard basis and then in the new). A far better  way is to use a "change of basis" matrix.
$[\vec{x}]_{c}=\left( [\vec{u}_{1}]_{c}[\vec{u}_{2}]_{c} \right)[\vec{x}]_{b}$
We take the basis vectors in $c$ and multiply by the representation of $\vec{x}$ in $b$ in order to find the representation of $\vec{x}$ in $c$. 


We take in some vectors from basis B, compute the representations of those in c, and then we use that to represent the transformation from B to C. We represent this change of basis matrix as $P_{c\leftarrow b}$. Because matrix multiplication is from right to left, we take a matrix represented in B from the right and multiply it to get a matrix in C. 

Suppose $B=\left\{ \vec{u}_{1},\dots,\vec{u}_{i} \right\}$ and $C=\left\{ v_{1},\dots,v_{n} \right\}$ then 

The $i^{th}$ column of $P_{c\leftarrow b}$ is $[\vec{u}_{i}]_{\epsilon}=\begin{bmatrix}p_{1,i}\\p_{2,i}\\\vdots\\p_{n,i}\end{bmatrix}$ and $\vec{u}_{i}=p_{1,i}\vec{v}_{i}+\dots+p_{n,i}\vec{v}_{i}$


If $\epsilon$ is any basis for $V,$ then $[u_{i}]_{\epsilon}=$
$$
\left( [\vec{v}_{1}]_{\epsilon},\dots,\vec{v}_{n}]_{\epsilon} \right) 
\begin{bmatrix}p_{1,i}\\p_{2,i}\\\vdots\\p_{n,i}\end{bmatrix}
$$


We can solve this with gaussian elimination
$$
\begin{bmatrix}
[\vec{v}_{1}]_{\epsilon} & [\vec{v}_{2}]_{\epsilon} & | & [\vec{u}_{1}]_{\epsilon} & [\vec{u}_{2}]_{\epsilon}
\end{bmatrix}
$$
Lets do a concrete example.
Take 
$$
B=\left\{ \begin{pmatrix}
1 \\ 0
\end{pmatrix}, \begin{pmatrix}
1 \\ 1
\end{pmatrix} \right\}, C = \left\{ \begin{pmatrix}
0 \\ 1 
\end{pmatrix}. \begin{pmatrix}
2 \\ 3
\end{pmatrix} \right\}
$$
We can compute the change of basis from $B\rightarrow C$

$$
P_{c \leftarrow  b} = \left( \begin{bmatrix}
\begin{pmatrix}
1 \\ 0
\end{pmatrix}
\end{bmatrix}_{c},\begin{bmatrix}
\begin{pmatrix}
1 \\ 1
\end{pmatrix}
\end{bmatrix}_{c} \right) 
$$
We can row reduce
$$
\begin{align}
\begin{bmatrix}
0 & 2 & | & 1 & 1 \\
1 & 3 & | & 0 & 1 \\
\end{bmatrix} \rightarrow  \\
\begin{bmatrix}
1 & 0 & |  & -\frac{3}{2} & -\frac{1}{2} \\
0 & 1 & | & \frac{1}{2} & \frac{1}{2}
\end{bmatrix}
\end{align}
$$
The right hand side is our change of basis matrix $P_{c \leftarrow b}$










