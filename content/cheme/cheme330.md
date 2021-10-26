---
title: "CHEM E 330 Transport Processes I"
date: 2021-10-25T00:00:00-07:00
---

## Phenomenological rate laws of transport

|Description|Equations|
|-:|:-|
|General form|flux = (coefficient)(driving force)|
|**Fourier's law** <br/> Heat conduction|$q = -k\dfrac{dT}{dy}$|
|**Fick's law** <br/> Species diffusion|$J_A^* = -D_{AB} \dfrac{dc_a}{dy}$|
|**Newton's law of viscosity** <br/> Momentum transfer|$\tau_{yx} = -\mu \dfrac{dv_x}{dy}$|

### Rate laws as concentration gradients

|Description|Equations|
|-:|:-|
|**Fourier's law**|$q_{y} = -\alpha \dfrac{dc_{H}}{dy}$|
|**Fick's law**|$J_A^* = -D_{AB} \dfrac{dc_a}{dy}$|
|**Newton's law of viscosity**|$\tau_{yx} = -\nu \dfrac{dc_{p_x}}{dy}$|
|Kinematic viscosity|$\nu = \dfrac{\mu}{\rho}$|
|Thermal diffusivity|$\alpha = \dfrac{k}{\rho \hat{c_P}}$|
|Diffusivity of A in B|$D_{AB}$|
|Prandtl number|$\mathrm{Pr} = \dfrac{\nu}{\alpha} = \dfrac{\hat{C}_p \mu}{k}$|
|Schmidt number|$\mathrm{Sc} = \dfrac{\nu}{D_{AB}} = \dfrac{\mu}{\rho D_{AB}}$|

### Heat transfer

|Description|Equations|
|-:|:-|
|Heat flow|$\dot{Q} = \dfrac{Q}{t}$|
|Heat flux|$q = \dfrac{\dot{Q}}{A}$|

### Mass transfer

|Description|Equations|
|-:|:-|
|Mass (species) transport|$N_A = x_A (\sum N_i) + J_A^*$|
|Diffusion of A through a stagnant layer of B|$N_A = -\dfrac{cD_{AB}}{1 - x_A}\dfrac{dx_A}{dy}$ <br/> $N_A = -\dfrac{cD_{AB}}{L}\ln(1-x_A^s)$|
|Equimolar counter diffusion|$N_A = -cD_{AB}\dfrac{dx_A}{dy}$|
|Reaction at catalytic surface <br/> $\ce{A = 2B} \implies N_B = 2N_A$|$N_A = -x_A N_A - cD_{AB}\dfrac{dx_A}{dy}$|

### Momentum transfer

|Description|Equations|
|-:|:-|
|Interpretation of $\tau_{yx}$|1. viscous shear stress exerted on a $y$-plane in the $+x$-direction by the fluid of lesser $y$ on that of greater $y$ <br/> 2. flux of $x$-momentum across a $y$-plane in the $+y$-direction|
|Shear strain rate|$\dot{\gamma} = \dfrac{dv_x}{dy}$|
|**Hooke's law** <br/> ★ Hookean solid|$\tau_{yx} = -G \dfrac{dx}{dy} = -G \gamma$|
|**Newton's law of viscosity** <br/> ★ Newtonian fluid|$\tau_{yx} = -\mu \dfrac{dv_x}{dy} = -\mu\dot{\gamma}$|
|General Newton's law of viscosity|$\tau_{yx} = -\eta(\dot{\gamma})\dot{\gamma}$|
|Viscosity function of power law fluid|$\eta = m\dot{\gamma}^{n-1}$|
|**Newton's law of viscosity** <br/> ★ Power law fluid|$\tau_{yx} = -m\dot{\gamma}^n$|
|**Carreau equation** <br/> ★ Slurry|$\dfrac{\eta - \eta_\infty}{\eta_o - \eta_\infty} = [1 + (\lambda\dot{\gamma})^2]^{(n-1)/2}$|

## Transport coefficients of fluids

### Ideal gas: Simple kinetic theory

|Description|Equations|
|-:|:-|
|Average velocity|$\bar{u} = \sqrt{\dfrac{8 k_B T}{\pi m}}$|
|Mean free path|$\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n}$|
|Number density|$n = \dfrac{N}{V}$|
|Molecular flux in the y-direction|$z = \frac{1}{4}n\bar{u}$|
|Average distance of molecules from ref plane when they initiate their jump|$\bar{a} = \frac{2}{3}\lambda$|
|**Viscosity of ideal gas**|$\mu = \dfrac{1}{3}\rho\bar{u}\lambda = \dfrac{2}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}$|
|**Thermal conductivity of ideal gas**|$k = \dfrac{1}{3}\rho\hat{c_v}\bar{u}\lambda = \dfrac{2\hat{c_v}}{3\pi^{3/2}}\dfrac{\sqrt{mk_BT}}{d^2}$|
|**Diffusivity of ideal gas A in B**|$D_{AB} = \dfrac{1}{3}\bar{u}_{AB}\lambda_{AB} = \dfrac{2}{\pi^{3/2}}\dfrac{\sqrt{{k_BT}^3/m_{AB}}}{d^2_{AB} P}$|
|Mean mass for diffusivity|$m_{AB} = \dfrac{2m_A m_B}{m_A+m_B}$|
|Mean distance for diffusivity|$d_{AB} = \frac{1}{2}(d_A + d_B)$|
|Prandtl number of monoatomic ideal gas|$\mathrm{Pr}_{\text{mono}} = 1$|
|Schmidt number of general ideal gas|$\mathrm{Sc} = 1$|

### Real gas: Chapman-Enskog equations

|Description|Equations|
|-:|:-|
|Lenard-Jones potential|$\varphi(r) = 4\varepsilon \left[\left(\dfrac{\sigma}{r}\right)^{12} - \left(\dfrac{\sigma}{r}\right)^6\right]$|
|Attractive force|$F_{\text{attr}} = \dfrac{24\varepsilon}{r} \left[\left(\dfrac{\sigma}{r}\right)^{6} - 2\left(\dfrac{\sigma}{r}\right)^{12}\right]$|
|Viscosity of real gas (analytic)|$\mu = \dfrac{5}{16\pi}\dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_\mu}$|
|Thermal conductivity of real gas (analytic)|$k = \dfrac{25}{32\pi} \dfrac{\sqrt{\pi m k_BT}}{\sigma^2 \Omega_k}\hat{c_v} = \dfrac{5}{2}\hat{c_v}\mu $|
|**Viscosity of real gas**|$\mu\left(\mathrm{\frac{g}{cm \cdot s}}\right) = 2.6692 \times 10^{-5} \dfrac{\sqrt{\mathcal{M}T}}{\sigma^2 \Omega_\mu}$|
|**Thermal conductivity of monoatomic real gas**|$k_{\text{mono}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = 1.989 \times 10^{-4} \dfrac{\sqrt{T / \mathcal{M}}}{\sigma^2 \Omega_k}$|
|**Thermal conductivity of polyatomic real gas** <br/> Euken factor|$k_{\text{poly}}\left(\mathrm{\frac{cal}{cm \cdot s \cdot K}}\right) = \left[ \hat{c_p} + \dfrac{5}{4}\dfrac{R}{\mathcal{M}} \right] \mu$|
|**Diffusivity of real gas** <br/> $T [=] \mathrm{K} \newline P [=] \mathrm{atm} \newline \sigma_{AB} [=]$ Å|$D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 2.63 \times 10^{-3} \dfrac{\sqrt{T^3 / \mathcal{M}_{AB}}}{P\sigma^2_{AB}\Omega_D}$|
|Mean molar mass for diffusivity|$\mathcal{M}_{AB} = \dfrac{2\mathcal{M}_A \mathcal{M}_B}{\mathcal{M}_A + \mathcal{M}_B}$|
|Mean distance for diffusivity|$\omega_{AB} = \frac{1}{2}(\omega_A + \omega_B)$|
|Viscosity at different temperatures|$\mu(T_2) = \mu(T_1)\sqrt{\dfrac{T_2}{T_1}}\dfrac{\Omega_{\mu_1}}{\Omega_{\mu_2}}$|
|Diffusivity at different temperatures|$D_{AB}(T_2) = D_{AB}(T_1)\left(\dfrac{T_2}{T_1}\right)^{3/2}\dfrac{\Omega_{D_1}}{\Omega_{D_2}}$|
|**$T$ and $P$ dependence of transport coefficients of gases at moderate pressure**|$\begin{aligned}\mu &\propto\sqrt{T} \\\ k_{\text{mono}} &\propto\sqrt{T} \\\ k_{\text{poly}} &= f(T, \hat{c_p}(T)) \\\ D_{AB} &\propto T^{3/2}P^{-1} \\\ D_{AB} &= D_{BA}\end{aligned}$|

### Ideal gas mixtures

|Description|Equations|
|-:|:-|
|**Wilkie equation** <br/> Viscosity of gas mixture|$\mu_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i \mu_i}{\sum_{j=1}^N x_j \Phi_{ij}}$|
|**Wilkie equation** <br/> Thermal conductivity of gas mixture|$k_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i k_i}{\sum_{j=1}^N x_j \Phi_{ij}}$|
|Wilkie equation parameter|$\Phi_{ij} = \frac{1}{\sqrt{8}} \left[ 1 + \frac{\mathcal{M}_i}{\mathcal{M}_j} \right]^{-1/2} \left[ 1 + \left[\frac{\mu_i}{\mu_j}\right]^{1/2} + \left[\frac{\mathcal{M}_i}{\mathcal{M}_j}\right]^{-1/4} \right]^2$|
|**Blanc's equation** <br/> Diffusivity of gas mixture|$D_{i, \text{mix}} = \left[ \displaystyle\sum_{j \not= 1}^{N} \dfrac{x_j}{D_{ij}} \right]^{-1}$|

### Liquids

|Description|Equations|
|-:|:-|
|**Eyring model** <br/> Viscosity of liquid|$\mu = \dfrac{N_A h}{\tilde{V}}\exp\left[ 0.408 \dfrac{\Delta U_{\text{vap}}}{RT} \right]$|
|**Bridgeman equation** <br/> Thermal conductivity of liquid|$k = 2.8 \left( \dfrac{N_A}{\tilde{V}}^{2/3} k_B v_s \right)$|
|Einstein equation|$D_{AB} \approx \dfrac{k_BT}{f}$|
|Hydrodynamic friction factor|$f = \begin{cases} 6\pi\mu_BR_A & \text{no slip} \\\ 4\pi\mu_BR_A & \text{free slip} \end{cases}$|
|**Stoke-Einstein Equation** <br/> Diffusivity of dilute liquid A|$D_{AB} = \dfrac{k_BT}{4\pi\mu_BR_A}$|
|**Wilke-Chang correlation** <br/> Diffusivity of dilute liquid A <br/> $\tilde{V} [=] \mathrm{cm^3/mol} \newline \mu_B [=] \mathrm{cP} \newline T [=] \mathrm{K}$|$D_{AB}\left(\mathrm{\frac{cm^2}{s}}\right) = 7.4 \times 10^{-8} \dfrac{(\psi_B \mathcal{M}_B)^{1/2} T}{\mu \tilde{V}_A^{0.6}}$|
|**Vigne's equation** <br/> Diffusivity of liquid mixture|$D_{AB} = (D_{AB}^0)^{x_B} (D_{BA}^0)^{x_A}$|
|**$T$ dependence of transport coefficients of liquids <br/> (no $P$ dependence)**|$\begin{aligned} \mu &= Ae^{B/T} \\\ D_{AB}\mu_B &\propto T \\\ D_{AB} &\not= D_{BA} \end{aligned}$|
|||

<!-- ★ -->