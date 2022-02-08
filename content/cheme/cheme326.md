---
title: "CHEM E 326 Chemical Engineering Thermodynamics"
date: 2022-01-05T00:00:00-08:00
lightgallery: true
---

## Thermodynamic Properties and Data

|Description|Equations|
|-:|:-|
|Mechanical equilibrium|$P_{\text{sys}} = P_{\text{surr}}$|
|Thermal equilibrium|$T_{\text{sys}} = T_{\text{surr}}$|
|Chemical equilibrium|$\mu(t_1) = \mu(t_2)$|
|Gibbs phase rule|$\mathcal{F} = 2 + c - p - r$|
|Quality|$x = \dfrac{n_v}{n_l + n_v} = \dfrac{v - v_l}{v_v - v_l}$|
|Critical point|$\left( \dfrac{\partial P}{\partial v} \right)\_{T_c} = 0, \left( \dfrac{\partial^2 P}{\partial v^2} \right)\_{T_c} = 0$|

## First Law of Thermodynamics

|System Type|Equations|
|-:|:-|
|Closed systems|$\Delta u + \Delta e_K + \Delta e_P = q + w$|
|Closed systems|$\Delta u = q + w$|
|Open systems|$\dfrac{dU}{dt} = \sum\limits_{\text{in}}\dot{n}_i h_i + \sum\limits_{\text{out}}\dot{n}_i h_i + \dot{Q} + \dot{W}_s$|
|Open system at steady state|$0 = \sum\limits_{\text{in}}\dot{n}_i h_i + \sum\limits_{\text{out}}\dot{n}_i h_i + \dot{Q} + \dot{W}_s$|

|Description|Equations|
|-:|:-|
|Work|$w = - \int P_{\text{ext}} dv$|
|Enthalpy|$h = u + Pv$|
|Efficiency of irreversible isothermal expansion|$\eta = \dfrac{w_{\text{irrev}}}{w_{\text{rev}}}$|
|Efficiency of irreversible isothermal compression|$\eta = \dfrac{w_{\text{rev}}}{w_{\text{irrev}}}$|

### Heat capacity

|Description|Equations|
|-:|:-|
|Constant volume heat capacity|$c_v = \left(\dfrac{\partial u}{\partial T}\right)_v$|
|Constant pressure heat capacity|$c_P = \left(\dfrac{\partial h}{\partial T}\right)_P$|
|Ideal gas heat capacity|$c_P = c_v + R$|
|Condensed phase heat capacity (l, s)|$c_P \approx c_v$|
|Mean heat capacity of gas|$\bar{c}\_P = \dfrac{1}{T_2 - T_1} \displaystyle\int_{T_1}^{T_2} c_P(T) dT$|

### Enthalpy

|Description|Equations|
|-:|:-|
|Enthalpy of vaporization|$\Delta h_{\text{vap}} = h_v - h_l$|
|Enthalpy of fusion|$\Delta h_{\text{fus}} = h_s - h_l$|
|Enthalpy of sublimation|$\Delta h_{\text{sub}} = h_v - h_s$|
|Enthalpy of phase change at any $T$|$\Delta h_{\text{vap}}(T) = \Delta h_{\text{vap}}(T_b) + \int_{T_b}^{T} (c_P^{v} - c_P^l)dT$|
|Enthalpy of reaction|$\Delta h_{\text{rxn}}^\circ = \sum \nu_i \Delta h_{f, i}$|

## Second Law of Thermodynamics

|System Type|Equations|
|-:|:-|
|Isolated system|$\Delta S_{\text{univ}} \ge 0$|
|Closed system|$\Delta S_{\text{sys}} - \dfrac{Q_{\text{sys}}}{T_{\text{surr}}} \ge 0$|
|Open system|$\sum\limits_{\text{out}} \dot{n}_i s_i - \sum\limits_{\text{in}} \dot{n}_i s_i - \dfrac{\dot{Q}}{T_{\text{surr}}} + \dfrac{dS}{dt} \ge 0$|
|Open system at steady state|$\sum\limits_{\text{out}} \dot{n}_i s_i - \sum\limits_{\text{in}} \dot{n}_i s_i - \dfrac{\dot{Q}}{T_{\text{surr}}} \ge 0$|

|Description|Equations|
|-:|:-|
|Entropy|$ds = \dfrac{\delta q_{\text{rev}}}{T}$|

## Closed System Balance

### Polytropic processes

|Description|$\gamma$|Equation|
|-:|:-:|:-|
|Polytropic|-|$PV^\gamma = \text{const}$|
|Isobaric|$0$|$P = \text{const}$|
|Isothermal|$1$|$PV = \text{const}$|
|Isentropic|$k = \dfrac{c_P}{c_v}$|$PV^k = \text{const}$|
|Isochoric|$\infty$|$V = \text{const}$|

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

### Adiabatic/Isentropic process

|Description|Equations|
|-:|:-|
|Condition <br/> ★ Ideal gas|$q = 0$|
|First law|$\Delta u = w$|
|Enthalpy change|$\Delta h = \Delta u + R \Delta T$|
|Work (changing volume)|$w = -\displaystyle\int \dfrac{RT}{v} dv = -RT\ln\left(\dfrac{v_2}{v_1}\right)$|
|Work (changing pressure)|$w = \displaystyle\int \dfrac{RT}{P} dP = RT\ln\left(\dfrac{P_2}{P_1}\right)$|
|Entropy change|$\Delta s = 0$|
|Heat capacity ratio|$\gamma = \dfrac{c_P}{c_v}$|
|PVT relationship|$P_1 V_1^\gamma = P_2 V_2^\gamma \newline T_1 V_1^{\gamma-1} = T_2 V_2^{\gamma-1} \newline P_1^{(1/\gamma)-1} T_1 = P_2^{(1/\gamma)-1} T_2$|

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

### Carnot cycle

|Description|Equations|
|-:|:-|
|Net work|$-W_{\text{net}} = \vert W_{12} \vert + \vert W_{23} \vert - \vert W_{34} \vert - \vert W_{41} \vert$|
|Net work and heat|$-W_{\text{net}} = \vert Q_H \vert - \vert Q_C \vert$|
|Carnot efficiency|$\eta = 1 - \dfrac{T_H}{T_C}$|
|State properties after cycle|$\Delta u_{\text{cycle}} = 0 \newline \Delta h_{\text{cycle}} = 0 \newline \Delta s_{\text{cycle}} = 0$|
|Entropy change of surrounding|$\Delta s_{\text{surr}} = 0 = -\dfrac{q_H}{T_H} -\dfrac{q_C}{T_C}$|

{{< image src="/cheme/cheme-326-carnot-cycle.png" caption="Carnot cycle. ([Episode C1 - Process Efficiency by Stu Adler UW](https://www.youtube.com/watch?v=jU1vC8Ys5vM&list=PLhXC30PF_5OXOGB0pbcCNwpVMUznQtBmN))" >}}
{{< image src="/cheme/cheme-326-carnot-cycle-diagram.png" caption="Carnot cycle diagrams. ([Episode C1 - Process Efficiency by Stu Adler UW](https://www.youtube.com/watch?v=jU1vC8Ys5vM&list=PLhXC30PF_5OXOGB0pbcCNwpVMUznQtBmN))" >}}

## Open System Balance

|Description|Equations|
|-:|:-|
|Open system balance|$0 = \dot{m}_1 (\hat{h} + \frac{1}{2}v^2 + gz)_1 - \dot{m}_2 (\hat{h} + \frac{1}{2}v^2 + gz)_2$|
|Shaft work|$\dot{w}_s = \int v \ dP + \Delta \dot{e}_K + \Delta \dot{e}_P$|
|Nozzle, diffuser simplifications|$0 = \Delta E_P = \dot{Q} = \dot{W}_s$|
|Turbine, pump, compressor simplifications|$0 = \Delta E_K = \dot{Q}$|
|Heat exchanger simplifications|$0 = \Delta E_P = \Delta E_K = \dot{W}_s$|
|Throttling device simplifications|$0 = \Delta E_P = \Delta E_K = \dot{Q} = \dot{W}_s$|

### Rankine cycle

|Description|Equations|
|-:|:-|
|Turbine|$\dot{w}_s = h_2 - h_1 \newline \dot{q} = 0$|
|Condenser|$\dot{q} = h_3 - h_2 \newline \dot{w}_s = 0$|
|Compressor|$\dot{w}_c = h_4 - h_3 = v\Delta P \newline \dot{q} = 0$|
|Boiler|$\dot{q} = h_1 - h_4 \newline \dot{w}_s = 0$|
|Efficiency|$\eta = \dfrac{\vert\dot{w}_s\vert - \dot{w}_c}{\dot{q}_h} = \dfrac{\vert h_2 - h_1 \vert - (h_4 - h_3)}{h_1 - h_4}$|
|Net work|$\dot{w}_{\text{net}} = \dot{q}_H - \vert\dot{q}_C\vert = \vert\dot{w}_s\vert - \dot{w}_c$|

{{< image src="/cheme/cheme-326-rankine-cycle.png" caption="Ideal Rankine cycle. (Engineering and Chemical Thermodynamics 2e by Koretsky p164.)" >}}

### Refrigeration cycle

|Description|Equations|
|-:|:-|
|Evaporator|$\dot{q} = h_2 - h_1 \newline \dot{w}_s = 0$|
|Compressor|$\dot{w}_s = h_3 - h_2 \newline \dot{q} = 0$|
|Condenser|$\dot{q} = h_4 - h_3 \newline \dot{w}_s = 0$|
|Value|$\dot{w}_s = 0 \newline \dot{q} = 0 \newline \Delta h = 0 \newline \Delta s > 0 \text{ (irreversible expansion)}$|
|Coefficient of performance|$\mathrm{COP} = \dfrac{\dot{Q}_C}{\dot{W}_c} = \dfrac{h_2 - h_1}{h_3 - h_2}$|

{{< image src="/cheme/cheme-326-refrigeration-cycle.png" caption="Ideal refrigeration cycle. (Engineering and Chemical Thermodynamics 2e by Koretsky p170.)" >}}

## Intermolecular Potentials

|Description|Equations|
|-:|:-|
|Conservative force|$F_{ij} = -\nabla \Gamma_{ij}$|
|Potential|$\Gamma_{ij} = -\int F_{ij} \ dr$|

### Attractive potentials (SI unit)

|Description|Equations (SI unit)|
|-:|:-|
|Coulomb interaction <br/> (electrostatic, point charges)|$\Gamma_{ij}(r) = \dfrac{Q_i Q_j}{4\pi\varepsilon_0}\dfrac{1}{r}$|
|Dipole-dipole interaction <br/> (polar, electric dipole, Keesom)|$\Gamma_{ij}(r) = -\dfrac{(2)}{3}\dfrac{\mu_i^2 \mu_j^2}{(4\pi\varepsilon_0)^2}\dfrac{1}{kT}\dfrac{1}{r^6}$|
|Dipole-induced dipole interaction <br/> (induction, Debye)|$\Gamma_{ij}(r) = -\dfrac{\alpha_i \mu_j^2}{(4\pi\varepsilon_0)^2}\dfrac{1}{r^6}$|
|Induced dipole-induced dipole interaction <br/> (dispersion, London)|$\Gamma_{ij}(r) = -\dfrac{3}{2}\dfrac{\alpha_i \alpha_j}{(4\pi\varepsilon_0)^2}\dfrac{I_i I_j}{I_i + I_j}\dfrac{1}{r^6}$|

|Description|Equations (SI unit)|
|-:|:-|
|van der Waals interaction|$\Gamma_{ij}^{\text{vdw}} = \Gamma_{ij}^{\text{K}} + \Gamma_{ij}^{\text{D}} + \Gamma_{ij}^{\text{L}} = -\dfrac{C_{\text{vdw}}}{r^6}$|
|Keesom coefficient|$C^{\text{K}} = \dfrac{(2)}{3}\dfrac{\mu_i^2 \mu_j^2}{(4\pi\varepsilon_0)^2}\dfrac{1}{kT}$|
|Debye coefficient|$C^{\text{D}} = \dfrac{\alpha_i \mu_j^2 + \alpha_j \mu_i^2}{(4\pi\varepsilon_0)^2}$|
|London coefficient|$C^{\text{L}} = \dfrac{3}{2}\dfrac{\alpha_i \alpha_j}{(4\pi\varepsilon_0)^2}\dfrac{I_i I_j}{I_i + I_j}$|

### Attractive potentials (CGS unit)

|Description|Equations (CGS unit)|
|-:|:-|
|Coulomb interaction <br/> (electrostatic, point charges)|$\Gamma_{ij}(r) = \dfrac{Q_i Q_j}{r}$|
|Dipole-dipole interaction <br/> (polar, electric dipole, Keesom)|$\Gamma_{ij}(r) = -\dfrac{(2)}{3}\dfrac{\mu_i^2 \mu_j^2}{kT}\dfrac{1}{r^6}$|
|Dipole-induced dipole interaction <br/> (induction, Debye)|$\Gamma_{ij}(r) = -\dfrac{\alpha_i \mu_j^2}{r^6}$|
|Induced dipole-induced dipole interaction <br/> (dispersion, London)|$\Gamma_{ij}(r) = -\dfrac{3}{2}\dfrac{\alpha_i \alpha_j}{r^6}\dfrac{I_i I_j}{I_i + I_j}$|

|Description|Equations (CGS unit)|
|-:|:-|
|van der Waals interaction|$\Gamma_{ij}^{\text{vdw}} = \Gamma_{ij}^{\text{K}} + \Gamma_{ij}^{\text{D}} + \Gamma_{ij}^{\text{L}} = -\dfrac{C_{\text{vdw}}}{r^6}$|
|Keesom coefficient|$C^{\text{K}} = \dfrac{(2)}{3}\dfrac{\mu_i^2 \mu_j^2}{kT}$|
|Debye coefficient|$C^{\text{D}} = \alpha_i \mu_j^2 + \alpha_j \mu_i^2$|
|London coefficient|$C^{\text{L}} = \dfrac{3}{2}\alpha_i \alpha_j\dfrac{I_i I_j}{I_i + I_j}$|

### Repulsive potentials

|Description|Equations (SI unit)|
|-:|:-|
|Hard sphere model|$\Gamma = \begin{cases} 0 & r > \sigma \\\ \infty & r \le \sigma \end{cases}$|
|Surtherland model|$\Gamma = \begin{cases} -\dfrac{C_{\text{vdw}}}{r^6} & r > \sigma \\\ \infty & r \le \sigma \end{cases}$|
|Lennard-Jones potential|$\Gamma = \dfrac{C_{\text{rep}}}{r^{12}} - \dfrac{C_{\text{vdw}}}{r^6}$|
|Lennard-Jones potential|$\Gamma = 4\varepsilon \left[ \left(\dfrac{\sigma}{r}\right)^{12} - \left(\dfrac{\sigma}{r}\right)^6 \right]$|

## Equations of State

### Principle of corresponding states

|Description|Equations|
|-:|:-|
|Ideal gas law|$Pv = RT$|
|Compressibility factor|$z = \dfrac{Pv}{RT}$|
|Reduced temperature|$T_r = \dfrac{T}{T_c}$|
|Reduced pressure|$P_r = \dfrac{P}{P_c}$|
|Pitzer acentric factor|$\omega = -1 - \log_{10} [P_r^{\text{sat}}(T_r = 0.7)]$|
|Generalized compressibility|$z = z^{(0)} + \omega z^{(1)}$|

### Cubic EOS

#### van der Waals EOS

|Description|Equations|
|-:|:-|
|van der Waals EOS <br/> (pressure explicit form)|$P = \dfrac{RT}{v-b} - \dfrac{a}{v^2}$|
|van der Waals EOS <br/> (cubic form)|$Pv^3 - (RT + Pb)v^2 + av - ab = 0$|
|van der Waals EOS <br/> (reduced form)|$P = \dfrac{8T_r}{3v_r - 1} - \dfrac{3}{v_r^2}$|
|Intermolecular force (pressure) correction|$a = \dfrac{27}{64}\dfrac{(RT_c)^2}{P_c}$|
|Volume correction|$b = \dfrac{RT_c}{8P_c}$|
|Critical compressibility factor|$z_c = \frac{3}{8}$|

#### Redlich-Kwong EOS

|Description|Equations|
|-:|:-|
|Redlich-Kwong EOS|$P = \dfrac{RT}{v-b} - \dfrac{a}{\sqrt{T}v(v+b)}$|
|Intermolecular force (pressure) correction|$a = 0.42748 \dfrac{R^2 T_c^{2.5}}{P_c}$|
|Volume correction|$b = 0.08664 \dfrac{RT_c}{P_c}$|
|Critical compressibility factor|$z_c = \frac{1}{3}$|

#### Peng-Robinson EOS

|Description|Equations|
|-:|:-|
|Peng-Robinson EOS|$P = \dfrac{RT}{v-b} - \dfrac{a \alpha(T)}{v(v+b) + b(v-b)}$|
|Intermolecular force (pressure) correction|$a = 0.45724 \dfrac{R^2 T_c^{2}}{P_c}$|
|Volume correction|$b = 0.07780 \dfrac{RT_c}{P_c}$|
|Constant|$\alpha(T) = [1 + \kappa(1 - \sqrt{T_r})]^2$|
|Constant|$\kappa = 0.37464 + 1.54226\omega - 0.26992\omega^2$|
|Critical compressibility factor|$z_c = 0.307$|

### Virial EOS

|Description|Equations|
|-:|:-|
|Virial EOS|$z = \dfrac{Pv}{RT} = 1 + \dfrac{B}{v} + \dfrac{C}{v^2} + \dfrac{D}{v^3} + \cdots$|
|Second virial coefficient|$B = \dfrac{RT_c B_r}{P_c}$|
|Reduced second virial coefficient|$B_r = B^{(0)} + \omega B^{(1)}$|
|0th order correction|$B^{(0)} = 0.083 - \dfrac{0.422}{T_r^{1.6}}$|
|1st order correction|$B^{(1)} = 0.139 - \dfrac{0.172}{T_r^{4.2}}$|

### Mixing rules of EOS parameters

#### Cubic EOS

|Description|Equations|
|-:|:-|
|$a$ for binary mixtures|$a_{\text{mix}} = y_1^2 a_1 + 2 y_1y_2 a_{12} + y_2^2 a_2$|
|$a$ of different species interaction|$a_{12} = \sqrt{a_1 a_2}(1 - k_{12})$|
|$b$ for binary mixtures|$b_{\text{mix}} = y_1b_1 + y_2b_2$|
|$a$ for multicomponent mixtures|$a_{\text{mix}} = \sum\limits_i\sum\limits_j y_i y_j a_{ij}$|
|$b$ for multicomponent mixtures|$b_{\text{mix}} = \sum\limits_i y_i b_{i}$|

#### Virial EOS

|Description|Equations|
|-:|:-|
|Second virial coefficient for binary mixture|$B_{\text{mix}} = y_1^2 B_{11} + 2 y_1 y_2 B_{12} + y_2^2 B_{22}$|
|Second virial coefficient for multicomponent mixture|$B_{\text{mix}} = \sum\limits_i\sum\limits_j y_i y_j B_{ij}$|
|Third virial coefficient for multicomponent mixture|$C_{\text{mix}} = \sum\limits_i\sum\limits_j\sum\limits_k y_i y_j y_k C_{ijk}$|

#### Principle of corresponding state

|Description|Equations|
|-:|:-|
|Pseudocritical temperature|$T_{pc} = \sum y_i T_{c, i}$|
|Pseudocritical pressure|$P_{pc} = \sum y_i P_{c, i}$|
|Pseudocritical acentric factor|$\omega_{pc} = \sum y_i \omega_{c, i}$|

### EOS for liquids and solids

|Description|Equations|
|-:|:-|
|Thermal expansion coefficient|$\beta = \dfrac{1}{v} \left(\dfrac{\partial v}{\partial T}\right)_P$|
|Isothermal compressibility|$\kappa = -\dfrac{1}{v} \left(\dfrac{\partial v}{\partial P}\right)_T$|
|Rackett equation|$v_l^{\text{sat}} = \dfrac{RT_c}{P_c} (0.29056 - 0.08775 \omega)^{(1 + (1 - T_r)^{2/7})}$|

## Thermodynamic Relations

### Mathematical Relations

|Description|Equations|
|-:|:-|
|Total differential|$dz = \left(\dfrac{\partial z}{\partial x}\right)_y dx + \left(\dfrac{\partial z}{\partial y}\right)_x dy$|
|Clairaut's theorem <br/> Symmetry of second derivative|$\dfrac{\partial}{\partial x} \left(\dfrac{\partial z}{\partial y} \right) = \dfrac{\partial}{\partial y} \left( \dfrac{\partial z}{\partial x} \right)$|
|Chain rule|$\dfrac{\partial z}{\partial x} = \dfrac{\partial z}{\partial y}\dfrac{\partial y}{\partial x}$|
|Cyclic relation <br/> Triple chain rule|$\left(\dfrac{\partial x}{\partial y}\right)_z \left(\dfrac{\partial y}{\partial z}\right)_x \left(\dfrac{\partial z}{\partial x}\right)_y = -1$|

### Thermodynamic Relations

|Relations|Internal energy $u$|Enthalpy $h$|Helmholz energy $a$|Gibbs energy $g$|
|-:|:-|:-|:-|:-|
|Definition|-|$h = u + Pv$|$a = u - Ts$|$g = h - Ts$|
|Fundamental property relations|$du = Tds - Pdv$|$dh = Tds + vdP$|$da = -sdT - Pdv$|$dg = -sdT + vdP$|
|Fundamental grouping|$\lbrace u, s, v \rbrace$|$\lbrace h, s, P \rbrace$|$\lbrace a, T, v \rbrace$|$\lbrace g, T, P \rbrace$|
|Fundamental grouping relations|$\left(\frac{\partial u}{\partial s}\right)_v = T$|$\left(\frac{\partial h}{\partial s}\right)_P = T$|$\left(\frac{\partial a}{\partial T}\right)_v = -s$|$\left(\frac{\partial g}{\partial T}\right)_P = -s$|
|Fundamental grouping relations|$\left(\frac{\partial u}{\partial v}\right)_s = -P$|$\left(\frac{\partial h}{\partial P}\right)_s = v$|$\left(\frac{\partial a}{\partial v}\right)_T = -P$|$\left(\frac{\partial g}{\partial P}\right)_T = v$|
|Maxwell's relations|$\left(\frac{\partial T}{\partial v}\right)_s = -\left(\frac{\partial P}{\partial s}\right)_v$|$\left(\frac{\partial T}{\partial P}\right)_s = \left(\frac{\partial v}{\partial s}\right)_P$|$\left(\frac{\partial s}{\partial v}\right)_T = \left(\frac{\partial P}{\partial T}\right)_v$|$\left(\frac{\partial s}{\partial P}\right)_T = -\left(\frac{\partial v}{\partial T}\right)_P$|

{{< image src="/cheme/cheme-326-thermodynamic-relations.png" caption="Thermodynamic relations. (Engineering and Chemical Thermodynamics 2e by Koretsky p274.)" >}}

### Measurable properties

|Description|Equations|
|-:|:-|
|Constant volume heat capacity|$c_v = \left(\dfrac{\partial u}{\partial T}\right)_v = T \left(\dfrac{\partial s}{\partial T}\right)_v$|
|Constant pressure heat capacity|$c_P = \left(\dfrac{\partial h}{\partial T}\right)_P = T \left(\dfrac{\partial s}{\partial T}\right)_P$|
|Constant volume heat capacity of real gas|$c_v^{\text{real}} = c_v^{\text{ideal}} + \displaystyle\int_{v_{\text{ideal}}}^{v_{\text{real}}} \left[T \left(\dfrac{\partial^2 P}{\partial T^2}\right)_v\right] dv$|
|Constant pressure heat capacity of real gas|$c_P^{\text{real}} = c_P^{\text{ideal}} - \displaystyle\int_{P_{\text{ideal}}}^{P_{\text{real}}} \left[T \left(\dfrac{\partial^2 v}{\partial T^2}\right)_P\right] dP$|
|Thermal expansion coefficient|$\beta = \dfrac{1}{v} \left(\dfrac{\partial v}{\partial T}\right)_P$|
|Thermal expansion coefficient of ideal gas|$\beta = \dfrac{1}{T}$|
|Isothermal compressibility|$\kappa = -\dfrac{1}{v} \left(\dfrac{\partial v}{\partial P}\right)_T$|
|Isothermal compressibility of ideal gas|$\kappa = \dfrac{1}{P}$|

### Property changes

|Description|Equations|
|-:|:-|
|Entropy change $s(T, v)$|$ds = \dfrac{c_v}{T} dT + \left(\dfrac{\partial P}{\partial T}\right)_v dv$|
|Entropy change $s(T, P)$|$ds = \dfrac{c_P}{T} dT + \left(\dfrac{\partial v}{\partial T}\right)_P dP$|
|Internal energy change $u(T, v)$|$du = c_v dT + \left[T \left(\dfrac{\partial P}{\partial T}\right)_v - P\right] dv$|
|Enthalpy change $h(T, P)$|$dh = c_P dT + \left[-T \left(\dfrac{\partial v}{\partial T}\right)_P + v\right] dP$|

### Property changes $(T, P)$

|General $f(T, P)$|Ideal gas $\beta = \frac{1}{T}, \kappa = \frac{1}{P}$|
|:-|:-|
|$ds = \dfrac{c_P}{T} dT - \beta v \ dP$|$ds = \dfrac{c_P}{T} dT - \dfrac{R}{P} dP$|
|$dv = \beta v \ dT - \kappa v \ dP$|$dv = \dfrac{v}{T}dT - \dfrac{v}{P}dP$|
|$du = (c_P - \beta Pv)dT + (\kappa Pv - \beta vT)dP$|$du = (c_P - R)dT$|
|$dh = (c_P - \beta Pv)dT + v \ dP$|$dh = c_P \ dT$|
|$da = -s \ dT + (\kappa Pv - \beta vT)dP$|$da = -s \ dT$|
|$dg = -s \ dT + v \ dP$|$dg = -s \ dT + v \ dP$|

### Departure functions

|Description|Equations|
|-:|:-|
|General departure function|$\mathrm{dep = real - ideal}$|
|Enthalpy departure function|$\Delta h^{\text{dep}} = h^{\text{real}} - h^{\text{ideal}}$|
|Entropy departure function|$\Delta s^{\text{dep}} = s^{\text{real}} - s^{\text{ideal}}$|
|Dimensionless enthalpy departure function|$\dfrac{\Delta h^{\text{dep}}}{RT_c} = T_r^2 \displaystyle\int_0^P \left[-\dfrac{1}{P_r}\left(\dfrac{\partial z}{\partial T_r}\right)_P \right] dP_r$|
|Dimensionless entropy departure function|$\dfrac{\Delta s^{\text{dep}}}{R} = \displaystyle\int_0^P -\left[\dfrac{z-1}{P_r} + \dfrac{T_r}{P_r}\left(\dfrac{\partial z}{\partial T_r}\right)_P \right] dP_r$|
|Dimensionless enthalpy departure function with Lee-Kesler EOS|$\dfrac{\Delta h^{\text{dep}}}{RT_c} = \left[\dfrac{\Delta h^{\text{dep}}}{RT_c}\right]^{(0)} + \omega \left[\dfrac{\Delta h^{\text{dep}}}{RT_c}\right]^{(1)}$|
|Dimensionless entropy departure function with Lee-Kesler EOS|$\dfrac{\Delta s^{\text{dep}}}{R} = \left[\dfrac{\Delta s^{\text{dep}}}{R}\right]^{(0)} + \omega \left[\dfrac{\Delta s^{\text{dep}}}{R}\right]^{(1)}$|

### Joule-Thomson Expansion

|Description|Equations|
|-:|:-|
|**Joule-Thomson expansion** <br/> Adiabatic reversible throttling|$\dot{q} = 0 \newline \dot{w}_s = 0 \newline \Delta h = 0$|
|Joule-Thomson coefficient|$\mu_{\text{JT}} = \left(\dfrac{\partial T}{\partial P}\right)_h$|
|Joule-Thomson coefficient|$\mu_{\text{JT}} = \dfrac{\left[-T \left(\dfrac{\partial v}{\partial T}\right)_P + v\right]}{c_P^{\text{real}}}$|

## Phase Equilibria

### Single-component equilibrium

|Description|Equations|
|-:|:-|
|Gibbs free energy|$g = h - Ts$|
|Second law of thermodynamics|$dG_i \le 0$|
|Criteria for chemical equilibrium|$g_i^\alpha = g_i^\beta$|
|**Clapeyron equation** <br/> General phase equilibrium|$\dfrac{dP}{dT} = \dfrac{\Delta s}{\Delta v} = \dfrac{\Delta h}{T\Delta v}$|
|**Clausius-Clapeyron equation** <br/> ★ Vapor-liquid equilibrium <br/> ★ Ideal gas, negligible liquid volume|$\dfrac{dP^{\text{sat}}}{P^{\text{sat}}} = \dfrac{\Delta h_{\text{vap}} dT}{RT^2}$|
|**Clausius-Clapeyron equation** <br/> ★ Vapor-liquid equilibrium <br/> ★ Ideal gas, negligible liquid volume <br/> ★ $\Delta h_{\text{vap}}$ independent of $T$|$\ln\dfrac{P_2^{\text{sat}}}{P_1^{\text{sat}}} = -\dfrac{\Delta h_{\text{vap}}}{R} \left(\dfrac{1}{T_2} - \dfrac{1}{T_1}\right)$|
|Antoine's equation|$\ln P^{\text{sat}} = A - \dfrac{B}{C+T}$|

### Properties of mixtures

|Description|Equations|
|-:|:-|
|Extensive total solution (mixture) property|$K$|
|Intensive total solution (mixture) property|$k = \dfrac{K}{n}$|
|Extensive pure species property|$K_i$|
|Intensive pure species property|$k_i = \dfrac{K_i}{n_i}$|
|Partial molar property|$\overline{K}\_i = \left(\dfrac{\partial K}{\partial n_i}\right)\_{T, P, n_{j\not= i}}$|
|Limiting case of partial molar property|$\displaystyle\lim_{x_i \to 1} \overline{K}_i = k_i \newline \lim_{x_i \to 0} \overline{K}_i = \overline{K}_i^\infty$|
|Differential of extensive property|$dK = \left(\frac{\partial K}{\partial T}\right)\_{P, n_i} dT + \left(\frac{\partial K}{\partial P}\right)\_{T, n_i} dP + \sum \overline{K}\_i dn_i$|
|Relation between properties <br/> ★ Constant T, P|$K = \sum n_i \overline{K}_i \newline k = \sum x_i \overline{K}_i$|
|**Gibbs-Duhem equation** <br/> ★ Constant T, P|$\sum n_i d\overline{K}_i = 0$|
|Corollary of Gibbs-Duhem equation <br/> ★ Binary mixture|$x_1 \dfrac{d\overline{K_1}}{x_1} + x_2 \dfrac{d\overline{K_2}}{x_1} = 0$|

### Property changes of mixtures

|Description|Equations|
|-:|:-|
|Extensive property change of mixing|$\Delta K_{\text{mix}} = K - \sum n_i k_i \newline \Delta K_{\text{mix}} = \sum n_i (\overline{K}_i - k_i)$|
|Intensive property change of mixing|$\Delta k_{\text{mix}} = k - \sum x_i k_i \newline \Delta k_{\text{mix}} = \sum x_i (\overline{K}_i - k_i)$|
|Enthalpy of mixing|$\Delta h_{\text{mix}} = \sum x_i (\overline{h}_i - h_i)$|
|Enthalpy of mixing|$\Delta h_{\text{mix}} = \dfrac{\Delta \tilde{h}\_s}{n+1} = \Delta \tilde{h}\_s x_1$|
|Enthalpy of solution|$\Delta \tilde{h}\_s = \dfrac{\Delta h_{\text{mix}}}{x_1} = \Delta h_{\text{mix}}(n+1)$|
|Entropy of mixing <br/> ★ Ideal gas, regular solution|$\Delta s_{\text{mix}} = -R\sum y_i \ln y_i$|
|Partial molar property change of mixing|$\overline{\Delta K}_{\text{mix}, i} = \overline{K}_i - k_i$|

### Determination of partial molar properties

|Description|Equations|
|-:|:-|
|Partial molar volume of species 1 <br/> ★ Virial EOS|$\overline{V}\_1 = \dfrac{RT}{P} + (y_1^2 + 2y_1 y_2)B_{11} + 2y_2^2 B_{12} - y_2^2 B_{22}$|
|Partial molar volume of species 2 <br/> ★ Virial EOS|$\overline{V}\_2 = \dfrac{RT}{P} - y_1^2 B_{11} + 2y_1^2 B_{12} + (y_2^2 + 2y_1 y_2)B_{22}$|
|Volume change of mixing <br/> ★ Virial EOS|$\Delta v_{\text{mix}} = y_1 y_2(2B_{12} - B_{11} - B_{22})$|
|Partial molar property|$\overline{K}\_i = k_i + \overline{\Delta K}_{\text{mix}, i}$|
|Graphical method <br/> Slope is difference|$\dfrac{dk}{dx_1} = \overline{K}_1 - \overline{K}_2$|
|Graphical method <br/> $\overline{K}_2$ is intercept|$k = x_1 \dfrac{dk}{dx_1} + \overline{K}_2$|
|Graphical method <br/> $\overline{K}_2$ explicit|$\overline{K}_2 = k - x_1 \dfrac{dk}{dx_1}$|

### Multicomponent equilibrium

|Description|Equations|
|-:|:-|
|Chemical potential|$\mu_i = \overline{G}\_i = \left(\dfrac{\partial G}{\partial n_i}\right)\_{T, P, n_{j \not= i}}$|
|Criteria for chemical equilibrium|$\mu_i^\alpha = \mu_i^\beta$|
|General multicomponent equilibrium|$\Delta \left[ -\dfrac{\overline{H}\_i}{T^2}dT - \dfrac{\overline{V}\_i}{T}dP + \dfrac{1}{T} \left[\dfrac{\partial \mu_i}{\partial x_i}\right]\_{T, P} dx_i \right] = 0$|
|Vapor liquid equilibrium <br/> ★ Ideal gas|$\begin{aligned} &-\dfrac{h\_i^v}{T^2}dT - R\dfrac{dP}{P} + R\dfrac{dx_i^v}{x_i^v} = -\dfrac{\overline{H}\_i^l}{T^2}dT - \dfrac{\overline{V}\_i^l}{T}dP + \dfrac{1}{T} \left[\dfrac{\partial \mu_i^l}{\partial x_i}\right]\_{T, P} dx_i \end{aligned}$|

<!-- ★ -->
