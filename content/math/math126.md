---
title: "MATH 126 Calculus III"
date: 2021-08-17T00:00:00+08:00
---

## Vectors and Geometry of Space

### 3D Coordinate System

|Description|Equations|
|-:|:-|
|Distance formula|$d = \sqrt{(x_1-x_2)^2 + (y_1-y_2)^2 + (z_1-z_2)^2}$|
|Equation of a sphere <br/> centered at $(a,b,c)$|$(x-a)^2 + (y-b)^2 + (z-c)^2 = r^2$|
|Norm/length/magnitude of vectors|$\lvert \mathbf{a} \rvert = \sqrt{a_1^2 + a_2^2 + a_3^2}$|
|Vector addition and subtraction|$\mathbf{a} \pm \mathbf{b} = \langle a_1 \pm b_1, a_2 \pm b_2, a_3 \pm b_3 \rangle$|
|Vector scalar multiplication|$c\mathbf{a} = \langle ca_1, ca_2, ca_3 \rangle$|
|Properties of vectors|$\mathbf{a}+\mathbf{b} = \mathbf{b}+\mathbf{a} \newline \mathbf{a}+(\mathbf{b}+\mathbf{c}) = (\mathbf{a}+\mathbf{b})+\mathbf{c} \newline \mathbf{a}+\mathbf{0}=\mathbf{a} \newline \mathbf{a}+(-\mathbf{a}) = \mathbf{0} \newline c(\mathbf{a}+\mathbf{b}) = c\mathbf{a}+c\mathbf{b} \newline (c+d)\mathbf{a} = c\mathbf{a}+d\mathbf{a} \newline (cd)\mathbf{a} = c(d\mathbf{a}) \newline 1\mathbf{a}=\mathbf{a}$|
|Standard basis vectors|$\mathbf{i} = \langle 1,0,0 \rangle \newline \mathbf{j} = \langle 0,1,0 \rangle \newline \mathbf{k} = \langle 0,0,1 \rangle$|

### Dot product

|Description|Equations|
|-:|:-|
|Dot product|$\mathbf{a}\cdot\mathbf{b} = a_1b_1 + a_2b_2 + a_3b_3$|
|Properties of dot product|$\mathbf{a}\cdot\mathbf{a}=\lvert\mathbf{a}\rvert^2 \newline \mathbf{a}\cdot\mathbf{b}=\mathbf{b}\cdot\mathbf{a} \newline \mathbf{a}\cdot(\mathbf{b}+\mathbf{c}) = \mathbf{a}\cdot\mathbf{b} + \mathbf{a}\cdot\mathbf{c} \newline (c\mathbf{a})\cdot\mathbf{b}=c(\mathbf{a}\cdot\mathbf{b})=\mathbf{a}\cdot(c\mathbf{b}) \newline \mathbf{0}\cdot\mathbf{a} = \mathbf{0}$|
|Dot product and angle between vectors|$\mathbf{a}\cdot\mathbf{b} = \lvert\mathbf{a}\rvert\lvert\mathbf{b}\rvert\cos\theta \newline \cos\theta = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\lvert\mathbf{a}\rvert\lvert\mathbf{b}\rvert}$|
|Dot product to check orthogonal vectors|$\mathbf{a}\cdot\mathbf{b} = 0$|
|Direction angles and direction cosines|$\cos\alpha = \dfrac{\mathbf{a}\cdot\mathbf{i}}{\lvert\mathbf{a}\rvert\lvert\mathbf{i}\rvert} = \dfrac{a_1}{\lvert\mathbf{a}\rvert} \newline \cos\beta = \dfrac{a_2}{\lvert\mathbf{a}\rvert} \newline \cos\gamma = \dfrac{a_3}{\lvert\mathbf{a}\rvert}$|
|Unit vector and direction cosines|$\dfrac{\mathbf{a}}{\lvert\mathbf{a}\rvert} = \langle \cos\alpha, \cos\beta, \cos\gamma \rangle$|
|Scalar projection of $\mathbf{b}$ onto $\mathbf{a}$|$\mathrm{comp}_{\mathbf{a}}\mathbf{b} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\lvert\mathbf{a}\rvert}$|
|Vector projection of $\mathbf{b}$ onto $\mathbf{a}$|$\mathrm{proj}_{\mathbf{a}}\mathbf{b} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\lvert\mathbf{a}\rvert}\dfrac{\mathbf{a}}{\lvert\mathbf{a}\rvert} = \dfrac{\mathbf{a}\cdot\mathbf{b}}{\lvert\mathbf{a}\rvert^2}\mathbf{a}$|

### Cross product

|Description|Equations|
|-:|:-|
|Cross product|$\mathbf{a}\times\mathbf{b} = \begin{vmatrix} a_1 & a_2 & a_3 \cr b_1 & b_2 & b_3 \cr c_1 & c_2 & c_3 \end{vmatrix} = \newline \langle a_2b_3-a_3b_2, a_3b_1-a_1b_3, a_1b_2-a_2b_1\rangle$|
|Cross product to generate orthogonal vectors|$\mathbf{a}\times\mathbf{b}$ is orthogonal to both $\mathbf{a}$ and $\mathbf{b}$|
|Cross product and angle between vectors|$\lvert\mathbf{a}\times\mathbf{b}\rvert = \lvert\mathbf{a}\rvert\lvert\mathbf{b}\rvert \sin\theta$|
|Cross product to check parallel vectors|$\mathbf{a}\times\mathbf{b} = \mathbf{0}$|
|Cross product as the area of parallelogram|$A = \lvert\mathbf{a}\times\mathbf{b}\rvert$|
|Cross products of standard basis vectors|$\mathbf{i}\times\mathbf{j} = \mathbf{k} \newline \mathbf{j}\times\mathbf{k} = \mathbf{i} \newline \mathbf{k}\times\mathbf{i} = \mathbf{j}$|
|Properties of cross product|$\mathbf{a}\times\mathbf{b} = -\mathbf{b}\times\mathbf{a} \newline (c\mathbf{a})\times\mathbf{b} = c(\mathbf{a}\times\mathbf{b}) = \mathbf{a}\times(c\mathbf{b}) \newline \mathbf{a}\times(\mathbf{b}+\mathbf{c}) = \mathbf{a}\times\mathbf{b}+\mathbf{a}\times\mathbf{c} \newline (\mathbf{a}+\mathbf{b})\times\mathbf{c} = \mathbf{a}\times\mathbf{c} + \mathbf{b}\times\mathbf{c} \newline \mathbf{a}\cdot(\mathbf{b}\times\mathbf{c}) = (\mathbf{a}\times\mathbf{b})\cdot\mathbf{c} \newline \mathbf{a}\times(\mathbf{b}\times\mathbf{c}) = (\mathbf{a}\cdot\mathbf{c})\mathbf{b} - (\mathbf{a}\cdot\mathbf{b})\mathbf{c}$|
|Scalar triple product as volume of parallelepiped|$V = \lvert \mathbf{a}\cdot(\mathbf{b}\times\mathbf{c}) \rvert$|
|Scalar triple product to check three coplanar vectors|$V=\mathbf{a}\cdot(\mathbf{b}\times\mathbf{c})=0$|

### Equations of lines

|Description|Equations|
|-:|:-|
|Vector equation of a line|$\mathbf{r} = \mathbf{r}_0 + t\mathbf{v}$|
|Parametric equations of a line <br/> through $(x_0, y_0, z_0)$, in direction of $\langle a, b, c \rangle$|$x=x_0+at \newline y = y_0+bt \newline z=z_0+ct$|
|Symmetric equation of a line|$\dfrac{x-x_0}{a} = \dfrac{y-y_0}{b} = \dfrac{z-z_0}{c}$|

### Equations of planes

|Description|Equations|
|-:|:-|
|Vector equation of a line segment|$\mathbf{r}(t) = (1-t)\mathbf{r}_0+t\mathbf{r}_1 \newline t\in[0,1]$|
|Vector equation of a plane|$\mathbf{n}\cdot(\mathbf{r}-\mathbf{r}_0) = 0 \newline \mathbf{n}\cdot\mathbf{r} = \mathbf{n}\cdot\mathbf{r}_0$|
|Scalar equation of a plane <br/> through $(x_0, y_0, z_0)$, normal vector $\langle a,b,c \rangle$|$a(x-x_0)+b(y-y_0)+c(z-z_0)=0$|
|Linear equation of a plane|$ax+by+cz+d=0$|
|Distance from a point to a plane|$D = \dfrac{\lvert ax_1+by_1+cz_1+d \rvert}{\sqrt{a^2+b^2+c^2}}$|

### Cylinders and quadratic surfaces

|Description|Equations|
|-:|:-|
|Ellipsoid|$\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}+\dfrac{z^2}{c^2}=1$|
|Cone|$\dfrac{z^2}{c^2}=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}$|
|Elliptic paraboloid|$\dfrac{z}{c}=\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}$|
|Hyperbolic paraboloid|$\dfrac{z}{c}=\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}$|
|Hyperboloid of one sheet|$\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}-\dfrac{z^2}{c^2}=1$|
|Hyperboloid of two sheets|$-\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}+\dfrac{z^2}{c^2}=1$|

## Vectors Functions

### Vector functions and space curves

|Description|Equations|
|-:|:-|
|Vector-valued function|$\mathbf{r}(t) = \langle f(t), g(t), h(t) \rangle$|
|Limit of a vector function|$\lim\limits_{t\to a}\mathbf{r}(t) = \langle \lim\limits_{t\to a}f(t), \lim\limits_{t\to a}g(t), \lim\limits_{t\to a}h(t) \rangle$|
|Continuity of vector function|$\lim\limits_{t\to a}\mathbf{r}(t) = \mathbf{r}(t)$|
|Parametric equation of space curves|$x = f(t) \newline y = g(t) \newline z = h(t)$|
|Derivative of vector function|$\mathbf{r}'(t) = \lim\limits_{h\to 0}\dfrac{\mathbf{r}(t+h) - \mathbf{r}(t)}{h}$|
|Derivative of vector function|$\mathbf{r}'(t) = \langle f'(t), g'(t), h'(t) \rangle$|
|Differentiation rules|$[\mathbf{u}(t)+\mathbf{v}(t)]' = \mathbf{u}'(t) + \mathbf{v}'(t)\newline$ $[c\mathbf{u}(t)]' = c\mathbf{u}'(t)\newline$ $[f(t)\mathbf{u}(t)]' = f'(t)\mathbf{u}(t) + f(t)\mathbf{u}'(t)\newline$ $[\mathbf{u}(t)\cdot\mathbf{v}(t)]' = \mathbf{u}'(t)\cdot\mathbf{v}(t) + \mathbf{u}(t)\cdot\mathbf{v}'(t)\newline$ $[\mathbf{u}(t)\times\mathbf{v}(t)]' = \mathbf{u}'(t)\times\mathbf{v}(t) + \mathbf{u}(t)\times\mathbf{v}'(t)\newline$ $[\mathbf{u}(f(t))]' = f'(t)\mathbf{u}'(f(t))$|
|Definite integral of vector function|$\int_a^b \mathbf{r}(t) \ dt \newline = \langle \int_a^b f(t) \ dt, \int_a^b g(t) \ dt, \int_a^b h(t) \ dt \rangle$|
|Position vector|$\mathbf{r}(t)$|
|Tangent (velocity) vector|$\mathbf{r}'(t)$|
|Unit tangent vector|$\mathbf{T}(t) = \dfrac{\mathbf{r}'(t)}{\lvert\mathbf{r}'(t)\rvert}$|

### Arc length and curvature

|Description|Equations|
|-:|:-|
|Length of a curve|$\begin{aligned}L &= \textstyle\int_a^b \lvert\mathrm{r}'(t)\rvert \ dt \cr &= \textstyle\int_a^b \sqrt{[f(t)]^2+[g(t)]^2+[h(t)]^2} \ dt\end{aligned}$|
|Arc length function|$\begin{aligned}s(t) &= \textstyle\int_a^t \lvert\mathrm{r}'(u)\rvert \ du \cr &= \textstyle\int_a^t \sqrt{[f(u)]^2+[g(u)]^2+[h(u)]^2} \ du\end{aligned}$|
|Rate of change in arc length and the tangent vector|$\dfrac{ds}{dt} = \lvert \mathbf{r}'(t) \rvert$|
|Curvature|$\kappa(t) = \bigg\lvert\dfrac{d\mathbf{T}}{ds}\bigg\rvert = \dfrac{\lvert\mathbf{T}'(t)\rvert}{\lvert\mathbf{r}'(t)\rvert} = \dfrac{\lvert\mathbf{r}'(t)\times\mathbf{r}''(t)\rvert}{\lvert\mathbf{r}'(t)\rvert^3}$|
|Curvature in terms of function|$\kappa(x) = \dfrac{\lvert f''(x)\rvert}{[1+(f'(x))^2]^{3/2}}$|
|Unit normal vector|$\mathbf{N}(t) = \dfrac{\mathbf{T}'(t)}{\lvert\mathbf{T}'(t)\rvert}$|
|Binormal vector|$\mathbf{B}(t) = \mathbf{T}(t)\times\mathbf{N}(t)$|
|Radius of osculating circle|$r = \frac{1}{\kappa}$|

### Velocity and acceleration

|Description|Equations|
|-:|:-|
|Position vector|$\mathbf{r}(t)$|
|Tangent (velocity) vector|$\mathbf{v}(t) = \mathbf{r}'(t)$|
|Acceleration vector|$\mathbf{a}(t) = \mathbf{v}'(t)$|
|Tangential and normal components of acceleration|$\mathbf{a}(t) = v'\mathbf{T}+\kappa v^2\mathbf{N}$|

## Partial Derivatives

### Function of several variables

|Description|Equations|
|-:|:-|
|Functions of two variables|$\{f(x,y) \vert (x, y) \in D\} \newline z = f(x,y)$|
|Level curves|$f(x,y) = k$|
|Function of three variables|$\{f(x,y,z) \vert (x, y, z) \in E\}$|
|Level surfaces|$f(x,y,z)=k$|
|Function of $n$ variables|$f(\mathbf{x}) = \mathbf{c}\cdot\mathbf{x}$|
|Interpretation of input of functions of several variables|1. $n$ real variables $x_1, x_2,..., x_n$ <br/> 2. a single point variable $(x_1, x_2,..., x_n)$ <br/> 3. a single vector variable $\mathbf{x} = \langle x_1, x_2,..., x_n \rangle$|
|Limit of function of two variables|$\lim\limits_{(x,y)\to(a,b)}f(x,y)=L$|
|Continuity of function of two variables|$\lim\limits_{(x,y)\to(a,b)}f(x,y)=f(a,b)$|
|Limit of function of several variables|$\lim\limits_{\mathbf{x}\to\mathbf{a}}f(\mathbf{x})=L$|
|Continuity of function of several variables|$\lim\limits_{\mathbf{x}\to\mathbf{a}}f(\mathbf{x})=f(\mathbf{a})$|

### Partial derivatives

|Description|Equations|
|-:|:-|
|Partial derivative with respect to $x$|$f_x(x,y) = \lim\limits_{h\to 0}\dfrac{f(x+h,y)-f(x,y)}{h}$|
|Partial derivative with respect to $y$|$f_y(x,y) = \lim\limits_{h\to 0}\dfrac{f(x,y+h)-f(x,y)}{h}$|
|Partial derivative rule|1. To find $f_x$, regard $y$ as a constant and differentiate $f(x,y)$ with respect to $x$ <br/> 2. To find $f_y$, regard $x$ as a constant and differentiate $f(x,y)$ with respect to $y$|
|Clairaut's theorem|$f_{xy}(a,b) = f_{yx}(a,b)$|

### Tangent plane and linear approximations

|Description|Equations|
|-:|:-|
|Tangent plane to a surface <br/> $z=f(x,y)$ at $(x_0,y_0,z_0)$|$z-z_0=f_x(x_0,y_0)+f_y(x_0,y_0)(y-y_0)$|
|Linear approximation|$f(x,y) \approx f(a,b)+f_x(a,b)(x-a)+f_y(a,b)(y-b)$|
|Total differential|$dz = f_x(x,y) dx + f_y(x,y) dy$|

### Extreme values

|Description|Equations|
|-:|:-|
|Critical point|a point with $f_x(a,b)=0$ and $f_y(a,b)=0$, $(\nabla f=\mathbf{0})$, or one of the partial derivatives does not exist|
|Local max/min and critical point|If $f$ has a local max/min at $(a,b)$, <br/> then $(a,b)$ is a critical point|
|Second derivative test <br/> ($(a,b)$ is a critical point)|$D(a,b) = f_{xx}(a,b)f_{yy}(a,b) - [f_{xy}(ab)]^2 \newline$ $= \begin{vmatrix} f_{xx} & f_{xy} \cr f_{yx} & f_{yy} \end{vmatrix}$ <br/> (a) If $D>0$ and $f_{xx}(a,b)>0$, <br/> then $f(a,b)$ is a local max <br/> (b) If $D>0$ and $f_{xx}(a,b)<0$, <br/> then $f(a,b)$ is a local min <br/> (c) If $D<0$, <br/> then $f(a,b)$ is a saddle point|
|Extreme value theorem for functions of two variables|If $f$ is continuous on a closed, bounded set $D\in \R^2$, <br/> then $f$ attains a absolute max and min at some points in $D$|
|Closed boundary method <br/> (Finding absolute max/min)|1. Find the values of $f$ at the critical points of $f$ in $D$ <br/> 2. Find the extreme values of $f$ on the boundary of $D$ <br/> 3. The largest value is the abs max; the smallest value is the abs min|

### Other topics

Chain rule, directional derivative, and gradient vector are not covered in MATH 126 but covered in [MATH 324](math324.html).

## Double Integrals

MATH 126 covers double integrals in Cartesian coordinates and polar coordinates with applications. They are reviewed in [MATH 324](math324.html).

## Taylor Series

### Linear and quadratic approximations

|Description|Equations|
|-:|:-|
|First Taylor polynomial<br/> (Tangent line approximation)|$T_1(x) \approx f(b) + f'(b)(x-b)$|
|Tangent line error|$\lvert E_1 \rvert = \bigg\lvert f(x) - [f(b)+f'(b)(x-b)] \bigg\rvert$|
|Tangent line error bound|$\lvert f''(t) \rvert \le M \newline \lvert E_1 \rvert \le \dfrac{M}{2}\lvert x-b \rvert^2$|
|Second Taylor polynomial <br/> (Quadratic approximation)|$T_2(x) = f(b) + f'(b)(x-b)+\frac{1}{2}f''(b)(x-b)^2$|
|Quadratic approximation error|$\lvert E_2 \rvert = \lvert f(x) - T_2(x) \rvert$|
|Quadratic approximation error bound|$\lvert E_2 \rvert \le \dfrac{M}{6}\lvert x-b \rvert^3$|

### Taylor polynomial and series

|Description|Equations|
|-:|:-|
|$n$th Taylor polynomial|$T_n(x) = \displaystyle\sum\limits_{k=0}^{n} \dfrac{f^{(k)}(b)}{k!} (x-b)^k \newline$ $= f(b) + f'(b)(x-a) + \dfrac{f''(b)}{2!}(x-a)^2 + ... + \dfrac{f^{(n)}(b)}{n!} (x-b)^n$|
|Taylor inequality <br/> $(\lvert f^{(n+1)}(t) \rvert \le M)$|$\lvert f(x) - T_n(x) \rvert \le \dfrac{M}{(n+1)!} \lvert x-b \rvert^{n+1}$|
|Taylor series|$\lim\limits_{n\to\infin}T_n(x) \newline$ $= \displaystyle\lim\limits_{n\to\infin}\sum\limits_{k=0}^{n} \dfrac{f^{(k)}(b)}{k!} (x-b)^k \newline$ $= \sum\limits_{k=0}^{\infin} \dfrac{f^{(k)}(b)}{k!} (x-b)^k$|
|Taylor series of exponential function|$e^x = \displaystyle\sum\limits_{k=0}^{\infin} \dfrac{x^{k}}{k!}$|
|Taylor series of sine|$\cos(x) = \displaystyle\sum\limits_{k=0}^{\infin} (-1)^k \dfrac{x^{2k}}{(2k)!}$|
|Taylor series of cosine|$\sin(x) = \displaystyle\sum\limits_{k=0}^{\infin} (-1)^k \dfrac{x^{2k+1}}{(2k+1)!}$|
|Geometric series as Taylor series <br/> $x\in(-1,1)$|$\dfrac{1}{1-x} = \displaystyle\sum\limits_{k=0}^{\infin} x^k$|
