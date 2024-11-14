# Vector Spaces

Matrices, directed line segments (vectors) and polynomials are seemingly unrelated concepts, but:
- they are all closed under addition
- they are all closed under scalar multiplication
- zero matrix, polynomial and vector are similar

Similarly, there are many regularities between many such concepts. The question is “What is the minimum number of regularities that are required so that every other regularity will follow?”. This is announced by the label **“Vector Space”**.

A vector space is a collection of vectors that satisfy a set of axioms/rules.

Suppose there are objects $u,v,w…$ belong to vector space $\mathbb{V}$.

Thus, vector space can be defined as a set of objects $\mathbb{V} = {u,v,w…}$ and scale as ${α,ß,Γ…}$ along with a binary operation of vector addition denoted by ⊕, and scalar multiplication denoted by ⊙ which possesses the following 10 properties:

- A1 - Close under addition: If $u,v ∈ \mathbb{V}$, then $u ⊕ v ∈ \mathbb{V}$
- A2 - Commutative law of addition: $u ⊕ v = v ⊕ u$ for $u,v ∈ \mathbb{V}$
- A3 - Associative law for addition: $u ⊕ (v ⊕ u) = (u ⊕ v) ⊕ w$ for $u,v,w ∈ \mathbb{V}$
- A4 - If a zero vector in $\mathbb{V}$, denoted by zero such that for every vector $u$ in $\mathbb{V}$, $0 ⊕ u = u ⊕ 0 = u$
- A5 - For every vector $u$ in $\mathbb{V}$, for a $-u$ in $\mathbb{V}$, $u ⊕ -u = 0$<br><br>
- S1 - Closure under scalar multiplication: If $u ∈ \mathbb{}\mathbb{V}$, then $α ⊙ u ∈ \mathbb{V}$ for any scalar $α$
- S2 - For any two scalars $α$ and $ß$, and any vector $u$ in $\mathbb{V}$, $α ⊙ (ß ⊙ u) = (αß) ⊙ u$
- S3 - For any vector $u$ in $\mathbb{V}$, $1 ⊙ u = u$
- S4 - For any 2 scalar $α$ and $ß$, and any vector $u$ in $\mathbb{V}$, $(α + ß) ⊙ u = α ⊙ u ⊕ ß ⊙ u$
- For any scalar $a$ and any two vectors $u$ and $\mathbb{V}$ in $\mathbb{V}$, $α ⊙ (u ⊕ v) = α ⊙ u ⊕ α ⊙ \mathbb{V}$
## Theorems

#### 1. For any vector $u$ in a vector space $\mathbb{V}$, $0 ⊙ u = 0$

#### 2. In any vector space $\mathbb{V}$, $α ⊙ 0 = 0$, for every scalar $α$

#### 3. The additive inverse of any vector $\mathbb{V}$ in a vector space $\mathbb{V}$ is unique

#### 4. The zero vector in any vector space $\mathbb{V}$ is unique

#### 5. For any vector $w$ in a vector space $\mathbb{V}$, $-1 ⊙ w = -w$

#### 6. For any vector $w$ in a vector space $\mathbb{V}$, $-(-w) = w$

#### 7. Let $α$ be a scalar and $u$ a vector in a vector space $\mathbb{V}$. If $α ⊙ u = 0$, then either $α = 0$ or $u = 0$.
# Subspaces - Definition and Examples

Since vector spaces are sets, it is convenient to use set notation. We denote sets by upper case letters in an outline font, such as $\mathbb{V}$ and $\mathbb{R}$. The format for a subset $\mathbb{S}$ of a set $\mathbb{W}$ is $\mathbb{S} = \{w ∈ \mathbb{W} \;|\; \text{property A}\}$. The ∈ is read “belongs to” or “is a member of” and the vertical line segment | is read “such that.” An element $w$ belongs to $\mathbb{S}$ only if $w$ is a member of $\mathbb{W}$ and if $w$ satisfies property A.

In particular, the set

$\mathbb{S} = \{\begin{bmatrix} x & y & z \end{bmatrix} ∈ \mathbb{R}^3 \;|\; y = 0\}$

is the set of all real 3-tuples, represented as row matrices, with a second component of zero.
# Linear independence of vectors

A set of vectors ${v_1,v_2,…,v_n}$ in a vector space $\mathbb{V}$ is linearly dependent if there exist scalars, $c_1,c_2,…,c_n$, not all zero, such that

$\large c_1v_1 + c_2v_2 + … + c_nv_n = 0$

The vectors are linearly independent if the only set of scalars that satisfies the above equation is the set $c_1 = c_2 = … = c_n = 0$.

All the vectors in the set need not be a linear combination of the preceding vectors for the set to be linearly dependent; there need only be one such vector for the whole set to be linearly dependent.
## Theorems

#### I. A subset of a vector space $\mathbb{V}$ consisting of a single vector $u$ is linearly dependent if and only if $u = 0$

#### II. A subset of a vector space $\mathbb{V}$ consisting of two distinct vectors is linearly dependent if and only if one vector is a scalar multiple of the other

#### III. A set of vectors in a vector space $\mathbb{V}$ that contains the zero vector is linearly dependent

#### IV. If a set of vectors $\mathbb{S}$ in a vector space $\mathbb{V}$ is linearly independent, then any subset of $\mathbb{S}$ is also linearly independent

#### V. If a set of vectors $\mathbb{S}$ in a vector space $\mathbb{V}$ is linearly dependent, then any larger set containing S is also linearly dependent
# Linear span

Spanning set is a set of vectors $\mathbb{S}$ in a vector space $\mathbb{V}$, for $\mathbb{V}$ if every vector in $\mathbb{V}$ can be written as a linear combination of vectors in $\mathbb{S}$
# Basis and dimension

If $\mathbb{S}$ is a spanning set for a vector space $\mathbb{V}$, then $\mathbb{S}$ is said to span $\mathbb{V}$. As a spanning set, $\mathbb{S}$ represents $\mathbb{V}$ completely because every vector in $\mathbb{V}$ can be gotten from the vectors in $\mathbb{S}$.

If we also require that $\mathbb{S}$ be a linearly independent set, then we are guaranteed that no vector in $\mathbb{S}$ can be written as a linear combination of other vectors in $\mathbb{S}$. Linear independence ensures that the set $\mathbb{S}$ does not contain any superfluous vectors.

A spanning set of vectors that is also a linearly independent set meets all our criteria for efficiently representing a given vector space. We call such a set a basis.
# Co-ordinate representation of vectors

In coordinate representation, a vector is described using its components along each axis. For example, in 2D space, a vector $\vec{v}$ can be represented as:

$\vec{v} = \begin{bmatrix} v_x \\ v_y \end{bmatrix} = v_x\begin{bmatrix} 1 \\ 0 \end{bmatrix} + v_y\begin{bmatrix} 0 \\ 1 \end{bmatrix}$

where $v_x$ and $v_y$ are the coordinates along the $x$- and $y$-axes, respectively. This notation shows both direction and magnitude along each axis.

In 3D, a vector $\vec{v}$ includes a $z$-component as well:

$\vec{v} = \begin{bmatrix} v_x \\ v_y \\ v_z \end{bmatrix} = v_x\begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} + v_y\begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} + v_z\begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$

Here, $v_x$, $v_y$, and $v_z$ are the coordinates along the $x$-, $y$-, and $z$-axes.

The other component along with the coordinates are called the basis

Standard basis in $\mathbb{R}^2$ are $\left\{\begin{bmatrix} 1 \\ 0 \end{bmatrix},\begin{bmatrix} 0 \\ 1 \end{bmatrix}\right\}$<br><br>
likewise in $\mathbb{R}^3$, basis → $\left\{\begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}, \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}\right\}$ 
# Row Space and Column Space

## Row Space

The **row space** of a matrix $A$ is the set of all possible linear combinations of its rows, forming a subspace within the vector space $\mathbb{R}^n$ (for an $m \times n$ matrix). This space provides insights into the relationships between rows and helps analyze solutions to linear equations represented by the matrix.

To determine the row space:

1. **Row Reduction**: First, reduce the matrix to row echelon form or reduced row echelon form (RREF). This form highlights the linear dependencies between rows.
2. **Non-Zero Rows**: The non-zero rows in the RREF of the matrix act as a basis for the row space. Each of these rows spans a dimension in the subspace, so the number of non-zero rows corresponds to the dimension of the row space, also known as the **row rank** of the matrix.

In summary, the row space of a matrix is spanned by the non-zero rows of its row echelon form, capturing all linear combinations that can be formed by the rows of the original matrix.

**Span of vectors in a set means the basis of the row space of the matrix created by those vectors**

### Example

For a matrix A = $\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$​​, the row echelon form might be $\begin{bmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & 0 \end{bmatrix}​$​​. The non-zero rows $\begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$ and $\begin{bmatrix} 0 & -3 & -6 \end{bmatrix}$ form a basis for the row space.

## Column Space

The **column space** of a matrix $A$ is the set of all possible linear combinations of its columns, forming a subspace in $\mathbb{R}^m$ (if $A$ is $m \times n$). This space represents all potential outputs of the linear transformation defined by $A$, showing which values in $\mathbb{R}^m$ can be reached by multiplying $A$ by a vector in $\mathbb{R}^n$.

To determine the column space:

1. **Pivot Columns**: Perform row reduction to find the pivot positions in the row echelon form of the matrix. These pivots indicate the columns that are linearly independent.
2. **Original Columns**: Use the columns in the _original matrix_ that correspond to these pivot positions to form a basis for the column space. These columns represent all linearly independent directions within the subspace spanned by the columns.

The number of pivot columns is the **rank** of the matrix and gives the dimension of the column space.

### Example

For $A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$, if row reduction reveals that columns 1 and 2 contain pivots, then the first two columns $\begin{bmatrix} 1 \\ 4 \\ 7 \end{bmatrix}​$​​ and $\begin{bmatrix} 2 \\ 5 \\ 8 \end{bmatrix}​$ form a basis for the column space.
