---
title: "MATH 324 Advanced Multivariable Calculus"
date: 2021-08-17T00:00:00+08:00
---

## Double Integrals

### Double integrals in Cartesian coordinates

|Description|Equations|
|-:|:-|
|Double integrals|$\iint\limits_{R} f(x, y) \ dA \newline = \lim\limits_{m, n \to\infty} \sum\limits_{i=1}^{m} \sum\limits_{j=1}^{n} f(x_{ij}^{*}, y_{ij}^{*}) \Delta A$|
|Fubini's Theorem <br/> $R = [a, b]\times[c, d]$|$\iint\limits_{R} f(x, y) \ dA \newline = \int_{a}^{b}\int_{c}^{d} f(x, y) \ dx \ dy \newline = \int_{c}^{d}\int_{a}^{b} f(x, y) \ dy \ dx$|
|Separation of iterative integrals <br/> $R = [a, b]\times[c, d]$|$\iint\limits_{R} g(x)h(y) \ dA = \int_{a}^{b} g(x) \ dx\int_{c}^{d} h(y) \ dy$|
|Type I region <br/> $D = x \times y = [a, b]\times[g_{1}(x), g_{2}(x)]$|$\iint\limits_{D} f(x, y) \ dA = \int_{a}^{b}\int_{g_{1}(x)}^{g_{2}(x)} f(x, y) \ dx \ dy$|
|Type II region <br/> $D = x \times y = [h_{1}(x), h_{2}(x)]\times[c, d]$|$\iint\limits_{D} f(x, y) \ dA = \int_{c}^{d}\int_{h_{1}(x)}^{h_{2}(x)} f(x, y) \ dy \ dx$|
|Addition of double integrals|$\iint\limits_{D} [f(x, y) + g(x, y)] \ dA \newline = \iint\limits_{D} f(x, y) \ dA + \iint\limits_{D} g(x, y) \ dA$|
|Constant multiple of double integrals|$\iint\limits_{D} cf(x, y) \ dA = c\iint\limits_{D} f(x, y) \ dA$|
|Region separation of double integrals|$\iint\limits_{D} f(x, y) \ dA \newline = \iint\limits_{D_{1}} f(x, y) \ dA + \iint\limits_{D_{2}} f(x, y) \ dA$|
|Area of a region $D$|$A(D) = \iint\limits_{D} dA$|
|Average value of a function|$\bar{f} = \dfrac{1}{A(R)} \iint\limits_{R} f(x, y) \ dA$|

### Double integrals in polar coordinates

|Description|Equations|
|-:|:-|
|Transformation to polar coordinates|$x = r\cos\theta \newline y = r\sin\theta \newline x^{2} + y^{2} = r^{2} \newline dA = r \ dr \ d\theta$|
|Double integrals in polar coordinates <br/> $R = r\times\theta = [a, b]\times[\alpha, \beta]$|$\iint\limits_{R} f(x, y) \ dA \newline = \int_{\alpha}^{\beta}\int_{a}^{b} f(r\cos\theta, r\sin\theta) \ r \ dr \ d\theta$|
|Double integrals in general polar region <br/> $R = r\times\theta = [h_{1}(\theta), h_{2}(\theta)]\times[\alpha, \beta]$|$\iint\limits_{R} f(x, y) \ dA \newline = \int_{\alpha}^{\beta}\int_{h_{1}(\theta)}^{h_{2}(\theta)} f(r\cos\theta, r\sin\theta) \ r \ dr \ d\theta$|

### Change of variables for double integrals

|Description|Equations|
|-:|:-|
|Transformation of two variables|$T(u, v) = (x(u, v), y(u, v))$|
|Jacobian of transformation of two variables|$\dfrac{\partial (x, y)}{\partial (u, v)} = \begin{vmatrix}\dfrac{\partial x}{\partial u} & \dfrac{\partial x}{\partial v} \cr \cr \dfrac{\partial y}{\partial u} & \dfrac{\partial y}{\partial v}\end{vmatrix}$|
|Change of variables for differentials|$dA = dx dy = \bigg\lvert \dfrac{\partial (x, y)}{\partial (u, v)} \bigg\rvert \ du \ dv$|
|Change of variables for double integrals|$\iint\limits_{R} f(x, y) dA \newline = \iint\limits_{S} f(x(u, v), y(u, v)) \ \bigg\lvert \dfrac{\partial (x, y)}{\partial (u, v)} \bigg\rvert \ du \ dv$|

### Applications of double integrals

|Description|Equations|
|-:|:-|
|Density function|$\rho (x, y) = \dfrac{dm}{dA}$|
|Mass|$m = \iint\limits_{D} \rho(x, y) \ dA$|
|Moment about x-axis|$M_{x} = \iint\limits_{D} y\rho(x, y) \ dA$|
|Moment about y-axis|$M_{x} = \iint\limits_{D} x\rho(x, y) \ dA$|
|Center of mass $(\bar{x}, \bar{y})$ | $\bar{x} = \dfrac{M_{y}}{m} = \dfrac{\iint\limits_{D} x\rho(x, y) \ dA}{\iint\limits_{D} \rho(x, y) \ dA}$ <br/><br/> $\bar{y} = \dfrac{M_{x}}{m} = \dfrac{\iint\limits_{D} y\rho(x, y) \ dA}{\iint\limits_{D} \rho(x, y) \ dA}$|
|Moment of inertia about x-axis <br/> (second moment)|$I_{x} = \iint\limits_{D} y^{2}\rho(x, y) \ dA$|
|Moment of inertia about y-axis <br/> (second moment)|$I_{y} = \iint\limits_{D} x^{2}\rho(x, y) \ dA$|
|Moment of inertia about the origin <br/> (polar moment of inertia)|$I_{0} = I_{x} + I_{y} = \iint\limits_{D} (x^{2} + y^{2})\rho(x, y) \ dA$|
|Surface area|$A = \iint\limits_{D} \sqrt{1 + \left( \dfrac{\partial z}{\partial x} \right)^{2} + \left( \dfrac{\partial z}{\partial y} \right)^{2}} dA$|

## Triple Integrals

### Triple integrals in Cartesian coordinates

|Description|Equations|
|-:|:-|
|Triple integrals|$\iiint\limits_{B} f(x, y, z) \ dV \newline = \lim\limits_{l, m, n \to \infty} \sum\limits_{i = 1}^{l} \sum\limits_{j = 1}^{m} \sum\limits_{k = 1}^{n} f(x_{ijk}^{*}, y_{ijk}^{*}, z_{ijk}^{*}) \Delta V$|
|Fubini's Theorem <br/> $B = x\times y\times z = \newline [a, b]\times[c, d]\times[r, s]$|$\iiint\limits_{B} f(x, y, z) \ dV \newline = \int_{r}^{s}\int_{c}^{d}\int_{a}^{b} f(x, y, z) \ dx \ dy \ dz \newline = \int_{c}^{d}\int_{r}^{s}\int_{a}^{b} f(x, y, z) \ dx \ dz \ dy \newline = ...$|
|Type 1 region <br/> $D = x \times y$ <br/> $E = D \times z = \newline D \times[u_{1}(x, y), u_{2}(x, y)]$|$\iiint\limits_{E} f(x, y, z) \ dV  =\iint\limits_{D} \left( \int_{u_{1}(x, y)}^{u_{2}(x, y)} f(x, y, z) dz \right) dA$|
|Type 2 region <br/> $D = y \times z$ <br/> $E = D \times x = \newline D \times[u_{1}(y, z), u_{2}(y, z)]$|$\iiint\limits_{E} f(x, y, z) \ dV  =\iint\limits_{D} \left( \int_{u_{1}(y, z)}^{u_{2}(y, z)} f(x, y, z) dx \right) dA$|
|Type 3 region <br/> $D = x \times z$ <br/> $E = D \times y = \newline D \times[u_{1}(x, z), u_{2}(x, z)]$|$\iiint\limits_{E} f(x, y, z) \ dV  =\iint\limits_{D} \left( \int_{u_{1}(x, z)}^{u_{2}(x, z)} f(x, y, z) dy \right) dA$|
|Example of a general region <br/> (6 general regions) <br/> $E = [a, b]\times[g_{1}(x), g_{2}(x)]\times[u_{1}(x, y), u_{2}(x, y)]$|$\iiint\limits_{E} f(x, y, z) \ dV = \int_{a}^{b} \int_{g_{1}(x)}^{g_{2}(x)} \int_{u_{1}(x, y)}^{u_{2}(x, y)} f(x, y, z) \ dz \ dy \ dx$|
|Volume of a solid $E$|$V(E) = \iiint\limits_{E} dV$|

### Triple integrals in cylindrical coordinates

|Description|Equations|
|-:|:-|
|Transformation to cylindrical coordinates|$x = r\cos\theta \newline y = r\sin\theta \newline z = z \newline x^{2} + y^{2} = r^{2} \newline dV = r \ dz \ dr \ d\theta$|
|Range of cylindrical coordinates|$r \in [0, \infty) \newline \theta \in [0, 2\pi] \newline z \in [0, \infty)$|
|Triple integrals in general cylindrical region <br/> $E = r \times \theta \times z = \newline$ $[\alpha, \beta]\times[h_{1}(\theta), h_{2}(\theta)] \times [u_{1}(x, y), u_{2}(x, y)]$|$\iiint\limits_{E} f(x, y, z) \ dV = \newline \int_{\alpha}^{\beta} \int_{h_{1}(\theta)}^{h_{2}(\theta)} \int_{u_{1}(r\cos\theta, r\sin\theta)}^{u_{2}(r\cos\theta, r\sin\theta)}... \newline ... f(r\cos\theta, r\sin\theta, z) \ r \ dz \ dr \ d\theta$|

### Triple integrals in spherical coordinates

|Description|Equations|
|-:|:-|
|Transformation to spherical coordinates|$(r = \rho \ \sin\phi) \newline x = \rho\sin\phi\cos\theta \newline y = \rho\sin\phi\sin\theta \newline z = \rho\cos\phi \newline \rho^{2} = x^{2} + y^{2} + z^{2} \newline dV = \rho^{2} \ \sin\phi \ d\rho \ d\theta \ d\phi$|
|Range of spherical coordinates|$\rho \in [0, \infty) \newline \theta \in [0, 2\pi] \newline \phi \in [0, \pi]$|
|Triple integrals in general spherical region <br/> $E = \theta \times \phi \times \rho = \newline$ $[\alpha, \beta] \times [c, d] \times [g_{1}(\theta, \phi), g_{2}(\theta, \phi)]$|$\iiint\limits_{E} f(x, y, z) dV = \newline \int_{c}^{d} \int_{\alpha}^{\beta} \int_{g_{1}(\theta, \phi)}^{g_{2}(\theta, \phi)} ... \newline ... f(\rho\sin\phi\cos\theta, \rho\sin\phi\sin\theta, \rho\cos\phi) ... \newline ... \rho^{2} \ \sin\phi \ d\rho \ d\theta \ d\phi$|

### Change of variables for triple integrals

|Description|Equations|
|-:|:-|
|Transformation of three variables|$T(u, v, w) = (x(u, v, w), y(u, v, w), z(u, v, w))$|
|Jacobian of transformation of three variables|$\dfrac{\partial (x, y, z)}{\partial (u, v, w)} = \begin{vmatrix}\dfrac{\partial x}{\partial u} & \dfrac{\partial x}{\partial v} & \dfrac{\partial x}{\partial w} \cr \cr \dfrac{\partial y}{\partial u} & \dfrac{\partial y}{\partial v} & \dfrac{\partial y}{\partial w} \cr \cr \dfrac{\partial z}{\partial u} & \dfrac{\partial z}{\partial v} & \dfrac{\partial z}{\partial w} \end{vmatrix}$|
|Change of variables for differentials|$dV = dx \ dy \ dz = \bigg\lvert \dfrac{\partial (x, y, z)}{\partial (u, v, w)} \bigg\rvert \ du \ dv \ dw$|
|Change of variables for triple integrals|$\iiint\limits_{R} f(x, y, z) dV \newline = \iiint\limits_{S} f(x(u, v, w), y(u, v, w), z(u, v, w)) ... \newline ... \bigg\lvert \dfrac{\partial (x, y, z)}{\partial (u, v, w)} \bigg\rvert \ du \ dv \ dw$|

### Applications of triple integrals

|Description|Equations|
|-:|:-|
|Mass|$m = \iiint\limits_{E} \rho(x, y, z) \ dV$|
|Moments about coordinate planes|$M_{yz} = \iiint\limits_{E} x\rho(x, y, z) \ dV \newline M_{xz} = \iiint\limits_{E} y\rho(x, y, z) \ dV \newline M_{xy} = \iiint\limits_{E} z\rho(x, y, z) \ dV$|
|Center of mass $(\bar{x}, \bar{y}, \bar{z})$|$\bar{x} = \dfrac{M_{yz}}{m} = \dfrac{\iiint\limits_{E} x\rho(x, y, z) \ dV}{\iiint\limits_{E} \rho(x, y, z) \ dV}$ <br/><br/> $\bar{y} = \dfrac{M_{xz}}{m} = \dfrac{\iiint\limits_{E} y\rho(x, y, z) \ dV}{\iiint\limits_{E} \rho(x, y, z) \ dV}$ <br/><br/> $\bar{z} = \dfrac{M_{xy}}{m} = \dfrac{\iiint\limits_{E} z\rho(x, y, z) \ dV}{\iiint\limits_{E} \rho(x, y, z) \ dV}$|
|Moments of inertia about coordinate axes|$I_{x} = \iiint\limits_{E} (y^{2} + z^{2}) \rho(x, y, z) \ dV \newline I_{y} = \iiint\limits_{E} (x^{2} + z^{2}) \rho(x, y, z) \ dV \newline I_{z} = \iiint\limits_{E} (x^{2} + y^{2}) \rho(x, y, z) \ dV$|

## Partial Differentiation

### Chain rule

|Description|Equations|
|-:|:-|
|Chain rule <br/> $z = f(x(t), y(t))$|$\dfrac{dz}{dt} = \dfrac{\partial z}{\partial x}\dfrac{dx}{dt} + \dfrac{\partial z}{\partial y}\dfrac{dy}{dt}$|
|Chain rule <br/> $z = f(x(s, t), y(s, t))$|$\dfrac{\partial z}{\partial s} = \dfrac{\partial z}{\partial x} \dfrac{\partial x}{\partial s} + \dfrac{\partial z}{\partial y} \dfrac{\partial y}{\partial s}$ <br/><br/> $\dfrac{\partial z}{\partial t} = \dfrac{\partial z}{\partial x} \dfrac{\partial x}{\partial t} + \dfrac{\partial z}{\partial y} \dfrac{\partial y}{\partial t}$|
|**Chain rule (general)** <br/> $z = f(x_{1}, ..., x_{n})$, <br/> where $x_{i} = x_{i}(t_{1}, ..., t_{m})$|$\dfrac{\partial z}{\partial t_{i}} = \dfrac{\partial z}{\partial x_{1}} \dfrac{\partial x_{i}}{\partial t_{i}} + ... + \dfrac{\partial z}{\partial x_{n}} \dfrac{\partial x_{n}}{\partial t_{i}}$|

### Directional derivatives and gradient vector

|Description|Equations|
|-:|:-|
|Assumptions|Unit vector $\mathbf{u} = \langle u_{1}, ..., u_{i} \rangle$ <br/> Independent variables $\mathbf{x} = \langle x_{1}, ..., x_{i} \rangle$|
|General directional derivatives|$D_{\mathbf{u}}f(\mathbf{x}) = \lim\limits_{h \to 0} \dfrac{f(\mathbf{x}+h\mathbf{u}) - f(\mathbf{x})}{h}$|
|General gradient vectors|$\nabla f(\mathbf{x}) = \bigg\langle \dfrac{\partial f}{\partial x_{1}}, ..., \dfrac{\partial f}{\partial x_{i}} \bigg\rangle$|
|General directional derivatives and gradient vectors|$D_{\mathbf{u}}f(\mathbf{x}) = \nabla f(\mathbf{x}) \cdot \mathbf{u}$|
|Directional derivative in 2D|$D_{\mathbf{u}}f(x, y) = f_{x} \cos\theta + f_{y} \sin\theta$|
|Gradient vector and maximum values|$\max(D_{\mathbf{u}}f(\mathbf{x})) = \lvert \nabla f(\mathbf{x}) \rvert$ <br/> where $\mathbf{u} = \dfrac{\nabla f(\mathbf{x})}{\lvert \nabla f(\mathbf{x}) \rvert}$|
|Gradient vector $\perp$ tangent vector <br/> for level surface $F(x, y, z) = k$|$\nabla F(x(t), y(t), z(t)) \cdot \mathbf{r}'(t) = 0 \newline \nabla F(x_{0}, y_{0}, z_{0}) \cdot \mathbf{r}'(t_{0}) = 0$|
|Tangent plane in terms of gradient vector (normal vector)|$\nabla F(x, y, z) \cdot \langle x-x_{0}, y-y_{0}, z-z_{0} \rangle= 0$|
|Symmetric equation of normal line|$\dfrac{x-x_{0}}{F_{x}(x_{0}, y_{0}, z_{0})} = \newline \dfrac{y-y_{0}}{F_{y}(x_{0}, y_{0}, z_{0})} = \newline \dfrac{z-z_{0}}{F_{z}(x_{0}, y_{0}, z_{0})}$|

## Vector Calculus

### Arc length and parameterization of curves

|Description|Equations|
|-:|:-|
|Vector field|$\mathbf{F}(\mathbf{x}) = \langle P(\mathbf{x}), Q(\mathbf{x}), R(\mathbf{x}) \rangle$|
|Conservative vector field <br/> and potential function|$\mathbf{F} = \nabla f$|
|Parameterization of line segments|$\mathbf{r}(t) = (1-t) \mathbf{r}_{0} + t \ \mathbf{r}_1$, for $0 \le t \le 1$|
|Parameterization of circles|$\mathbf{r}(t) = \langle r\cos(t), r\sin(t) \rangle$|
|Parameterization of functions|$\mathbf{r}(t) = \langle t, f(t) \rangle$|
|Arc length|$L = \int_{a}^{b} \ \lvert \mathbf{r}'(t) \rvert \ dt$|
|Arc length parameter|$s(t) = \int_{a}^{t} \ \lvert \mathbf{r}'(u) \rvert \ du \newline s'(t) = \lvert \mathbf{r}'(t) \rvert \newline ds = \lvert \mathbf{r}'(t) \rvert \ dt$|

### Line integrals

|Description|Equations|
|-:|:-|
|Line integral|$\int_{C} f(x, y) \ ds = \lim\limits_{n \to \infty} \sum\limits_{i=1}^{n} f(x_{i}^{*}, y_{i}^{*}) \Delta s_{i}$|
|**Line integral with respect to arc length**|$\int_{C} f(x, y) \ ds \newline = \int_{a}^{b} f(x(t), y(t)) \sqrt{\left( \dfrac{dx}{dt} \right)^{2} + \left( \dfrac{dy}{dt} \right)^{2}} dt \newline = \int_{a}^{b} f(\mathbf{r}(t)) \ \lvert \mathbf{r}'(t) \rvert \ dt$|
|Line integral with respect to $x$ and $y$|$\int_{C} f(x, y) \ dx = \int_{a}^{b} f(x(t), y(t)) \ x'(t) \ dt \newline \int_{C} f(x, y) \ dy = \int_{a}^{b} f(x(t), y(t)) \ y'(t) \ dt$|
|Line integrals of vector fields|$\int_{C} \mathbf{F} \cdot \mathbf{T} \ ds \newline = \int_{C} \mathbf{F} \cdot d\mathbf{r} \newline = \int_{a}^{b} \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t) \ dt$|
|Line integrals of vector fields and scalar fields|$\mathbf{F} = \langle P, Q, R \rangle \newline \int_{C} \mathbf{F} \cdot d\mathbf{r} \newline = \int_{C} P \ dx + Q \ dy + R \ dz \newline = \int_{C} P \ x'(t) + Q \ y'(t) + R \ z'(t) \ dt$|
|Orientation properties of line integrals with respect to arc length, $x$, and $y$|$\int_{-C} f(x, y) \ ds = \int_{C} f(x, y) \ ds \newline \int_{-C} f(x, y) \ dx = -\int_{C} f(x, y) \ dx \newline \int_{-C} f(x, y) \ dy = -\int_{C} f(x, y) \ dy$|
|Orientation properties of line integrals of vector fields|$\int_{-C} \mathbf{F} \cdot d\mathbf{r} = -\int_{C} \mathbf{F} \cdot d\mathbf{r}$|
|Line integral of a piecewise-smooth curve|$\int_{C} f \ ds = \sum\limits_{i=1}^{N} \int_{C_{i}} f \ ds \newline C = C_{1} \cup C_{2} \cup ... \cup C_{N}$|

### Fundamental theorem of line integrals

- path - a smooth curve with initial and terminal point
- simple curve - a curve that does not intersect itself anywhere between its endpoints
- closed curve - a curve where its terminal point coincides with its initial point
- simple region - a region that is bounded by two line segments in one direction (type-1, type-2 regions)
- open region - a region that does not contain boundary points
- closed region - a region that contains all boundary points
- connected region - two points in the region can be joined by a path that lies in the region
- simply-connected region - a region that every simple closed curve in D encloses only points that are in D
  - has no hole
  - doesn't consist of separate pieces

|Description|Equations|
|-:|:-|
|Fundamental theorem of line integrals|$\int_{C} \nabla f \cdot d\mathbf{r} = f(\mathbf{r}(b)) - f(\mathbf{r}(a))$|
|Line integrals of non-conservative fields are not path independent (same end points)|$\int_{C_{1}} \mathbf{F} \cdot d\mathbf{r} \not= \int_{C_{2}} \mathbf{F} \cdot d\mathbf{r}$|
|Line integrals of conservative fields are path independent (same end points)|$\int_{C_{1}} \nabla f \cdot d\mathbf{r} = \int_{C_{2}} \nabla f \cdot d\mathbf{r}$|
|Line integrals of closed path|$\int_{C_{\mathrm{closed}}} \mathbf{F} \cdot d\mathbf{r} = 0 \Leftrightarrow \newline \int_{C} \mathbf{F} \cdot d\mathbf{r}$ is path independent|
|Path independence and conservative vector field *(open, connected region)*|$\int_{C} \mathbf{F} \cdot d\mathbf{r}$ is path independent $\Rightarrow$ <br/> $\mathbf{F} = \nabla f$ (conservative field)|
|Property of conservative vector field|$\mathbf{F} = \nabla f \Rightarrow \dfrac{\partial P}{\partial y} = \dfrac{\partial Q}{\partial x}$|
|Determine conservative vector field in 2D <br/> *(open simply-connected region)*|$\dfrac{\partial P}{\partial y} = \dfrac{\partial Q}{\partial x} \Rightarrow \mathbf{F} = \nabla f$|

#### Summary

- Fundamental theorem of line integral (FTL) is always true (with assumptions).
- Other statements are not true for general $\mathbf{F} = \langle P, Q \rangle$
  - They have to be verified for each given $\mathbf{F}$ or derived from theorems.
$$\begin{aligned} \mathrm{curl}\ \mathbf{F} &= \mathbf{0} &\color{gray}\footnotesize\text{(checking 3D conservative field)} \cr \dfrac{\partial P}{\partial y} &= \dfrac{\partial Q}{\partial x} &\color{gray}\footnotesize\text{(checking 2D conservative field)} \cr & \color{blue}\upharpoonleft\downharpoonright \footnotesize\text{open, simply-connected }D \cr \mathbf{F} &= \nabla f &\color{gray}\footnotesize\text{(def. of conservative field)} \cr \textstyle\int_{C} \nabla f \cdot d\mathbf{r} & = f(\mathbf{r}(b)) - f(\mathbf{r}(a)) &\color{gray}\footnotesize\text{(FTL)} \cr \color{blue}\footnotesize\text{open, connected }D & \color{blue}\upharpoonleft\downharpoonright \cr \textstyle\int_{C_{1}} \mathbf{F} \cdot d\mathbf{r} &= \textstyle\int_{C_{2}} \mathbf{F} \cdot d\mathbf{r} &\color{gray}\footnotesize\text{(path independence)} \cr & \color{blue}\upharpoonleft\downharpoonright \cr \textstyle\int_{C} \mathbf{F} &\cdot d\mathbf{r} = 0 \footnotesize\text{ on a closed path} &\color{gray}\footnotesize\text{(closed path)} \end{aligned}$$

### Curl and divergence

|Description|Equations|
|-:|:-|
|Gradient|$\mathrm{grad}\ f = \nabla f \newline = \langle \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}, \frac{\partial f}{\partial z} \rangle$|
|Curl|$\mathrm{curl}\ \mathbf{F} = \nabla \times \mathbf{F} \newline = \langle \frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z}, \frac{\partial P}{\partial z} - \frac{\partial R}{\partial x}, \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \rangle$|
|Divergence|$\mathrm{div}\ \mathbf{F} = \nabla \cdot \mathbf{F} \newline = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$|
|Laplace operator on scalar functions|$\nabla^{2}f = \nabla\cdot\nabla f = \mathrm{div}(\nabla f) \newline = \frac{\partial^{2}f}{\partial x^{2}} + \frac{\partial^{2}f}{\partial y^{2}} + \frac{\partial^{2}f}{\partial z^{2}}$|
|Laplace operator on vector fields|$\nabla^{2}\mathbf{F} = \langle \nabla^{2}P, \nabla^{2}Q, \nabla^{2}R \rangle$|
|Property of conservative vector field|$\mathrm{curl}\ \nabla f = \mathbf{0}$|
|Determine conservative vector field in 3D <br/> *(open simply-connected region)*|$\mathrm{curl}\ \mathbf{F} = \mathbf{0} \Rightarrow \mathbf{F} = \nabla f$|
|Property of divergence and curl|$\mathrm{div}\ \mathrm{curl}\ \mathbf{F} = \nabla\cdot(\nabla\times\mathbf{F}) = 0$|
|Determine curl field|$\mathrm{div}\ \mathbf{F} \not= 0 \Rightarrow \mathbf{F}$ is not curl of any field|

### Green's theorem

|Description|Equations|
|-:|:-|
|**Green's Theorem** <br/> *(positively oriented, piecewise-smooth, simple, closed curve $C$ enclosing $D$)*|$\displaystyle\oint_{C} \mathbf{F}\cdot d\mathbf{r} = \iint\limits_{D} \left( \dfrac{\partial Q}{\partial x} - \dfrac{\partial P}{\partial y} \right) dA$|
|Circulation-Curl form of Green's Theorem|$\oint_{C} \mathbf{F}\cdot d\mathbf{r} = \iint\limits_{D} (\nabla\times\mathbf{F})\cdot \mathbf{k} \ dA$|
|Flux-Divergence form of Green's Theorem|$\oint_{C} \mathbf{F}\cdot \mathbf{n} \ ds = \iint\limits_{D} \nabla\cdot\mathbf{F} \ dA$|
|Area of region $D$ enclosed by $C$|$A = \iint\limits_{D}1\ dA \newline = \oint_{C} x \ dy \newline = -\oint_{C} y \ dx \newline = \dfrac{1}{2}\oint_{C} x \ dy - y \ dx$|

### Surface area and parameterization of surfaces

|Description|Equations|
|-:|:-|
|General parametric surface|$\mathbf{r}(u, v) = \langle x(u, v), y(u, v), z(u, v) \rangle$|
|Parametric equation of a plane|$\mathbf{r}(u, v) = \mathbf{r}_{0} + u\mathbf{a} + v\mathbf{b}$|
|Parametric equation of a sphere|$\mathbf{r}(\phi, \theta) = \langle a\sin\phi\cos\theta, a\sin\phi\sin\theta, a\cos\phi \rangle$|
|Parametric equation of an explicit function|$\mathbf{r}(u, v) = \langle u, v, f(u, v) \rangle$|
|Parametric equation of a surface of revolution|$\mathbf{r}(u, \theta) = \langle u, f(u)\cos\theta, f(u)\sin\theta \rangle$|
|Normal vector of a tangent plane|$\mathbf{r}_{u} \times \mathbf{r}_v$|
|Surface area of a parametric surface|$\iint\limits_{D} \lvert \mathbf{r}_{u}\times\mathbf{r}_{v} \rvert \ dA$|
|Surface area of the graph of an explicit function $z = f(x, y)$|$\iint\limits_{D} \sqrt{1 + (\frac{\partial z}{\partial x})^{2} + (\frac{\partial z}{\partial y})^{2}} \ dA$|
|Surface area of the graph of an implicit function $C = f(x, y, z)$|$\iint\limits_{D} \dfrac{\lvert \nabla f \rvert}{\lvert \nabla f \cdot \mathbf{k} \rvert} \ dA$|

### Surface integral

|Description|Equations|
|-:|:-|
|Surface integral of a function over a parametric surface|$\iint\limits_{S} f(x,y,z) \ dS \newline = \iint\limits_{D} f(\mathbf{r}(u,v)) \lvert \mathbf{r}_{u}\times\mathbf{r}_{v} \rvert \ dA$|
|Surface integral of an explicit function $z = f(x, y)$|$\iint\limits_{S} f(x,y,z) \ dS \newline = \iint\limits_{D} f(x, y, g(x, y)) \sqrt{1+(\frac{\partial z}{\partial x})^{2}+(\frac{\partial z}{\partial y})^{2}} \ dA$|
|Surface integral of piecewise smooth surface|$\iint\limits_{S} f \ dS = \sum\limits_{i=1}^{N}\iint\limits_{S_{i}}f \ dS \newline S = S_{1} \cup S_{2} \cup ... \cup S_{N}$|
|Unit normal vector|$\mathbf{n} = \dfrac{\mathbf{r}\_{u}\times\mathbf{r}\_{v}}{\lvert \mathbf{r}\_{u}\times\mathbf{r}\_{v} \rvert}$|
|Surface integral of a vector field over a parametric surface|$\iint\limits_{S} \mathbf{F}\cdot d\mathbf{S} = \iint\limits_{S} \mathbf{F}\cdot \mathbf{n} \ dS \newline = \iint\limits_{D} \mathbf{F}\cdot (\mathbf{r}_{u}\times\mathbf{r}_{v}) \ dA \newline = \iint\limits_{D} \left( -P \frac{\partial g}{\partial x} -Q \frac{\partial g}{\partial y} + R \right) dA$|

### Stoke's theorem

|Description|Equations|
|-:|:-|
|**Stoke's Theorem** <br/> *(S: oriented, piecewise-smooth surface <br/> C: simple, closed, piecewise-smooth curve <br/> F: continuous partial derivatives in open region)*|$\displaystyle\int_{C} \mathbf{F}\cdot d\mathbf{r} = \iint\limits_{S} (\nabla\times\mathbf{F})\cdot d\mathbf{S}$|
|Alternative surface <br/> ($C$ is a common curve of $S_{1}$ and $S_{2}$)|$\iint\limits_{S_{1}} (\nabla\times\mathbf{F})\cdot d\mathbf{S} \newline = \int_{C} \mathbf{F}\cdot d\mathbf{r} \newline = \iint\limits_{S_{2}} (\nabla\times\mathbf{F})\cdot d\mathbf{S}$|

### Divergence theorem (Gauss's theorem)

|Description|Equations|
|-:|:-|
|**Divergence Theorem** <br/> *(E: simple, solid region <br/> S: positively oriented surface <br/> F: continuous partial derivatives in open region)*|$\displaystyle\iint\limits_{S}\mathbf{F}\cdot d\mathbf{S} = \iiint\limits_{E}\nabla\cdot\mathbf{F} \ dV$|

## Appendix

### Types of functions

|Function Type|Domain $\to$ Range|Equation|Example|
|-|:-:|:-:|-|
|Function of several variables|$\R^{n} \to \R$|$f(\mathbf{x})$|$f(x, y, z) = \newline 2x^{2} + e^{y} - 5z^{3} - 7$|
|Vector-valued function|$\R \to \R^{n}$|$\mathbf{v}(t)$|$\mathbf{v}(t) = \newline \langle t^{2}, -2t, e^{t} \rangle$|
|Vector field|$\R^{n} \to \R^{n}$|$\mathbf{F}(\mathbf{x})$|$\mathbf{F}(x, y, z) = \newline \langle 3x-y, z, z^{2}-x \rangle$|
