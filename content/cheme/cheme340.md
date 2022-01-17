---
title: "CHEM E 340 Transport Process II"
date: 2022-01-16T00:00:00-08:00
---

## Modes of Heat Transfer

### Conduction

|Description|Equations|
|-:|:-|
|Heat rate|$\mathbf{q} = \mathbf{q''}A$|
|Fourier's law (conduction)|$\mathbf{q''} = -k \nabla T$|
|Fourier's law (conduction)|$q_x'' = -k \dfrac{dT}{dx}$|

### Convection

|Description|Equations|
|-:|:-|
|Newton's law of cooling (convection)|$q'' = h (T_s - T_\infty)$|

### Radiation

|Description|Equations|
|-:|:-|
|Stefan-Boltzman's law (radiation)|$E_b = \varepsilon\sigma T_s^4$|
|Gray body|$\varepsilon = \alpha$|
|Blackbody|$\varepsilon = \alpha = 1$|
|Irradiation from isothermal surrounding|$G = \sigma T_{\text{surr}}^4$|
|Absorbed irradiation|$G_{\text{abs}} = \alpha G$|
|Net heat flux from radiation|$q_{\text{rad}}'' = \varepsilon\sigma T_s^4 - \alpha G$|
|Net heat flux from radiation <br/> ★ gray surface, isothermal surrounding $T_{\text{surr}}$|$q_{\text{rad}}'' = \varepsilon\sigma (T_s^4 - T_{\text{surr}}^4)$|
|Net heat flux from radiation in rate law form|$q_{\text{rad}}'' = h_{\text{rad}} (T_s - T_{\text{surr}}) \newline h_{\text{rad}} = \varepsilon\sigma (T_s + T_{\text{surr}})(T_s^2 + T_{\text{surr}}^2)$|

### Energy balance

|Description|Equations|
|-:|:-|
|Total energy balance|$\text{In - Out + Generation = Accumulation}$|
|Total energy balance|$E_{\text{in}} - E_{\text{out}} + E_{\text{gen}} = \Delta E_{\text{acc}}$|
|Total energy balance|$\dot{E}\_{\text{in}} - \dot{E}\_{\text{out}} + \dot{E}\_{\text{gen}} = \dot{E}\_{\text{acc}} = \dfrac{d E_{\text{acc}}}{dt}$|
|Surface energy balance <br/> ★ $\dot{E}\_{\text{gen}} = \dot{E}\_{\text{acc}} = 0$|$\dot{E}\_{\text{in}} = \dot{E}\_{\text{out}}$|

## Heat Diffusion Equation

|Description|Equations|
|-:|:-|
|Heat Diffusion Equation|$\nabla^2 T + \dfrac{\dot{q}}{k} = \dfrac{1}{\alpha}\dfrac{\partial T}{\partial t}$|
|Heat Diffusion Equation|$\nabla \cdot q'' = \dot{q} - \rho c_P\dfrac{\partial T}{\partial t}$|
|Heat Diffusion Equation|$\dfrac{\partial T}{\partial t} = \alpha\nabla^2 T + \dfrac{\dot{q}}{\rho c_P}$|
|Volumetric heat generation|$\dot{q}$|
|Volumetric heat capacity (storage)|$\rho c_P$|
|Thermal diffusivity|$\alpha = \dfrac{k}{\rho c_P}$|

### Cartesian coordinates

|Direction|Heat flux|Differential Area|
|-:|:-|:-|
|$x \in (-\infty, \infty)$|$q_x'' = -k \frac{\partial T}{\partial x}$|$dA = dydz$|
|$y \in (-\infty, \infty)$|$q_y'' = -k \frac{\partial T}{\partial y}$|$dA = dxdz$|
|$z \in (-\infty, \infty)$|$q_z'' = -k \frac{\partial T}{\partial z}$|$dA = dxdy$|

$$
\dfrac{\partial}{\partial x} \left( k \dfrac{\partial T}{\partial x} \right) +
\dfrac{\partial}{\partial y} \left( k \dfrac{\partial T}{\partial y} \right) +
\dfrac{\partial}{\partial z} \left( k \dfrac{\partial T}{\partial z} \right) +
\dot{q} = \rho c_P \dfrac{\partial T}{\partial t}
$$

### Cylindrical coordinates

|Direction|Heat flux|Differential Area|
|-:|:-|:-|
|$r \in [0, \infty)$|$q_r'' = -k \frac{\partial T}{\partial r}$|$dA = r \ d\phi dz$|
|$\phi \in [0, 2\pi]$|$q_\phi'' = -k \frac{1}{r}\frac{\partial T}{\partial \phi}$|$dA = drdz$|
|$z \in [-\infty, \infty)$|$q_z'' = -k \frac{\partial T}{\partial z}$|$dA = r \ drd\phi$|

$$
\dfrac{1}{r}\dfrac{\partial}{\partial r} \left( k r\dfrac{\partial T}{\partial r} \right) +
\dfrac{1}{r^2}\dfrac{\partial}{\partial \phi} \left( k \dfrac{\partial T}{\partial \phi} \right) +
\dfrac{\partial}{\partial z} \left( k \dfrac{\partial T}{\partial z} \right) +
\dot{q} = \rho c_P \dfrac{\partial T}{\partial t}
$$

### Spherical coordinates

|Direction|Heat flux|Differential Area|
|-:|:-|:-|
|$r  \in [0, \infty)$|$q_r'' = -k \frac{\partial T}{\partial r}$|$dA = r^2 \sin\theta \ d\theta d\phi$|
|$\theta  \in [0, 2\pi]$|$q_\theta'' = -k \frac{1}{r}\frac{\partial T}{\partial \theta}$|$dA = r\sin\theta drd\phi$|
|$\phi  \in [0, \pi]$|$q_\phi'' = -k \frac{1}{r \sin\theta}\frac{\partial T}{\partial \phi}$|$dA = r \ drd\theta$|

$$
\dfrac{1}{r^2}\dfrac{\partial}{\partial r} \left( k r^2 \dfrac{\partial T}{\partial r} \right) +
\dfrac{1}{r^2 \sin\theta}\dfrac{\partial}{\partial \theta} \left( k \sin\theta \dfrac{\partial T}{\partial \theta} \right) +
\dfrac{1}{r^2 \sin^2\theta}\dfrac{\partial}{\partial \phi} \left( k \dfrac{\partial T}{\partial \phi} \right) +
\dot{q} = \rho c_P \dfrac{\partial T}{\partial t}
$$

<!-- ★ -->
