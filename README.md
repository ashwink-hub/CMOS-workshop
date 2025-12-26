## CMOS Circuit Design Workshop - Spice Simulation using Sky130nm Technology
### Lab Documentation

---

## Day 01  
### day1_nfet_idvds_L2_W5.spice

Open Virtual Box.

In the Terminal Emulator, open the folder of design files using the following command:

``bash
cd sky130CircuitDesignWorkshop/design/
Now type ls and press Enter to see the list of design files.

<img width="863" height="568" alt="Image" src="https://github.com/user-attachments/assets/7e8a7934-97a7-498c-ab0c-7d9682aa7a35" />

The code for Lab 1 is seen using the vim editor as follows:

<img width="1457" height="820" alt="Image" src="https://github.com/user-attachments/assets/277421e0-b64d-4943-a08c-e53838f92a4f" />

Above we see Vdd varying from 0 to 1.8 volts with step size of 0.1 V and Vgs sweeping from 0 to 1.8 V with step size of 0.2 V.

Now let’s do SPICE simulation using the following command:

ngspice day1_nfet_idvds_L2_W5.spice


Then,

plot -vdd#branch


The result is a plot of the above SPICE code in another tab as a pop-up.

![Spice Simulation](Day1/Day1(1).png)

To check the value of Id for corresponding Vds and Vgs, just left click and see.

![Spice Simulation](Day1/Day1(2).png)

## Day 02
### Lab 2.1 – day2_nfet_idvds_L015_W039.spice

The SPICE code for the Day 02 Id vs Vgs is given below.

--image--

From the above code, we can see the values for L and W is 0.15u and W = 0.39u.

The plot shows Id vs Vds for different Vgs values. For low values of Vgs, it is showing quadratic type behaviour, and for higher Vgs values it becomes almost linear.

If we want to see the peak current for Vgs = 1.8 V, just left click on the curve at Vgs = 1.8 V.

--image--

Here also, we take L = 0.15u and W = 0.39u. Vds is maintained at 1.8 V and Vgs is swept from 0 to 1.8 V in steps of 0.1 V.

In the above graph we can see that, due to short channel effect we are seeing a linear behaviour for higher Vgs and Vds being constant.

From the above curve we can find threshold voltage by seeing that Vt is the value when current increases drastically for small change in Vgs. To calculate, we draw a tangent on the curve and see where it touches.

It comes around 0.72.

--image--

## Day 03
### Lab 3.1 – day3_inv_tran_Wp084_Wn036.spice

The waveform is given by:

--image--

From the above waveform we can find the Rise and Fall Delay.

Rise Delay:

--image--

Fall Delay:

--image--

### Lab 3.2 – day3_inv_vtc_Wp084_Wn036.spice

SPICE code for the VTC characteristics can be given below.

--image--

Here we are using pfet and nfet for the CMOS inverter. The W/L ratio of PMOS is taken as 2.33 times compared to NMOS.

Vin is swept from 0 to 1.8 V with step size 0.01 V and Vout is plotted.

--image--

Now we need to find the switching threshold from this graph. It is the point where Vin is equal to Vout.

To zoom into the curve, press the right mouse button and hold it.

--image--

## Day 04
### Lab 4.1 – Day4_inv_noisemargin_wp1_wn036.spice

Here is the SPICE code for Day 04.

--image--

Here we take the W/L ratio of PMOS and NMOS as 2.77 and Vin is swept from 0 to 1.8 V with step size 0.01 V.

--image--

#### Noise Margin High:

--image--

#### Noise Margin Low:

--image--

We take the point where slope becomes –1.

The x-axis gives VIL and VIH, while the y-axis gives VOH and VOL.

Noise Margin High = VOH − VIH = 1.73 − 0.984 = 0.746
Noise Margin Low  = VIL − VOL = 0.7566 − 0.1 = 0.6566

## Day 05
## Lab 5.1 – Supply Variation

### day5_inv_supplyvariation_Wp1_Wn036.spice

SPICE code is given below.

--image--

First the supply voltage is taken as 1.8 V, then it is decreased by 0.2 V each time.
So overall, it gives around 6 iterations.

--image--

From the above waveform, we can calculate the gain and supply variation.

## Lab 5.2 – Device Variation

### Day5_inv_devicevariation_wp7_wn042.spice

SPICE code can be given below.

--image--

From the code, we can see that PMOS width is higher than NMOS, so it is strong PMOS and weak NMOS case.

Hence the Vm will shift to the right.
