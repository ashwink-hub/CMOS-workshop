Cmos Circuit Design Workshop

Day 1 – NMOS basics and SPICE intro

Learnt basic NMOS structure and how threshold voltage comes from strong inversion.
Understood cutoff, linear and saturation region using Id–Vds curves.
Saw how pinch-off happens and why current saturates.
Got idea about channel length modulation (Id slightly depends on Vds).
Learnt why SPICE simulations are needed before physical design.
Did first NGSPICE simulation using sky130 NMOS models.

Day 2 – Short channel and velocity saturation

Compared long channel vs short channel MOSFET behaviour.
Observed Id–Vgs becomes more linear in short channel due to velocity saturation.
Learnt relation between electric field, mobility and velocity saturation.
Ran simulations by changing W and L but keeping W/L same.
Understood why current doesn’t scale ideally for lower node devices.
Extracted threshold voltage from Id–Vgs curve.

Day 3 – CMOS inverter and switching threshold

Built CMOS inverter using NMOS and PMOS in SPICE.
Generated VTC curve and understood inverter switching behaviour.
Learnt about switching threshold Vm and why both transistors conduct there.
Studied effect of PMOS width on Vm shifting.
Did transient simulation to calculate rise and fall delay.
Understood why symmetric inverter is important for clock buffers.

Day 4 – Noise margin analysis

Learnt what noise margin is and why it matters in digital circuits.
Identified VIL, VIH, VOL and VOH from VTC curve.
Calculated noise margin using slope = −1 method.
Observed how PMOS sizing affects noise margin.
Noticed noise margin saturates after certain width.
Understood why CMOS inverter is robust to noise.

Day 5 – Supply and device variation

Studied effect of supply voltage scaling on VTC.
Observed lower Vdd reduces power but increases delay.
Compared gain for different supply voltages.
Learnt process variations like etching and oxide thickness.
Simulated strong PMOS / weak NMOS and vice versa cases.
Observed Vm shifts but noise margin remains mostly stable.
