# Introduction

(under construction)

In very general terms, two theories (formalized as categories) are Morita equivalent if their categories of models are equivalent. 
- The question posed by Morita was when two rings induce equivalent categories of modules. For example, any ring $R$ is Morita equivalent to the ring of 
$n\times n$ matrices with elements from $R$. We will see variations of this result below.
- Presheaf categories $[\mathcal C^{op},\sf Set]$ and  $[\mathcal D^{op},\sf Set]$ are equivalent iff the closure under retracts of $\mathcal C$ and of $\mathcal D$ are equivalent. This closure is known as the Karoubi envelope, or also as closure under splitting of idempotents, a terminology that will be explained below.
- In the following, we will be mainly interested in the question when two algebraic theories give rise to equivalent categories (varieties) of algebras.

To see why Morita equivalence of varieties is interesting let us look at some examples.

## Sets and Rectangular Bands with Involution

This is Example 2 in {cite}`McKenzie:equivalence-for-varieties`.

Consider algebras (which I call RBI-algebras for now) given by a unary operation $s$ and a binary operation $\cdot$ satisfying the equations

\begin{gather}
x\cdot (y\cdot z) = (x\cdot y)\cdot z\\
x\cdot y \cdot z = x\cdot z\\
x\cdot x = x\\
s(s(x)) = x
\end{gather}

**Fact:** Every RBI-algebra $B$ is of the form $B=A\times A$. 

We can say more: The category $\sf RBI$ of RBI-algebras ("RBI" as in "rectangular bands with involution") is equivalent to the category $\sf Set$.

**Observation:** One can interpret the equations thinking of the elements of an RBI-algebra as pairs $(a,b)$ with operations defined by 
\begin{gather}
(a,b) \cdot (c,d)=(a,d)\\
s(a,b)=(b,a)
\end{gather}

In other words, every set $A$ gives rise to an RBI-algebra $A^2$.

**Exercise:** Show that (with $s$ and $\cdot$ defined as in the remark above) the operation $H$ 

\begin{align}
{\sf Set} & \stackrel H ⟶ \sf RBI\\
A & \ \mapsto \ (A^2,s,\cdot)
\end{align}

is an equivalence of categories:
- $H$ is a functor.
- $H$ is essentially surjective.
- $H$ is full and faithful.

One aspect that makes equivalences like this interesting is that they may not preserve free algebras:

**Exercise:** Show that the free RBI over $X$ has $(2X)^2$ elements.


**Remark/Question:** The category $\sf Set$ can be seen as a category of algebras defined by no operations and no equations. As we have seen $\sf Set^{[2]}$ is equivalent to RBI which is defined by a much more sophisticated algebraic theory. Is there a general theory that explains which algebraic theories give rise to equivalent categories of algebras? Conversely, given a category of algebras, can we classify all equivalent categories?

To answer these and similar questions is the purpose of  Morita equivalence. 

As a warm-up, we notice that the proof of the previous exercise can be decomposed into two steps. Instead of doing $\sf Set \to RBI$ in one go we want to introduce an intermediate step $\sf Set \to Set^{[2]}\to RBI$. The reason to do this is that the first step will turn out to be part of a general method.

**Exercise:** The category $\sf Set^{[2]}$ has as objects sets $A^2=A\times A = \{(a,b) \mid a,b \in A\}$ with operations formed from projections $p^n_i:A^n\to A$, $p^n_i(x_1,\ldots x_n)=x_i$ and tupling. 
- List the four operations $A^2\to A^2$, which we will call $id$, $l$ (for left), $r$ (for right), $s$ (for swap). 
- More generally, the set of operations $A^m\to A^k$ formed by projections and tupling is of cardinality $m^k$.
- Define an operation $\cdot$ of type $(A^2)^2 \to A^2$ such that 
    \begin{gather}
    x\cdot (y\cdot z) = (x\cdot y)\cdot z\\
    x\cdot y \cdot z = x\cdot z\\
    x\cdot x = x
    \end{gather}
- Define $l$ and $r$ using $s$ and $\cdot$.
- Show that a morphism $A^2\to B^2$ compatible with maps defined from projections must be of the form $(a,a')\mapsto (f(a),f(a'))$ for some $f:A\to B$.
- Show that the obvious functor $\sf Set\to Set^{[2]}$ is an equivalence of categories.

(to be continued)

