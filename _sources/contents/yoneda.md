# The Yoneda Embedding

(under construction)

I leave it as an exercise to show that the following implicit definitions are equivalent to the familiar ones.

It is instructive to develop this in parallel for categories and for posets. 

Let $\mathcal C$ be a category and let $X$ be a poset.

$X(x,y)=1$ means $x\le y$ and $X(x,y)=0$ means $x\not\le y$. The function $X(x,y)$ is order-reversing in $x$ and order-preserving in $y$.

$\mathcal C(A,B)$ is the set of arrows $A\to B$. The functor $\mathcal C(A,B)$ is contravariant in $A$ and covariant in $B$. 

Note that $\mathcal C^{op}(A,B)=\mathcal C(B,A)$.

## Warm-up

An arrow $f:B\to A$ is mono if $\mathcal C(X,f):\mathcal C(X,B)\to \mathcal (X,A)$ is injective for all $X\in\mathcal C$.

An arrow $f:A\to B$ is epi if $\mathcal C(f,X):\mathcal C(B,X)\to \mathcal (A,X)$ is injective for all $X\in\mathcal C$.

## Limits

**Categories:** $A\times B$ is the product of $A$ and $B$ iff

$$\mathcal C(C,A\times B)\cong \mathcal C(C,A)\times  \mathcal C(C,B)$$

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


## The Yoneda Embedding

We have seen that various category theoretic notions can be defined both explicitely via universal properties and implicitely via equations up to isomorphism. 

There is a general explanation for this, that is based on the following results.
- Limits in functor categories are computed pointwise.
- The Yoneda embedding preserves limits.
- The Yoneda embedding is fully faithful.

For every small[^small] category $\mathcal C$ there is a functor

\begin{align}
\mathcal C^{op}\times \mathcal C  & \to \sf Set\\
A\ ,B & \mapsto \mathcal C(A,B)
\end{align}

The two Yoneda embeddings are obtained by fixing one of the coordinates

\begin{align}
\mathcal C(-,A) : \mathcal C^{op}  & \to \sf Set\\
\end{align}

\begin{align}
\mathcal C(A,-) : \mathcal C  & \to \sf Set\\
\end{align}

- In the case of monos, we use that $m$ is mono if $(1,1)$ is a pullback of $(m,m)$. We can now prove the "Warm-up" as follows.
    - If $m$ is mono, then $(1,1)$ is a pullback of $(m,m)$. Since the Yoneda embedding preserves limits, we have that  $(\mathcal C(-,1),\mathcal C(-,1))$ is a pullback of $\mathcal C(-,m),\mathcal C(-,m)$. Since limits in functor categories are computed pointwise, $(\mathcal C(X,1),\mathcal C(X,1))$ is a pullback of $\mathcal C(X,m),\mathcal C(X,m)$ for all $X\in\mathcal C$. Note that $\mathcal C(X,1)$ is the identity on $X$. Hence $\mathcal C(X,m)$ is mono for all $X$. Because monos in $\sf Set$ are injective, we proved that \mathcal C(X,m)$ is injective for all $X$.
    - Conversely, $m$ is mono if $(1,1)$ is a pullback of $(m,m)$. Because the Yoneda embedding is fully faithful, this follows if $(\mathcal C(X,1),\mathcal C(X,1))$ is a pullback of $\mathcal C(X,m),\mathcal C(X,m)$ for all $X\in\mathcal C$. But the latter, as we have seen in the previous item, is just another way to say that $\mathcal C(X,m)$ is injective for all $X$.
- The case of epis is the dual, using that an epi in $\mathcal C$ is a mono in $\mathcal C^{op}$.
- The case of products (or limits) uses the same steps of reasoning as the case of monos. The case of coproducts (or colimits) is dual again.

[^small]: Small here means that the collection $\mathcal C_0$ of objects of $\mathcal C$ is an object in $\sf Set$. Many categories do have a "proper class" of objects. In that case, one can use a category $\sf Set$ that has so-called Grothendieck universes (or an inaccessible cardinal).

**Exercise:** Show that the Yoneda embedding preserves limits, that is, if $C\cong\lim D$ then $\mathcal C(X,C)\cong\lim\mathcal C(X,D)$. [^functorCategory]

[^functorCategory]: If $D:\mathcal I\to\mathcal C$ is a functor ($D$ for "diagram"), then $\mathcal C(X,D)$ is the induced  functor $\mathcal I\to \sf Set$.

## Order-Enriched Categories

Many categories have more structure than just being a category. For example, in a category of ordered structures one can define an order on morphisms pointwise. Then homsets are ordered sets, typically partial orders (posets). Given such a category $\mathcal C$, we have a functor 

$$\mathcal C(-,-):\mathcal C^{op}\times\mathcal C\to \sf Pos.$$

This allows us to introduce new variations on the notions of this section. 

For example, above we showed that *an arrow $f:B\to A$ is mono if $\mathcal C(X,f):\mathcal C(X,B)\to \mathcal (X,A)$ is injective for all $X\in\mathcal C$.*

In $\sf Pos$, instead of saying injective, we can also say embedding (order-preserving and order-reflecting).

**Exercise:** What is the "diagrammatic" definition that characterizes, in a category $\mathcal C$ with ordered homsets, arrows $f$ with $\mathcal C(X,f):\mathcal C(X,B)\to \mathcal (X,A)$ is an *embedding* for all $X\in\mathcal C$?

**Exercise:** What is the "diagrammatic" definition that characterizes, in a category $\mathcal C$ with ordered homsets, the product $A\times B$ now defined by asking the equation

$$\mathcal C(C,A\times B)\cong \mathcal C(C,A)\times  \mathcal C(C,B)$$

to be an isomorphism in the category of posets?






