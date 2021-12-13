---
title: "CHEM E 330 Transport Processes I"
date: 2021-12-08T00:00:00-07:00
---

## -★- TRANSPORT PHENOMENA

## Rate Laws for Diffusive Transport

|Description|Equations|
|-:|:-|
|General form|flux = -(coefficient)(driving force)|
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

★ Moderate pressure

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

## Shell Balance (Bottom-Up)

### Boundary conditions and shell volume

|Description|Equations|
|-:|:-|
|Rectilinear shell volume|$\Delta V = LW\Delta y$|
|Cylindrical shell volume|$\Delta V = 2\pi r L \Delta r$|
|Spherical shell volume|$\Delta V = 4 \pi r^2 \Delta r$|
|Newton's law of cooling|$q = h(T_{\text{solid}} - T_{\text{fluid}})$|
|Relationship between $N_A$ and $c_A$ at boundary|$N_A = k_m (c_{A, \text{solid}} - c_{A, \text{fluid}})$|
|Reynolds number|$\mathrm{Re} = \dfrac{L_{\text{char}}v_{\text{char}}\rho}{\mu}$|
|No slip condition|$v_1 = v_2$|
|Free slip condition|$-\mu_1\left(\dfrac{dv_x}{dy}\right)_1 = 0$|
|Continuity of stress|$\begin{aligned}\tau_{y, 1} &= \tau_{y, 2} \\\ -\mu_1\left(\dfrac{dv_x}{dy}\right)_1 &= -\mu_2\left(\dfrac{dv_x}{dy}\right)_2 \end{aligned}$|

### Shell balance method

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
9. Evaluate $c_1, c_2$ using boundary conditions

### Axial transport in rectilinear systems

- Rectilinear coordinates
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

- Cylindrical coordinates
- No generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{d(rq)}{dr} = 0$|
|Flux distribution (inverse)|$q(r) = \dfrac{k(T_i - T_0)}{r \ln(\frac{R_0}{R_i})}$|
|Temperature profile (logarithmic)|$T(r) = T_i - \dfrac{T_i - T_0}{\ln(\frac{R_0}{R_i})} \ln\left(\dfrac{r}{R_i}\right)$|

### Radial transport in spherical systems

- Spherical coordinates
- No generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{d(r^2 q)}{dr} = 0$|
|Flux distribution (inverse squared)|$q(r) = \dfrac{k(T_i - T_0)}{r^2 (\frac{1}{R_i} - \frac{1}{R_0})}$|
|Temperature profile (inverse)|$T(r) = T_i - \dfrac{T_i - T_0}{(\frac{1}{R_i} - \frac{1}{R_0})} \left(\dfrac{1}{r} - \dfrac{1}{R_i}\right)$|

### Axial transport in rectilinear systems (with generation)

- Rectilinear coordinates
- With generation
- No driving force
- Steady state

|Description|Equations|
|-:|:-|
|Differential equation of flux distribution|$\dfrac{dq}{dy} = S$|
|Flux distribution (linear)|$q(y) = Sy + \dfrac{k}{H}(T_2 - T_1) - \dfrac{SH}{2}$|
|Temperature profile (quadratic)|$T(y) = T_1 - \dfrac{S}{2k} y^2 + \left[ \dfrac{SH}{2k} - \dfrac{T_2 - T_1}{H} \right] y$|

### Flow down inclined plane (falling film)

- Rectilinear coordinates
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

- Cylindrical coordinates
- Pressure-gravity driving force
- Steady state
- No tube bents, constant cross section
- Negligible P dependence with r

|Description|Equations|
|-:|:-|
|Modified pressure|$\mathcal{P} = P + \rho gh$|
|Pressure-gravity driving force|$-\dfrac{dP}{dz} + \rho g \cos\beta = \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L}$|
|Differential equation of flux distribution|$\dfrac{d (r\tau_{rz})}{dr} = \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$|
|Flux distribution (linear)|$\tau_{rz}(r) = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) r$|
|Velocity profile (quadratic)|$v_z(r) = \dfrac{R^2}{4\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) \left[ 1 - \left( \dfrac{r}{R} \right)^2 \right]$|
|★ Incompressible Newtonian fluid|$\Delta\mu = 0, \Delta\rho = 0$|
|★ Laminar flow|$\mathrm{Re}_{\text{laminar}} \le 2100$|
|★ Fully developed flow (no entry length effect)|$L_e \approxeq 0.035 D \mathrm{Re}$|
|Reynolds number for pipe flow|$\mathrm{Re}_{\text{pipe}} = \dfrac{D \langle v_z \rangle\rho}{\mu}$|

#### Flow descriptors

|Description|Equations|
|-:|:-|
|Skin friction|$\tau_{rz}^0 = \dfrac{1}{2} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right) R$|
|Volumetric flow|$Q = \dfrac{R^4 \pi}{8 \mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|
|Average velocity|$\langle v_z \rangle = \dfrac{R^2}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|
|Mass flow rate|$\dot{m} = \dfrac{R^4 \pi\rho}{8\mu} \left( \dfrac{\mathcal{P}_1 - \mathcal{P}_2}{L} \right)$|

### Laminar flow through porous media

|Description|Equations|
|-:|:-|
|**Darcy's law** - average velocity <br/> $\kappa$ - bed permeability|$\langle v \rangle = \dfrac{\kappa}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$|
|**Darcy's law** - volumetric flow rate <br/> $A$ - empty bed cross section <br/> $\varepsilon$ - porosity, void fraction|$Q = \dfrac{\kappa A \varepsilon}{\mu L}(\mathcal{P}_1 - \mathcal{P}_2)$|
|**Blake-Kozeny model** <br/> Bed permeability|$\kappa = \dfrac{D_p^2}{150} \left( \dfrac{\varepsilon}{1 - \varepsilon} \right)^2$|
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

## Rate Laws in 3D

|Description|Equations|
|-:|:-|
|Fourier's law in 3D|$\utilde{q} = -k \nabla T$|
|Fick's law in 3D|$\utilde{J}_A^* = -D_{AB} \nabla c_A$|
|Newton's law of viscosity in 3D|$\underset{\approx}{\tau} = -\mu (\underset{\approx}{\Delta} + \underset{\approx}{\Delta}^{\dagger})$|
|Viscous stress tensor|$\underset{\approx}{\tau} = \begin{bmatrix} \tau_{xx} & \tau_{xy} & \tau_{xz} \\\ \tau_{yx} & \tau_{yy} & \tau_{yz} \\\ \tau_{zx} & \tau_{zy} & \tau_{zz} \end{bmatrix}$|
|Rate of strain tensor|$\underset{\approx}{\Delta} = \begin{bmatrix} \dfrac{\partial v_x}{\partial x} & \dfrac{\partial v_x}{\partial y} & \dfrac{\partial v_x}{\partial z} \\\ \\\ \dfrac{\partial v_y}{\partial x} & \dfrac{\partial v_y}{\partial y} & \dfrac{\partial v_y}{\partial z} \\\ \\\ \dfrac{\partial v_z}{\partial x} & \dfrac{\partial v_z}{\partial y} & \dfrac{\partial v_z}{\partial z} \end{bmatrix}$|

## Conservation Laws in 3D

|Description|Equations|
|-:|:-|
|Conservation of thermal energy|$\nabla\cdot\utilde{q} = S - \rho \hat{c_p} \dfrac{\partial T}{\partial t}$|
|**Conduction equation** <br/> ★ No convection|$\dfrac{\partial T}{\partial t} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}$|
|**Molecular diffusion equation** <br/> ★ No convection|$\dfrac{\partial c_A}{\partial t} = D_{AB} \nabla^2 c_A + R_A$|

## -★- FLUID MECHANICS

## Navier-Stokes Equation

|Description|Equations|
|-:|:-|
|**Continuity equation**|$\dfrac{\partial \rho}{\partial t} + \nabla\cdot(\rho\utilde{v}) = 0$|
|**Continuity equation of incompressible liquid** <br/> ★ Constant $\rho$|$\nabla\cdot\utilde{v} = 0$|
|**Equation of motion** ($v$-form)|$\rho\dfrac{D\utilde{v}}{Dt} = -\nabla p + \mu\nabla^2\utilde{v} + \rho g$|
|**Equation of motion** ($\tau$-form)|$\rho\dfrac{D\utilde{v}}{Dt} = -\nabla p - \nabla\cdot\underset{\approx}{\tau} + \rho g$|
|Equation of motion ($x$-component)|$\begin{aligned} &\rho \left[ \dfrac{\partial v_x}{\partial t} + \utilde{v}\cdot\nabla v_x \right] \\\ =& -\dfrac{\partial p}{\partial x} - \left[ \dfrac{\partial \tau_{xx}}{\partial x} + \dfrac{\partial \tau_{yx}}{\partial y} + \dfrac{\partial \tau_{zx}}{\partial z} \right] + \rho g_x \end{aligned}$|

### Operators

|Description|Equations|
|-:|:-|
|Gradient operator $\nabla$|Operates on scalar to give a vector, whose magnitude is the maximum rate of change of the scalar with position, and whose direction points in the direction of that change|
|Divergence operator $(\nabla\cdot)$|Operates on a vector to give a scalar|
|Divergence of a flux vector $(\nabla\cdot\utilde{f})$|Rate of efflux (outflow) of the transported quantity per unit volume|
|Laplacian operator|$\nabla^2 = \nabla\cdot\nabla$|
|Substantial derivative operator|$\dfrac{D}{Dt} = \dfrac{\partial}{\partial t} + \utilde{v}\cdot\nabla$|

### Generalization to convection

|Description|Equations|
|-:|:-|
|Thermal energy equation|$\dfrac{DT}{Dt} = \alpha \nabla^2 T + \dfrac{S}{\rho \hat{c_p}}$|
|Convective diffusion equation|$\dfrac{D c_A}{Dt} = D_{AB} \nabla^2 c_A + R_A$|

### Flow in conduit

|Description|Equations|
|-:|:-|
|Mach number|$\mathrm{Ma} = \dfrac{v_{\text{char}}}{v_{\text{sound}}}$|
|Conduit flow|$\begin{aligned} \dot{m}_1 &= \dot{m}_2 \\\ \rho_1 Q_1 &= \rho_2 Q_2 \end{aligned}$|
|Incompressible conduit flow <br/> ★ Constant $\rho$|$\begin{aligned} Q_1 &= Q_2 \\\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}$|

## Apply N-S Equations (Top-Down)

### Flow between parallel plates

|Assumptions|Equations|
|-:|:-|
|Rectilinear coordinates|$f(x, y, z)$|
|Constant $\rho, \mu$|$\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$|
|Laminar flow|$\mathrm{Re} < \mathrm{Re}_{\text{cr}}$|
|Steady state|$\frac{\partial}{\partial t} = 0$|
|$v_x$ component only|$v_y = v_z = 0$|
|No edge effect|$\frac{\partial}{\partial z} = 0$|
|No end effect|$\frac{\partial v_x}{\partial x} = 0$|
|No hydrostatic pressure diff between plates|$b \ll W, L \implies -\frac{\partial p}{\partial y} + \rho g_y = 0$|

|Description|Equations|
|-:|:-|
|$x$-momentum equation|$\dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} + \mu\dfrac{\partial^2 v_x}{\partial y^2} = 0$|
|Velocity profile (quadratic)|$v_x(y) = \dfrac{1}{2\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)(-y^2 + by)$|
|Average velocity|$\langle v_x \rangle = \dfrac{b^2}{12\mu}\left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)$|
|Skin friction at bottom plate|$\tau^0 = \dfrac{b}{2} \left( \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right)$|

### Couette flow between concentric rotating cylinders

|Assumptions|Equations|
|-:|:-|
|Cylindrical coordinates|$f(r, \theta, z)$|
|Constant $\rho, \mu$|$\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$|
|Laminar flow|$\mathrm{Re} < \mathrm{Re}_{\text{cr}}$|
|Steady state|$\frac{\partial}{\partial t} = 0$|
|$v_\theta$ component only|$v_r = v_z = 0$|
|Axial symmetry|$\frac{\partial}{\partial \theta} = 0$|
|No end effect|$\frac{\partial v_\theta}{\partial z} = 0$|
|Vertical orientation|$g_z = -g, g_\theta = g_r = 0$|

|Description|Equations|
|-:|:-|
|$r$-momentum equation|$-\rho\dfrac{v_\theta^2}{r} = -\dfrac{\partial p}{\partial r}$|
|$\theta$-momentum equation|$\mu\dfrac{\partial}{\partial r} \left( \dfrac{1}{r}\dfrac{\partial}{\partial r} (rv_\theta) \right) = 0$|
|$z$-momentum equation|$-\dfrac{\partial p}{\partial z} - \rho g = 0$|
|Velocity profile (general form)|$v_\theta(r) = c_1\dfrac{r}{2} + \dfrac{c_2}{r}$|
|Velocity profile|$v_\theta(r) = \dfrac{\Omega_0}{1 - \kappa^2}\left[r - \dfrac{(\kappa R)^2}{r}\right]$|
|Pressure profile|$P - P_{\kappa R} = \dfrac{1}{2}\rho \left(\dfrac{\Omega_0\kappa R}{1-\kappa^2}\right)^2 \left[\left(\dfrac{r}{\kappa R}\right)^2 - \left(\dfrac{\kappa R}{r}\right)^2 - 4\ln\left(\dfrac{r}{\kappa R}\right) \right]$|
|Shear stress distribution|$\tau_{r\theta} = -2\mu\kappa^2\left(\dfrac{\Omega_0}{1-\kappa^2}\right)\left(\dfrac{R}{r}\right)^2$|
|**Torque**|$\mathcal{T} = 4\pi\mu L \Omega_0 R^2\dfrac{\kappa^2}{1 - \kappa^2}$|
|**Couette viscometer**|$\mu = \dfrac{\mathcal{T}}{4\pi L \Omega_0 R^2}\dfrac{1 - \kappa^2}{\kappa^2}$|

### Stoke's law: Flow around a sphere

|Assumptions|Equations|
|-:|:-|
|Spherical coordinates|$f(r, \theta, \phi)$|
|Constant $\rho, \mu$|$\frac{\partial \rho}{\partial t} = 0, \frac{\partial \mu}{\partial t} = 0$|
|Laminar flow|$\mathrm{Re} < \mathrm{Re}_{\text{cr}}$|
|Steady state|$\frac{\partial}{\partial t} = 0$|
|Axial symmetry|$\frac{\partial}{\partial \phi} = 0$|
|No spinning|$v_\phi = 0$|
|Vertical orientation|$g_r = -g \cos\theta, g_\theta = g \sin\theta, g_\phi = 0$|
|$v_\theta$ component only|$v_r = v_z = 0$|

|Description|Equations|
|-:|:-|
|$r$ velocity profile|$v_r = v_\infty \left[ 1 - \dfrac{3}{2}\left(\dfrac{R}{r}\right) + \dfrac{1}{2}\left(\dfrac{R}{r}\right)^2 \right] \cos\theta$|
|$\theta$ velocity profile|$v_\theta = -v_\infty \left[ 1 - \dfrac{3}{4}\left(\dfrac{R}{r}\right) - \dfrac{1}{4}\left(\dfrac{R}{r}\right)^3 \right] \sin\theta$|
|Pressure profile|$p = p_0 - \rho gz - \dfrac{3}{2}\dfrac{\mu v_\infty}{R}\left(\dfrac{R}{r}\right)^2 \cos\theta$|
|Viscous drag|$4\pi\mu v_\infty R$|
|Pressure force (buoyancy + form frag)|$\frac{4}{3}\pi R^3 \rho g + 2\pi R \mu v_\infty$|
|**Stoke's law**|$v_\infty = \dfrac{2R^2 (\rho_s - \rho)g}{9\mu}$|
|**Falling ball viscometer**|$\mu = \dfrac{2R^2 (\rho_s - \rho)g}{9 v_\infty}$|

### Centrifuge viscometer

|Description|Equations|
|-:|:-|
|Terminal velocity|$v_\infty = \dfrac{2R^2 (\rho_s - \rho) \omega ^2r}{9\mu}$|
|**Centrifuge viscometer**|$\mu = \dfrac{2R^2 (\rho_s - \rho)\omega^2}{9 \ln\left(\frac{R_2}{R_1}\right)} \Delta t$|

## Turbulence

### Transition to turbulence

|Geometry|Reynolds Number|Critical Reynolds Number|
|-:|:-|:-|
|Circular tube flow|$\mathrm{Re} = \dfrac{D \langle v \rangle \rho}{\mu}$|$\mathrm{Re_c} \approx 2100$|
|Falling film|$\mathrm{Re} = \dfrac{4 \delta \langle v \rangle \rho}{\mu}$|$\mathrm{Re_c} \approx 1500$|
|Flow between parallel plates|$\mathrm{Re} = \dfrac{2b \langle v \rangle \rho}{\mu}$|$\mathrm{Re_c} \approx 1780$|
|Tangential flow in an annulus (Couette flow between rotating cylinders)|$\mathrm{Re} = \dfrac{\Omega_0 R^2 \langle v \rangle \rho}{\mu}$|$\mathrm{Re_c} \approx 50000$|

### Laminar vs. turbulent

|Property|Laminar Flow $(\mathrm{Re} < 2100)$|Turbulent Flow $(\mathrm{Re} \in [10^4, 10^5])$|
|-:|:-|:-|
|Velocity profile|$\dfrac{v_z}{v_{z, \max}} = 1 - \left(\dfrac{r}{R}\right)^2$|$\dfrac{v_z}{v_{z, \max}} \approx \left(1 - \dfrac{r}{R}\right)^{1/7}$|
|Average velocity|$\langle v_z \rangle = \frac{1}{2}v_{z, \max}$|$\langle v_z \rangle \approx \frac{4}{5}\bar{v}_{z, \max}$|
|Volumetric flow rate|$Q = \dfrac{\pi R^4}{8\mu} \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)$|$Q \propto \left(\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right)^{4/7}$|
|Entry length|$L_e = 0.035 D \mathrm{Re}$|$L_e \approx 40D$|
|Derivation|From theory|From experiment|

|Description|Equations|
|-:|:-|
|Velocity decomposition|$v_z = \bar{v}_z + v_z'$|
|Velocity profile in turbulent flow|$\bar{v}\_z = \bar{v}_{z, \max}\left(1 - \dfrac{r}{R}\right)^{1/n}$ <br/> $n = \begin{cases} 6 & \mathrm{Re} \in [2\times 10^3, 10^4] \\\ 7 & \mathrm{Re} \in [10^4, 10^5] \\\ 8 & \mathrm{Re} \in [10^5, 10^6] \end{cases}$|

### Time-smoothed N-S equation

|Description|Equations|
|-:|:-|
|Time-smoothed continuity equation|$\nabla\cdot\utilde{\bar{v}} = 0 \newline \nabla\cdot\utilde{v}' = 0$|
|Time-smoothed equation of motion ($\tau$-form)|$\rho\dfrac{D\utilde{\bar{v}}}{Dt} = -\nabla \bar{p} - \nabla\cdot\underset{\approx}{\bar{\tau}}^{\text{total}} + \rho g$|
|Time-smoothed equation of motion ($x$-component)|$\begin{aligned} &\rho \left[ \dfrac{\partial \bar{v}\_x}{\partial t} + \utilde{\bar{v}}\cdot\nabla \bar{v}\_x \right] \\\ =& -\dfrac{\partial \bar{p}}{\partial x} - \left[ \dfrac{\partial \bar{\tau}^{\text{total}}\_{xx}}{\partial x} + \dfrac{\partial \bar{\tau}^{\text{total}}\_{yx}}{\partial y} + \dfrac{\partial \bar{\tau}^{\text{total}}\_{zx}}{\partial z} \right] + \rho g_x \end{aligned}$|
|Total shear stress (viscous + turbulent)|$\begin{aligned} \bar{\tau}^{\text{total}}\_{yx} &= \bar{\tau}\_{yx}^{(v)} + \bar{\tau}\_{yx}^{(t)} \\\ &= \bar{\tau}\_{yx} + \rho \overline{v_y' v_x'} \end{aligned}$|

### Shear stress distribution

|Description|Equations|
|-:|:-|
|Shear stress distribution in round tube|$\tau_{r\theta} = \dfrac{1}{2}\left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right]r$|
|Shear stress distribution in general conduit|$\tau_{r\theta} = \left[\dfrac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] R_H$|
|Hydraulic radius|$R_H = \mathrm{\dfrac{cross \ sectional \ area}{wetted \ perimeter}}$|
|Characteristic length|$l_{\text{char}} = 4R_H$|
|Characteristic velocity|$v_{\text{char}} = \langle v_z \rangle$|

### Universal velocity profile

|Layer|Normalized velocity|Normalized length range|
|-:|:-|:-|
|Laminar sublayer|$v^+ = y^+$|$y^+ \in (0, 5)$|
|Buffer layer|$v^+ = 5 \ln(y^+ + 0.205) - 3.27$|$y^+ \in (5, 30)$|
|Turbulent core|$v^+ = 2.5 \ln(y^+) + 5.5$|$y^+ \in (30, \infty)$|

|Description|Equations|
|-:|:-|
|Characteristic length|$y_* = \dfrac{\mu}{v_* \rho}$|
|Characteristic velocity|$v_* = \sqrt{\dfrac{\tau^0}{\rho}}$|
|Normalized length|$y^+ = \dfrac{y}{y_*}$|
|Normalized velocity|$v^+ = \dfrac{v}{v_*}$|
|Eddie viscosity|$\mu^{(t)} = - \dfrac{\bar{\tau}_{yz}^{\text{total}}}{\left(\frac{dv_z}{dy}\right)} - \mu = - \dfrac{\left[\frac{\mathcal{P}_0 - \mathcal{P}_1}{L}\right] \frac{r}{2}}{\left(\frac{dv_z}{dy}\right)} - \mu$|

## Dynamic Similarity and Dimensional Analysis

### Flow around a sphere outside of Stoke's law

|Description|Equations|
|-:|:-|
|★ Non-Stoke's law condition|$\mathrm{Re} \ge 0.1$|
|Nondimensionalized continuity equation|$\breve{\nabla}\cdot\utilde{\breve{v}} = 0$|
|x-component of momentum equation|$\dfrac{D\breve{v}_x}{D\breve{t}} = -\dfrac{\partial\breve{p}}{\partial\breve{x}} + \dfrac{1}{\mathrm{Re}}\breve{\nabla}^2 \breve{v}_x + \dfrac{1}{\mathrm{Fr}}\breve{g}_x$|
|Drag coefficient <br/> Friction factor|$c_D = f = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}$|
|Drag coefficient in Stoke's law region|$c_D = \dfrac{24}{\mathrm{Re}}$|
|Drag coefficient in non-Stoke's law region|$c_D = \left(\sqrt{\dfrac{24}{\mathrm{Re}}} + 0.5407\right)^2$|

#### Dimensionless groups

|Description|Equations|
|-:|:-|
|Reynolds number|$\mathrm{Re} = \dfrac{l_0 v_0 \rho}{\mu} = \mathrm{\dfrac{inertial \ forces}{viscous \ forces}}$|
|Froude number|$\mathrm{Fr} = \dfrac{v_0^2}{gl_0} = \mathrm{\dfrac{inertial \ forces}{gravitational \ forces}}$|
|Capillary number|$\mathrm{Ca} = \dfrac{\mu v_0}{\sigma} = \mathrm{\dfrac{viscous \ forces}{surface \ tension \ forces}}$|
|Weber number|$\mathrm{Fr} = \dfrac{l_0 \rho v_0^2}{\sigma} = \mathrm{\dfrac{inertial \ forces}{surface \ tension \ forces}}$|
|Euler's number|$\mathrm{Eu} = \dfrac{(\Delta p)D^4}{\rho Q^2}$|

### Dimensional analysis

- *Buckingham $\pi$ theorem* - A function $f(X_1, X_2, \dots, X_k)$ with dimensional variables $X_i$ can be rewritten in a function $\Phi(\Pi_1, \Pi_2, \dots, \Pi_{k-n})$ with dimensionless variables $\Pi_j$ by enforcing dimensional consistency using $n$ fundamental dimensions.
  - Define fundamental dimensions
  - Choose stand-in variables for fundamental dimensions
  - Rewrite other variables in terms of stand-in variables to get dimensionless groups

## Bernoulli Analysis and Applications

### N-S equation for steady flow in stream tubes

|Assumptions|Equations|
|-:|:-|
|Constant density fluid|$\Delta \rho = 0$|
|1D flow in $z$ direction|$v_r = v_\theta = 0$|
|Plug flow - uniform velocity across cross section|$\langle v \rangle = v = \mathrm{constant} \newline v_z = v_z(z)$|
|Inviscid flow|$\mu \approx 0, \mathrm{Re} \ge 10000$|
|No sharp bends|Straight stream lines|

|Description|Equations|
|-:|:-|
|Continuity equation|$\begin{aligned} Q_1 &= Q_2 \\\ A_1 \langle v \rangle_1 &= A_2 \langle v \rangle_2 \end{aligned}$|
|Equation of motion|$\rho v \dfrac{dv}{dz} = -\dfrac{dp}{dz} - \rho g \dfrac{dh}{dz}$|

### Bernoulli equation

|Description|Equations|
|-:|:-|
|Bernoulli equation (energy form)|$p_1 + \frac{1}{2}\rho v_1^2 + \rho gh_1 = p_2 + \frac{1}{2}\rho v_2^2 + \rho gh_2$|
|Bernoulli equation (head form)|$\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2$|
|Bernoulli head|$\mathcal{B} = \dfrac{v^2}{2g} + \dfrac{p}{\rho g} + h = \mathrm{constant}$|
|Drag coefficient|$c_D = \dfrac{F_D}{\frac{1}{2}\rho v_\infty^2 A_{\text{approach}}}$|
|Lift coefficient|$c_L = \dfrac{F_L}{\frac{1}{2}\rho v_\infty^2 A_{\text{planform}}}$|
|Pressure change in contracting conduit <br/> $\Delta p \equiv p_1 - p_2$|$\Delta p = \dfrac{8\rho Q^2}{\pi^2 D_1^4}\left[\left(\dfrac{D_1}{D_2}\right)^4 - 1\right] + \rho g (h_2 - h_1)$|
|Torricelli's law|$\langle v \rangle = \sqrt{2g\Delta h}$|
|Pressure at stagnation point|$\begin{aligned} p &= p_{\text{static}} + p_{\text{dynamic}} \\\ &= p_{\text{static}} + \textstyle\frac{1}{2}\rho v_\infty^2 \end{aligned}$|

### Flow-metering devices

|Description|Equations|
|-:|:-|
|Manometer equation|$\Delta p = (\rho_\mathrm{m} - \rho)gH$|
|Local velocity <br/> **Pitot tube**|$v = \sqrt{\dfrac{2\Delta p}{\rho}}$|
|Volumetric flow rate <br/> **Venturi meter** $c_0 \in [0.96, 0.98]$ <br/> **Orfice meter** $c_0 \in [0.40, 0.80]$ <br/> **Nozzle meter** $c_0 \in [0.96, 0.98]$|$Q = c_0\pi D_0^2 \sqrt{\dfrac{\Delta p}{8\rho [1 - (\frac{D_0}{D})^4]}}$|
|Rotameter|Calibrated specifically to the fluid with falling sphere|

### Full Bernoulli analysis

|Description|Equations|
|-:|:-|
|Full Bernoulli equation|$\dfrac{v_1^2}{2g} + \dfrac{p_1}{\rho g} + h_1 = \dfrac{v_2^2}{2g} + \dfrac{p_2}{\rho g} + h_2 + H_{L12}$|
|Head loss|$H_{L12} = H_{L12f} + H_{L12c}$|
|Skin friction loss $H_{L12f}$|Viscous work done per unit weight by fluid on walls of conduit in moving from 1 to 2|
|Skin friction loss (general)|$H_{L12f} = \dfrac{\tau^0 L}{\rho g R_H}$|
|Skin friction loss for circular tube|$H_{L12f} = \dfrac{4\tau^0 L}{\rho g D}$|
|Fanning friction factor|$f = \dfrac{\tau^0}{\frac{1}{2}\rho \langle v \rangle^2}$|
|Skin friction loss for circular tube|$H_{L12f} = \dfrac{2\langle v \rangle^2 L}{g D}f = \dfrac{32Q^2 L}{\pi^2 D^5 g}f$|
|Skin friction loss for non-circular tube|$H_{L12f} = \dfrac{\langle v \rangle^2 L}{2 g R_H}f = \dfrac{Q^2 L}{2g A_c^2 R_H}f$|
|Reynolds number for noncircular pipes|$\mathrm{Re} = \dfrac{4R_H \langle v \rangle \rho}{\mu}$|
|Configurational loss of one fitting in circular tube|$H_{Lc} = e_v\dfrac{\langle v \rangle^2_{\text{downstream}}}{2g}$|
|Configurational loss of all fittings in circular tube|$H_{L12c} = \dfrac{\langle v \rangle^2_{\text{down}}}{2g} (\sum\limits_i e_{v, i}) = \dfrac{8Q^2}{\pi^2 D^4 g} (\sum\limits_i e_{v, i})$|
|**Total head loss** for circular tube|$H_{L12} = \begin{cases} \dfrac{2 \langle v \rangle^2}{Dg} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \\\ \dfrac{32 Q^2}{\pi^2 D^5 g} [(\sum\limits_i L_i)f + \frac{D}{4} (\sum\limits_i e_{v, i})] \end{cases}$|
|Kinetic head correction factor|$\alpha = \dfrac{\langle v^3 \rangle}{\langle v \rangle^3}$|
|Brake horse power|$\mathrm{bhp} = \dfrac{P}{\eta} = \dfrac{H_p \rho g Q}{\eta}$|

#### Fanning friction factor correlations

|Description|Equations|Conditions|
|-:|:-|:-|
|Hydraulically smooth pipes (Blasius)|$f = \dfrac{0.0791}{\mathrm{Re}^1/4}$|$\mathrm{Re} \in [2100, 10^5]$|
|Hydraulically smooth pipes (Koo)|$f = 0.0014 + \dfrac{0.125}{\mathrm{Re}^{0.32}}$|$\mathrm{Re} \in [10^4, 10^7]$|
|Pipes of general roughness (Haaland)|$\dfrac{1}{\sqrt{f}} = -3.6\log_{10} \left[\dfrac{6.9}{\mathrm{Re}} + \left(\dfrac{k/D}{3.7}\right)^{10/9}\right]$|$\mathrm{Re} \in [4\times 10^4, 10^7] \newline k/D < 0.05$|
|Commercial standard piping (Drew)|$f = 0.0014 + \dfrac{0.090}{\mathrm{Re}^{0.27}}$|$\mathrm{Re} \in [10^4, 10^7] \newline k/D \approx 0.00015$|
|Full rough conduit|$\dfrac{1}{\sqrt{f}} = 2.28 - 4.0 \log_{10} \left(\dfrac{k}{D}\right)$|$\mathrm{Re} > 10^4 \newline k/D > 0.01$|

#### Kinetic head correction factor

|$\mathrm{Re}$|$n$|$\alpha$|
|-:|:-:|:-|
|$2 \times 10^3 \sim 10^4$|$6$|$1.08$|
|$10^4 \sim 10^5$|$7$|$1.06$|
|$10^5 \sim 10^7$|$8$|$1.05$|

### Flow through packed bed

|Description|Equations|
|-:|:-|
|Specific area of packing element|$a_v = \dfrac{\text{area of packing element}}{\text{volume of packing element}}$|
|Effective diameter of packing element (particle)|$D_p = \dfrac{6}{a_v}$|
|**Darcy's law** <br/> ★ $\mathrm{Re_{bed}} \lesssim 10$|$\langle v \rangle = \dfrac{\kappa}{\mu} \left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right]$|
|Volumetric flow rate|$Q = \langle v \rangle \varepsilon A = v_0 A$|
|Superficial velocity|$v_0 = \langle v \rangle \varepsilon$|
|Bed Reynolds number|$\begin{aligned}\mathrm{Re_{bed}} &= \dfrac{D_p v_0 \rho}{\mu}\dfrac{1}{1 - \varepsilon} \\\ &= \dfrac{D_p \langle v \rangle \rho}{\mu}\dfrac{\varepsilon}{1 - \varepsilon} \\\ &= \dfrac{D_p Q \rho}{\mu A}\dfrac{1}{1 - \varepsilon}\end{aligned} $|
|Tube Reynolds number|$\mathrm{Re_{tube}} = \dfrac{2}{3}\mathrm{Re_{bed}}$|
|Hydrolic radius|$R_H = \dfrac{D_p\varepsilon}{6(1-\varepsilon)}$|
|Friction factor of tube <br/> ★ $\mathrm{Re_{bed}} \le 10$|$f_{\text{tube}} = \dfrac{24(1-\varepsilon)\mu}{D_p v_0 \rho}$|
|Friction factor of tube <br/> ★ $\mathrm{Re_{bed}} > 1000$|$f_{\text{tube}} = \dfrac{7}{12}$|
|Bed permeability|$\kappa = \dfrac{D_p^2}{150} \left(\dfrac{\varepsilon}{1-\varepsilon}\right)^2$|
|**Blake-Kozeny equation** <br/> ★ $\mathrm{Re_{bed}} \le 10$|$\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = 150 \dfrac{\mu v_0}{D_p^2}\dfrac{(1-\varepsilon)^2}{\varepsilon^3}$|
|**Burke-Plummer equation** <br/> ★ $\mathrm{Re_{bed}} > 1000$|$\left[ \dfrac{\mathcal{P}_0 - \mathcal{P}_L}{L} \right] = \dfrac{7}{4}\dfrac{\rho v_0^2}{D_p}\dfrac{1-\varepsilon}{\varepsilon^2}$|
|Superficial mass flux|$G_0 = \rho v_0 = \dfrac{\dot{m}}{A}$|
|**Ergun equation** <br/> ★ $\mathrm{Re_{bed}} \in [10, 1000]$|$\left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \left[ \dfrac{1-\varepsilon}{\frac{D_p G_0}{\mu}} \right] + \dfrac{7}{4} \newline \left[ \dfrac{(\mathcal{P}_0 - \mathcal{P}_L)\rho}{G_0^2} \right] \dfrac{D_p}{L}\dfrac{\varepsilon^3}{1-\varepsilon} = 150 \dfrac{1}{\mathrm{Re\_{bed}}} + \dfrac{7}{4}$|

### Cavitation and vortex motion

|Description|Equations|
|-:|:-|
|Cavitation number|$\sigma = \dfrac{p_A - p_C}{\frac{1}{2}\rho v_\infty^2}$|

#### Forced vortex flow in rotating cylinder

|Description|Equations|
|-:|:-|
|Velocity profile|$v_\theta = r\Omega$|
|Pressure difference <br/> ★ 1 defined arbitrarily, 2 defined at center|$p_2 - p_1 = \dfrac{1}{2}\rho\Omega^2 (r_2^2 - r_1^2) + \rho g (z_1 - z_2)$|
|Height|$h = \dfrac{\Omega^2}{2g} r^2$|

#### Free vortex flow during drainage

|Description|Equations|
|-:|:-|
|Pressure difference  <br/> ★ 1 defined arbitrarily, 2 defined at $r \to\infty$|$p_2 - p_1 = \dfrac{1}{2}\rho C^2 \left(\dfrac{1}{r_1^2} - \dfrac{1}{r_2^2}\right) + \rho g (z_1 - z_2)$|
|Depth|$h = \dfrac{C^2}{2g} \dfrac{1}{r^2}$|

## Microfluidics*

### Validity of continuum description

|Description|Equations|
|-:|:-|
|Mean free path|$\lambda = \dfrac{1}{\sqrt{2}\pi d^2 n} \newline \lambda(\mathrm{\mu m}) \approx 3.1\times 10^{-3} \dfrac{T(\mathrm{K})}{\sigma^2(\mathrm{\mathring{A}^2}) p(\mathrm{atm})}$|
|Knudsen number|$\mathrm{Kn} = \dfrac{\lambda}{L_c}$|

|Characteristics|Range|
|-:|:-|
|Molecular flow|$\mathrm{Kn} \in (10, \infty)$|
|Transition flow|$\mathrm{Kn} \in (0.1, 10)$|
|N-S equations hold, but no-slip condition fails|$\mathrm{Kn} \in (0.001, 0.1)$|
|N-S equations hold, and no-slip condition holds|$\mathrm{Kn} \in (0, 0.001)$|

### Forces in microfluidic flows

- Viscous force dominate over inertial forces and gravity forces
  - Driving force
    - Pressure
    - Capillary (surface tension) forces
    - Electro-kinetic forces
    - Magnetic forces
  - Resisting forces: viscous force, dominated by wall effects

|Description|Equations|
|-:|:-|
|Reynolds number <br/> ★ Creeping flow|$\mathrm{Re} = \dfrac{\text{inertial forces}}{\text{viscous forces}} = \dfrac{Lv\rho}{\mu} \to 0$|
|Froude number|$\mathrm{Fr} = \dfrac{\text{inertial forces}}{\text{gravity forces}} = \dfrac{v^2}{gL}$|
|Viscous force dominates gravity force|$\mathrm{\dfrac{Re}{Fr}} = \dfrac{\text{gravity forces}}{\text{viscous forces}} = \dfrac{gL^2}{\mu v} \to 0$|

### Generalized Hagen-Poiseuille flow

|Description|Equations|
|-:|:-|
|Differential equation of generalized H-P flow|$0 = \dfrac{\Delta p}{L} + \mu \left(\dfrac{\partial^2 v_z}{\partial x^2} + \dfrac{\partial^2 v_z}{\partial y^2}\right)$|
|No-slip condition <br/> $F(x, y)$ is equation of conduit perimeter|$v_z(x, y) = 0 for F(x, y) = 0$|
|Velocity profile|$v_z(x, y) = \dfrac{\Delta p}{\mu L} F(x, y)$|
|Volumetric flow rate|$Q = \dfrac{\Delta p}{\mu L} \displaystyle\iint F(x, y) \ dy\ dx$|

### Hydraulic resistance in micro-channels

|Description|Equations|
|-:|:-|
|Flow equation|$\Delta p = \mathcal{R}_{\text{hyd}}Q$|
|Volumetric flow rate|$Q = \dfrac{\Delta p}{\mathcal{R}_{\text{hyd}}}$|

### Capillary driving force and wicking phenomena

|Description|Equations|
|-:|:-|
|Pressure difference|$\Delta p = \sigma\kappa = \dfrac{2\sigma}{R}$|
|Wicking velocity|$v = \dfrac{r^2}{8\mu}\dfrac{\Delta P}{x} = \dfrac{r\sigma \cos\theta}{4\mu x}$|
|Washburn equation|$x = \sqrt{\dfrac{r\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}$|
|Wicking into porous media|$h = \sqrt{\dfrac{r_e\sigma\cos\theta}{2\mu} t} \propto \sqrt{t}$|
