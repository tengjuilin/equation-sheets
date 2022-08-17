---
title: "CHEM E 457 Principles of Molecular Engineering"
date: 2022-06-08T00:00:00-08:00
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

## Ch 13 Chemical Equilibrium

### Multicomponent reactions

|Description|Equations|
|-:|:-|
|Multicomponent gas phase reaction <br/> ★ No intermolecular interactions|$\ce{aA + bB -> cC + dD}$|
|Difference in ground state energy|$\Delta \varepsilon_0 = d \varepsilon_{0D} + c \varepsilon_{0C} - b \varepsilon_{0B} - a \varepsilon_{0A}$|
|Difference in Dissociation energy|$\Delta D = d D_D + c D_C - b D_B - a D_A$|
|Dissociation energy|$D = - \varepsilon_0 \\\ \Delta D = -\Delta \varepsilon_0$|
|Equilibrium constant|$K = \dfrac{N_C^c N_D^d}{N_A^a N_B^b} = \dfrac{q_C^c q_D^d}{q_A^a q_B^b} \exp\left(\dfrac{\Delta D}{kT}\right)$|
|Pressure-based equilibrium constant|$K_p = \dfrac{p_C^c p_D^d}{p_A^a p_B^b} = \left(\dfrac{kT}{V}\right)^{(c+d) - (a+b)} \dfrac{q_C^c q_D^d}{q_A^a q_B^b} \exp\left(\dfrac{\Delta D}{kT}\right)$|
|Chemical potential|$\mu = kT \ln\left(\dfrac{p}{p_{int}^\circ}\right) = \mu^\circ + kT \ln p$|
|Internal pressure|$p_{int}^\circ = q_0' kT$|

### $T, P$ dependence of equilibrium

|Description|Equations|
|-:|:-|
||$\ln K_p = -\dfrac{\Delta\mu^\circ}{kT}$|
|**vant's Hoff equation** <br/> ★ $\Delta h^\circ \not =\Delta h^\circ(T)$|$\dfrac{\partial (\ln K_p)}{\partial T} = \dfrac{\Delta h^\circ}{kT^2}$|
|vant's Hoff plot <br/> ★ $\Delta h^\circ \not =\Delta h^\circ(T)$|$\dfrac{\partial (\ln K_p)}{\partial (1/T)} = - \dfrac{\Delta h^\circ}{k}$|
|vant's Hoff equation extrapolation <br/> ★ $\Delta h^\circ \not =\Delta h^\circ(T)$|$\ln \left(\dfrac{K_{p2}}{K_{p1}}\right)=-\dfrac{\Delta h^{\circ }}{k}\left(\dfrac{1}{T_2}-\dfrac{1}{T_1}\right)$|
|Gibbs-Helmholtz equation|$\dfrac{\partial }{\partial T}\left(\dfrac{G}{T}\right)=-\dfrac{H}{T^2}$|
|Gibbs-Helmholtz equation|$\dfrac{\partial }{\partial T}\left(\dfrac{F}{T}\right)=-\dfrac{U}{T^2}$|
|Pressure dependence of equilibrium constant|$\dfrac{\partial (\ln K)}{\partial p} = -\dfrac{\Delta v^\circ}{kT}$|

## Ch 14 Physical Equilibrium

|Description|Equations|
|-:|:-|
|Equilibrium condition|$\mu_{\mathrm{vapor}} = \mu_{\mathrm{condensed}}$|
|Chemical potential of vapor|$\mu_{\mathrm{vapor}} = kT\ln \left(\dfrac{p}{p^{\circ}_{int}}\right)$|
|Entropy of condensed phase|$\Delta S_{\mathrm{condensed}} = 0$|
|Internal energy of condensed phase|$\Delta U_{\mathrm{condensed}} = \frac{1}{2} Nzw_{AA}$|
|Free energy of condensed phase|$\Delta F_{\mathrm{condensed}} = \frac{1}{2} Nzw_{AA}$|
|Chemical potential of condensed phase|$\mu_{\mathrm{condensed}} = \left(\dfrac{\partial F}{\partial N}\right)_{T,V} = \dfrac{1}{2}zw_{AA}$|

|Description|Equations|
|-:|:-|
|Equilibrium vapor pressure|$p = p^{\circ}\_{int} \exp \left(\dfrac{zw_{AA}}{2kT}\right)$|
|Clausius-Clapyeron equation|$\ln \left(\dfrac{p_2^{\text{sat}}}{p_1^{\text{sat}}}\right)=-\dfrac{\Delta h}{R}\left(\dfrac{1}{T_2}-\dfrac{1}{T_1}\right)$|
|Enthalpy of vaporization|$\Delta h_{\mathrm{vap}} = - \frac{1}{2}zw_{AA}$|
|Internal energy to close a cavity|$\Delta U = \frac{1}{2}zw_{AA}$|
|Internal energy to open a cavity|$\Delta U = - \frac{1}{2}zw_{AA}$|
|Surface tension|$\sigma = -\dfrac{w_{AA}}{2a}$|
|Free energy of adsorption|$F_{\text{ads}} = \sigma a = -\dfrac{w_{AA}}{2a}$|

## Ch 15 Mixtures

### Ideal solutions

|Description|Equations|
|-:|:-|
|Entropy of solution for binary systems|$\Delta S_{\text{soln}} = -Nk(x_A \ln x_A + x_B \ln x_B)$|
|Entropy of solution for multicomponent systems|$\Delta S_{\text{soln}} = -Nk \sum x_i \ln x_i$|
|Internal energy of solution|$\Delta U_{\text{soln}} = 0$|
|Free energy of solution|$\Delta F_{\text{soln}} = -T \Delta S_{\text{soln}}$|

### Regular solutions

|Description|Equations|
|-:|:-|
|Exchange parameter <br/> (dimensionless free energy)|$\chi_{AB} = \dfrac{z}{kT} (w_{AB}-\frac{1}{2}\left(w_{AA}+w_{BB}\right))$|
|Exchange parameter|$\chi_{AB} = -\ln K_{\text{exch}}$|
|Exchange parameter interpretation|$\chi_{AB} > 0$, mixing unfavorable <br/> $\chi_{AB} < 0$, mixing favorable|
|Exchange energy|$RT\chi_{AB}$|
|Constant|$\begin{aligned}c_1 &= \chi_{AB}T \\\ &= \dfrac{z}{k} (w_{AB}-\frac{1}{2}\left(w_{AA}+w_{BB}\right))\end{aligned}$|
|Entropy of solution for binary systems|$\Delta S_{\text{soln}} = -Nk(x_A \ln x_A + x_B \ln x_B)$|
|Entropy of solution for multicomponent systems|$\Delta S_{\text{soln}} = -Nk \sum x_i \ln x_i$|
|Internal energy of solution of binary systems|$\Delta U_{\text{soln}} = NkT\chi_{AB}x_A x_B$|
|Internal energy of solution of multicomponent systems|$\Delta U_{\text{soln}} = NkT \sum \chi_{ij} x_i x_j$|
|Free energy of solution|$\Delta F_{\text{soln}} = \Delta U_{\text{soln}} - T \Delta S_{\text{soln}}$|
|Free energy of solution of binary systems|$\Delta F_{\text{soln}} = NkT (x_A \ln x_A + x_B \ln x_B + \chi_{AB}x_A x_B)$|
|Free energy of solution of multicomponent systems|$\Delta F_{\text{soln}} = NkT (\sum x_i \ln x_i + \sum\chi_{ij}x_i x_j)$|
|Chemical potentials of binary systems|$\mu_A = \ln x_A + \dfrac{zw_{AA}}{2kT} + \chi_{AB} x_B^2 \\\ \ \\\ \mu_B = \ln x_B + \dfrac{zw_{BB}}{2kT} + \chi_{AB} x_A^2$|
|Chemical potentials of multicomponent systems|$\begin{aligned} \mu_i & = \ln x_i + \dfrac{zw_{ii}}{kT} + \chi_{ij} (1-x_i)^2 \\\ &=\mu^\circ + kT \ln(\gamma x) \end{aligned}$|

### Surface tension

|Description|Equations|
|-:|:-|
|Interfacial tension|$\begin{aligned} \sigma_{AB} &= \dfrac{1}{a} (w_{AB}-\frac{1}{2}\left(w_{AA}+w_{BB}\right)) \\\ &= \dfrac{kT}{za} \chi_{AB} \end{aligned}$|
|Free energy of adsorption|$F_{\text{ads}} = \sigma a = \dfrac{kT}{z} \chi_{AB}$|

## Ch 16 Solvation and Phase Transfer

### Lewis/Randall rule

|Description|Equations|
|-:|:-|
|Notation <br/> ★ Solvent, pure limit $x_B \to 1$|A - non-volatile solute (e.g. $\ce{NaCl}$) <br/> B - volatile solvent (e.g. $\ce{H2O}$)|
|**Lewis/Randall rule** reference state|$\begin{aligned}p_B &= p_{B, int}^\circ x_B \exp \left(\chi _{AB}x_A^2+\dfrac{zw_{BB}}{2kT}\right) \\\ &= p_{B}^\circ x_B \exp \left(\chi _{AB}x_A^2\right)\end{aligned}$|
|**Raoult's law** <br/> ★ Ideal solution $\chi_{AB} = 0$|$p_B = p_B^\circ x_B$|
|Vapor pressure of B|$p_B^\circ = p_{B, int}^\circ \exp \left(\dfrac{zw_{BB}}{2kT}\right)$|

### Henry's law

|Description|Equations|
|-:|:-|
|Notation <br/> ★ Solute, dilute limit $x_B \to 0$|A - non-volatile solvent (e.g. $\ce{H2O}$) <br/> B - volatile solute (e.g. $\ce{CO_2}$)|
|**Henry's law** reference state|$\begin{aligned} p_B &= p_{B, int}^\circ x_B \exp \left(\chi_{AB} + \dfrac{aw_{BB}}{2kT}\right) \\\ &= p_{B, int}^\circ x_B \exp \left(w_{AB} - \dfrac{w_{AA}}{2}\right) \\\ &=\mathcal{H}_B x_B \end{aligned}$|
|Henry's constant|$\begin{aligned}\mathcal{H}\_B &= p_{B, int}^\circ \exp\left(\dfrac{z}{kT}w_{AB} - \dfrac{w_{AA}}{2}\right) \\\ &= p_{B, int}^\circ \exp\left(\dfrac{\Delta h^\circ_{\mathrm{soln}}}{kT}\right)\end{aligned}$|
|Enthalpy of solution|$\Delta h^\circ_{\mathrm{soln}} = z\left(w_{AB} - \dfrac{w_{AA}}{2}\right)$|

### Activity coefficient

|Description|Equations|
|-:|:-|
|Standard state chemical potential|$\Delta \mu_B^\circ = \mu_B^\circ(\text{liquid}) - \mu_B^\circ(\text{gas})$|
|Activity coefficient|$\gamma_B = \dfrac{p_B}{x_B}\exp\left(-\dfrac{\Delta \mu_B^\circ}{kT}\right)$|
|Activity coefficient in Lewis/Randall solvent convection|$\gamma_B = \exp[\chi_{AB} (1 - x_B)^2]$|
|Activity coefficient in Henry's solute convection|$\gamma_B = \exp[\chi_{AB} x_B (x_B - 2)]$|

### Colligative properties

|Description|Equations|
|-:|:-|
|Boiling point elevation|$\Delta T_b = \dfrac{RT_b^2 x_A}{\Delta h_{\text{vap}}^\circ}$|
|Freezing point depression|$\Delta T_f = \dfrac{RT_f^2 x_A}{\Delta h_{\text{fus}}^\circ}$|
|Osmotic pressure|$\pi = \dfrac{RTx_A}{v_B} = RTc_A$|

### Solute partition

|Description|Equations|
|-:|:-|
|Notation|A - immiscible solvent <br/> B - immiscible solvent <br/> s - solute|
|Partition coefficient from solvent A to B|$K_A^B = \dfrac{x_{sB}}{x_{sA}}$|
|Free energy of transfer|$\Delta \mu^\circ = \mu_s^\circ(B) - \mu_s^\circ(A)$|
|Statistical mechanical interpretation|$\ln K_A^B = \chi_{sA} (1 - x_{sA})^2 - \chi_{sB} (1 - x_{sB})^2$|
|Thermodynamical interpretation|$\ln K_A^B = - \dfrac{\mu_s^\circ(B) - \mu_s^\circ(A)}{kT} - \ln \left(\dfrac{\gamma_{sB}}{\gamma_{sA}}\right)$|
|Partition coefficient at infinite dilution <br/> ★ Infinite dilution of solute in both phases $x_{sa} \ll 1$, $x_{sB} \ll 1$, $\gamma_{sa} \to 1$, $\gamma_{sB} \to 1$|$\begin{aligned}\ln K_A^B &= - \dfrac{\mu_s^\circ(B) - \mu_s^\circ(A)}{kT} \\\ &= \chi_{sA} - \chi_{sB} \end{aligned}$|

## Ch 25 Phase Transitions

|Description|Equations|
|-:|:-|
|Fractions|$f^\alpha = \dfrac{n^\alpha}{n}$|
|Lever rule|$f' = \dfrac{x'' - x_0}{x'' - x'} \\\ f'' = \dfrac{x_0 - x'}{x'' - x'}$|
|Lever rule|$v_A = f^\alpha v_A^\alpha + f^\beta v_A^\beta$|
|Binodal curve|$\dfrac{\partial (\Delta F_{\text{mix}})}{\partial x} = 0 = NkT\left[\ln \left(\dfrac{x}{1-x}\right)+\chi _{AB}\left(1-2x\right)\right]$|
|Binodal curve <br/> ★ Dilute solute $x' \ll 1$, large $\chi_{AB}$|$\chi_{AB} = -\ln x'$|
|Spinodal curve|$\dfrac{\partial^2 F}{\partial x^2} = 0 = NkT\left[\frac{1}{x}+\frac{1}{1-x}-2\chi _{AB}\right]$|
|Spinodal curve <br/> ★ Dilute solute $x' \ll 1$, large $\chi_{AB}$|$x' = \dfrac{1}{2\chi_{AB} - 1}$|
|Critical point|$\dfrac{\partial^3 F}{\partial x^2} = 0$|
|Critical composition|$x_c = \dfrac{1}{2}$|
|Critical exchange parameter|$\chi_c = 2$|
|Critical exchange temperature|$T_c = \dfrac{c_1}{2}$|
|van der Waals EOS|$\left(p + \dfrac{a}{v^2}\right)(v-b) = RT$|
|Reduced form of van der Waals EOS|$\left(p_r + \dfrac{3}{v_r^2}\right)\left(v_r - \dfrac{1}{3}\right) = \dfrac{8}{3}T_r$|

<!-- ★ -->