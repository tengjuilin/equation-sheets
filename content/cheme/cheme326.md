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

<!-- ★ -->
