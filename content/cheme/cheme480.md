---
title: "CHEM E 480 Process Dynamics and Control"
date: 2023-01-19T00:00:00-08:00
---

## Intro to Process Dynamics and Control

- ### Definitions

  - **Process** - conversion of feed materials to products using chemical and physical operations
    - Continuous, batch, semi-batch
  - **Process dynamics** - unsteady-state/transient process behavior
    - Start-ups, shutdowns, process disturbances, planned transitions
  - **Process control** - maintain a process at desired operating conditions
    - Utilize information flow
    - Impacts safety, environment, quality, economics
    - **Manual control** - control strategy implemented by a person
    - **Automatic control** - control strategy automated by computers
  - Types of variables
    - **Set point** - desired nominal value of controlled variable
    - **Controlled variable** - variable being regulated and maintained (to be controlled) at set point
    - **Manipulated variable** - variable that can be adjusted
    - **Disturbance variable** - variable that perturbs the system, changes controlled variable, but cannot be directly tuned

- ### Classification of control strategies

  - **Feedback control** - controlled variable is measured to adjust manipulated variable (disturbance variable not measured)
    - **Negative feedback** - controller forces controlled variable toward set point
    - **Positive feedback** - controller forces controlled variable farther away from set point
    - :heavy_plus_sign: Correction occurs regardless of source of disturbance
    - :heavy_plus_sign: Reduces sensitivity of controlled variable to unmeasured disturbance and process changes
    - :heavy_minus_sign: Correction only happens after controlled variable deviates set point (disturbance has occurred)
  - **Feedforward control** - disturbance variable measured to adjust manipulated variable (controlled variable not measured)
    - :heavy_plus_sign: Correction happens before controlled variable deviates set point
    - :heavy_minus_sign: Disturbance variable must be measured or accurately estimated
    - :heavy_minus_sign: Do not account for unmeasured disturbances
    - :heavy_minus_sign: Process model is required
  - Challenges
    - Systems are often nonlinear
    - Time delays are common at scale
    - Real systems are complex and interconnected
  - Iterative design
    - Formulate control objective
    - Identify variables
    - Model process
    - Implement control strategy
    - Tune controller

- ### Types of control processes

  - **Single-input/single-output (SISO)** - one manipulated variables (input) and one controlled variables (output)
    - :heavy_plus_sign: Easy to model and implement
    - :heavy_minus_sign: Less control
  - **Multiple-input/multiple-output (MIMO)** - multiple manipulated variables (input) and multiple controlled variables (output)
    - :heavy_plus_sign: Better control
    - :heavy_minus_sign: Hard to model and implement
  - Balance robustness to disturbance  and complexity of model

- ### Hierarchy of control activities

  1. Measurement and actuation (< 1 s)
  2. Safety and environmental/equipment protection (< 1 s)
  3. Regulatory control (sec - min)
  4. Multivariable and constraint control (sec - min)
  5. Real-time optimization (hr - day)
  6. Planning and scheduling (day - month)

## Theoretical Models of Chemical Processes

- ### **Dynamic models**

  - **Theoretical models** - developed using principles of physics, chemistry, and biology
    - :heavy_plus_sign: Physical insight into process behavior
    - :heavy_plus_sign: Applicable over wide ranges of conditions
    - :heavy_minus_sign: Expensive and time-consuming to develop
    - :heavy_minus_sign: Model parameter not readily available
  - **Empirical models** - obtained by fitting experimental data
    - :heavy_plus_sign: Easy to develop and use
    - :heavy_minus_sign: Do not extrapolate to conditions beyond range
  - **Semi-empirical models** - numerical values of 1(+) parameters in a theoretical model are calculated from experimental data
    - :heavy_plus_sign: Incorporate theoretical knowledge
    - :heavy_plus_sign: Extrapolate over wider range of operating conditions
    - :heavy_plus_sign: Requires less developmental effort
  - Improve process understanding
  - Train plant operating personnel
  - Develop control strategies for new processes
  - Optimize process operating conditions

- ### General modeling principles

  - Simplifying assumptions balances model complexity and accuracy
  - Higher-order ODEs approximated by first-order processes have solutions with **exponential** and **oscillatory** response
    - Conservation of mass
    - Conservation of energy
    - Rate expressions
    - Equilibrium expressions
  - Normalized response - $x_N(t) = \dfrac{x(t) - x(0)}{x(\infty) - x(0)}$

## Laplace Transforms

- ### Definitions

  - Laplace transform - $\mathcal{L}[f(t)] = F(s) = \displaystyle\int_{0}^{\infin} e^{-st}f(t) \ dt$
  - Heaviside function (unit step function centered at $c$)
    - $u_c(t) = u(t-c) = \begin{cases} 0 & t < c \cr 1 & t \ge c \end{cases}$
  - Rectangular pulse function
    - $f(t) = \begin{cases} 0 & t<0 \\\ h & t \in [0, t_w] \\\ 0 & t \ge t_w \end{cases}$
  - Impulse (Dirac delta) function

- ### Properties of Laplace transform

  - Laplace transform is linear
    - $\mathcal{L}[c_{1}f(t)+c_{2}g(t)] = c_{1}\mathcal{L}[f(t)] + c_{2}\mathcal{L}[g(t)]$
  - Laplace transforms of derivatives incorporate initial conditions
    - $\mathcal{L}[f\'(t)] = sF(s) - f(0)$
    - $\mathcal{L}[f\'\'(t)] = s^2F(s)-sf(0)-f\'(0)$
    - $\mathcal{L}[f^{(n)}(t)] = s^nF(s)-s^{n-1}f(0) - s^{n-2}f^{(1)}(0) - ... - f^{(n-1)}(0)$
  - Heaviside function has a simple Laplace transforms
    - $\mathcal{L}[u_c(t)] = \dfrac{e^{-sc}}{s}$

- ### Translation theorems

  - Time domain translation
    - $\mathcal{L}[f(t-c)u_{c}(t)] = e^{-sc}\mathcal{L}[f(t)]$
    - $\mathcal{L}^{-1}[e^{-sc}\mathcal{L}[f(t)]] = f(t-c)u_c(t)$
  - Laplace domain translation
    - $\mathcal{L}[e^{ct}f(t)] = F(s-c)$
    - $\mathcal{L}^{-1}[F(s-c)] = e^{ct}f(t)$

- ### Solving ODEs with Laplace transform

  1. Time domain: difficult ODE
     - Laplace transform ($t \to s$)
  2. Laplace domain: easy algebra problem
     - Solve the algebra problem
  3. Laplace domain: solution to algebra problem
     - Inverse Laplace transform ($s \to t$)
  4. Time domain: solution of difficult ODE
     - Problem solved

- ### Partial fraction decomposition

  - Heaviside expansion
    - $Y(s) = \dfrac{N(s)}{D(s)} = \dfrac{N(s)}{\displaystyle \prod_{i=1}^n (s+b_i)} = \displaystyle \sum_{i=1}^n \dfrac{\alpha_i}{s + b_i}$

### Fundamental signals

|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|
|-:|:---|-:|:-|
|$1$|$\dfrac{1}{s}$|$\delta(t)$|$1$
|$S(t) \equiv u_0(t)$|$\dfrac{1}{s}$|$S(t-c) \equiv u_{c}(t)$|$\dfrac{e^{-sc}}{s}$|
|$e^{-at}$|$\dfrac{1}{s+a}$|$t$|$\dfrac{1}{s^2}$|
|$\dfrac{1}{a}e^{-t/a}$|$\dfrac{1}{as+1}$|$t^{n}$|$\dfrac{n!}{s^{n+1}}$|
|$1 - e^{t/a}$|$\dfrac{1}{s(as+1)}$|$\sqrt{t}$|$\dfrac{\sqrt{\pi}}{2s^{3/2}}$|
|$e^{-at+b}$|$\dfrac{e^b}{a+s}$|$te^{-at}$|$\dfrac{1}{(a+s)^2}$
|||$t^ne^{-at}$|$\dfrac{n!}{(a+s)^{n+1}}$|

### Oscillatory signals

|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|
|-:|:---|-:|:-|
|$\sin(at)$|$\dfrac{a}{s^{2}+a^{2}}$|$t\sin(at)$|$\dfrac{2as}{(s^{2}+a^{2})^{2}}$|
|$\cos(at)$|$\dfrac{s}{s^{2}+a^{2}}$|$t\cos(at)$|$\dfrac{s^{2}-a^{2}}{(s^{2}+a^{2})^{2}}$|
|$\sin(at)-at\cos(at)$|$\dfrac{2a^{3}}{(s^{2}+a^{2})^{2}}$|$\cos(at)-at\sin(at)$|$\dfrac{s(s^{2}-a^{2})}{(s^{2}+a^{2})^{2}}$|
|$\sin(at)+at\cos(at)$|$\dfrac{2as^{2}}{(s^{2}+a^{2})^{2}}$|$\cos(at)+at\sin(at)$|$\dfrac{s(s^{2}+3a^{2})}{(s^{2}+a^{2})^{2}}$|
|$\sinh(at)$|$\dfrac{a}{s^{2}-a^{2}}$|$\sin(at+b)$|$\dfrac{s\sin(b)+a\cos(b)}{s^2+a^2}$|
|$\cosh(at)$|$\dfrac{s}{s^{2}-a^{2}}$|$\cos(at+b)$|$\dfrac{s\cos(b)-a\sin(b)}{s^2+a^2}$|
|$e^{at}\sin(bt)$|$\dfrac{b}{(s-a)^2+b^2}$|$e^{at}\sinh(bt)$|$\dfrac{b}{(s-a)^2-b^2}$|
|$e^{at}\cos(bt)$|$\dfrac{s-a}{(s-a)^2+b^2}$|$e^{at}\cosh(bt)$|$\dfrac{s-a}{(s-a)^2-b^2}$|

### Convenient inverse signals

|Inverse L.T. <br/> $f(t)$|Laplace Transform <br/> $F(s)$|Comment|
|-:|:---|:-|
|$\dfrac{t^{n-1} e^{-b t}}{(n-1) !}(n>0)$|$\dfrac{1}{(s+b)^{n}}$|
|$\dfrac{1}{\tau^{n}(n-1) !} t^{n-1} e^{-t / \tau}$|$\dfrac{1}{(\tau s+1)^{n}}$|
|$\dfrac{1}{b_{1}-b_{2}}\left(e^{-b_{2} t}-e^{-b_{1} t}\right)$|$\dfrac{1}{\left(s+b_{1}\right)\left(s+b_{2}\right)}$|
|$\dfrac{1}{\tau_{1}-\tau_{2}}\left(e^{-t / \tau_{1}}-e^{-t / \tau_{2}}\right)$|$\dfrac{1}{\left(\tau_{1} s+1\right)\left(\tau_{2} s+1\right)}$|
|$\dfrac{b_{3}-b_{1}}{b_{2}-b_{1}} e^{-b_{1} t}+\dfrac{b_{3}-b_{2}}{b_{1}-b_{2}} e^{-b_{2} t}$|$\dfrac{s+b_{3}}{\left(s+b_{1}\right)\left(s+b_{2}\right)}$|
|$\dfrac{1}{\tau_{1}} \dfrac{\tau_{1}-\tau_{3}}{\tau_{1}-\tau_{2}} e^{-t / \tau_{1}}+\dfrac{1}{\tau_{2}} \dfrac{\tau_{2}-\tau_{3}}{\tau_{2}-\tau_{1}} e^{-t / \tau_{2}}$|$\dfrac{\tau_{3} s+1}{\left(\tau_{1} s+1\right)\left(\tau_{2} s+1\right)}$|
|$\dfrac{1}{\tau \sqrt{1-\zeta^{2}}} e^{-\zeta t / \tau} \sin \left(\sqrt{1-\zeta^{2}} t / \tau\right)$|$\dfrac{1}{\tau^{2} s^{2}+2 \zeta \tau s+1}$|$(0 \leq\vert\zeta\vert<1)$|
|$1+\dfrac{1}{\tau_{2}-\tau_{1}}\left(\tau_{1} e^{-t / \tau_{1}}-\tau_{2} e^{-t / \tau_{2}}\right)$|$\dfrac{1}{s\left(\tau_{1} s+1\right)\left(\tau_{2} s+1\right)}$|$(\tau_1 \not= \tau_2)$|
|$1-\dfrac{1}{\sqrt{1-\zeta^{2}}} e^{-\zeta t / \tau} \sin \left[\sqrt{1-\zeta^{2}} t / \tau+\psi\right]$|$\dfrac{1}{s\left(\tau^{2} s^{2}+2 \zeta \tau s+1\right)}$|$\footnotesize\begin{aligned}\psi=\tan ^{-1} \dfrac{\sqrt{1-\zeta^{2}}}{\zeta}\end{aligned} \newline (0 \leq\vert\zeta\vert<1)$|
|$\begin{aligned}1-e^{-\zeta t / \tau}\left[\cos \left(\sqrt{1-\zeta^{2}} t / \tau\right)+\dfrac{\zeta}{\sqrt{1-\zeta^{2}}} \sin \left(\sqrt{1-\zeta^{2}} t / \tau\right)\right]\end{aligned}$|$\dfrac{1}{s\left(\tau^{2} s^{2}+2 \zeta \tau s+1\right)}$|$(0 \leq\vert\zeta\vert<1)$|
|$1+\dfrac{\tau_{3}-\tau_{1}}{\tau_{1}-\tau_{2}} e^{-t / \tau_{1}}+\dfrac{\tau_{3}-\tau_{2}}{\tau_{2}-\tau_{1}} e^{-t / \tau_{2}}$|$\dfrac{\tau_{3} s+1}{s\left(\tau_{1} s+1\right)\left(\tau_{2} s+1\right)}$|$(\tau_1 \not= \tau_2)$|

<!-- ★ -->