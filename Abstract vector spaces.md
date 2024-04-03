## Linear combinations
A linear combination looks the same as before,
$c_{1}v_{1}+\dots+c_{n}v_{n}$. We know that this holds, as the vector space is closed under addition and scalar multiplication. 

The span of a set is the set of all linear combinations. If $v=span(s), v$ is a spanning set for $V$. 

We can now ask some fun questions:
is $3-2x^{2}$ in the span of $p(x)=1-x+x^{2}\text{ and } q(x)=2+x-3x^{2}$
We can write out the polynomials as vectors and check if there exists $c_{1},c_{2}$ such that
$$
c_{1}\begin{bmatrix}
1 x^{2} \\ -x \\ 1
\end{bmatrix} + c_{2} \begin{bmatrix}
-3x^{2} \\ x \\ 2
\end{bmatrix} = \begin{bmatrix}
-2x^{2}\\0\\3
\end{bmatrix}
$$
We can rewrite this more neatly
$$
\begin{bmatrix}
c_{1}-3c_{2}=-2 \\
-c_{1}+c_{2}=0 \\
c_{1}+2c_{2}=3 \\
\end{bmatrix}
$$
aka                                          c1       c2         value we want
$$
\begin{bmatrix}
1 & -3 & | & -2 \\
-1 & 1 & | & 0 \\
1 & 2 & | & 3
\end{bmatrix}
$$
Can we find a solution? We row reduce and get 
$$
\begin{bmatrix}
1 & 0 \\
0 & 1 \\
0 & 0
\end{bmatrix} \begin{bmatrix}
c_{1} \\ c_{2}
\end{bmatrix} = \begin{bmatrix}
1\\1\\0
\end{bmatrix}
$$
We see that $c_{1}=1,c_{2}=1$. So $3-2x^{2}=1(p(x))+1(q(x))$

Also, we can see that we don't span all of $P_{2}$, as we only have 2 equations and need to represent 3 variables $c,x,x^{2}$. 

## Subspaces:
Let v be a vector space an $W$ be a nonempty subset of V. $W$ is a #subspace if and only if :
* it contains the zero vector: $\vec{0}\in W$ where $\vec{0}$ is the zero vector of $V$
* closed under addition: if $\vec{u},\vec{v} \in W$,  then $\vec{u}+\vec{v}\in W$
* closed under scalar multiplication: if $\vec{u}\in W$ and $C$ is scalar, then $c\vec{u} \in W$ 


Lets do some practice:
$$
\left\{ \begin{bmatrix}
a  & b\\ c & d
\end{bmatrix} : ad=0,\,  a,b,c,d \in  \mathrm{Re} \right\}
$$
Is this a subspace of $M_{2,2}$? (answer - no)
For $2\times 2$ matrices, we add and multiply component wise.
### 1:
This is a non empty set, as $\downarrow$
### 2:
we have the zero vector in the set $\begin{bmatrix}0&0\\0&0\end{bmatrix}$
### 3:
we are closed under scalar multiplication since
$$
s\begin{bmatrix}
a & b \\
c & d
\end{bmatrix} = \begin{bmatrix}
sa & sb\\ sc & sd
\end{bmatrix}, ab=0,(sa)(sb)=0,s(ab)=0, s(0)=0
$$
so we are closed under multiplication.

### 4:
BUT! not closed under addition.
$$
\begin{bmatrix}
a_{1} & b_{1} \\ c_{1} & d_{1}
\end{bmatrix} + \begin{bmatrix}
a_{2} & b_{2} \\ c_{2} & d_{2}
\end{bmatrix} = \begin{bmatrix}
a_{1}+a_{2} & b_{1}+b_{2} \\
c_{1}+c_{2} & d_{1}+d_{2}
\end{bmatrix}
$$
$(a_{1},d_{1})=0 \text{ and } a_{2}b_{2}=0$ does not imply
$(a_{1}+a_{2})(d_{1}+d_{2})=0$
Because this term expands to
$$
\begin{align}
(a_{1}d_{1})+(a_{1}d_{2})+(a_{2}d_{1})+(a_{2}d_{2}) \\
0+a_{1}d_{2}+a_{2}d_{1}+0 \text{ is not always 0 }
\end{align}
$$
### Conclusion:
We didn't check all the boxes. Therefore, this is a subset of $M_{2,2}$ but not a subspace of $M_{2,2}$.


