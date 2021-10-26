---
title: "CHEM E 330 Transport Processes I"
date: 2021-10-25T00:00:00-07:00
---

## Phenomenological Rate Laws for Diffusive Transport

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

## Transport Coefficients of Fluids

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
|**Wilke equation** <br/> Viscosity of gas mixture|$\mu_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i \mu_i}{\sum_{j=1}^N x_j \Phi_{ij}}$|
|**Wilke equation** <br/> Thermal conductivity of gas mixture|$k_{\text{mix}} = \displaystyle\sum_{i=1}^{N}\dfrac{x_i k_i}{\sum_{j=1}^N x_j \Phi_{ij}}$|
|Wilke equation parameter|$\Phi_{ij} = \frac{1}{\sqrt{8}} \left[ 1 + \frac{\mathcal{M}_i}{\mathcal{M}_j} \right]^{-1/2} \left[ 1 + \left[\frac{\mu_i}{\mu_j}\right]^{1/2} + \left[\frac{\mathcal{M}_i}{\mathcal{M}_j}\right]^{-1/4} \right]^2$|
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

## Shell Balances for Flux Distributions and Profiles

### Boundary conditions and shell volume

|Description|Equations|
|-:|:-|
|Rectilinear shell volume|$\Delta V = LW\Delta y$|
|Cylindrical shell volume|$\Delta V = 2\pi r L \Delta r$|
|Spherical shell volume|$\Delta V = 4 \pi r^2 \Delta r$|
|Newton's law of cooling|$q = h(T_{\text{solid}} - T_{\text{fluid}})$|
|Relationship between $N_A$ and $c_A$ at boundary|$N_A = k_m (c_{A, \text{solid}} - c_{A, \text{fluid}})$|
|Reynolds number|$\mathrm{Re} = \dfrac{L_{\text{char}}v_{\text{char}}\rho}{\mu}$|

<!-- ### Shell balance method

1. Sketch the system with coordinate system
2. Sketch the shell that is thin in the direction of transport (change)
3. Write shell volume $\Delta V$
4. Write shell balance OIGA of transported quantity
   - $\mathrm{out - in = generation - accumulation}$
5. Take limit as shell thickness approach 0
   - **Differential equation of flux distribution**
6. Separate variable and integrate
   - **Flux distribution, $c_1$**
7. Substitute rate law
8. Separate variable and integrate
   - **Profile, $c_1, c_2$**
9. Evaluate $c_1, c_2$ using boundary conditions -->

### Axial transport in rectilinear systems

- Rectilinear system
- No generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{dq}{dy} = 0$|
|Temperature profile (linear)|$T(y) = T_1 - \dfrac{q}{k} y$|
|Flux distribution (inverse)|$q(y) = \dfrac{k(T_1 - T)}{y}$|
|Flux across the whole layer|$q = \dfrac{k(T_1 - T_2)}{H}$|

### Radial transport in cylindrical systems

- Cylindrical system
- No generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{d(rq)}{dr} = 0$|
|Flux distribution (inverse)|$q(r) = \dfrac{k(T_i - T_0)}{r \ln(\frac{R_0}{R_i})}$|
|Temperature profile (logarithmic)|$T(r) = T_i - \dfrac{T_i - T_0}{\ln(\frac{R_0}{R_i})} \ln\left(\dfrac{r}{R_i}\right)$|

### Radial transport in spherical systems

- Spherical system
- No generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{d(r^2 q)}{dr} = 0$|
|Flux distribution (inverse squared)|$q(r) = \dfrac{k(T_i - T_0)}{r^2 (\frac{1}{R_i} - \frac{1}{R_0})}$|
|Temperature profile (inverse)|$T(r) = T_i - \dfrac{T_i - T_0}{(\frac{1}{R_i} - \frac{1}{R_0})} \left(\dfrac{1}{r} - \dfrac{1}{R_i}\right)$|

### Axial transport in rectilinear systems (with generation)

- Rectilinear system
- With generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{dq}{dy} = S$|
|Flux distribution (linear)|$q(y) = Sy + \dfrac{k}{H}(T_2 - T_1) - \dfrac{SH}{2}$|
|Temperature profile (quadratic)|$T(y) = T_1 - \dfrac{S}{2k} y^2 + \left[ \dfrac{SH}{2k} - \dfrac{T_2 - T_1}{H} \right] y$|

### Flow down inclined plane (falling film)

- Rectilinear system
- Gravity driving force, but no pressure gradient
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{d\tau_{yx}}{dy} = \rho g \cos\beta$|
|Flux distribution (linear)|$\tau_{yx}(y) = -\rho g \cos\beta (\delta - y)$|
|Velocity profile (quadratic)|$v_x(y) = \dfrac{g \cos\beta}{2\nu}(2\delta y - y^2)$|
|★ No entry length effect|$L \gg \delta$|
|★ No edge effect|$W \gg \delta$|
|★ Incompressible Newtonian fluid|$\Delta\mu = 0, \Delta\rho = 0$|
|★ No end effect, no ripple|$\mathrm{Re}_{\text{rippling}} \lesssim 20$|
|Reynolds number for falling film|$\mathrm{Re} = \dfrac{4\delta \langle v_x \rangle\rho}{\mu}$|

#### Flow descriptors

|Description|Equations|
|-:|:-|
|Skin friction|$\tau^0 = \rho g \cos(\beta)\delta$|
|Free surface velocity|$v_x^{\text{surf}} = \dfrac{g \cos\beta}{2\nu}\delta^2$|
|Volumetric flow rate|$Q = \int v_\perp \ dA$|
|Volumetric flow rate per unit area|$\dfrac{Q}{W} = \dfrac{g \cos(\beta) \delta^3}{3\nu}$|
|Average velocity|$\langle v_x \rangle = \dfrac{g\cos(\beta)\delta^2}{3\nu}$|
|Mass flow rate|$\dot{m} = \rho Q$|
|Mass flow rate per unit width|$\Gamma = \dfrac{\rho Q}{W} = \dfrac{\rho g \cos(\beta) \delta^3}{3\nu}$|
|Film thickness given $\Gamma$|$\delta = \sqrt[3]{\dfrac{3\nu \Gamma}{\rho g \cos\beta}}$|

### Flow in round tube (Hagen-Poiseuille flow)

- Cylindrical system
- Pressure-gravity driving force
- Steady state
- No tube bents, constant cross section
- Negligible P dependence with r

|Description|Equations|
|-:|:-|
|Modified pressure|$\mathcal{P} = P + \rho gh$|
|Pressure-gravity driving force|$-\dfrac{dP}{dz} + \rho g \cos\beta = \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}$|
|Differential equation of flux distribution|$\dfrac{d (r\tau_{yx})}{dy} = \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$|
|Flux distribution (linear)|$\tau_{yx}(r) = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$|
|Velocity profile (quadratic)|$v_z(r) = \dfrac{R^2}{4\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) \left[ 1 - \left( \dfrac{r}{R} \right)^2 \right]$|
|★ Incompressible Newtonian fluid|$\Delta\mu = 0, \Delta\rho = 0$|
|★ Laminar flow|$\mathrm{Re}_{\text{laminar}} \le 2100$|
|★ Fully developed flow (no entry length effect)|$L_e \approxeq 0.035 D \mathrm{Re}$|
|Reynolds number for pipe flow|$\mathrm{Re}_{\text{pipe}} = \dfrac{D \langle v_z \rangle\rho}{\mu}$|

#### Flow descriptors

|Description|Equations|
|-:|:-|
|Skin friction|$\tau_{yx}^0 = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) R$|
|Volumetric flow|$Q = \dfrac{R^4 \pi}{8 \mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|
|Average velocity|$\langle v_z \rangle = \dfrac{R^2}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|
|Mass flow rate|$\dot{m} = \dfrac{R^4 \pi\rho}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|

### Laminar flow through porous media

|Description|Equations|
|-:|:-|
|**Darcy's law** - average velocity <br/> $\kappa$ - bed permeability|$\langle v \rangle = \dfrac{\kappa}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$|
|**Darcy's law** - volumetric flow rate <br/> $A$ - empty bed cross section <br/> $\varepsilon$ - porosity, void fraction|$Q = \dfrac{\kappa A \varepsilon}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$|
|**Blake-Kozeny model** <br/> Bed permeability|$\kappa = \dfrac{D_p^2}{150} \left( \dfrac{\varepsilon}{1 - \varepsilon} \right)$|
|Effective packing particle diameter|$D_p = \dfrac{6}{a_v} = \dfrac{6 V}{A} \newline D_{p, \text{spheres}} = D$|
|Bed Reynolds number|$\mathrm{Re}_{\text{bed}} = \dfrac{D_p Q \rho}{\mu A (1-\varepsilon)}$|
|★ Laminar flow|$\mathrm{Re}_{\text{laminar}} < 10$|

### Fluid pressure, hydrostatic, manometer

|Description|Equations|
|-:|:-|
|Equation of hydrostatic|$P_1 - P_2 = \rho g(h_2 - h_1)$|
|Manometer equation|$P_1 - P_2 = (\rho_m - \rho) gH + \rho g(h_2 - h_1)$|
|Manometer equation|$\mathcal{P}_1 - \mathcal{P}_2 = (\rho_m - \rho) gH$|

### Unsteady state transport

|Description|Equations|
|-:|:-|
|Unsteady state conduction in rectilinear system|$\left(\dfrac{\partial T}{\partial t}\right)_y = \alpha \dfrac{\partial^2 T}{\partial y^2} + \dfrac{S}{\rho \hat{c_p}}$|
|Unsteady state diffusion in rectilinear system|$\left(\dfrac{\partial c_A}{\partial t}\right)_y = D\_{AB} \dfrac{\partial^2 c_A}{\partial y^2} + R_A$|
|Unsteady state Couette flow (1D rectilinear shear flow)|$\left(\dfrac{\partial v_x}{\partial t}\right)_y = \nu \left(\dfrac{\partial^2 v_x}{\partial y^2}\right)_t$|
|Unsteady state flow in cylindrical system|$\left(\dfrac{\partial v_z}{\partial t}\right)_r = \nu \left[ \dfrac{\partial^2 v_z}{\partial r^2} + \dfrac{1}{r} \dfrac{\partial v_z}{\partial r} \right] + \dfrac{1}{\rho} \left[\dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}\right]$|

<!-- ★ -->