---
title: "CHEM E 467 Biochemical Engineering"
date: 2023-04-29T00:00:00-08:00
---

## Enzyme Kinetics

|Description|Equations|
|-:|:-|
|Arrhenius equation|$k = A\exp\left(\dfrac{E_A}{RT}\right)$|
|Power law|$r_P = k\prod C_i^{\nu_i}$|
|Linearized 1st order rate law|$\ln\left(\dfrac{[A]}{[A]_0}\right) -kt$|

### Michaelis-Menten kinetics

|Description|Equations|
|-:|:-|
|Overall reaction|$\ce{E + S -> E + P}$|
|Reaction mechanism|$\ce{S + E <=>[\mathit{k}\_1][\mathit{k}_\{-1}] ES} \newline \ce{ES ->[\mathit{k}\_{2}] P + E}$|
|Enzyme balance|$\ce{[E_T] = [E] + [ES]} \newline \ce{[E] = [E_T] - [ES]}$|
|Pseudo-steady-state approximation|$\begin{aligned}r_{\ce{ES}} &= k_1\ce{[S][E]} - k_{-1} \ce{[ES]} - k_2 \ce{[ES]} = 0 \\\ r_{\ce{ES}} &= k_1\ce{[S]([E_T] - [ES])} - k_{-1} \ce{[ES]} - k_2 \ce{[ES]} = 0 \end{aligned} \newline \ce{[ES]} = \dfrac{k_1 \ce{[S][E_T]}}{k_1 \ce{[S]} + k_{-1} + k_2} = \dfrac{\ce{[E_T][S]}}{K_M + \ce{[S]}}$|
|Turnover number (# substrates converted to product per unit time on one enzyme at saturation)|$k_{\mathrm{cat}} = k_2$|
|Michaelis-Menten constant (attraction of enzyme of its substrate, [Substrate] which rate of rxn is 1/2 max)|$K_M = \dfrac{k_{\mathrm{cat}} + k_{-1}}{k_1}$|
|Maximum rate|$V_{\max} = k_{\mathrm{cat}} \ce{[E_T]}$|
|**Michaelis-Menten equation** <br/> Rate of reaction|$\begin{aligned}r_{\ce{P}} &= k_{2} \ce{[ES]} \\\ &= \dfrac{k_1 k_{2} \ce{[S][E_T]}}{k_1 \ce{[S]} + k_{-1} + k_2} \\\ &= \dfrac{k_{\mathrm{cat}} \ce{[S][E_T]}}{K_M + \ce{[S]}} \\\ &= \dfrac{V_{\max} \ce{[S]}}{K_M + \ce{[S]}} \end{aligned}$|
|**Lineweaver-Burk equation**|$\dfrac{1}{r_{\ce{P}}} = \dfrac{K_M}{V_{\max}}\dfrac{1}{\ce{[S]}} + \dfrac{1}{V_{\max}}$|
|Eadie-Hofstee equation|$r_{\ce{P}} = V_{\max} - K_M\dfrac{r_{\ce{P}}}{\ce{[S]}}$|
|Hanes-Woolf equation|$\dfrac{\ce{[S]}}{r_{\ce{P}}} = \dfrac{K_M}{V_{\max}} + \dfrac{1}{V_{\max}}\ce{[S]}$|

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

## Cell Growth Kinetics

|Description|Equations|
|-:|:-|
|Nomenclature|$S$ = substrate mass <br/> $P$ = product mass <br/> $X$ = cell mass|
|Mass balance|$\Delta S +  \Delta P = \Delta X$|
|Yield coefficient (mass basis)|$Y_{X/S} = -\dfrac{\Delta X}{\Delta S} = \dfrac{[X] - [X]_0}{[S]_0 - [S]}$|
|Exponential growth|$[X] = [X]\_0 \exp(\mu_{\max}t)$|
|Doubling time|$t_d = \dfrac{\ln 2}{\mu}$|
|Exponential death|$[X] = [X]_0 \exp(-k_d t)$|
|Optical density (absorbance)|$\mathrm{OD}\_\lambda = A_\lambda = \log \dfrac{I}{I_0}$|

## Cell Reaction Stoichiometry

### Elemental (atomic) balance

|Description|Equations|
|-:|:-|
|Cell reaction|$\ce{C_wH_xO_yN_z + a O_2 + b NH_3} \newline \ce{-> c CH_\alpha O_\beta N_\delta\ + d CO_2 + e H_2O + f C_jH_kO_lN_m}$|
|Respiratory quotient|$\mathrm{RQ} = \dfrac{\text{mol } \ce{CO2} \text{ produced}}{\text{mol } \ce{O2} \text{ consumed}} = \dfrac{d}{a}$|
|Biomass yield (mass basis)|$Y_{X/S} = \dfrac{\Delta X}{\Delta S} = \dfrac{\text{g cell}}{\text{g substrate}}$|
|Product yield (mass basis)|$Y_{P/S} = \dfrac{\Delta P}{\Delta S} = \dfrac{\text{g product}}{\text{g substrate}}$|
|Substrate utilization rate (SUR)|$\mathrm{SUR} = \dfrac{\text{mol substrate}}{\text{time}}$|
|Oxygen utilization rate (OUR)|$\mathrm{OUR} \equiv A = a\ \mathrm{SUR}$|
|Carbon dioxide evolution rate (CER)|$\mathrm{CER} \equiv D = d\ \mathrm{SUR}$|

### Electron balance

|Description|Equations|
|-:|:-|
|Cell reaction|$\ce{C_wH_xO_yN_z + a O_2 + b NH_3} \newline \ce{-> c CH_\alpha O_\beta N_\delta\ + d CO_2 + e H_2O + f C_jH_kO_lN_m}$|
|Degree of reduction|$\gamma_i = \dfrac{(\text{Valance \\# of element } i) (\text{\\# atom in element } i)}{\text{\\#} \ce{C} \text{ atom}}$|
|Stoichiometric coefficient of oxygen|$a = \frac{1}{4}(w\gamma_S - c\gamma_X - fj\gamma_P)$|

<!-- ★ -->