---
layout: post 
author: utoppia
date: 2020-06-13
title: 2. Finite-Dimensional Vector Spaces
subtitle: <Linear Algebra Done Right>
tags: math linear-algebra-done-right
---

1. <span class='p-notation'> Notation </span> $\mathrm{F}, V$
> + $\mathrm{F}$ denotes $\mathrm{R}$ or $\mathrm{C}$.
> + $V$ denotes a vector space over $\mathrm{F}$.

### Span and Linear Independence 

2. <span class='p-notation'> Notation </span> ***list of vectors***
> We will usually write lists of vectors without surrounding parentheses.

3. <span class='p-definition'> Definition </span> ***linear combination***
> A ***linear combination*** of a list $v_1, \ldots, v_m$ of vectors in $V$ is a vector of the form \[ a_1v_1 + \dots + a_mv_m ,\] where $a_1, \ldots, a_m \in \mathrm{F}$.

5. <span class='p-definition'> Definition </span> ***span*** 
> The set of all linear combinations of a list of vectors $v_1, \ldots, v_m$ in $V$ is called the ***span*** of $v_1, \ldots, v_m$, denoted $\text{span}(v_1,\ldots, v_m)$. In other words, \[ \text{span}(v_1, \ldots, v_m) = \{ a_1v_1 + \dots + a_mv_m:a_1, \ldots, a_m \in \mathrm{F}\}. \] The span of the empty list $()$ is defined to be $\{0\}$.

7. Span is the smallest containing subspace 
> The span of a list of vectors in $V$ is the smallest subspace of $V$ containing all the vectors in the list.

8. <span class='p-definition'> Definition </span> ***spans***
> If $\text{span}(v_1, \ldots, v_m)$ equals $V$, we say that $v_1, \ldots, v_m$ ***spans*** $V$.

10. <span class='p-definition'> Definition </span> ***finite-dimensional vector space***
> A vector space is called ***finite-dimensional*** if some list of vectors in it spans the space.

11. <span class='p-definition'> Definition </span> ***polynomial***, $\mathcal{P}(\mathrm{F})$
> + A function $p: \mathrm{F} \to \mathrm{F}$ is called a ***polynomial*** with coeffecients in $\mathrm{F}$ if there exist $a_0, \ldots, a_m \in \mathrm{F}$ such that \[ p(z) = a_0 + a_1z + \dots + a_mz^m \] for all $z \in \mathrm{F}$.
> + $\mathcal{P}(\mathrm{F})$ is the set of all polynomials with coeffecients in $\mathrm{F}$.

12. <span class='p-definition'> Definition </span> ***degree of a polynomial***, $\text{deg }p$
> + A polynomial $p \in \mathcal{P}(\mathrm{F})$ is said to have ***degree*** $m$ if there exist scalars $a_0, \ldots, a_m \in \mathrm{F}$ with $a_m \neq 0$ such that \[ p(z) = a_0 + a_1z + \dots + a_mz^m \] for all $z \in \mathrm{F}$. If $p$ has degree $m$, we write $\text{deg }p = m$.
> + The polynomial that is identically $0$ is said to have degree $-\infty$.

13. <span class='p-definition'> Definition </span> $\mathcal{P}_m(\mathrm{F})$
> For $m$ a nonnegative integer, $\mathcal{P}_m(\mathrm{F})$ denote the set fo all polynomials with coeffecients in $\mathrm{F}$ and degree at most $m$.

15. <span class='p-definition'> Definition </span> ***infinite-dimensional vector space***
> A vector space is called ***infinite-dimensional*** if it is not finite-dimensional.

17. <span class='p-definition'> Definition </span> ***linear independent***
> + A list $v_1, \ldots, v_m$ of vectors in $V$ is called ***linear independent*** if the only choice of $a_1, \ldots, a_m \in \mathrm{F}$ that makes $a_1v_1 + \dots + a_mv_m$ equals $0$ is $a_1 = \dots = a_m = 0$.
> + The empty list $()$ is also declared to be linearly independent.

19. <span class='p-definition'> Definition </span> ***linearly dependent***
> + A list of vectors in $V$ is called ***linearly dependent*** if it is not linearly independent.
> + In other words, a list $v_1, \ldots, v_m$ of vectors in $V$ is liearly dependent if there exist $a_1, \ldots, a_m \in \mathrm{F}$, not all $0$, such that $a_1v_1 + \dots + a_mv_m = 0$.

21. Linear Dependence Lemma
> Suppose $v_1, \ldots, v_m$ is linearly dependent list in $V$. Then there exists $j \in \{1,2,\ldots,m\}$ such that the following hold:
    > (a). $v_j \in \text{span}(v_1, \ldots, v_{j-1})$;
    > (b). if the $j^{\text{th}}$ term is removed from $v_1, \ldots, v_m$, the span of the remaining list equals $\text{span}(v_1, \ldots, v_m)$.

23. Length of linearly independent list $\leq$ length of spanning list 
> In a finite-dimensional vector space, the length if every linearly independent list of vectors is less than or equal to the length to the length of every spanning list of vectors.

26. Finite-dimensional subspaces
> Every subspace of a finite-dimensional vector space if finite-dimensional.

### Bases 

27. <span class='p-definition'> Definition </span>***basis***
> A ***basis*** of $V$ is a list of vectors in $V$ that is linearly independent and spans $V$.

29. Criterion for basis 
> A list $v_1, \ldots, v_m$ of vectors in $V$ is a basis of $V$ if and only if every $v \in V$ can be written uniquely in the form \[ v = a_1v_1 + \dots + a_nv_n, \]
where $a_1, \ldots, a_n \in \mathrm{F}$.

31. Spanning list contains a basis 
> Every spanning list in a vector space can be reduced to a basis of the vector space.

32. Basis of finite-dimensional vector space 
> Every finite-dimensional vector space has a basis.

33. Linearly independent list extends to a basis
> Every linearly independent list of vectors in a finite-dimensional vector space can be extended to a basis of the vector space.

34. Every subspace if $V$ is part of a direct sum equal to $V$
> Suppose $V$ is finite-dimensional and $U$ is a subspace if $V$. Then there is a subspace $W$ of $V$ such that $V = U \oplus W$.

### Dimension

35. Basis length does not depend on basis 
> Any two bases of a finite-dimensional vector space have the same length.

36. <span class='p-definition'> Definition </span> ***dimension***, $\dim{V}$
> + The ***dimension*** of a finite-dimensional vector space is the length of any basis of the vector space.
> + The dimension of $V$ (if $V$ is finite-dimensional) is denoted by $\dim{V}$.

38. Dimension of a subspace
> If $V$ is finite-dimensional and $U$ is a subspace of $V$, then $\dim{U} \leq \dim{V}$.

39. Linearly independent list of the right length is a basis 
> Suppose $V$ is finite-dimensional. Then every linearly independent list of vectors in $V$ with length $\dim{V}$ is a basis of $V$.

42. Spanning list of the right length is a basis
> Suppose $V$ is finite-dimensional. Then every spanning list of vectors in $V$ with length $\dim{V}$ is a basis of $V$.


43. Dimension of a sum 
> If $U_1$ and $U_2$ are subspaces if a finite-dimensional vector space, then \[ \dim{(U_1 + U_2)} = \dim{U_1} + \dim{U_2} - \dim{(U_1 \cap U_2)}.\]