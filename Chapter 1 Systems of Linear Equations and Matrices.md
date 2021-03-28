# Chapter 1 Systems of Linear Equations and Matrices

## 1.1 线性方程组介绍 Introduction to Systems of Linear Equations

##### 线性方程 linear equation

$$
a_1x_1 + a_2x_2 +\dots+ a_nx_n = b
$$

where $a_1, a_2,\dots,a_n$ and $b$ are constants, and the $a_i$ are not all zero.

##### 齐次线性方程 homogeneous linear equation

$$
a_1x_1 + a_2x_2 +\dots+ a_nx_n = 0
$$

##### 线性方程组 system of linear equations

A finite set of linear equations. $x_i$ are unknowns.

A general linear system of *m* equations in the *n* unknowns can be written as:
$$
a_{11}x_1 + a_{12}x_2 +\dots+ a_{1n}x_n = b_{1}\\
a_{21}x_1 + a_{22}x_2 +\dots+ a_{2n}x_n = b_{1}\\
\vdots\\
a_{m1}x_1 + a_{m2}x_2 +\dots+ a_{mn}x_n = b_{m}
$$
**解 solution:**
$$
x_1 = s_1, x_2 = s_2,\dots, x_n = s_n\qquad(s_1,s_2,\dots,s_n)
$$

### Linear Systems in Two and Three Unknowns

For:
$$
a_1x + b_1y = c_1\\a_2x + b_2y = c_2
$$

1. The lines may be *parallel and distinct*, in which case there is no intersection and consequently *no solution*.
2. The lines may intersect at only *one point*, in which case the system has exactly *one solution*.
3. The lines may *coincide*, in which case there are infinitely many points of intersection(the points on the common line) and consequently *infinitely many solutions*.

相容的 consistent: at least one solution.

不相容的 inconsistent: no solution.

> Every system of linear equations has zero, one, or infinitely many solutions. There are no other possibilities.

### 增广矩阵和基本行操作 Augmented Matrices and Elementary Row Operations

 abbreviate the linear system we get augmented matrix

$$
\begin{bmatrix}
a_{11}&a_{12}&\dots&a_{1n}&b_{1}\\
a_{21}&a_{22}&\dots&a_{2n}&b_{2}\\
\vdots&\vdots& &\vdots&\\
a_{m1}&a_{m2}&\dots&a_{mn}&b_{m}\\
\end{bmatrix}
$$
The basic method for solving a linear system: 

1. Multiply an equation through by a nonzero constant.
2. Interchange two equations.
3. Add a constant times one equation to another.

Since the rows (horizontal lines) of an augmented matrix correspond to the equations in the associated system, the **elementary row operations** on a matrix

1. 一行乘以非零常数 Multiply a row through by a nonzero constant.
2. 交换两行 Interchange two rows.
3. 一行的倍数加到令一行上 Add a constant times one row to another

## 1.2 高斯消元法 Gaussian Elimination

### 阶梯型 Echelon Forms

A matrix that is in 简化行阶梯型 *reduced row echelon form*

1. If a row does not consist entirely of zeros, then the first nonzero number in the row is a 1. We call this a *leading 1*.
2. If there are any rows that consist entirely of 0s, then they are grouped together at the bottom of the matrix.
3. In any two successive rows that do not consist entirely of 0s, the leading 1 in the lower row occurs farther to the right than the leading 1 in the higher row.
4. Each column that contains a leading 1 has 0s everywhere else in that column.

A matrix that has the first three properties is said to be in 行阶梯型 *row echelon form*.

$$
\begin{bmatrix}
0&1&*&*&*&*&*&*&*&*\\
0&0&0&1&*&*&*&*&*&*\\
0&0&0&0&1&*&*&*&*&*\\
0&0&0&0&0&1&*&*&*&*\\
0&0&0&0&0&0&0&0&1&*
\end{bmatrix}\qquad
\begin{bmatrix}
0&1&*&0&0&0&*&*&0&*\\
0&0&0&1&0&0&*&*&0&*\\
0&0&0&0&1&0&*&*&0&*\\
0&0&0&0&0&1&*&*&0&*\\
0&0&0&0&0&0&0&0&1&*
\end{bmatrix}\\
\text{row echelon form}\qquad\qquad\qquad\qquad\qquad\text{reduced row echelon form}
$$

### 高斯消元法步骤 Elimination Methods











