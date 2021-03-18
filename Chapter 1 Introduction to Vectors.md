# Chapter 1 Introduction to Vectors

## 1.1 Vectors and Linear Combinations

Column vector $\vec{v}$.

### Linear Combinations

1. A vector $\vec{v}$ in two-dimensional space has two components $v_1$ and $v_2$. 
2. $\vec{v} + \vec{w} = ( v_1 + w_1, v_2 + w_2$) and $c\vec{v} = ( cv_1, cv_2)$ are found a component at a time.
3. A linear combination of three vectors $\vec{u}$ and $\vec{v}$ and $\vec{w}$ is $c\vec{u}+ d\vec{v} + e\vec{w}$.
4. Take all linear combinations of $\vec{u}$, or $\vec{u}$ and $\vec{v}$, or $\vec{u}$, $\vec{v}$, $\vec{w}$. In three dimensions, those combinations typically fill a line, then a plane, then the whole space $\mathbf{R}^3$ . 

## 1.2 Lengths and Dot Products

### Lengths and Unit Vectors

$$
\|\vec{v}\|=\sqrt{\vec{v}\cdot\vec{v}}=(\sum_{k=1}^n v_k^2)^{\frac{1}{2}}
$$

A unit vector $\vec{u}$ is a vector whose length equals one. Then $\vec{u} \cdot \vec{u} = 1$.

### The Angle Between Two Vectors

1. The dot product $\vec{v} \cdot \vec{w}$ multiplies each component $v_i$ by $w_i$ and adds all $viwi$. 
2. The length $\|\vec{v}\|$ is $\sqrt{\vec{v}\cdot\vec{v}}$. Then $\vec{u}=\vec{v}/\|\vec{v}\|$ is a unit vector: length 1.
3. The dot product is $\vec{v} \cdot \vec{w} = 0$ when vectors $\vec{v}$ and $\vec{w}$ are perpendicular.
4. The cosine of  the angle between any nonzero $\vec{v}$ and $\vec{w}$ never exceeds 1:

Cosine of the angle: $\cos\theta=\frac{\vec{v}\cdot\vec{u}}{\|\vec{v}\|\|\vec{u}\|}$

Schwarz inequality: $|\vec{v}\cdot\vec{u}|\le\|\vec{v}\|\|\vec{u}\|$ 

## 1.3 Matrices

### Linear Equations

### The Inverse Matrix

### Cyclic Differences

### Independence and Dependence

1. Matrix times vector: $A\vec{x}=$ combination of the columns of $A$.
2. The solution to $A\vec{x} = \vec{b}$ is $\vec{x} = A^{-1}\vec{b}$, when $A$ is an invertible matrix.
3. The cyclic matrix $C$ has no inverse. Its three columns lie in the same plane. Those dependent columns add to the zero vector. $C\vec{x} = \vec{0}$ has many solutions.
4. This section is looking ahead to key ideas, not fully explained yet~~~.







