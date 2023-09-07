---
title: "CHM ENG 250 Transport Processes"
date: 2023-09-05T00:00:00-08:00
---

## Math "Review"

### Notations

|Description|Equations|
|-:|:-|
|Zero-order tensor (Scalar)|$(s) \in \mathbb{R}$|
|First-order tensor (Vector)|$[\mathbf{v}] \in E^3$|
|Second-order tensor|$\\{ \mathbf{T} \\} \in L(E^3, E^3)$|
|Partial derivatives|$\phi_{,i} \equiv \dfrac{\partial \phi}{\partial x_i}$|
|Kronecker delta|$\delta_{ij} = \begin{cases} 1 &&  i = j \\\ 0 && i \not= j \end{cases}$|
|Permutation symbol <br/> Levi-Civita symbol|$\varepsilon_{ijk} = \begin{cases} 1 &  ijk = 123, 231, 312 \\\ -1 & ijk = 321, 132, 213 \\\ 0 & \text{otherwise (two indices alike)} \end{cases}$|

### Set theory

|Description|Equations|
|-:|:-|
|Integers|$\mathbb{Z}$|
|Natural numbers|$\mathbb{N}$|
|Real numbers|$\mathbb{R}$|
|Element of (in)|$x \in X$|
|Not element of (not in)|$x \not\in X$|
|Subset|$X \sube Y$|
|Proper subset|$X \sub Y$|
|Union (or)|$X \cup Y$|
|Intersection (and)|$X \cap Y$|
|Empty set|$\varnothing$|
|Cartesian product|$X \times Y = \\{(x, y) \ \vert\ x \in X, y \in Y\\}$|

### Vector spaces

|Definition of Vector Space $\\{V, +; \mathbb{R}, \cdot\\}$|Equations|
|-:|:-|
|Closure under linear combination|$\mathbf{u} \in V$, $\mathbf{v} \in V$ satisfing $(a \cdot \mathbf{u} + b \cdot \mathbf{v}) \in V$|
|Existence of null element|$\exist\mathbf{0}\in V$ satisfying $\mathbf{u + 0 = u}$|
|Existence of additive inverse|$\exist(\mathbf{-u})\in V$ satisfying $\mathbf{u + (-u) = 0}$|
|Existence of scalar identity|$1 \cdot \mathbf{u} = \mathbf{u}$|
|Associativity of vector addition $(+)$|$(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$|
|Associativity of scalar multiplication $(\cdot)$|$(\alpha\beta)\cdot \mathbf{u} = \alpha \cdot(\beta\cdot\mathbf{u})$|
|Distributivity w.r.t. $\mathbb{R}$|$(\alpha + \beta) \cdot \mathbf{u} = \alpha \cdot \mathbf{u} + \beta \cdot \mathbf{u}$|
|Distributivity w.r.t. $V$|$\alpha \cdot (\mathbf{u} + \mathbf{v}) = \alpha \cdot \mathbf{u} + \alpha \cdot \mathbf{v}$|
|Commutativity of vector addition $(+)$|$\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$|

|Description|Equations|
|-:|:-|
|Linear subspace|$U \sube V$ <br/> $\alpha\mathbf{u}_1 + \beta\mathbf{u}_2 \in U$|
|Linear independent|$\displaystyle\sum_{i}^N \alpha_i \mathbf{v}_i = 0 \iff \alpha_i = 0$|
|Finite dimensional|$V^n, \exist n \in \mathbb{Z}$ such that all linearly independent sets contain at most $n$ elements|
|Basis|$\displaystyle\mathbf{v} = \sum_{i=1}^n \alpha_i \mathbf{b}_i$|

### Euclidean space $E^n$

#### Inner product

|Definition of inner product|Equations|
|-:|:-|
|Commutativity of inner product $(\cdot)$|$\mathbf{u \cdot v = v \cdot u}$|
|Distributivity of $(+)$|$\mathbf{u \cdot (v + w) = u \cdot v + u \cdot w}$|
|Associativity of $(\cdot)$|$(\alpha \mathbf{u})\cdot \mathbf{v} = \alpha (\mathbf{u \cdot v})$|
|Positive definite|$\mathbf{u \cdot u} \ge 0$ <br/> $\mathbf{u \cdot u} = 0 \iff \mathbf{u} = 0$|

|Description|Equations|
|-:|:-|
|Euclidean norm (magnitude)|$\vert\mathbf{u}\vert = \sqrt{\mathbf{u \cdot u}}$|
|Distance|$d(\mathbf{u, v}) \equiv \vert\mathbf{u \cdot v}\vert$|
|Orthogonal|$\mathbf{u \cdot v} = 0$|
|Orthonormal|$\mathbf{e}_1 \cdot \mathbf{e}\_2 = \delta\_{ij}$|
|Orthonormal basis|$\displaystyle\mathbf{v} = \sum_i^n \alpha_i \mathbf{e}_i$|

### Vector product

|Definition of vector product|Equations|
|-:|:-|
|Negative commutativity|$\mathbf{u \times v = - v  \times u}$|
|Triple product <br/> (Box product)|$\mathbf{(u \times v) \cdot w = (v \times w) \cdot u = (w \times u) \cdot v}$ <br/> $\mathbf{[u, v, w] = [v, w, u] = [w, u, v]}$|
|Magnitude of vector product|$\lvert \mathbf{u \times v} \rvert = \lvert\mathbf{u}\rvert \lvert\mathbf{v}\rvert \sin\theta$ , where $\cos\theta = \dfrac{\mathbf{u \cdot v}}{\mathbf{\lvert u \rvert\lvert v \rvert}}$|
|Triple cross product|$\mathbf{u \times (v \times w) = (u \cdot w) v - (v \cdot u) w}$|

|Description|Equations|
|-:|:-|
|Self cross product|$\mathbf{u \times u = 0}$|
|Cross product is orthogonal to original vectors|$\mathbf{(u \times u) \cdot u} = 0$ <br/> $\mathbf{(u \times v) \cdot v} = 0$|
|Right-handed orthonormal basis|$\displaystyle\mathbf{e}\_i \times \mathbf{e}\_j = \sum_{i=1}^3 \varepsilon_{ijk} \mathbf{e}\_k$|
|Vector product in tensor notation|$\displaystyle\mathbf{u} \times \mathbf{v} = \sum_{i=1}^3 \sum_{j=1}^3 u\_i v\_j \mathbf{e}_i \times \mathbf{e}_j$|
|Vector product in permutation notation|$\displaystyle\mathbf{u} \times \mathbf{v} = \sum_{i=1}^3 \sum_{j=1}^3 \sum_{k=1}^3 u\_i v\_j\varepsilon_{ijk}\mathbf{e}_k$|

### Linear functions

|Description|Equations|
|-:|:-|
|Vector-to-scalar function|$f: U \to R$|
|Vector-to-vector function|$\mathbf{f}: U \to V$|
|Linear function|$f(\alpha_1 \mathbf{v}_1 + \alpha_2 \mathbf{v}_2) = \alpha_1 f({\mathbf{v}_1}) + \alpha_2 f(\mathbf{v}_2)$|
|General form of linear function|$f(\mathbf{v}) = \mathbf{a \cdot v}$|

### Indicial notation

|Description|Equations|
|-:|:-|
|**Dummy index** appears twice and summed|$\displaystyle u_i v_i \equiv \sum_{i=1}^3 u_i v_i = \mathbf{u \cdot v}$|
|**Free index** appears once and stacked|$\displaystyle v_{i} \equiv v_i \mathbf{e}\_i = \sum_{i=1}^3 v_i \mathbf{e}\_i = \begin{bmatrix}v_1 & v_2 & v_3\end{bmatrix}^T$ <br/> $\begin{aligned}\displaystyle V_{ij} \equiv V_{ij} \mathbf{e}\_i \otimes \mathbf{e}\_j = \sum_{i=1}^3 \sum_{j=1}^3 V_{ij} \mathbf{e}\_i \otimes \mathbf{e}\_j = \begin{bmatrix}V_{11} & V_{12} & V_{13} \\\ V_{21} & V_{22} & V_{23} \\\ V_{31} & V_{32} & V_{33}\end{bmatrix}\end{aligned}$|
|No index appears more than twice|$\cancel{v_{iii}}$ <br/> $\cancel{v_i u_i w_i}$|

<center>All notations below follows Einstein's indicial notation.</center>

### Tensors

|Description|Equations|
|-:|:-|
|Tensor|$\mathbf{A}$ in $\mathbf{f}(\mathbf{v}) = \mathbf{Av}$|
|Tensor (dyadic) product|$\mathbf{(a \otimes b) v \equiv (b \cdot v)a}$|
|Tensor (dyadic) product|$\mathbf{(a \otimes b)} = a_ib_j$|

### Tensor operations

|Description|Equations|
|-:|:-|
|Transpose|$\mathbf{u \cdot T v \equiv v \cdot T}^T \mathbf{u}$ <br/> $T_{ij} = T_{ji}^T$|
|Tensor multiplication|$\mathbf{(TS)v \equiv T(Sv)}$ <br/> $\mathbf{TS} = T\_{ik} S\_{kj}$|
|Trace|$\mathrm{tr}(\mathbf{u \otimes v}) \equiv \mathbf{u \cdot v}$ <br/> $\mathrm{tr}(\mathbf{T}) = T_{ii} = \sum\mathrm{diag}(\mathbf{T})$|
|Contraction <br/> (Inner product, dot product)|$\mathbf{T \cdot S} \equiv \mathrm{tr}(\mathbf{TS}^T)$ <br/> $\mathbf{T \cdot S} = T_{ij}S_{ij}$|
|Identity tensor|$\mathbf{Iv \equiv v}$ <br/> $\mathbf{I} = \delta\_{ij}$|
|Zero tensor|$\mathbf{Ov = O}$ <br/> $\mathbf{O} = O_{ij}$|
|Symmetric|$\mathbf{T}^T = \mathbf{T}$ <br/> $T_{ij} = T_{ji}$|
|Skew-symmetric|$\mathbf{T}^T = -\mathbf{T}$ <br/> $T_{ij} = -T_{ji}$|
|Positive-definite|$\mathbf{v \cdot T v} \ge 0$ <br/> $\mathbf{v \cdot T v} = 0 \iff \mathbf{v = 0}$|
|Invertible|$\mathbf{Tv = w}$ uniquely determines $\mathbf{v} \implies \mathbf{v = T}^{-1}\mathbf{w}$ <br/> $\mathbf{TT}^{-1} = \mathbf{I}$|
|Orthogonal|$\mathbf{T}^T \mathbf{T} = \mathbf{T}\mathbf{T}^T = \mathbf{I}$ <br/> $\mathbf{T}^T = \mathbf{T}^{-1}$|
|Characteristic polynomial|$\begin{aligned}\det (\mathbf{T - \lambda I}) &= 0 \\\ -\lambda^3 + I_1 \lambda^2 - I_2 \lambda + I_3 &= 0 \end{aligned}$|
|Eigenvalue|$\lambda$|
|Principal invariant 1|$I_1 = \mathrm{tr}(\mathbf{T})$|
|Principal invariant 2|$I_2 = \frac{1}{2}[\mathrm{tr}(\mathbf{T}^2) - \mathrm{tr}(\mathbf{T})^2]$|
|Principal invariant 3|$I_3 = \det(\mathbf{T})$|

### Tensor properties

|Description|Equations|
|-:|:-|
|Distributivity of transpose|$(\mathbf{T} + \mathbf{S})^T = \mathbf{S}^T + \mathbf{T}^T$|
|Transpose flips multiplication order|$(\mathbf{T}\mathbf{S})^T = \mathbf{S}^T \mathbf{T}^T$|
|Inverse flips multiplication order|$(\mathbf{T}\mathbf{S})^{-1} = \mathbf{S}^{-1}\mathbf{T}^{-1}$|
|Transpose-inverse|$\mathbf{T}^{-T} \equiv (\mathbf{T}^{-1})^T = (\mathbf{T}^{T})^{-1}$|

### Tensor calculus

#### Common functions

|Description|Notation|Domain|Range|
|-:|:-|-:|:-|
|Scalar-to-scalar|$\phi_1(t)$|$\mathbb{R}$|$\mathbb{R}$|
|Vector-to-scalar|$\phi_2(\mathbf{x})$|$E^3$|$\mathbb{R}$|
|Multivariable scalar-valued|$\phi_3(\mathbf{x}, t)$|$E^3 \times \mathbb{R}$|$\mathbb{R}$|
|Scalar-to-vector|$\mathbf{v}_1(t)$|$\mathbb{R}$|$E^3$|
|Vector-to-vector|$\mathbf{v}_2(\mathbf{x})$|$E^3$|$E^3$|
|Multivariable vector-valued|$\mathbf{v}_3(\mathbf{x}, t)$|$E^3 \times \mathbb{R}$|$E^3$|
|Scalar-to-tensor|$\mathbf{T}_1(t)$|$\mathbb{R}$|$L(E^3, E^3)$|
|Vector-to-tensor|$\mathbf{T}_2(\mathbf{x})$|$\mathbb{R}$|$L(E^3, E^3)$|
|Multivariable tensor-valued|$\mathbf{T}_3(\mathbf{x}, t)$|$E^3 \times \mathbb{R}$|$L(E^3, E^3)$|

#### Properties of functions

|Description|Definition|
|-:|:-|
|**Gradient** of a scalar function|$[\mathrm{grad} \ \phi(\mathbf{x})] \cdot \mathbf{w} \equiv \left[\frac{d}{d\omega} \phi(\mathbf{x} + \omega \mathbf{w})\right]_{\omega = 0}$|
|**Gradient** of a vector function|$[\mathrm{grad} \ \mathbf{v}(\mathbf{x})] \mathbf{w} \equiv \left[\frac{d}{d\omega} \mathbf{v}(\mathbf{x} + \omega \mathbf{w})\right]_{\omega = 0}$|
|**Divergence** of a vector function|$\mathrm{div} \ \mathbf{v}(\mathbf{x}) \equiv \mathrm{tr}[\mathrm{grad} \ \mathbf{v}(\mathbf{x})]$|
|**Divergence** of a tensor function|$[\mathrm{div} \ \mathbf{T}(\mathbf{x})] \cdot \mathbf{w} \equiv \mathrm{div}[\mathbf{T}^T(\mathbf{x}) \mathbf{w}]$|
|**Curl** of a vector function|$[\mathrm{curl} \ \mathbf{v}(\mathbf{x})] \cdot \mathbf{w} \equiv \mathrm{div}(\mathbf{\mathbf{v}(x) \times w})$|

|Description|Expression in Orthonomal Coordinates|
|-:|:-|
|**Gradient** of a scalar function|$\mathrm{grad} \ \phi(\mathbf{x}) = \phi_{,i} \mathbf{e}_i$|
|**Gradient** of a vector function|$\mathrm{grad} \ \mathbf{v}(\mathbf{x}) = v_{i, j} \mathbf{e}_i \otimes \mathbf{e}_j$|
|**Divergence** of a vector function|$\mathrm{div} \ \mathbf{v}(\mathbf{x}) = v_{i, i}$|
|**Divergence** of a tensor function|$\mathrm{div} \ \mathbf{T}(\mathbf{x}) = T\_{ji,i} \mathbf{e}\_j = T_{ij,j} \mathbf{e}\_i$|
|**Curl** of a vector function|$\mathrm{curl} \ \mathbf{v}(\mathbf{x}) = \varepsilon_{ijk}v_{j,i}\mathbf{e}_k$|

|Description|Domain|Range|
|-:|-:|:-|
|**Gradient** of a scalar function|Scalar function|Vector function|
|**Gradient** of a vector function <br/> $\mathrm{grad} = \nabla$|Vector function|Tensor function|
|**Divergence** of a vector function|Vector function|Scalar|
|**Divergence** of a tensor function <br/> $\mathrm{div} = \nabla\cdot$|Tensor function|Vector|
|**Curl** of a vector function <br/> $\mathrm{curl} = \nabla \times$|Vector function|Vector function|

#### Tensor calculus identities

|Description|Equations|
|-:|:-|
|-|$\mathrm{grad}(\phi\mathbf{v}) = \phi\mathrm{grad}(\mathbf{v}) + \mathbf{v} \otimes \mathrm{grad}(\phi)$|
|-|$\mathrm{div}(\phi\mathbf{v}) = \phi\mathrm{div}(\mathbf{v}) + \mathbf{v} \cdot \mathrm{grad}(\phi)$|
|-|$\mathrm{curl} [\mathrm{grad} (\phi)] = \mathbf{0}$|
|-|$\mathrm{div} [\mathrm{curl} (\mathbf{v})] = 0$|
|-|$\mathrm{grad}(\mathbf{v \cdot w}) = [\mathrm{grad} (\mathbf{v})]^T \mathbf{w} + [\mathrm{grad} (\mathbf{w})]^T \mathbf{v}$|
|-|$\mathrm{grad}[\mathrm{div}(\mathbf{v})] = \mathrm{div}[\mathrm{grad}(\mathbf{v})]^T$|
|-|$\mathrm{div}(\mathbf{v \otimes w}) = \mathrm{div}[\mathrm{grad}(\mathbf{v})]^T$|
|-|$\mathrm{curl}[\mathrm{curl}(\mathbf{v})] = \mathrm{grad}[\mathrm{div}(\mathbf{v})] - \mathrm{div}[\mathrm{grad}(\mathbf{v})]$|
|-|$\mathrm{div}(\mathbf{v \times w}) = \mathbf{w} \cdot \mathrm{curl}(\mathbf{v}) - \mathbf{v}\cdot \mathrm{curl}(\mathbf{w})$|
|-|$\mathrm{curl}(\mathbf{v \times w}) = \mathrm{div}(\mathbf{v \otimes w - w \otimes v})$|

### Misc properties

|Description|Equations|
|-:|:-|
|Permutation symbol|$\varepsilon_{ijk} = \frac{1}{2}(i - j)(j - k)(k - i)$|
|Permutation symbol and Kronecker delta|$\varepsilon_{ijk} \varepsilon_{ijm} = 2 \delta_{km}$|
|$\varepsilon$-$\delta$ identity|$\varepsilon_{ijk}\varepsilon_{mnk} = \delta_{im}\delta_{jn} - \delta_{in}\delta_{jm}$|
|Determinant in permutation symbol|$\det(\mathbf{A}) = \begin{vmatrix}a_{11} & a_{12} & a_{13} \\\ a_{21} & a_{22} & a_{23} \\\ a_{31} & a_{32} & a_{33}\end{vmatrix} =\varepsilon_{ijk} a_{1i}a_{2j}a_{3k}$|
|Dot product of basis vectors|$\mathbf{e}\_i \cdot \mathbf{e}\_j = \delta_{ij}$ as a scalar|
|Basis set of tensor|$\mathbf{e}\_i \otimes \mathbf{e}\_j = \delta_{ij}$ as a tensor|

Note that the notations depends on the context of the expression following the indicial notation. E.g. $\delta_{ij}$ could be a scalar or a tensor depending on the context of that it's multiplied to.

## Kinematics

<!-- ★ -->