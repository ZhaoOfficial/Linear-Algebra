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

augmented matrix: abbreviation of the linear system

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

> Step 1. Locate the leftmost *column* that does not consist entirely of 0.
> $$
> \begin{bmatrix}
> 0&0&−2&0&7&12\\
> 2&4&−10&6&12&28\\
> 2&4&−5&6&−5&−1
> \end{bmatrix}
> $$
> Step 2. Interchange the top row with another row, if necessary, to bring a nonzero entry to the top of the column found in Step 1.
> $$
> \begin{bmatrix}
> 2&4&−10&6&12&28\\
> 0&0&−2&0&7&12\\
> 2&4&−5&6&−5&−1
> \end{bmatrix}
> $$
> Step 3. If the entry that is now at the top of the column found in Step 1 is *a*, multiply the first row by *1/a* in order to introduce a leading 1.
> $$
> \begin{bmatrix}
> 1&2&−5&3&6&14\\
> 0&0&−2&0&7&12\\
> 2&4&−5&6&−5&−1
> \end{bmatrix}
> $$
> Step 4. Add suitable multiples of the top row to the rows below so that all entries below the leading 1 become 0.
> $$
> \begin{bmatrix}
> 1&2&−5&3&6&14\\
> 0&0&−2&0&7&12\\
> 0&0&5&0&−17&−29
> \end{bmatrix}
> $$
> Step 5. Again with Step 1 applied to the submatrix that remains. Continue in this way until the *entire* matrix is in row echelon form.
> $$
> \begin{bmatrix}
> 1&2&-5&3&6&14\\
> 0&0&1&0&-\frac{7}{2}&-6\\
> 0&0&0&0&1&2
> \end{bmatrix}
> $$
> Step 6. Beginning with the last nonzero row and working upward, add suitable multiples of each row to the rows above to introduce zeros above the leading 1’s.
> $$
> \begin{bmatrix}
> 1&2&0&3&0&7\\
> 0&0&1&0&0&1\\
> 0&0&0&0&1&2
> \end{bmatrix}
> $$

#### 解的情况

1. 如果最后一行存在类似
   $$
   0x+0y+0z=c\qquad(c\ne0)
   $$
   则该方程组无解。

2. 如果最后一行存在类似
   $$
   0x+0y+0z=0
   $$
   则该行可以忽略，对解没有影响。

3. Variable correspond to the leading 1’s in the augmented matrix are the *leading variables*. The remaining variables are called *free variables*.

   > So the solution can be expressed as:
   > $$
   > x_1=7-2x_2-3x_4\quad x_3=1\quad x_5=2
   > $$

4. 

### 齐次线性方程组 Homogeneous Linear Systems

$$
a_{11}x_1 + a_{12}x_2 +\dots+ a_{1n}x_n = 0\\
a_{21}x_1 + a_{22}x_2 +\dots+ a_{2n}x_n = 0\\
\vdots\\
a_{m1}x_1 + a_{m2}x_2 +\dots+ a_{mn}x_n = 0
$$

$x_1= 0, x_2 = 0,\dots,x_n = 0$ is always a solution, called 平凡解 *trivial solution*. If there are other solutions, they are called 非平凡解 *nontrivial solutions*.

Now consider a general homogeneous linear system with *n* unknowns, and suppose that the reduced row echelon form of the augmented matrix has *r* nonzero rows.
$$
\begin{bmatrix}
x_{k_1}&&&&+ \sum( ) & 0\\
&x_{k_2}&&&+ \sum( ) & 0\\
&&\ddots&&\vdots\\
&&&x_{k_r}&+ \sum( ) & 0
\end{bmatrix}
$$

### THEOREM 1.2.1 Free Variable Theorem for Homogeneous Systems

If a homogeneous linear system has *n* unknowns, and if the reduced row echelon form of its augmented matrix has *r* nonzero rows, then the system has *n − r* free variables.

### THEOREM 1.2.2

A homogeneous linear system with *more* unknowns than equations has infinitely many solutions.



 3 facts about row echelon forms and reduced row echelon forms:

1. Every matrix has a unique reduced row echelon form; that is, regardless of whether you use Gauss–Jordan elimination or some other sequence of elementary row operations, the same reduced row echelon form will result in the end.
2. Row echelon forms are not unique; that is, different sequences of elementary row operations can result in different row echelon forms.
3. Although row echelon forms are not unique, the reduced row echelon form and all row echelon forms of a matrix *A* have the same number of zero rows, and the leading 1’s always occur in the same positions. Those are called the pivot positions of *A*. A column that contains a pivot position is called a pivot column of *A*.

## 1.3 矩阵和矩阵操作 Matrices and Matrix Operations

### Matrices

Definition1: A matrix is a rectangular array of numbers. The numbers in the array are called the *entries* in the matrix.

Size: number of rows and columns.

A matrix with *n* rows and *n* columns is said to be a n阶方阵 square matrix of order n.

A matrix with only one row is called a row vector and a matrix with only one column is called a column vector.

### Matrix Operations

*Equal*: $a_{ij}=b_{ij}$

*Addition and Subtraction*: $(a+b)_{ij}=a_{ij}+b_{ij}$

*Scalar product*: $c(a_{ij})=ca_{ij}$

*Matrix product*: $c_{ij}=\sum_{k}a_{ik}b_{kj}$

*Partition*: divide into submatrices and/or vectors

### Matrix Multiplication by Columns and by Rows