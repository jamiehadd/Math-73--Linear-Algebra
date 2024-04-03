And now, we begin our voyage into the lands of abstract vector spaces...

We've learned about vector algebra and matrix algebra, which have properties of commutativity, associativity, identity, and inverse properties. These are examples of #vector_spaces the *set* of objects that satisfy those properties.  More rigorously, a vector space is a set $V$ with two operations:
$$
\begin{align}
:\vec{u}+\vec{v} \text{ where } \vec{u},\vec{v} \in V\\
:c\vec{u}\text{ where } \vec{u}\in V,c\text{ is a scaler} \\
\end{align}
$$
The set $V$ must follow 10 axioms:
1) V is closed under addition, ie $\vec{u}+\vec{v} \in V$
2) $\vec{u}+\vec{v}=\vec{v}+\vec{u}$
3) $(\vec{u}+\vec{v})+\vec{w}=\vec{u}+(\vec{v}+\vec{w})$
4) there is a vector $\vec{0}\in V$ which satisfies $\vec{u}+\vec{0}=\vec{u}$
5) for each $\vec{u} \in V$ there is a vector $-\vec{u} \in V$ which satisfies $\vec{u}+(-\vec{u})=\vec{0}$
6) $c\vec{u} \in V$
7) $c(\vec{u}+\vec{v})=c\vec{u}+c\vec{v}$
8) $(c+d) \vec{u}=c\vec{u}+d\vec{u}$
9) $c(d \vec{u})=(cd) \vec{u}$
10) $I \vec{u}=\vec{u}$

Before we can decide if something is in the vector space, we have to specify
* the set of objects/elements $V$
* vector addition +
* the set of scalars (chose to be elements of any *field*)
* scalar multiplication $c\vec{u}$

We understand the vector space $\mathbb{R}^{n}$, but we can abstract now to many more spaces. 

