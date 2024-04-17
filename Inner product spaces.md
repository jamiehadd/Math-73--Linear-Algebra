
## Inner products
Def: $\vec{u},\vec{v},\vec{w}$ are vectors in a vector space $V$ and $c$ is a real scalar. an #inner_product is an operation that assigns a real number $\left< \vec{u},\vec{v} \right>$ to each pair of vectors $\vec{u},\vec{v}$ and is 
* Symmetric: 
	* $\left< \vec{u},\vec{v} \right> = \left< \vec{v},\vec{u} \right>$
	* $\left< \vec{u},\vec{v}+\vec{w} \right> = \left< \vec{u},\vec{v} \right>+\left< \vec{u},\vec{w} \right>$
* Linear:
	* $\left< c\vec{u},\vec{v} \right> = c\left<\vec{u},\vec{v}  \right>$
* Positive semi-definite:
	* $\left< \vec{u},\vec{v} \right> \geq 0$ with $\left< \vec{u},\vec{u} \right> =0$  if and only if $\vec{u}=\vec{0}$.


We can define length, distance, and orthogonality for any inner product.

Def: let $\left< \vec{u},\vec{v} \right>$ be an inner product on vector space $v$. The length or norm of $\vec{v}\in V$ is $\left| \vec{v} \right|=\sqrt{ \left< \vec{v},\vec{v} \right> }$. A unit vector satisfies $\left| \vec{v} \right|=1$. The distance between $\vec{u}\text{ and } \vec{v}$ is $\left| \vec{u}-\vec{v} \right|$. We say $\vec{u}\text{ and } \vec{v}$ are orthogonal if $\left< \vec{u},\vec{v} \right> =0$.

IE, the distance between $\sin(x) \text{ and } \cos(x)\in [0,2\pi]$ is
$$
\begin{align}
\left< \sin(x),\cos(x) \right> =\int_{0}^{2\pi} \sin(x)\cos(x) \, dx  \\
=\frac{1}{2}\int_{0}^{2\pi} 2\sin(x)\cos(x) \, d \\
=\frac{1}{2}\int_{0}^{2\pi} \sin(2x) \, d \\
=0  
\end{align}
$$
so $\sin(x)\text{ and } \cos(x)$ are orthogonal in $c[0,2\pi]$ with respect to this inner product.

We can also generalize:
* Pythagorean Theorem: If $\vec{u},\vec{v}$ are orthogonal, $\left| \vec{u} \right|^{2}+\left| \vec{v} \right|^{2}= \lvert \vec{u}+\vec{v} \rvert^{2}$
* Cauchy - Schwarz inequality: $\left| \left< \vec{u},\vec{v} \right> \right|\leq \lvert \vec{u} \rvert\lvert \vec{v} \rvert$
* Triangle inequality: $\left| \vec{u}+\vec{v} \right|\leq \lvert \vec{u} \rvert+\lvert \vec{v} \rvert$

### Gram-Schmidt
We can even generalize the Gram-Schmidt process to general vector spaces with an inner product!

For example: Find an orthogonal basis for $W=span\left\{ 2,x+1,x^{2}-1 \right\}$
We take $v_{1}=y_{1}=2$
$$
\begin{align}
v_{2}&=y_{2}- \frac{\left< \vec{y}_{2},\vec{v}_{1} \right> }{\left< \vec{v}_{1},\vec{v}_{1} \right> }\vec{v}_{1} \\
&=c+2-\frac{\left( \int_{0}^{1} 2(x+1) \, dx  \right)}{\int_{0}^{1} 2*2 \, dx }2 \\
&= x+1-\frac{3}{2}=x-\frac{1}{2} \\
v_{3}&=y_{3}-\frac{\left< v_{3},v_{1}\right>v_{1} }{\left< v_{1},v_{1} \right> } - \frac{\left< y_{3},v_{2} \right>}{\left< v_{2},v_{2} \right> }v_{2}  \\
\end{align}
$$
$$
\begin{align}
&=x^{2}-1-\frac{\left( \int_{0}^{1} 2(x^{2}-1) \, dx  \right)}{\int_{0}^{1} 4 \, dx }2- \frac{\left( \int_{0}^{1} \left( x-\frac{1}{2} \right)(x^{2}-1) \, dx  \right)}{\left( \int_{0}^{1} \left( x-\frac{1}{2} \right)^{2} \, dx  \right)}\left( x-\frac{1}{2} \right)\\
&= x^{2}-x+\frac{1}{6}
\end{align}
$$

