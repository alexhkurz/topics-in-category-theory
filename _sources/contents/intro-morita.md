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

The category $\sf Set$ is equivalent to the category $\sf RBI$ of "rectangular bands with involution", that is, to the category of algebras $B$ with a unary operation $s$ and a binary operation $\cdot$ satisfying

\begin{gather}
x\cdot (y\cdot z) = (x\cdot y)\cdot z\\
x\cdot y \cdot z = x\cdot z\\
x\cdot x = x\\
s(s(x)) = x
\end{gather}

**Remark:** To interpret the equations one can think of elements $x$ as pairs $(a,b)$ with operations defined by 
\begin{gather}
(a,b) \cdot (c,d)=(a,d)\\
s(a,b)=(b,a)
\end{gather}

**Exercise:** Show that (with $s$ and $\cdot$ defined as in the remark above) the operation $H$ 

\begin{align}
{\sf Set} & \stackrel H ⟶ \sf RBI\\
A & \ \mapsto \ (A^2,s,\cdot)
\end{align}

is an equivalence of categories:
- $H$ is a functor.
- $H$ is essentially surjective.
- $H$ is full and faithful.

**Remark/Question:** The category $\sf Set$ can be seen as a category of algebras defined by no operations and no equations. As we have seen $\sf Set$ is equivalent to the category of rectangular bands with involution defined by a much more sophisticated algebraic theory. Is there a general theory that explains which algebraic theories give rise to equivalent categories of algebras? Conversely, given a category of algebras, can we classify the algebraic theories that give rise to equivalent categories of algebras?

The proof of the previous exercise can be decomposed into two steps. Instead of doing $\sf Set \to RBI$ in one go we want to introduce an intermediate step $\sf Set \to Set^{[2]}\to RBI$. The reason to do this is that the first step will turn out to be a general method, while the second step will contain the reasoning particular to the situation at hand.

**Exercise:** The category $\sf Set^{[2]}$ has as objects sets $A^2=A\times A = \{(a,b) \mid a,b \in A\}$ with operations formed from projections $p^n_i:A^n\to A$, $p^n_i(x_1,\ldots x_n)=x_i$. 
- List the four operation $A^2\to A^2$, which we will call $id$, $l$ (for left), $r$ (for right), $s$ (for swap). 
- Define an operation $\cdot$ of type $(A^2)^2 \to A^2$ such that 
    \begin{gather}
    x\cdot (y\cdot z) = (x\cdot y)\cdot z\\
    x\cdot y \cdot z = x\cdot z\\
    x\cdot x = x
    \end{gather}
- Define $l$ and $r$ using $s$ and $\cdot$.
- Show that a morphism $A^2\to B^2$ compatible with projections must be of the form $f\times f$ with $f:A\to B$.
- Show that the obvious functor $\sf Set\to Set^{[n]}$ is an equivalence of categories.

(to be continued)

