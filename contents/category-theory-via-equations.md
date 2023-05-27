# Category Theory via Equations

(under construction)

I leave it as an exercise to show that the following implicit definitions are equivalent to the familiar ones.

It is instructive to develop this in parallel for categories and for posets. 

Let $\mathcal C$ be a category and let $X$ be a poset.

$X(x,y)=1$ means $x\le y$ and $X(x,y)=0$ means $x\not\le y$. The function $X(x,y)$ is order-reversing in $x$ and order-preserving in $y$.

$\mathcal C(A,B)$ is the set of arrows $A\to B$. The functor $\mathcal C(A,B)$ is contravariant in $A$ and covariant in $B$.

## Warm-up

An arrow $f:B\to A$ is mono if $\mathcal C(C,f):\mathcal C(C,B)\to \mathcal (C,A)$ is injective for all $C\in\mathcal C$.

An arrow $f:A\to B$ is epi if $\mathcal C(f,C):\mathcal C(B,C)\to \mathcal (A,C)$ is injective for all $C\in\mathcal C$.

## Limits

**Categories:** $A\times B$ is the product of $A$ and $B$ iff

$$ \mathcal C(C,A\times B)\cong \mathcal C(C,A)\times  \mathcal C(C,B)$$

where the $\times$ on the left is what is defined and the $\times$ on the right is the ordinay cartesian product in Set.

*Exercise:* Generalize this to other limits.

**Orders:** $x\wedge y$ is the meet of $x$ and $y$ iff

$$X(z,x\wedge y) = X(z,x)\wedge X(z,y)$$

where the $\wedge$ on the left is the meet in $X$ defined by the equation and the $\wedge$ on the right is the "and" in the 2-element Boolean algebra.

## Colimits

**Categories:** $A + B$ is the product of $A$ and $B$ iff

$$ \mathcal C(A + B, C)\cong \mathcal C(A,C)\times  \mathcal C(B,C).$$

*Exercise:* Generalize this to other colimits.

**Orders:** $x\vee y$ is the join of $x$ and $y$ iff

$$X(x\vee y,z) = X(x,z)\wedge X(y,z).$$


## Yoneda Lemma

That these implicit definitions define the object in question up to isomorphism, is a consequence of the Yoneda lemma ... tbc ...