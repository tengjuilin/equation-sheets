---
title: "AMATH 351 Differential Equations and Applications"
date: 2021-08-17T00:00:00+08:00
---

## First Order Differential Equations

### First order ODE concepts

- *Differential equations (DE)* - relationship between an unknown function $y$ and its derivative
  - $F(y(x), y\'(x), y\'\'(x), ...) = 0$
- *Order* - order of the highest order derivative in the DE
- *Ordinary differential equation (ODE)* - contains derivative with respect to only 1 variable
- *Partial differential equation (PDE)* - contains derivative with respect to multiple variables
- *Linear* - unknowns of DE do not appear as argument of nonlinear functions or multiply with each other or themselves
- *Valid solution* - a solution of an ODE that does not...
  - have a complex number
  - have $\lim\limits_{x\to a} = \infty$ ($\lim\limits_{x\to \infty} = \infty$ is ok)
  - have division by zero
  - have undefined operation (e.g. $\ln(-2)$)
- *Interval of validity* - the largest interval where the solution is valid.
- *Distinct solution* - $y_{1}(x) \not = y_{2}(x)$ for some $x$

#### Existence and uniqueness theorem

- [x] 1st order ODE
- Consider the IVP $y\' = f(t, y)$, $y(0) = 0$.
  - first order ODE only
- If $f$ and $\frac{\partial f}{\partial y}$ are continuous for $\lvert t \rvert \le a, \lvert y \rvert \le b$,
  - then there exists a $\lvert t \rvert \le h \le a$ such that there exists a unique solution $y(t) = \phi(t)$ of the IVP.

### Solving initial value problems (IVP)

Given some initial values $y(0) = a_{0}, y\'(0) = a_{1}, ..., y^{(n)}(0) = a_{n}$. Solve the ODE $F(y(x), y\'(x), y\'\'(x), ...) = 0$

1. Find the general solution to the ODE (or verify a given solution).
2. Plug in any initial values to determine the values of unknown constants in the ODE general solution.
3. Check if there is any additional prompt to do with the solution of the ODE.

### Solving ODEs using separation of variables

- [x] 1st order
- [x] Nonlinear, linear
- [x] Separable

1. Write the DE in the form of separable DE $\dfrac{dy}{dx} = g(x) h(y)$.
2. Check if $h(y) = 0$ generates trivial solutions.
3. Separate the $x$ and $y$ terms: $\dfrac{dy}{h(y)} = g(x) dx$. (Don't consider int. const.)
4. Integrate both sides and add constant of integration: $\displaystyle\int\dfrac{dy}{h(y)} = \int g(x) dx$.
   1. Solve for $y$ for explicit solution.
5. IVP

### Solving ODEs using integrating factors

- [x] 1st order
- [x] Linear

1. Write the DE in the form of $y\'(x) + p(x)y(x) = q(x)$.
2. Find the integrating factor $\mu(x) = \exp(\int p(x)dx)$.
3. The solution is in the form $y(x) = \dfrac{\displaystyle\int \mu(x)q(x)dx + C}{\mu(x)}$.
4. IVP

### Solving exact ODEs

- [x] 1st order
- [x] Nonlinear, linear
- [x] Exact

1. Write the DE in the form of $N(x, y)y\' + M(x, y) = 0$
   1. Let $y = f(x, y)$.
   2. Let $M(x, y) = \dfrac{\partial f}{\partial x}$, and $N(x, y) = \dfrac{\partial f}{\partial y}$
2. Check if the DE is an exact DE by verifying $\dfrac{\partial M}{\partial y} = \dfrac{\partial N}{\partial x}$
3. Find the solution $f(x, y)$ using one of the following methods:
   - Method A1
      1. Find $\displaystyle f(x, y) = \int \partial f = \int M \ \partial x = f_{\text{main}}(x, y) + h(y)$.
      2. Solve for $h\'(y)$ in $N = \dfrac{\partial f}{\partial y} = \dfrac{\partial f_{\text{main}}}{\partial y} + h\'(y)$.
      3. Solve for $h(y)$ and plug in $f(x, y)$.
   - Method A2
      1. Find $\displaystyle f(x, y) = \int \partial f = \int N \ \partial y = f_{\text{main}}(x, y) + g(x)$.
      2. Solve for $g\'(x)$ in $M = \dfrac{\partial f}{\partial x} = \dfrac{\partial f_{\text{main}}}{\partial x} + g\'(x)$.
      3. Solve for $g(x)$ and plug in $f(x, y)$.
   - Method B
     - Do not consider int. const. $g(x)$ and $h(y)$ in the following steps.

      1. Find $\displaystyle f_{1}(x, y) \equiv \int \partial f = \int M \ \partial x \equiv f_{\text{mixed-terms}}(x, y) + f_{\text{y-terms}}(y)$
      2. Find $\displaystyle f_{2}(x, y) \equiv \int \partial f = \int N \ \partial y \equiv f_{\text{mixed-terms}}(x, y) + f_{\text{x-terms}}(x)$
      3. Match up the terms to get the solution <br/> $f(x, y) = f_{\text{mixed-terms}}(x, y) + f_{\text{x-terms}}(x) + f_{\text{y-terms}}(y) = C$
4. IVP

### Solving ODEs using substitution

- [x] 1st order
- [x] Nonlinear, linear

1. Substitute function $y$ with $u$ to find an easy-to-solve ODE by...
   1. Given DE $y\' = f(x, y)$,
      - write the DE in terms of $y\'$
      - find the substitution $u = u(x, y(x))$
      - find the inverse substitution $y = y(x, u(x))$
   2. By chain rule, find $u\' = \dfrac{\partial u}{\partial x} + \dfrac{\partial u}{\partial y} y\'$.
   3. Substitution (replace $y\'$ with original ODE): <br/> $u\' = \dfrac{\partial u}{\partial x} + \dfrac{\partial u}{\partial y} y\' \xleftarrow{y\'} y\' = f(x, y)$ <br/> $u\' = \dfrac{\partial u}{\partial x} + \dfrac{\partial u}{\partial y} f(x, y) \equiv F(x, y, u)$
   4. Substitution (replace $y$ with inverse substitution): <br/> $u\' = F(x, y, u) \xleftarrow{y} y(x, u(x))$ <br/> $u\' = F(x, y(x, u), u) \equiv G(x, u)$
2. Solve the ODE $u\' = G(x, u)$ for $u(x)$.
3. Substitution: <br/> $y(x, u(x)) \xleftarrow{u(x)} u(x)$ <br/> $y(x)$
4. IVP

### Mathematical modeling

#### Radioactive decay

|Description|Equations|
|-:|:---|
|DE of radioactive decay|$\dfrac{dN}{dt} = -k N(t)$|
|Number of nuclei over time (solution)|$N(t) = N(0)e^{-kt} = N_{0}e^{-kt}$|
|Half life|$N(\tau) = \dfrac{N_{0}}{2}$|
|Decay constant|$k = \dfrac{\ln2}{\tau}$|
|Radioactive dating|$t = \dfrac{\ln \left( \dfrac{N_{1}(t)}{N_{2}(t)} \dfrac{N_{2}(0)}{N_{1}(0)} \right)}{\ln 2} \dfrac{\tau_{1}\tau_{2}}{\tau_{1} - \tau_{2}}$|

#### Other equations

|Description|Equations|
|-:|:---|
|Logistic equation <br/> ($r, k > 0$)|$P\'(t) = r \left( 1-\dfrac{P}{k} \right)P$|
|**Bernoulli equation**|$y\' + p(t)y = q(t)y^{n}$|
|General solutions of Bernoulli equation <br/>($n = 1,2,3$)|$n = 0: y(t) = \dfrac{\displaystyle\int e^{\int p(t) dt} q(t) dt + C}{e^{\int p(t) dt}} \newline n = 1: y(t) = Ce^{\int q(t)-p(t) \ dt} \newline n = 2: y(t) = \dfrac{-e^{-\int p(t) dt}}{\displaystyle\int e^{-\int p(t) dt} q(t) dt + C}$|
|General solutions of Bernoulli equation|$\forall n: y(t) = \left( \dfrac{1-n}{f(t)} \displaystyle\int q(t)f(t) dt \right)^{1/(1-n)}$ <br/> where $f(t) = e^{\int (1-n) p(t) dt}$|
|**Riccati equation**|$y\' = q_{0}(t) + q_{1}(t)y + q_{2}(t)y^{2}$|
|Solving  Riccati equation known particular solution $y_{1}$|$y = y_{1} + \dfrac{1}{v(t)}$, where $v$ satisfies <br/> $v\'(t) = -(q_{1} + 2q_{2}y_{1})v - q_{2}$|
|General solutions of Riccati equation <br/> known particular solution $y_{1}$|$y = y_{1} + \dfrac{\mu(t)}{-\displaystyle\int \mu(t)q_{2} dt + C}$ <br/> where $\mu(t) = e^{\int q_{1}+2q_{2}y_{1} \ dt}$|

### Stability and phase plane analysis

1. Plot $P\'(t)$ vs $P(t)$.
2. Find fixed point $P^{*}$ such that $P\' = 0$
   - x-intercept of $P\'(t)$ vs $P(t)$ plot
   - a solution with initial value $P(0) = P^{*}$ is constant over time
3. Draw flow arrows near fixed points
   - $P\' > 0$ flows to the right
   - $P\' < 0$ flows to the left
4. Identify stability of fixed points by flow arrows
   - stable - solution approaches the fixed point
   - unstable - solution diverges from the fixed point
   - semi-stable - solution approaches the fixed point from one side and diverges from another
5. Sketch solution $P(t)$ vs. $t$ so that
   - $P$ increases in region flow to the right
   - $P$ decreases in region flow to the left
   - solution approaches to stable fixed point
   - solution diverges from unstable fixed point

## Second Order Differential Equations

### Second order ODE concepts

- Second order linear differential equation - $r(x)y\'\' + p(x)y\' + q(x)y = g(x)$
- Homogeneous - $g(x) = 0$
- Non-homogeneous - $g(x) \not= 0$
- Linearly independent - $c_{1}f(x) + c_{2}g(x) = 0$ can only be satisfied by choosing $c_{1} = c_{2} = 0$ for functions $f, g$
- Wronskian - $W(f, g)(x) = fg\' - f\' g$

#### Principle of superposition

- [x] 2nd order homogeneous ODE

- Consider 2nd order homogeneous ODE $r(x)y\'\' + p(x)y\' + q(x)y = 0$.
- If Wronskian $W(y_{1}, y_{2}) \not = 0$ ($y_{1}$ and $y_{2}$ are linearly independent solution of the ODE),
  - then the general solution of the ODE is $y(x) = c_{1}y_{1}(x) + c_{2}y_{2}(x)$.

#### Wronskian and linear (in)dependence

- Two functions $f$ and $g$ are linearly dependent
  - if their Wronskian $W(f, g)(x) = fg\' - f\' g = 0$.
- Corollary
  - two linearly independent functions $f$ and $g$ has $W(f, g)(x) \not= 0$.

#### Abel's theorem

- If $y_{1}$ and $y_{2}$ be any two solutions of $y\'\' + p(x)y\' + q(x)y = 0$,
  - then $W(y_{1}, y_{2}) = xe^{-\int p(d) dx}$.
- Corollary: reduction of order formula
  - Known $y_{1}$, then $y_{2} = y_{1}\displaystyle\int\dfrac{W}{y_{1}^{2}}dx$

#### Euler's formula

- $e^{i\beta x} = \cos(\beta x) + i\sin(\beta x)$
- $e^{-i\beta x} = \cos(\beta x) - i\sin(\beta x)$

### Solving 2nd order homogeneous constant coefficient ODEs

- [x] 2nd order
- [x] Linear
- [x] Constant coefficient
- [x] Homogeneous

1. Write the ODE in the form of $ay\'\' + by\' + cy = 0$.
2. Write the characteristic equation $a\lambda^{2} + b\lambda + c = 0$.
3. Solve the characteristic equation $\lambda_{1}, \lambda_{2} = \dfrac{-b \pm \sqrt{b^{2} - 4ac}}{2a}$.
   - If $\lambda_{1} \not = \lambda_{2}$ and $\lambda_{1}, \lambda_{2} \in \Reals$,
     - then the general solution is $y(x) = c_{1}e^{\lambda_{1}x} + c_{2}e^{\lambda_{2}x}$.
   - If $\lambda_{1} = \lambda_{2}$, and $\lambda_{1}, \lambda_{2} \in \Reals$,
     - then the general solution is $y(x) = c_{1}e^{\lambda_{1}x} + c_{2}xe^{\lambda_{1}x}$.
     - [by Abel's theorem and reduction of order](#abels-theorem)
   - If $\lambda_{1} \not = \lambda_{2}$, and $\lambda_{1}, \lambda_{2} \in \Complex$, where $\lambda_{1}, \lambda_{2} = \alpha \pm i\beta$,
     - then the general solution is $y(x) = c_{1}e^{\alpha x} \cos(\beta x) + c_{2}e^{\alpha x} \sin(\beta x)$,
     - where $\alpha = -\dfrac{b}{2a}$, $\beta = \dfrac{\sqrt{4ac-b^{2}}}{2a}$.
     - [by Euler's formula](#eulers-formula)
4. IVP

#### Solving ODEs by reduction of order

- [x] 2nd order
- [x] Linear
- [x] Non-constant coefficient, constant coefficient
- [x] Homogeneous

0. Given a solution $y_{1}$.
1. Write the ODE in the form of $y\'\' + p(x) y\' + q(x)y = 0$.
2. Calculate the Wronskian by Abel's Theorem $W = ce^{-\int p(x)dx}$.
3. Find $y_{2}$ by reduction of order formula $y_{2} = y_{1} \displaystyle\int \dfrac{W}{y_{1}^{2}} \ dx$.
4. Pick a convenient coefficient $c$ (but $c \not= 0$).
5. Write the general solution $y(x) = c_{1}y_{1}(x) + c_{2}y_{2}(x)$.
6. IVP

### Solving Euler equation

- [x] 2nd order
- [x] Linear
- [x] Non-constant coefficient (of special type)
- [x] Homogeneous
- [x] Euler equation

1. Write the ODE in the form of $x^{2}y\'\' + \alpha xy\' + \beta y = 0$.
2. Write the indicial equation $s^{2} + (\alpha - 1)s + \beta = 0$.
3. Solve the indicial equation $s_{1}, s_{2} = \dfrac{1 - \alpha \pm \sqrt{(\alpha - 1)^{2} - 4\beta}}{2}$.
   - If $s_{1} \not = s_{2}$ and $s_{1}, s_{2} \in \Reals$,
     - then the general solution is $y(x) = c_{1}x^{s_{1}} + c_{2}x^{s_{2}}$.
   - If $s_{1} = s_{2}$, and $s_{1}, s_{2} \in \Reals$,
     - then the general solution is $y(x) = c_{1}x^{s_{1}} + c_{2}\ln(x)x^{s_{1}}$.
     - [by Abel's theorem and reduction of order](#abels-theorem)
   - If $s_{1} \not = s_{2}$, and $s_{1}, s_{2} \in \Complex$, where $s_{1}, s_{2} = \eta \pm i\mu$,
     - then the general solution is <br/> $y(x) = c_{1}x^{\eta} \cos(\mu \ln(x)) + c_{2}x^{\eta} \sin(\mu \ln(x))$,
     - where $\eta = -\dfrac{1-\alpha}{2}$, $\mu = \dfrac{\sqrt{4\beta-(\alpha - 1)^{2}}}{2}$.
     - [by Euler's formula](#eulers-formula)
4. IVP

### Solving nonhomogeneous ODEs by method of undetermined coefficients

- [x] 2nd order
- [x] Linear
- [x] Constant coefficient
- [x] Nonhomogeneous

1. Write the ODE in the form of $L[y] \equiv ay\'\' + by\' + cy = g(x)$.
2. Calculate the solution $y_{H}$ to the homogeneous problem $L[y_{H}] = 0$.
3. Guess a particular solution $y_{P}$ to the nonhomogeneous problem $L[y_{H}] = g(x)$.
4. Substitute $y_{P}$ into the ODE and solve for any constants.
5. Write the general solution $y(x) = y_{H}(x) + y_{P}(x)$.
6. IVP

#### Rules for guessing $y_{P}$

- Consider each term of nonhomogeneity $g(x)$ separately.
- Beware of the constants
  - Changes
    - $\alpha \to A$
    - $\beta \to B$
    - $P_{n}(x) \to S_{n}(x)$ contains $\alpha_{i} \to A_{i}, \forall n$
    - $Q_{m}(x) \to T_{m}(x)$ contains $\alpha_{i} \to A_{i}, \forall n$
  - No changes
    - $k, \omega$
- If a term of guessed $y_{P}$ conflicts with $y_{H}$, then multiply the term of guessed $y_{P}$ (not the entire guess of $y_{P}$) by $x$.

|Term of Nonhomogeneity $g(x)$|Term of guessed particular solution $y_{P}$|
|-:|:-|
|$\alpha$|$A$|
|$\alpha e^{kx}$|$A e^{kx}$|
|$P_{n}(x) = \sum\limits_{i=0}^{n} \alpha_{i}x^{i}$|$S_{n}(x) = \sum\limits_{i=0}^{n} A_{i}x^{i}$|
|$e^{k x}P_{n}(x)$|$e^{k x}S_{n}(x)$|
|$\alpha\cos(\omega x) + \beta\sin(\omega x)$|$A\cos(\omega x) + B\sin(\omega x)$|
|$P_{n}(x)\cos(\omega x) + Q_{m}(x)\sin(\omega x)$|$S_{n}(x)\cos(\omega x) + T_{m}(x)\sin(\omega x)$|
|$e^{k x}[P_{n}(x)\cos(\omega x) + Q_{m}(x)\sin(\omega x)]$|$e^{k x}[S_{n}(x)\cos(\omega x) + T_{m}(x)\sin(\omega x)]$|

### Solving nonhomogeneous ODEs by variation of parameters

- [x] 2nd order
- [x] Linear
- [x] Non-constant coefficient, constant coefficient
- [x] Nonhomogeneous

1. Write the ODE in the form of $L[y] \equiv y\'\' + p(x)y\' + r(x)y = g(x)$.
2. Calculate the solution to the homogeneous problem $L[y_{H}] = 0$
   - $y_{H} = c_{1}y_{1} + c_{2}y_{2}$
3. Calculate the Wronskian $W(y_{1}, y_{2})$
4. Calculate the particular solution $y_{P}$ to the nonhomogeneous problem $L[y_{H}] = g(x)$
   - $y_{P} = -y_{1} \displaystyle\int \dfrac{g(x)y_{2}}{W(y_{1}, y_{2})} dx + y_{2} \int \dfrac{g(x)y_{1}}{W(y_{1}, y_{2})} dx$
5. Write the general solution $y(x) = y_{H}(x) + y_{P}(x)$.
6. IVP

### Mechanical vibrations

- A mass on a spring moves vertically in a fluid bath on Earth.
- Newton's second law adds up all the forces
  - $\sum F = mx\'\'(t)$
  - $F_{\mathrm{damper}} = -\gamma x\'(t)$
  - $F_{\mathrm{spring}} = -kx(t)$
  - $F_{\mathrm{external}}$
- ODE: $mx\'\'(t) + \gamma x\'(t) + kx(t) = F_{\mathrm{ext}}(t)$

#### Unforced oscillation

- No external force on the system: $F_{\mathrm{ext}}(t) \equiv 0$
- Homogeneous ODE: $\boxed{mx\'\' + \gamma x\' + kx = 0} \ (m > 0, \gamma, k \ge 0)$
  - Overdamped system
    - $\gamma^{2} - 4mk > 0$
    - $\lambda_{1} \not= \lambda_{2} \in \Reals$
    - General solution: $x(t) = c_{1}e^{\lambda_{1}t} + c_{2}e^{\lambda_{2}t}$
  - Critically damped system
    - $\gamma^{2} - 4mk = 0$
    - $\lambda_{1} = \lambda_{2} \in \Reals$
    - General solution: $x(t) = c_{1}e^{\lambda_{1}t} + c_{2}te^{\lambda_{2}t}$
  - Underdamped system
    - $\gamma^{2} - 4mk < 0$
    - $\lambda_{1} \not= \lambda_{2} \in \Complex$
    - General solution: $x(t) = e^{-\gamma t/2m} [c_{1} \cos(\omega t) + c_{2}\sin(\omega t)]$
    - Undamped spring
      - $\gamma = 0$
      - General solution: $x(t) = c_{1} \cos(\omega t) + c_{2}\sin(\omega t)$
      - Phase-amplitude form: $x(t) = A\cos(\omega t - \varphi)$
        - amplitude $A = \sqrt{c_{1}^{2}+c_{2}^{2}}$
        - phase $\varphi = \arctan(c_{2}/c_{1})$
        - natural frequency $\omega = \sqrt{\dfrac{k}{m}}$
        - period $T = \dfrac{2\pi}{\omega}$
      - Graph: oscillating wave with constant amplitude
    - Underdamped spring
      - $\gamma > 0$
      - General solution: $x(t) = e^{-\gamma t/2m} [c_{1} \cos(\omega t) + c_{2}\sin(\omega t)]$
      - Phase-amplitude form: $x(t) = Ae^{-\gamma t/2m}\cos(\omega t - \varphi)$
        - amplitude $A = \sqrt{c_{1}^{2}+c_{2}^{2}}$
        - phase $\varphi = \arctan(c_{2}/c_{1})$
        - natural frequency $\omega = \sqrt{\dfrac{k}{m}}$
        - period $T = \dfrac{2\pi}{\omega}$
      - Graph: oscillating wave with exponentially decreasing amplitude

#### Forced oscillation

- Has external force on the system: $F_{\mathrm{ext}}(t) \not= 0$
- Investigate a special case of oscillating external force $F_{\mathrm{ext}}(t) \equiv F_{0}\cos(\Omega t)$
- Non-homogeneous ODE: $\boxed{mx\'\' + \gamma x\' + kx = F_{0}\cos(\Omega t)} \ (m, \gamma, k \ge 0)$
  - No damping, no resonance
    - $\gamma = 0, \Omega \not= \omega_{0} = \sqrt{\dfrac{k}{m}}$
    - General solution: $x(t) = \left( c_{1} + \dfrac{F_{0}}{m(\omega_{0}^{2} - \Omega_{0}^{2})} \right) \cos(\omega_{0}t) + c_{2}\sin(\omega_{0} t)$
    - Graph: modulated wave + beats pattern
  - No damping, with resonance
    - $\gamma = 0, \Omega = \omega_{0} = \sqrt{\dfrac{k}{m}}$
    - General solution: $x(t) = c_{1}\cos(\omega_{0}t) + \left( c_{2} + \dfrac{F_{0}}{2\omega_{0}m}t \right) \sin(\omega_{0}t)$
    - Graph: oscillating wave with linearly increasing amplitude

## Systems of Differential Equations

### Introduction to linear algebra

#### Linear independence

- Linear combination - $\mathbf{x} = c_1\mathbf{x}_1 + c_2\mathbf{x}_2 + ... + c_n\mathbf{x}_n$
- Linearly dependent - vectors satisfy the equation $c_1\mathbf{x}_1 + c_2\mathbf{x}_2 + ... + c_n\mathbf{x}_n = \mathbf{0}$ such that the constants are not all zero
- Linearly independent - vectors that are not linearly dependent
- Wronskian - $W[\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n] = \det([\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n]) = \det(X)$
- Checking linear independence
  - If $W[\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n] \not= 0$
    - then they are linearly independent

#### Matrix inversion

- Inverse of a square matrix - $A^{-1}$ thats satisfies $AA^{-1} = A^{-1}A = I_n$
- Finding matrix inverse
  - $A = \begin{bmatrix} a & b \cr c & d \end{bmatrix}, A^{-1} = \dfrac{1}{ad-bc} \begin{bmatrix} d & -b \cr -c & a \end{bmatrix}$
- Solving systems of equations using inverse
  - $A\mathbf{x} = \mathbf{b}$
  - $\mathbf{x} = A^{-1}\mathbf{b}$

#### Matrix determinant

- Finding matrix determinant
  - $A = \begin{bmatrix} a & b \cr c & d \end{bmatrix}, \det(A) = ad-bc$
  - $A = \begin{bmatrix} a & b & c \cr d & e & f \cr g & h & i \end{bmatrix}, \det(A) = a\begin{vmatrix} e & f \cr h & i \end{vmatrix} - b\begin{vmatrix} d & f \cr g & i \end{vmatrix} + c\begin{vmatrix} d & e \cr g & h \end{vmatrix}$
- Singular matrix - matrix with a determinant of 0
- Equivalent statements
  - $\det(A)=0$
  - $A$ is singular
  - $A^{-1}$ does not exist
  - $A\mathbf{x} = \mathbf{b}$ has either no solution or infinitely many solutions
  - columns of $A$ are linearly dependent
  - rows of $A$ are linearly dependent

#### Eigenvalues and eigenvectors of matrix

- Eigenvector - vector $\mathbf{v}$ such that $A\mathbf{v} = \lambda\mathbf{v}$ for square matrix $A$
  - $\mathbf{0}$ is not an eigenvector by convention
- Eigenvalue - constant $\lambda$ corresponding to the eigenvector $\mathbf{v}$
- Finding eigenvalues and eigenvectors
  1. Solve for $\lambda$ in $\det(A-\lambda I) = 0$
  2. Substitute $\lambda$ into $A\mathbf{v} = \lambda\mathbf{v}$ to find relationship between components of eigenvectors

### Systems of differential equations

#### Rewriting ODEs into systems of 1st order ODEs

1. Define $n$ auxiliary variables $y_1$, ..., $y_n$ for $n$th order ODE
   1. Let $y_1$ be the original function in the ODE
   2. Let $y_2 = y_1\'$
   3. ...
   4. Let $y_n = y_{n-1}\'$
2. Rearrange the ODE to isolate the highest order derivative, and write it in terms of the auxiliary variables.
3. Write a system of ODEs with derivatives of auxiliary variables on the left hand side and their expression on the right hand side in terms of the auxiliary variables
   1. $y_1\' = y_2$ (by definition)
   2. ...
   3. $y_{n-1}\' = y_{n}$ (by definition)
   4. $y_{n}\' =$ highest order derivative in step 2

#### Linear system of ODEs

- $\begin{cases} y_1\' = a_{11}y_1 + a_{12}y_2 + ... + a_{1n}y_{n} + b_1 \cr y_2\' = a_{21}y_1 + a_{22}y_2 + ... + a_{2n}y_{n} + b_2 \cr \vdots \cr y_n\' = a_{n1}y_1 + a_{n2}y_2 + ... + a_{nn}y_{n} + b_n \end{cases} \Rightarrow \boxed{\mathbf{y}\' = A\mathbf{y} + \mathbf{b}}$
  - where $\mathbf{y} = \begin{bmatrix} y_1 \cr y_2 \cr \vdots \cr y_n \end{bmatrix}, \mathbf{y}\' = \begin{bmatrix} y_1\' \cr y_2\' \cr \vdots \cr y_n\' \end{bmatrix}, \mathbf{b} = \begin{bmatrix} b_1 \cr b_2 \cr \vdots \cr b_n \end{bmatrix}, A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \cr a_{21} & a_{22} & \cdots & a_{2n} \cr \vdots & \vdots & \ddots & \vdots \cr a_{n1} & a_{n2} & \cdots & a_{nn} \end{bmatrix}$
- Homogeneous - $\mathbf{b} = \mathbf{0}$
- Nonhomogeneous - $\mathbf{b} \not= \mathbf{0}$
- Superposition principle
  - If the vectors $\mathbf{x}_1, \mathbf{x}_2, ..., \mathbf{x}_n$ are linearly independent solutions of the homogeneous system $\mathbf{x}\' = P\mathbf{x}$
    - then the general solution $\mathbf{x}$ is the linear combination of them <br/> $\mathbf{x} = c_1\mathbf{x}_1 + c_2\mathbf{x}_2 + ... + c_n\mathbf{x}_n$

#### Solving homogeneous constant-coefficient systems of ODEs

- [x] ODE system
- [x] 1st order
- [x] Linear
- [x] Constant coefficient
- [x] Homogeneous

1. Write the system of ODEs in the form of $\mathbf{x}\' = P\mathbf{x}$
2. For $P\mathbf{v} = \lambda\mathbf{v}$, find the eigenvalues of $\lambda$ by solving $\det(P-\lambda I_n) = 0$
3. For $P\mathbf{v} = \lambda\mathbf{v}$, find the eigenvectors of by substitution of $\lambda$
4. Write the general solution
   - $\le n$ distinct $\lambda\in\R$; $n$ distinct real $\mathbf{v}$
     - General solution: $\mathbf{x} = c_1\mathbf{v}_1 e^{\lambda_1 t} + ... + c_n\mathbf{v}_n e^{\lambda_n t}$
   - $\le n$ distinct $\lambda\in\Complex$; $n$ distinct complex $\mathbf{v}$
     - Known: $\mathbf{x}_1 = c_1\mathbf{v}_1 e^{\lambda_1 t} = \mathrm{Re}(\mathbf{x}_1) + i\mathrm{Im}(\mathbf{x}_1)$
     - General solution: $\mathbf{x} = c_1 \mathrm{Re}(\mathbf{x}_1) + c_2 \mathrm{Im}(\mathbf{x}_1)$
   - $\le n$ distinct $\lambda$; $<n$ distinct $\mathbf{v}$
     - General solution: $\mathbf{x} = c_1 \mathbf{v} e^{\lambda t} + c_2(\mathbf{v}te^{\lambda t} + \vec{\eta}e^{\lambda t})$
       - Find $\vec{\eta}$ (relationship between its components) by substituting into the ODE

#### Solving Euler systems

- [x] Linear
- [x] Non-constant coefficient (of special type)
- [x] Homogeneous
- [x] Euler system

1. Write the system of ODEs in the form of $\mathbf{x}\' = P\mathbf{x}$
2. For $P\mathbf{v} = \lambda\mathbf{v}$, find the eigenvalues of $\lambda$ by solving $\det(P-\lambda I_n) = 0$
3. For $P\mathbf{v} = \lambda\mathbf{v}$, find the eigenvectors of by substitution of $\lambda$
4. Write the general solution
   - $\le n$ distinct $\lambda\in\R$; $n$ distinct real $\mathbf{v}$
     - General solution: $\mathbf{x} = c_1\mathbf{v}_1 t^{\lambda_1} + ... + c_n\mathbf{v}_n t^{\lambda_n}$
   - Other conditions are not discussed

## Laplace Transform

### Laplace transform concepts

- Laplace transform - $\mathcal{L}[f(t)] = F(s) = \displaystyle\int_{0}^{\infin} e^{-st}f(t) \ dt$
- Heaviside function (unit step function)
  - $u_c(t) = u(t-c) = \begin{cases} 0 & t < c \cr 1 & t \ge c \end{cases}$

### Properties of Laplace transform

- Laplace transform is linear
  - $\mathcal{L}[c_{1}f(t)+c_{2}g(t)] = c_{1}\mathcal{L}[f(t)] + c_{2}\mathcal{L}[g(t)]$
- Laplace transforms of derivatives incorporate initial conditions
  - $\mathcal{L}[f\'(t)] = sF(s) - f(0)$
  - $\mathcal{L}[f\'\'(t)] = s^2F(s)-sf(0)-f\'(0)$
  - $\mathcal{L}[f^{(n)}(t)] = s^nF(s)-s^{n-1}f(0) - s^{n-2}f^{(1)}(0) - ... - f^{(n-1)}(0)$
- Heaviside function has a simple Laplace transforms
  - $\mathcal{L}[u_c(t)] = \dfrac{e^{-sc}}{s}$

### Translation theorems

- Time domain translation
  - $\mathcal{L}[f(t-c)u_{c}(t)] = e^{-sc}\mathcal{L}[f(t)]$
  - $\mathcal{L}^{-1}[e^{-sc}\mathcal{L}[f(t)]] = f(t-c)u_c(t)$
- Laplace domain translation
  - $\mathcal{L}[e^{ct}f(t)] = F(s-c)$
  - $\mathcal{L}^{-1}[F(s-c)] = e^{ct}f(t)$

### Solving ODEs with Laplace transform

1. Time domain: difficult ODE
   - Laplace transform ($t \to s$)
2. Laplace domain: easy algebra problem
   - Solve the algebra problem
3. Laplace domain: solution to algebra problem
   - Inverse Laplace transform ($s \to t$)
4. Time domain: solution of difficult ODE
   - Problem solved

### Laplace transform table

|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|
|-:|:---|-:|:-|
|$1$|$\dfrac{1}{s}$|$e^{at}$|$\dfrac{1}{s-a}$|
|$t^{n}$|$\dfrac{n!}{s^{n+1}}$|$\sqrt{t}$|$\dfrac{\sqrt{\pi}}{2s^{3/2}}$|
|$\sin(at)$|$\dfrac{a}{s^{2}+a^{2}}$|$t\sin(at)$|$\dfrac{2as}{(s^{2}+a^{2})^{2}}$|
|$\cos(at)$|$\dfrac{s}{s^{2}+a^{2}}$|$t\cos(at)$|$\dfrac{s^{2}-a^{2}}{(s^{2}+a^{2})^{2}}$|
|$\sin(at)-at\cos(at)$|$\dfrac{2a^{3}}{(s^{2}+a^{2})^{2}}$|$\cos(at)-at\sin(at)$|$\dfrac{s(s^{2}-a^{2})}{(s^{2}+a^{2})^{2}}$|
|$\sin(at)+at\cos(at)$|$\dfrac{2as^{2}}{(s^{2}+a^{2})^{2}}$|$\cos(at)+at\sin(at)$|$\dfrac{s(s^{2}+3a^{2})}{(s^{2}+a^{2})^{2}}$|
|$\sinh(at)$|$\dfrac{a}{s^{2}-a^{2}}$|$\sin(at+b)$|$\dfrac{s\sin(b)+a\cos(b)}{s^2+a^2}$|
|$\cosh(at)$|$\dfrac{s}{s^{2}-a^{2}}$|$\cos(at+b)$|$\dfrac{s\cos(b)-a\sin(b)}{s^2+a^2}$|
|$e^{at}\sin(bt)$|$\dfrac{b}{(s-a)^2+b^2}$|$e^{at}\sinh(bt)$|$\dfrac{b}{(s-a)^2-b^2}$|
|$e^{at}\cos(bt)$|$\dfrac{s-a}{(s-a)^2+b^2}$|$e^{at}\cosh(bt)$|$\dfrac{s-a}{(s-a)^2-b^2}$|
|$u_{c}(t)$|$\dfrac{e^{-sc}}{s}$|
