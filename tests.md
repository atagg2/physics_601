## 1

a) Construct a vector space using a scalar field of your choice and the set of $2 \times 2$ matrices with complex entries.  Show that all the properties of a vector space hold under your construction

Let $V = \mathbb{C}^{2 \times 2}$

First we must define vector addition

$$A + B = \begin{pmatrix}

a_{11} + b_{11} & a_{12} + b_{12} \\

a_{21} + b_{21} & a_{22} + b_{22}

\end{pmatrix}$$

where $a_{ij}$ and $b_{ij}$ are the $ijth$ element of $A$ and $B$ respectively, and $A,B \in V$.  Here $a_{ij} + b_{ij}$ represents the normal sum of two complex numbers in $\mathbb{C}$.  Wince $\mathbb{C}$ already satisfies the requirements of a vector space, I will not elaborate on addition and multiplication for complex scalars, but focus on the $2 \times 2$ matrix of complex scalars

$$A + B = a_{ij} + b_{ij} = b_{ij} + a_{ij} = B + A$$

$$A + (B + C) = a_{ij} + (b_{ij} + c_{ij}) = (a_{ij} + b_{ij}) + c_{ij} = (A + B) + C$$

The zero vector in $V$ is a $2 \times 2$ matrix full of complex zeros (zero real and zero imaginary) defined as $0 = 0_{ij}$

$$A + 0 = a_{ij} + 0_{ij} = a_{ij} = A$$

The negative of a vector $A \in V$ is defined as $-A = -a_{ij}$.  $-a_{ij}$ consists of the negative of the real part of $a_{ij}$ and the negative of the imaginary part of $a_{ij}$

$$A + -A = a_{ij} + -a_{ij} = 0_{ij} = 0$$

Scalar multiplication is defined as $\alpha A = \alpha a_{ij}$ where $\alpha a_{ij}$ for the complex scalar is $\alpha$ time the real and imaginary part of $a_{ij}$

$$\alpha (\beta A) = \alpha (\beta a_{ij}) = \alpha \beta a_{ij} = \alpha \beta A$$

$$1 A = 1 a_{ij} = a_{ij} = A$$

$$\alpha(A + B) = \alpha (a_{ij} + b_{ij}) = \alpha a_{ij} + \alpha b_{ij}$$

$$(\alpha + \beta)A = (\alpha + \beta)a_{ij} = \alpha a_{ij} + \beta a_{ij} = \alpha A + \beta A$$

Therefore all off the requirements are satisfied and $V$ is a vector space


b) Is it possible to define an inner product and extend this vector space to an inner product space?  If not, demonstrate why not.  If it is possible, give an example of an inner product and show that the necessary properties hold.


It is possible to define an inner product. 

$$\langle A, B \rangle = \sum_{ij}a_{ij} b_{ij}$$

This is an inner product because

$$\langle A, B \rangle =  \sum_{ij}a_{ij} b_{ij} =  \sum_{ij}b_{ij} a_{ij} = \langle B, A \rangle$$

$$\langle A, \beta B + \gamma C \rangle =  \sum_{ij}a_{ij} (\beta b_{ij} + \gamma c_{ij}) =  \sum_{ij}a_{ij} \beta b_{ij} + a_{ij} \gamma c_{ij} =  \beta \langle A, B\rangle + \gamma \langle A, C\rangle $$

$$\langle A, A \rangle = \sum_{ij}a_{ij}^2 \ge 0$$

## 2

Find a bijection $f : \mathbb{N} \to \mathbb{Z}$ where $\mathbb{N}$ are the natural (non-negative integer) numbers and $\mathbb{Z}$ is the set of all integers.  How do you know that your mapping is not a surjection or injection, but a bijection?

The map

$$f(n) = \begin{cases}
\frac{n+1}{2} & \text{if n is odd} \\
\frac{-n}{2} & \text{if n is even}
\end{cases}$$

Is injective because one output was produced by only one input.  If the output s negative the input was even, and the absolute value of the negative integer determines which even natural number was input, and the same is true for the positive integers.

It is also surjective because every integer is hit once. As the natural numbers go to infinity, the outputs are sequentially positive then negative then positive then negative, and the absolute values of the integers keeps incrementing to infinity.

## 3

Consider the space of real polynomials of degree 2 or less $P_2^r[t]$, starting with the set $\{ 1, t, t^2\}$ and the inner product

$$\langle g, f \rangle = \int_{-1}^1 g(t) f(t) w(t) dt $$



a) Use the Grahm-Schmidt process to find an orthonormal basis for this vector space

$$e_0 = \frac{a_0}{\sqrt{\langle a_0, a_0 \rangle}} = \frac{1}{\sqrt{2}}$$

$$e_1' = a_1 - e_0 \langle e_0, a_1 \rangle = t - \frac{1}{2} \int_{-1}^1 t dt = t$$

$$e_1 = \frac{e_1'}{\sqrt{\langle e_1', e_1' \rangle}} = \sqrt{\frac{3}{2}}t$$

$$e_2' = a_2 - e_1 \langle e_1, a_2 \rangle - e_0 \langle e_0, a_2 \rangle = t^2 - \frac{3}{2}t \int_{-1}^1 t^3 dt - \frac{1}{2} \int_{-1}^1 t^2 dt = t^2 - \frac{1}{3}$$

$$e_2 = \frac{e_2'}{\sqrt{\langle e_2', e_2' \rangle}} = \frac{t^2 - \frac{1}{3}}{\sqrt{\int_{-1}^{1}(t^4 - \frac{2t^2}{3} + \frac{1}{9})dt}} = \sqrt{\frac{45}{8}}(t^2 - \frac{1}{3}) $$

b) Express $h(t) = 3 t^2 - 1$ in this basis
 
$$h(t) = c_0e_0 + c_1e_1 + c_2e_2$$

Where

$$c_0 = \langle e_0, h \rangle = 0$$ 
$$c_1 = \langle e_1, h \rangle = 0$$

$$c_2 = \langle e_2, h \rangle = \sqrt{\frac{45}{8}}\int_{-1}^1(3t^4 - 2t^2 + 1/3) = \sqrt{\frac{45}{8}}\frac{8}{15}$$

The coefficients are projections of the funciton $h$ onto each basis function.  $h$ expressed in this basis is $(0,0,\sqrt{\frac{45}{8}}\frac{8}{15})$

## 4

The mapping $\xi(|a \rang) = \lang a | a \rang$ is not generally linear.

If we define $a$ as

$$a = \begin{pmatrix}
a_1 \\
a_2 \\
\vdots \\
a_n
\end{pmatrix}$$

And the inner product $\lang a|b \rang$ as the normal sum of the products of the vector elements, then

$$\lang a | a \rang = \sum_{i=1}^n a_i^2$$

This inner product is clearly not linear with respect to $a$ because

$$\xi(\alpha a + \beta b) = \lang\alpha a + \beta b | \alpha a + \beta b\rang = \sum_{i=1}^n (\alpha a_i + \beta b_i)^2 = \sum_{i=1}^n \alpha^2a_i^2 + 2\alpha \beta a_ib_i + \beta^2 b_i^2$$

$$\alpha\xi(a) + \beta\xi(b) = \alpha\sum_{i=1}^n a_i^2 + \beta\sum_{i=1}^n b_i^2$$

The two expressions are not equal, and the mapping is not linear. 
