# Vector Spaces

Matrices, directed line segments (vectors) and polynomials are seemingly unrelated concepts, but:
- they are all closed under addition
- they are all closed under scalar multiplication
- zero matrix, polynomial and vector are similar

Similarly, there are many regularities between many such concepts. The question is “What is the minimum number of regularities that are required so that every other regularity will follow?”. This is announced by the label **“Vector Space”**.

A vector space is a collection of vectors that satisfy a set of axioms/rules.

Suppose there are objects $u,v,w…$ belong to vector space $\mathbb{V}$.

Thus, vector space can be defined as a set of objects $V = {u,v,w…}$ and scale as ${α,ß,Γ…}$ along with a binary operation of vector addition denoted by ⊕, and scalar multiplication denoted by ⊙ which possesses the following 10 properties:

- A1 - Close under addition: If $u,v ∈ V$, then $u ⊕ v ∈ V$
- A2 - Commutative law of addition: $u ⊕ v = v ⊕ u$ for $u,v ∈ V$
- A3 - Associative law for addition: $u ⊕ (v ⊕ u) = (u ⊕ v) ⊕ w$ for $u,v,w ∈ V$
- A4 - If a zero vector in $\mathbb{V}$, denoted by zero such that for every vector $u$ in $\mathbb{V}$, $0 ⊕ u = u ⊕ 0 = u$
- A5 - For every vector *u* in V, for a *-u* in V, *u ⊕ -u* = 0<br><br>
- S1 - Closure under scalar multiplication: If $u ∈ V$, then $α ⊙ u ∈ V$ for any scalar $α$
- S2 - For any two scalars $α$ and $ß$, and any vector $u$ in $\mathbb{V}$, $α ⊙ (ß ⊙ u) = (αß) ⊙ u$
- S3 - For any vector $u$ in $\mathbb{V}$, $1 ⊙ u = u$
- S4 - For any 2 scalar $α$ and $ß$, and any vector $u$ in $\mathbb{V}$, $(α + ß) ⊙ u = α ⊙ u ⊕ ß ⊙ u$
- For any scalar $a$ and any two vectors $u$ and $\mathbb{V}$ in $\mathbb{V}$, $α ⊙ (u ⊕ v) = α ⊙ u ⊕ α ⊙ v$


## Theorems

#### 1. For any vector $u$ in a vector space $\mathbb{V}$, $0 ⊙ u = 0$

#### 2. In any vector space $\mathbb{V}$, $α ⊙ 0 = 0$, for every scalar $α$

#### 3. The additive inverse of any vector $\mathbb{V}$ in a vector space $\mathbb{V}$ is unique

#### 4. The zero vector in any vector space $\mathbb{V}$ is unique

#### 5. For any vector $w$ in a vector space $\mathbb{V}$, $-1 ⊙ w = -w$

#### 6. For any vector $w$ in a vector space $\mathbb{V}$, $-(-w) = w$

#### 7. Let $α$ be a scalar and $u$ a vector in a vector space $\mathbb{V}$. If $α ⊙ u = 0$, then either $α = 0$ or $u = 0$.
# Subspaces - Definition and Examples

Since vector spaces are sets, it is convenient to use set notation. We denote sets by upper case letters in an outline font, such as $\mathbb{V}$ and $\mathbb{R}$. The format for a subset $\mathbb{S}$ of a set $W$ is $S = \{w ∈ W \;|\; \text{property A}\}$. The ∈ is read “belongs to” or “is a member of” and the vertical line segment | is read “such that.” An element w belongs to S only if w is a member of W and if w satisfies property A.

In particular, the set

$S = \{\begin{bmatrix} x & y & z \end{bmatrix} ∈ \mathbb{R}^3 \;|\; y = 0\}$

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

# Row space and Column space

