# Chapter 5 Eigenvalues and Eigenvectors

## 5.1 特征值和特征向量 Eigenvalues and Eigenvectors

### DEFINITION 1

If $A$ is an $n\times n$ matrix, then a nonzero vector $\mathbf x$ in $\mathbb R^n$ is called an *eigenvector* of $A$ (or of the matrix operator $T_A$) if $A\mathbf x$ is a scalar multiple of $\mathbf x$; that is,
$$
A\mathbf x=\lambda\mathbf x
$$
for some scalar $\lambda$. The scalar $\lambda$ is called an *eigenvalue* of $A$ (or of $T_A$), and $\mathbf x$ is said to be an eigenvector corresponding to $\lambda$.

### THEOREM 5.1.1

If $A$ is an $n\times n$ matrix, then $\lambda$ is an eigenvalue of $A$ if and only if it satisfies the equation
$$
\det(\lambda I − A) = 0
$$
This is called the 特征方程 *characteristic equation* of $A$.

#### Proof

$$
\begin{align*}
A\mathbf x&=\lambda\mathbf x\\
A\mathbf x&=\lambda I\mathbf x\\
(\lambda I-A)\mathbf x&=\mathbf 0&(\mathbf x\ne\mathbf 0)\\
\det(\lambda I-A)&=0
\end{align*}
$$

When the characteristic equation $\det(\lambda I − A)$ is expanded, it takes the form
$$
\lambda^n+c_1\lambda^{n-1}+\dots+c_n=0
$$
then we called 
$$
p(\lambda)=\lambda^n+c_1\lambda^{n-1}+\dots+c_n
$$
the 特征多项式 *characteristic polynomial* of $A$.

### THEOREM 5.1.2

If $A$ is an $n\times n$ triangular matrix, (upper triangular, lower triangular, or diagonal), then the eigenvalues of $A$ are the entries on the main diagonal of $A$.

The diagonal entries of triangular matrix will be the eigenvalues of it, and the product of the diagonal entries of triangular matrix will be the determinant of it.

### THEOREM 5.1.3

If $A$ is an $n\times n$ matrix, the following statements are equivalent.

1. $\lambda$ is an eigenvalue of $A$.
2. $\lambda$ is a solution of the characteristic equation $\det(\lambda I − A) = 0$.
3. The system of equations $(\lambda I − A)\mathbf x = \mathbf 0$ has nontrivial solutions.
4. There is a nonzero vector $\mathbf x$ such that $A\mathbf x = \lambda\mathbf x$.

### 特征空间 The eigenspace of A

1. The solution/null space of $(\lambda I − A)\mathbf x = \mathbf 0$.
2. The kernel of the matrix operator $T_{\lambda I-A}:R^n\to R^n$.
3. The span of the set of vectors for which $A\mathbf x = \lambda\mathbf x$.

### THEOREM 5.1.4

A square matrix $A$ is invertible if and only if $\lambda = 0$ is not an eigenvalue of $A$.

#### Proof

Suppose A is an $n\times n$ matrix, and suppose $\lambda = 0$ is an eigenvalue of $A$, then for 
$$
p(\lambda)=\lambda^n+c_1\lambda^{n-1}+\dots+c_n=0
$$
$c_n$ should be $0$.

But if $\lambda = 0$
$$
\det(\lambda I-A)=\det(-A)=(-1)^n\det(A)=c_n=0
$$
then $A$ is invertible.

### DEFINITION 2

If $T : V\to V$ is a linear operator on a vector space $V$ , then a nonzero vector $\mathbf x$ in $V$ is called an eigenvector of $T$ if $T(\mathbf x)$ is a scalar multiple of $\mathbf x$; that is, for some scalar $\lambda$ . The scalar $\lambda$  is called an eigenvalue of $T$ , and $\mathbf x$ is said to be an eigenvector corresponding to $\lambda$.
## 5.2 对角化 Diagonalization

### DEFINITION 1

If $A$ and $B$ are square matrices, then we say that $B$ is similar to $A$ if there is an invertible matrix $P$ such that $B = P^{-1}AP$

A and B are 相似矩阵 *similar matrices* to each other.

### DEFINITION 2

A square matrix $A$ is said to be *diagonalizable* if it is similar to some diagonal matrix; that is, if there exists an invertible matrix $P$ such that $P^{−1}AP$ is diagonal. In this case the matrix $P$ is said to diagonalize $A$.

### THEOREM 5.2.1

If $A$ is an $n\times n$ matrix, the following statements are equivalent.

1. $A$ is diagonalizable.
2. $A$ has $n$ linearly independent eigenvectors.

#### Proof

##### 1 => 2

$$
AP=PD\\
A\begin{bmatrix}\mathbf p_1&\dots&\mathbf p_n\end{bmatrix}=\begin{bmatrix}A\mathbf p_1&\dots&A\mathbf p_n\end{bmatrix}=\begin{bmatrix}\lambda_1\mathbf p_1&\dots&\lambda_n\mathbf p_n\end{bmatrix}\\
A\mathbf p_i=\lambda_i\mathbf p_i
$$

Since $P$ is invertible, then $\mathbf p_i$ are linearly independent (non-zero), then they are the eigenvectors.

##### 2 => 1

$$
AP=A\begin{bmatrix}\mathbf p_1&\dots&\mathbf p_n\end{bmatrix}=\begin{bmatrix}A\mathbf p_1&\dots&A\mathbf p_n\end{bmatrix}=\begin{bmatrix}\lambda_1\mathbf p_1&\dots&\lambda_n\mathbf p_n\end{bmatrix}=PD\\
$$

Since $\{\mathbf p_1,\dots,\mathbf p_n\}$ are linearly independent, then $P$ is invertible, then $D=P^{-1}AP$.

### THEOREM 5.2.2

1. If $\lambda_1, \lambda_2,\dots,\lambda_k$ are distinct eigenvalues of a matrix $A$, and if $\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_k$ are corresponding eigenvectors, then $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_k\}$ is a linearly independent set.
2. An $n\times n$ matrix with $n$ distinct eigenvalues is diagonalizable.

#### Proof

##### 1

Suppose $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_k\}$ is a linearly dependent set.

Since $\mathbf v_i\ne\mathbf 0$, then $\{\mathbf v_1\}$ is a linearly independent set. Let $r(1\le r< k)$ be the largest integer such that $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_r\}$ is a linearly dependent set. Then $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_{r+1}\}$ is a linearly dependent set.
$$
c_1\mathbf v_1+c_2\mathbf  v_2+\dots+c_{r+1} \mathbf v_{r+1}=\mathbf0\tag{1}\\
$$
Multiplying both sides of (1) by $A$
$$
A(c_1\mathbf v_1+c_2\mathbf  v_2+\dots+c_{r+1} \mathbf v_{r+1})=\mathbf0\\

c_1\lambda_1\mathbf v_1+c_2\lambda_2\mathbf  v_2+\dots+c_{r+1}\lambda_{r+1}\mathbf v_{r+1}=\mathbf0\tag{2}\\
$$
$(2)-\lambda_{r+1}(1)$
$$
c_1(\lambda_1-\lambda_{r+1})\mathbf v_1+c_2(\lambda_2-\lambda_{r+1})\mathbf  v_2+\dots+c_{r+1}(\lambda_{r+1}-\lambda_{r+1})\mathbf v_{r+1}=\mathbf0\\
c_1(\lambda_1-\lambda_{r+1})\mathbf v_1+c_2(\lambda_2-\lambda_{r+1})\mathbf  v_2+\dots+c_{r}(\lambda_{r}-\lambda_{r+1})\mathbf v_{r}=\mathbf0\\
$$
Since $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_r\}$ is a linearly dependent set, then 
$$
c_1=c_2=\dots=c_r=0
$$
But $c_{r+1}\ne0$, then $\mathbf v_{r+1}=\mathbf0$, which is not an proper eigenvector, then $\{\mathbf v_1,\mathbf  v_2,\dots, \mathbf v_k\}$ is a linearly independent set.

##### 2

Since matrix has $n$ distinct eigenvalues, then it has $n$ linearly independent eigenvectors, then it is diagonalizable.

> 方针对角化的步骤：
>
> 1. 计算方阵的特征值和特征向量。
> 2. 观察特征向量是否为 $n$ 个线性无关的向量，否则不可对角化。
> 3. $P$ 为 $n$ 个特征向量组成的矩阵。
> 4. $D$ 为对应的特征值组成的对角矩阵。

> Example:
> $$
> A=\begin{bmatrix}0&0&-2\\1&2&1\\1&0&3\end{bmatrix}
> $$
> Then
> $$
> \det(\lambda I-A)=\begin{bmatrix}\lambda &0&2\\-1&\lambda -2&-1\\-1&0&\lambda -3\end{bmatrix}=(\lambda -1)(\lambda -2)^2=0
> $$
> For $\lambda=2$:
> $$
> \begin{bmatrix}2&0&2\\-1&0&-1\\-1&0&-1\end{bmatrix}\thicksim\begin{bmatrix}1&0&1\\0&0&0\\0&0&0\end{bmatrix}\\
> x_1=-s,x_2=t,x_3=s
> $$
> then
> $$
> \mathbf p_1=\begin{bmatrix}1\\0\\-1\end{bmatrix}\quad\mathbf p_2=\begin{bmatrix}0\\1\\0\end{bmatrix}
> $$
> For $\lambda=2$:
> $$
> \begin{bmatrix}1&0&2\\-1&-1&-1\\-1&0&-2\end{bmatrix}\thicksim\begin{bmatrix}1&0&2\\0&1&-1\\0&0&0\end{bmatrix}\\
> x_1=-2s,x_2=s,x_3=s
> $$
> then
> $$
> \mathbf p_3=\begin{bmatrix}-2\\1\\1\end{bmatrix}
> $$
> Then
> $$
> P=\begin{bmatrix}1&0&-2\\0&1&1\\-1&0&1\end{bmatrix}\quad
> D=\begin{bmatrix}2&0&0\\0&2&0\\0&0&1\end{bmatrix}
> $$

### THEOREM 5.2.3 矩阵幂的特征值 Eigenvalues of Powers of a Matrix

If $k$ is a positive integer, $\lambda$ is an eigenvalue of a matrix $A$, and $\mathbf x$ is a corresponding eigenvector, then $\lambda^k$ is an eigenvalue of $A^k$ and $\mathbf x$ is a corresponding eigenvector.

#### Proof

$$
(A^k)\mathbf x=(A^{k-1})A\mathbf x=\lambda(A^{k-1})\mathbf x=\lambda^k\mathbf x
$$

Notice that
$$
D^k=\begin{bmatrix}\lambda_1^k&\cdots&0\\\vdots&\ddots&\vdots\\0&\cdots&\lambda_n^k\end{bmatrix}
$$
then
$$
\begin{align*}
A^k&=(P^{-1}DP)^k\\
&=(P^{-1}DPP^{-1}DP)(P^{-1}DP)^{k-2}\\
&=(P^{-1}D^2P)(P^{-1}DP)^{k-2}\\
&=P^{-1}D^kP
\end{align*}
$$
Easy for computing.

### 几何重数和代数重数 Geometric and Algebraic Multiplicity

Notice that the example shows that the converse of THEOREM 5.2.2(2) does not hold.

If $\lambda_0$ is an eigenvalue of an $n\times n$ matrix $A$.

The geometric multiplicity of $\lambda_0$: the dimension of the eigenspace corresponding to $\lambda_0$.

The algebraic multiplicity of $\lambda_0$: the number of times that $\lambda − \lambda_0$ appears as a factor in the characteristic polynomial of $A$.

### THEOREM 5.2.4

`without proof`

If $A$ is a square matrix, then:

1. For every eigenvalue of $A$, the geometric multiplicity is less than or equal to the algebraic multiplicity.
2. A is diagonalizable if and only if the geometric multiplicity of every eigenvalue is equal to the algebraic multiplicity.

## 5.3 复线性空间 Complex Vector Spaces

### DEFINITION 1

If $n$ is a positive integer, then a complex $n$-tuple is a sequence of $n$ complex numbers ($v_1,v_2,\dots, v_n$). The set of all complex $n$-tuples is called complex $n$-space and is denoted by $\mathbb C ^n$. Scalars are complex numbers, and the operations of addition, subtraction, and scalar multiplication are performed component-wise.

Any vector in $\mathbb C^n$ can be split into 实部 *real* and 虚部 *imaginary* parts

$$
\begin{align*}
\mathbf v&=(v_1,v_2,\dots, v_n)=(a_1+ib_1,a_2+ib_2,\dots,a_n+ib_n)\\
&=(a_1,a_2,\dots,a_n)+i(b_1,b_2,\dots,b_n)\\
&=\Re e(\mathbf v)+i\Im m(\mathbf v)
\end{align*}
$$
then we define the *complex conjugate* of vector $\mathbf v$
$$
\bar{\mathbf v}=\Re e(\mathbf v)-i\Im m(\mathbf v)
$$
Real matrix: entries are real

Complex matrix: entries are real or complex

Similarly, we can define the *complex conjugate* of matrix $A$ as $\bar{A}$.

### THEOREM 5.3.1

If $\mathbf u$ and $\mathbf v$ are vectors in $\mathbb C^n$, and if $k$ is a scalar, then:

1. $\bar{\bar{\mathbf u}} = \mathbf u$
2. $\overline{k\mathbf u} = \bar{k}\bar{\mathbf u}$
3. $\overline{\mathbf u \pm \mathbf v} = \bar{\mathbf u} \pm \bar{\mathbf v}$

### THEOREM 5.3.2

If A is an $m \times k$ complex matrix and $B$ is a $k \times n$ complex matrix, then:

1. $\bar{\bar{A}} = A$
2. $(\overline{A^T}) = (\bar{A})^T$
3. $\overline{AB} =\overline{A}\overline{B}$

### DEFINITION 2

If $u = (u_1,u_2,\dots, u_n)$ and $v = (v_1,v_2,\dots, v_n)$ are vectors in $\mathbb C^n$, then the *complex Euclidean inner product* of $\mathbf u$ and $\mathbf v$ (also called the complex dot product) is denoted by $\mathbf u \cdot \mathbf v$ and is defined as
$$
\mathbf u \cdot \mathbf v = u_1\overline{v_1} + u_2\overline{v_2} +\cdots+ u_n\overline{v_n}
$$
We also define *the Euclidean norm on $\mathbb C^n$* to be
$$
\|\mathbf v\| = \sqrt{\mathbf v \cdot \mathbf v} = \sqrt{|v_1|^2 + |v_2|^2 +\dots+|v_n|^2}
$$
Unit vector and orthogonal are the same as real.







