# Chapter 6 Inner Product Spaces

## 6.1 内积 Inner Products

### DEFINITION 1

An inner product on a **real vector** space $V$ is a function that associates a real number $\langle\mathbf u, \mathbf v\rangle$ with each pair of vectors in $V$ in such a way that the following axioms are satisfied for all vectors $\mathbf u$, $\mathbf v$, and $\mathbf w$ in $V$ and all scalars $k$.

1. $\langle\mathbf u, \mathbf v\rangle$ [ Symmetry axiom]
2. $\langle\mathbf u+\mathbf v,\mathbf w\rangle=\langle\mathbf u, \mathbf w\rangle+\langle\mathbf v, \mathbf w\rangle$ [ Additivity axiom]
3. $\langle k\mathbf u, \mathbf v\rangle = k\langle\mathbf u, \mathbf v\rangle$ [Homogeneity axiom]
4. $\langle\mathbf v, \mathbf v\rangle \ge 0$ and $\langle\mathbf v, \mathbf v\rangle = 0$ if and only if $\mathbf v = \mathbf 0$ [Positivity axiom]

A real vector space with an inner product is called a 实内积空间 *real inner product space*.

### DEFINITION 2

If $V$ is a real inner product space, then the *norm* of a vector $\mathbf v$ in $V$ is denoted by $\|\mathbf v\|$ and is defined by
$$
\|\mathbf v\|=\sqrt{\langle\mathbf v,\mathbf v\rangle}
$$
and the *distance* between two vectors is denoted by $d(\mathbf u, \mathbf v)$ and is defined by
$$
d(\mathbf u, \mathbf v)=\|\mathbf u-\mathbf v\|=\sqrt{\langle\mathbf u-\mathbf v,\mathbf u-\mathbf v\rangle}
$$
A vector of norm $1$ is called a *unit vector*.

### THEOREM 6.1.1

If $\mathbf u$ and $\mathbf v$ are vectors in a real inner product space $V$, and if $k$ is a scalar, then:

1. $\|\mathbf v\|\ge0$ with equality if and only if $\mathbf v = 0$
2. $\|k\mathbf v\|=|k|\|\mathbf v\|$
3. $d(\mathbf u, \mathbf v) = d(\mathbf v, \mathbf u)$
4. $d(\mathbf u, \mathbf v) \ge 0$ with equality if and only if $\mathbf v=\mathbf u$

### DEFINITION 3

If $V$ is an inner product space, then the set of points in V that satisfy $\|\mathbf u\|=1$ is called the *unit sphere* or sometimes the *unit circle* in $V$.

