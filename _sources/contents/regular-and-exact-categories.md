# Regular and Exact Categories

(under construction)

## Introduction

Regular categories

- are a generalisation of abelian categories and ordinary categories of algebras;
-  have a good notion of image factorisation;
-  gives rise to a categories of relations. [^relations]
 
[^relations]: Why is it that the notion of a category is general enough to accommodate relations as arrows but then every introduction to category theory quickly abandons the example of relations and focusses on examples in which arrows are functions? One reason is that categories of relations are typically not closed under limits and colimits. A move that often works is the following. Regular categories are very common and they give rise to categories of relations with good properties, which are often best studied as so-called double categories in which "relational" arrows and "functional" arrows exist together.

For a rough comparison, we can look at

|general categories | categories with free algebras
|:---:|:---:|
|regular | quasi-variety |
|exact | variety |

## Definitions

An arrow that arises as a coequalizer is called  a **regular epi**.

**Definition:** A **regular category** has finite limits and coequalizers and regular epis are stable under pullbacks. 

**Examples:** 
- Varities and quasi-varities in the sense of universal algebra are regular categories. 
- The category of posets (and many other categories of topological spaces) are not regular because regular epis are not stable under pullbacks.
- If $\mathcal B$ is regular than the category of functors $[\mathcal A,\mathcal B]$ is regular. In particular, presheaf categories are regular.
- If $\mathcal A$ is regular than the slice category $\mathcal A/A$ is regular.

**Exercises:**
- Every regular epi is an epi.
- If a regular epimorphism has a kernel pair, it is the coequalizer of that kernel pair.
- If a kernel pair has a coequalizer, it is the kernel pair of that regular epimorphism.
- Find a pullback $(p,q)$ of $(j,k)$ in the category of posets where $k$ is a regular epi but $p$ is not.

**Exercises**:
- (Epis don't need to be surjective.) In the category of monoids, the inclusion $(\mathbb N,0,+)\to (\mathbb Z,0,+)$ is epi but not regular epi.
- In a regular category, every morphism factors as a regular epi followed by a mono.[^factorization]
- In a regular category, the composition of regular epis is regular.[^compRegEpi]

[^factorization]: To factorize $f$, we observe that the coequalizer $e$ of the kernel pair of $f$ is a regular epi. The universal property of a coequalizer allows us to factor $f=m\circ e$. We want to show that $m$ is mono. This needs two lemmas. First, that an arrow is mono iff the two legs of its kernel pair are equal. Second, that "pulling $e$ back along the kernel pairs of $f$ and $m$" (it needs to be made precise what that means) results in an epi.

[^compRegEpi]: This needs some work. One can show that, in a regular category, regular epis and strong epis coincide and then use that strong epis are closed under composition.

**Remark:** There are various other strengthenings of the notion of epi (which we will not need in the following), such as extremal epis and strong epis. In regular categories, strong epis and regular epis coincide. This is a step we will skip, but is useful to know, because strong epis are closed under composition but regular epis in general are not.

Let us recall from the exercises:

**Fact:** In a regular category every arrow can be factored into a regular epi followed by a mono.

## Relations

In any category $\mathcal C$, one can define a relation $R:A\to B$ as a monomorphic span. If $\mathcal C$ is regular, then one defines composition of relation via pullback and image factorisation. Moreover, due to regular epis being stable under pullbacks, the composition of relations is associative.


To summarize, for every regular category $\mathcal C$ there is the category of relations

$$\sf Rel\mathcal C.$$

**Exercise:** Define reflexive, symmetric, and transitive relations in $\mathcal C$.


**Theorem:** The Yoneda embedding $\mathcal C\to [\mathcal C^{op},Set]$ ... ... 

## Exact Categories

Early category was mostly category theory enriched over abelian groups (additive categories) and much of the category theory we know today was developed as a generalisation of the additive case. This is explicit in the original paper on exact categories:

![](https://hackmd.io/_uploads/B1gY7pTH2.png )

**Definition:** A regular category is **exact** if it has effective equivalence relations, that is, every equivalence relation is the kernel pair of its coequaliser. A functor is *exact* if it preserves finite limits and regular epis.

**Example:** We have already seen that quasi-varieties are regular. Quasi-varieties are typically not exact, but varieties are. In fact, it is not hard to see how effective equivalence relations corresponds to closure under homomorphic images.

**Example:** If $\mathcal C$ is regular, then the Yoneda embedding $\mathcal C\to [\mathcal C^{op},Set]$ is exact.

This means that one can transfer the usual set-theoretic proofs of properties of relations to all regular categories.


## References

For a textbook account on regular and exact categories see

- Borceux, Handbook of Categorical Algebra, Volume 2, 1994.

I also recommend the section on metatheorems in the introduction of

- Borceux, Bourn, *Mal’cev, protomodular, homological and semi-abelian categories*, 2004.

nLab has all definitions I skipped and also valuable further information. 
- https://ncatlab.org/nlab/show/regular+category
