# Full or Faithful Adjoints

Let $F:X\to A$, $G:A\to X$, $F\dashv G$, $\eta_x:x\to GFx$, $\epsilon_a:FGa\to a$.

![](https://hackmd.io/_uploads/Hk_kNrB83.png =600x)


Mac Lane, page 88:

![](https://hackmd.io/_uploads/B1aZI1Sji.png)

This is proved using:

![](https://hackmd.io/_uploads/SJRXUJSos.png)

From the lemma we obtain the theorem

| counit componentwise | right adjoint|
|:---:|:---:|
|   epi |  faithful |
|  split mono | full |

and its dual

| unit componentwise| left adjoint|
|:---:|:---:|
|  mono | faithful |
| split epi | full |

as corollaries.

## The proof

For variety, we prove the dual of lemma and theorem.

**Lemma:** Let $f^\ast:X(-,y) \to X(-,z)$ given by Yoneda for $f:y\to z$. Then $f^\ast$ is componentwise injective iff $f$ is mono and $f^\ast$ is componentwise onto iff $f$ is split epi.

*Proof:* This is straightforward from the respective definitions.

To prove the dual of the theorem, consider
$$X(x,y)\stackrel {F_{x,y}} \longrightarrow 
A(Fx,Fy) \stackrel \cong \longrightarrow 
X(x,UFy)$$

which is the transformation natural in $x$ determined (via Yoneda) by the unit $\eta_y:y\to UFy$.

The lemma tells us that the natural transformation (hence $F_{x,y}$) is componentwise injective iff $\eta_y$ is mono and is componentwise surjective iff $\eta_y$ is split epi.

We have shown that $F$ is faithful iff the unit is componentwise mono and full iff the unit is componentwise split epi.

---

[Diagrams](https://q.uiver.app/#q=WzAsNixbMSwxLCJYIl0sWzMsMSwiQSJdLFswLDAsIngiXSxbMCwyLCJHRngiXSxbNCwwLCJGR2EiXSxbNCwyLCJhIl0sWzAsMSwiRiIsMCx7ImN1cnZlIjotMn1dLFsxLDAsIkciLDAseyJjdXJ2ZSI6LTJ9XSxbMCwxLCJcXGJvdCIsMSx7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFsyLDMsIlxcZXRhX3giLDFdLFs0LDUsIlxcdmFyZXBzaWxvbl9hIiwxXV0=)




