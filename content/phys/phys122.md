---
title: "PHYS 122 Electromagnetism"
date: 2021-08-17T00:00:00+08:00
---

## Electrical Charge and Electric Field

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Electrical field <br/> (point charge)|$\mathrm{N/C} \newline \mathrm{(V/m)}$|$\vec{E}\_{s} = \dfrac{\vec{F}\_{0}}{q_{0}} = \dfrac{1}{4\pi\varepsilon_{0}} \dfrac{q}{r^{2}} \hat{r}$|
|Linear charge density|$\mathrm{C/m}$|$\lambda = \dfrac{dQ}{dl}$|
|Surface charge density|$\mathrm{C/m^{2}}$|$\sigma = \dfrac{dQ}{dA}$|
|Volume charge density|$\mathrm{C/m^{3}}$|$\rho = \dfrac{dQ}{dV}$|
|Electric dipole moment <br/> (direction from - to +)|$\mathrm{C\cdot m}$|$\vec{p} = q\vec{d}$|
|Induced dipole moment <br/> (direction from - to +)|$\mathrm{C\cdot m}$|$\vec{p} = \alpha\vec{E}$|

|Description|Equations|
|-:|:-|
|Coulomb's law|$F = \dfrac{1}{4\pi\varepsilon_{0}} \dfrac{q_{1}q_{2}}{r^{2}} \hat{r}$|
|Force on test charge by an electric field|$\vec{F}\_0 = q_{0} \vec{E}$|
|Superposition of electric forces|$\vec{F} = \sum\limits_{i} \vec{F}\_{i}$|
|Superposition of electric fields|$\vec{E} = \sum\limits_{i} \vec{E}\_{i}$|
|Torque on an electric dipole in an uniform electrical field|$\vec{\tau} = \vec{p} \times \vec{E}$|
|Potential energy of an electric dipole in an uniform electric field|$U = -\vec{p}\cdot\vec{E}$|
|Electric field of test charge on x axis caused by dipole at origin oriented in + y direction|$E_{x} = 0 \newline E_{y} = -\dfrac{kp}{\|x\|^{3}}$|
|Electric field of test charge on y axis caused by dipole at origin oriented in + y direction|$E_{x} = 0 \newline E_{y} = \dfrac{2kp}{\|y\|^{3}}$|

## Gauss's Law

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Electric flux through a surface|$\mathrm{N \cdot m^{2}/C}$ <br/> $\mathrm{(V\cdot m)}$|$\Phi_{E} = \displaystyle\int \vec{E} \cdot d\vec{A}$|

|Description|Equations|
|-:|:-|
|Electric flux of a uniform electric field|$\Phi_{E} = \vec{E} \cdot \vec{A}$|
|Electric flux of a nonuniform electric field|$\Phi_{E} = \displaystyle\int \vec{E} \cdot d\vec{A} = \displaystyle\int E \cos\theta \ dA$|
|**Gauss's law** <br/> Electric flux through a closed surface|$\begin{aligned}\Phi_{E} &= \displaystyle\oint \vec{E} \cdot d\vec{A} \cr &= \displaystyle\oint E \cos\theta \ dA = \dfrac{Q}{\varepsilon_{0}}\end{aligned}$|

### Electric field of uniform *spherical* charge distributions

- charged = *uniformly* charged throughout (insulating)
- conducting = charge only on surface

|Charge Distribution|Point in Electric Field|Electric Field Magnitude|
|---:|:-:|:---|
|Point charge|-|$E = \dfrac{1}{4\pi\varepsilon_{0}}\dfrac{q}{r^{2}}$|
|Solid conducting sphere <br/> Hollow charged sphere|Outside sphere, $r>R$|$E = \dfrac{1}{4\pi\varepsilon_{0}}\dfrac{q}{r^{2}}$|
|Solid conducting sphere <br/> Hollow charged sphere|Inside sphere, $r<R$|$E = 0$|
|Solid charged sphere|Outside sphere, $r>R$|$E = \dfrac{1}{4\pi\varepsilon_{0}}\dfrac{q}{r^{2}}$|
|Solid charged sphere|Inside sphere, $r<R$|$E = \dfrac{1}{4\pi\varepsilon_{0}}\dfrac{r}{R^{3}}q$|

### Electric field of uniform *cylindrical* charge distributions

|Charge Distribution|Point in Electric Field|Electric Field Magnitude|
|---:|:-:|:---|
|$\infin$ wire/rod|-|$E = \dfrac{1}{2\pi\varepsilon_{0}}\dfrac{\lambda}{r} = \dfrac{2k\lambda}{r}$|
|$\infin$ solid conducting cylinder <br/> $\infin$ hallow charged cylinder|Outside cylinder, $r>R$|$E = \dfrac{1}{2\pi\varepsilon_{0}}\dfrac{\lambda}{r} = \dfrac{2k\lambda}{r}$|
|$\infin$ solid conducting cylinder <br/> $\infin$ hallow charged cylinder|Inside cylinder, $r<R$|$E = 0$|
|$\infin$ solid charged cylinder|Outside cylinder, $r>R$|$E = \dfrac{1}{2\pi\varepsilon_{0}}\dfrac{\lambda}{r} = \dfrac{2k\lambda}{r}$|
|$\infin$ solid charged cylinder|Inside cylinder, $r<R$|$E = \dfrac{1}{2\pi\varepsilon_{0}}\dfrac{r}{R^{2}} \lambda = \dfrac{2k\lambda r}{R^{2}}$|

### Electric field of uniform *planar* charge distributions

|Charge Distribution|Point in Electric Field|Electric Field Magnitude|
|---:|:-:|:---|
|$\infin$ charged sheet/plate|-|$E = \dfrac{\sigma}{2\varepsilon_{0}}$|
|$\infin$ conducting sheet/plate|-|$E = \dfrac{\sigma}{\varepsilon_{0}} = \dfrac{q}{2\varepsilon_{0}A}$ <br/> ($q$ spreads at each surface)|
|Two oppositely charged conducting plates|Between plates|$E = \dfrac{\sigma}{\varepsilon_{0}}$|
|Charged conductor|At surface|$E = \dfrac{\sigma}{\varepsilon_{0}}$|

## Electric Potential

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Electric potential energy <br/> (point charge) <br/> (choose $U = 0$ at $\infty$)|$\mathrm{J}$|$U = \dfrac{1}{4\pi\varepsilon_{0}} \dfrac{q_{s}q_{0}}{r}$|
|Electric potential <br/> (point charge) <br/> (choose $V = 0$ at $\infty$)|$\mathrm{V}$ <br/> $\mathrm{(J/C)}$|$V = \dfrac{U}{q_{0}} = \dfrac{1}{4\pi\varepsilon_{0}} \dfrac{q_{s}}{r}$|

|Description|Equations|
|-:|:-|
|Electric potential energy of a test charge due to many source charges|$U = \dfrac{q_{0}}{4\pi\varepsilon_{0}} \sum\limits_{i} \dfrac{q_{i}}{r_{i}}$|
|Total electric potential energy of all source charges|$U = \dfrac{1}{4\pi\varepsilon_{0}} \sum\limits_{i<j} \dfrac{q_{i}q_{j}}{r_{ij}}$|
|Electric potential due to many source charges|$V = \dfrac{1}{4\pi\varepsilon_{0}} \sum\limits_{i} \dfrac{q_{i}}{r_{i}}$|
|Electric potential due to continuous distribution of charges|$V = \dfrac{1}{4\pi\varepsilon_{0}} \displaystyle\int \dfrac{dq}{r}$|
|Electric potential and potential energy of point charges|$U = q_{2}V_{1}$|
|Work by electric force and electric field|$W_{a \to b} = \displaystyle\int_{a}^{b} \vec{F} \cdot d\vec{l} = q \int_{a}^{b} \vec{E} \cdot d\vec{l}$|
|Work by electric force on a closed path|$W_{a \to b \to a} = q \displaystyle\oint \vec{E} \cdot d\vec{l} = 0$|
|Work by electric force and change in potential energy|$W_{a \to b} = -\Delta U$|
|Potential difference|$V_{ab} = V_{b} - V_{a}$|
|Potential difference between terminals of battery|$V_{\mathrm{batt}} = V_{-+} = V_{+} - V_{-}$|
|Potential difference and work, potential energy difference|$V_{ab} = \dfrac{\Delta U}{q_{0}} = -\dfrac{W_{a \to b}}{q_{0}}$|
|Potential difference and electric field|$V_{ab} = -\displaystyle\int_{a}^{b} \vec{E} \cdot d\vec{l} = -\displaystyle\int E \cos\theta \ dl$|
|Electric field and potential gradient|$\begin{aligned}\vec{E} &= -\vec{\nabla}V \cr &= \left<-\dfrac{\partial V}{\partial x}, -\dfrac{\partial V}{\partial y}, -\dfrac{\partial V}{\partial z} \right>\end{aligned}$|

## Capacitance and Dielectrics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Capacitance <br/> (in vacuum)|$\mathrm{F} \newline \mathrm{(C/V = C^{2}/J)}$|$C = \dfrac{Q}{V_{-+}} = \dfrac{Q}{V_{+} - V_{-}}$|
|Electric energy density <br/> (in vacuum)|$\mathrm{J/m^{3}}$|$u = \dfrac{U}{Ad} = \dfrac{1}{2} \varepsilon_{0}E^{2}$|

|Description|Equations|
|-:|:-|
|Capacitance of a parallel-plate capacitor in vacuum|$C = \dfrac{Q}{V_{-+}} = \varepsilon_{0} \dfrac{A}{d}$|
|Potential energy stored in a charged capacitor (define $U_{\mathrm{uncharged}} \equiv 0)$|$U = \dfrac{Q^{2}}{2C} = \dfrac{1}{2}CV^{2} = \dfrac{1}{2}QV$|
|Electric energy density in vacuum|$u = \dfrac{U}{Ad} = \dfrac{1}{2} \varepsilon_{0}E^{2}$|
|Dielectric constant|$\kappa = \dfrac{C}{C_{0}} = \dfrac{V_{0}}{V} = \dfrac{E_{0}}{E}$|
|Induced surface charge density on a dielectric in an isolated capacitor|$\sigma_{\mathrm{induced}} = \sigma_{\mathrm{bound}} \newline \sigma_{0} = \sigma_{\mathrm{free}} \newline \sigma_{\mathrm{induced}} = \sigma_{0} \left(1 - \dfrac{1}{\kappa} \right)$|
|Permittivity of a dielectric|$\varepsilon = \kappa \varepsilon_{0}$|
|Capacitance of a parallel-plate capacitor with dielectric between plates|$C = \kappa C_{0} = \kappa\varepsilon_{0}\dfrac{A}{d} = \varepsilon\dfrac{A}{d}$|
|Electric energy density in a dielectric|$u = \dfrac{1}{2}\kappa\varepsilon_{0}E^{2} = \dfrac{1}{2}\varepsilon E^{2}$|
|Gauss's law in dielectrics|$\displaystyle\oint \vec{E}\cdot d\vec{A} = \dfrac{q_{\mathrm{free, enc}}}{\kappa\varepsilon_{0}}$|

## Current, Resistance, and emf

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Current|$\mathrm{A} \newline \mathrm{(C/s)}$|$I = \dfrac{dQ}{dt}$|
|Current density <br/> (per unit cross-section area)|$\mathrm{A/m^{2}}$|$\vec{J} = nq\vec{v}\_d \newline J = \dfrac{I}{A} = n \lvert q \rvert v_{d}$|
|Conductivity <br/> (intrinsic to a material)|$\mathrm{(\Omega\cdot m)^{-1}} \newline \mathrm{A/(V\cdot m)}$|$\sigma = \dfrac{J}{E}$|
|Resistivity <br/> (intrinsic to a material)|$\mathrm{\Omega\cdot m}$|$\rho = \dfrac{E}{J}$|
|Resistance|$\mathrm{\Omega}$|$R = \dfrac{V}{I} = \dfrac{\rho L}{A} = \dfrac{L}{\sigma A}$|

|Description|Equations|
|-:|:-|
|Drift velocity of charge carrier|$\vec{v}\_{d} = -\dfrac{q\vec{E}}{m}\tau$|
|Current and conductor properties|$I = \dfrac{dQ}{dt} = n \lvert q \rvert v_{d}A = JA$|
|Current density <br/> (per unit cross-section area)|$\vec{J} = nq\vec{v}\_d \newline J = \dfrac{I}{A} = n \lvert q \rvert v_{d} = \dfrac{nq^{2}\tau}{m_{q}}E$|
|Conductivity <br/> (intrinsic to a material)|$\sigma = \dfrac{J}{E} = \dfrac{nq^{2}\tau}{m_{q}}$|
|Temperature dependence of resistivity|$\rho(T) = \rho_{0} (1 + \alpha (T-T_{0}))$|
|Temperature dependence of resistance|$R(T) = R_{0} (1 + \alpha (T-T_{0}))$|

## Direct-Current (DC) Circuits

### Circuit analysis

|Description|Equations|
|-:|:-|
|Circuit elements in series <br/> $\lvert Q \rvert, I$ - Equal <br/> $V, R$ - Add <br/> $C$ - Reciprocal|$\lvert Q \rvert = \lvert Q_{1} \rvert  = ... = \lvert Q_{i} \rvert \newline I = I_{1} = ... = I_{i} \newline V = \sum\limits_{i} V_{i} \newline R = \sum\limits_{i} R_{i} \newline \dfrac{1}{C} = \sum\limits_{i} \dfrac{1}{C_{i}}$|
|Circuit elements in parallel <br/> $V$ - Equal <br/> $Q, I, C$ - Add <br/> $R$ - Reciprocal|$V = V_{1} = ... = V_{i} \newline Q = \sum\limits_{i} Q_{i} \newline I = \sum\limits_{i} I_{i} \newline C = \sum\limits_{i} C_{i} \newline \dfrac{1}{R} = \sum\limits_{i} \dfrac{1}{R_{i}}$|
|Algebra of reciprocal values of two elements|$\dfrac{1}{A} = \dfrac{1}{A_{1}} + \dfrac{1}{A_{2}} \Rightarrow A = \dfrac{A_{1}A_{2}}{A_{1} + A_{2}}$|
|Kirchhoff's junction rule <br/> (conservation of charge)|$\sum I = 0$|
|Kirchhoff's loop rule <br/> (conservation of energy)|$\sum V = 0$|
|Battery $(- \to +)$|$+\mathcal{E}$|
|Resistor (along reference direction)|$-IR$|
|Capacitor $(- \to +)$|$+\dfrac{q(t)}{C}$|

### Ohm's law and power

|Description|Equations|
|-:|:-|
|Ohm's law|$V = IR$|
|Potential difference of source with internal resistance|$V_{-+} = \mathcal{E} - Ir = IR$|
|Current of source with internal resistance|$I = \dfrac{\mathcal{E}}{R + r}$|
|Power delivered to or extracted from a circuit element|$P = IV$|
|Power delivered to a resistor <br/> (Note: both $I$ and $V$ depend on $R$)|$P = IV = I^{2}R = \dfrac{V^{2}}{R}$|
|Power output of a source|$P = I\mathcal{E} = IV + I^{2}r = I^{2}(R+r)$|

### R-C circuit

|Description|Equations|
|-:|:-|
|Time constant|$\tau = RC$|
|Charge when charging capacitors|$\begin{aligned}q(t) &= C\mathcal{E} (1-e^{-t/RC}) \cr &= Q_{f}(1-e^{-t/RC})\end{aligned}$|
|Current when charging capacitors|$i(t) = \dfrac{\mathcal{E}}{R}e^{-t/RC} = I_{0}e^{-t/RC}$|
|Charge when discharging capacitors|$q(t) = Q_{0} e^{-t/RC}$|
|Current when discharging capacitors|$i(t) = -\dfrac{Q_{0}}{RC}e^{-t/RC} = I_{0}e^{-t/RC}$|
|Power of battery in R-C circuit|$P = i\mathcal{E} = i^{2}R + \dfrac{iq}{C}$|
|Total energy stored in capacitor|$U = \dfrac{1}{2}QV = \dfrac{1}{2}Q_{f}\mathcal{E}$|

## Magnetic Force and Motion

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Magnetic force|$\mathrm{N}$|$\begin{aligned}\vec{F} &= q\vec{v}\times\vec{B} \cr &= \lvert q \rvert v B \sin\theta\end{aligned}$|
|Magnetic flux through a surface|$\mathrm{Wb} \newline (\mathrm{T\cdot m^{2}})$|$\Phi_{B} = \displaystyle\int \vec{B}\cdot d\vec{A}$|
|Magnetic dipole moment <br/> (direction from S to N)|$\mathrm{A\cdot m^{2}} \newline \mathrm{J/T}$|$\vec{\mu} = I\vec{A}$|

### Magnetic interactions of charged particles

|Description|Equations|
|-:|:-|
|Magnetic force on a charged particle|$\vec{F} = q\vec{v}\times\vec{B} = \lvert q \rvert v B \sin\theta$|
|Radius of a circular orbit in a magnetic field <br/> (charge where $v\perp B$)|$R = \dfrac{mv}{\lvert q \rvert B}$|
|Angular speed (frequency) of circular motion|$\omega = 2\pi f = \dfrac{2\pi}{T} = \dfrac{\lvert q \rvert B}{m}$|
|Frequency of circular motion|$f = \dfrac{1}{T} = \dfrac{\omega}{2\pi} = \dfrac{\lvert q \rvert B}{2\pi m}$|
|Period of circular motion|$T = \dfrac{1}{f} = \dfrac{2\pi}{\omega} = \dfrac{2\pi m}{\lvert q \rvert B}$|
|Velocity selector|$v = \dfrac{E}{B}$|
|Thompson's experiment|$v = \sqrt{\dfrac{2qV}{m}} \newline \dfrac{q}{m} = \dfrac{E^{2}}{2VB^{2}}$|
|Mass spectrometers|$m = \dfrac{\vert q \rvert B^{2}R}{E}$|

### Magnetic interactions of current-carrying conductor

|Description|Equations|
|-:|:-|
|Magnetic force on a straight wire segment|$\vec{F} = I\vec{l}\times\vec{B}$|
|Magnetic force on an infinitesimal wire segment|$d\vec{F} = I \ d\vec{l}\times\vec{B}$|
|Magnetic dipole moment|$\vec{\mu} = I\vec{A}$|
|Magnetic torque on a current loop|$\vec{\tau} = \vec{\mu}\times\vec{B} = IAB\sin\theta$|
|Magnetic torque on a solenoid|$\vec{\tau} = N\vec{\mu}\times\vec{B} = NIAB\sin\theta$|
|Potential energy for a magnetic dipole in B field|$U = -\vec{\mu}\cdot\vec{B} = -\mu B \cos\theta$|

### Magnetic flux and other effects

|Description|Equations|
|-:|:-|
|Magnetic flux through a surface|$\Phi_{B} = \displaystyle\int \vec{B}\cdot d\vec{A}$|
|Gauss's law for magnetism|$\displaystyle\oint \vec{B}\cdot d\vec{A} = 0$|
|Electromagnetic (Lorentz) force|$\vec{F} = q(\vec{E} + \vec{v}\times\vec{B})$|
|Hall effect|$nq = \dfrac{-J_{x}B_{y}}{E_{z}}$|

## Magnetic Field

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Magnetic field|$\mathrm{T} \newline \mathrm{N/(A\cdot m)} \newline 1\mathrm{G} = 10^{-4}\mathrm{T}$|$\vec{B} = \dfrac{\mu_{0}}{4\pi}\displaystyle\int\dfrac{I d\vec{l}\times\hat{r}}{r^{2}}$|

|Description|Equations|
|-:|:-|
|**Ampere's law**|$\displaystyle\oint \vec{B}\cdot d\vec{l} = \mu_{0}I$|
|Magnetic field of a point charge|$\vec{B} = \dfrac{\mu_{0}}{4\pi}\dfrac{q \vec{v}\times\hat{r}}{r^{2}}$|
|**Biot-Savart law** <br/> Magnetic field of infinitesimal length of wire|$d\vec{B} = \dfrac{\mu_{0}}{4\pi}\dfrac{I d\vec{l}\times\hat{r}}{r^{2}}$|
|Force on two $\infin$ parallel wires per unit length|$\vec{F} = q\vec{v}\times\vec{B}$ <br/> $\dfrac{F}{l} = \dfrac{\mu_{0}I_{1}I_{2}}{2\pi d}$|
|Force on two moving charges|$\vec{F} = I\vec{l}\times\vec{B}$ <br/> $\vec{F}\_{1 \to 2} = \dfrac{\mu_{0}}{4\pi}\dfrac{q_{1}q_{2}}{r}\vec{v}\_2\times\vec{v}\_{1}\times\hat{r}$|

### Magnetic field of *linear* conductors

|Conductor Form|Magnetic Field Magnitude|
|---:|:---|
|$\infin$ straight wire|$B = \dfrac{\mu_{0}I}{2\pi r}$|
|$\infin$ current-conducting plane|$B = \dfrac{1}{2}\mu_{0}K$|

### Magnetic field of *circular* conductors

|Conductor Form|Magnetic Field Magnitude|
|---:|:---|
|On the axis of circular wire loop|$B_{x} = \dfrac{\mu_{0}IR^{2}}{2(x^{2}+R^{2})^{3/2}}$|
|On the axis of N circular wire loops|$B_{x} = \dfrac{N\mu_{0}IR^{2}}{2(x^{2}+R^{2})^{3/2}} = \dfrac{\mu_{0}\mu}{2\pi(x^{2}+R^{2})^{3/2}}$|
|At the center of N circular wire loops|$B_{x} = \dfrac{N\mu_{0}I}{2a}$|
|At the center of a circular arc|$B = \dfrac{\mu_{0}I\theta}{4\pi r}$|
|Inside cylindrical conductor|$B = \dfrac{\mu_{0}I}{2\pi}\dfrac{r}{R^{2}} \ \ (r<R)$|
|Outside cylindrical conductor|$B = \dfrac{\mu_{0}I}{2\pi r} \ \ (r>R)$|
|Inside $\infin$ solenoid|$B = N\mu_{0}I$|
|Inside finite length solenoid|$B = \dfrac{N\mu_{0}I}{l}$|
|Inside toroid|$B = \dfrac{N\mu_{0}I}{2\pi r}$|

## Changing Magnetic Field (Induction)

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Inductance|$\mathrm{H} \newline \mathrm{V \cdot s/A}$|$L = \dfrac{\Phi_{B}}{i}$|

|Description|Equations|
|-:|:-|
|**Faraday's law**|$\mathcal{E} = -\dfrac{d\Phi_{B}}{dt}$|
|Motional emf|$\mathcal{E} = \displaystyle\oint (\vec{v}\times\vec{B})\cdot d\vec{l} \newline \mathcal{E}= vBl$|
|Faraday's law for stationary integration path <br/> (Induced electric field and magnetic flux)|$\displaystyle\oint\vec{E}\cdot d\vec{l} = -\dfrac{d\Phi_{B}}{dt}$|
|Inductance of a solenoid|$L = \dfrac{\mu_{0}N^{2}A}{l}$|
|Inductance as amount of change in current associated with change in magnetic flux|$\begin{aligned}\mathcal{E} &= -L\dfrac{di}{dt} \cr \dfrac{d\Phi_{B}}{dt} &= L\dfrac{di}{dt}\end{aligned}$|
|Magnetic potential energy|$U = \dfrac{1}{2}LI^{2}$|
|Magnetic energy density|$u = \dfrac{1}{2}\dfrac{B^{2}}{\mu_{0}}$|

## Changing Electric Field

|Description|Equations|
|-:|:-|
|Conduction current|$i_{C} = \dfrac{dq}{dt} = \varepsilon_{0}\dfrac{d\Phi_{E}}{dt}$|
|Displacement current|$i_{D} = \varepsilon_{0}\dfrac{d\Phi_{E}}{dt}$|
|**Maxwell-Ampere's law**|$\begin{aligned}\displaystyle\oint\vec{B}\cdot d\vec{l} &= \mu_{0}(i_{C}+i_{D}) \cr &= \mu_{0}i_{C} + \mu_{0}\varepsilon_{0}\dfrac{d\Phi_{E}}{dt}\end{aligned}$|
|Magnetic field inside a circular capacitor|$B=\dfrac{\mu_{0}Ir}{2\pi R^{2}} \ (r<R) \newline B=\dfrac{\mu_{0}I}{2\pi R} \ (r \ge R)$|
|**Maxwell's Equations**|$\displaystyle\oint\vec{E}\cdot d\vec{A} = \dfrac{Q}{\varepsilon_{0}} \newline \oint\vec{B}\cdot d\vec{A} = 0 \newline \oint\vec{E}\cdot d\vec{l} = -\dfrac{d\Phi_{B}}{dt} \newline \oint\vec{B}\cdot d\vec{l} = \mu_{0}\left( i_{C} + \varepsilon_{0}\dfrac{d\Phi_{E}}{dt} \right)$|
|Maxwell's equation in empty free space|$\oint\vec{E}\cdot d\vec{A} = 0 \newline \oint\vec{B}\cdot d\vec{A} = 0 \newline \oint\vec{E}\cdot d\vec{l} = -\frac{d\Phi_{B}}{dt} \newline \oint\vec{B}\cdot d\vec{l} = \mu_{0}\varepsilon_{0}\frac{d\Phi_{E}}{dt}$|

## Alternating-Current (AC) Circuits

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Capacitive reactance|$\mathrm{\Omega}$|$X_{C} = \dfrac{1}{\omega C}$|
|Inductive reactance|$\mathrm{\Omega}$|$X_{L} = \omega L$|
|Impedance|$\mathrm{\Omega}$|$Z = \dfrac{\mathcal{E}_{\mathrm{max}}}{I}$|

|Description|Equations|
|-:|:-|
|AC source in AC circuit|$\mathcal{E} = \mathcal{E}_{\mathrm{max}}\sin(\omega t)$|
|Angular frequency of oscillation|$\omega = 2\pi f$|
|Resistor in AC circuit <br/> (i and v in phase)|$v_{R} = \mathcal{E}_{\mathrm{max}}\sin(\omega t) \newline i = I\sin(\omega t) \newline V_{R} = IR$|
|Capacitor in AC circuit <br/> (i leads v by 90 deg)|$v_{C} = \mathcal{E}_{\mathrm{max}}\sin(\omega t) \newline i = I\sin(\omega t + 90^{\circ}) \newline V_{C} = IX_{C} = \dfrac{I}{\omega C}$|
|Inductor in AC circuit <br/> (i lags v by 90 deg)|$v_{L} = \mathcal{E}_{\mathrm{max}}\sin(\omega t) \newline i = I\sin(\omega t - 90^{\circ}) \newline V_{L} = IX_{L} = I\omega L$|
|RC series AC circuit|$Z_{RC} = \sqrt{R^{2} + 1/(\omega C)^{2}} \newline \tan\phi = -\dfrac{V_{C}}{V_{R}} = -\dfrac{1}{\omega RC}$|
|RLC series AC circuit|$Z_{RLC} = \sqrt{R^{2} + (\omega L-1/\omega C)^{2}} \newline \tan\phi = \dfrac{V_{L} - V_{C}}{V_{R}} = \dfrac{\omega L - 1/\omega C}{R}$|
|RC filters|$V_{C} = V_{R} \newline \omega_{\mathrm{cutoff}} = \dfrac{1}{RC}$ <br/> High pass measures R <br/> Low pass measures C|
|RL filters|$V_{R} = V_{L} \newline \omega_{\mathrm{cutoff}} = \dfrac{R}{L}$ <br/> High pass measures L <br/> Low pass measures R|
|Trigonometric identities|$\sin\theta = \cos(\frac{\pi}{2} - \theta) \newline \cos\theta = \sin(\frac{\pi}{2} - \theta) \newline \sin(-\theta) = -\sin\theta \newline \cos(-\theta) = \cos\theta$|

## Special Relativity

|Description|Equations|
|-:|:-|
|Lorentz factor|$\gamma = \dfrac{1}{\sqrt{1-v^{2}/c^{2}}}$|
|Time dilation|$\Delta t_{v} = \gamma\Delta t_{\mathrm{proper}}$|
|Length contraction|$l_{v} = \dfrac{l_{\mathrm{proper}}}{\gamma}$|
|Space-time interval|$s^{2} = (c\Delta t)^{2} - (\Delta x)^{2}$|
|Lorentz transformation|$x' = \gamma(x - ut) \newline y' = y \newline z' = z \newline t' = \gamma (t-ux/c^{2}) \newline v_{x}' = \dfrac{v_{x} - u}{1-uv_{x}/c^{2}}$|
|Relativistic inertia|$m_{v} = \gamma m$|
|Relativistic momentum|$p = \gamma mv$|
|Relativistic kinetic energy|$K = (\gamma - 1)mc^{2}$|
|Internal (rest) energy|$E_{\mathrm{int}} = mc^{2}$|
|Total energy|$E = K + E_{\mathrm{int}} \newline E^{2} = (mc^{2})^{2} + (pc)^{2}$|

## Appendix: List of Constants

|Quantity|Value|
|-:|:-|
|Coulomb constant|$k = 8.99\times 10^{9} \ \mathrm{N\cdot m^{2}/C^{2}}$|
|Electric constant|$\varepsilon_{0} = 8.85\times 10^{-12} \ \mathrm{F/m}$|
|Magnetic constant|$\mu_{0} = 1.26\times 10^{-6} \ \mathrm{H/m}$|
|Elementary charge|$q_{e} = 1.60\times 10^{-19} \ \mathrm{C}$|
|Mass of electron|$m_{e} = 9.11\times 10^{-31} \ \mathrm{kg}$|
|Speed of light in vacuum|$c = 3.00\times 10^{8} \ \mathrm{m/s}$|
