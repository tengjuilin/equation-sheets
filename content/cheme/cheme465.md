---
title: "CHEM E 465 Reactor Design"
date: 2022-11-04T00:00:00-08:00
---

## Rate Law

### Equilibrium constant

|Description|Equations|
|-:|:-|
|Equilibrium constant and concentration|$K_c = \prod_i C_i^{\nu_i}$|
|Equilibrium constant and rate constant|$K_i = \dfrac{k_i}{k_{-i}}$|
|van't Hoff equation <br/> ★ $\Delta h_{\mathrm{rxn}}^\circ \not= f(T)$|$\dfrac{d \ln K}{dT} = \dfrac{\Delta h_{\mathrm{rxn}}^\circ}{RT^2}$|
|T dependence of equilibrium constant|$\ln \left(\dfrac{K_2}{K_1}\right)=-\dfrac{\Delta h_{\mathrm{rxn}}^\circ}{R}\left(\dfrac{1}{T_2}-\dfrac{1}{T_1}\right)$|

### Rate constant

|Description|Equations|
|-:|:-|
|General reaction|$\ce{aA + bB ->[\mathit{k}] cC + dD}$|
|Relative reaction rates|$\dfrac{-r_A}{a} = \dfrac{-r_B}{b} = \dfrac{-r_C}{c} = \dfrac{-r_D}{d}$|
|Power law|$r_A = -k C_A^a C_B^b$|
|Unit of rate constant|$k \ [=] \ \mathrm{M^{1-n}/s}$|
|Arrhenius equation <br/> ★ $E_a \not= f(T)$|$\dfrac{d \ln k}{dT} = \dfrac{E_a}{RT^2}$|
|Arrhenius equation|$k = A\exp\left(-\dfrac{E_a}{RT}\right)$|
|T dependence of rate constant|$\ln \left(\dfrac{k_2}{k_1}\right)=-\dfrac{E_a}{R}\left(\dfrac{1}{T_2}-\dfrac{1}{T_1}\right)$|
|Arrhenius plot|$\ln k = \ln A - \dfrac{E_a}{R}\dfrac{1}{T}$|
|Note|Increase $E_a$, increase $k$'s sensitivity to T|
|Collision theory|$k \propto \sqrt{T}\exp\left(-\dfrac{E_0}{RT}\right)$|
|Transition state theory|$k \propto T\exp\left(-\dfrac{\Delta H^*}{RT}\right)$|

## Reactor Design and Sizing

|Description|Equations|
|-:|:-|
|General mole balance|$\begin{aligned}&\mathrm{in} &&- \mathrm{out} &&+ \mathrm{generation} &&= \mathrm{accumulation} \\\ &F_{j0} &&- F_j &&+ G_j &&= \dfrac{dN_i}{dt}\end{aligned}$|
|General generation term|$G_j = \int r_j dV$|
|Spatially uniform generation term|$G_j = r_j V$|
|Conversion|$X_j \equiv X = \dfrac{N_{j0} - N_{j}}{N_{j0}} = \dfrac{F_{j0} - F_{j}}{F_{j0}}$|
|Mole/flow rate in terms of conversion|$N_j = N_{j0} (1 - X) \newline F_j = F_{j0} (1 - X)$|

### Batch reactors

|Description|Equations|
|-:|:-|
|**Design equation** <br/> ★ Perfectly mixed|$\dfrac{dN_j}{dt} = r_j V$|
|**Design equation** <br/> ★ Perfectly mixed|$N_{j0}\dfrac{dX}{dt} = -r_j V$|
|**Time needed** <br/> Integral form of design equation|$t = \displaystyle\int_{N_{j1}}^{N_{j0}} \dfrac{dN_j}{-r_j V} = N_{j0} \displaystyle\int_0^X \dfrac{dX}{-r_j V}$|
|Reaction rate of constant volume operation|$r_j = \dfrac{C_j}{dt}$|
|Reaction rate of constant pressure operation|$r_j = \dfrac{dC_j}{dt} + \dfrac{C_j}{V}\dfrac{dV}{dt}$|

### Continuous-flow reactors

#### Continuous stirred tank reactor (CSTR)

|Description|Equations|
|-:|:-|
|Also known as|Vat, backmix reactor|
|**Design equation** <br/> ★ Perfectly mixed, steady-state|$V = \dfrac{F_{j0} - F_j}{-r_j} = \dfrac{F_{j0}X}{-r_j}$|
|Reaction rate|$r_j = \dfrac{F_{j0} - F_j}{-V} = -\dfrac{F_{j0}X}{V}$|

#### Plug-flow reactor (PFR)

|Description|Equations|
|-:|:-|
|Also known as|Tubular reactor|
|**Design equation** <br/> ★ Perfectly mixed, steady state <br/> ★ Plug flow, no radial dependence|$r_j = \dfrac{dF_j}{dV} = -F_{j0}\dfrac{dX}{dV}$|
|**Volume needed** <br/> Integral form of design equation|$V = \displaystyle\int_{F_A}^{F_{A0}}\dfrac{dF_A}{-r_A} = F_{j0} \displaystyle\int_0^X \dfrac{dX}{-r_j}$|

#### Packed-bed reactor (PBR)

|Description|Equations|
|-:|:-|
|Heterogeneous reaction rate|$r_A = \rho_b r_A'$|
|**Design equation**|$r_A\' = \dfrac{dF_A}{dW} = -F_{j0}\dfrac{dX}{dW}$|
|**Mass of catalyst** <br/> Integral form of design equation|$W = \displaystyle\int_{F_A}^{F_{A0}}\dfrac{dF_A}{-r_A\'} = F_{j0} \displaystyle\int_0^X \dfrac{dX}{-r_j\'}$|

### Semi-batch reactor

|Description|Equations|
|-:|:-|
|Design equation|$r_j = \dfrac{\dfrac{dN_j}{dt} - F_{j0}}{V(t)}$|

### Levenspiel plot

|Description|Equations|
|-:|:-|
|Levenspiel plot|$\dfrac{F_{j0}}{-r_j}$ vs. $X$|
|CSTR volume|$V = \dfrac{F_{j0}X}{-r_j}$ = Area of rectangle|
|PFR volume|$V = F_{j0} \displaystyle\int_0^X \dfrac{dX}{-r_j}$ = Area under Levenspiel plot|
|Reaction of order > 0|$V_{\mathrm{CSTR}} > V_\mathrm{PFR}$ (Choose PFR)|
|Reaction of order < 0|$V_{\mathrm{CSTR}} < V_\mathrm{PFR}$ (Choose CSTR)|

### Reactor choice

|Reactor Type|Advantage|Disadvantage|
|-:|:-|:-|
|Batch|- High conversion|- High labor cost and downtime <br/> - Difficult to scale up <br/> - Batch-to-batch variability|
|CSTR|- Good T control|- Hard to get high conversion|
|PFR|- Easy maintenance <br/> - High conversion per unit volume|- Difficult for T control|

<!-- ★ -->