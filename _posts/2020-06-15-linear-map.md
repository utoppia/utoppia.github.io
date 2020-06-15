---
layout: post
author: utoppia 
title: #### Linear Map
subtile: <Linear Algebra Done Right>
tags: math linear-algebra-done-right
---

### Linear Map
#### <span class='p-notation'> Notation </span> $\mathrm{F}, V, W$
- $\mathrm{F}$ denotes $\mathrm{R}$ or $\mathrm{C}$.
- $V$ and $W$ denote vector spaces over $\mathrm{F}$.

#### <span class='p-definition'> Definition </span> linear map
A ***linear map*** from $V$ to $W$ is a function $T: V \to W$ with the following properties:
    - **additicity** \[ T(u+v) = Tu + Tv \text{ for all } u,v\in V;\]
    - **homogeneity**: \[ T(\lambda v) = \lambda (Tv) \text{ for all } \lambda \in \mathrm{F} \text{ and all } v \in V.\]

#### <span class='p-notation'> Notation </span> $\mathcal{L}(V,W)$
The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$.

#### <span class="p-lemma"> Linear maps and basis of domain </span> 
Suppose $v_1 \ldots, v_n$ is a basis of $V$ and $w_1 \ldots, w_n \in W$. Then there exists a **unique** linear map $T:V \to W$ such that \[ Tv_j = w_j \] for each $j=1 \ldots,n$.

#### <span class='p-definition'> Definition </span>: addition and scalar multiplication on $\mathcal{L}(V,W)$
Suppose $S,T \in \mathcal{L}(V,W)$ and $\lambda \in \mathrm{F}$. The ***sum*** $S+T$ and the ***product*** $\lambda T$ are the linear maps from $V$ to $W$ defined by \[ (S+T)(v) = Sv + Tv \quad \text{and} \quad (\lambda T)(v) = \lambda (Tv)\] for all $v \in V$.

#### <span class="p-lemma"> $\mathcal{L}(V,W)$ is a vector space </span> 
With the operations of addition and scalar multiplication as defined abvoe, $\mathcal{L}(V,W)$ is a vector space.

#### <span class='p-definition'> Definition </span> Product of Linear Maps
If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{V,W}$, then the **product** $ST \in \mathcal{L}(U,W)$ is defined by \[ (ST)(u) = S(Tu)\] for $u \in U$.

#### <span class="p-lemma"> Algebraic properties of products of linear maps </span>
- **associativity** \[ (T_1T_2)T_3= T_1(T_2T_3) \]
- **identity** \[ TI = IT = T\]
- **distributive properties**: \[ (S_1 + S_2)T = S_1T + S_2T \quad \text{ and }\quad S(T_1+ T_2) = ST_1 + ST_2 \]

#### <span class="p-lemma"> Linear maps take $0$ to $0$ </span>
Suppose $T$ is a linear map from $V$ to $W$. Then $T(0)=0$.

### Null Spaces and Ranges
#### <span class='p-definition'> Definition </span>: null space, $\text{null }T$
For $T \in \mathcal{L}(V,W)$, the **null space** of $T$, denoted $\text{null }T$, is the subset of $V$ consisting of those vectors that $T$ maps to $0$: \[ \text{null }T = \{v \in V: Tv=0 \} .\]

#### <span class="p-lemma"> The null space is a subspace </span> 
Suppose $T \in \mathcal{L}(V,W)$. Then $\text{null }T$ is a subspace of $V$.

#### <span class='p-definition'> Definition </span>: injective 
A function $T: V \to W$ is called **injective** if $Tu = Tv$ implies $u=v$.

#### Injectivity is equivalent to null space equals $0$
Let $T \in \mathcal{L}(V, W)$. Then $T$ is injective if and only if $\text{null } T = 0$.

#### <span class='p-definition'> Definition </span>: range
For $T$ a function from $V$ to $W$, the **range** of $T$ is the subset of $W$ consisting of those vectors that are of the form $Tv$ for some $v \in V$: \[ \text{range } T = \{Tv:v \in V\} .\]
#### <span class="p-lemma"> The range is a subspace </span>
If $T \in \mathcal{L}(V,W)$, then range $T$ is a subspace of $W$.

#### <span class='p-definition'> Definition </span>: surjective 
A function $T: V \to M$ is called **surjective** if its range equals $W$.

#### <span class="p-lemma"> Fundamental Theorem of Linear Maps </span>
Suppose $V$ is finite-dimensional and $T \in \mathcal{L}(V,W)$. Then range $T$ is finite-dimensional and \[ \dim{T} = \dim{\text{null }T} + \dim{\text{range }T}.\]

#### <span class="p-lemma"> A map to a smaller dimensional space is not injective </span>
Suppose $V$ and $W$ are finite-dimensional vector space such that $\dim{T} > \dim{W}$. Then no linear map from $V$ to $W$ is injective.

#### <span class="p-lemma"> A map to a larger dimensional space is not surjective </span>
Suppose $V$ and $W$ are finite-dimensional vector space such that $\dim{T} < \dim{W}$. Then no linear map from $V$ to $W$ is surjective.

#### <span class="p-lemma"> Homogeneous system of linear equations </span>
A homogeneous system of linear equations with more variables than equations has nonzero solutions.

#### <span class="p-lemma"> Inhomogeneous system of linear equations </span>
An inhomogeneous system of linear equations with more equations than variables has no solution for some choice of the constant terms.

### Matrices 

#### <span class="p-definition"> Definition </span> ***matrix*** $A_{j,k}$

Let $m$ and $n$ denote positive integers. An $m$-by-$n$ ***matrix*** $A$ is rectangular array of element of $\mathrm{F}$ with $m$ rows and $n$ columns: 

$$
    A = 
    \begin{pmatrix}
        A_{1,1} & \ldots & A_{1,n} \\
        \vdots & ~ & \vdots \\
        A_{m,1} & \ldots & A_{m,n}
    \end{pmatrix}
$$

The notation $A_{j,k}$ denotes the entry in row $j$, column $k$ of $A$. In other words, the first index refers to the row number and the second index refers to the column number.

#### <span class="p-definition"> Definition </span> ***matrix of a linear map***, $\mathcal{M}(T)$

Suppose $T \in \mathcal{L}(V,W)$ and $v_1 \ldots, v_n$ is a basis of $V$ and $w_1 \ldots, w_m$ is a basis of $W$. The ***matrix of*** $T$ with respect to these bases is the $m$-by-$n$ matrix $\mathcal{M}(T)$ whose entries $A_{j,k}$ are defined by 

\[ Yv_k = A_{1,k}w_1+ \dots + A{m,k}w_m. \] 

If the bases are not clear from the context, then the notation $\mathcal{M}\left(T, (v_1 \ldots, v_n), (w_1 \ldots, w_m)\right)$ is used.

#### <span class="p-definition"> Definition </span> ***matrix addition***

The ***sum of two matrices of the same size*** is the matrix obtained by adding corresponding entries in the matrices:

$$
\begin{pmatrix} 
A_{1,1} & \ldots & A_{1,n} \\
\vdots & ~ & \vdots \\
A_{m,1} & \ldots & A_{m,n}
\end{pmatrix} + 
\begin{pmatrix}
C_{1,1} & \ldots & C_{1,n} \\
\vdots & ~ & \vdots \\
C_{m,1} & \ldots & C_{m,n} 
\end{pmatrix} = 
\begin{pmatrix}
    A_{1,1} + C_{1,1} & \ldots & A_{1,n} + C_{1,n} \\
    \vdots & ~ & \vdots \\
    A_{m,1} + C_{m,1} & \ldots & A_{m,n} + C_{m,n}
\end{pmatrix}.
$$

In other words, $$(A+C)_{j,k} = A_{j,k} + C_{j,k}$$.

#### <span class="p-lemma"> The matrix of the sum of linear maps </span>

Suppose $S, T \in \mathcal{L}(V,W)$. Then $\mathcal{M}(S+T) = \mathcal{M}(S) + \mathcal{M}(T)$.


#### <span class="p-definition"> Definition </span> ***scalar multiplication of a matrix***

The product of a scalar and a matrix is the matrix obtained by multiplying each entry in the matrix by the scalar:

$$
    \lambda 
    \begin{pmatrix}
        A_{1,1} & \ldots & A_{1,n} \\
        \vdots & ~ & \vdots \\
        A_{m,1} & \ldots & A_{m,n}
    \end{pmatrix} = 
    \begin{pmatrix} 
        \lambda A_{1,1} & \ldots & \lambda A_{1,n} \\
        \vdots & ~ & \vdots \\
        \lambda A_{m,1} & \ldots & \lambda A_{m,n}
    \end{pmatrix}.
$$

In other words, $$(\lambda A)_{j,k} = \lambda A_{j,k}$$.

#### <span class="p-lemma"> The matrix of a scalar times a linear map </span>

Suppose $\lambda \in \mathrm{F}$ and $T \in mathcal{L}(V,W)$. Then $\mathcal{M}(\lambda T) = \lambda \mathcal{M}(T)$.

#### <span class="p-notation"> Notation </span> $\mathrm{F}^{m,n}$

For $m$ and $n$ positive integers, the set of all $m$-by-$n$ matrices with entries in $\mathrm{F}$ is denoted by $\mathrm{F}^{m,n}$.

#### <span class="p-lemma"> $\dim{\mathrm{F}^{m,n}} = mn$ </span>

Suppose $m$ and $n$ are positive integers. With addition and scalar multiplication defined as above, $\mathrm{F}^{m,n}$ is a vector space with dimension $mn$.

#### <span class="p-definition"> Definition </span> ***matrix multiplication***

Suppose $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix. Then $AC$ is defined to be the $m$-by-$p$ matrix whose entry in row $j$, column $k$, is given by the following equation:

$$ (AC)_{j,k} = \sum_{r=1}^{n} A_{j,r}C_{r,k}. $$

In other words, the entry in row $j$, column $k$, of $AC$ is computed by taking row $j$ of $A$ and column $k$ of $C$, multiplying together corresponding entries, and then summing.

#### <span class="p-lemma"> The matrix of the product of linear maps </span>

If $T \in \mathcal{L}(U,V)$ and $S \in \mathcal{L}(V,W)$, then $\mathcal{M}(ST) = \mathcal{M}(S)\mathcal{M}(T)$.

#### <span class="p-notation"> Notation </span> $A_{j,\cdot}$, $A_{\cdot,k}$

Suppose $A$ is an $m$-by-$n$ matrix.

- If $1 \leq j \leq m$, then $A_{j, \cdot}$ denotes the $1$-by-$n$ matrix consisting of row $j$ of $A$.
- If $1 \leq k \leq n$, then $A_{\cdot, k}$ denotes the $m$-by-$1$ matrix consisting of column $k$ of $A$.

#### <span class="p-lemma"> Entry of matrix product equals row times column </span>

Suppose $A$ is an $m$-by-$n$ matrix and $C$ is an $n$-by-$p$ matrix. Then 

$$ (AC)_{j,k} = A_{j,\cdot} C_{\cdot,k} $$

for $1 \leq j \leq m$ and $1 \leq k \leq p$.

#### <span class="p-lemma"> Column of matrix product equals matrix times column </span>

Suppose $A$ is an $m$-y-$n$ matrix and $C$ is an $n$-by-$p$ matrix. Then 

\[ (AC){\cdot, k} = AC_{\cdot, k} \]

for $1 \leq k \leq p$.

#### <span class="p-lemma"> Linear combination of columns </span>

Suppose $A$ is an $m$-by-$n$ matrix and $$c = \begin{pmatrix} c_1 \\ \vdots \\ c_n \end{pmatrix}$$ is an $n$-by-$1$ matrix. Then 

\[ Ac = c_1A_{\cdot,1} + \dots + c_n A_{\cdot, n}. \]

In other words, $Ac$ is a linear combination of the columns of $A$, with scalars that multiply the columns coming from $c$.