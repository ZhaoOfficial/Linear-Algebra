# Chapter 4 广义线性空间 General Vector Spaces

## 4.1 实线性空间 Real Vector Spaces

### DEFINITION 1

Let $V$ be an arbitrary nonempty set of objects on *which two* operations are defined: *addition*, and *multiplication* by numbers called scalars. By addition we mean a rule for associating with each pair of objects $\mathbf u$ and $\mathbf v$ in $V$ an object $\mathbf u + \mathbf v$, called the sum of $\mathbf u$ and $\mathbf v$; by scalar multiplication we mean a rule for associating with each scalar $k$ and each object $\mathbf u$ in $V$ an object $k\mathbf u$, called the scalar multiple of $\mathbf u$ by $k$. **If the following 10 axioms are satisfied by all objects $\mathbf u$, $\mathbf v$, $\mathbf w$ in $V$ and all scalars $k$ and $m$, then we call $V$ a vector space and we call the objects in $V$ vectors.**

1. If $\mathbf u$ and $\mathbf v$ are objects in $V$, then $\mathbf u + \mathbf v$ is in $V$
2. $\mathbf u + \mathbf v = \mathbf v + \mathbf u$
3. $\mathbf u + (\mathbf v + \mathbf w) = (\mathbf u + \mathbf v) + \mathbf w$
4. There is an object $\mathbf 0$ in $V$, called a zero vector for $V$, such that $\mathbf 0 + \mathbf u = \mathbf u + \mathbf 0 = \mathbf u$ for all u in $V$.
5. For each $\mathbf u$ in $V$, there is an object $−\mathbf u$ in $V$, called a negative of $\mathbf u$, such that $\mathbf u + (−\mathbf u) = (−\mathbf u) + \mathbf u = \mathbf 0$
6. If $k$ is any scalar and $\mathbf u$ is any object in $V$, then $k\mathbf u$ is in $V$
7. $k(\mathbf u + \mathbf v) = k\mathbf u + k\mathbf v$
8. $(k + m)\mathbf u = k\mathbf u + m\mathbf u$
9. $k(m\mathbf u) = (km)(\mathbf u)$
10. $1\mathbf u = \mathbf u$

Any kind of object can be a vector, and the operations of addition and scalar multiplication need not have any relationship to those on $\mathbb R^n$. The only requirement is that the ten vector space axioms be satisfied.

> $\{\mathbf 0\}$, $\mathbb R^n$, $\mathbb R^{\infty}$, $m\times n$ matrix, real valued functions are vector space.

### THEOREM 4.1.1

Let $V$ be a vector space, $\mathbf u$ a vector in $V$, and $k$ a scalar; then:

1. $0\mathbf u = \mathbf 0$
2. $k\mathbf 0 = \mathbf 0$
3. $(−1)\mathbf u = −\mathbf u$
4. If $k\mathbf u = 0$, then $k = 0$ or $\mathbf u = 0$.

## 4.2 子空间 Subspaces

### DEFINITION 1

A subset $W$ of a vector space $V$ is called a subspace of $V$ if $W$ is itself a vector space under the addition and scalar multiplication defined on $V$.

In general, to show that a nonempty set $W$ with two operations is a vector space one must verify the ten vector space axioms. However, if $W$ is a subspace of a known vector space $V$, then certain axioms need not be verified because they are "inherited" from $V$.

### THEOREM 4.2.1

If $W$ is a set of one or more vectors in a vector space $V$, then $W$ is a subspace of $V$ if and only if the following conditions are satisfied.

1. If $\mathbf u$ and $\mathbf v$ are vectors in $W$, then $\mathbf u+\mathbf v$ is in $W$.
2. If $k$ is a scalar and $\mathbf u$ is a vector in $W$, then $k\mathbf u$ is in $W$.

> $\{\mathbf 0\}$ for any space, lines, planes through origin for $\mathbb R^n$,  continuous functions with Continuous Derivatives on $(-\infty, \infty)$ for function on $(-\infty, \infty)$, polynomials for polynomials are corresponding subspaces.
>
> $F(-\infty, \infty)\supset C(-\infty, \infty)\supset C^1(-\infty, \infty)\supset C^n(-\infty, \infty)\supset C^{\infty}(-\infty, \infty)\supset P_n$

### THEOREM 4.2.2

If $W_1, W_2,\dots,W_r$ are subspaces of a vector space $V$, then the intersection of these subspaces is also a subspace of $V$.

### DEFINITION 2

If $\mathbf w$ is a vector in a vector space $V$, then $\mathbf w$ is said to be a 线性组合 *linear combination* of the vectors $\mathbf v_1, \mathbf v_2,\dots, \mathbf v_r$ in $V$ if $\mathbf w$ can be expressed in the form $\mathbf w = k_1\mathbf v_1 + k_2\mathbf v_2 +\dots+ k_r\mathbf v_r$ where $k_1, k_2,\dots,k_r$ are scalars. These scalars are called the 系数 *coefficients* of the linear combination.

### THEOREM 4.2.3

If $S = {\mathbf w_1, \mathbf w_2,\dots, \mathbf w_r}$ is a nonempty set of vectors in a vector space $V$, then:

1. The set $W$ of all possible linear combinations of the vectors in $S$ is a subspace of $V$.
2. The set $W$ in part(a)is the “smallest” subspace of $V$ that contains all of the vectors in $S$ in the sense that any other subspace that contains those vectors contains $W$.

#### Proof

##### 1

$W$ is closed under addition and











