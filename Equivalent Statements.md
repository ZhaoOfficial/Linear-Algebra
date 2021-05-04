# Equivalent Statements

If $A$ is an $n \times n$ matrix, then the following statements are equivalent.

1. $A$ is invertible.
2. $A\mathbf x = \mathbf0$ has only the trivial solution.
3. The reduced row echelon form of $A$ is $I_n$.
4. $A$ is expressible as a product of elementary matrices.
5. $A\mathbf x=\mathbf b$ is consistent for every $n\times1$ matrix $\mathbf b$.
6. $A\mathbf x=\mathbf b$ has exactly one solution for every $n\times1$ matrix $\mathbf b$.

## proof:

### (1)=>(2)

$$
(A^{-1})A\mathbf x=(A^{-1})\mathbf 0\Rightarrow I\mathbf x=\mathbf x=\mathbf 0
$$

### (2)=>(3)

The row reduced echelon form of the corresponding augmented matrix will be
$$
\begin{bmatrix}
x_{1}&&&& 0\\
&x_{2}&&& 0\\
&&\ddots&\\
&&&x_{n}  & 0
\end{bmatrix}
$$
which can be reduced to $I_n$

### (3)=>(4)

When reducing, there are a sequence of elementary matrices corresponding to the row operations, so we left multiply them in order and thus we can obtain
$$
E_k\dots E_2E_1A=I_n\Rightarrow A=E_1^{-1}E_2^{-1}\dots E_k^{-1}I_n
$$

### (4)=>(1)

$$
A^{-1}=E_k\dots E_2E_1I_n
$$

### (1)=>(6)

$$
\mathbf x=A^{-1}\mathbf b
$$

### (6)=>(5)

By definition.

### (5)=>(1)

$$
A[\mathbf x_1|\cdots|\mathbf x_n]=[\mathbf e_1|\cdots|\mathbf e_n]
$$

has solutions, then $[\mathbf x_1|\cdots|\mathbf x_n]=A^{-1}$

