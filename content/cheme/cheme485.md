---
title: "CHEM E 485 Process Design I"
date: 2023-01-26T00:00:00-08:00
---

## -★- Chemical Processes Design

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

- ### Exchangers

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

## Ch 1 Design Process

- ### Block flow diagram (BFD)

  - Blocks represent unit operations
  - Blocks connected by inputs and outputs with arrows
  - Flow goes from left to right in general
  - Light stream toward top, heavy stream toward bottom
  - Critical info presented (important $T, P$, conversion, yield, chemical reaction)
  - If lines cross, horizontal line is continuous, vertical line broken
  - Simplified material balance provided

- ### Process flow diagram (PFD)

  - #### Process topology

    - **Process topology** - location of and interaction between equipment and process stream
    - Major equipment represented by icons with unique equipment number and descriptive name
    - All streams identified by stream number
    - All utility streams supplied to major equipment provided
    - Basic control loops with important control strategy shown

    - {{< admonition type=tip title="Naming convention: process equipments" open=false >}}

- Abbreviations
  - `V` - Vessel
  - `P` - Pump
  - `E` - Heat exchanger
  - `H` - Fire heaters
  - `R` - Reactor
  - `C` - Turbines/Compressors (trapezoid, shape relative to process stream flow)
  - `T` - Towers
  - `TK` - Storage tanks
- Equipment numbering
  - XX-YBB A/B
    - XX - equipment abbreviation
    - Y - unit number (could be a subunit of a larger plant/process)
    - BB - equipment number of the unit
    - A/B - built in degeneracy (spare equipment) for important locations

{{< /admonition >}}

    - Non-significant equipment replacement inherits equipment name and number
    - Significant equipment change uses new equipment name and number

  - #### Stream information

    - Stream number identified in a diamond box
    - Stream direction identified by arrow
    - {{< admonition type=tip title="Naming convention: utility streams" open=false >}}

Electrical component is not shown on PFD as utility streams

- `lps` - Low-Pressure Steam: 3–5 barg (sat)*
- `mps` - Medium-Pressure Steam: 10–15 barg (sat)*
- `hps` - High-Pressure Steam: 40–50 barg (sat)*
- `htm` - Heat Transfer Media (Organic): to 400°C
- `cw` - Cooling Water: From Cooling Tower 30°C Returned at Less than 45°C
- `wr` - River Water: From River 25°C Returned at Less than 35°C
- `rw` - Refrigerated Water: In at 5°C Returned at Less than 15°C
- `rb` - Refrigerated Brine: In at −45°C Returned at Less than 0°C
- `cs` - Chemical Wastewater with High COD
- `ss` - Sanitary Wastewater with High BOD, etc.
- `el` - Electric Heat (Specify 220, 440, 660V Service)
- `bfw` - Boiler Feed Water
- `ng` - Natural Gas
- `fg` - Fuel Gas
- `fo` - Fuel Oil
- `fw` - Fire Water

{{< /admonition >}}

    - Stream flow summary
      - Requires: Stream number, temperature, pressure, vapor fraction, total mass flow rate, total mole flow rate, component mole flow rates
      - Optional: Component mole fraction, component mass fraction, component mass flow rate, volumetric flow rates, significant physical properties, thermodynamic data, stream name
    - Stream identification symbols (stream flag) shows info critical for safety

  - #### Equipment information

    - Equipment descriptions used for estimate equipment purchase cost
    - **Towers**: Size (height and diameter), pressure, temperature, number and type of trays, height and type of packing, materials of construction
    - **Heat Exchangers**
      - Type: Gas-Gas, Gas-Liquid, Liquid-Liquid, Condenser, Vaporizer
      - Process: Duty, Area, Temperature, and Pressure for Both Streams
      - Number of Shell and Tube Passes
      - Materials of Construction: Tubes and Shell
    - **Tanks and Vessels**: Height, Diameter, Orientation, Pressure, Temperature, Materials of Construction
    - **Pumps**: Flow, Discharge Pressure, Temperature, ΔP, Driver Type, Shaft Power, Materials of Construction
    - **Compressors**: Actual Inlet Flowrate, Temperature, Pressure Inlet and Outlet, Driver Type, Shaft Power, Materials of Construction
    - **Heaters (Fired)**: Type, Tube Pressure, Tube Temperature, Duty, Fuel, Material of Construction
    - **Other**: Provide Critical Information

- ### Piping and instrumentation diagram (P&ID)

## Ch 2 Structure and Synthesis of Process Flow Diagrams

- ### Hierarchy of design process

  - Decide batch/continuous
  - Identify input/output
  - Identify and define recycle
  - Identify and design separation
  - Identify and design heat exchanger or energy recovery system

- ### Batch/continuous

  - **Batch process** - finite quantity of product is made during a time period
  - **Continuous process** - feed is continuously sent to equipment; outputs continuously sent to storage or further processing
  - Pilot plant is important to gain insight into full-scale operations

    |Factor|Batch|Continuous|
    |:-|:-|:-|
    |Size|:heavy_plus_sign: Small throughput <500 ton/yr|:heavy_plus_sign: Large throughput > 5000 ton/yr (economy of scale)|
    |Product quality/batch accountability|:heavy_plus_sign: When product quality must be verified and certified (pharm and food)|:heavy_plus_sign: When off-spec material could be blended or stored and reworked <br/> :heavy_minus_sign: Could produce large quantities of off-spec product|
    |Operational flexibility|:heavy_plus_sign: Same equipment can be used for multiple operations|:heavy_minus_sign: Inefficient use of idle units <br/> :heavy_minus_sign: Need retrofitting of plants if demand changes|
    |Standardized equipment - multiple products|:heavy_plus_sign: Same equipment can produce different products|:heavy_minus_sign: Same equipment can only produce designed products|
    |Processing efficiency|:heavy_minus_sign: Require strict scheduling <br/> :heavy_minus_sign: Energy integration not possible - more utility usage <br/> :heavy_minus_sign: Difficulty separation and recycle|:heavy_plus_sign: Efficiency increases with throughput <br/> :heavy_plus_sign: Recycle is easy|
    |Maintenance and operating labor|:heavy_minus_sign: Higher operating labor cost (cleaning, preparation)|:heavy_plus_sign: Lower operating labor cost|
    |Feedstock availability|:heavy_plus_sign: When availability is limited/seasonal|:heavy_plus_sign: When needed in large quantity throughout the year :heavy_minus_sign: Seasonal feed need to be stored|
    |Product demand|:heavy_plus_sign: When demand is seasonal|:heavy_minus_sign: Difficult to make other products during off-season|
    |Rate of reaction to produce products|:heavy_plus_sign: When reaction rate is slow and need high residence times|:heavy_plus_sign: When reaction rate is high and need less residence time|
    |Equipment fouling|:heavy_plus_sign: When equipment fouling is significant|:heavy_minus_sign: Fouling is harder to handle|
    |Safety|:heavy_minus_sign: Worker exposure to chemicals <br/> :heavy_minus_sign: Higher operator error|:heavy_plus_sign: Established safety procedure and record <br/> :heavy_plus_sign: Less risk with handling chemicals|
    |Controllability|:heavy_minus_sign: Controllability is difficulty and complicated|:heavy_plus_sign: Easier to control|

- ### Input/output

  - Process concept diagram
    - Reactions, side reactions, reactants, products, byproducts
  - Block flow diagram
    - Reactor feed prep, reactor, separator feed prep, separator, recycle, environmental control
  - Process flow diagram
    - Input not consumed in reactor must operate equipment or pass through the process as inerts
    - Outputs must have entered from feed or be produced from reactions
    - Utility streams provide heat or work and do not contact process stream
  - Heuristics
    - Do not separate trace inert impurities before feeding
    - Do not separate impurities before feeding if difficult
    - Purify feed if impurities foul or poison catalyst
    - Purify feed if impurities react to form hard-to-separate or hazardous product
    - Purify feed if impurities is in large quantity

- ### Recycle

  - Raw material cost is ~25-75% total operating cost
  - :heavy_plus_sign: Higher overall conversion, reduce raw material cost
  - :heavy_plus_sign: Less waste processing
  - :heavy_plus_sign: Less environmental impact
  - :heavy_minus_sign: Bigger equipment (larger flow rate)
  - :heavy_minus_sign: More equipment (more separation steps)
    |Description|Equation|Heuristics|
    |-:|:-|-|
    |Single-pass conversion|$\small\dfrac{\text{Reactant consumed in reaction}}{\text{Reactant fed to reactor}}$|$\downarrow$ single-pass conversion, <br/> $\uparrow$ recycle flow rate|
    |Overall conversion|$\small\dfrac{\text{Reactant consumed in process}}{\text{Reactant fed to reactor}}$|$\uparrow$ overall conversion, <br/> $\downarrow$ raw material loss|
    |Yield|$\small\dfrac{\text{Moles of reactant to produce desired product}}{\text{Moles of limiting reactant reacted}}$|$\uparrow$ yield, <br/> $\downarrow$ side reaction loss|
  - Recycle types
    - Separate feed from product then recycle
      - If separation is easy
    - Recycle feed and product together, with purge stream
      - If not eqm reaction, cannot react further, or inert (avoid accumulation)
    - Recycle feed and product together, no purge stream
      - If eqm reaction, or can react further in reactor

## Ch 3 Batch Processing

- Batch processing is unsteady state
- **Gantt charts** - tables that illustrate a series of tasks (rows) that occur over period of time (columns)
- **Flowshop plant** - all products use the same equipment in the same sequence, but not the same length of time
- **Jobshop plant** - not all products use the same equipment or used in the same sequence

|Description|Equation|
|-:|:-|
|Total time of non-overlapping operations|$t_{NO} = n\sum t_i$|
|Total time of overlapping operations|$t_O = (n - 1) \max (t_i)+ \sum t_i$|
|Cycle time of non-overlapping operations|$t_{\text{cycle}, NO} = \dfrac{t_{NO}}{n} = \sum t_i$|
|Cycle time of overlapping operations|$t_{\text{cycle}, O} = \dfrac{t_O}{n} = \dfrac{1}{n}[(n - 1) \max (t_i)+ \sum t_i]$|
|Cycle time of overlapping operations <br/> ★ $n \to \infty$|$t_{\text{cycle}, O} \approx \max(t_i)$|
|Total processing (production cycle) time of flowshop plant <br/> ★ $n > 20$|$t = \displaystyle\sum_j n_j(t_{\text{cycle}})_j \approx \sum_j n_j[\max(t_i)]_j$|

## Ch 4 Chemical Product Design

- **Commodity chemical** - manufactured by many companies in large quantity (usually continuous)
- **Specialty chemical** - made in smaller quantities (usually batch), usually by inventer company
- Product design strategies: needs, ideas, selection, manufacture

## Ch 5 Tracing Chemicals through PFD

- **Mixer** - two or more input streams are combined to form a single stream
- **Splitter** - a single input stream is split into two or more output streams
  - Same $T, P, x_i, y_i$, Different $\dot{m}, \dot{n}, \dot{V}$
- **Primary chemicals** - species identified in the overall block flow diagram with chemical reaction
- **Primary flow paths** - path followed by primary chemicals between reactor and the boundaries of process
- Only reactors converts reactant to product
- **Recycle loop** - stream in a loop flow so that the flow path forms a complete circuit back to the point of origin
- **Bypass stream** - streams in a loop flow so that the flow path does not form a complete circuit back to the place of origin

## Ch 6 Process Conditions

- The ability to make an economic analysis of a chemical process on a PFD is not proof that the process will actually work
- Stream $T, P, x_i, and y_i$ should be adjusted to process condition before fed into the unit
  - Changing $T, P$ is easier than $x_i, y_i$
- $P \in [1, 10] \ \mathrm{bar}$
  - $P > 10 \ \mathrm{bar}$ - High pressure needs thicker wall, more expensive equipment
  - $P < 1 \ \mathrm{bar}$ - Vaccum conditions needs larger equipment with special construction technique
- $T \in [40, 260] ^\circ \mathrm{C}$
  - $T < 40 ^\circ \mathrm{C}$ - lowest $T$ for water cooling. Cryogenic condition needs expensive construction material and refrigerant
  - $T > 260 ^\circ \mathrm{C}$ - highest $T$ for steam heating. Combustion heater needed
  - $T > 400 ^\circ \mathrm{C}$ - highest $T$ for stainless steeel to have no loss in tensile strength. Equipment needs expensive alloys and refractory-lined

## -★- ChemE Economic Analysis

## Ch 7 Estimation of Capital Costs

- ### Classifications of capital cost estimates

  - **Economics** - evaluation of capital costs and operating costs associated with construction and operation of a chemical process
  - **Capital cost** - costs of construction of a new plant or modification to an existing plant

  |Name|Diagrams|Level of project definition|Purpose|Method|Expected accuracy index|Preparation effort index|
  |:-:|:-:|:-:|:-:|:-:|:-:|:-:|
  |**Order-of-magnitude estimate** <br/> (Ratio/feasibility estimate)|BFD|0 - 2 %|Screening or feasibility|Stochastic or judgement|4 - 20|1 <br/> (Lowest) <br/> [0.015%, 0.300%] total plant cost|
  |**Study estimate** <br/> (Major equipment/factored estimate)|PFD|1 - 15 %|Concept study or feasibility|Primarily stochastic|3 - 12|2 - 4|
  |**Preliminary estimate** <br/> (Scope estimate)|PFD|10 - 40 %|Budget, authorization, or control|Mixed but primarily stochastic|2 - 6|3 - 10|
  |**Definitive estimate** <br/> (Project control estimate)|PFD, P&ID|30 - 70 %|Control or bid/tender|Primarily deterministic|1 - 3|5 - 20|
  |**Detailed estimate** <br/> (Firm/Contractor's estimate)|PFD, P&ID|50 - 100 %|Check estimate or bid/tender|Deterministic|1 <br/> (Highest^) <br/> [-4%, +6%]|10 - 100|

- ### Estimation of equipment costs

  - **Equipment cost attribute (capacity)** - equipment parameter used to correlate capital costs
  - **Six-tenth rule** - equipment without known cost exponent $n$ can be estimated with $n = 0.6$
    - **Economy of scale** - Larger equipment has lower cost of equipment per unit capacity
    - $n < 1$
  - Cost index
    - Marshall and Swift process industry index
    - Chemical engieering plant cvost index (**CEPCI**)

  |Description|Equation|
  |-:|:-|
  |Capacity and cost <br/> $n \in [0.4, 0.8]$|$\dfrac{C_2}{C_1} = \left(\dfrac{A_2}{A_1}\right)^n$|
  |Time and cost|$\dfrac{C_2}{C_1} = \dfrac{I_2}{I_1}$|
  |Time and capacity adjustments|$\dfrac{C_2}{C_1} = \left(\dfrac{A_2}{A_1}\right)^n \left(\dfrac{I_2}{I_1}\right)$|

- ### Estimating total capital cost

  - Total module cost $C_{\text{TM}} = C_{\text{BM}}^\circ + C_{\text{Cont}} + C_{\text{Fee}}$
    - Bare module cost $C_{\text{BM}}^\circ = C_{\text{DE}} + C_{\text{IDE}}$
      - Direct project expenses $C_{\text{DE}} = C_p + C_M + C_L$
        - **Equipment free on board (f.o.b.) cost** $C_p$ - purchased cost of equipment at manufacturer's site
        - **Materials required for installation** $C_M$ - piping, insulation, fireproofing, foundations, structural support, instrumentation, electrical, painting
        - **Labor to install equipment and material** $C_L$
      - Indirect project expenses $C_{\text{IDE}} = C_{\text{FIT}} + C_O + C_E$
        - **Freight insurance and taxes** $C_{\text{FIT}}$ - transportation, insurance, and tax cost for shipping equipment to plant site
        - **Construction overhead** $C_O$ - fringe benefit (vacation, sick leave, retirement benefits), labor burden (social security, unemployment insurance), salary and overhead for supervisory personnel
        - **Contractor engineering expenses** $C_E$ - salary and overhead for engineering, drafting, and project management personnel
    - **Contingency** $C_{\text{Cont}}$ - covers unforeseen circumstances: loss of time from weather and strikes, small change in design, unpredicted price increase
    - **Contractor fee** $C_{\text{Fee}}$
  - Auxiliary facility
    - **Site development** $C_{\text{Site}}$ - purchase of land; grading and excavation of site; installation and hookup of electrical, water, and sewer system; construction of all internal roads, walkways, and parking lots
    - **Auxiliary buildings** $C_{\text{Aux}}$ - administration offices, maintenance shope, control rooms, warehouses, service buildings (cafeteria, dressing rooms, medical facilities)
    - **Off-sites and utilities** $C_{\text{Off}}$ - raw material and final product storage and loading/unloading facility; equipment for process utility; central environmental control facility; fire protection system

  |Level 5 cost|Level 4 cost|Level 3 cost|Level 2 cost|Level 1 cost|Definition|Expression in terms of $C_p^\circ$|
  |:-:|:-:|:-:|:-:|:-:|-|-|
  |Grassroot cost|-|-|-|-|$C_{GR} = C_{\text{TM}} + C_{\text{Aux}}$||
  |\||Total module cost|-|-|-|$\begin{aligned}C_{\text{TM}} = C_{\text{BM}}^\circ + C_{\text{Cont}} + C_{\text{Fee}}\end{aligned}$|$\begin{aligned}=C_p^\circ (1 + \alpha_M)(1 + \alpha_L + \alpha_{\text{FIT}} + \alpha_L \alpha_O + \alpha_E)(1 + \alpha_{\text{Cont}} + \alpha_{\text{Fee}})\end{aligned}$|
  |\||\||Bare module cost|-|-|$C_{\text{BM}}^\circ = C_{\text{DE}} + C_{\text{IDE}}$|$=C_p^\circ (1 + \alpha_M)(1 + \alpha_L + \alpha_{\text{FIT}} + \alpha_L \alpha_O + \alpha_E)$|
  |\||\||\||Direct project expenses|-|$C_{\text{DE}} = C_p^\circ + C_M + C_L$|$=C_p^\circ (1 + \alpha_M)(1 + \alpha_L)$|
  |\||\||\||\||Equipment|$C_p^\circ = C_p^\circ$|$=C_p^\circ$|
  |\||\||\||\||Materials|$C_M = \alpha_M C_p^\circ$|$=C_p^\circ \alpha_M$|
  |\||\||\||\||Labor|$C_L = \alpha_L (C_p^\circ + C_M)$|$=C_p^\circ (1 + \alpha_M)\alpha_L$|
  |\||\||\||Indirect project expenses|-|$C_{\text{IDE}} = C_{\text{FIT}} + C_O + C_E$|$=C_p^\circ (1 + \alpha_M)(\alpha_{\text{FIT}} + \alpha_L \alpha_O + \alpha_E)$|
  |\||\||\||\||Freight|$C_{\text{FIT}} = \alpha_{\text{FIT}} (C_p^\circ + C_M)$|$=C_p^\circ (1 + \alpha_M)\alpha_{\text{FIT}}$|
  |\||\||\||\||Overhead|$C_O = \alpha_O C_L$|$=C_p^\circ (1 + \alpha_M)\alpha_L \alpha_O$|
  |\||\||\||\||Engineering|$C_E = \alpha_E (C_p^\circ + C_M)$|$=C_p^\circ (1 + \alpha_M)\alpha_E$|
  |\||\||Contingency|-|-|$C_{\text{Cont}} = \alpha_{\text{Cont}}C_{\text{BM}}^\circ$|$=C_p^\circ (1 + \alpha_M)(1 + \alpha_L + \alpha_{\text{FIT}} + \alpha_L \alpha_O + \alpha_E)\alpha_{\text{Cont}}$|
  |\||\||Fee|-|-|$C_{\text{Fee}} = \alpha_{\text{Fee}}C_{\text{BM}}^\circ$|$=C_p^\circ (1 + \alpha_M)(1 + \alpha_L + \alpha_{\text{FIT}} + \alpha_L \alpha_O + \alpha_E)\alpha_{\text{Fee}}$|
  |\||Auxiliary fee|-|-|-|$C_{\text{Aux}}$||

- ### Bare module cost

  - **Lang factor technique** - used to estimate cost to build major expansion to existing plant
    - $C = F_{\text{Lang}} \sum C_{p, i}$
  - **Module costing technique** - used to estimate cost of a new plant
    - $C_{BM} = C_p^\circ F_{BM}$
    - **Bare module cost** - sum of direct and indirect cost based on base case of equipment built with carbon steel at 1 atm
    - Module costing technique protocol
      - Estimate bare module cost of exchangers, pumps, vessels
        1. Calculate bare module cost (2001) $C_{BM} = C_p^\circ F_{BM}$
           1. Estimate equipment cost at base case $C_p^\circ$
              1. $\log C_P^\circ = K_1 + K_2 \log A + K_3 [\log A]^2$
              2. (Table A.1 gives $K_i$)
              3. Figures A.1 - A.17
           2. Identify relationship of bare module factor $F_{BM}$
              1. $F_{BM} = B_1 + B_2 F_M F_P$
              2. (Table A.4 gives $B_i$)
           3. Estimate pressure factor $F_P$
              1. $\log F_P = C_1 + C_2 \log P + C_3 [\log P]^2 \quad (P [\mathrm{barg}])$
              2. (Table A.2 gives $C_i$)
              3. Vessel
                 1. $t = \dfrac{PD}{2SE - 1.2P} + \mathrm{CA} = \dfrac{PD}{2[850 - 0.6P]} + 0.00315 \quad (P [\mathrm{barg}], D[\mathrm{m}])$
                 2. $t_{\min} = 0.0063 \ \mathrm{m}$
                 3. $F_P =\begin{cases} \dfrac{t}{t_{\min}} & P > -0.5 \ \mathrm{barg} && t > t_{\min} \\\ 1 & P > -0.5 \ \mathrm{barg} && t < t_{\min} \\\ 1.25 & P < -0.5 \ \mathrm{barg}\end{cases}$
           4. Estimate material factor $F_M$
              1. Table A.3 + Figure A.18 - exchanger, pumps, vessels
        2. Calculate bare module cost with CECPI time correction
           1. $C_2 = C_1 \dfrac{I_2}{I_1}$
      - Estimate bare module factor of other equipment
        1. Table A.5 + Table A.6 + Figure A.19 - compressors, blowers, drives, evaporators, vaporizers, fans, fired heaters, furnaces, power recovery equipment, trays, demister pads, tower packing
        2. Table A.7 - conveyor, crystallizers, dryers, dust collectors, filters, mixers, reactors, screens
        3. Calculate bare module cost with CECPI time correction
           1. $C_2 = C_1 \dfrac{I_2}{I_1}$

  {{< admonition type=info title="Symbol Conventions" open=false >}}

- Cost
  - $C$ - total cost
  - $C_p$ - Purchased cost of equipment
  - $C_p^\circ$ - Purchased cost of equipment at base condition (built with carbon steel at 1 atm)
  - $C_{BM}$ - Base module cost
- Factors
  - $F_{\text{Lang}}$ - Lang factor
  - $F_{BM}$ - Base module factor
  - $F_P$ - pressure factor
  - $F_M$ - material factor
- Others
  - $\alpha$ - Multiplication cost factors
  - $A$ - Equipment capacity
  - $B$ - Correlation fitting parameters
  - $K$ - Correlation fitting parameters
  - $S$ - maximum allowable stress for carbon steel = 944 bar
  - $E$ - weld efficiency = 0.9
  - $D$ - vessel diameter [=] m
  - $P$ - pressure [=] barg
  - $\mathrm{CA}$ - corrosion allowance [=] 0.00315 m
  - $t_{\min}$ - minimum allowable vessel thickness [=] 0.0063 m

{{< /admonition >}}

- ### Grassroots and total module cost

  - **Total module cost** - cost of making small to moderate expansion or alteration to existing plant
    - Total module cost = bare module cost + contingency + fee
      - Contingency = 15% bare module cost
      - Fee = 3% bare module cost
  - **Grassroots (green field) cost** - cost of new facility which the construction is started on undeveloped land
    - Grassroot cost = total module cost + auxiliary facility cost
      - Auxiliary facility cost = 50% bare module cost at base condition

  |Description|Equation|
  |-:|:-|
  |Total module cost|$C_{TM} = \sum C_{TM, i} = 1.18 \sum C_{BM, i}$|
  |Grassroot cost|$C_{GR} = C_{TM} + 0.5 \sum C_{BM, i}^\circ$|

- ### Plant costs

  |Description|Equation|
  |-:|:-|
  |Total module cost of a plant|$C_{TM} = C_0 \left(\dfrac{F}{F_0}\right)^n$|
  |Grassroot cost of a plant|$C_{GR} = C_0 \left(\dfrac{F}{F_0}\right)^n$|
  |Total module cost of parallel plants (trains)|$C_{TM, n\text{ trains}} = C_{TM, \text{train}} (n_{\text{trains}})^{0.9}$|
  |Grassroot cost of parallel plants (trains)|$C_{GR, n\text{ trains}} = C_{GR, \text{train}} (n_{\text{trains}})^{0.9}$|

## Ch 8 Estimation of Manufacturing Costs

- ### Factors affecting manufacturing costs

  - **Cost of Manufacturing (COM)** = DMC + FMC + GE
    - **Direct manufacturing costs (DMC)** - vary with rate of production
      - **Raw materials** - costs of chemical feedstock
      - **Waste treatment**
      - **Utility** - fuel gas/oil/coal, electric power, steam, cooling water, process water, coiler feed water, instrument air, inert gas, refrigeration
      - **Operating labor** - costs of operations personnel
      - **Direct supervisory and clerical labor** - costs of administrative, engineering, and supportive personnel
      - **Maintenance and repairs** - costs of labor and materials associated with maintenance
      - **Operating supplies** - cost of misc supplies that support daily operation but not considered to be raw materials
      - **Laboratory charges** - cost of routine and special lab tests for quality control and troubleshooting
      - **Patent and royalties** - cost of using patented or licensed technology
    - **Fixed manufacturing costs (FMC)** - not affected by rate of production
      - **Depreciation** - costs associated with physical plant (buildings, equipment, etc). Legal operating expense for tax purposes
      - **Local taxes and insurance** - costs of property taxes and liability insurance
      - **Plant overhead costs (factory expenses)** - catch-all costs associated with operation of auxiliary facilities, payroll and accounting services, fire protection and safety services, medical services, cafeteria, recreation, payroll overhead, employee benefits, general engineering
    - **General expenses (GE)** - management-level and admin activities not directly related to manufacturing
      - **Admin costs** - salary, other admin, building, and activities
      - **Distribution and selling costs** - costs of sales and marketing
      - **Research and development** - costs of research activity related to process and product

  {{< admonition type=info title="Symbol Conventions" open=false >}}

- Cost
  - $\mathrm{COM}$ - total manufacturing cost
  - $\mathrm{COM}_d$ - total manufacturing cost without depreciation
  - $\mathrm{FCI}$ - fixed capital investment
    - $C_{TM}$ - total module cost
    - $C_{GR}$ - grassroot cost
  - $C_{RM}$ - cost of raw materials
  - $C_{WT}$ - cost of waste treatment
  - $C_{UT}$ - cost of utilities
  - $C_{OL}$ - cost of operating labor

{{< /admonition >}}

  |Description|Equation|
  |-:|:-|
  |Total manufacturing cost|$\mathrm{COM} = 0.28 \mathrm{FCI} + 2.73 C_{OL} + 1.23(C_{UT} + C_{WT} + C_{RM})$|
  |Total manufacturing cost without depreciation|$\mathrm{COM}\_d = 0.18 \mathrm{FCI} + 2.73 C_{OL} + 1.23(C_{UT} + C_{WT} + C_{RM})$|

- ### Cost of operating labor $C_{OL}$

  - 1 operator = 245 shift/year (49 week/year, 5 shift/week, 8 hour/shift)
  - 1 plant = 1095 shift/year (365 day/year, 3 shift/day, 8 hour/shift)
  - 4.5 operator/$N_{OL}$
  - Wage estimation
    - :heavy_multiplication_x: Do not use CEPCI
    - :heavy_check_mark: Use *The Oil and Gas Journal and Engineering News Record*
      - 66910 $/year (2080 hour/year) (May 2016, Texas)
      - 32.16 $/hour

  |Description|Equation|
  |-:|:-|
  |Number of operators per shift <br/> ★ $P \le 2$|$N_{OL} = (6.29 + 31.7 P^2 + 0.23 N_{np})^{0.5}$|
  |Number of particular solid process|$P$|
  |Number of nonparticular process <br/> ★ Compressor, tower, reactor, heater, exchanger|$N_{np}$|

- ### Utility cost $C_{UT}$

  - **Battery limit** - boundary of responsibility; PFD only include core unit operations, but not units that generate utilities.
  - Types of fuels
    - **Coal** - negative environmental impact, used near mines
    - **No. 6 fue oil** - heavy oil with high sulfur content
    - **Natural gas** - high regional variation of price
    - **No. 2 fuel oil** - used near coast, large price fluctuation
    - **Electricity** - generated by all sources
      - Only electricity can be predicted by CEPCI
  - Utility supply methods
    - Purchasing from public or private utility
    - Supplied by company
    - Self-generated and used by a single process unit
  - Types of utilities
    - **Air supply** - pressurized and dried air
    - **Steam from boilers** - process steam providing latent heat
    - **Steam generated from process** - process steam  providing heat
    - **Cooling tower water** - process cooling water
    - **Other water**
    - Electrical substation
    - Fuels
    - Refrigeration
    - Thermal system
    - Waste disposal
    - Wastewater treatment
  - Estimate utility cost
    - Capital investment to build a facility to supply utility - use grassroot cost for FCI
    - Table 8.3

- ### Raw material cost $C_{RM}$

  - Table 8.4
  - **Stream factor (SF)** - fraction of time that the plant is operating in a year
    - $\mathrm{SF} \in [0.90, 0.96]$

- ### Waste treatment cost $C_{WT}$

  - Table 8.3

---

## -★- Synthesis and Optimization of Chemical Processes

## Ch11 Design Heuristics

- **Heuristic** - statement concerning equipment sizes, operating conditions, and equipment performance that reduces need for calculations
- **Shortcut method** - faster method that replaces extensive calculation to evaluate equipment sizes, operating conditions, and equipment performance

- Compressors
  - If $P_{out}/P_{in} > 3$, use multiple stages of compressors (which will raise $T$) and intercooling between compressors
  - If hot inlet gas, cool it before compression
- Heat exchangers
  - Heat integration - use heat generated in one part of the process to heat up other parts
  - If $\Delta T_{lm} > 100 \deg C$, need better heat integration
  - If stream have diff $T$ for mixing, need better heat integration

## Ch12 Reactor and Separation Design Heuristics

- Table 12.1 - choice of separation units
  - Example: separate A, B, C needs $\ge 2$ sep units. need design decisions to optimize cost-effectiveness
    - Sep A, then Sep B and C
    - Sep B, then Sep A and C
    - Sep C, then Sep A and B
  - Almost always need $(n-1)$ separation units for $n$ species
  - Number of ways to configure separation units: $S = \dfrac{[2(N-1)]!}{N! (N-1)!}$
    - Example: separate 4 components, need 3 columns, $S=5$ configurations
- Table 12.2 - choice of sequencing separation units
  - Remove the largest product stream first if possible

<!-- |Description|Equations|
|-:|:-|
||| -->

<!-- ★ -->