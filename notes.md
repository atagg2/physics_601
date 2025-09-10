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

**Automorphism**: A bijective linear map of $V$ onto itself, also called invertible linear map.  This is denoted by $GL(V)$

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

### 3.1.2 Homorphisms

Linear maps between algebras that satisfy

$$\phi(ab) : A \to B = \phi(a)\phi(b)$$

Are called homorphisms


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


