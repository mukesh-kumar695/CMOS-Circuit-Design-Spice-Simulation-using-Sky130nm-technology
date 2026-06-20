# CMOS-Circuit-Design-Spice-Simulation-using-Sky130nm-technology
# CMOS-Circuit-Design-Spice-Simulation-using-Sky130nm-technology

# Table of Contents

- [Day 1 - NMOS Characteristics and SPICE Basics](#day-1---nmos-characteristics-and-spice-basics)
  - [Circuit Design and Simulation](#circuit-design-and-simulation)
    - [L1 How does SPICE help?](#l1-how-does-spice-help)
    - [L2 What is NMOS?](#l2-what-is-nmos)
    - [L3 What is strong inversion?](#l3-what-is-strong-inversion)
    - [L4 How does body bias affect Vth?](#l4-how-does-body-bias-affect-vth)
  - [NMOS Operating Regions](#nmos-operating-regions)
    - [L1 What is the linear region?](#l1-what-is-the-linear-region)
    - [L2 What is drift current?](#l2-what-is-drift-current)
    - [L3 How is drain current modeled?](#l3-how-is-drain-current-modeled)
    - [L4 What do simulations reveal?](#l4-what-do-simulations-reveal)
    - [L5 When does pinch-off occur?](#l5-when-does-pinch-off-occur)
    - [L6 What defines saturation current?](#l6-what-defines-saturation-current)
  - [Introduction to SPICE](#introduction-to-spice)
    - [L1 What is a SPICE setup?](#l1-what-is-a-spice-setup)
    - [L2 How is a netlist written?](#l2-how-is-a-netlist-written)
    - [L3 How are model parameters defined?](#l3-how-are-model-parameters-defined)
    - [L4 How is the first simulation performed?](#l4-how-is-the-first-simulation-performed)
    - [L5 How are Sky130 models used?](#l5-how-are-sky130-models-used)

- [Day 2 - Velocity Saturation and CMOS VTC](#day-2---velocity-saturation-and-cmos-vtc)
  - [Device Scaling Effects](#device-scaling-effects)
    - [L1 What are lower technology nodes?](#l1-what-are-lower-technology-nodes)
    - [L2 How do Id-Vgs curves vary?](#l2-how-do-id-vgs-curves-vary)
    - [L3 What causes velocity saturation?](#l3-what-causes-velocity-saturation)
    - [L4 How does velocity affect current?](#l4-how-does-velocity-affect-current)
    - [L5 How is Id-Vgs analyzed?](#l5-how-is-id-vgs-analyzed)
    - [L6 How is threshold voltage extracted?](#l6-how-is-threshold-voltage-extracted)
  - [CMOS Voltage Transfer Characteristics](#cmos-voltage-transfer-characteristics)
    - [L1 Why use MOSFETs as switches?](#l1-why-use-mosfets-as-switches)
    - [L2 What are CMOS parameters?](#l2-what-are-cmos-parameters)
    - [L3 How do PMOS and NMOS characteristics compare?](#l3-how-do-pmos-and-nmos-characteristics-compare)
    - [L4 How is Vin obtained?](#l4-how-is-vin-obtained)
    - [L5 How is Vout determined?](#l5-how-is-vout-determined)
    - [L6 How is the VTC plotted?](#l6-how-is-the-vtc-plotted)

- [Day 3 - CMOS Switching and Dynamic Analysis](#day-3---cmos-switching-and-dynamic-analysis)
  - [Inverter Simulations](#inverter-simulations)
    - [L1 How is a SPICE deck created?](#l1-how-is-a-spice-deck-created)
    - [L2 How is CMOS behavior simulated?](#l2-how-is-cmos-behavior-simulated)
    - [L3 How are Sky130 models applied?](#l3-how-are-sky130-models-applied)
  - [Switching Threshold Analysis](#switching-threshold-analysis)
    - [L1 What is switching voltage Vm?](#l1-what-is-switching-voltage-vm)
    - [L2 How does transistor sizing affect Vm?](#l2-how-does-transistor-sizing-affect-vm)
    - [L3 How are W/L ratios selected?](#l3-how-are-wl-ratios-selected)
    - [L4 How are static and transient responses studied?](#l4-how-are-static-and-transient-responses-studied)
    - [L5 What happens with larger PMOS width?](#l5-what-happens-with-larger-pmos-width)
    - [L6 Why are CMOS inverters important?](#l6-why-are-cmos-inverters-important)

- [Day 4 - Noise Margin Evaluation](#day-4---noise-margin-evaluation)
  - [Noise Margin Analysis](#noise-margin-analysis)
    - [L1 Why is noise margin important?](#l1-why-is-noise-margin-important)
    - [L2 What are noise margin voltages?](#l2-what-are-noise-margin-voltages)
    - [L3 How is noise margin calculated?](#l3-how-is-noise-margin-calculated)
    - [L4 How does PMOS width influence noise margin?](#l4-how-does-pmos-width-influence-noise-margin)
    - [L5 How are noise margins verified?](#l5-how-are-noise-margins-verified)

- [Day 5 - Supply and Process Variations](#day-5---supply-and-process-variations)
  - [Supply Voltage Effects](#supply-voltage-effects)
    - [L1 How are supply variations simulated?](#l1-how-are-supply-variations-simulated)
    - [L2 What are low-voltage tradeoffs?](#l2-what-are-low-voltage-tradeoffs)
    - [L3 How are supply tests performed?](#l3-how-are-supply-tests-performed)
  - [Device Variations](#device-variations)
    - [L1 What causes process variations?](#l1-what-causes-process-variations)
    - [L2 How does etching affect devices?](#l2-how-does-etching-affect-devices)
    - [L3 Why does oxide thickness matter?](#l3-why-does-oxide-thickness-matter)
    - [L4 How are variations simulated?](#l4-how-are-variations-simulated)
    - [L5 What conclusions are obtained?](#l5-what-conclusions-are-obtained)
    - [L6 How are Sky130 variation labs conducted?](#l6-how-are-sky130-variation-labs-conducted)



# Day 1 - NMOS Characteristics and SPICE Basics

##  Circuit Design and Simulation

###  How does SPICE help?
SPICE simulations characterize CMOS circuits by extracting delay, slew, and power parameters used in timing analysis, clock tree synthesis, and cell library generation. These simulations generate delay lookup tables based on input slew and output load, enabling accurate physical design and STA.

! [Inverter Circuit]  (./CMOS-1(30775193327552). jpg)

The above inverter circuit has certain electrical characteristics.To understand its behaviour ,we perform SPICE simulations which help us analyze important parameters such as delay,switching behavior,and performance.Based on these results,we can determine the proper  W/L (width /Length) ratio of the transistors .


















  

























































  




















































































































































