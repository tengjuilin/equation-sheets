---
title: "CHEM E 325 Energy and Entropy"
date: 2021-12-23T00:00:00-08:00
---

## Thermodynamic Properties and Data

|Description|Equations|
|-:|:-|
|Pressure (kinetic theory)|$P = \dfrac{F}{A}$|
|Ideal gas law|$PV = nRT \newline Pv = RT$|
|Quality|$q = \dfrac{n_v}{n_l + n_v}$|
|Fraction|$x_A = f^\alpha x_A^\alpha + (1-f^\alpha)x_A^\beta$|
|Lever rule for intensive properties|$v_{\text{total}} = v_v q + v_l (1-q)$|
|Gibbs phase rule|$\mathcal{F} = 2 + c - p - r$|
|Mole fraction|$x_i = \dfrac{n_i}{\sum_j n_j}$|

## Intermolecular Interactions

### Intermolecular potentials

|Description|Equations|
|-:|:-|
|Keesom potential (dipole-dipole)|$\Gamma_{ij} = -\dfrac{2}{3}\dfrac{\mu_i^2 \mu_j^2}{r_{ij}^6 k_B T}$|
|Debye potential (dipole-induced dipole)|$\Gamma_{ij} = -\dfrac{\alpha_i \mu_j^2}{r_{ij}^6}$|
|London dispersion potential (induced dipole-induced dipole)|$\Gamma_{ij} = -\dfrac{3}{2}\dfrac{\alpha_i \alpha_j}{r_{ij}^6}\dfrac{1}{\frac{1}{I_i} + \frac{1}{I_j}}$|
|Lennard-Jones potential|$\Gamma = 4\varepsilon \left[ \left(\dfrac{\sigma}{r}\right)^{12} - \left(\dfrac{\sigma}{r}\right)^{6} \right]$|
|Equilibrium intermolecular distance|$r(\Gamma_{\min}) = r(\varepsilon) = 2^{1/6}\sigma = 1.12 \sigma$|

### Molecular dynamics simulation

|Description|Equations|
|-:|:-|
|Nondimensionalized distance|$"r" = \dfrac{r}{\sigma}$|
|Nondimensionalized temperature|$"T" = \dfrac{k_BT}{\varepsilon}$|
|Nondimensionalized pressure|$"P" = \dfrac{\sigma^3}{\varepsilon}P$|
|Nondimensionalized energy|$"E" = \dfrac{U}{\varepsilon}$|
|Nondimensionalized time|$"t" = \dfrac{t}{\sigma \sqrt{m/\varepsilon}}$|
|Kinetic energy and temperature|$\mathrm{KE} = nT$|
|Ideal gas pair potential energy|$\mathrm{PE} = 0$|
|Condensed phase interaction potential energy <br/> (with normalized energy unit of $\varepsilon$)|$\mathrm{PE} = -N_{\text{inter}}$|
|Amount of interactions|$N_{\text{inter}} = \frac{1}{2}$(# molecules)(# neighbors)|

## Equation of States

### van der Waals EOS

|Description|Equations|
|-:|:-|
|van der Waals EOS in terms of $P$|$P = \dfrac{RT}{v-b} - \dfrac{a}{v^2}$|
|van der Waals EOS in terms of $v$|$v^3 - \left(\dfrac{RT}{v-b}\right) v^2 + \dfrac{a}{P} v - \dfrac{a}{P}b = 0$|
|van der Waals parameter $a$|$a = \dfrac{27}{64}\dfrac{(RT_c)^2}{P_c}$|
|van der Waals parameter $b$|$b = \dfrac{RT_c}{8P_c}$|
|Molar potential energy|$e_p = -\dfrac{a}{v}$|
|Pressure at zero kinetic energy|$P = - \dfrac{a}{v^2}$|
|Reduced temperature|$T_r = \dfrac{T}{T_c}$|
|Reduced pressure|$P_r = \dfrac{P}{P_c}$|
|Compressibility factor|$z = \dfrac{v_{\text{real}}}{v_{\text{ideal}}} = \dfrac{Pv}{RT}$|
|Potential energy|$e_p = u_{\text{real}}(T, P) - u_{\text{ideal}}(T, P=0)$|
|Internal energy departure function|$\dfrac{e_p}{RT_c} = \dfrac{u_{\text{real}} - u_{\text{ideal}}}{RT_c}$|
|Internal energy departure function in van der Waals EOS|$\dfrac{e_p}{RT_c} = -\dfrac{27 P_r}{64T_r z}$|

### Lee-Kesler EOS

|Description|Equations|
|-:|:-|
|Lee-Kesler compressibility factor|$z = z^{(0)} + \omega z^{(1)}$|
|Acentric factor|$\omega = -1-\log_{10}(P^{\text{sat}}_r(T_r=0.7))$|
|General departure function in Lee-Kesler EOS|$\text{dep} = \text{dep}^{(0)} + \omega \ \text{dep}^{(1)}$|
|Internal energy and enthalpy departure function|$\dfrac{u_{\text{real}} - u_{\text{ideal}}}{RT_c} = \dfrac{h_{\text{real}} - h_{\text{ideal}}}{RT_c} + T_r (1-z)$|

## First Law of Thermodynamics

|System Type|First Law of Thermodynamics|
|-:|:-|
|Isolated system|$\Delta U = 0$|
|Closed system|$\Delta U = Q + W$|
|Open system|$\dfrac{dU}{dt} = \sum\limits_{\text{in}} \dot{n}\_i h_i - \sum\limits_{\text{out}} \dot{n}\_i h_i + \sum \dot{Q_i} + \dot{W_s}$|
|Open system in steady state|$0 = \sum\limits_{\text{in}} \dot{n}\_i h_i - \sum\limits_{\text{out}} \dot{n}\_i h_i + \sum \dot{Q_i} + \dot{W_s}$|

|Description|Equations|
|-:|:-|
|Work|$W = \displaystyle\int P \ dV$|
|Enthalpy|$H = U + PV$|
|Constant volume molar heat capacity|$c_v = \left(\dfrac{\partial u}{\partial T}\right)_v$|
|Constant pressure molar heat capacity|$c_P = \left(\dfrac{\partial h}{\partial T}\right)_P$|
|Relationship between molar heat capacities|$c_P = c_v + R$|

## Second Law of Thermodynamics

|System Type|Second Law of Thermodynamics|
|-:|:-|
|Isolated system <br/> $S_{\text{gen}} \ge 0$|$\Delta S = S_{\text{gen}}$|
|Closed system <br/> $S_{\text{gen}} \ge 0$|$\Delta S = \displaystyle\int \dfrac{\delta Q}{T} + S_{\text{gen}}$|
|Open system <br/> $\dot{S}_{\text{gen}} \ge 0$|$\dfrac{dS}{dt} = \sum\limits_{\text{in}} \dot{n}\_i s_i - \sum\limits_{\text{out}} \dot{n}\_i s_i + \sum \dfrac{\dot{Q_i}}{T_i} + \dot{S}_{\text{gen}}$|
|Open system in steady state <br/> $\dot{S}_{\text{gen}} \ge 0$|$0 = \sum\limits_{\text{in}} \dot{n}\_i s_i - \sum\limits_{\text{out}} \dot{n}\_i s_i + \sum \dfrac{\dot{Q_i}}{T_i} + \dot{S}_{\text{gen}}$|

### Counting configurations

|Description|Equations|
|-:|:-|
|Ergotic hypothesis|$\lvert f \rvert = \langle f \rangle$|
|Equal probability postulate|$P_j = \dfrac{1}{\Omega}$|
|Entropy|$S = k_B \ln\Omega$|
|Permutability <br/> $N_A$ distinguishable particles in $N$ sites|$\Pi = \dfrac{N!}{(N-N_A)!}$|
|Multiplicity <br/> $N_A$ indistinguishable particles in $N$ sites|$\Omega = \dfrac{N!}{N_A!(N-N_A)!}$|
|Multiplicity <br/> $N_A, N_B, ...$ indistinguishable particles in $N$ sites|$\Omega = \dfrac{N!}{N_A!N_B!N_C! \cdots}$|
|Stirling approximation|$\lim\limits_{a \to\infty} \ln(a!) = a \ln(a) - a$|
|Entropy of $N$ sites with fraction $x$ activated|$S = k_BN[-x\ln(x) - (1-x)\ln(1-x)]$|

### Fundamental properties

|Description|Equations|
|-:|:-|
|Molar entropy <br/> $\mathcal{C}$ = constant|$s = R\ln(vu^{3/2}) + \mathcal{C}$|
|Molar internal energy <br/> $\mathcal{C}$ = constant|$u = \mathcal{C}v^{-2/3}\exp\left(\dfrac{2}{3}\dfrac{s}{R}\right)$|
|Temperature|$T = \left(\dfrac{\partial u}{\partial s}\right)_v$|
|Pressure|$P = -\left(\dfrac{\partial u}{\partial v}\right)_s$|
|Fundamental property relation|$du = T ds - P dv$|
|Reversible heat at constant $v$|$\Delta u = q = \int T \ ds$|
|Reversible work at constant $s$|$w = - \int P \ dv$|

### Entropy generation

|Description|Equations|
|-:|:-|
|Reversible process|$s_{\text{gen}} = 0$|
|Irreversible process (caused by temperature gradient)|$s_{\text{gen}} > 0$|

## First and Second Law Analysis

### Isothermal/Isoenergetic process

Isoenergetic process ($\Delta u = 0 \implies \Delta T = 0$) of ideal gas  has similar analysis.

|Description|Equations|
|-:|:-|
|Condition <br/> ★ Ideal gas|$\Delta T = 0$|
|Internal energy change|$\Delta u = 0$|
|Enthalpy change|$\Delta h = 0$|
|First law|$\Delta u = q  + w = 0$|
|Work (changing volume)|$w = -\displaystyle\int \dfrac{RT}{v} dv = -RT\ln\left(\dfrac{v_2}{v_1}\right)$|
|Work (changing pressure)|$w = \displaystyle\int \dfrac{RT}{P} dP = RT\ln\left(\dfrac{P_2}{P_1}\right)$|
|Heat|$q = -w$|
|Entropy change|$\Delta s = \displaystyle\int \dfrac{\delta q}{T} = \dfrac{q}{T} = -\dfrac{w}{T}$|
|Entropy change (changing volume)|$\Delta s = R\ln\left(\dfrac{v_2}{v_1}\right)$|
|Entropy change (changing concentration)|$\Delta s = -R\ln\left(\dfrac{c_2}{c_1}\right)$|
|Entropy change (changing pressure)|$\Delta s = -R\ln\left(\dfrac{P_2}{P_1}\right)$|

### Adiabatic process

|Description|Equations|
|-:|:-|
|Condition <br/> ★ Ideal gas|$q = 0$|
|First law|$\Delta u = w$|
|Enthalpy change|$\Delta h = \Delta u + R \Delta T$|
|Work (changing volume)|$w = -\displaystyle\int \dfrac{RT}{v} dv = -RT\ln\left(\dfrac{v_2}{v_1}\right)$|
|Work (changing pressure)|$w = \displaystyle\int \dfrac{RT}{P} dP = RT\ln\left(\dfrac{P_2}{P_1}\right)$|
|Entropy change|$\Delta s = 0$|

### Isochoric process

|Description|Equations|
|-:|:-|
|Condition <br/> ★ Ideal gas|$\Delta v = 0$|
|Work|$w = 0$|
|Internal energy change|$\Delta u = \displaystyle\int c_v \ dT$|
|First law|$q = \Delta u$|
|Entropy change|$\Delta s = \displaystyle\int \dfrac{\delta q}{T} = \int \dfrac{du}{T} = \int \dfrac{c_v}{T} \ dT$|

### Isobaric process

|Description|Equations|
|-:|:-|
|Condition <br/> ★ Ideal gas|$\Delta P = 0$|
|Internal energy change|$\Delta u = \displaystyle\int c_v \ dT$|
|Enthalpy change|$\Delta h = \displaystyle\int c_p \ dT$|
|Work|$w = -P\Delta v$|
|Heat|$q = \Delta h$|
|Entropy change|$\Delta s = \displaystyle\int \dfrac{\delta q}{T} = \int \dfrac{dh}{T} = \int \dfrac{c_p}{T} \ dT$|

### Other processes

|Description|Equations|
|-:|:-|
|Incompressible condensed phases|$v_0$ is constant, small|
|Incompressible condensed phases at low pressure|$\Delta u = \Delta h = \displaystyle\int c_p \ dT$|
|Incompressible condensed phases at high pressure|$\Delta h = \displaystyle\int c_p \ dT + v_0(P_1 - P_0)$|
|Incompressible condensed phases|$\Delta s = \displaystyle\int \dfrac{c_p}{T} dT = c_p \ln\left(\dfrac{T_1}{T_2}\right)$|
|Phase change|$\Delta h = q \newline \Delta s = \dfrac{q}{T} =  \dfrac{\Delta h}{T}$|

## Process Efficiency

|Description|Equations|
|-:|:-|
|Maximum work of heat engine|$W_{\max} = Q_{\text{in}} \left(1 - \dfrac{T_c}{T_h}\right)$|
|Minimum work of heat heat pump|$W_{\max} = Q_{\text{out}} \left(1 - \dfrac{T_c}{T_h}\right)$|
|Reversible work|$W_{\text{rev}} = Q_{1} \left(1 - \dfrac{T_c}{T_h}\right)$|
|Carnot efficiency|$\eta = \dfrac{W_{\text{rev}}}{Q_1} = 1 - \dfrac{T_c}{T_h}$|
|Ideal gas entropy|$\Delta s(T, v) = \displaystyle\int \dfrac{c_v}{T} dT + R \ln\left(\dfrac{v}{v_0}\right)$|
|Ideal gas entropy|$\Delta s(T, P) = \displaystyle\int \dfrac{c_p}{T} dT - R \ln\left(\dfrac{P}{P_0}\right)$|
|Lost work|$W_{\text{lost}} = T_c s_{\text{gen}}$|
|Exthalpy for multi-stream|$\dot{E} = \dot{W}_{\text{rev}} \newline = \sum\limits\_{i}^{\text{source}} \dot{n}_i (h_i - T_0 s_i) - \sum\limits\_{i}^{\text{ground}} \dot{n}_i (h_i^\circ - T_0 s_i^\circ)$|
|Exthalpy for single stream|$\dot{W}_{\text{rev}} = \Delta h - T_0 \Delta s$|

## Phase equilibrium

### Single component equilibrium

|Description|Equations|
|-:|:-|
|Gibbs free energy (constant $T, P$)|$G = H - TS$|
|Helmholtz free energy (constant $T, V$)|$F = A = U - TS$|
|Entropy change of universe|$\Delta S_{\text{univ}} \ge 0$|
|Gibbs free energy change of spontaneous process|$\Delta G \le 0$|
|Helmholtz free energy change of spontaneous process|$\Delta F \le 0$|
|Thermal equilibrium|$T^\alpha = T^\beta$|
|Mechanical equilibrium|$P^\alpha = P^\beta$|
|Chemical equilibrium|$g^\alpha = g^\beta$|
|Clausius-Clapeyron equation|$\dfrac{d \ln P_{\text{sat}}}{d (1/T)} = -\dfrac{1}{R}\Delta h_{\text{vap}}(T)$|
|**Clausius-Clapeyron equation** <br/> ★ modest pressure, incompressible liquid, ideal gas, constant $\Delta h_{\text{vap}}$|$\ln\left(\dfrac{P_{\text{sat}}}{P_0}\right) = -\dfrac{\Delta h_{\text{vap}}^\circ}{R} \left(\dfrac{1}{T} - \dfrac{1}{T_0}\right)$|
|Antoine equation|$\ln(P_{\text{sat}}) = A - \dfrac{B}{C + T}$|

### Multicomponent equilibrium

|Description|Equations|
|-:|:-|
|Partial molar properties|$\bar{x}_i = \left(\dfrac{\partial x}{\partial n_i}\right)\_{\mathrm{others}, n\_{j \not = i}}$|
|Partial molar gibbs free energy|$\bar{g}_i = \left(\dfrac{\partial G}{\partial n_i}\right)\_{T, P, n\_{j \not = i}}$|
|Partial molar gibbs free energy|$\bar{g}_i = \bar{h}_i - T\bar{s}_i$|
|Entropy|$S = -\left(\dfrac{\partial G}{\partial T}\right)\_{P, n\_{j}}$|
|Volume|$V = \left(\dfrac{\partial G}{\partial P}\right)\_{T, n\_{j}}$|
|Total derivative of gibbs free energy|$dG = -S \ dT + V \ dP + \sum\limits_i \bar{g}_i \ dn_i$|
|Chemical potential|$\mu_i = \bar{g}_i$|
|Chemical equilibrium|$\mu_i^\alpha = \mu_i^\beta$|
|Raoult's law|$P_A = x_A^g P = x_A^l P_A^{\text{sat}}$|
|Condensation curve|$P = (P_A^{\text{sat}} - P_B^{\text{sat}})x_A^l + P_B^{\text{sat}}$|
|Boiling curve|$P = \dfrac{P_A^{\text{sat}}P_B^{\text{sat}}}{P_A^{\text{sat}} - (P_A^{\text{sat}} - P_B^{\text{sat}})x_A^g}$|
|Henry's law <br/> ★ Low pressure, dilute solution|$C_A = K_H(T) P_A$|
|Gibbs-Duhem Equations|$\sum \mu_i \ dn_i = 0 \newline \sum n_i \ d\mu_i = 0$|
|Colligative property|$\mu_{\text{solvent}} = RT \ln(1 - x_A) + \mu_{\text{solvent}}^\circ$|

<!-- ★ -->
