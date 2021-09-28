---
title: "CHEM 145 Honors General Chemistry I"
date: 2021-08-17T00:00:00+08:00
---

## Gas

### Kinetic Theory of Gas

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Pressure|$\mathrm{N/m^{2}}$|$P = \dfrac{F}{A}$|
|Mole fraction of $a$|-|$X_{a} = \dfrac{n_{a}}{n_{\mathrm{total}}}$|
|Partial pressure of $a$|$\mathrm{N/m^{2}}$|$P_{a} = X_{a}P_{\mathrm{total}}$|
|Pressure-volume work|$\mathrm{J}$|$W = -P\Delta V$|
|Compressibility of gas|-|$z = \dfrac{PV}{nRT}$|

|Description|Equations|
|-:|:-|
|Ideal gas law|$PV = nRT$|
|Ideal gas constant and Boltzmann constant|$R = N_{A}k_{B}$|
|Average kinetic energy of one gas molecule|$\varepsilon = \dfrac{3}{2}k_{B}T$|
|Root mean square speed gas|$v_{\mathrm{RMS}} = \sqrt{\dfrac{3RT}{\mathcal{M}}} = \sqrt{\dfrac{3k_{B}T}{m}}$|
|Mean speed of gas|$\bar{v} = \sqrt{\dfrac{8RT}{\pi\mathcal{M}}} = \sqrt{\dfrac{8k_{B}T}{\pi m}}$|
|Most probable speed of gas|$v_{\mathrm{mp}} = \sqrt{\dfrac{2RT}{\mathcal{M}}} = \sqrt{\dfrac{2k_{B}T}{m}}$|
|Maxwell-Boltzmann speed distribution|$f(v) = 4\pi \left(\dfrac{m}{2\pi k_{B}T}\right) v^{2} \exp\left(\dfrac{-mv^{2}}{2k_{B}T}\right)$|
|Van der Waals equation of state|$(P + a\dfrac{n^{2}}{V^{2}})(V - bn) = nRT$|
|Lennard-Jones potential|$V_{\mathrm{LJ}} = 4\varepsilon \left(\left(\dfrac{\sigma}{R}\right)^{12} - \left(\dfrac{\sigma}{R}\right)^{6} \right)$|

### Molecular Collisions and Rate Processes

|Description|Equations|
|-:|:-|
|Molecule collision rate with wall|$Z_{w} \propto \dfrac{1}{4}\dfrac{N}{V}\bar{v}A = \dfrac{1}{4}\dfrac{N}{V}\sqrt{\dfrac{8RT}{\pi\mathcal{M}}}A$|
|Graham's law of effusion|$\dfrac{\text{rate of effusion of A}}{\text{rate of effusion of B}} = \dfrac{N_{\mathrm{A}}}{N_{\mathrm{B}}} \sqrt{\dfrac{\mathcal{M}_{\mathrm{B}}}{\mathcal{M}_{\mathrm{A}}}}$|
|Molecule-molecule collision rate|$Z_{1} = 4\dfrac{N}{V}d^{2}\sqrt{\dfrac{\pi RT}{\mathcal{M}}}$|
|Mean free path|$\lambda = \dfrac{\bar{v}}{Z_{1}} = \dfrac{V}{\sqrt{2}\pi d^{2}N}$|
|Mean square displacement of diffusion in 3D|$\overline{\Delta r}^{2} = 6Dt$|
|Gas diffusion constant|$D = \dfrac{3}{8} \sqrt{\dfrac{RT}{\pi\mathcal{M}}} \dfrac{V}{Nd^{2}}$|

### Intermolecular Interactions

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Electrostatic force|$\mathrm{N}$|$F = \dfrac{q_{1}q_{2}}{4\pi\varepsilon r^{2}}$|
|Electrostatic potential energy|$\mathrm{N}$|$V = \dfrac{q_{1}q_{2}}{4\pi\varepsilon r}$|
|Dipole moment|$\mathrm{C\cdot m}$|$\mu = qd$|
|Polarizability|$\mathrm{C\cdot m^{2}/V}$|$\alpha = \dfrac{\mu}{E}$|
|Induced dipole moment|$\mathrm{C\cdot m}$|$\mu^{*} = \alpha E$|

|Description|Equations|
|-:|:-|
|Ion-ion interactions|$E \propto \dfrac{q_{1}q_{2}}{r}$|
|Ion-dipole interactions|$E \propto -\dfrac{q\mu}{r^{2}}$|
|Dipole-dipole interactions|$E \propto -\dfrac{\mu_{1}\mu_{2}}{r^{3}}$|
|Induced-dipole-induced-dipole (London)|$E \propto -\dfrac{\alpha_{1}\alpha_{2}}{r^{6}}$|
|Dipole-induced-dipole|$E \propto -\dfrac{\mu_{1}^{2}\alpha_{2}}{r^{6}}$|
|Rotating fixed dipole (Keesom)|$E \propto -\dfrac{\mu_{1}^{2}\mu_{2}^{2}}{r^{6}}$|

## Thermodynamics

### First law of thermodynamics

|Quantity|Unit|Definition|
|---:|:-:|:---|
|Specific heat capacities|$\mathrm{J \cdot kg^{-1} \cdot K^{-1}}$|$q = mc_{s}\Delta T = n\bar{c}\Delta T$|
|Heat capacity|$\mathrm{J/K}$|$q = C\Delta T$|
|Molar heat capacities|$\mathrm{J \cdot mol^{-1} \cdot K^{-1}}$|$q_{V} = nc_{V}\Delta T$ <br> $q_{P} = nc_{P}\Delta T$|
|Enthalpy|$\mathrm{J}$|$H = U + PV$|

|Description|Equations|
|-:|:-|
|First law of thermodynamics|$\Delta U = q + w$ <br/> $dU = \cancel{d}q + \cancel{d}w$ <br/> $\Delta U_{\mathrm{univ}} = \Delta U_{\mathrm{sys}} + \Delta U_{\mathrm{surr}} = 0$|
|Enthalpy change|$q_{P} = \Delta (U + PV) = \Delta H$|
|Molar heat capacity of monoatomic ideal gas at constant volume|$c_{V} = \dfrac{3}{2}R$|
|Molar heat capacity of any ideal gas at constant pressure|$c_{P} = c_{V} + R = \dfrac{5}{2}R$|
|Internal energy change of any ideal gas|$\Delta U = nc_{V}\Delta T$|
|Enthalpy change of any ideal gas|$\begin{aligned}\Delta H &= nc_{P}\Delta T \cr &= \Delta U + \Delta(PV) \cr &= nc_{V}\Delta T + nR\Delta T\end{aligned}$|
|Hess's law|$\Delta H^{\circ} = \sum\limits_{i}^{\text{prod}} n_{i}\Delta H_{i}^{\circ} - \sum\limits_{j}^{\text{react}} n_{j}\Delta H_{j}^{\circ}$|
|Molality|$b = \dfrac{n_{\mathrm{solute}}}{m_{\mathrm{solvent}}}$|
|Boiling point elevation <br/> ($i$ is vant's Hoff dissociation factor)|$\Delta T_{\mathrm{boil}} = ibK_{\mathrm{boil}}$|
|Freezing point depression <br/> ($i$ is vant's Hoff dissociation factor)|$\Delta T_{\mathrm{freeze}} = ibK_{\mathrm{freeze}}$|
|Reversible isothermal process of ideal gas|$\Delta T = 0$ <br/> $\Delta U = 0$ <br/> $\Delta H = 0$ <br/> $w = -\displaystyle\int_{V_{1}}^{V_{2}} P \ dV = -nRT \ln\dfrac{V_{2}}{V_{1}}$ <br/> $q = -w$|
|Reversible adiabatic process of ideal gas|$q = 0$ <br/> $\Delta U = nc_{V}\Delta T = w$ <br/> $\Delta H = nc_{P}\Delta T$ <br/> $\gamma = \dfrac{c_{P}}{c_{V}}$ <br/> $T_{1}V_{1}^{\gamma - 1} = T_{2}V_{2}^{\gamma - 1}$ <br/> $P_{1}V_{1}^{\gamma} = P_{2}V_{2}^{\gamma}$|

### Second law of thermodynamics

|Description|Equations|
|-:|:-|
|Entropy|$S = k_{B} \ln\Omega$|
|Entropy change|$\Delta S = \displaystyle\int_{i}^{f} \dfrac{dq_{\mathrm{rev}}}{T}$|
|$\Delta S_{\mathrm{sys}}$ for reversible isothermal process|$\Delta S = \displaystyle\int_{i}^{f} \dfrac{dq_{\mathrm{rev}}}{T} = \dfrac{1}{T} \displaystyle\int_{i}^{f} dq_{\mathrm{rev}} = \dfrac{q_{\mathrm{rev}}}{T}$|
|$\Delta S_{\mathrm{sys}}$ for reversible isothermal process - compression/expansion of ideal gas|$q_{\mathrm{rev}} = nRT \ln \left( \dfrac{V_{2}}{V_{1}} \right)$ <br/> $\Delta S = nR \ln \left( \dfrac{V_{2}}{V_{1}} \right)$|
|$\Delta S_{\mathrm{sys}}$ for reversible isothermal process - phase transitions|$q_{\mathrm{rev}} = \Delta H_{\mathrm{fus}}$ <br/> $\Delta S_{\mathrm{fus}} = \dfrac{q_{\mathrm{rev}}}{T_{\mathrm{fus}}} = \dfrac{\Delta H_{\mathrm{fus}}}{T_{\mathrm{fus}}}$|
|$\Delta S_{\mathrm{sys}}$ for reversible adiabatic process|$q = 0$ <br/> $\Delta S = 0$|
|$\Delta S_{\mathrm{sys}}$ for reversible isochoric process|$\Delta V = 0$ <br/> $dq_{\mathrm{rev}} = nc_{V}dT$ <br/> $\Delta S = nc_{V} \displaystyle\int_{T_{1}}^{T_{2}} \dfrac{dT}{T} = nc_{V} \ln \left( \dfrac{T_{2}}{T_{1}} \right)$|
|$\Delta S_{\mathrm{sys}}$ for reversible isobaric process|$\Delta P = 0$ <br/> $dq_{\mathrm{rev}} = nc_{P}dT$ <br/> $\Delta S = nc_{P} \displaystyle\int_{T_{1}}^{T_{2}} \dfrac{dT}{T} = nc_{P} \ln \left( \dfrac{T_{2}}{T_{1}} \right)$|
|Entropy change of surrounding|$\Delta S_{\mathrm{surr}} = \dfrac{-\Delta H_{\mathrm{sys}}}{T_{\mathrm{surr}}}$|
|Second law of thermodynamics|$\Delta S \geq \dfrac{q_{\mathrm{rev}}}{T}$|
|Enthalpy of spontaneous process|$\Delta S_{\mathrm{total}} = \Delta S_{\mathrm{sys}} + \Delta S_{\mathrm{surr}} > 0$|
|Standard molar entropy|$S^{\circ} = \displaystyle\int_{0K}^{298.15\mathrm{K}} \dfrac{c_{P}}{T} dT + \Delta S \text{(phase changes between 0K and 298.15K)}$|
|Gibbs free energy for reaction at constant temperature|$\Delta G = \Delta H - T\Delta S$|
|Efficiency of Carnot engines|$\begin{aligned}\varepsilon &= \dfrac{\text{work on surrounding}}{\text{heat into system}} \cr &= \dfrac{T_{\mathrm{high}} - T_{\mathrm{low}}}{T_{\mathrm{high}}} = 1-\dfrac{T_{\mathrm{low}}}{T_{\mathrm{high}}}\end{aligned}$|
|Relationship between heat and temperature in Carnot cycle|$\dfrac{q_{\mathrm{high}}}{T_{\mathrm{high}}} + \dfrac{q_{\mathrm{low}}}{T_{\mathrm{low}}} = 0$|
|Work done by Carnot cycle in one cycle|$w_{\mathrm{cycle}} = -nR(T_{\mathrm{hot}} - T_{\mathrm{cold}}) \ln\dfrac{V_{B}}{V_{A}}$|

## Equilibrium

|Description|Equations|
|-:|:-|
|Law of mass action - partial pressure|$K = \dfrac{\prod\limits_{j}(P_{\text{product }j} / P_{\mathrm{ref}})_{eq}^{b_{j}}}{\prod\limits_{i}(P_{\text{reactant }i} / P_{\mathrm{ref}})_{eq}^{a_{i}}}$|
|Law of mass action - concentration|$K = \dfrac{\prod\limits_{j}(c_{\text{product }j} / c_{\mathrm{ref}})_{eq}^{b_{j}}}{\prod\limits_{i}(c_{\text{reactant }i} / c_{\mathrm{ref}})_{eq}^{a_{i}}}$|
|Gibbs free energy of isothermal reactions|$\Delta G = -T\Delta S = nRT\ln\dfrac{P_{2}}{P_{1}}$|
|Equilibrium expression: relationship between Gibbs free energy and equilibrium constant (gas phase reaction)|$\Delta G^{\circ} = -RT\ln K$|
|Equilibrium expression: alternative form|$\ln K = -\dfrac{\Delta G^{\circ}}{RT} = - \dfrac{\Delta H^{\circ}}{RT} + \dfrac{\Delta S}{R}$|
|Change in Gibbs free energy at non-standard conditions|$\Delta G = \Delta G^{\circ} + RT\ln Q = RT\ln\dfrac{Q}{K}$|
|Reaction quotient - partial pressure|$Q = \dfrac{\prod\limits_{j}(P_{\text{product }j} / P_{\mathrm{ref}})^{b_{j}}}{\prod\limits_{i}(P_{\text{reactant }i} / P_{\mathrm{ref}})^{a_{i}}}$|
|Reaction quotient - concentration|$Q = \dfrac{\prod\limits_{j}(c_{\text{product }j} / c_{\mathrm{ref}})^{b_{j}}}{\prod\limits_{i}(c_{\text{reactant }i} / c_{\mathrm{ref}})^{a_{i}}}$|
|**vant's Hoff equation** <br/> temperature dependence of equilibrium constant of a reaction|$\ln\dfrac{K_{2}}{K_{1}} = -\dfrac{\Delta H^{\circ}}{R} \left( \dfrac{1}{T_{2}} - \dfrac{1}{T_{1}} \right)$|
|**Clapeyron equation** <br/> for two phase in equilibrium, construct phase diagram by finding change of pressure as a function of temperature|$\left( \dfrac{dP}{dT} \right)_{eq} = \dfrac{\Delta S}{\Delta V} = \dfrac{\Delta H}{T\Delta V}$|
|**Clausius-Clapeyron equation** <br/> temperature dependence of vapor pressure for condensed phase and gas phase in equilibrium|$\ln\dfrac{P_{2}}{P_{1}} = -\dfrac{\Delta H_{\mathrm{vap}}}{nR} \left( \dfrac{1}{T_{2}} - \dfrac{1}{T_{1}} \right)$|
|**Clausius-Clapeyron equation** <br/> for $P_{1} = P^{\circ}; \Delta S^{\circ} = \dfrac{\Delta H^{\circ}}{T^{\circ}}$|$\ln\dfrac{P_{2}}{P^{\circ}} = -\dfrac{\Delta H_{\mathrm{vap}}}{nRT_{2}} + \dfrac{\Delta S^{\circ}_{\mathrm{vap}}}{nR}$|
