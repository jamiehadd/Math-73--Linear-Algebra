
Def: A #linear_transformation from a vector space $V$ to a vector space $W$ is a mapping $T:V\rightarrow W$ such that
* $T(\vec{u}+\vec{v})=T(\vec{u})+T(\vec{v})$
* $T(c\vec{u})=cT(\vec{u})$
for $\vec{u},\vec{v} \in V$ and $c\text{ scalar }$
These requirements mean that $T$ preserves linear combinations. 

Properties:
* $T(\vec{0_{v}})=\vec{0}_{w}$
* $T(-\vec{v})=-T(\vec{v})$
* $T(\vec{u}-\vec{v})=T(\vec{u})-T(\vec{v})$
for all $\vec{u},\vec{v} \in V$.

## Composition
We can say the same for compositions of linear combinations.

$$
\begin{align}
(S\circ F)v =S(F(v)) \\
\text{  we can prove two things: } \\
(S \circ  F)(\vec{u}+\vec{t}) \\
=S(F(\vec{u}))+S(F(\vec{v})) \\
=(S\circ  F) \vec{u}+(s\circ  F)\vec{v}
\end{align}
$$
$$
\begin{align}
\text{ and }  
(S\circ  F)(c \vec{u}) \\
= S(F(c\vec{u})) \\
= c (S(F(\vec{u}))) \\
= c (S\circ  F)(\vec{u})
\end{align}
$$


## kernel and range

The kernel of $T$ is the set of all vectors that are mapped to zero in the output space $W$, ie $ker(t)=\left\{ \vec{v}\in V:T(\vec{v})=\vec{0}_{w} \right\}$
The range is all possible outputs, ie $T=\mathscr{P}_{3}\rightarrow\mathscr{P}_{2}$
$T(\vec{u})=\frac{d\vec{u}}{dx}$
$range(t)=\mathscr{P}_{2}$
$ker(T)=\mathscr{P}_{0}$

dim(ker(T))+dim(range(T))= dim(input space)

## one to one and onto
One to one: every input has a unique output vector. 
Onto: for a transformation $T:V\rightarrow W$, every vector in the set $W$ has a corresponding vector in $V$ that transforms onto it. To prove one to one, we have to look at the kernel and check that it is $\left\{ \vec{0} \right\}$. 

A linear transformation is called an #isomorphism if it is one to one and onto


a transformation is invertible if there is an inverse 
Theorem 1: $T$ is invertible $\Leftrightarrow$ $T$ is one to one and onto.


Theorem 2: A linear transformation $T:V\rightarrow W$ is one to one $\Rightarrow$ $ker(T)=\left\{ \vec{0} \right\}$

Proof for 2 (In the forward direction):
Assume $T$ is one to one. By definition of kernel, $T(\vec{v})=\vec{0}$ if $V\in ker(T)$. We know $T(\vec{0})=\vec{0}$ so $\vec{0}\in ker(T)$. But $T$ is one to one so if $T(\vec{v})=\vec{0}=T(\vec{0})$ then $\vec{v}=\vec{0}$. Thus, $ker(T)=\left\{ \vec{0} \right\}$. 
It is an exercise to the reader to prove the backwards direction.  for the second theorem. 


Theorem 3: If $T$ is one-to-one, ${\vec{v}_{1},\vec{v}_{2}\dots,\vec{v}_{n}}$ is linearly independent. This implies that $T(\vec{v}_{1}),T(\vec{v}_{2}),\dots,T(\vec{v}_{n})$ is linearly independent.  

Theorem 4: Let $T:V\rightarrow W$ be a linear transformation with $dim(V)=dim(W)$, then $T \text{ is one to one } \Leftrightarrow \text{ T is onto }$. 



is $\mathscr{P}_{2} \text{ isomorphic to } \mathbb{R}^{3}$? 
- they are the same dimension
- Can we provide a transformation tat is 1-1 and onto?

We can take the constants for each monomial in $\mathscr{P}_{2}$ and write it as the coordinate vector in $\mathbb{R}^{3}$.  We get that it is onto and one to one because they are both 3 dimensional, so we can use theorem 4. We can easily show either one-to-one or onto and prove that it is an isomorphism. 

Two finite dimensional vector spaces are isomorphic $\Leftrightarrow$ their dimensions are the same.

## Matrix of linear transformation

If $T:V\rightarrow W$ is a linear transformation, and $V,W$ have bases $B,C$, then there exists $A=\left[  T(\vec{v}_{1})_{c}, \dots , T(\vec{v}_{n})_{c}\right]$ that satisfies
$$
A[\vec{v}]_{b}=T(\vec{v})_{c}
$$
*side note*:  from this arises change of basis if the transformation is the identity.

Example: let $D:\mathscr{P}_{3}\rightarrow \mathscr{P}_{2}$ be the differential operator $D(p(x))=p'(x)$
Find the matrix $A$ of $D$ with respect to bases $B=\left\{ 1,x,x^{2},x^{3} \right\}$ for $\mathscr{P}_{3}$ and $C=\left\{ 1,x,x^{2} \right\}$ for $\mathscr{P}_{2}$. 

$A$ takes in vectors in $\mathbb{R}^{4}$ and spits out vectors in $\mathbb{R}^{3}$, so $A$ is a $3\times 4$ matrix.
We apply $D$ to every element of $B$. $D(1)=0,D(x)=1,D(x^{2})=2x,D(x^{3})=3x^{2}$
Now we find the coordinate vectors of each of these with respect to $c$.
We get 
$$
\begin{align}
A=\left[ \begin{pmatrix}
0 \\ 0 \\ 0
\end{pmatrix}, \begin{pmatrix}
1 \\ 0 \\ 0
\end{pmatrix}, \begin{pmatrix}
0 \\ 2 \\ 0
\end{pmatrix}, \begin{pmatrix}
0 \\ 0 \\ 3
\end{pmatrix}\right]  \\
A = \begin{bmatrix}
0 & 1 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 0 & 3
\end{bmatrix}
\end{align}
$$
We can now take derivatives of anything in $\mathscr{P}_{}^{3}$
Take, for example, $D(7-2x+9x^{2}-4x^{3})=-2+18x-12x^{2}$.
We can compute this with matrices by taking the coordinates from the input space and multiplying by $A$.
EX:
$$
\begin{bmatrix}
0 & 1 & 0 & 0 \\
0 & 0 & 2 & 0 \\
0 & 0 & 0 & 3
\end{bmatrix}\begin{pmatrix}
7 \\ -2 \\ 9 \\ -4
\end{pmatrix} = \begin{pmatrix}
-2 \\ 18 \\ -12
\end{pmatrix}
$$
A question: Is this invertible?

Theorem: $T$ is invertible $\Leftrightarrow$ the matrix $A$ is invertible. 

Note that
$$\begin{align}

T=I\circ  T=T\circ  I\text{ so } \\
[T]_{b\leftarrow  c}=[I]_{b\leftarrow  c}[T]_{c\leftarrow  c} \\
[T]_{b\leftarrow  c}=[T]_{b\leftarrow  b}[I]_{b\leftarrow  c}
\end{align}
$$
We have a somewhat familiar - (similar!) - equation that arises
$$
[T]_{c\leftarrow  c}=P_{b\leftarrow  c}^{-1}\, T_{b\leftarrow  b}\, P_{b\leftarrow  c}
$$
We have finished the fundamental theorem of invertible matrices:


$$
\begin{align}
\text{ A is invertible }
\end{align}
$$
$$
\begin{align}
\text{ Transformations: } \\
\text{ T is invertible } \\
\text{ T is one to one } \\
\text{ T is onto } \\
\text{ ker($T$) }={\vec{0}} \\
\text{ range($T$)=W }
\end{align}
$$

$$
\begin{align}
\text{ Solutions + Matrix forms: } \\
a\vec{x}=\vec{b} \text{ has a unique solution for every }\vec{b}\in \mathbb{R}^{n} \\
A\vec{x}=\vec{0} \text{ has only the trivial solution } \\
\text{ The RREF of A is }I_{n} \\
\text{ A is a product of elementary matrices }
\end{align}
$$

$$
\begin{align}
\text{ Columns: } \\
\text{ The column vectors of A are linearly independent } \\
\text{ The column vectors of A span }\mathbb{R}^{n} \\
\text{ The column vectors of A for a basis for } \mathbb{R}^{n}
\end{align}
$$
$$
\begin{align}
\text{ Subspaces: } \\
\text{ Rank(A)} =n \\
\text{ Nullity(A) }=0
\end{align}
$$
$$
\begin{align}
\text{ Rows: } \\
\text{ The row vectors of A are linearly indepenent } \\
\text{ The row vectors of A span } \mathbb{R}^{n} \\
\text{ The row vectors of A form a basis for } \mathbb{R}^{n}
\end{align}
$$
