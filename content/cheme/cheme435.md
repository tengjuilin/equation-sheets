---
title: "CHEM E 435 Transport Process III"
date: 2022-12-24T00:00:00-08:00
---

## Separation

|Description|Equations|
|-:|:-|
|||

## Membrane Separations

|Description|Equations|
|-:|:-|
|Transmembrane molar flux|$\begin{aligned}N_i &= \dfrac{P_{M, i}}{l_M}(\text{driving force}) \\\ &= \bar{P}\_{M, i}(\text{driving force}) \end{aligned}$|
|Permeance|$\bar{P}\_{M, i} = \dfrac{P_{M, i}}{l_M}$|
|Permeability|$P_{M, i} = \bar{P}\_{M, i} l_M$|
|Selectivity|$S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}}$|
|Gas permeability unit|$\begin{aligned}&1 \ \mathrm{barrer} \\\ &= 10^{-10} \ \mathrm{cm^3_{STP} \cdot cm/(cm^2 \cdot s \cdot cmHg)} \\\ &= 3.35 \times 10^{-16} \ \mathrm{mol \cdot m / (m^2 \cdot s \cdot Pa)} \\\ &= 5.58 \times 10^{-12} \ \mathrm{lbmol \cdot ft / (ft^2 \cdot h \cdot psi)}\end{aligned}$|
|Mole of gas in standard temperature and pressure (STP)|$1 \ \mathrm{mol} \sim 22.4 \ \mathrm{L_{STP}}$|

### Transport through porous membranes

#### Bulk flow

|Description|Equations|
|-:|:-|
|Hagen-Poiseuille flow <br/> ★ Laminar flow $\mathrm{Re} < 2100$|$v = \dfrac{D^2}{32\mu L}(P_0 - P_L)$|
|Pore number density|$n = \dfrac{n_\text{total}}{A_c} = \dfrac{\text{total \\# of pores}}{\text{membrane cross sectional area}}$|
|Porosity (void fraction) <br/> ★ Straight cylindrical pore|$\varepsilon = \frac{1}{4}n\pi D^2$|
|Bulk flow flux <br/> ★ Straight cylindrical pore|$\begin{aligned}N &= v\rho\varepsilon \\\ &= \dfrac{\varepsilon\rho D^2}{32 \mu l_M} (P_0 - P_L) \\\ &= \dfrac{n\pi\rho D^4}{128 v l_M}(P_0 - P_L)\end{aligned}$|
|Empirical hydraulic diameter|$d_H = \dfrac{4\varepsilon}{a_v}$|
|Specific surface area|$a_v = \dfrac{a}{1 - \varepsilon}$|
|Total pore surface area|$a = a_v (1 - \varepsilon)$|
|Tortuosity correction of membrane width|$\tau l_M$|
|Bulk flow flux <br/> ★ General pore|$N = \dfrac{\rho\varepsilon^2}{2(1-\varepsilon)^2 \tau a_v^2 \mu l_M}(P_0 - P_L)$|
|Ergun equation|$\dfrac{P_0 - P_L}{l_M} = \dfrac{150 \mu v_0 (1-\varepsilon)^2}{D_P^2 \varepsilon^3} + \dfrac{1.75 \rho v_0^2 (1 - \varepsilon)}{D_P \varepsilon^3}$|
|Mean spherical particle diameter|$D_P = \dfrac{6}{a_v}$|

#### Liquid diffusion

|Description|Equations|
|-:|:-|
|Concentration driving force|$\Delta c \not= 0 \newline \Delta P = 0$|
|Transmembrane mass flux|$N_i = \dfrac{D_{e, i}}{l_M}(c_{i, 0} - c_{i, L})$|
|Effective diffusivity|$D_{e, i} = \dfrac{\varepsilon D_i}{\tau} K_{r, i}$|
|Restrictive factor of solute|$K_r = \left[ 1 - \dfrac{d_m}{d_p}\right]^4$|
|Selectivity|$S_{i, j} = \dfrac{D_i K_{r, i}}{D_j K_{r, j}}$|

#### Gas diffusion

|Description|Equations|
|-:|:-|
|Transmembrane molar flux <br/> ★ Ideal gas, uniform transmembrane T, P|$\begin{aligned} N_i &= \dfrac{c_M}{P}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \\\ &= \dfrac{1}{RT}\dfrac{D_{e, i}}{l_M}(P_{i, 0} - P_{i, L}) \end{aligned}$|
|Effective diffusivity|$D_{e, i} = \dfrac{\varepsilon}{\tau} \left[\dfrac{1}{(1/D_i) + (1/D_{K, i})}\right]$|
|Knudsen diffusivity of straight cylindrical pore <br/> ★ Kinetic theory of gas|$D_{K, i} \ [\mathrm{cm/s}] = 4850 d_p \ [\mathrm{cm}] \sqrt{\dfrac{T}{\mathcal{M}_i}\dfrac{[\mathrm{K}]}{[\mathrm{g/mol}]}}$|
|Selectivity of Knudsen diffusion <br/> ★ $D_i \gg D_{K, i}$ <br/> ★ $D_{e, i} \sim D_{K, i}$|$S_{i, j} = \dfrac{P_{M, i}}{P_{M, j}} = \sqrt{\dfrac{\mathcal{M}_j}{\mathcal{M}_i}}$|

### Transport through nonporous (dense) membranes

#### Solution-diffusion of liquid mixtures

|Description|Equations|
|-:|:-|
|Thermodynamic equilibrium partition coefficient|$K_i = \dfrac{c_i}{c_i\'}$|
|Transmembrance mass flux <br/> ★ Fick's law|$N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})$|
|Transmembrance mass flux <br/> ★ $K_{i, 0} = K_{i, L} = K_{i}$|$N_i = \dfrac{K_i D_i}{l_M}(c\'\_{i, 0} - c\'\_{i, L})$|
|Transmembrance mass flux <br/> ★ No mass transfer resistance in fluid boundary layers <br/> ★ $c\'\_{i, 0} = c_{i, F}$ and $c\'\_{i, L} = c_{i, P}$|$N_i = \dfrac{K_i D_i}{l_M}(c_{i, F} - c_{i, P})$|

#### Solution-diffusion of gas mixtures

|Description|Equations|
|-:|:-|
|Henry's constant|$H_i = \dfrac{c_i}{P_i}$|
|Transmembrance mass flux <br/> ★ Fick's law|$N_i = \dfrac{D_i}{l_M}(c_{i, 0} - c_{i, L})$|
|Transmembrance mass flux <br/> ★ $H_{i, 0} = H_{i, L} = H_{i}$|$N_i = \dfrac{H_i D_i}{l_M}(P_{i, 0} - P_{i, L})$|
|Transmembrance mass flux <br/> ★ No mass transfer resistance in external boundary layers <br/> ★ $P_{i, 0} = P_{i, F}$ and $P_{i, L} = P_{i, P}$|$N_i = \dfrac{H_i D_i}{l_M}(P_{i, F} - P_{i, P})$|

#### Separation factor

|Description|Equations|
|-:|:-|
|**Ideal separation factor** <br/> ★ Downstream permeate pressure negligible compared to upstream feed pressure <br/> ★ $x_{i, P} P_P \ll x_{i, F} P_F$ and $x_{j, P} P_P \ll x_{j, F} P_F$ |$\alpha^*_{i, j} = \dfrac{H_i D_i}{H_j D_j} = \dfrac{P\_{M, i}}{P\_{M, j}}$|
|Separation factor|$\alpha_{i, j} = \alpha^*_{i, j} \left[\dfrac{(x\_{j, F} / x\_{j, P}) - r\alpha\_{i, j}}{(x\_{j, F} / x\_{j, P}) - r}\right]$|
|Cut (fraction of feed permeated)|$\theta = \dfrac{\dot{n}_P}{\dot{n}_F}$|

### Reverse osmosis

|Description|Equations|
|-:|:-|
|Osmotic pressure <br/> ★ Equilibrium|$\Pi \equiv P_1 - P_{\ce{H2O}}$|
|Osmotic pressure of water|$\Pi_{\ce{H2O}} = 0$|
|Osmotic process|$P_1 - P_{\ce{H2O}} < \Pi$|
|Reverse osmotic process|$P_1 - P_{\ce{H2O}} > \Pi$|
|Osmotic pressure's thermodynamic derivation <br/> ★ Between pure water and solution <br/> ★ Solvent $A$, solute $B$|$\Pi = -\dfrac{RT}{v_{A}} \ln(x_A \gamma_A)$|
|Osmotic pressure <br/> ★ Ideal solution, dilute $B$|$\Pi = \dfrac{RT n_B}{v_A} = \dfrac{RTc_B}{\mathcal{M}_B}$|

#### Seawater reverse osmosis

|Description|Equations|
|-:|:-|
|Seawater as solution 1; salt as solute B|$\ce{A} = \text{water} = \ce{H2O} \newline \ce{B} = \text{salt} = \ce{S}$|
|Molar mass|$\mathcal{M} = \dfrac{m}{n}$|
|Molarity (molar concentration)|$M = \dfrac{n}{V} = \dfrac{\mathrm{wt \\% \ S}}{100 \\% - \mathrm{wt \\% \ S}}\dfrac{\rho_{\ce{H2O}}}{\mathcal{M}_S}$|
|Seawater osmotic pressure correlation|$\Pi \ [\mathrm{psia}] = 1.12 T \ [\mathrm{K}] \sum M_i \ [\mathrm{mol/L}]$|
|Transmembrane molar flux of water (solvent A)|$N_{\ce{H2O}} = \dfrac{P_{M, \ce{H2O}}}{l_M} (\Delta P - \Delta \pi)$|
|Salt passage|$\mathrm{SP} = \dfrac{c_{S, P}}{c_{S, F}}$|
|Salt rejection|$\mathrm{SR} = 1 - \mathrm{SP}$|
|Concentration polarization factor|$\Gamma \equiv \dfrac{c_{S, i} - c_{S, F}}{c_{S, F}} = \dfrac{N_{\ce{H2O}} (\mathrm{SR})}{k_S}$|
|Significant concentration polarization|$\Gamma > 0.2$|

{{< admonition type=info title="Symbol Convention" open=false >}}

- $\varepsilon$ - Porosity (Void fraction)
- $M_i$ - Molar mass

{{< /admonition >}}

<!-- ★ -->