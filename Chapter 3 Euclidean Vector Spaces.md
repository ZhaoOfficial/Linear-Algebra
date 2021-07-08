# Chapter 3 Euclidean Vector Spaces

## 3.1 二维三维 n 维空间的向量 Vectors in 2-Space, 3-Space, and n-Space

Vector is a directed arrow.

$\mathbf v + \mathbf w$ is the translation of $\mathbf v$ by $\mathbf w$ or the translation of $\mathbf w$ by $\mathbf v$.
$$
\mathbf v+\mathbf w=\mathbf w+\mathbf v
$$

$$
\mathbf w − \mathbf v = \mathbf w + (−\mathbf v)
$$

### THEOREM 3.1.1

If $\mathbf u$, $\mathbf v$, and $\mathbf w$ are vectors in $\mathbb R^n$, and if $k$ and $m$ are scalars, then:

1. $\mathbf u + \mathbf v = \mathbf v + \mathbf u$
2. $(\mathbf u + \mathbf v) + \mathbf w = \mathbf u + (\mathbf v + \mathbf w)$
3. $\mathbf u + \mathbf 0 = \mathbf 0 + \mathbf u = \mathbf u$
4. $\mathbf u + (−\mathbf u) = \mathbf 0$
5. $k(\mathbf u + \mathbf v) = k\mathbf u + k\mathbf v$
6. $(k + m)\mathbf u = k\mathbf u + m\mathbf u$
7. $k(m\mathbf u) = (km)\mathbf u$
8. $1\mathbf u = \mathbf u$

### THEOREM 3.1.2

If $\mathbf v$ is a vector in $\mathbb R^n$ and $k$ is a scalar, then:

1. $0\mathbf v = \mathbf 0$
2. $k\mathbf 0 = \mathbf 0$
3. $(−1)\mathbf v = −\mathbf v$

### DEFINITION 4

If $\mathbf w$ is a vector in $\mathbb R^n$, then $\mathbf w$ is said to be a linear combination of the vectors $\mathbf v1, \mathbf v2,\dots, \mathbf vr$ in $\mathbb R^n$ if it can be expressed in the form $\mathbf w = k_1\mathbf v_1 + k_2\mathbf v_2 +\dots+k_r \mathbf v_r$ where $k_1, k_2,\dots, k_r$ are scalars. These scalars are called the coefficients of the linear combination.

## 3.2 范数，点乘和距离 Norm, Dot Product, and Distance in $\mathbb R^n$

### DEFINITION 1

If $\mathbf v = (\mathbf v_1, \mathbf v_2,\dots, \mathbf v_n)$ is a vector in $\mathbb R^n$, then the norm of $\mathbf v$ is denoted by $\|\mathbf v\|$, and is defined by the formula 
$$
\|\mathbf v\|=\sqrt{\sum_{i=1}^nv_i^2}
$$

### THEOREM 3.2.1

If $\mathbf v$ is a vector in $\mathbb R^n$, and if $k$ is any scalar, then:

1. $\|\mathbf v\|\ge0$
2. $\|\mathbf v\|=0$ if and only if $\mathbf v=\mathbf 0$
3. $\|k\mathbf v\|=|k|\|\mathbf v\|$

### 单位向量 Unit Vectors

A vector of norm 1 is called a unit vector.
$$
\mathbf u=\frac{1}{\|\mathbf v\|}\mathbf v
$$

### 标准单位向量 The Standard Unit Vectors

The unit vectors in the positive directions of the coordinate axes are called the standard unit vectors. The standard unit vectors in $\mathbb R^n$ are
$$
\mathbf e_1=(1, 0,\dots,0),\mathbf e_2=(0, 1,\dots,0),\dots,\mathbf e_n=(0, 0,\dots,1),
$$

### DEFINITION 2

If $\mathbf u = (u_1, u_2,\dots, u_n)$ and $\mathbf v = (v_1, v_2,\dots, v_n)$ are points in $\mathbb R^n$, then we denote the distance between $\mathbf u$ and $\mathbf v$ by $d(\mathbf u, \mathbf v)$ and define it to be
$d(\mathbf u, \mathbf v) = \|\mathbf u − \mathbf v\| =\sqrt{(u_1 − v_1)^2 + (u_2 − v_2)^2 +\dots+(u_n − v_n)^2}$

### Dot Product

If $\mathbf u$ and $\mathbf v$ are nonzero vectors in $\mathbb R^2$ or $\mathbb R^3$, and if $\theta$ is the angle between $\mathbf u$ and $\mathbf v$, then the dot product (also called the Euclidean inner product) of $\mathbf u$ and $\mathbf v$ is denoted by $\mathbf u\cdot \mathbf v$ and is defined as
$$
\mathbf u\cdot\mathbf v=\|\mathbf u\|\|\mathbf v\|\cos\theta=\sum_{i=1}^n u_iv_i
$$
If $\mathbf u = 0$ or $\mathbf v = 0$, then we define $\mathbf u\cdot \mathbf v$ to be $0$.

$$
\cos\theta=\frac{\mathbf u\cdot\mathbf v}{\|\mathbf u\|\|\mathbf v\|}
$$

### THEOREM 3.2.2

If $\mathbf u$, $\mathbf v$, and $\mathbf w$ are vectors in $\mathbb R^n$, and if $k$ is a scalar, then:

1. $\mathbf u\cdot\mathbf v = \mathbf v\cdot\mathbf u$ [Symmetry property]
2. $\mathbf u \cdot (\mathbf v + \mathbf w) = \mathbf u \cdot \mathbf v + \mathbf u \cdot \mathbf w$ [Distributive property]
3. $k(\mathbf u \cdot \mathbf v) = (k\mathbf u) \cdot \mathbf v$ [Homogeneity property]
4. $\mathbf v \cdot \mathbf v ≥ 0$ and $\mathbf v \cdot \mathbf v = 0$ if and only if $\mathbf v = \mathbf 0$ [Positivity property]

### THEOREM 3.2.3

If $\mathbf u$, $\mathbf v$, and $\mathbf w$ are vectors in $\mathbb R^n$, and if $k$ is a scalar, then:

1. $\mathbf 0 \cdot \mathbf v = \mathbf v \cdot \mathbf 0 = 0$
2. $(\mathbf u + \mathbf v)  \cdot \mathbf w = \mathbf u  \cdot \mathbf w + \mathbf v  \cdot \mathbf w$
3. $\mathbf u \cdot (\mathbf v − \mathbf w) = \mathbf u \cdot \mathbf v − \mathbf u \cdot \mathbf w$
4. $(\mathbf u − \mathbf v) \cdot \mathbf w = \mathbf u \cdot \mathbf w − \mathbf v \cdot \mathbf w$
5. $k(\mathbf u \cdot \mathbf v) = \mathbf u \cdot (k\mathbf v)$

### Cauchy–Schwarz Inequality and Angles in $\mathbb R^n$

Since
$$
-1\le\theta=\arccos(\frac{\mathbf u\cdot\mathbf v}{\|\mathbf u\|\|\mathbf v\|})\le1
$$

### THEOREM 3.2.4 Cauchy–Schwarz Inequality

If $\mathbf u = (u_1, u_2,\dots, u_n)$ and $\mathbf v = (v_1, v_2,\dots, v_n)$ are points in $\mathbb R^n$, then
$$
|\mathbf u\cdot\mathbf v|\le\|\mathbf u\|\|\mathbf v\|\\
(\sum_{i=1}^nu_iv_i)^2\le(\sum_{i=1}^nu_i^2)(\sum_{i=1}^nv_i^2)
$$

### THEOREM 3.2.5

If $\mathbf u$, $\mathbf v$, and $\mathbf w$ are vectors in $\mathbb R^n$, then:

1. $\|\mathbf u+\mathbf v\|\le\|\mathbf u\|+\|\mathbf v\|$ [Triangle inequality for vectors]
2. $d(\mathbf u, \mathbf v) ≤ d(\mathbf u, \mathbf w) + d(\mathbf w, \mathbf v)$ [Triangle inequality for distances]

### THEOREM 3.2.6 Parallelogram Equation for Vectors

If $\mathbf u$and $\mathbf v$ are vectors in $\mathbb R^n$, then:
$$
\|\mathbf u+\mathbf v\|^2+\|\mathbf u-\mathbf v\|^2=2(\|\mathbf u\|^2+\|\mathbf v\|^2)
$$

### THEOREM 3.2.7

If $\mathbf u$and $\mathbf v$ are vectors in $\mathbb R^n$ with the Euclidean inner product, then
$$
\mathbf u\cdot\mathbf v=\frac{1}{4}(\|\mathbf u+\mathbf v\|^2-\|\mathbf u-\mathbf v\|^2)
$$
If $A$ is an $n \times n$ matrix and $\mathbf u$ and $\mathbf v$ are $n \times 1$ matrices, then:
$$
A\mathbf u\cdot\mathbf v=\mathbf v^T(A\mathbf u)=(\mathbf v^TA)\mathbf u=(A^T\mathbf v)^T\mathbf u=\mathbf u\cdot A^T\mathbf v\\
\mathbf u\cdot A\mathbf v=(A\mathbf v)^T\mathbf u=(\mathbf v^TA^T)\mathbf u=\mathbf v^T(A^T\mathbf u)=A^T\mathbf u\cdot\mathbf v
$$
If the row vectors of $A$ are $\mathbf r_1, \mathbf r_2,\dots, \mathbf r_m$ and the column vectors of $B$ are $\mathbf c_1,\mathbf c_2,\dots, \mathbf c_n$, then the matrix product $AB$ can be expressed as
$$
AB=\begin{bmatrix}
\mathbf r_1\cdot\mathbf c_1&\mathbf r_1\cdot\mathbf c_2&\cdots&\mathbf r_1\cdot\mathbf c_n\\
\mathbf r_2\cdot\mathbf c_1&\mathbf r_2\cdot\mathbf c_2&\cdots&\mathbf r_2\cdot\mathbf c_n\\
\vdots&\vdots&&\vdots\\
\mathbf r_m\cdot\mathbf c_1&\mathbf r_m\cdot\mathbf c_2&\cdots&\mathbf r_m\cdot\mathbf c_n
\end{bmatrix}
$$

## 3.3 正交性 Orthogonality

### DEFINITION 1

Two nonzero vectors $u$ and $v$ in $\mathbb R^n$ are said to be *orthogonal* (or perpendicular) if $\mathbf u \cdot \mathbf v = 0$. We will also agree that the zero vector in $\mathbb R^n$ is orthogonal to every vector in $\mathbb R^n$.

### 法向量 Lines and Planes Determined by Points and Normals

Consider a line in $\mathbb R^2$ that passes $(x_0, y_0)$. An arbitary point on the line $(x,y)$, 
$$
a(x-x_0)+b(y-y_0)=\begin{bmatrix}a\\b\end{bmatrix}\cdot\begin{bmatrix}x-x_0\\y-y_0\end{bmatrix}=0
$$
where $(a, b)$ is the normal of the line.

The same for plane in $\mathbb R^3$
$$
\begin{bmatrix}a\\b\\c\end{bmatrix}\cdot\begin{bmatrix}x-x_0\\y-y_0\\z-z_0\end{bmatrix}=0
$$
Vector form of the line.

### 正投影 Orthogonal Projections

### Projection Theorem

If $\mathbf u$ and $\mathbf a$ are vectors in $\mathbb R^n$, and if $\mathbf a \ne\mathbf 0$, then $\mathbf u$ can be expressed in exactly one way in the form $\mathbf u = \mathbf w_1 + \mathbf w_2$, where $\mathbf w_1$ is a scalar multiple of $\mathbf a$ and $\mathbf w_2$ is orthogonal to $\mathbf a$.

#### Proof:

Since
$$
\mathbf w_1=k\mathbf a
$$
Then
$$
\mathbf u=k\mathbf a+\mathbf w_2\\
\mathbf u\cdot\mathbf a=k\mathbf a\cdot\mathbf a+\mathbf w_2\cdot\mathbf a\\
\mathbf u\cdot\mathbf a=k\|\mathbf a\|^2\\
k=\frac{\mathbf u\cdot\mathbf a}{\|\mathbf a\|^2}\\
\mathbf w_2=\mathbf u-\frac{\mathbf u\cdot\mathbf a}{\|\mathbf a\|^2}\mathbf a
$$
We call the $\mathbf w_1$ the orthogonal projection of $\mathbf u$ on $\mathbf a$, we denote it as $\text{proj}_{\mathbf a}\mathbf u$, the $\mathbf w_2$ the vector component of $\mathbf u$ orthogonal to $\mathbf a$.

### THEOREM 3.3.3 Theorem of Pythagoras in $\mathbb R^n$

If $\mathbf u$ and $\mathbf v$ are orthogonal vectors in $\mathbb R^n$ with the Euclidean inner product, then
$$
\|\mathbf u+\mathbf v\|^2=\|\mathbf u\|^2+\|\mathbf v\|^2
$$

### THEOREM 3.3.4

$$
D=\frac{|ax_0+by_0+cz_0+d|}{\sqrt{a^2+b^2+c^2}}=\frac{\mathbf n\cdot\mathbf x}{\|\mathbf n\|}
$$

## 3.4 线性方程组的几何意义 The Geometry of Linear Systems









