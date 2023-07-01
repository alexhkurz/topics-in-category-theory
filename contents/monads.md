# Monads

Monads can be seen as generalising two different concepts: closure operators and monoids. 

Algebras for a monad are generalising cosed elements and actions.

## Preliminaries

- Closure operator: [Wkipedia](https://en.wikipedia.org/wiki/Closure_operator), [nLab](https://ncatlab.org/nlab/show/closure+operator)
- Monoid (or Group) Action: [Wikipedia](https://en.wikipedia.org/wiki/Group_action), [nLab](https://ncatlab.org/nlab/show/action)

## Definition

Definition of Monad and algebra of a monad:

MacLane ... nLab ...

This definition makes sense in any 2-category and in any ordered category.

Check that closure operators are examples.

**Theorem:** If $F\dashv U:A \to X$ then $UF$ is a monad.

*Proof:* Exercise.

**Theorem:** If $M$ is a monad on $\cal X$, then the forgetful functor $U:\sf Alg(M)\to\cal X$ has a left-adjoint $F$ and $F\dashv U$ and $M=UF$.

**Example:** In the ordered setting, this is specialises to the well known theorem that every closure operator arises from a Galois connection.

## Beck's Theorem

...




