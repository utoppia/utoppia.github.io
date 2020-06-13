---
layout: post
author: utoppia 
date: 2020-06-13
title: 3. Linear Map
subtile: <Linear Algebra Done Right>
tags: math linear-algebra-done-right
---

### Linear Map
1. <span class='p-notation'> Notation </span> $\mathrm{F}, V, W$
> - $\mathrm{F}$ denotes $\mathrm{R}$ or $\mathrm{C}$.
> - $V$ and $W$ denote vector spaces over $\mathrm{F}$.
2. <span class='p-definition'> Definition </span>: linear map
> A ***linear map*** from $V$ to $W$ is a function $T: V \to W$ with the following properties:
    - **additicity** \[ T(u+v) = Tu + Tv \text{ for all } u,v\in V;\]
    - **homogeneity**: \[ T(\lambda v) = \lambda (Tv) \text{ for all } \lambda \in \mathrm{F} \text{ and all } v \in V.\]
3. <span class='p-notation'> Notation </span> $\mathcal{L}(V,W)
> The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$.
5. Linear maps and basis of domain
> Suppose $v_1, \ldots, v_n$ is a basis of $V$ and $w_1, \ldots, w_n \in W$. Then there exists a **unique** linear map $T:V \to W$ such that \[ Tv_j = w_j \] for each $j=1,\ldots,n$.
6. <span class='p-definition'> Definition </span>: addition and scalar multiplication on $\mathcal{L}(V,W)$
> Suppose $S,T \in \mathcal{L}(V,W)$ and $\lambda \in \mathrm{F}$. The ***sum*** $S+T$ and the ***product*** $\lambda T$ are the linear maps from $V$ to $W$ defined by \[ (S+T)(v) = Sv + Tv \quad \text{and} \quad (\lambda T)(v) = \lambda (Tv)\] for all $v \in V$.
7. $\mathcal{L}(V,W)$ is a vector space
> With the operations of addition and scalar multiplication as defined abvoe, $\mathcal{L}(V,W)$ is a vector space.
8. <span class='p-definition'> Definition </span> Product of Linear Maps
> If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{V,W}$, then the **product** $ST \in \mathcal{L}(U,W)$ is defined by \[ (ST)(u) = S(Tu)\] for $u \in U$.
9. Algebraic properties of products of linear maps
    - **associativity** \[ (T_1T_2)T_3 = T_1(T_2T_3) \]
    - **identity** \[ TI = IT = T\]
    - **distributive properties**: \[ (S_1+S_2)T = S_1T + S_2T \quad \text{ and }\quad S(T_1 + T_2) = ST_1 + ST_2\]
11. Linear maps take $0$ to $0$.
> Suppose $T$ is a linear map from $V$ to $W$. Then $T(0)=0$.

### Null Spaces and Ranges
13. <span class='p-definition'> Definition </span>: null space, $\text{null }T$
> For $T \in \mathcal{L}(V,W)$, the **null space** of $T$, denoted $\text{null }T$, is the subset of $V$ consisting of those vectors that $T$ maps to $0$: \[ \text{null }T = \{v \in V: Tv=0 \} .\]
14. The null space is a subspace 
> Suppose $T \in \mathcal{L}(V,W)$. Then $\text{null }T$ is a subspace of $V$.
15. <span class='p-definition'> Definition </span>: injective 
> A function $T: V \to W$ is called **injective** if $Tu = Tv$ implies $u=v$.
16. Injectivity is equivalent to null space equals $\{0\}$
> Let $T \in \mathcal{L}(V, W)$. Then $T$ is injective if and only if $\text{null } T = \{0\}$.
17. <span class='p-definition'> Definition </span>: range
> For $T$ a function from $V$ to $W$, the **range** of $T$ is the subset of $W$ consisting of those vectors that are of the form $Tv$ for some $v \in V$: \[ \text{range } T = \{Tv:v \in V\} .\]
19. The range is a subspace 
> If $T \in \mathcal{L}(V,W)$, then range $T$ is a subspace of $W$.

20. <span class='p-definition'> Definition </span>: surjective 
> A function $T: V \to M$ is called **surjective** if its range equals $W$.

22. **Fundamental Theorem of Linear Maps**
> Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V,W)$. Then range $T$ is finite-dimensional and \[ \dim{T} = \dim{\text{null }T} + \dim{\text{range }T}.\]
23. A map to a smaller dimensional space is not injective
> Suppose $V$ and $W$ are finite-dimensional vector space such that $\dim{T} > \dim{W}$. Then no linear map from $V$ to $W$ is injective.
24. A map to a larger dimensional space is not surjective
> Suppose $V$ and $W$ are finite-dimensional vector space such that $\dim{T} < \dim{W}$. Then no linear map from $V$ to $W$ is surjective.
26. Homogeneous system of linear equations
> A homogeneous system of linear equations with more variables than equations has nonzero solutions.
29. Inhomogeneous system of linear equations
> An inhomogeneous system of linear equations with more equations than variables has no solution for some choice of the constant terms.