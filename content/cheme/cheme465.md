---
title: "CHEM E 465 Reactor Design"
date: 2022-11-03T00:00:00-08:00
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

1. Reactor design equation (mole balance): $r_i = f(n) = f(X)$
2. Rate law: $r_i = f(C_i)$
3. Stoichiometry: $C_i = f(X)$
4. Combine: $r_i = f(X)$

|Description|Equations|
|-:|:-|
|General mole balance|$\begin{aligned}&\mathrm{in} &&- \mathrm{out} &&+ \mathrm{generation} &&= \mathrm{accumulation} \\\ &\dot{n}\_{i0} &&- \dot{n}\_i &&+ G_i &&= \dfrac{dn_i}{dt}\end{aligned}$|
|General generation term|$G_i = \int r_i dV$|
|Spatially uniform generation term|$G_i = r_i V$|
|Conversion|$X_i \equiv X = \dfrac{n_{i0} - n_{i}}{n_{i0}} = \dfrac{\dot{n}\_{i0} - \dot{n}\_{i}}{\dot{n}\_{i0}}$|
|Mole/flow rate in terms of conversion|$n_i = n_{i0} (1 - X) \newline \dot{n}\_i = \dot{n}\_{i0} (1 - X)$|
|Heterogeneous reaction rate|$r_i = \rho_b r_i'$|

|Reactor|Design Equations|Integral Form|
|-:|:-|:-|
|**Batch** <br/> ★ Perfectly mixed|$\begin{aligned}r_i V = \dfrac{dn_i}{dt} = -n_{i0}\dfrac{dX}{dt}\end{aligned}$|$\begin{aligned}t = \displaystyle\int_{n_{i1}}^{n_{i0}} \dfrac{dn_i}{-r_i V} = n_{i0} \displaystyle\int_0^X \dfrac{dX}{-r_i V}\end{aligned}$|
|**CSTR** <br/> ★ Perfectly mixed, steady-state|$V = \dfrac{\dot{n}\_{i0} - \dot{n}\_i}{-r_i} = \dfrac{\dot{n}\_{i0}X}{-r_i}$|-|
|**PFR** <br/> ★ Steady state <br/> ★ Plug flow, no radial dependence|$r_i = \dfrac{d\dot{n}\_i}{dV} = -\dot{n}\_{i0}\dfrac{dX}{dV}$|$V = \displaystyle\int_{\dot{n}\_i}^{\dot{n}\_{i0}}\dfrac{d\dot{n}\_i}{-r_i} = \dot{n}\_{i0} \displaystyle\int_0^X \dfrac{dX}{-r_i}$|
|**PBR** <br/> ★ Steady state|$r_i\' = \dfrac{d\dot{n}\_i}{dm} = -\dot{n}\_{i0}\dfrac{dX}{dm}$|$m = \displaystyle\int_{\dot{n}\_i}^{\dot{n}\_{i0}}\dfrac{d\dot{n}\_i}{-r_i\'} = \dot{n}\_{i0} \displaystyle\int_0^X \dfrac{dX}{-r_i\'}$|
|**Semi-batch reactor**|$r_i = \dfrac{\dfrac{dn_i}{dt} - \dot{n}\_{i0}}{V(t)}$|-|

### Levenspiel plot

|Description|Equations|
|-:|:-|
|Levenspiel plot|$\dfrac{\dot{n}\_{i0}}{-r_i}$ vs. $X$|
|CSTR volume|$V = \dfrac{\dot{n}\_{i0}X}{-r_i}$ = Area of rectangle|
|PFR volume|$V = \dot{n}\_{i0} \displaystyle\int_0^X \dfrac{dX}{-r_i}$ = Area under Levenspiel plot|
|Reaction of order > 0|$V_{\mathrm{CSTR}} > V_\mathrm{PFR}$ (Choose PFR)|
|Reaction of order < 0|$V_{\mathrm{CSTR}} < V_\mathrm{PFR}$ (Choose CSTR)|

### Reactor choice

|Reactor Type|Advantage|Disadvantage|
|-:|:-|:-|
|Batch|- High conversion|- High labor cost and downtime <br/> - Difficult to scale up <br/> - Batch-to-batch variability|
|CSTR|- Good T control|- Hard to get high conversion|
|PFR|- Easy maintenance <br/> - High conversion per unit volume|- Difficult for T control|

## Stoichiometry

### Stoichiometric table

|Species|Initial|Change|Remaining|
|-:|:-|:-|:-|
|$\ce{A}$|$n_{{A}0}$|$-n_{A0}X$|$n_A = n_{A0}(1-X)$|
|$\ce{B}$|$n_{B0}$|$-\frac{b}{a}n_{A0}X$|$n_B = n_{A0}(\Theta_B - \frac{b}{a}X)$|
|$\ce{C}$|$n_{C0}$|$\frac{c}{a}n_{A0}X$|$n_C = n_{A0}(\Theta_C + \frac{c}{a}X)$|
|$\ce{D}$|$n_{D0}$|$\frac{d}{a}n_{A0}X$|$n_D = n_{A0}(\Theta_D + \frac{d}{a}X)$|
|$\ce{I}$|$n_{I0}$|$0$|$n_I = n_{I0}$|
|Total|$n_{T0}$|$\delta n_{A0}X$|$n_T = n_{T0} + \delta n_{A0}X$|

|Description|Equations|
|-:|:-|
|Sample reaction|$\color{blue}\ce{A + \dfrac{b}{a} B -> \dfrac{c}{a}C + \dfrac{d}{a}D}$|
|$\dfrac{\text{total mol change}}{\text{mol A reacted}}$|$\delta = \sum \nu_i = \dfrac{d}{a} + \dfrac{c}{a} - \dfrac{b}{a} - 1$|
|$\dfrac{\text{mol Z initially}}{\text{mol A initially}}$|$\Theta_Z = \dfrac{n_{Z0}}{n_{A0}} = \dfrac{\dot{n}\_{Z0}}{\dot{n}\_{A0}}= \dfrac{y_{Z0}}{y_{A0}}= \dfrac{C_{Z0}}{C_{A0}}$|
|$\dfrac{\text{total mol change for } X = 1}{\text{mol feed}}$|$\varepsilon = y_{A0}\delta = \dfrac{\dot{n}\_{Tf} - \dot{n}\_{T0}}{\dot{n}\_{T0}}$|
|Concentration|$C_i = \dfrac{n_i}{V} = \dfrac{\dot{n}_i}{\dot{V}}$|
|Molar fraction|$y_i = \dfrac{\dot{n}\_i}{\dot{n}\_T}$|
|Pressure ratio|$p = \dfrac{P}{P_0}$|

|Description|Equations|
|-:|:-|
|Molar flow rate|$\dot{n}\_i = \dot{n}\_{A0} (\Theta_i - \nu_i X)$|
|Concentration <br/> ★ Constant $PVT$|$C_i = C_{A0} (\Theta_i - \nu_i X)$|
|Volumetric flow rate|$\begin{aligned}\dot{V} &= \dot{V}_0 \left(\dfrac{\dot{n}\_T}{\dot{n}\_{T0}}\right) \left(\dfrac{P_0}{P}\right) \left(\dfrac{T}{T_0}\right) \\\ &= \dot{V}_0 (1 + \varepsilon X)\left(\dfrac{P_0}{P}\right) \left(\dfrac{T}{T_0}\right) \end{aligned}$|
|Concentration|$\begin{aligned}C_i &= \dfrac{\dot{n}\_i}{\dot{V}} \\\ &= C_{A0} \left(\dfrac{\dot{n}\_i}{\dot{n}\_{T}}\right) \left(\dfrac{P}{P_0}\right) \left(\dfrac{T_0}{T}\right) \\\ &= C_{A0} y_i p \left(\dfrac{T_0}{T}\right) \\\ &= \dfrac{C_{A0} (\Theta_i + \nu_i X)}{1+\varepsilon X} \left(\dfrac{P}{P_0}\right) \left(\dfrac{T_0}{T}\right) \end{aligned}$|

## Isothermal Reactor Design

### Batch reactor

|Description|Equations|
|-:|:-|
|Characteristic reaction time (1st order)|$t_R = \dfrac{1}{k}\ln\left(\dfrac{1}{1-X}\right)$|
|Characteristic reaction time (2nd order)|$t_R = \dfrac{1}{k C_{A0}}\dfrac{X}{1-X}$|
|Total time|Total = Fill + Heat + Reaction + Clean|

### CSTR

|Description|Equations|
|-:|:-|
|Space time|$\tau = \dfrac{V}{\dot{V}} = \dfrac{C_{A0}X}{-r_A}$|
|Damkohler number|$\begin{aligned}\mathrm{Da} &= \dfrac{-r_{A0}V}{\dot{n}\_{A0}} \\\ &= \dfrac{\text{rate at entrance}}{\text{molar flow at entrance}} \\\ &= \dfrac{\text{reaction rate}}{\text{convective mass transport rate}}\end{aligned}$|
|Damkohler number and conversion|$\mathrm{Da} < 0.1, X < 0.1 \newline \mathrm{Da} > 10, X > 0.9$|

|Reaction, Reactor|Damkohler number $\mathrm{Da}\_i$|Space time $\tau$|Conversion $X$|Concentration $C_i$|
|-:|:-|:-|:-|:-|
|1st order, single CSTR|$\begin{aligned}\tau k = \dfrac{X}{1-X}\end{aligned}$|$\dfrac{X}{k(1-X)}$|$\dfrac{\tau k}{1 + \tau k}$|$\dfrac{C_{A0}}{1 + \tau k}$|
|2nd order, single CSTR|$\tau k C\_{A0}$|$\dfrac{X}{kC_{A0}(1-X)^2}$|$\dfrac{1 + 2\mathrm{Da}_2 - \sqrt{1 + 4\mathrm{Da}_2}}{2\mathrm{Da}_2}$|$C_{A0} \dfrac{-1 + \sqrt{1 + 4\mathrm{Da}_2}}{2\mathrm{Da}_2}$|
|1st order, CSTR series|-|-|$1 - \dfrac{1}{(1 + \mathrm{Da}_1)^n}$|$\dfrac{C_{A0}}{(1 + \mathrm{Da}_1)^n}$|

### PFR

|Description|Equations|
|-:|:-|
|Reactor volume for 2nd order gas phase rxn|$V = \dfrac{\dot{V}\_{A0}}{kC_{A0}} \left[ 2\varepsilon(1 + \varepsilon) \ln(1-X) + \varepsilon^2 X + \dfrac{(1 + \varepsilon)^2 X}{1-X} \right]$|
|Ergun equation|$\dfrac{dP}{dz} = \dfrac{G}{\rho g_c D_P}\left(\dfrac{1 - \phi}{\phi^3}\right) \left[\dfrac{150(1-\phi)\mu}{D_P} + 1.75G\right]$|
|Porosity (void fraction)|$\phi = \dfrac{\text{void volume}}{\text{total bed volume}}$|
|PBR pressure drop|$\dfrac{dP}{dz} = -\beta_0 \left(\dfrac{P_0}{P}\right)\left(\dfrac{T}{T_0}\right)\left(\dfrac{\dot{n}_T}{\dot{n}\_{T0}}\right)$|
|Packed bed property|$\beta_0 = \dfrac{G(1-\phi)}{\rho_0 g_c D_P \phi^3}\left[\dfrac{150(1-\phi)\mu}{D_P} + 1.75G \right] [=] \mathrm{\dfrac{Pa}{m}}$|
|Bulk density of catalyst|$\rho_b = \rho_c(1-\phi)$|
|Catalyst mass|$m = (1-\phi)A_c z\rho_c = A_c z \rho_b$|
|Ergun equation for packed bed (multiple reaction)|$\dfrac{dp}{dm} = -\dfrac{\alpha}{2p}\dfrac{T}{T_0}\dfrac{\dot{n}\_T}{\dot{n}\_{T0}}$|
||$\alpha = \dfrac{2\beta_0}{A_c \rho_c (1-\phi)P_0} [=] \mathrm{kg^{-1}}$|
|Ergun equation for packed bed (single reaction)|$\dfrac{dp}{dm} = -\dfrac{\alpha}{2p} (1+\varepsilon X) \dfrac{T}{T_0}$|
|System of pressure and conversion ODEs|$\begin{cases}\dfrac{dX}{dm} = F_1(X, p) & \text{Reactor design} \\\ \dfrac{dp}{dm} = F_2(X, p) & \text{Ergun equation}\end{cases}$|
|Pressure ratio<br/> ★ $\varepsilon = 0$ or $\varepsilon X \ll 1$, isothermal|$p = \sqrt{1-\alpha m} = \sqrt{1 - \dfrac{2\beta_0}{P_0}z}$|
|Pressure drop in pipes|$p = \sqrt{1 - \alpha_p V}$|
|Pipe factor|$\alpha_p = \dfrac{4 f G^2}{A_c \rho_0 P_0 D}$|

## Rate law determination by data

### Batch reactors

|Description|Equations|
|-:|:-|
|Power law|$r_A = -k C_A^\alpha C_B^\beta$|
|Integral method|$\dfrac{dC_A}{dt} = -kC_A^\alpha$|
|0th order rxn|$C_A = C_{A0} - kt$|
|1st order rxn|$\ln\dfrac{C_{A0}}{C_A} = kt \\\ \ln C_A = \ln C_{A0} - kt$|
|2nd order rxn|$\dfrac{1}{C_A} = kt + \dfrac{1}{C_{A0}}$|
|Differential method|$\ln\left(-\dfrac{dC_A}{dt}\right) = \ln k_A + \alpha \ln C_A$|

### Differential reactors (PBR)

|Description|Equations|
|-:|:-|
||$-r_A' = \dfrac{\dot{V}\_0 C_{A0} - \dot{V} C_{AP}}{\Delta m} = \dfrac{\dot{V}\_{A0}X}{\Delta m} = \dfrac{\dot{V}\_P}{\Delta m}$|

## Multiple reactions

### Batch reactors

|Description|Equations|
|-:|:-|
|Parallel (competing) reactions|$\ce{A ->[\mathit{k}_1] B} \newline \ce{A ->[\mathit{k}_2] C}$|
|Series (consecutive) reactions|$\ce{A ->[\mathit{k}_1] B ->[\mathit{k}_2] C}$|
|Independent reactions|$\ce{A -> B + C} \newline \ce{D -> E + F}$|
|Complex reactions|$\ce{A + B -> C + D} \newline \ce{A + C -> E} \newline \ce{E -> G}$|

|Description|Equations|
|-:|:-|
|Instantaneous selectivity based on rate|$S_{D/U} = \dfrac{r_D}{r_U} = \dfrac{\text{rate of formation of D}}{\text{rate of formation of U}}$|
|Overall selectivity based on flow rate|$\tilde{S}\_{D/U} = \dfrac{\dot{n}\_D}{\dot{n}\_U} = \dfrac{n_D}{n_U} = \dfrac{\text{exit molar flow rate of D}}{\text{exit molar flow rate of U}}$|
|Selectivity of CSTR|$S_{D/U} = \tilde{S}\_{D/U}$|
|Instantaneous yield based on rate|$Y_D = -\dfrac{r_D}{r_A}$|
|Overall yield based on flow rate|$\tilde{Y}\_D = \dfrac{\dot{n}\_D}{\dot{n}\_{A0} - \dot{n}\_A} = \dfrac{n_D}{n_{A0} - n_A}$|
|Conversion of batch and flow reactor|$X_A = \dfrac{\dot{n}\_{A0} - \dot{n}\_{A}}{\dot{n}\_{A0}}$|
|Conversion of semi-batch reactor|$X_A = \dfrac{C_{A0} V_0 - C_A V}{C_{A0}V}$|
|Conversion of semi-batch reactor|$X_B = \dfrac{\dot{n}\_{B0} t - C_B V}{\dot{n}\_{B0} t}$|

### Parallel reactions

|Description|Equations|
|-:|:-|
|Concentration dependence of instantaneous selectivity|$S_{D/U} = \dfrac{r_D}{r_U} = \dfrac{k_D}{k_U}C_A^{\alpha_1 - \alpha_2}$|
|$\alpha_1 > \alpha_2$|$\uparrow C_A, \uparrow S_{D/U}$|
|$\alpha_1 < \alpha_2$|$\downarrow C_A, \uparrow S_{D/U}$|
|Temperature dependence of instantaneous selectivity|$S_{D/U} = \dfrac{r_D}{r_U} ~ \dfrac{k_D}{k_U} = \dfrac{A_D}{A_U}\exp\left(-\dfrac{E_D - E_U}{RT}\right)$|
|$E_D > E_U$|$\uparrow T, \uparrow S_{D/U}$|
|$E_D < E_U$|$\downarrow T, \uparrow S_{D/U}$|

## Enzymatic Reactions

|Description|Equations|
|-:|:-|
|Pseudo-steady-state hypothesis|$r_{A*} = \sum r_{i, A*} = 0$|

### Mechanism development

|Rate law|Mechanism (rule of thumb)|
|-:|:-|
|Species concentration in denominator|Species collision with active intermediate|
|Constant in denominator|Reaction of spontaneous decomposition of active intermediate|
|Species concentration in numerator|Species produce active intermediate|

### Michaelis-Menten kinetics

|Description|Equations|
|-:|:-|
|Overall reaction|$\ce{E + S -> E + P}$|
|Reaction mechanism|$\ce{S + E <=>[\mathit{k}\_1][\mathit{k}_\{-1}] ES} \newline \ce{ES + W ->[\mathit{k}\_{2}] P + E}$|
|Enzyme balance|$\ce{[E_T] = [E] + [ES]} \newline \ce{[E] = [E_T] - [ES]}$|
|Pseudo-steady-state approximation|$\begin{aligned}r_{\ce{ES}} &= k_1\ce{[S][E]} - k_{-1} \ce{[ES]} - k_2 \ce{[ES][W]} = 0 \\\ r_{\ce{ES}} &= k_1\ce{[S]([E_T] - [ES])} - k_{-1} \ce{[ES]} - k_2 \ce{[ES][W]} = 0 \end{aligned} \newline \ce{[ES]} = \dfrac{k_1 \ce{[S][E_T]}}{k_1 \ce{[S]} + k_{-1} + k_2 \ce{[W]}}$|
|Turnover number (# substrates converted to product per unit time on one enzyme at saturation)|$k_{\mathrm{cat}} = k_2 \ce{[W]}$|
|Michaelis-Menten constant (attraction of enzyme of its substrate, [Substrate] which rate of rxn is 1/2 max)|$K_M = \dfrac{k_{\mathrm{cat}} + k_{-1}}{k_1}$|
|Maximum rate|$V_{\max} = k_{\mathrm{cat}} \ce{[E_T]}$|
|**Michaelis-Menten equation** <br/> Rate of reaction|$\begin{aligned}r_{\ce{P}} &= k_{2} \ce{[ES][W]} \\\ &= \dfrac{k_1 k_{2} \ce{[S][E_T][W]}}{k_1 \ce{[S]} + k_{-1} + k_2 \ce{[W]}} \\\ &= \dfrac{k_{\mathrm{cat}} \ce{[S][E_T]}}{K_M + \ce{[S]}} \\\ &= \dfrac{V_{\max} \ce{[S]}}{K_M + \ce{[S]}} \end{aligned}$|
|**Lineweaver-Burk equation**|$\dfrac{1}{r_{\ce{P}}} = \dfrac{K_M}{V_{\max}}\dfrac{1}{\ce{[S]}} + \dfrac{1}{V_{\max}}$|
|Eadie-Hofstee equation|$r_{\ce{P}} = V_{\max} - K_M\dfrac{r_{\ce{P}}}{\ce{[S]}}$|
|Hanes-Woolf equation|$\dfrac{\ce{[S]}}{r_{\ce{P}}} = \dfrac{K_M}{V_{\max}} + \dfrac{1}{V_{\max}}\ce{[S]}$|

### Product-enzyme complex

|Description|Equations|
|-:|:-|
|Overall reaction|$\ce{E + S -> E + P}$|
|Reaction mechanism|$\ce{S + E <=> ES <=> PE <=> P + E}$|
|Briggs-Haldane equation|$r_{\ce{P}} = \dfrac{V_{\max}(\ce{[S]} - \ce{[P]} / K_C)}{\ce{[S]} + K_{\max} + K_P \ce{[P]}}$|

### Batch enzymatic reactor

|Description|Equations|
|-:|:-|
|Time |$\begin{aligned}t &= \dfrac{K_M}{V_{\max}}\ln\left(\dfrac{\ce{[A]_0}}{\ce{[A]}}\right) + \dfrac{\ce{[A]\_0 - [A]}}{V\_{\max}} \\\ &= \dfrac{K_M}{V\_{\max}} \ln\left(\dfrac{1}{1-X}\right) + \dfrac{\ce{[A]_0}X}{V\_{\max}} \end{aligned}$|
|Linearized form|$\dfrac{1}{t} \ln\left(\dfrac{\ce{[A]_0}}{\ce{[A]}}\right) = \dfrac{V\_{\max}}{K_M} - \dfrac{\ce{[A]_0 - [A]}}{K_M t}$|

### Enzymatic inhibition

#### Competitive inhibition

|Description|Equations|
|-:|:-|
|Reaction mechanism|$\ce{E + S <=> ES} \newline \ce{ES -> E + P} \newline \ce{E + I <=> EI} \text{ (inactive)}$|
|Reaction rate|$r_{\ce{P}} = \dfrac{V_{\max}\ce{[S]}}{\ce{[S]} + K_M \left[1 + \dfrac{\ce{[I]}}{K_I}\right]}$|
|Lineweaver-Burk form <br/> $\uparrow K_I, \uparrow \text{slope}$|$\dfrac{1}{r_{\ce{P}}} = \dfrac{1}{\ce{[S]}} \left[\dfrac{K_M}{V_{\max}} \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right] \right] + \dfrac{1}{V_{\max}}$|

#### Uncompetitive inhibition

|Description|Equations|
|-:|:-|
|Reaction mechanism|$\ce{E + S <=> ES} \newline \ce{ES -> E + P} \newline \ce{ES + I <=> ESI} \text{ (inactive)}$|
|Reaction rate|$r_{\ce{P}} = \dfrac{V_{\max}\ce{[S]}}{K_M + \ce{[S]} \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right]}$|
|Lineweaver-Burk form <br/> $\uparrow K_I, \uparrow \text{intercept}$|$\dfrac{1}{r_{\ce{P}}} = \dfrac{1}{\ce{[S]}} \dfrac{K_M}{V_{\max}} + \dfrac{1}{V_{\max}} \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right]$|

#### Noncompetitive (mixed) inhibition

|Description|Equations|
|-:|:-|
|Reaction mechanism|$\ce{E + S <=> ES} \newline \ce{ES -> E + P} \newline \ce{E + I <=> EI} \text{ (inactive)} \newline \ce{ES + I <=> ESI} \text{ (inactive)} \newline \ce{S + EI <=> ESI} \text{ (inactive)}$|
|Reaction rate|$r_{\ce{P}} = \dfrac{V_{\max}\ce{[S]}}{(\ce{[S]} + K_M) \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right]}$|
|Lineweaver-Burk form <br/> $\uparrow K_I, \uparrow \text{slope}, \uparrow \text{intercept}$|$\dfrac{1}{r_{\ce{P}}} = \dfrac{1}{\ce{[S]}} \dfrac{K_M}{V_{\max}} \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right] + \dfrac{1}{V_{\max}} \left[ 1 + \dfrac{\ce{[I]}}{K_I}\right]$|

## Catalytic Reactions

### Reaction mechanisms

|Reaction|Mechanism|Rate Law|
|-:|:-|:-|
|Adsorption|$\ce{A + ^* <=> A^*}$|$r_{\ce{A}} = k_{\ce{A}}\left[P_{\ce{A}} \ce{[^\*] - \dfrac{\ce{[A^*]}}{K_{\ce{A}}}}\right]$|
|Desorption|$\ce{A^* <=> A + ^*}$|$r_{\ce{D}} = k_{\ce{D}}\left[\ce{[A^*] - \dfrac{P_{\ce{A}} \ce{[^\*]}}{K_{\ce{D}}}}\right]$|
|Single site surface rxn|$\ce{A^* <=>[\mathit{k}\_S][\mathit{k}_{-S}] B^*}$|$r\_{\ce{S}} = k_{\ce{S}} \left[\ce{[A^\*]} - \dfrac{\ce{[B^*]}}{K_{\ce{S}}}\right]$|
|Dual site (I) surface rxn|$\ce{A^* + ^* <=>[\mathit{k}\_S][\mathit{k}_{-S}] B^* + ^*}$|$r\_{\ce{S}} = k_{\ce{S}} \left[\ce{[A^\*][^\*]} - \dfrac{\ce{[B^*][^\*]}}{K_{\ce{S}}}\right]$|
|Dual site (II) surface rxn|$\ce{A^* + B^* <=>[\mathit{k}\_S][\mathit{k}_{-S}] C^* + D^*}$|$r\_{\ce{S}} = k_{\ce{S}} \left[\ce{[A^\*][B^\*]} - \dfrac{\ce{[C^*][D^\*]}}{K_{\ce{S}}}\right]$|
|Dual site (III) surface rxn|$\ce{A^* + B^{\*}\' <=>[\mathit{k}\_S][\mathit{k}_{-S}] C^{\*}\' + D^*}$|$r\_{\ce{S}} = k_{\ce{S}} \left[\ce{[A^\*][B^{\*}\']} - \dfrac{\ce{[C^{\*}\'][D^\*]}}{K_{\ce{S}}}\right]$|
|Eley-Rideal surface rxn|$\ce{A^* + B (g) <=>[\mathit{k}\_S][\mathit{k}_{-S}] C^{\*}}$|$r\_{\ce{S}} = k_{\ce{S}} \left[\ce{[A^\*]} P_{\ce{B}} - \dfrac{\ce{[C^{\*}]}}{K_{\ce{S}}}\right]$|

<!-- ★ -->