---
title: "Basic Linear Algebra"
date: 2021-08-19T00:00:00+08:00
---

## Vectors

### Vector space

#### Definition of vector space

Let $V$ be a set of elements on which vector addition and scalar multiplication are defined. $V$ is a vector space if the following axioms are satisfied:

##### Axioms for Vector Addition

1. If $\mathbf{x}, \mathbf{y} \in V$, then $\mathbf{x} + \mathbf{y} \in V$
2. For all $\mathbf{x}, \mathbf{y} \in V$, $\mathbf{x}+\mathbf{y}=\mathbf{y}+\mathbf{x}$
3. For all $\mathbf{x}, \mathbf{y}, \mathbf{z} \in V$, $(\mathbf{x}+\mathbf{y})+\mathbf{z} = \mathbf{x}+(\mathbf{y}+\mathbf{z})$
4. There is a unique vector $\mathbf{0} \in V$ such that $\mathbf{0}+\mathbf{x} = \mathbf{x}+\mathbf{0} = \mathbf{x}$
5. For each $\mathbf{x} \in V$, there exists a vector $-\mathbf{x}$ such that $\mathbf{x}+(-\mathbf{x}) = (-\mathbf{x})+\mathbf{x} = \mathbf{0}$

##### Axioms for Scalar Multiplication

1. If $k$ is any scalar and $\mathbf{x} \in V$, then $k\mathbf{x}\in V$
2. $k(\mathbf{x}+\mathbf{y}) = k\mathbf{x}+k\mathbf{y}$
3. $(k_1+k_2)\mathbf{x} = k_1\mathbf{x} + k_2\mathbf{x}$
4. $k_1(k_2\mathbf{x}) = (k_1k_2)\mathbf{x}$
5. $1\mathbf{x} = \mathbf{x}$

#### Concepts

- *Subspace* - A subset $W$ of a vector space $V$ that is itself a vector space under the operations of vector addition and scalar multiplication defined in $V$.
  - Criteria for a subspace
    - Closed vector addition satisfied: If $\mathbf{x}$, $\mathbf{y} \in W$, then $\mathbf{x}+\mathbf{y} \in W$
    - Closed scalar multiplication satisfied: If $\mathbf{x} \in W$ and $k$ is a scalar, then $k\mathbf{x} \in W$
- *Linearly independent* - a set of vectors where $k_1\mathbf{x}_1 + k_2\mathbf{x}_2 + \cdots + k_n\mathbf{x}_n = \mathbf{0}$ can only satisfied by $k_1=k_2=\cdots=k_n=0$
- *Linearly dependent* - a set of vectors that are not linearly independent
- *Basis* - a set of vectors $B \in V$ that is linearly independent and every vector in $V$ can be expressed as a linear combination of vectors in $B$, i.e. $\mathrm{span}(B) = V$
  - Standard basis in $\Reals^n$
    - $\mathbf{e}_1 = \langle 1,0,0,...,0 \rangle$
    - $\mathbf{e}_2 = \langle 0,1,0,...,0 \rangle$
    - $\cdots$
    - $\mathbf{e}_n = \langle 0,0,0,...,1 \rangle$
  - Coordinates $c_i$ of $\mathbf{v}$ relative to the basis $B=\{\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n\}$
    - $\mathbf{v} = c_1\mathbf{x}_1 + c_2\mathbf{x}_2 + \cdots + c_n\mathbf{x}_n$
- *Dimension* - number of vectors in a basis $B$ for a vector space $V$
  - the number of vectors in the spanning set $S$
- *Span* - the set of all linear combinations of the any set of vectors $S=\{\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n\}$ in $V$, where $\mathrm{span}(S) = \{c_1\mathbf{x}_1 + c_2\mathbf{x}_2 + ... + c_n\mathbf{x}_n\}$
  - Spanning set - $S$ where $V = \mathrm{span}(S)$

### Gram-Scmidt orthogonalization

- Coordinates of $\mathbf{u}$ relative to an orthogonal basis $B = \{\mathbf{w}_1, \mathbf{w}_2, ..., \mathbf{w}_n\}$
  - $\mathbf{u} = (\mathbf{u}\cdot\mathbf{w}_1)\mathbf{w}_1 + (\mathbf{u}\cdot\mathbf{w}_2)\mathbf{w}_2 + \cdots + (\mathbf{u}\cdot\mathbf{w}_n)\mathbf{w}_n$
- Gram-Scmidt Orthogonalization
  - Given $B = \{\mathbf{u}_1, \mathbf{u}_2, ..., \mathbf{u}_n\}$ is a set of basis,
  - then $B' = \{\mathbf{v}_1, \mathbf{v}_2, ..., \mathbf{v}_n\}$ is a set of orthogonal basis where
    - $\mathbf{v}_1 = \mathbf{u}_1$
    - $\mathbf{v}_2 = \mathbf{u}\_2 - \mathbf{proj}\_{\mathbf{u}_2}\mathbf{v}_1$
    - $\mathbf{v}_3 = \mathbf{u}\_3 - \mathbf{proj}\_{\mathbf{u}_3}\mathbf{v}\_1 - \mathbf{proj}\_{\mathbf{u}_3}\mathbf{v}_2$
    - $\cdots$
    - $\mathbf{v}_n = \mathbf{u}\_n - \mathbf{proj}\_{\mathbf{u}_n}\mathbf{v}\_1 - \mathbf{proj}\_{\mathbf{u}_n}\mathbf{v}\_2 - \cdots - \mathbf{proj}\_{\mathbf{u}\_n}\mathbf{v}\_{n-1}$
    - Note: $\mathbf{proj}_{\mathbf{u}_a}\mathbf{v}_b = \left(\dfrac{\mathbf{u}_a\cdot\mathbf{v}_b}{\mathbf{v}_b\cdot\mathbf{v}_b}\right)\mathbf{v}_b$
  - and $B'' = \{\mathbf{w}_1, \mathbf{w}_2, ..., \mathbf{w}_n\}$ is a set of orthonormal basis where
    - $\mathbf{w}_i = \dfrac{\mathbf{v}_i}{\lVert\mathbf{v}_i\rVert}$

## Matrices

### Systems of linear equations

- *Consistent* - system with at least one solution
  - Unique solution
  - Infinitely many solution
- *Inconsistent* - system with no solutions
- *Homogeneous* - all constants are zero $\mathbf{A}\mathbf{x} = \mathbf{0}$
- *Nonhomogeneous* - not all constants are zero $\mathbf{A}\mathbf{x} = \mathbf{b}$
- *Elementary row operations*
  - $cR_i$ - Multiply a row by a nonzero constant
  - $R_1 \leftrightarrow R_j$ - Interchange any two rows
  - $cR_i + R_j$ - Add a nonzero multiple of one row to any other row
- *Row equivalent* - matrix obtained by a sequence of elementary row operations on another matrix
- *Row reduction* - procedure of carrying out elementary row operations on a matrix
- *Row-echelon form* - augmented matrix which...
  - Rows consisting of all zeros are at the bottom of the matrix
  - In consecutive nonzero rows, the first entry nonzero entry (pivot) in the lower row appears to the right of the pivot in the higher row
  - The first nonzero entry in a nonzero row is a 1
    - (depend on text, could be definition of reduced row-echelon form)
  - Note: row-echelon form is non-unique
- *Reduced row-echelon form* - augmented matrix which...
  - Is in row-echelon form
  - A column containing a first entry 1 has zeros everywhere else
    - column of leading entries are standard vectors
  - Note: reduced row-echelon form is unique
- *Gaussian elimination* - row-reduce the augmented matrix until arrive at row-echelon form
- *Gauss-Jordan elimination* - row-reduce the augmented matrix until arrive at reduced row-echelon form
- *Overdetermined* - linear systems with more equations than variables
- *Underdetermined* - linear systems with fewer equations than variables
- *Trivial solution* - solution consisting of all zeros, i.e. $\mathbf{x} = \mathbf{0}$
- *Nontrivial solution* - solution with at least one nonzero entry, i.e. $\mathbf{x} \not= \mathbf{0}$
  - Existence of nontrivial solutions
    - An underdetermiend homogeneous system has nontrivial solutions
- *Superposition principle*
  - If $\mathbf{x}_1, \mathbf{x}_2$ are solutions of homogeneous system $\mathbf{A}\mathbf{x} = \mathbf{0}$
    - then their linear combination is also a solution: $\mathbf{x} = c_1\mathbf{x}_1 + c_2\mathbf{x}_2$

### Rank of a matrix

- *Row vector* - $1 \times n$ matrices that are rows of a matrix
  - *Row space* - the span of all row vectors
- *Column vector* - $n \times 1$ matrices that are columns of a matrix
  - *Column space* - the span of all column vectors
- *Rank* - maximum number of linearly independent row vector in a matrix
  - Rank by row reduction: $\mathbf{A}$ is row equivalent to a row-echelon form $\mathbf{B}$
    - Row space of $\mathbf{A}$ = Row space of $\mathbf{B}$
    - Nonzero rows of $\mathbf{b}$ form a basis for the row space of $\mathbf{A}$
    - $\mathrm{rank}(\mathbf{A})$ = number of nonzero rows in $\mathbf{B}$
- Consistency of nonhomogeneous systems
  - $\mathbf{A}\mathbf{x} = \mathbf{b}$ is consistent $\iff \mathrm{rank}(\mathbf{A}) = \mathrm{rank}(\mathbf{A}|\mathbf{B})$
  - If $\mathbf{A}\mathbf{x} = \mathbf{b}$ with $m$ equations and $n$ variables is consistent with $\mathrm{rank}(A) = r$
    - then the solution contains $n-r$ parameters

$$\footnotesize\mathbf{A}\mathbf{x} = \mathbf{0} \implies \text{Always consistent}
  \begin{cases}
    \text{Unique solution: } \mathbf{x} = \mathbf{0} \cr
    \text{Infinity of solutions: } \mathrm{rank}(\mathbf{A}) < n, n-r \text{ params}
  \end{cases}$$

$$\footnotesize\mathbf{A}\mathbf{x} = \mathbf{b}
  \begin{cases}
    \text{Consistent: } \mathrm{rank}(\mathbf{A}) = \mathrm{rank}(\mathbf{A}|\mathbf{B})
      \begin{cases}
        \text{Unique solution: } \mathrm{rank}(\mathbf{A}) = n \cr
        \text{Infinity of solutions: } \mathrm{rank}(\mathbf{A}) < n, n-r \text{ params}
      \end{cases} \cr
    \text{Inconsistent: } \mathrm{rank}(\mathbf{A}) < \mathrm{rank}(\mathbf{A}|\mathbf{B})
  \end{cases}$$

### Determinant

#### Finding the determinant

- *Determinant of a square matrix* - $\det\mathbf{A}$
  - $\det\mathbf{B} = \begin{vmatrix} a_{11} & a_{12} \cr a_{21} & a_{22} \end{vmatrix} = a_{11}a_{22} - a_{12}a_{21}$
- *Minor determinant* - $M_{ij}$, the determinant of the submatrix obtained by deleting the $i$th row and the $j$th column of $\mathbf{A}$
- *Cofactor* - $C_{ij}$, signed minor determinant
  - $C_{ij} = (-1)^{i+j}M_{ij}$
  - The sign gives checkerboard pattern starting from plus
- *Cofactor expansion of $\det\mathbf{A}$ along the $i$th row*
  - $\det\mathbf{A} = a_{i1}C_{i1} + a_{i2}C_{i2} + \cdots + a_{in}C_{in}$
- *Cofactor expansion of $\det\mathbf{A}$ along the $j$th column*
  - $\det\mathbf{A} = a_{1j}C_{1j} + a_{2j}C_{2j} + \cdots + a_{nj}C_{nj}$

#### Properties of determinants

- $\det\mathbf{A}^T = \det\mathbf{A}$
- $\det(\mathbf{A}\mathbf{B}) = \det\mathbf{A}\cdot\det\mathbf{B}$
- If $\mathbf{A}$ has two rows or columns the same,
  - then $\det\mathbf{A} = 0$
- If $\mathbf{A}$ has all zero entries in a row or column,
  - then $\det\mathbf{A} = 0$
- If $\mathbf{A}$ is a triangular matrix,
  - then $\det\mathbf{A} = a_{11}a_{22}\cdots a_{nn}$
- If $\mathbf{B}$ by interchange row/column of $\mathbf{A}$,
  - then $\det\mathbf{B} = -\det\mathbf{A}$
- If $\mathbf{B}$ by multiplying row/column of $\mathbf{A}$ by $k$,
  - then $\det\mathbf{B} = k\det\mathbf{A}$
- If $\mathbf{B}$ by multiplying row/column of $\mathbf{A}$ by $k$ and add to another,
  - then $\det\mathbf{B} = \det\mathbf{A}$

### Inverse of a matrix

#### Finding the inverse

- *Inverse* - $\mathbf{A}^{-1}$ such that $\mathbf{A}^{-1}\mathbf{A} = \mathbf{A}\mathbf{A}^{-1} = \mathbf{I}$
  - Invertible (nonsingular) - matrix with inverse
  - Noninvertible (singular) - matrix with no inverse
- Properties of inverse
  - $(\mathbf{A}^{-1})^{-1} = \mathbf{A}$
  - $(\mathbf{A}\mathbf{B})^{-1} = \mathbf{B}^{-1}\mathbf{A}^{-1}$
  - $(\mathbf{A}^{T})^{-1} = (\mathbf{A}^{-1})^{T}$
- *Adjoint* - the transpose of the matrix of cofactors of $\mathbf{A}$
  - $\mathrm{adj}\mathbf{A} = \begin{bmatrix} C_{11} & C_{12} & \cdots & C_{1n} \cr C_{21} & C_{22} & \cdots & C_{2n} \cr \vdots & \vdots & \ddots & \vdots \cr C_{n1} & C_{n2} & \cdots & C_{nn} \end{bmatrix}^{T}$
- Adjoint method
  - $\mathbf{A}^{-1} = \left(\dfrac{1}{\det\mathbf{A}}\right)\mathrm{adj}\mathbf{A}$
  - Nonsingular $\iff \det\mathbf{A} \not= 0$
  - Singular $\iff \det\mathbf{A} = 0$
- Row operation method
  - $(\mathbf{A}|\mathbf{I}) \xRightarrow{\text{Elementary row operation}} (\mathbf{I}|\mathbf{A})$

#### Using the inverse to solve systems

- Nonmobonegeous system $\mathbf{A}\mathbf{x} = \mathbf{b}$
  - $\mathbf{x} = \mathbf{A}^{-1}\mathbf{b}$
- Homogeneous system $\mathbf{A}\mathbf{x} = \mathbf{0}$
  - Nonsingular $\iff$ Only trivial solution $\mathbf{x} = \mathbf{0}$
  - Singular $\iff$ Has nontrivial solution

### Cramer's rule

- If $\mathbf{A}\xleftarrow{i} \mathbf{b}$ is the matrix obtained by replacing $\mathbf{A}$'s $i$th column by $\mathbf{b}$,
  - then the $i$th component of the solution $\mathbf{x}$ is $x_i = \dfrac{\det\mathbf{A}\xleftarrow{i} \mathbf{b}}{\det\mathbf{A}}$

### Eigenvalues and eigenvectors

- *Eigenvalue* - a number $\lambda$ that satisfies $\mathbf{A}\mathbf{v} = \lambda\mathbf{v}$
- *Eigenvector* - a non-zero vector $\mathbf{v}$ that satisfies $\mathbf{A}\mathbf{v} = \lambda\mathbf{v}$ with corresponding $\lambda$
  - *Characteristic equation* - $\det(\mathbf{A} - \lambda\mathbf{I}) = 0$
    - Eigenvalues are the roots of the characteristic equation
    - Eigenvectors  is the solution to $(\mathbf{A} - \lambda\mathbf{I})\mathbf{v} = 0$ by applying Gauss-Jordan elimination to $(\mathbf{A} - \lambda\mathbf{I} | 0)$
      - Eigenvectors are not unique
      - A nonzero constant multiple of an eigenvector is another eigenvector
- Complex eigenvalues and eigenvectors
  - If $\lambda = \alpha + i\beta$ is a complex eigenvalue,
    - then its complex conjugate $\overline{\lambda} = \alpha - i\beta$ is also an eigenvalue
  - If $\mathbf{v}$ is an eigenvector corresponding to $\lambda$,
    - then $\overline{\mathbf{v}}$ is an eigenvector corresponding to $\overline{\lambda}$
- Singular matrix and zero eigenvalue
  - Singular $\iff \lambda = 0$
  - Nonsingular $\iff \lambda \not= 0$
  - Determinant of $\mathbf{A}$ is the product of its eigenvalues
    - $\det\mathbf{A} = \lambda_1\lambda_2\cdots\lambda_n$
- If $\mathbf{A}$ has eigenvalue $\lambda$ with corresponding eigenvector $\mathbf{v}$,
  - then $\mathbf{A}^{-1}$ has eigenvalue $1/\lambda$ with the same corresponding eigenvector $\mathbf{v}$
- If $\mathbf{A}$ is a triangular matrix,
  - then the eigenvalues are the main diagonal entries.

### Powers of matrices

- *Cayley-Hamilton theorem* - an $n \times n$ matrix $\mathbf{A}$ satisfies its own characteristic equation
  - Characteristic equation: $(-1)^n \lambda^{n} + c_{n-1}\lambda^{n-1} + \cdots + c_1\lambda + c_0 = 0$
  - Cayley-Hamilton theorem: $(-1)^n \mathbf{A}^{n} + c_{n-1}\mathbf{A}^{n-1} + \cdots + c_1\mathbf{A} + c_0\mathbf{I} = \mathbf{0}$
- Matrix of order 2
  - $\mathbf{A}^m = c_0\mathbf{I} + c_1\mathbf{A}$
  - $\lambda^m = c_0 + c_1\lambda$
- Matrix of order n
  - $\mathbf{A}^m = c_0\mathbf{I} + c_1\mathbf{A} + c_2\mathbf{A}^2 + \cdots + c_{n-1}\mathbf{A}^{n-1}$
  - $\lambda^m = c_0 + c_1\lambda + c_2\lambda^2 + \cdots + c_{n-1}\lambda^{n-1}$

### Orthogonal matrices

- *Symmetric* - $\mathbf{A}$ where $\mathbf{A}^T = \mathbf{A}$
  - Symmetric matrix has real eigenvalues
  - Symmetric matrix has orthogonal eigenvectors corresponding to distinct eigenvalues
- *Orthogonal* - $\mathbf{A}$ where $\mathbf{A}^T = \mathbf{A}^{-1}$
  - $\mathbf{A}^T\mathbf{A} = \mathbf{I}$
  - *Orthonormal* - a set of vectors where every pair of distinct vectors is orthogonal and is a unit vector
  - Orthogonal $\iff$ Columns form an orthonormal set

### Approximation of eigenvalues

- *Dominant eigenvalue* - eigenvalue with absolute value greatest than that of the remaining $\lvert \lambda_k \rvert > \lvert \lambda_i \rvert, i=1,2,...,n$
- *Dominant eigenvector* - eigenvector corresponding to dominant eigenvalue $\lambda_k$
- Power method
  - $\mathbf{A}^m\mathbf{x}_0\approx\lambda_1^m c_1 \mathbf{v}_1$ approximates dominant eigenvector $\mathbf{v}_1$
  - $\lambda_1\approx\dfrac{\mathbf{A}\mathbf{x}_m\cdot\mathbf{x}_m}{\mathbf{x}_m\cdot\mathbf{x}_m}$ approximates dominant eigenvalue $\lambda_1$
    - *Rayleigh quotient* - $\lambda_1\approx\dfrac{\mathbf{A}\mathbf{x}_m\cdot\mathbf{x}_m}{\mathbf{x}_m\cdot\mathbf{x}_m}$

### Diagonalization

- *Diagonalizable* - $\mathbf{A}$ has a nonsingular $\mathbf{P}$ that satisfies $\mathbf{P}^{-1}\mathbf{A}\mathbf{P} = \mathbf{D}$ where $\mathbf{D}$ is a diagonal matrix
  - $\mathbf{P}^{-1}\mathbf{A}\mathbf{P} = \mathbf{D}$
  - $\mathbf{A}\mathbf{P} = \mathbf{P}\mathbf{D}$
  - Diagonalizable $\iff$ Has $n$ linearly independent eigenvectors
    - $n$ distinct eigenvalues $\implies$ diagonalizable
- Symmetric matrix can always be diagonalized
  - *Orthogonally diagonalizable* - an orthogonal matrix $\mathbf{P}$ diagonalizes $\mathbf{A}$
    - $\mathbf{A}$ is symmetric $\iff \mathbf{A}$ can be orthogonally diagonalized

### LU-Factorization

- *LU-factorization* - $\mathbf{A} = \mathbf{L}\mathbf{U}$
  - *Lower triangular matrix* - square matrix $\mathbf{L}$ whose entries above the main diagonal are all zero
  - *Upper triangular matrix* - square matrix $\mathbf{U}$ whose entries below the main diagonal are all zero
  - LU-factorization is not uniquely determined
- Doolittle's method
