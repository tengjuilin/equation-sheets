---
title: "CHEM E 457 Principles of Molecular Engineering"
date: 2022-04-24T00:00:00-08:00
---

## Counting and Probability

### Counting

|Description|Equations|
|-:|:-|
|Total possible events if each event $E_i$ can occur in $n_i$ ways|$\prod n_i$|
|**Permutation** of $n$ elements taken $r$ at a time|$P(n, r) = \dfrac{n!}{(n-r)!}$|
|**Distinguishable permutations** of $n$ objects, with $n_i$ are alike of one kind|$\dfrac{n!}{n_1! n_2! \cdots n_k!}$|
|**Combination** of $n$ elements taken $r$ at a time|$\displaystyle C(n, r) = \binom{n}{r} = \dfrac{n!}{r!(n-r)!}$|
|Stirling's approximation|$x! \approx \left(\dfrac{x}{e}\right)^x$|
|Stirling's approximation|$\ln(x!) = x \ln(x) - x$|

### Probability

|Description|Equations|
|-:|:-|
|Probability|$\mathbf{P}(A) = \dfrac{n_A}{N}$|
|Addition rule of mutually exclusive outcomes|$\mathbf{P}\left(\bigcup A_i\right) = \sum \mathbf{P}(A_i)$|
|Multiplication rule of independent outcomes|$\mathbf{P}\left(\bigcap A_i\right) = \prod \mathbf{P}(A_i)$|
|General addition rule|$\mathbf{P}(A\cup B) = \mathbf{P}(A) + \mathbf{P}(B) - \mathbf{P}(A\cap B)$|
|Conditional probability|$\mathbf{P}(A\vert B) \equiv \dfrac{\mathbf{P}(A\cap B)}{\mathbf{P}(B)}$|
|Bayes' rule|$\mathbf{P}(A\vert B) = \dfrac{\mathbf{P}(A) \mathbf{P}(B\vert A)}{\mathbf{P}(B)}$|
|Total probability theorem|$\mathbf{P}(B) = \mathbf{P}(A)\mathbf{P}(B\vert A) + \mathbf{P}(A^c)\mathbf{P}(B\vert A^c)$|
|Degree of correlation|$g = \dfrac{\mathbf{P}(B\vert A)}{\mathbf{P}(B)} = \dfrac{\mathbf{P}(A \cap B)}{\mathbf{P}(A)\mathbf{P}(B)}$|

### Continuous probability distribution

|Description|Equations|
|-:|:-|
|Normalization condition of probability distribution function|$\displaystyle\int_a^b P(x) dx = 1$|
|Binomial distribution|$P(n, N) = \dfrac{N!}{n!(N-n)!}p^n (1-p)^{N-n}$|
|Multinomial distribution|$P(n_1, n_2, ..., n_t, N) = \dfrac{N!}{\prod n_i!}\prod p_i^{n_i}$|
|Average|$\langle x \rangle = \displaystyle\int_a^b xP(x) dx$|
|Average of a function|$\langle f(x) \rangle = \displaystyle\int_a^b f(x)P(x) dx$|
|$n$th moment|$\langle x^n \rangle = \displaystyle\int_a^b x^nP(x) dx$|
|Variance|$\sigma^2 = \langle x^2 \rangle - \langle x \rangle^2$|

## Extremum Principles Predicts Equilibria

|Physical Description|Math Description|Equations|
|-:|:-|:-|
|Equilibrium|Critical point|$f'(x) = 0$|
|Stable equilibrium|Minimum|$f'(x) = 0, f''(x) > 0$|
|Unstable equilibrium|Maximum|$f'(x) = 0, f''(x) < 0$|
|Metastable equilibrium|Local minimum|$f'(x) = 0, f''(x) > 0$ in some $dx$|
|Neutral equilibrium|Constant|$f'(x) = 0$ for all $x$|

- Extremum principles
  - Minimization of energy
  - Maximization of entropy (multiplicity)

|Description|Equations|
|-:|:-|
|**Method of Lagrange multiplier** <br/> Finding extremum of objective function $f(\mathbf{x})$ subjected to constraint $g(\mathbf{x})$|$\nabla f(\mathbf{x}) = \lambda \nabla g(\mathbf{x})$|

## Entropy and Boltzmann Law

- Ground state - state of lowest energy
- Excited state - states of higher energy
- Microstate - microscopic configuration
- Macrostate - collection of microstate

### General applications

|Description|Equations|
|-:|:-|
|Entropy in terms of multiplicity|$S = k\ln(W)$|
|Entropy in terms of probability|$S = -k \sum p_i \ln (p_i)$|
|Probability of a microstate <br/> ★ No constraint on observation <br/> ★ Maximized entropy|$p_i = \dfrac{1}{t}$|
|**Boltzmann distribution law** <br/> Probability of a microstate <br/> ★ With constraint on observation <br/> ★ Maximized entropy|$p_i = \dfrac{e^{-\beta \varepsilon_i}}{\sum e^{-\beta \varepsilon_i}} = \dfrac{e^{-\beta \varepsilon_i}}{q}$|
|Partition function|$q = \sum e^{-\beta \varepsilon_i}$|
|Average observation|$\langle \varepsilon \rangle = \sum \varepsilon_i p_i$|

### Molecular distributions

|Description|Boltzmann Distribution Law|Partition Function|
|-:|:-|:-|
|System with energy levels|$p_i = \dfrac{\exp(-E_i/kT)}{Q}$|$Q = \sum \exp\left(-E_i/kT\right)$|
|System with energy differences|$p_i = \dfrac{\exp(-(E_i-E_j)/kT)}{Q}$|$Q = \sum\exp\left(-(E_i-E_j)/kT\right)$|
|System with degenerate energy levels|$p_i = \dfrac{W(E_l) \exp(-E_l/kT)}{Q}$|$Q = \sum W(E_l) \exp(-E_l / kT)$|

|Description|Equations|
|-:|:-|
|Thermodynamic beta|$\beta = \dfrac{1}{kT}$|
|Relative populations of particles in energy level $i$ and $j$ at equilibrium|$\dfrac{p_i}{p_j} = \exp\left(-\dfrac{E_i - E_j}{kT}\right)$|
|Partition function of subsystem of independent distinguishable particles (solid)|$Q = \prod_i^N q_i = q^N$|
|Partition function of subsystem of independent indistinguishable particles (gas)|$Q = \dfrac{q^N}{N!}$|
|Internal energy|$U = kT^2 \left(\dfrac{\partial\ln Q}{\partial T}\right)_{V, N}$|
|Average particle energy|$\langle \varepsilon \rangle = \dfrac{U}{N} = \dfrac{kT^2}{N} \left(\dfrac{\partial\ln Q}{\partial T}\right)_{V, N}$|
|Entropy|$S = k \ln Q + \dfrac{U}{T}$|
|Helmholtz free energy|$F = U - TS = -kT \ln Q$|
|Chemical potential|$\mu = \left(\dfrac{\partial F}{\partial N}\right)\_{T, V} = -kT\left(\dfrac{\partial\ln Q}{\partial N}\right)\_{T, V}$|
|Pressure|$p = -\left(\dfrac{\partial F}{\partial V}\right)\_{T, N} = kT \left(\dfrac{\partial\ln Q}{\partial N}\right)\_{T, N}$|


### Ensembles

- controlled set of variables
- collection of all the possible microstates

|Description|Equations|
|-:|:-|
|Canonical ensemble|$(T, V, N)$|
|Microcanonical ensemble|$(U, V, N)$|
|Isobaric-isothermal ensemble|$(T, P, N)$|
|Grand canonical ensemble|$(T, V, \mu)$|

<!-- ★ -->