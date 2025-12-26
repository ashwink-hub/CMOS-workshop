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

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/b6c8ff95-ad70-456a-8821-944e2bdf378e" />

To check the value of Id for corresponding Vds and Vgs, just left click and see.

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/7b998c5f-6d05-4c0c-9b61-c512261a0793" />

## Day 02
### Lab 2.1 – day2_nfet_idvds_L015_W039.spice

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/fed60fca-aeef-42d6-9f91-d8cfddff0702" />

The SPICE code for the Day 02 Id vs Vgs is given below.

<img width="1465" height="828" alt="image" src="https://github.com/user-attachments/assets/88d78cec-42ea-46fc-926f-2b5764984f7f" />


From the above code, we can see the values for L and W is 0.15u and W = 0.39u.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d2c549e4-7a84-4694-92ab-f18363abd350" />


The plot shows Id vs Vds for different Vgs values. For low values of Vgs, it is showing quadratic type behaviour, and for higher Vgs values it becomes almost linear.

If we want to see the peak current for Vgs = 1.8 V, just left click on the curve at Vgs = 1.8 V.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/35b0a23f-9205-4c8f-b375-8b7216dd2170" />


Here also, we take L = 0.15u and W = 0.39u. Vds is maintained at 1.8 V and Vgs is swept from 0 to 1.8 V in steps of 0.1 V.

In the above graph we can see that, due to short channel effect we are seeing a linear behaviour for higher Vgs and Vds being constant.

From the above curve we can find threshold voltage by seeing that Vt is the value when current increases drastically for small change in Vgs. To calculate, we draw a tangent on the curve and see where it touches.

It comes around 0.72.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6f7d226a-69b3-4c62-8b1f-a0a5b52dec78" />


## Day 03
### Lab 3.1 – day3_inv_tran_Wp084_Wn036.spice

<img width="1229" height="694" alt="image" src="https://github.com/user-attachments/assets/549b6092-da43-43ab-9e08-dfd72e5bd949" />

The waveform is given by:

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/49fea75c-b7fb-4f75-9e7c-fd6f5239f4fb" />


From the above waveform we can find the Rise and Fall Delay.

Rise Delay:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/bd1d8ba5-4a1c-4962-b849-9f02a27bccbf" />


Fall Delay:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/324ec7fc-7810-480a-b2d9-76d6d1f33efd" />


### Lab 3.2 – day3_inv_vtc_Wp084_Wn036.spice

SPICE code for the VTC characteristics can be given below.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/a35b80ba-a01a-40fd-aef6-f8c74cc4931c" />


Here we are using pfet and nfet for the CMOS inverter. The W/L ratio of PMOS is taken as 2.33 times compared to NMOS.

Vin is swept from 0 to 1.8 V with step size 0.01 V and Vout is plotted.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9efd196b-fe32-42a2-99f8-0f62e4f1fd0c" />


Now we need to find the switching threshold from this graph. It is the point where Vin is equal to Vout.

To zoom into the curve, press the right mouse button and hold it.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/36b7955b-3f67-476d-ad5b-e1a52610d2f6" />


## Day 04
### Lab 4.1 – Day4_inv_noisemargin_wp1_wn036.spice

Here is the SPICE code for Day 04.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/b2233eda-9ba8-4ea0-9bc7-66072cb0b68f" />


Here we take the W/L ratio of PMOS and NMOS as 2.77 and Vin is swept from 0 to 1.8 V with step size 0.01 V.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/64c7f7ee-07ca-4c8b-a7f5-9df7dff6e17d" />


#### Noise Margin High:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/66d15fc2-0f74-4cd3-83f5-260a690c526c" />


#### Noise Margin Low:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b63bbcd3-9f83-4484-af5b-a14c7283ddcf" />


We take the point where slope becomes –1.

The x-axis gives VIL and VIH, while the y-axis gives VOH and VOL.

Noise Margin High = VOH − VIH = 1.73 − 0.984 = 0.746
Noise Margin Low  = VIL − VOL = 0.7566 − 0.1 = 0.6566

## Day 05
## Lab 5.1 – Supply Variation

### day5_inv_supplyvariation_Wp1_Wn036.spice

SPICE code is given below.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/cb368833-59e6-4795-a356-f4ef0f8e31c1" />


First the supply voltage is taken as 1.8 V, then it is decreased by 0.2 V each time.
So overall, it gives around 6 iterations.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c979902e-11ee-4769-bf24-16452966eb94" />


From the above waveform, we can calculate the gain and supply variation.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6598ce85-0971-4906-a55a-0a85134b185d" />


## Lab 5.2 – Device Variation

### Day5_inv_devicevariation_wp7_wn042.spice

SPICE code can be given below.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/146a063f-6d9e-47a9-b595-72c15b45c0f0" />

The simulation, 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/592b3ae1-8b05-45e3-a859-f00550e46d69" />

From the code, we can see that PMOS width is higher than NMOS, so it is strong PMOS and weak NMOS case.

Hence the Vm will shift to the right.

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f2f414bc-834e-4721-a0b1-74f797c1a1d4" />
