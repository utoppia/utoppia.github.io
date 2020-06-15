---
layout: post
author: utoppia
title: #### Vector Spaces
subtitle: <Linear Algebra Done Right>
tags: math linear-algebra-done-right
---

### $\mathrm{R}^n$ and $\mathrm{C}^n$
{: .section}

#### <span class='p-definition'> Definition </span> complex numbers 
+ A **complex number** is an ordered pair $(a,b)$, where $a,b \in \mathrm{R}$, but we will write this as $a + bi$.
+ The set of all complex numbers is denoted by $\mathrm{C}$: \[\mathrm{C} = \{ a+bi: a,b \in \mathrm{R} \}.\]
+ ***Addition and multiplication*** on $\mathrm{C}$ are defined by \[ (a+bi) + (c+di) = (a+c) + (b+d)i, \] \[ (a+bi)(c+di) = (ac-bd) + (ad+bc)i; \] here $a,b,c,d \in \mathrm{R}$.

#### <span class="p-lemma"> Properties of complex arithmetic </span>
+ **commuttivity** \[ \alpha + \beta = \beta + \alpha \quad \text{and} \quad \alpha \beta = \beta \alpha \quad \text{for all} \quad \alpha, \beta \in \mathrm{C}; \]
+ **associativity** \[ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) \quad \text{and} \quad (\alpha \beta) \lambda = \alpha (\beta \lambda) \quad \text{for all} \quad \alpha, \beta, \lambda \in \mathrm{C}; \]
+ **identities** \[ \lambda + 0 = \lambda \quad \text{and} \quad \lambda 1 = \lambda \quad \text{for all} \quad \lambda \in \mathrm{C}; \]
+ **additive inverse** \[ \text{for every } \alpha \in \mathrm{C} \text{ with } \alpha \neq 0, \text{ there exists a unique } \beta \in \mathrm{C} \text{ such that } \alpha \beta = 1;  \]
+ **distributive property** \[ \lambda (\alpha + \beta) = \lambda \alpha + \lambda \beta \quad \text{for all} \quad \lambda, \alpha, \beta \in \mathrm{C}. \]

#### <span class='p-definition'> Definition </span> $-\alpha$, ***substraction***, $1/\alpha$, ***division***
Let $\alpha, \beta \in \mathrm{C}$.
+ Let $-\alpha$ denote the additive inverse of $\alpha$. Thus $-\alpha$ is the unique complex number such that \[ \alpha + (-\alpha) = #### \]
+ **Subtraction** on $\mathrm{C}$ is defined by \[ \beta - \alpha = \beta + (-\alpha). \]
+ For $\alpha \neq 0$, let $1/\alpha$ denote the multiplicative inverse of $\alpha$. Thus $1/\alpha$ is the unique complex number such that \[ \alpha(1/\alpha) = #### \]
+ **Divition** on $\mathrm{C}$ is defined by \[ \beta / \alpha = \beta (1/\alpha). \]

#### <span class="p-notation"> Notation </span> $\mathrm{F}$
$\mathrm{F}$ stands for either $\mathrm{R}$ or $\mathrm{C}$.
#### <span class='p-definition'> Definition </span> ***list, length***
Suppose $n$ is a nonnegative integer. A ***list*** of ***length*** $n$ is an ordered collection of $n$ elements (which might be numbers, other lists, or more abstract entries) separated by commas and surrounded by parentheses. A list of length $n$ looks like this: \[ (x_1, \ldots, x_n). \] Two lists are equal if and only if they have the same length and the same elements in the same order.

#### <span class='p-definition'> Definition </span> $\mathrm{F}^n$
$\mathrm{F}^n$ is the set of all lists of length $n$ of elements of $\mathrm{F}^n$: \[ \mathrm{F}^n = \{(x_1,\ldots,x_n):x_j \in \mathrm{F} \text{ for } j=1, \ldots, n \}. \] For $(x_1, \ldots, x_n) \in \mathrm{F}^n$ and $j \in \{1,\ldots,n\}$, we say that $x_j$ is the $j^{\text{th}}$ ***coordinate*** of $(x_1, \ldots, x_n)$.

#### <span class='p-definition'> Definition </span> ***addition in*** $\mathrm{F}^n$
***Addition*** in $\mathrm{F}^n$ is defined by adding corresponding coordinates: \[ (x_1,\ldots,x_n) + (y_1, \ldots, y_n) = (x_1 +y_1, \ldots, x_n + y_n). \]

#### <span class="p-lemma"> Commutativity of addition in $\mathrm{F}^n$ </span>
If $x, y \in \mathrm{F}^n$, then $x + y = y + x$.

#### <span class='p-definition'> Definition $0$
Let $0$ denote the list of length $n$ whose coordinates are all $0$: \[ 0 = (0,\ldots,0). \]

#### <span class='p-definition'> Definition ***additive inverse in*** $\mathrm{F}^n$
For $x \in \mathrm{F}^n$, the ***additive inverse*** of $x$, denoted $-x$, is the vector $-x \in \mathrm{F}^n$ such that \[ x + (-x) = #### \] 

#### <span class='p-definition'> Definition ***scalar multiplication in*** $\mathrm{F}^n$
The ***product*** of a number $\lambda$ and a vector in $\mathrm{F}^n$ is computed by multiplying each coordinate of the vector by $\lambda$: \[ \lambda(x_1, \ldots, x_n) = (\lambda x_1, \ldots, \lambda x_n); \] here $\lambda \in \mathrm{F}$ and $(x_1,\ldots, x_n) \in \mathrm{F}^n$.

### Definition of Vector Space 
{: .section}

#### <span class='p-definition'> Definition </span> ***addition, scalar multiplication***
+ An ***addition*** on a set $V$ is a funtion that assigns an element $u + v \in V$ to each pair of elements $u, v \in V$.
+ A ***scalar multiplication*** on a set $V$ is a function that assigns an element $\lambda v \in V$ to each $\lambda \in \mathrm{F}$ and each $v \in V$.

#### <span class='p-definition'> Definition </span> ***vector space***
A ***vector space*** is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$ such that the following properties hold:
+ **commutativity** \[ u + v = v + u \quad \text{for all} \quad u,v \in V; \]
+ **associativity** \[ (u+v) + w = u + (v+w) \quad \text{for all} \quad u,v,w \in V,\] \[ (ab)v = a(bv) \quad \text{for all} \quad a,b\in \mathrm{F} \text{ and } v \in V. \]
+ **additive identity**
    > there exists an element $0 \in V$ such that $v + 0 = v$ for all $v \in V$;
+ **additive inverse** 
    > for every $v \in V$, there exists $w \in V$ such that $v + w = 0$;
+ **multiplicative identity**
    > $1v = v$ for all $v \in V$;
+ **distributive properties**
    > $a(u+v) = au + av$ and $(a+b)v = av + bv$ for all $a,b \in \mathrm{F}$ and all $u,v \in V$.

#### <span class='p-definition'> Definition </span> ***vector, point***
Elements of a vector space are called ***vectors** or ***points***.

#### <span class='p-definition'> Definition </span> ***real vector space, complex vector space***
+ A vector space over $\mathrm{R}$ is called ***real vector space***.
+ A vector space over $\mathrm{C}$ is called ***complex vector space***.

#### <span class='p-notation'> Notation </span> $\mathrm{F}^S$
+ If $S$ is a set, then $\mathrm{F}^S$ denotes the set of functions from $S$ to $\mathrm{F}$.
+ For $f, g \in \mathrm{F}^S$, the ***sum*** $f + g \in \mathrm{F}^S$ is the function defined by \[ (f+g)(x) = f(x) + g(x) \] for all $x \in S$.
+ For $\lambda \in \mathrm{F}$ and $f \in \mathrm{F}^S$, the ***product*** $\lambda f \in \mathrm{F}^S$ is the function defined by \[ (\lambda f)(x) = \lambda f(x) \] for all $x \in S$.

#### <span class="p-lemma"> Unique additive identity  </span>
A vector space has a unique additive identity.

#### <span class="p-lemma"> Unique additive inverse </span>
Every element in a vector space has a unique additive inverse.

#### <span class='p-notation'> Notation </span>$-v, w-v$
Let $v, w \in V$. Then 
+ $-v$ denotes the additive inverse of $v$;
+ $w - v$ is defined to be $w + (-v)$.

#### <span class='p-notation'> Notation </span> $V$
$V$ denotes a vector space over $\mathrm{F}$.

#### <span class="p-lemma"> The number $0$ times a vector  </span>
$0 v = 0$ for every $v \in V$.

#### <span class="p-lemma"> A number times the vector $0$ </span>
$a0 = 0$ for every $a \in \mathrm{F}$.

#### <span class="p-lemma"> The number $-1$ times a vector </span>
$(-1)v = -v$ for every $v \in V$.

### Subspaces
{: .section}

#### <span class='p-definition'> Definition </span> ***subspace***
A subset $U$ of $V$ is called ***subspace*** of $V$ if $U$ is also a vector space (using the same addition and scalar multiplication as on $V$).

#### <span class="p-lemma"> Conditions for a subspace </span>
A subset $U$ of $V$ is a subspace of $V$ if and only if $U$ satisfies the following three conditions:
+ **additive identity** 
    
    \[ 0 \in U \]

+ **closed under addition**
    
    $u, w \in U$ implies $u + w \in U$;

+ **closed undert scalar multiplication**
    
    $a \in \mathrm{F}$ and $u \in U$ implies $au \in U$.

#### <span class='p-definition'> Definition </span> ***sum of subsets***
Suppose $U_1, \ldots, U_m$ are subsets of $V$. The ***sum*** of $U_1,\ldots, U_m$, denoted $U_1 + \dots + U_m$, is the set of all posible sums of elements of $U_1, \ldots, U_m$. More precisely, \[ U_1 + \dots + U_m = \{u_1+\dots+u_m:u_1 \in U_1, \ldots, u_m \in U_m\}. \]

#### <span class="p-lemma"> Sum of subspaces is the smallest containing subspace </span> 
Suppose $U_1, \ldots, U_m$ are subspaces of $V$. Then $U_1 + \dots + U_m$ is the smallest subspace of $V$ containing $U_1, \ldots, U_m$.

#### <span class='p-definition'> Definition </span> ***direct sum***
Suppose $U_1, \ldots, U_m$ are subspaces of $V$.
+ The sum $U_1 + \dots + U_m$ is called ***direct sum*** if each element of $U_1 + \dots + U_m$ can be written in only one way as a sum $u_1 + \dots + u_m$, where each $u_j$ is in $U_j$.
+ If $U_1 + \dots + U_m$ is a direct sum, then $U_1 \oplus \dots \oplus U_m$ denotes $U_1 + \dots + U_m$, with $\oplus$ notation serving as an indication that this is a direct sum.

#### <span class="p-lemma"> Condition for a direct sum </span> 
Suppose $U_1, \ldots, U_m$ are subspaces of $V$. Then $U_1 + \dots + U_m$ is a direct sum if and only if the only way to write $0$ as a sum $u_1 + \dots + u_m$, where each $u_j$ is in $U_j$, is taking each $u_j$ equal to $0$.

#### <span class="p-lemma"> Direct sum of two subspaces </span>
Suppose $U$ and $W$ are subspaces of $V$. Then $U + W$ is a direct sum if and only if $U \cap W = \{0\}$.
