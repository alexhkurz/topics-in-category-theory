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

The category $\sf Set$ is equivalent the category of $\cal W$ of "rectangular bands with involution", that is, to the category of algebras $B$ with a unary operation $s$ and a binary operation $\cdot$ satisfying

\begin{gather}
x\cdot (y\cdot z) = (x\cdot y)\cdot z\\
x\cdot y \cdot z = x\cdot z\\
x\cdot x = x\\
s(s(x)) = x
\end{gather}

To interpret the equations one can think of elements $x$ as pairs $(a,b)$ and $(a,b) \cdot (c,d)=(a,d)$ and $s(a,b)=(b,a)$. 

**Exercise:** Show that (with $s$ and $\cdot$ defined as indicated above) the operation $H$ 

\begin{align}
{\sf Set} & \stackrel H ⟶ \cal W\\
A & \ \mapsto \ (A^2,s,\cdot)
\end{align}

is an equivalence of categories:
- $H$ is a functor.
- $H$ is essentially surjective.
- $H$ is full and faithful.

