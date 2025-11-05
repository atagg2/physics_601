# Mathematical Physics Notes

## 1.1 Sets

* Elements in a set: $a \in A$
* Set definitions: $\{x^n \; | \; \text{n is a natural number}\}$ or $\{x^n\}_{n \in N}$
* Subsets: $B \subset A$
* Union: $A \cup B$
* Intersection: $A \cap B$
* Difference: $A \sim B = \{ a \; | \; a \in A \text{ and } a \notin B\}$
* Compliment: $\sim A$
* Catesian product: $A \times B = \{ (a,b) \; | \; a \in A \text{ and } b \in B\}$

### Equivalence relations

* Relation on A: $a \triangle b \text{ if } (a,b) \in A \text{ passes the specified test}$ - grouping together elements in a set
* Equaivalence relations are relations with the following properties
    * $a \triangle a \; \forall a \in A$
    * $a \triangle b \implies b \triangle a \; \; a,b \in A$
    * $a \triangle b \text{, and } b \triangle c \implies a \triangle c \; \; a,b,c \in A$
* Equivalence class: $[[a]] = {b \in A \; | \; b \triangle a}$ - set of all elements that are equivalent to $a$
* Partition: $\{[[a]] \; | \; a \in A \}$ - The set of all equivalence classes of $A$ partitions $A$ meaning their union encompasses $A$ and there is no intersection between them
* This is called a quotient set or factor set denoted as $A$ / $\triangle$ 
* If the equivalence relation on $R^3$ is defined by two points lying on the same line the passes through the origin, then the quotient set $R^3$ / $\triangle$ is the set of all lines in space passing through the origin

## 1.2 Maps

* A map from set $X$ to set $Y$ is denoted by $f \; : \; X \to Y$
    * Each element of $X$ corresponds to only one element of $Y$, not the other way arround. (so not all of $Y$ necessarily has to be covered by $f$)
* Range: subset $f(X) \subset Y$
* Image: $f(x)$ is the image of $x$ under $f$
* Domain: $X$
* Codomain: $Y$ is the codomain
* Function: a map whose codomain is $R$ or $C$ (reals or complexes)
* Graph: $\Gamma_f = \{ (a, f(a)) \; | \; a \in A \} \subset A \times B$
    * In algebra and calculus $A = B = R$ and $A \times B$ is the xy plane
* Preimage: $f^{-1}(B) = \{ x \in X \; | \; f(x) \in B\}$ all elements of x whose images are in $B \subset Y$
    * If $B$ consists of a single element $b$ then $f^{-1}(b) = \{ x \in X \; | \; f(x) = b\}$ consists of all elements of $X$ that are mapped to $b$
* Composition: $f \; : \; X \to Y$ and $g \; : \; Y \to W$, then the mapping $h \; : \; X \to W$ given by $h(x) = g(f(x))$
* Injective: $f(x_1) = f(x_2) \implies x_1 = x_2$
    * 1 value of $Y$ has only 1 value of $X$
* Surjective: $f(X) = Y)$
    * The range of $f$ covers the entre space of $Y$
    * 1 value of $X$ has only one value of $Y$
* Bijective: injective and surjective - one to one, invertable
* Defining an equivalence relation $\triangle$ by $x_1 \triangle x_2$ if $f(x_1) = f(x_2)$ Equivalence classes are subsets of $X$ whose elements map to a single $Y$
    * $[[x]] = f^{-1}(f(x))$

## 1.4 Cardinality

* Cardinality: 2 sets with the same cardinality have the same number of elements

### Things to think about

1. Let $A$ be a subset of the integers $\{a \mid 1 \le a \le 9\}$. Let $B$ be another subset of the integers $\{b \mid 7 \le b \le 12\}$. What is $A \sim B$?

$A \sim B = \{ a \; | \; 1 \le a < 7 \}$

2. Let $A$ be a subset of the integers $\{a \mid 1 \le a \le 9\}$. Define a partition $B_\alpha$ of this set.

$B_{\alpha} = \{[[1]], [[2]], [[3]], [[4]], [[5]], [[6]], [[7]], [[8]], [[9]]\}$

3. Invent an example of an equivalence class composed of (some of the) complex numbers in the complex plane.

All points that lie on the unit circle

$\mathbb{C} / \triangle = \{a \in \mathbb{C} \; | \; |a| = 1\}$

4. Consider the mapping $f: \mathbb{R} \to \mathbb{R}$ where $f(x) = e^x$.  
   - Is this mapping injective? - Yes
   - Surjective? - No
   - Bijective? - No

   How about the function (with the same domain and codomain) $f(x) = e^{\cos x}$?

Not injective, surjective, or bijective 

5. 1-to-1 and onto are not synonyms. How can a mapping be 1-to-1 but not onto? Or vice versa? Give an example.

1-to-1 means injective, onto means surjective.  An example of injective but not surjective would be $e^x : \mathbb{R} \to \mathbb{R}$.  An example of surjective but not injective would be $cos(x): \mathbb{R} \to (-1, 1)$ 

6. Is the cardinality of the integers greater than the cardinality of the even integers?

No, they are the same


## 2.1 Vector spaces

**Vector spaces**: The set of vectors in which the folowing is defined

* Vector addition is defined
    * $a + b = b + a$
    * $a + (b + c) = (a + b) + c$
    * zero vector is defined as 0 where $a + 0 = a$
    * $a + -a = 0$
* Scalar multiplication is defined
    * $\alpha (\beta a) = (\alpha \beta) a$
    * $1 a = a$ 
* Scalar multiplication is distributive
    * $\alpha (a + b) = \alpha a + \alpha b$
    * $(\alpha + \beta) a = \alpha a + \beta a$

**Field**: A field is a set of objects that have two binary operations defined: addition and multiplication

**Subspaces**: The subpsace $W$ is a subset of the vector space $V$ such that if $a,b \in W$ then $\alpha a + \beta b \in W$ for all $\alpha, \beta \in \mathbb{C}$

**Basis**: The basis $B$ of vector space $V$ is a set of linearly independent vectors that span all of $V$

Theorem - All bases of a finite-dimensional vector space have the same number of linearly independant dasis vectors

**Factor space**: $W$ is a subspace of $V$. $V / W = \{ v + W \; | \; v \in V\}$.  where $v + W = \{ v + w \; | \; w \in W\}$

**Direct sum**: $U$ and $W$ are subspaces of $V$. $V$ is a direct sum of $U$ and $W$ if $V = u + W$ and $U \cap W = \{0\}$.  $U + W$ is the set of vectors that can be written as the sum of a vector in $U$ and a vector in $W$

Proposition - If a vector space $V$ is the direct sum of the subspaces $\{U_i\}_{i=1}^r$, then the subspaces are linearly independant.

## 1.3 Metric spaces

A set $X$ together with a real valued function $d : X \times X \to \mathbb{R}$ such that

* $d(x,y) \ge 0 \; \forall x, y$, and $d(x, y) = 0$ iff $x = y$ 
* $d(x,y) = d(y,x)$
* $d(x,y) \le d(x,z) + d(z,y)$


$d$ is the astracted notion of distance

Euclidean space is a metric space

# 2 Vectors and Linear Maps

## 2.2 Inner product

Inner products in complex vector spaces are defined with conjugation: $\langle \bar{u}, v \rangle$

**Inner product space**: A vector space with a defined inner product

For infinite-dimensional vector spaces, the inner product is

$$\int_a^b w(x) f(x) g(x)$$

### 2.2.1 Orthogonality

If $\langle a, b \rangle = 0$ then $a$ and $b$ are orthogonal.

An orthonormal basis means

$$\langle e_i, e_j\rangle = \delta_{ij} = \begin{cases}
1 & \text{if} \; i = j \\
0 & \text{if} \; i \ne j
\end{cases}$$


### 2.2.2 Grahm Schmidt process

Starting with the basis $B = \{ a_i\}_{i=1}^N$.  We create the first orthonormal basis

$$e_1 = \frac{a_1}{\sqrt{\langle a_1, a_1 \rangle}}$$

Then we subtract from $a_2$ its projection along $e_1$ then the result will be orthogonal to $e_1$

$$e_2' = a_2 - e_1 \langle e_1, a_2 \rangle$$

$$e_2 = \frac{e_2'}{\sqrt{\langle e_2', e_2' \rangle}}$$

Generalizing to $m$ orthonormal vectors

$$e_{m+1}' = a_{m+1} - \sum_{i=1}^m e_i \langle e_i, a_{m+1} \rangle$$

$$e_{m+1} = \frac{e_{m+1}'}{\sqrt{\langle e_{m+1}', e_{m+1}' \rangle}}$$

### 2.2.3 Schwarz Inequality

For any pair of vectors $a$ and $b$. in an inner product space $V$,

$$\langle a, a \rangle \langle b, b \rangle \ge |\langle a, b\rangle|^2$$

### 2.2.4 Length of a vector

The length of vector is defined by the square root of the inner product with itself

$$||a|| = \sqrt{\langle a, a \rangle}$$

The norm has the following properties

* $||0|| = 0$
* $||a|| \ge 0$ and $||a|| = 0$ if and only if $a = 0$
* $||\alpha a|| = |\alpha| ||a||$ for any complex $\alpha$
* $||a + b|| \le ||a|| + ||b||$

Any function on a vector space with these properties is a norm, and if the norm is defined then the vector space is a normed linear space.

You do not need an inner product to have a norm.

Distance can be defined by the norm

$$d(a,b) = ||a - b||$$

Inner product spaces are automatically normed spaces but the converse is not true

If the norm satisfies the parallelogram law

$$||a+b||^2 + ||a-b||^2 = 2||a||^2 + 2||b||^2$$

Then it is an inner product space.

Other possible norms can be defined as

$$\|a\|_p = \left( \sum_{i=1}^N |\alpha_i|^p \right)^{\tfrac{1}{p}}$$

where $a = (\alpha_1, \alpha_2, ... \alpha_i)$

## 2.3 Linear Maps

Linear maps preserve the structure of the input and output spaces.  Gven a map $F : V \to W$,

$$F(\alpha a + \beta b) = \alpha F(a) + \beta F(b) \; \forall a, b \in V \text{ and } \alpha, \beta \in \mathbb{C}$$

The set of all linear maps from $V$ to $W$ is denoted $L(V,W)$ and is a vector space.  The set of transformations from $V$ to itself is just $L(V)$

**Endomorphism**: A transformation from $V$ to $V$ is an endomorphism of $V$

The zero transformation $0$ takes every vector in $V$ to the zero vectro of $W$

An isometric map from $V4 to $W$ obeys the following

$$\langle Ta, Tb \rangle = \langle a, b \rangle \; \forall a, b \in V$$

This implies that the inner products are the same in both spaces

If $W = V$ then $T$ is an isometry of $V$ or unitary operator

### 2.3.1 Kernel (null space) of a linear map

For a linear map $T : V \to W$, every vector in $V$ that is mapped to the zero vector of $W$ is in the null space

**Rank**:  The rank of a linear map $T$ is the dimension of the range of $T$

If the null space is $0$ then the mapping is injective

Dimension theorem:

$$dim V  = dim \; ker V + dim T(V)$$

$T(V)$ is the range of $T$

### 2.3.2 Linear Isomorphism

A vector space $V$ is isomorphic to another vector space $W$ if there is a bijective linear map $T : V \to W$.  

$T$ is called an isomorphism.

**Automorphism**: A bijective linear map of $V$ onto itself, also called invertible linear map.  This is denoted by $GL(V)$ or $End(V)$

Two finite-dimensional vectro spaces are isomorphic if and only if they have the same dimension.  This means that all $n$ dimensional vector spaces over $\mathbb{R}$ are isomorphic to $\mathbb{R}^n$.  This is why the vector space defined by an interval on the real number line is isomorphic to the entire number line.

## 2.5 Linear functionals

For the linear map $T : V \to W$ if $W$ is the set of scalars, $\mathbb{C}$, or $\R$, then the map $T$ is a linear functional

### 2.5.2 Dual space and dual basis

The dual space of $V$ is the set of all linear functionals on $V$.  So the set of all linear scalar fields of $V$.  This is a vector space because you can make linear combinations of them.

Take an $N$-dimensional vector space $B = \{ a_1, a_2, \cdots, a_N\}$.  For any given set of $N$ scalars $\{ \alpha_1, \alpha_2, \cdots, \alpha_N\}$  the linear function $\phi_{\alpha}$ is defined by $\phi_{\alpha} a_i = \alpha_i$. For $\phi_{\alpha}$ acting on an arbitrary vector

$$\phi_{\alpha}b = \phi_{\alpha} \sum_{i=1}^N \beta_i a_i \ = \sum_{i=1}^N \beta_i \phi_{\alpha}a_i = \sum_{i=1}^N \beta_i \alpha_i$$

So the linear functional acting on a vector becomes a sum of scalar products.  This suggests that $b$ can be represented as a column vector with entries $\beta_1, \beta_2, \cdots,  \beta_N$ and $\phi_{\alpha}$ as a row vector with entries $\alpha_1, \alpha_2, \cdots, \alpha_N$. Then $\phi_{\alpha}b$ is just the dot product of the row vector and the column vector.  $b \cdot\phi_{\alpha}$

$\phi_{\alpha}$ is a map from the vector space to scalars \, and when it acts of the $i_{th}$ basis vector of the original vector space, it maps to the $i_{th}$ scalar in the predefined set $\{ \alpha_1, \alpha_2, \cdots, \alpha_N \}.$

$\phi_{\alpha}$ is uniquely determined by the set $\{\alpha_1, \alpha_2, \cdots,\alpha_N\}$.  Corresponding to every set of $N$ scalars, there exists a unique linear functional.  There is a particular set of functionals $\phi_1, \phi_2, \cdots, \phi_N$ that correspond to the sets of scalars $\{1,0,0,\cdots,0\}, \{0,1,0,\cdots,0\}, \cdots, \{0,0,0,\cdots,1\}.$

This means that 

$$\phi_i a_j = \delta_{ij}$$

Remember that $\phi_ia_j$ is the dot product of $\beta_1, \beta_2, \cdots,  \beta_N$ and $\alpha_1, \alpha_2, \cdots, \alpha_N$.  So this is saying $\phi_1$ maps $a_1$ (the first basis) to $1$, and maps all other bases to $0$.

These particular functionals $\phi_1, \phi_2, \cdots, \phi_N$ form a basis of the dual space.

For a vector space with $N$ bases, there is a unique dual space with $N$ bases, and is isomorphic to the original space.

Every vector $a \in V$ is uniquely determined by its components $(\alpha_1, \alpha_2, \cdots, \alpha_N)$ in a basis $B$.  The unique linear functional $\phi_a$ corresponding to $a$ is 

$$\phi_a = \sum_{i=1}^N \alpha_i \phi_i$$ 

where $\phi_i \in B^*$.  This means that the dual of a vector is that same vector's coefficients,but just in a different basis.

$a$ is thought of as a column of numbers. In the basis $B^*$,  the linear transformation of $a$ is a row of numbers.  The row of numbers is called $\phi_a$ and belongs to the dual space $V^*$.  $\phi_a$ is dual to $a$

The dual of the linear transformation $T : V \to U$ is defined as $T^* : U^* \to V^*$ by

$$[T^*(\gamma)]a = \gamma(Ta) \; \forall a \in V, \gamma \in U^*$$ 

On the left, $\gamma$ is a vector in $U^*$ and gets transformed by $T^*$ into a vector in $V^*$, then it gets dotted with $a$, which is in $V$ to make a single scalar.  On the right, $a$ gets transformed by $T$ to a vector in $U$.  Then that gets dotted with a vector $\gamma$ whic is in $U^*$ to get the same scalar as on the left.

The operation that "duals" a vector follows

$$(\alpha|a\rang + \beta|b\rang)^\dag = \alpha^* \lang a| + \beta^* \lang b |$$

where the $*$ superscript denotes complex congugation and $\lang a|$ is the dual of $|a \rang$

So if 

$$| a \rang = \begin{pmatrix}
\alpha_1 \\ 
\alpha_2 \\
\vdots \\
\alpha_n

\end{pmatrix}$$


The dual is

$$\lang a | = (\alpha_1^*, \alpha_2^*, \cdots, \alpha_n^*)$$

And the inner product is written as 

$$\lang a | b \rang = (\alpha_1^*, \alpha_2^*, \cdots, \alpha_n^*)\begin{pmatrix}
\beta_1 \\ 
\beta_2 \\
\vdots \\
\beta_n

\end{pmatrix} = \sum_{i=1}^n \alpha_i^* \beta_i$$

# 3 Algebras
An Algebra is a vector space with a defined vector-vector product (like matrix multiplication)

## 3.1 From vector space to Algebra
Multiplication of two vectors $(a,b) \in A \times A$ must satisfy the following

$$a(\beta b + \gamma c) = \beta ab + \gamma ac$$
$$(\beta b + \gamma c)a = \beta ba + \gamma ca$$

for all $a,b,c \in A$ and $\beta, \gamma \in \mathbb{C}$ (or $\R$)

**Associative:** An algebra is associative if $a(bc) = (ab)c$

**Communitive:** An algebra is associative if $ab = ba$

**Identity:** An algebra with an identity $1$ satisfies $1a = a$

**Left inverse:** $b$ is the left inverse of $a$ if $ba = 1$

**Right inverse:** $b$ is the right inverse of $a$ if $ab = 1$

### 3.1.1 General properties 

$$a0 = 0a = 0$$

The identity of an algebra is unique.  If $1$ and $e$ were both identities, then $1e = e$, $1e = 1$

In associative algebras, there is no difference between left and right inverses - but why do we talk about left inverses and right inverses sometimes in linear algebra?

**Matrix algebra:** the space of all $n \times n$ matrices, with multiplication defined as the matrix multiplication.  This is associative but not communitive

**Subalgebra:** if $A'$ is a subspace of $A$, and $ab \in A' \; \forall a,b \in A'$ then $A'$ is a subalgebra of $A$ 

**Center:** If $A$ is an algebra, the set of elements which commute with all elements of $A$ is the center and is a subalgebra of $A$

**Central:** An algebra is central if its center is $Span\{1\}$

**Structure constants:** Given the basis $B \{e_i\}_{i=1}^N$ 

$$e_ie_j = \sum_{k=1}^Nc_{ij}^k e_k$$

$c_{ij}^k$ are the structure constants of the algebra.  You can define an algebra with a vector space, basis, and structure constaints

For example, in the classical cross product definition,

$$a \times b = (a_yb_z - a_zb_y, a_zb_x - a_xb_z, a_xb_y - a_yb_x)$$

given the basis $\{e_x, e_y, e_z\}$

$$e_xe_y = 0e_x + 0e_y + 1e_z$$
$$e_ye_x = 0e_x + 0e_y - 1e_z$$
$$e_xe_z = 0e_x -1e_y + 0e_z$$

and so on.  This algebra has $27$ structure constaints - $3$ for each of the $9$ combinations of $i$ and $j$

**Generator:** A subset of an algebra $A$ is a generator of $A$ if $A$ can be spanned by a linear combination of the products of the subset. Bases are always generators, but they are not the smallest ones.  For example, the algebra $(\R^3, \times)$ has the basis $\{e_x,e_y,e_z\}$, but $\{e_x, e_y\}$ is a generator because $e_z = e_x \times e_y$

### 3.1.2 Homomorphisms

Linear maps between algebras that satisfy

$$\phi(ab) : A \to B = \phi(a)\phi(b)$$

Are called homorphisms.  They are linear maps that are not bijective.  An example is $f(x) = 1$ 

**Monomorphism:** An injective homorphism

**Epimorphism:** A surjective homorphism

**Isomorphism:** A bijective homorphism

**Automorphism:** An isomorphism of an algebra onto itself

## 3.2 Ideals

Subalgebras whose elements are stable under the whole algebra (when multiplied by elements in the whole algebra, they still stay in the subalgebra)

**Left ideal:** A subspace $B$ of $A$ is a left ideal of $A$ if it contains $ab$ for all $a \in A$ and $b \in B$.  Written $AB \subset B$

**Right ideal:** $BA \subet B$

**Ideal:** both left and right ideal

**Minimal ideal:** An ideal of $A$ is minimal if every ideal of $A$ contained in $M$ coincides with $M$.  Does this mean there are no other ideals contained within $M$ other than $M$ itself?

If $A$ is a direct sum of subalgebras, then each subalgebra is an ideal of $A$.  Any other ideal of $A$ is contained entirely in one of the components of this direct sum

### 3.2.1 Factor algebras

If $A$ is an algebra and $B$ is a subspace of $A$, then the factor space $A/B$ can be turned into an algebra if and only if $B$ is an ideal in $A$

Example - $A$ is the algebra of real polynomials $\R[x]$ and $B$ is all polynomials of the form $f(x)(x^2 + 1)$ (every polynomial with factor $x^2 + 1$).  $B$ is an ideal in $A$ because multiplying by any other polynomial in $A$ will still be in $B$.

$A/B$ is a factor space - every element is an equivalents class of polynomials modulo $x^2 + 1$

$$f(x) = g(x) \text{ if } f(x) - g(x) \in x^2 + 1$$

## 3.3 Total matrix algebra

The vector space of $n \times n$ matrices with a basis $\{ e_{ij}\}_{i,j = 1}^n$ where $e_ij$ has a $1$ at the $ij$th position and a zero everywhere else.  This basis has $n^2$ vectors in it. 

$$(e_{ij})_{lk} = \delta_{il} \delta_{jk}$$

This is saying that the $lk$th element of $e_{ij}$ is zero everywhere except when $k = j$ and $l=i$

$$(e_{ij}e_{kl})_{mn} = \sum_{r=1}^n (e_{ij})_{mr}(e_{kl})_{rn}$$

$$= \sum_{r=1}^n \delta_{im}\delta_{jr}\delta_{kr}\delta_{ln} = \delta_{im}\delta_{jk}\delta_{ln} = \delta_{jk}(e_{il})_{mn}$$

$$e_{ij}e_{kl} = \delta_{jk}e_{il}$$

structure constants are $c_{ij,kl}^{mn} = \delta_{im}\delta_{jk}\delta_{ln}$

# 4 Operator algebra

Algebra of linear transformations

## 4.1 Algebra of $End(V)$

The product in the vector space of endomorphims $End(V)$ is defined as the composition of maps.  It has the zero element and the identity.

Only automorphims of a vector space are invertible

The inverse of a linear operator is unique.  If $T$ and $S$ are invertible linear operators, then $TS$ is also invertible and $(TS)^{-1} = S^{-1}T^{-1}$

An endomorphism $T \in End(V)$ is invertible iff it sends a basis of $V$ onto another basis of $V$

### 4.1.1 Polynomials of operators

We can construct polynomials of operators

$$p(T) = \alpha_01 + \alpha_1T + \alpha_2T^2 + ... + \alpha_nT^n$$

Negative powers of an operator are defined as $T^{-n} = (T^{-1})^n$ 

A great example of products of operators and inverses of operators is in the Hassani book pg 103-104

### 4.1.2 Functions of operators

Going beyond polynomials to general functions of operators.

We use the taylor series expansion.

$$f(x) = \sum_{k=0}^{\infty} \frac{(x - x_0)^k}{k!} \left. \frac{d^kf}{dx^k} \right|_{x=x_0} $$

To generalize this to operators,

$$f(T) = \sum_{k=0}^{\infty} \frac{(T - x_01)^k}{k!} \left. \frac{d^kf}{dx^k} \right|_{x=x_0} $$

## 4.2 Derivatives of operators

Operators can be dynamic For the mapping $H : \R \to End(V)$ The derivative can be expressed as

$$\frac{dH}{dt} = \lim_{\Delta t \to 0} \frac{H(t + \Delta t) - H(t)}{\Delta t}$$

## 4.3 Conjugation of operators

If there is a map $c = Tb$ then there is another map $c^{\dagger} = b^{\dagger} T^{\dagger}$ 

$T^{\dagger}$ is the adjoint or hermitian conjugate

The definition of the adjoint is

$$(a^{\dagger} T b)^{\dagger} = b^{\dagger} T^{\dagger} a$$

Operators can also be decomposed inot real and imaginary parts

$$T = X + iY$$

**Hermitian:** A linear operator is hermitian if $H^{\dag} = H$

For a hermitian operator,  $a^{\dag}Ha$ is real

**Positive definite:** An operator is positive definite if $a^{\dag} H a > 0$ for all $a \neq 0$.  Positive definite operators are invertible

### 4.3.2 Unitary operators

Unitary operators preserve distances and the scalar product

If $U$ is a unitary operator, and $a' = Ua$ and $b' = Ub$ then $\lang a', b' \rang = \lang a, b \rang$

In other words, $U$ preserves distances and angles

$$U^{\dag}U = 1$$

The common example is rotation and translation

## 4.4 Idempotents

Linear maps with the property $P^2 = P$.  These are like projections onto subspaces where if something is already in the subspace, then the projection does not change it.  $P_x(x,y) = (x,0)$

### 4.4.1 Projection operators

A projection operator is a hermitian idempotent.  (hermitian meaning $T^{\dag} = T$)

if $P_1$ and $P_2$ are projection operators, then $P_1 + P_2$ is also a projection operator iff $P_1$ and $P_2$ are orthogonal meaning $P_1P_2 = P_2P_1 =  0$

Given a normal vector $e$, $e e^{\dag}$ is a projection operator

$$P_y = \frac{yy^{\dag}}{y^{\dag}y}$$

or 

$$P_y = \frac{|y\rang \lang y|}{\lang y|y\rang}$$

$P_y x$ is the projection of $x$ along $y$

## 4.5 Representation of algebras

A real (or complex) representation of an algebra $A$ in a vector space $V$ is a mapping $\rho : A \to End_{\R}(V)$

An example is the real representation of quaternions from the book pg 126 where 

$$\rho(q) = \begin{pmatrix} 
q_0 & -q_1 & -q_2 & -q_3 \\
q_1 & q_0 & -q_3 & q_2 \\
q_2 & q_3 & q_0 \cdots
\end{pmatrix}$$

Or perhaps the real representation the algebra of complex numbers?

## 5.4 Change of basis

there is a matrix that represents a change of basis

$$a' = Ba$$

The $ij$th component of $B$ is calculated by $\rang e_i | e_j' \lang$

More details on pg 150

## 6.1 Invariant supspaces

$M$ is a subspace of $V$.  $M^\perp$ is the set of all vectors in $V$ that are orthogonal to $M$ 

We can make subspaces of a finite dimensional vector space using a linear operator $A$

$$a, Aa, A^2a, \cdots$$

Are all linearly independant and span a subspace $M = Span \{ A^k a\}$

for any vector $x \in M$, $Ax$ is also in $M$

**Invariant supcae:**  the subspace $M$ is an invariant subspace of the operator $A$ if $A$ transforms vectors from $M$ into vectors of $M$.  $A(M) \subset M$

$M$ reduces $A$ if $M$ and $M^{\perp}$ are invariant subspaces of $A$

Think of block diagonal matrices for this

$$\begin{pmatrix} 1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 2 \end{pmatrix}$$

$M$ is the $x-y$ plane, and $M^{\perp}$ is the $z$ axis 

Both are subspaces of $V$ that are invariant under $A$

## 6.4 Complex Spectral Decomposition

**Normal Operator:** An operator that commutes with its adjoint (must act on an inner product space)

If it is normal, the operator satisfies

$$||Ax|| = ||A^{\dag}x||$$

Any invariant subspace of a normal operator reduces that operator

If $x$ is an eigenvector of $A$ with eigenvalue $\lambda$ then $x$ is also an eigenvalue of $A^{\dag}$ with eigenvalue $\lambda^*$ ($A$ must be normal)

If we apply this to a hermitian operator we get 

$$Hx = \lambda x = H^{\dag}x = \lambda^*x$$

therefore

$$\lambda = \lambda^*$$

which means $\lambda$ is real

For a unitary operator we get 

$$\lambda \lambda^* = 1$$

And $\lambda$ has absolute value of $1$

An eigenspace of a normal operator reduces that operator, and the eigenvectors of a normal operator are orthogonal

**Complex Spectral Decomposition Theorem:**

Let $A$ be a normal operator on a finite-dimensional complex inner product space $V$, and let $\lambda_1, \lambda_2, \cdots, \lambda_n$ be it's eigenvalues. Then

$$V = M_1 \oplus M_2 \oplus \cdot \oplus M_n$$

where $M_i$ is the eigenspace corresponding to $\lambda_i$

And the projection operators 

$$P_1, P_2, \cdots, P_n$$

where $P_i$ projects onto $M_i$ satisfy

$$1 = \sum_{i=1}^n P_i$$

$$P_iP_j = 0 \text{, for } i \ne j$$

$$A = \sum_{i=1}^n \lambda_i P_i$$

A normal operator is diagonalizable and a diagonalizable operator is normal

The largest eigenvalue can be approximated by

$$\lambda_1 = \lim_{m \to \infty} \frac{\lang y | A^{m+1} | x \rang}{\lang y | A^{m} | x \rang}$$

## Polar Decomposition

Any matrix $A$ can be decomposed as

$$A = UR$$

where 

$$R^2 = A^{\dag}A$$

and

$$U = AR^{-1}$$

### 6.4.1 simultaneous diagonalization

Two operators are simultaneously diagonalizable if they can be written

$$A_1 = P \Lambda_1 P^{-1}$$

$$A_2 = P \Lambda_2 P^{-1}$$

I \frac{1}{\sqrt{3}}\begin{pmatrix} 1 \\ -i \\ 1\end{pmatrix}n other words, they share the same eigenvectors, but have different eigenvalues

## 7 Hilbert spaces

Infinite dimensional vector spaces

Convergence of infinite series

## 8 Classical orthogonal polynomials

Legendre

$$a_n = \frac{2n + 1}{2}\int_{-1}^1 f(x) P_n(x) dx $$

Hermite

$$a_n = \frac{1}{\sqrt{\pi} 2^n n!}\int_{-1}^1 f(x) H_n(x) e^{-x^2}dx $$


## 9.1 Fourier Series

The Fourier series expansion of $f(x)$ is

$$F(x) = \frac{1}{2}A_0 + \sum_{n=1}^{\infty} \left( A_n \cos \frac{2 n \pi x}{L} + B_n \sin \frac{2 n \pi x}{L} \right)$$

$$A_n = \frac{2}{L} \int_a^b \cos \frac{2 n \pi x}{L} F(x) dx$$
$$B_n = \frac{2}{L} \int_a^b \sin \frac{2 n \pi x}{L} F(x) dx$$


## 9.2 Fourier transform

To get to the fourier transform, we consider expanding a fourier series over the interval $(-\infty, \infty)$.  If we separate our function copies by extending the period by $\Delta$ on either side, as $\Delta \to \infty$, the infinite sum of the fourier series becomes an integral

$$F(\omega) = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty} f(x) e^{-i \omega x}dx$$

And the inverse transform is


$$f(x) = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty} F(\omega) e^{-i \omega x}d \omega$$

### 9.2.2 Fourier transforms and derivtives

The fourier d\transform turns derivatives into multiplication due to the nature of the exponential

$$\frac{df}{dx} = \int_{-\infty}^{\infty} F(\omega) -i \omega e^{-i \omega x}dx$$

### 9.2.3 Discrete fourier transform

Discrete fourier transform is a way to go from the time domain to frequency domain with discrete measurements.  It basically tells you what highest frequency content of your signal is.

## 23.1 Groups

**Group:** A set $G$ together with a defined binary operation called multiplication.  The set contatins an identity element $ge = eg = g$, and the inverse $gg^{-1} = e$ 

Examples:

* The set of integers whose binary operation is addition
* The set $\{ -1, 1\}$ with the binary operation of multiplication

**Transformation group:** the set of invertible mappings of a set onto itself

**Abelian group:** all elements commute: $ab = ba \forall a, b \in G$

**Homomorphism:** f(a*b) = f(a)*f(b)

**Isomorphism:** a homomorphism that is also a bijection

**General Linear group:** $GL(V)$ the set of all invertible endomorphisms of $V$

**Subgroup:** a subgroupd $S$ of $G$ is a group in it's own right under the binary operation of $G$

## 23.2.1 Direct products

A groupd $G$ is a direct product of two subgroups $H_1$ and $H_2$ $G = H_1 \times H_2$ if 

* All elements of $H_1$ commute iwth all elements of $H_2$
* the group identity is the only element in common between $H_1$ and $H_2$
* every elements $g \in G$ can be written as $g = h_1h_2$ where $h_1 \in H_1$ and $h_2 in H_2$


## 23.3 Group Action

The left action of group $G$ on set $M$ is a mapping $\phi : G \times M \to M$ such that

* $\phi(e,m) = m \;\; \forall m \in M$
* $\phi(g_1g_2, m) = \phi(g_1, \phi(g_1, m))$

Think of it as moving from one point in $M$ to another point in $M$ through the action $g \in G$

The mapping $\phi(g,m)$ is denoted as $gm$

The **orbit** of m is denote as $Gm$

$$Gm = \{x \in M | x = gm \text{ for some } g \in G\}$$

This is all the points in $M$ that can be reached from the single point $m$ by any transformation in the group $G$

**Transitive:** $Gm = M$ - the whole set can be reached by the transformations in $G$

**Stabilizer of m:** $G_m = \{g \in G | gm = m\}$ - the group of transformations that just map $m \to m$

**Free action:** if $G_m = \{e\} \; \forall m \in M$ - meaning the only stabilizer for any $m$ is the identity

**Effective:** if $gm = m$ implies that $g = e$

Read over remark 23.3.1 on page 714 - this helps a lot

two points are connected by a unique element of $G$ iff $G$ acts freely on the orbit

Think of a free action as the condition that there is no point in $M$ from which no transformation $G$ can take you to a new point - like rotations on the point at the origin will only give you the origin, there is no escape from the origin.

effective: no g is stuck for all m
free: no g is stuck for any m


## 23.4 Symmetric (permutation) group

the permutation $\pi$ defined with the product $\pi_2(i) * \pi_1(i) = \pi_2(\pi_1(i))$

**r_cyle:** generated by $i$ is the set of $r$ distinct elements $\{\pi^r(i)\}_{k=0}^{r-1}$ where $\pi^r(i) = i$ - its the elements that appear in a cycle that takes us from $i$ all the way back to $i$ by some defined permutaion $\pi$

Start with $1$ and apply  $\pi$ to it repeatedly until you obtain $1$ again. The collection of elements so obtained forms a cycle in which $1$ is contained. Then we select a second number that is not in this cycle and apply $\pi$ to it repeatedly until the original number is obtained again. Continuing in this way, we produce a set of disjoint cycles that exhausts all elements of $\{1,2,...,n\}$.

Any permutation can be boken up into disjoint cycles

## 24.1 Representations of groups

Let $G$ be a group and $H$ a Hilbert space.  A representation of $G$ on $H$ is a homomorphism $T : G \to GL(H)$

**faithful:** the representation is faithful if it is bijective

**equivalent:** two representations $T: G \to GL(H)$ and $T' : G \to GL()H'$ are equivalent if there exists an isomorphism $f : H \to H'$ such that $T' = f \circ T \circ f^{-1}$ for all $g \in G$

A representation $T : G \to GL(H)$ defines an action of a group $G$ on a Hilbert space $H$ by $\phi(g, |a \rang) = T_g |a \rang$ 

For a Hamiltonian $\mathbf{H}(x)$ with a group of symmetry $G$

$$T_g [\mathbf{H}(x)]T_g^{-1} = \mathbf{H}(x \cdot g)$$


The action of the group on a function is defined by

$$(T_g \psi)(x) = \psi(x \cdot g)$$

where $(T_g \psi)$ is a new function

Applied to matrices where multiplication is most natural on the left,

$$(T_g \psi)(x) = \psi(g^{-1}x)$$


