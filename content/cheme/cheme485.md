---
title: "CHEM E 485 Process Design I"
date: 2023-01-08T00:00:00-08:00
---

## Aspen Plus Unit Operations

- ### Mixers/Splitters

  - `Mixer` - Mixes 1+ inlets to 1/2 outlet streams. The second outlet is the decant stream based on density.
  - `SSplit` - Splits flow based on only two outlet parameters (split fraction, flow)
  - `FSplit` - Splits flow based on many outlet parameters (split fraction, flow, limit flow, cumulative flow)
    - Cannot specify outlet conditions, homogeneously mixed

- ### Separators

  - Flash - Used for flash drums, evaporators, single-stage separators
    - Cannot specify outlet conditions, determined by thermodynamics
    - `Flash2` - Separates feed into 2 outlets (VLE)
    - `Flash3` - Separates feed into 3 outlets (VLLE)
  - `Decanter` - Liquid-liquid separation
  - Separator - Used for single-stage distillation and absorption with known inlet and outlet conditions
    - Need to specify outlet conditions
    - `Sep` - Separates feed into 2+ outlets
    - `Sep2` - Separates feed into 2 outlets

- ### (Heat) Exchangers

  - `Heater`
  - `HeatX`
  - `MHeatX`

- ### Columns

  - Shortcut columns - Used for rapid estimation
    - Assume constant molar overflow and constant relative volatility between light and heavy keys
    - `DSTWU` - Winn-Underwood Gilliland method
      - Fenske (Winn) equation determines min number of stages $N_{\min}$ and optimum feed location $N_{F, \min}$ at total reflex condition
      - Underwood equation determines the min reflux ratio $(L/D)_{\min}$
      - Gilliland correlation determines the actual number of stages $N$ and feed location $N_F$ at actual reflex ratio $L/D$
    - `Distl` - Edmister's method
      - Requires design specification or simulation data from `DSTWU`
        - Actual number of stages $N$, feed location $N_F$, reflex ratio $L/D$, distillate to feed molar ratio $D/F$, condenser type, and operating pressures of condenser and reboiler
  - Rigorous columns - Used for rigorous simulation
    - Can perform detailed design of column iternals: geometries, hydraulics, packings etc.
    - `RadFrac` - Used for absorption, stripping, distillation (extractive, azeotropic, reactive)
    - `Extract` - Used for ternary liquid-liquid extraction
      - Requires thermal specification and stage-wise pressure profile
  - Crude/Petroleum
    - `MultiFrac`, `SCFrac`, `PetroFrac`, `ConSep`

- ### Reactors

  - Balance/Stoichiometry-based
    - `RStoic` - Models given stoichiometry and conversion (extent of reaction) but unknown kinetics and sizing
    - `RYield` - Models given stoichiometry and yield but unknown kinetics and sizing
      - Satisfies total mass balance, but not component balance (may not satisfy 1st law of thermo)
  - Equilibrium-based
    - `REquil` - Models reversible reaction assuming max conversion at chemical and phase equilibrium
      - Requires separate liquid and vapor outlets
    - `RGibbs` - Models chemical equilibrium with minimum $G$ of outlet mixture without given reaction
      - Follows 1st law of thermo
  - Kinetic model-based
    - `RCSTR`
    - `RPlus`
    - `RBatch`

Source: [<i class="fab fa-youtube"></i> Aspen Plus Simulation Software (NPTEL, Indian Institute of Technology, Guwahati)](https://www.youtube.com/playlist?list=PLwdnzlV3ogoWmaPmHqavPktjRTvXcZxb7)

