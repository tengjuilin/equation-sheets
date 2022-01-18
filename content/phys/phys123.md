---
title: "PHYS 123 Waves"
date: 2021-08-17T00:00:00+08:00
---

## Periodic Motion

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Period|$\mathrm{s}$|$T = \dfrac{1}{f} = \dfrac{2\pi}{\omega}$|
|Frequency|$\mathrm{Hz}$|$f = \dfrac{1}{T} = \dfrac{\omega}{2\pi}$|
|Angular frequency|$\mathrm{s^{-1}}$|$\omega = 2\pi f = \dfrac{2\pi}{T}$|

### Simple harmonic motion (SHM)

|Description|Equations|
|-:|:-|
|Angular frequency in SHM|$\omega = \sqrt{\dfrac{k}{m}}$|
|Spring constant|$k = m\omega^2$|
|Displacement in SHM|$x(t) = A\sin(\omega t + \phi)$|
|Velocity in SHM|$v(t) = \omega A\cos(\omega t + \phi)$|
|Acceleration in SHM|$a(t) = -\omega^2 A\sin(\omega t + \phi) = -\omega^2 x(t)$|
|Restoring force in SHM|$F = -k\Delta x$|
|Simple harmonic oscillator equation|$\frac{d^2 x}{dt^2} = -\omega^2 x = -\frac{k}{m}x$|
|Conservation of energy in SHM|$E = \frac{1}{2}mv^2 + \frac{1}{2}kx^2 = \frac{1}{2}kA^2$|
|Amplitude|$A = \sqrt{x_0^2 + \dfrac{v_0^2}{\omega^2}}$|
|Phase angle|$\phi = \arctan\left(\dfrac{\omega x_0}{v_0}\right)$|

### Applications of SHM

|Description|Equations|
|-:|:-|
|Restoring torque in angular SHM|$\tau = -\kappa\Delta\theta$|
|Rotational displacement in angular SHM|$\theta(t) = \theta_{\mathrm{max}}\sin(\omega t + \phi)$|
|Angular frequency in angular SHM|$\omega = \sqrt{\dfrac{\kappa}{I}}$|
|Angular frequency in simple pendulum|$\omega = \sqrt{\dfrac{g}{L}}$|
|Angular frequency in physical pendulum|$\omega = \sqrt{\dfrac{mgL}{I}}$|

### Damped oscillation

|Description|Equations|
|-:|:-|
|Drag force|$F = -bv$|
|Time constant|$\tau = \dfrac{m}{b}$|
|Angular frequency of damped oscillator|$\omega_d = \sqrt{\omega^2 - \left(\frac{b}{2m}\right)^2}$|
|Displacement of damped oscillator|$x(t) = Ae^{-bt/2m}\sin(\omega_d t + \phi)$|

## 1D Waves

|Description|Equations|
|-:|:-|
|Wave speed, wavelength, and frequency|$c = \lambda f = \dfrac{\lambda}{T}$|
|Wave number|$k = \dfrac{2\pi}{\lambda}$|
|Angular frequency|$\omega = kc = 2\pi f$|
|Linear mass density|$\mu = \dfrac{m}{l}$|s
|Wave speed of strings|$c = \sqrt{\dfrac{F_T}{\mu}}$|
|Particle speed|$v = \frac{\partial f}{\partial t}$|
|Wave and particle speed|$c \not= v$|
|Energy put into a wave|$E = \frac{1}{2}\mu\lambda\omega^2A^2$|
|Average power supplied to produce waves|$\begin{aligned}\overline{P} &= \mu cv^2 \cr &= \frac{1}{2}\mu c A^2\omega^2 \cr &= \frac{1}{2}\sqrt{\mu F_T}\omega^2A^2\end{aligned}$|
|Wave kinetic and potential energy|$K = U$|

### Wave function and boundary conditions

|Description|Equations|
|-:|:-|
|Traveling wave functions|$f(x,t) = f(x - ct)$ to right <br/> $f(x,t) = f(x + ct)$ to left|
|Harmonic (sinusoidal) traveling wave functions|$f(x,t) = A\sin(kx-\omega t+\phi)$ to right <br/> $f(x,t) = A\sin(kx+\omega t+\phi)$ to left|
|1D wave equation|$\dfrac{\partial^2 f}{\partial x^2} = \dfrac{1}{c^2}\dfrac{\partial^2 f}{\partial t^2}$|
|Principle of superposition|$f(x,t) = f_1(x,t)+f_2(x,t)$|
|Boundary conditions|Free end: heavy $\rightarrow$ light spring <br/> Fixed end: light $\rightarrow$ heavy spring|
|Shape of reflected wave|Free end: horizontal reflection only <br/> Fixed end: horizontal reflection,  vertical inversion|
|Shape of transmitted wave|Similar to incident wave|

### Standing waves

|Description|Equations|
|-:|:-|
|Standing wave function|$f(x,t) = 2A\sin(kx)\cos(\omega t)$|
|**Standing wave of strings <br/> *with two fixed ends***|$n$th harmonic, $n$ antinodes, $n+1$ nodes|
|Wavelength of $n$th harmonic|$\lambda_n = \dfrac{2L}{n}$|
|Frequency of $n$th harmonic|$f_n = n\dfrac{c}{2L} = nf_1$|
|Location of $m$th node of $n$th harmonic|$x_m = \dfrac{m\lambda_n}{2} \newline m \in [0, n+1]$|

## 2D and 3D Waves

|Quantity|Unit|Definition|
|---:|:-:|:---|
|2D intensity|$\mathrm{W/m}$|$I = \dfrac{P}{L} = \dfrac{P}{2\pi r}$|
|3D intensity|$\mathrm{W/m^2}$|$I = \dfrac{P}{A} = \dfrac{P}{4\pi r^2}$|
|Intensity level|$\mathrm{dB}$|$\beta = (10 \ \mathrm{dB})\log\left(\dfrac{I}{I_{\text{th}}}\right) \newline I_{\text{th}} = 10^{-12} \ \mathrm{W/m^2}$|

|Description|Equations|
|-:|:-|
|Path difference of constructive interference (in phase, at antinodal line)|$\delta = n\lambda$|
|Path difference of destructive interference (out of phase, at nodal line)|$\delta = (n - \frac{1}{2})\lambda$|
|Beat frequency|$f_b = \lvert f_1 - f_2 \rvert$|
|Average frequency|$\overline{f} = \frac{1}{2}(f_1 + f_2)$|
|Wave function of beats|$\begin{aligned}y(x, t) &= y_1 + y_2 \cr &= 2A \cos(2\pi \frac{1}{2}f_b t)\sin(2\pi\overline{f}t)\end{aligned}$|
|Doppler effect $(v_s < c)$ <br/> s - source; o - observer; rel to medium|$\dfrac{f_{\mathrm{o}}}{f_{\mathrm{s}}} = \dfrac{c \pm v_{\mathrm{o}}}{c \pm v_{\mathrm{s}}}$|
|Angle of shock wave $(v_s > c)$|$\sin\theta = \dfrac{c}{v_s}$|
|Mach number|$\footnotesize\text{Mach number} = \dfrac{v_s}{c}$|

## Ray Optics (Geometric Optics)

|Description|Equations|
|-:|:-|
|Law of reflection|$\theta_1 = \theta_2$|
|Refraction index|$n_1 c_1 = n_2 c_2$|
|Wavelength of light in a new medium|$n_1\lambda_1 = n_2\lambda_2$|
|**Snel's law**|$n_1\sin\theta_1 = n_2\sin\theta_2$|
|Critical angle <br/> $(n_2>n_1)$|$\arcsin\left(\dfrac{n_1}{n_2}\right)$|
|**Lens equation** <br/> o - object; i - image|$\dfrac{1}{f} = \dfrac{1}{d_\text{o}} + \dfrac{1}{d_\text{i}}$|
|Magnification|$M = \dfrac{h_\text{i}}{h_\text{o}} = -\dfrac{d_\text{i}}{d_\text{o}}$|
|Radius of curvature (distance of center) of mirror and focal length|$R = 2\lvert f \rvert$|
|Angular magnification|$M_\theta = \bigg\lvert\dfrac{\theta_\text{i}}{\theta_\text{o}}\bigg\rvert$|
|Small-angle (paraxial) approximation of angular magnification|$M_\theta = \dfrac{0.25 \ \mathrm{m}}{f}$|
|Lens strength|$d = \dfrac{1 \ \mathrm{m}}{f}$|

### Lens/mirror equation sign convention

|Sign|Lens|
|-:|:-|
|$f>0 \newline f<0$|converging lens <br/> diverging lens|
|$d_\text{o}>0 \newline d_\text{o}<0$|object in front of lens <br/> object behind lens|
|$d_\text{i}>0 \newline d_\text{i}<0$|image behind lens (in front of mirror) <br/> image in front of lens (behind mirror)|
|$h_\text{i}>0 \newline h_\text{i}<0$|image upright <br/> image inverted|
|$\lvert M \rvert>1 \newline \lvert M \rvert<1$|image larger than object <br/> image smaller than object|

### Converging lens images

|Object distance $d_\text{o}$|Image distance $\lvert d_\text{i}\rvert$|Image location|Upright <br/> Inverted|Magnification|Real/Virtual|
|:-:|:-:|:-:|:-:|:-:|:-:|
|$(0, f)$|$\lvert d_\text{i} \lvert>f$|Same|Upright|Magnified|Virtual|
|$f$|$\infty$|-|-|-|Parallel light|
|$(f, 2f)$|$(2f, \infty)$|Opposite|Inverted|Magnified|Real|
|$2f$|$2f$|Opposite|Inverted|Same|Real|
|$(2f, \infty)$|$(f, 2f)$|Opposite|Inverted|Demagnified|Real|
|$\infty$|$f$|Opposite|-|-|Point|

### Diverging lens images

|Object distance $d_\text{o}$|Image distance $\lvert d_\text{i}\rvert$|Image Location|Upright/ <br/> Inverted|Magnification|Real/Virtual|
|:-:|:-:|:-:|:-:|:-:|:-:|
|$(0, \infty)$|$\lvert d_\text{i}\rvert<d_\text{o}$|Same|Upright|Demagnified|Virtual|

## Wave and Particle Optics

### Single slit interference

|Description|Equations|
|-:|:-|
|Variables|$n = 1, 2, 3, ... \newline a =$ width of the slit|
|Destructive interference|$a\sin\theta = \pm n\lambda$|
|Location of destructive interference <br/> (only for small angles)|$y_n = \pm n\dfrac{\lambda L}{a}$|

### Double slit interference

|Description|Equations|
|-:|:-|
|Fringe order|$m = 0, 1, 2, ... \newline n = 1, 2, 3, ...$|
|Constructive interference|$d\sin\theta = \pm m\lambda$|
|Destructive interference|$d\sin\theta = \pm(n-\frac{1}{2})\lambda$|
|Distance between adjacent maxima|$D = \dfrac{L\lambda}{d}$|

### Multiple slit interference

|Description|Equations|
|-:|:-|
|Variables|$m = 0, 1, 2, ...$ $\newline N =$ number of slits $\newline k =$ integer not multiple of $N$|
|Constructive interference (principal maxima)|$d\sin\theta = \pm m\lambda$|
|Destructive interference (minima)|$d\sin\theta = \pm\dfrac{k}{N}\lambda$|
|Minima adjacent to principle maxima|$d\sin\theta = \pm \dfrac{mN+1}{N}\lambda$|
|Phasors|$\delta\varphi = 2\pi\dfrac{\delta s}{\lambda}$|

### Thin-film interference

Note: constructive and destructive interference refers to reflected light, not transmitted light.

|Description|Equations|
|-:|:-|
|Thin-film interference <br/> $t$ - thickness <br/> $m = 0, 1, 2, ...$ <br/> a - incident medium <br/> b - thin film medium <br/> c - transmitted medium|$\phi = \dfrac{4\pi n_b t\cos\theta_b}{\lambda_a} + \phi_{r2} - \phi_{r1} \newline$ $\phi = \begin{cases} 2m\pi & \small\text{constructive} \cr (2m+1)\pi & \small\text{destructive} \end{cases} \newline$ $\phi_{r} = \begin{cases} 0 & n_i>n_f \cr \pi & n_i<n_f \end{cases}$|
|Constructive interference if in phase <br/> (If $\pi$-shifted, use destructive condition)|$2t = m\lambda_b = m\dfrac{n_a}{n_b}\lambda_a$|
|Destructive interference if in phase <br/> (If $\pi$-shifted, use constructive condition)|$2t = (m+\frac{1}{2})\lambda_b = (m+\frac{1}{2})\dfrac{n_a}{n_b}\lambda_a$|

### Circular aperture

|Description|Equations|
|-:|:-|
|Variables|$d$ - diameter of the circular aperture <br/> $f$ - focal distance of the lens|
|First minimum with circular aperture|$\sin\theta = 1.22\dfrac{\lambda}{d}$|
|Angular resolution <br/>Rayleigh's criterion of resolution angle|$\theta \approx \sin\theta = 1.22\dfrac{\lambda}{d}$|
|Linear resolution <br/> Radius of the first minimum by a lens|$y = 1.22\dfrac{\lambda f}{d}$|

### Wave-particle duality

|Description|Equations|
|-:|:-|
|Bragg's condition with Bragg angle <br/> X-ray diffraction|$2d\sin\alpha = m\lambda \newline (2d\cos\theta = m\lambda, \alpha = 90^\circ - \theta)$|
|Energy of a photon|$E = h\nu$|
|Momentum of a photon|$p = \dfrac{h\nu}{c}$|
|Wavelength of a particle|$\lambda = \dfrac{h}{p} = \dfrac{h}{mv}$|
|Photoelectric effect|$E_k = h\nu - \Phi = eV_{\text{stop}}$|
|Stopping potential|$V_{\text{stop}} = \dfrac{h\nu}{e} - \dfrac{\Phi}{e}$|
|Intensity of light|$I \propto$ rate of electron emitted from the metal|

## Fluid Mechanics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Density|$\mathrm{kg/m^3}$|$\rho = \dfrac{m}{V}$|
|Pressure|$\mathrm{Pa} \newline \mathrm{N/m^2}$|$P = \dfrac{dF}{dA}$|
|Volumetric flow rate|$\mathrm{m^3/s}$|$Q = \dot{V} = \dfrac{dV}{dt}$|

|Description|Equations|
|-:|:-|
|Pressure of stationary fluid|$P = P_{\text{surf}} + \rho gh$|
|Pressure of stationary fluid|$P_1 + \rho gy_1 = P_2 + \rho gy_2$|
|Buoyant force|$F_b = F_{\text{bottom}} - F_{\text{top}}$|
|**Archimedes' principle**|$F_b = \rho_f gV_{\text{disp}}$|
|Volume of displaced fluid of floating object|$V_{\text{disp}} = \dfrac{\rho_o}{\rho_f}V_o$|
|Condition of object buoyancy <br/> o - object; f - fluid|$\begin{cases}\rho_o < \rho_f & \text{float} \cr \rho_o = \rho_f & \text{hang} \cr \rho_o > \rho_f & \text{sink}\end{cases}$|
|Absolute pressure and gauge pressure|$P_{\text{abs}} = P_{\text{atm}} + P_g$|
|Hydraulic system|$P = \dfrac{F_1}{A_1} = \dfrac{F_2}{A_2}$|
|**Continuity equation** <br/> Laminar flow of nonviscous fluid|$\begin{aligned}\dot{m}_1 &= \dot{m}_2 \cr \rho_1 Q_1 &= \rho_2 Q_2 \cr \rho_1 A_1 v_1 &= \rho_2 A_2 v_2 \end{aligned}$|
|**Bernoulli's equation** <br/> Laminar flow of incompressible nonviscous fluid|$P_1 + \rho gy_1 + \frac{1}{2}\rho v_1^2 = P_2 + \rho gy_2 + \frac{1}{2}\rho v_2^2$|

## Entropy

|Description|Equations|
|-:|:-|
|Partition|$M = \dfrac{V}{\delta V}$|
|Microstate (basic state)|$\Omega = M^N$|
|Entropy|$S = \ln\Omega = \ln M^N$|
|Linearity of entropy|$S = S_A + S_B \newline \Omega = \Omega_A\Omega_B$|
|Constant temperature change in entropy|$\Delta S = N\ln\left(\dfrac{V_f}{V_i}\right)$|
|Second law of thermodynamics <br/> in closed system|$\Delta S \begin{cases} >0 & \footnotesize\text{toward equilibrium} \cr = 0 & \footnotesize\text{at equilibrium} \end{cases}$|
|Equipartition of space|$\dfrac{N_A}{V_A} = \dfrac{N_B}{V_B}$|
|Root-mean-square (rms) speed|$v_{\text{rms}} = \sqrt{\overline{v^2}}$|
|Absolute temperature|$\dfrac{1}{k_BT} = \dfrac{dS}{dE_{\text{th}}}$|
|Equipartition of energy|$\dfrac{E_{\text{th}, A}}{N_A} = \dfrac{E_{\text{th}, B}}{N_B}$|

### Monoatomic ideal gas

|Description|Equations|
|-:|:-|
|Thermal energy|$E_{\text{th}} = N\overline{K} = \dfrac{1}{2}Nmv_{\text{rms}}^2$|
|Pressure|$P = \dfrac{2}{3}\dfrac{E_{\text{th}}}{V}$|
|Thermal energy|$E_{\text{th}} = \dfrac{3}{2}Nk_BT$|
|Average kinetic energy|$\overline{K} = \dfrac{3}{2}k_BT$|
|rms speed|$v_{\text{rms}} = \sqrt{\dfrac{3k_BT}{m}}$|
|Ideal gas law|$PV = nRT \newline PV = Nk_BT$|
|Constant volume change in entropy|$\Delta S = \dfrac{3}{2}N\ln\left(\dfrac{T_f}{T_i}\right)$|
|Total change in entropy|$\Delta S = \dfrac{3}{2}N\ln\left(\dfrac{T_f}{T_i}\right) + N\ln\left(\dfrac{V_f}{V_i}\right)$|

## Thermodynamic Processes

|Description|Equations|
|-:|:-|
|General energy balance|$\Delta E = W + Q$|
|Energy balance of ideal gas|$\Delta E_{\text{th}} = W + Q$|
|Change in thermal energy of ideal gas|$\Delta E_{\text{th}} = \dfrac{d}{2} Nk_B \Delta T$|
|PV Work|$W = \displaystyle\int_{V_i}^{V_f} P \ dV$|
|Entropy change|$\Delta S = N \ln\left(\dfrac{V_f}{V_i}\right) + \dfrac{d}{2}N \ln\left(\dfrac{T_f}{T_i}\right)$|
|Constant volume heat capacity|$C_V = \dfrac{Q}{N\Delta T} = \dfrac{d}{2}k_B$|
|Constant pressure heat capacity|$C_P = \dfrac{Q}{N\Delta T} = \left(\dfrac{d}{2}+1\right) k_B$|
|Heat capacity relationship|$C_P = C_V + k_B$|
|Heat capacity ratio|$\gamma = \dfrac{C_P}{C_V} = 1+\dfrac{2}{d}$|

### Isochoric process

|Description|Equations|
|-:|:-|
|Isochoric process|$\Delta V = 0$|
|Work|$W = 0$|
|Thermal energy and heat|$\Delta E_{\text{th}} = Q = \dfrac{d}{2}Nk_B T = NC_V \Delta T$|
|Entropy|$\Delta S = \dfrac{d}{2}N \ln\left(\dfrac{T_f}{T_i}\right) = \dfrac{NC_V}{k_B}\ln\left(\dfrac{T_f}{T_i}\right)$|

### Isentropic process

|Description|Equations|
|-:|:-|
|Isobaric process (quasistatic adiabatic)|$\Delta S = 0$|
|Heat|$Q = 0$|
|Thermal energy and work|$\Delta E_{\text{th}} = W = NC_V \Delta T$|
|PVT relationship|$P_1 V_1^\gamma = P_2 V_2^\gamma \newline T_1 V_1^{\gamma-1} = T_2 V_2^{\gamma-1} \newline P_1^{(1/\gamma)-1} T_1 = P_2^{(1/\gamma)-1} T_2$|

### Isobaric process

|Description|Equations|
|-:|:-|
|Isobaric process|$\Delta P = 0$|
|Work|$W = -P\Delta V = -Nk_B\Delta T$|
|Heat|$Q = NC_P\Delta T$|
|Thermal energy|$\Delta E_{\text{th}} = NC_V\Delta T$|
|Entropy|$\Delta S = \dfrac{NC_P}{k_B}\ln\left(\dfrac{T_f}{T_i}\right)$|

### Isothermal process

|Description|Equations|
|-:|:-|
|Isothermal process|$\Delta T = 0$|
|Thermal energy|$\Delta E_{\text{th}} = 0$|
|Work and Heat|$Q=-W$|
|Work|$W = -Nk_BT\ln\left(\dfrac{V_f}{V_i}\right)$|
|Heat|$Q = Nk_BT\ln\left(\dfrac{V_f}{V_i}\right)$|
|Entropy|$\Delta S = N\ln\left(\dfrac{V_f}{V_i}\right) = \dfrac{Q}{k_B T}$|

## Degradation of Energy

|Description|Equations|
|-:|:-|
|Complete cycle of steady device|$\Delta E = 0 \newline W = Q_{\text{out}} - Q_{\text{in}} \newline \Delta S_{\text{sys}} = 0 \newline \Delta S_{\text{surr}} \ge 0$|
|Steady device thermally transferring energy to lower temperature|$\Delta S_{\text{surr}} = \dfrac{Q_{\text{out}}}{k_B}\left(\dfrac{1}{T_{\text{out}}} - \dfrac{1}{T_{\text{in}}}\right)$|
|Steady device thermally transferring energy to higher temperature|$\Delta S_{\text{surr}} = - \dfrac{Q_{\text{out}}}{k_B}\left(\dfrac{1}{T_{\text{out}}} - \dfrac{1}{T_{\text{in}}}\right)$|
|Steady device converting mechanical energy to thermal energy|$\Delta S_{\text{surr}} = \dfrac{Q_{\text{out}}}{k_B T_{\text{out}}}$|
|Reversible heat engine|$\dfrac{Q_{\text{out}}}{Q_{\text{in}}} = \dfrac{T_{\text{out}}}{T_{\text{in}}} = \dfrac{T_{\text{low}}}{T_{\text{high}}}$|
|Energy balance|$Q_{\text{in}} + W_{\text{in}} = Q_{\text{out}} + W_{\text{out}}$|
|Efficiency of heat engine|$\eta = -\dfrac{W_{\text{out}}}{Q_{\text{in}}} = 1-\dfrac{Q_{\text{out}}}{Q_{\text{in}}}$|
|Maximum efficiency of reversible heat engine|$\eta_{\mathrm{max}} = 1-\dfrac{T_{\text{low}}}{T_{\text{high}}}$|
|Coefficient of performance of heating|$\mathrm{COP_{heating}} = \dfrac{Q_{\text{out}}}{W} = \dfrac{1}{1-Q_{\text{in}}/Q_{\text{out}}}$|
|Maximum coefficient of performance of heating (reversible heat pump)|$\mathrm{COP_{heating, max}} = \dfrac{1}{1-T_{\text{in}}/T_{\text{out}}}$|
|Coefficient of performance of cooling|$\mathrm{COP_{cooling}} = \dfrac{Q_{\text{in}}}{W} = \mathrm{COP_{heating}} - 1$|
|Maximum coefficient of performance of cooling (reversible heat pump)|$\mathrm{COP_{cooling, max}} = \dfrac{T_{\text{in}}}{T_{\text{out}}-T_{\text{in}}}$|

<!--
## Template
|Quantity|Unit|Definition|
|---:|:-:|:---|
||$\mathrm{}$||

|Description|Equations|
|-:|:-|

-->
