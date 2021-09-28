---
title: "CHEM 155 Honors General Chemistry II"
date: 2021-08-17T00:00:00+08:00
---

## Acid-Base Equilibria

### Fundamentals

|Description|Equations|
|-:|:-|
|Autoionization of water|$\color{blue} \ce{2H2O <=> H3O+ + OH-}$ <br/> $K_{w} = \ce{[H3O+][OH-]} = 10^{-14}$|
|pH function|$\ce{pH} = -\log \ce{[H3O+]}$|
|Acid dissociation constant|$\color{blue} \ce{HA + H2O <=> H3O+ + A-}$ <br/> $K_{a} = \dfrac{\ce{[H3O+][A-]}}{\ce{HA}}$|
|Base dissociation constant|$\color{blue} \ce{B + H2O <=> HB+ + OH-}$ <br/> $K_{b} = \dfrac{\ce{[HB+][OH-]}}{\ce{[B]}}$|
|Relationship between dissociation constants|$K_{w} = K_{a}K_{b}$ <br/> $\ce{p}K_{a} + \ce{p}K_{b} = \ce{p}K_{w} = 14$|
|Indicators|$\color{blue} \ce{HIn + H2O <=> H3O+ + In-}$ <br/> $\dfrac{\ce{[H3O+]}}{K_{a}} = \dfrac{\ce{[HIn]}}{\ce{[In^{-}]}}$|

### Buffer and titration

|Description|Equations|
|-:|:-|
|**Henderson–Hasselbalch equation** <br/> pH of a buffer|$\ce{pH} = \ce{p}K_{a} + \log{\dfrac{\ce{[A^{-}]_{0}}}{\ce{[HA]_{0}}}}$|
|Titration curve at half equivalence point|$\ce{pH} = \ce{p}K_{a}$ (where $\ce{[HA] = [A-]}$)|
|Titration curve until equivalence point <br/> ($0 < V < V_{e}$)|(1) Stoichiometric calculation of neutralization gives new acid/base concentration. (2) calculate pH using buffer (H-H equation).|
|Titration curve at equivalence point <br/> $V = V_{e}$|$\ce{mol acid = mol base}$ <br/> $c_{0}V_{0} = c_{e}V_{e}$|
|Titration curve beyond equivalence point <br/> $V > V_{e}$|Calculate pH using excess base that wasn't consumed in the neutralization reaction.|

### Polyprotic acid

|Description|Equations|
|-:|:-|
|Polyprotic acid reactions|$\color{blue} \ce{H2A + H2O <=> HA- + H3O+} (K_{a1}) \newline \ce{HA- + H2O <=> A^2- + H3O+} (K_{a2}) \newline \ce{A^2- + H2O <=> HA- + OH-} (K_{b1}) \newline \ce{HA- + H2O <=> H2A + OH-} (K_{b2})$|
|Relationship between dissociation constants|$K_{b1} = \dfrac{K_{w}}{K_{a2}}$ <br/> $K_{b2} = \dfrac{K_{w}}{K_{a1}}$|
|Effect of pH on solution composition|$\dfrac{\ce{[HA-]}}{\ce{[H2A]}} = \dfrac{K_{a1}}{\ce{[H3O+]}}$ <br/> $\dfrac{\ce{[A^2-]}}{\ce{[HA-]}} = \dfrac{K_{a2}}{\ce{[H3O+]}}$ <br/> $\ce{p}K_{a1}$ and $\ce{p}K_{a2}$ are located at the intersections of titration curve (half equivalence point).|

### Exact treatment of acid-base equilibria

|Description|Equations|
|-:|:-|
|pH of dilute weak acid <br/> $x \equiv \ce{[H3O+]}$|$x^{3} + (c_{b} + K_{a})x^{2} - (K_{w} + c_{a}K_{a})x - K_{a}K_{w} = 0$ |
|Amphoteric equilibria <br/> for $\ce{[amph]} \gg K_{a1}$ <br/> $\ce{[amph]}K_{a2} \gg K_{w}$|$\ce{pH} \approx \dfrac{1}{2} (\ce{p}K_{a1} + \ce{p}K_{a2})$ <br/> $\ce{[H3O+]} \approx \sqrt{K_{a1}K_{a2}}$|

## Solution Equilibria

|Description|Equations|
|-:|:-|
|Solubility product|$\color{blue} \ce{M_aX_b <=> aM^b+ + bX^a-}$ <br/> $K_{sp} = \ce{[M^b+]^{a}[X^a-]^{b}}$|
|Complex ion equilibria <br/> Formation constant|$\color{blue} \ce{M^a+ + X <=> MX^a+} (K_{1}) \newline \ce{MX^a+ + X <=> MX_2^a+} (K_{2}) \newline \ce{M^a+ + 2X <=> MX_2^a+ (K_{f})}$ <br/> $K_{f} = K_{1}K_{2}$|
|Selective precipitation of ions|$\color{blue} \ce{M_aX_b <=> aM^b+ + bX^a-}$ <br/> $\ce{[M^b+]^{a}} = \dfrac{K_{sp}}{\ce{[X^a-]^{b}}}$ <br/> $a\log{\ce{[M^b+]}} = -b\log{\ce{[X^a-]}} + \log K_{sp}$ <br/> The linear equation can be plotted on a log-log M vs X graph.|
|Metal sulfides|$\color{blue} \ce{H2S + H2O <=> H3O+ + HS-} \newline \ce{MS + H2O <=> M^2+ + HS- + OH-}$|

## Electrochemistry

### Fundamentals

|Description|Equations|
|-:|:-|
|Galvanic (voltaic) cells|spontaneous, produce electricity to do work|
|Electrolytic cells|nonspontaneous, use electricity supply to do work|
|cathode|reduction, gain electron|
|anode|oxidation, lose electron|
|Electrostatic potential|$E = \dfrac{U_{e}}{q}$|
|Change in electrostatic potential energy|$\Delta U_{e} = q\Delta E$|
|Total charge passed in current in given time|$Q = it$|
|Moles of electrons transferred in current in given time|$n = \dfrac{it}{F}$|
|pH meter reaction at cathode|$\color{blue} \ce{2H3O+ + 2e- -> H2 + 2H2O}$|
|pH meter reaction at anode|$\color{blue} \ce{H2 + 2H2O -> 2H3O+ + 2e-}$|

### Cell potentials and Gibbs free energy

|Description|Equations|
|-:|:-|
|Electrical work <br/> $(\Delta P = 0; \Delta T = 0)$|$w = \Delta U_{e} = -QE_{\text{cell}} = -itE_{\text{cell}}$ <br/> $w_{\text{rev}} = \Delta G$|
|Standard cell potential|$E^{\circ}\_{\mathrm{cell}} = E^{\circ}_{\mathrm{red}}(\text{cathode}) - E^{\circ}\_{\mathrm{red}}(\text{anode})$|
|Change in Gibbs free energy at standard conditions and standard cell potential|$\Delta G^{\circ} = -nFE^{\circ}_{\text{cell}}$|
|Change in Gibbs free energy at standard conditions and equilibrium constant|$\Delta G^{\circ} = -RT \ln K$|
|Cell potential at standard conditions|$E^{\circ}_{\text{cell}} = \dfrac{RT}{nF} \ln K = \dfrac{0.0257\mathrm{V}}{n} \ln K$|
|Change in Gibbs free energy at nonstandard conditions|$\Delta G = \Delta G^{\circ} + RT \ln Q$|

### Concentration effect and Nerst Equation

|Description|Equations|
|-:|:-|
|**Nerst Equation** <br/> cell potential at nonstandard conditions|$E = E^{\circ} - \dfrac{RT}{nF} \ln Q$ <br/><br/> $E = E^{\circ} - \dfrac{0.0592 \mathrm{V}}{n} \log Q \ (\mathrm{at \ 25^{\circ}C})$|
|Measuring equilibrium constant from standard cell potential|$\ln K = \dfrac{nF}{RT}E^{\circ}\_{\text{cell}} \ (\mathrm{at \ 25^{\circ}C})$ <br/> $\log K = \dfrac{n}{\mathrm{0.0592 V}} E^{\circ}_{\text{cell}} \ (\mathrm{at \ 25^{\circ}C})$|

## Kinetics

### Rate laws

|Description|Equations|
|-:|:-|
|Rate of reaction|$\color{blue}\ce{aA + b B -> cC + dD}$ <br/> $\text{rate} = -\dfrac{1}{a}\dfrac{d\ce{[A]}}{dt} = -\dfrac{1}{b}\dfrac{d\ce{[B]}}{dt}$ <br/><br/> $\text{rate} = \dfrac{1}{c}\dfrac{d\ce{[C]}}{dt} = \dfrac{1}{d}\dfrac{d\ce{[D]}}{dt}$|
|**First order rate law** <br/> Negative line in ln[A] vs t graph.|$\text{rate} = -\dfrac{1}{a}\dfrac{d\ce{[A]}}{dt} = k\ce{[A]}$ <br/> $\ln\ce{[A]}\_{t} = -akt + \ln\ce{[A]}\_{0}$ <br/> $\ce{[A]}\_{t} = \ce{[A]}\_{0} e^{-akt}$|
|**Second order rate law** <br/> Positive line in 1/[A] vs t graph.|$\text{rate} = -\dfrac{1}{a}\dfrac{d\ce{[A]}}{dt} = k\ce{[A]}^{2}$ <br/><br/> $\dfrac{1}{\ce{[A]}\_{t}} = \dfrac{1}{\ce{[A]}\_{0}} + akt$|
|**Zeroth order rate law** <br/> Negative line in [A] vs t graph.|$\text{rate} = -\dfrac{1}{a}\dfrac{d\ce{[A]}}{dt} = k$ <br/> $\ce{[A]}\_{t} = -akt + \ce{[A]}\_{0}$|

### Kinetics and chemical equilibrium

|Description|Equations|
|-:|:-|
|**Principle of detailed balance** <br/> equilibrium rate of elementary reaction is balanced by (equal to) the rate of reverse reaction|$\ce{aA + bB <=>[\mathit{k_{1}}][\mathit{k_{-1}}] cC + dD}$ <br/> $k_{1} \ce{[A]^{a}[B]^{b}} = k_{-1} \ce{[C]^{c}[D]^{d}}$ <br/> $K_{1} = \dfrac{\ce{[C]^{c}[D]^{d}}}{\ce{[A]^{a}[B]^{b}}}$ <br/> $\boxed{K_{1} = \dfrac{k_{1}}{k_{-1}}}$|
|Overall relationship between equilibrium constant and rate constant|$K = \prod\limits_{i} K_{i} = \dfrac{\prod\limits_{i}k_{i}}{\prod\limits_{i}k_{-i}}$|

### Steady-state approximation

|Description|Equations|
|-:|:-|
|**Steady-state approximation** <br/> no single step in the reaction is much slower than the others; assume concentration of intermediates remain constant throughout reaction (B is neighboring molecule) <br/> (*Specific reaction may differ*)|$\color{blue} \ce{A -> C} \ (\text{overall}) \newline \ce{A + B <->[\mathit{k_{1}}][\mathit{k_{-1}}] I + B} \newline \ce{I ->[\mathit{k_{2}}] C}$ <br/> $\dfrac{d\ce{[I]}}{dt} = 0 = k_{1}\ce{[A][B]} - k_{-1}\ce{[I][B]} - k_{2} \ce{[I]}$ <br/> $[I] = \dfrac{k_{1}\ce{[A][B]}}{k_{-1}\ce{[B]} + k_{2}}$ <br/> $\mathrm{rate} = \dfrac{d\ce{[C]}}{dt} = k_{2}\ce{[I]} = \dfrac{k_{1}k_{2}\ce{[A][B]}}{k_{-1}\ce{[B]} + k_{2}}$|
|**Enzyme Kinetics (Michaelis-Menten)** <br/> follows analysis from steady-state approximation: intermediate $\ce{[ES]}$ remains constant; total enzyme $\ce{[E_{T}]}$ remains constant|$\color{blue} \ce{E + S -> P} \ (\text{overall}) \newline \ce{E + S <=>[\mathit{k_{1}}][\mathit{k_{-1}}] ES} \newline \ce{ES ->[\mathit{k_{2}}] E + P}$ <br/> $\ce{[E_{T}] \equiv [E] + [ES]} \implies \ce{[E] = [E_{T}] - [ES]}$ <br/><br/> $\dfrac{d\ce{[ES]}}{dt} = 0 = k_{1} \ce{[E][S]} - k_{-1}\ce{[ES]} - k_{2}\ce{[ES]}$ <br/><br/> $0 = k_{1}\ce{[E_{T}][S]} - k_{1}\ce{[ES][S]} - k_{-1}\ce{[ES]} - k_{2}\ce{[ES]}$ <br/><br/> $\ce{[ES]} = \dfrac{k_{1}\ce{[E_{T}][S]}}{k_{1}\ce{[S]} + k_{-1} + k_{2}} = \dfrac{\ce{[E_{T}][S]}}{\ce{[S]} + K_{m}}$|
|**Michaelis-Menten equation** <br/> rate of enzyme catalysis|$\mathrm{rate} = \dfrac{d\ce{[P]}}{dt} = k_{2}\ce{[ES]} = \dfrac{k_{2}\ce{[E_{T}][S]}}{\ce{[S]} + K_{m}}$|
|Michaelis-Menten constant|$K_{m} = \dfrac{k_{-1}+k_{2}}{k_{1}}$|
|Maximum rate of enzyme catalysis <br/> $(\ce{[S]} \gg K_{m})$|$\dfrac{d\ce{[P]}}{dt} = \dfrac{k_{2}\ce{[E_{T}][S]}}{\ce{[S]} + K_{m}} = \dfrac{V_{\text{max}}\ce{[S]}}{\ce{[S]} + K_{m}}$ <br/> $V_{\text{max}} = k_{2}\ce{[E_{T}]}$|
|Experimental determination of Michaelis-Menten constant|$K_{m} = \ce{[S]} \left( \left( \dfrac{V_{\text{max}}}{dP/dt} \right) - 1 \right)$|
|Observation from dP/dt vs. [S] graph|When $\ce{[S]} = K_{m}$, $\dfrac{d\ce{[P]}}{dt} = \dfrac{1}{2}V_{\text{max}}$ <br/><br/> When $\ce{[S]} \rightarrow \infty$, $\dfrac{d\ce{[P]}}{dt} \rightarrow V_{\text{max}}$|
|Turnover number of enzyme <br/> (when saturated, $\ce{[E_{T}] = [ES]}$)|$k_{\text{cat}} \equiv k_{2} = \dfrac{V_{\text{max}}}{\ce{[E_{T}]}}$|
|Linearization of Michaelis-Menten equation|$\dfrac{1}{dP/dt} = \left( \dfrac{K_{m}}{V_{\text{max}}} \right) \dfrac{1}{\ce{[S]}} + \dfrac{1}{V_{\text{max}}}$|

### Effect of temperature on reaction rates

|Description|Equations|
|-:|:-|
|**Arrhenius equation** <br/> temperature dependence of reaction rate|$k = Ae^{-E_{a}/RT}$|
|**Linearization of Arrhenius equation** <br/> experimental determination of activation energy|$\ln k = \ln A - \dfrac{E_{a}}{RT}$ <br/> $\ln\dfrac{k_{2}}{k_{1}} = -\dfrac{E_{a}}{R} \left( \dfrac{1}{T_{2}} - \dfrac{1}{T_{1}} \right)$|

## Nuclear Chemistry

### Baryons and leptons

Baryon number is conserved.
|Types of Baryon|Symbol|Baryon Number|Charge|
|-:|:-|:-|:-|
|Proton|$\ce{p+}$|+1|+1|
|Antiproton|$\bar{\ce{p}}$|-1|-1|
|Neutron|$\ce{n}$|+1|0|
|Antineutron|$\bar{\ce{n}}$|-1|0|

Lepton number is conserved.
|Types of Lepton|Symbol|Lepton Number|Charge|
|-:|:-|:-|:-|
|Electron|$\ce{e-}$, $\beta^{-}$|+1|-1|
|Positron|$\ce{e+}$, $\beta^{+}$|-1|+1|
|Neutrino|$\nu_{e}$|+1|0|
|Antineutrino|$\bar{\nu}_{e}$|-1|0|

### Nuclear decay process

|Decay Type|Emitted Particle|$\Delta Z$ Atomic Number|$\Delta N$ Neutron Number|$\Delta A$ Mass Number|Example|
|-|-|:-:|:-:|:-:|:-:|
|$\alpha$ decay|$\ce{^4_2He}$|-2|-2|-4|$\ce{^238U -> ^234Th + ^4_2He}$|
|$\beta^{-}$ decay|energetic $\ce{e-}, \bar{\nu}_{e}$|+1|-1|0|$\ce{^14C -> ^14N + \beta-} + \bar{\nu}_{e}$|
|$\beta^{+}$ emission|energetic $\ce{e+}, \nu_{e}$|-1|+1|0|$\ce{^22Na -> ^22Ne + \beta+ + \nu_{e}}$|
|Electron capture|$\nu_{e}$|-1|+1|0|$\ce{^207Bi + e- -> ^207Pb + \nu_{e}}$|
|$\gamma$-ray emission|photon $h\nu$|0|0|0|$\ce{^60Ni^* -> ^60Ni + \gamma}$|
|Internal conversion|$\ce{e-}$|0|0|0|$\ce{^125Sb^m -> ^125Sb + e-}$|

|Description|Equations|
|-:|:-|
|Proton-neutron conversion|$\ce{^1_1p+ -> ^1_0n + ^0_1e+ + \nu_e}$ <br/> $\ce{^1_0n -> ^1_1p+ + ^0_-1e- + \bar{\nu_{e}}}$|

### Mass-energy relationship

|Description|Equations|
|-:|:-|
|Mass-energy equivalence|$E^{2} = m_{0}^{2}c^{4} + p^{2}c^{2}$ <br/> $\Delta E = c^{2} \Delta m \ \ (p = 0)$|
|Spontaneity of nuclear reactions|$\Delta E < 0 \implies \Delta m < 0$|
|Energy equivalent conversion|$\dfrac{1 \mathrm{u}}{931.494 \mathrm{MeV}} = 1$|

### Kinetics of radioactive decay

|Description|Equations|
|-:|:-|
|Activity|$A = -\dfrac{dN}{dt} = kN$|
|Activity and number of nuclei over time|$A_{t} = A_{0}e^{-kt}$ <br/> $N_{t} = N_{0} e^{-kt}$|
|Decay constant and half life|$k = \dfrac{\ln 2}{t_{1/2}}$|

## Introduction to Quantum Mechanics

### Waves and energy quantization

|Description|Equations|
|-:|:-|
|Wavelength and frequency of electromagnetic waves|$c = \lambda \nu$|
|Quantization of energy|$\varepsilon = nh\nu \newline n = 1, 2, 3, ...$|
|Atomic spectra of H atom|$\nu = \left( \dfrac{1}{4} - \dfrac{1}{n^{2}} \right) \times 3.29 \times 10^{15} \ \mathrm{s^{-1}} \newline n = 3,4,5,...$|
|Energy quantization of photon|$\Delta E = h \nu$|
|Frank-Hertz experiment <br/> verifies Bohr's model|$\nu = \dfrac{\Delta E}{h} = \dfrac{eV_{\text{thr}}}{h}$|

### Bohr's model

|Description|Equations|
|-:|:-|
|Total mechanical energy of H atom|$E = \dfrac{1}{2}m_{e}v^{2} - \dfrac{Ze^{2}}{4\pi\epsilon_{0}r}$|
|Uniform circular motion of electron <br/> a classical description|$\dfrac{Ze^{2}}{4\pi\epsilon_{0}r} = m_{e} \dfrac{v^{2}}{r}$|
|Quantized angular momentum of electron|$L = m_{e}vr = n\dfrac{h}{2\pi} \newline n = 1,2,3,...$|
|Allowed radius of H atom|$r_{e} = \dfrac{\epsilon_{0}n^{2}h^{2}}{\pi Z e^{2}m_{e}} = \dfrac{n^{2}}{Z} a_{0}$|
|Allowed velocity of H atom|$v_{n} = \dfrac{nh}{n\pi m_{e}r_{n}} = \dfrac{Ze^{2}}{2\epsilon_{0}nh}$|
|Allowed energy of H atom|$\begin{aligned}E_{n} &= -\dfrac{Z^{2}e^{4}m_{e}}{8\epsilon_{0}^{2}n^{2}h^{2}} \cr &= -(2.18 \times 10^{-18}\mathrm{J}) \dfrac{Z^{2}}{n^{2}} \cr &= -(13.60 \mathrm{eV}) \dfrac{Z^{2}}{n^{2}}\end{aligned} \newline n = 1,2,3,...$|
|Emission atomic spectra of H atom|$\nu = (3.29 \times 10^{15} \mathrm{s^{-1}})Z^{2} \left( \dfrac{1}{n_{f}^{2}} - \dfrac{1}{n_{i}^{2}} \right) \newline n_{i} > n_{f} = 1,2,3,...$|
|Absorption atomic spectra of H atom|$\nu = (3.29 \times 10^{15} \mathrm{s^{-1}})Z^{2} \left( \dfrac{1}{n_{i}^{2}} - \dfrac{1}{n_{f}^{2}} \right) \newline n_{f} > n_{i} = 1,2,3,...$|

### Wave-particle duality

|Description|Equations|
|-:|:-|
|Planck's constant <br/> lazy physicist/chemist|$\hbar = \dfrac{h}{2\pi}$|
|Conservation of energy in photoelectric effect|$h\nu = E_{lost} + K + \Phi$|
|Work function of metal|$\Phi = h\nu_{0}$|
|Maximum kinetic energy of photoelectrons <br/> $(E_{lost} = 0)$|$E_{\text{max}} = K = \dfrac{1}{2}mv_{e}^{2} = \dfrac{p^{2}}{2m} = h\nu - \Phi$|
|de Broglie wavelength|$\lambda = \dfrac{h}{p} = \dfrac{h}{mv}$|
|Heisenberg uncertainty principle|$(\Delta x)(\Delta p) \ge \dfrac{h}{4\pi} = \dfrac{\hbar}{2}$|
|1D standing wave|$f(x, t) = A\sin(kt)\sin(\omega t)$|
|Wave traveling to the right|$f(x, t) = A\sin(\omega t - kx)$|

### The Schrodinger equation

|Description|Equations|
|-:|:-|
|Time independent Schrodinger equation|$-\dfrac{h^{2}}{8\pi^{2}m} \dfrac{d^{2}\psi(x)}{dx^{2}} + V(x)\psi(x) = E\psi(x)$ <br/> $\hat{H}\Psi = E\Psi \newline \hat{H} = -\dfrac{h^{2}}{8\pi^{2}m} \dfrac{d^{2}}{dx^{2}} + V(x)$|
|Time dependent Schrodinger equation|$\hat{H}\Psi = i\hbar \dfrac{\partial\Psi}{\partial t}$|
|Normalization of wave function|$\displaystyle\int_{-\infty}^{\infty} \psi^{*} \psi \ dx = 1$|
|Boundary conditions of wave functions|$\lim\limits_{x \to \pm\infty} \psi(x) = 0$|

### Particle in a box

|Description|Equations|
|-:|:-|
|Wave function of 1D particles in a box|$\psi_{n}(x) = \sqrt{\dfrac{2}{L}} \sin\left( \dfrac{n\pi x}{L} \right)n \newline n = 1,2,3,...$|
|Allowed energy of 1D particles in a box|$E_{n} = \dfrac{n^{2}h^{2}}{8mL^{2}} \newline n = 1,2,3,...$|
|Allowed energy of 3D particles in cubic boxes|$E_{n_{x}n_{y}n_{z}} = \dfrac{h^{2}}{8mL^{2}}[n_{x}^{2} + n_{y}^{2} + n_{z}^{2}] \newline n_{x} = 1,2,3,... \newline n_{y} = 1,2,3,... \newline n_{z} = 1,2,3,...$|
|Wave function of 2D particles in square boxes|$\begin{aligned}&\Psi_{n_{x}n_{y}}(x, y) \cr = &\psi_{n_{x}}(x) \psi_{n_{y}}(y) \cr = &\dfrac{2}{L} \sin \left( \dfrac{n_{x}\pi x}{L} \right) \sin \left( \dfrac{n_{y}\pi y}{L} \right)\end{aligned}$|
|Wave function of 3D particles in cubic boxes|$\begin{aligned}&\Psi_{n_{x}n_{y}n_{z}}(x, y, z) \cr = &\psi_{n_{x}}(x) \psi_{n_{y}}(y) \psi_{n_{z}}(z) \cr = &\left( \dfrac{2}{L} \right)^{3/2} \sin \left( \dfrac{n_{x}\pi x}{L} \right) \sin \left( \dfrac{n_{y}\pi y}{L} \right) \sin \left( \dfrac{n_{z}\pi z}{L} \right)\end{aligned}$|

## Quantum Mechanics and Atomic Structure

### The hydrogen atom

|Description|Equations|
|-:|:-|
|**Principle quantum number** $n$ <br/> determines energy of the electron|$E_{n} = -\dfrac{Z^{2}e^{4}m_{e}}{8\epsilon_{0}^{2}n^{2}h^{2}} \newline = -(2.18 \times 10^{-18}\mathrm{J}) \dfrac{Z^{2}}{n^{2}} \newline = -(13.60 \mathrm{eV}) \dfrac{Z^{2}}{n^{2}} \newline n = 1,2,3,...$|
|**Angular momentum quantum number** $l$ <br/> determines angular momentum of electron|$L^{2} = l(l+1)\dfrac{h^{2}}{4\pi^{2}} \newline l = 0,1,...,n-1$|
|**Magnetic quantum number** $m$ <br/> determines z-component of angular momentum of electron|$L_{z} = m\dfrac{h}{2\pi} \newline m = -l, -l+1, ..., 0, ..., l-1, l$|
|Spin|$m_{s} = -\dfrac{1}{2}, \dfrac{1}{2}$|
|Wave function of electron in quantum state $(n, l, m)$ have radial part and angular part|$\psi_{nlm}(r, \theta, \phi) = R_{nl}(r) Y_{lm}(\theta, \phi)$|
|Wave function as probability density|$(\psi_{nlm})^{2} dV = [R_{nl}(r)]^{2} [Y_{lm}]^{2} dV \newline dV = r^{2}\sin\theta \ dr \ d\theta \ d\phi$|
|Radial probability density (s orbital)|$r^{2} [R_{nl}(r)]^{2} \ dr$|
|Average value of distance of electron from nucleus in an orbital|$\bar{r}_{nl} = \dfrac{n^{2}a\_{0}}{Z} \left\[ 1 + \dfrac{1}{2} \left[ 1 - \dfrac{l(l+1)}{n^{2}} \right] \right\]$|

### Hartree orbital model for many-electron atoms

|Description|Equations|
|-:|:-|
|Orbital approximation for atoms|$\psi_{\text{atom}} = \prod\limits_{i} \varphi_{i}(r_{i})$|
|Coulomb potential of electron moving in shell n and effective nuclear charge|$V_{n}^{\text{eff}}(r) \approx -\dfrac{Z_{\text{eff}}(n)e^{2}}{r}$|

## Quantum Mechanics and Molecular Structure

### Exact molecular model for $\ce{H2+}$

|Description|Equations|
|-:|:-|
|**Born-Oppenheimer approximation** <br/> light slow nuclei; heavy fast electron|$\psi \approx \psi_{e^{-}} + \psi_{\text{nuclei}}$ <br/> $E_{\text{total}} = E_{e^{-}} + E_{\text{nuclei}}$|

### Molecular Orbital (MO) and Linear Combination of Atomic Orbitals (LCAO) Approximation

|Description|Equations|
|-:|:-|
|MO-LCAO approximation for bonding orbital of $\ce{H2+}$|$1\sigma_{g} \approx \sigma_{g1s} = C_{g}[\varphi_{1s}^{A} + \varphi_{1s}^{B}]$|
|MO-LCAO approximation for antibonding orbital of $\ce{H2+}$|$1\sigma_{u}^{*} \approx \sigma_{u1s}^{*} = C_{u}[\varphi_{1s}^{A} - \varphi_{1s}^{B}]$|
|Bond order|$\mathrm{B.O.} = \frac{1}{2} (\text{bonding } e^{-} - \text{antibonding } e^{-})$|

## Spectroscopy

### Electronic spectroscopy

Ultraviolet-Visible (UV-Vis) Spectroscopy
|Description|Equations|
|-:|:-|
|Transmittance <br/> ($I_{0}$ is incident light; $I$ is transmitted light)|$T = \dfrac{I}{I_{0}}$|
|Absorbance|$A = \log \dfrac{I_{0}}{I} \newline A = -\log T$|
|**Beer's Law** <br/> absorbance depends on molar absorption coefficient, concentration, and path legth|$I = I_{0}10^{-\varepsilon c l}$ <br/> $A = \varepsilon c l$|

### Vibrational spectroscopy - harmonic oscillator model

Infrared (IR) Spectroscopy
|Description|Equations|
|-:|:-|
|Reduced mass of system|$\mu = \dfrac{m_{1}m_{2}}{m_{1}+m_{2}}$|
|Frequency|$\omega = \sqrt{\dfrac{k}{\mu}}$|
|Characteristic frequency|$\nu = \dfrac{\omega}{2\pi} = \dfrac{1}{2\pi} \sqrt{\dfrac{k}{\mu}}$|
|Vibrational energy|$E_{n} = (n + \dfrac{1}{2})\hbar\omega = (n + \dfrac{1}{2})h\nu \newline n = 1,2,3,...$|
