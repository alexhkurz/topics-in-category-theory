# Clones, Monads, Lawvere Theories

Categories of algebras are usually defined wrt to a choice of *fundamental operations*. The choice of fundamental operations is somewhat arbitrary, their purpose is to define, via composition, the set of all terms. Clones, monads and Lawvere theories are three different ways to axiomatize "collections of all terms" without referring to a choice of fundamental operations.

The definitions are available in many places, eg at the nLab:
- [clone](https://ncatlab.org/nlab/show/clone#definition)
- [monad](https://ncatlab.org/nlab/show/monad#definition)
- [Lawvere theory](https://ncatlab.org/nlab/show/Lawvere+theory#definition)

What I want to do here is to sketch why these notions are equivalent.

We start from a category that has a forgetful ([faithful](https://ncatlab.org/nlab/show/faithful+functor)) functor $U:\cal A\to\sf Set$ with a left-adjoint $F\dashv U$. This includes in particular the case where $\cal A$ is a [variety](https://ncatlab.org/nlab/show/variety+of+algebras#definitions) in the sense of universal algebra, that is, a class of algebras defined by (finitary) operations and equations. 

In this more general situation, can we say what a term is, only referring to data provided by $U:\cal A\to\sf Set$? How can we collect all terms in one mathematical structure? How can we axiomatize this structure so that the axioms pick out exactly the structures that arise from those $U:\cal A\to\sf Set$ where $\cal A$ is a variety?

A key observation is that an $n$-ary term can be represented both as a morphism $F1\to Fn$ and as an element $1\to UFn$ of the underlying set of the free algebra over $n$ generators. 

The first leads us to Lawvere theories, the second to monads.

Given $U:\cal A\to\sf Set$, the induced 
- Lawvere theory is the opposite of the full subcategory of $\cal A$ spanned by $\{Fn \mid n \in \mathbb N\}$;[^n]
- monad is $UF$.[^inducedMonad]

[^n]: Our notation identifies a natural number $n$ with their cardinals $\{0,\dots n-1\}$.

[^inducedMonad]: We also need to define the unit $\eta$ which is the unit of the adjunction and the multiplication $\mu$ which is $U\varepsilon F$ where $\varepsilon$ is the counit of the adjunction. In the case that $\cal A$ is a variety, the unit maps a variable $x$ to the term $x$ and the multiplication $\mu_X:UFUFX\to UFX$ maps $t(t_1,\ldots t_n) \in UFUFX$ to $t(t_1,\ldots t_n) \in UFX$.

We will see later more reasons why one may want to define the Lawvere theory as the *opposite* of the full subcategory of finitely generated free algebras. For now, let us just note that we want to type an $n$-ary term as an arrow $n\to 1$ (because it takes $n$ inputs and gives $1$ output), the direction of which is opposite to the one from the morphism $F1\to Fn$ representing the term.

## Back and Forth Between The Definitions

In the following we sketch the constructions that allows us to go betweem the various axiomatization of algebra. Varieties and Lawvere theories are equivalent. Monads are more general. The monads that are equivalent to Lawvere theories are the finitary monads $\sf Set\to\sf Set$.

### Universal Algebra and Lawvere Theories 

Given a variety defined by operations and equations, let $\mathcal L(n,1)$ be the equivalence classes of $n$-ary terms.

Conversely, given a Lawvere theory, take all elements of $\mathcal L(n,1)$ as fundamental operations of arity $n$ and take all commuting triangles in $\cal L$ (with codomain $1$) as equations.

### Lawvere Theories and Monads 

Given a Lawvere theory $\cal L$, define $Mn=\mathcal L(n,1)$. To define $M$ on arrows we make use of the fact that a Lawvere theory comes with an identity-on-object product-preserving functor $\mathbb F^{op}\to\cal L$, where $\mathbb F$ is the category of finite cardinals with all functions.[^mathbbF] Finally, it remains to extend $M$ from finite sets to all sets, which can be done using standard techniques (such as the using the left-Kan extension along $\mathbb F\to\sf Set$).  


[^mathbbF]: $\mathbb F$ is the free category with finite coproducts on one generator. Dually, $\mathbb F^{op}$ is the free category with finite products on one generator. For example, there are exactly $n$ arrows $n\to 1$ in $\mathbb F^{op}$ and they corresponed to the $n$ projections from the $n$th power. In detail, given a set $A$ and an element in $A^n$, that is, a function $n\to A$ as well as an arrow $1\to n$, precomposing $n\to A$ with $1\to n$ is projection on to the coordinate selected by $1\to n$.


Conversely, given a monad $M:\sf Set\to Set$, $\mathcal L(n,1)=Mn$ defines a Lawvere theory.

### Universal Algebra and Monads

Given a variety $F\dashv U:\cal A\to\sf Set$, $M=UF$ defines a monad.

Conversely, given a monad $M$ one takes the elements of $Mn$ as the fundamental operations and the kernel of the multiplications $\mu_n:MMn\to Mn$ as the equations.






