---
title: "CHEM E 455 Surface and Colloid Science Laboratory"
date: 2022-04-04T00:00:00-08:00
---

## Fluid Interface and Capillarity

### Surface tension

|Description|Equations|
|-:|:-|
|Surface tension|$\sigma = \dfrac{dF}{dl}$|

#### $T$ dependence of $\sigma$

|Description|Equations|
|-:|:-|
|Eotovs law|$\sigma v^{2/3} = k_E (T_c - T)$|
|Guggenheim law|$\sigma = \sigma^* \left(1 - \dfrac{T}{T_c}\right)^{11/9}$|
|Empirical linear equation <br/> ★ Modest T|$\sigma =a-bT \newline b = \dfrac{d\sigma}{dT} = -0.1 \ \mathrm{mM/m \cdot K}$|

#### $\sigma$ and intermolecular forces

|Description|Equations|
|-:|:-|
|van der Waals attraction|$\Phi_{\text{vdW}} = -\dfrac{B_{\text{vdW}}}{r^6}$|
|Born repulsion|$\Phi_{\text{rep}} = \dfrac{B_{\text{rep}}}{r^{12}}$|
|Lennard-Jones potential|$\Phi = 4\varepsilon \left[\left(\dfrac{\delta }{r}\right)^{12}-\left(\dfrac{\delta }{r}\right)^6\right]$|
|Lennard-Jones attractive force|$F_{\text{attr}} = -\dfrac{24\varepsilon }{r}\left[2\left(\dfrac{\delta }{r}\right)^{12}-\left(\dfrac{\delta }{r}\right)^6\right]$|
|**Bakker's equation**|$\sigma = \displaystyle\int_{-\infty}^\infty (p - p_T) dz$|

#### Components of $\sigma$

|Description|Equations|
|-:|:-|
|Components of surface tension|$\sigma = \sigma^{\text{disperison}} + \sigma^{\text{dipole}} + \sigma^{\text{induced dipole}} + \sigma^{\text{H-bond}} + \sigma^{\text{metallic bond}} + \cdots$|
|Surface tension of liquid|$\sigma = \sigma^{\text{disperison}} + \sigma^{\text{acid-base}}$|
|Surface tension of molten salt|$\sigma = \sigma^{\text{disperison}} + \sigma^{\text{metallic bond}}$|

#### Combining rules of $\sigma$

|Description|Equations|
|-:|:-|
|Antanov|$\sigma_{AB} = \vert \sigma_{A(B)} - \sigma_{B(A)} \vert$|
|Girifalco & Good|$\sigma_{AB} = \sigma_A + \sigma_B - 2\Phi \sqrt{\sigma_A \sigma_B}$|
|Fowkes|$\sigma_{AB} = \sigma_A + \sigma_B - 2 \sqrt{\sigma_A^d \sigma_B^d}$|

### Young-Laplace equation

#### Curvature in 2D

|Description|Equations|
|-:|:-|
|Curvature of a plane curve|$\kappa = \dfrac{d\phi}{dS}$|
|Curvature of a plane curve|$\kappa = \pm y'' [1+(y')^2]^{-3/2}$|
|Curvature of a line|$\kappa = 0$|
|Curvature of a circle|$\kappa = \dfrac{1}{R}$|

#### Curvature in 3D

|Description|Equations|
|-:|:-|
|Curvature of a surface|$\kappa = \pm \left(\dfrac{1}{R_1}+\dfrac{1}{R_2}\right)=\pm \dfrac{2}{R_{\text{mean}}}$|
|Curvature of a surface|$\kappa = \pm \dfrac{z_{xx}\left[1+\left(z_y\right)^2\right]-2z_xz_yz_{xy}+z_{yy}\left[1+\left(z_x\right)^2\right]}{\left[1+\left(z_x\right)^2+\left(z_y\right)^2\right]^{3/2}}$|
|Curvature of a sphere|$\kappa = \dfrac{2}{R}$|
|Curvature of a circular cylinder|$\kappa = \dfrac{1}{R}$|
|Curvature of a cylindrical surface|$\kappa = \pm y'' [1+(y')^2]^{-3/2}$|
|Curvature of an axially symmetric surface|$\kappa = $|

#### Young-Laplace equation

|Description|Equations|
|-:|:-|
|**Young-Laplace equation**|$\Delta p = p'' - p' = \sigma\kappa$|

<!-- ★ -->