Lets take some data: the points $(0,0),(1,1),(2,4)$. What is the best straight line to approximate this data? We are trying  to find the "best" solution to systems without solutions.

A line through this data has the form $y=c+mx$ where we want to compute $m$ and $c$. 

$$
\begin{align}
c+2m=4 \\
c+1m=1 \\
c+0m=0
\end{align} \implies \begin{pmatrix}
1 & 2\\ 1 & 1 \\ 1  & 0
\end{pmatrix} \begin{pmatrix}
c \\ m 
\end{pmatrix} = \begin{pmatrix}
4 \\ 1 \\ 0
\end{pmatrix}
$$

Trying to solve yields
$$
\begin{align}
\begin{pmatrix}
1 & 2 & | & 4 \\
1 & 1 & | & 1 \\
1 & 0 & | & 0
\end{pmatrix}\rightarrow  \begin{pmatrix}
1 & 2 & | & 4 \\
1 & 1 & | & 1 \\
0 & 1 & | & 1
\end{pmatrix}\rightarrow  \begin{pmatrix}
1 & 2 & | & 4 \\
0 & 1 & | & 3 \\
0 & 1 & | & 1
\end{pmatrix}
\end{align}
$$
This doesn't have a solution, but we can still ask what has the best line. 

We want to minimize the distance between each point and the line, aka the least squares error. 
We will minimize the norm of errors between these points
$$
\begin{align}
\sqrt{ e_{1}^{2}+e_{2}^{2}+e_{3}^{2} } 
\end{align}
$$
By best approximation, we mean
$$
\begin{align}
\left| v-\bar{v}  \right|\leq \left< v-w \right> \forall \, w\in  W \text{ where  } w\neq \vec{v}
\end{align}
$$
If $Ax=b$ has a solution, then $e_{1}=e_{2}=e_{3}=0$. That is, $\left| b-Ax \right|=0$, $b$ and $Ax$ are the same vector. If there is no solution, then what is the vector $\bar{y}=A\bar{x}$ in col(A) that is the best approximation to $b$?

That is, the vector in $W$ that has the shortest distance to v. 
![[Pasted image 20240417115232.png]]
Claim: $\bar{v}=proj_{w}(v)$.
Proof: By the Pythagorean theorem, $\lvert v-\bar{v} \rvert^{2}+\lvert \bar{v}-w \rvert^{2}=\lvert v-w \rvert^{2}$ since $v-\bar{v}$ is orthogonal to $\bar{v}-w\in W$. Thus, $\lvert v-\bar{v} \rvert^{2}\leq \left| v-w \right|^{2}$ for any $w\neq \bar{v},w\in W$.

We want $x=\bar{x}$ that gives the orthogonal projection of b onto col(A). 
$$
\begin{align}
A\bar{x} & =proj_{col(A)}(b) \\
b-A\bar{x} & =b-proj_{col(A)}(b)  \text{ (in the nulll( }A^{T}\text{)) }\\
A^{T}(b-A\bar{x}) & =0 \implies A^{T}A\bar{x}=A^{T}b.
\end{align}
$$
Theorem: Let $A$ be an $m\times n$ matrix and $b\in \mathbb{R}^{m}$. Then a least squares solution $\bar{x}$ of $Ax=b$ satisfies "the normal equations for $\bar{x}$": $A^{T}A\bar{x}=A^{T}b$.

Lets solve this with our example. Remember, we have the points $(0,0),(1,1),(2,4)$. 
Since we can't solve the system, we will look for a least squares solution $\bar{x}:$
$$
\begin{align}
A^{T}A\bar{x}=A^{T}b \\
A^{T}A=\begin{bmatrix}
1 & 1 & 1 \\
2 & 1 & 0
\end{bmatrix} \begin{bmatrix}
1 & 2 \\
1 & 1 \\
1 & 0
\end{bmatrix} = \begin{bmatrix}
3 & 3 \\
3 & 5
\end{bmatrix} \\
A^{T}b=\begin{bmatrix}
1 & 1 & 1 \\
2 & 1 & 0
\end{bmatrix}\begin{bmatrix}
4 & 1 & 0
\end{bmatrix}=\begin{bmatrix}
5\\9
\end{bmatrix}
\end{align}
$$
so we have 
$$
\begin{align}
\begin{bmatrix}
3 & 3 \\
3 & 5
\end{bmatrix}\begin{bmatrix}
\bar{x}_{1}\\\bar{x}_{2}
\end{bmatrix}  & = \begin{bmatrix}
5\\9
\end{bmatrix} \\
\begin{bmatrix}
3 & 3 & | & 5 \\
3 & 5 & | & 9
\end{bmatrix} & \rightarrow  \begin{bmatrix}
3 & 3 & | & 5 \\
0 & 2 & | & 4
\end{bmatrix}\rightarrow  \begin{bmatrix}
3 & 0 & | & -1 \\
0 & 1 & | & 2
\end{bmatrix} \\
 & \rightarrow  \begin{bmatrix}
1 & 0 & | & -\frac{1}{3} \\
0 & 1 & | & 2
\end{bmatrix}  \\
  \text{ because } x_{1}  & = c,x_{2}=m ,\text{ the line we seek is } \\
  y&=2x-\frac{1}{3}
\end{align}
$$
We can calculate the least squares error:
$$
\begin{align}
\left| e \right| & =\left| b-A\bar{x} \right| \\
 & = \left| \begin{pmatrix}
4\\1\\0
\end{pmatrix} -\begin{bmatrix}
1 & 2\\1 & 1\\1 & 0
\end{bmatrix} \begin{pmatrix}
-\frac{1}{3}\\2
\end{pmatrix}\right| \\
 & =\left| \begin{pmatrix}
4\\1\\0
\end{pmatrix} -\begin{pmatrix}
\frac{\frac{11}{3}\\5}{3}\\-\frac{1}{3}
\end{pmatrix}\right| \\
 & =\left|\begin{pmatrix}
\frac{1}{3} \\-\frac{2}{3}\\-\frac{1}{3}
\end{pmatrix}  \right| \\
 & =\frac{1}{3}\left| \begin{pmatrix}
1\\-2\\-1 
\end{pmatrix} \right| \\
 & = \begin{bmatrix}
1\\-2\\-1
\end{bmatrix} \\
 & =\frac{\sqrt{ 6 }}{3}
\end{align}
$$
However, small numerical errors in Gaussian elimination create large errors in the least squares solution (a computer struggles with $\frac{1}{3}$, they approximate it). IE. exploding rockets etc in the real world because of how massively these rounding errors stack up. 
QR factorizations are more reliable and stable in this case.

Suppose $A$ is a $m\times n$ matrix with linearly independent columns, $b\in \mathbb{R}^{m}$. 
We can use $QR$ factorization to find the least squares solution $\bar{x}$ for $Ax=b$.

Since $A$ has linearly independent columns, we can find a $QR$ factorization
$A=QR$ where $Q$ is orthogonal and $R$ is upper triangular and invertible. With some manipulation, we can find a much better system of equations.
$$
\begin{align}
 & A^{T}A\bar{x} =A^{T}b \\
 & \implies (AR)^{T}(AR)\bar{x}=(QR)^{T}b \\
 & \implies R^{T}Q^{T}QR\bar{x}=R^{T}Q^{T}b \\
 & \implies R^{T}R\bar{x}=R^{T}Q^{T}b \\
 & \implies R\bar{x}=Q^{T}b
 & \end{align}
$$
The only math we have to do is multiplication and subtraction when solving for $R$. This is a much nicer system.


