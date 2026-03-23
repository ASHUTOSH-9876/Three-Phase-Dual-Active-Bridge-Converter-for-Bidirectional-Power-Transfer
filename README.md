[README.pdf](https://github.com/user-attachments/files/26183043/README.pdf)

FOR DIRECT TEXT (without opening the pdf):
README FILE 
Problem: 
Problem 1: Bidirectional Power Transfer using Three-Phase DAB Converters 
This project simulates a three-phase Dual Active Bridge (DAB) converter for 
bidirectional power transfer between two battery systems using Simulink. The model 
demonstrates controlled charging and discharging using phase-shift modulation. 
Software Used: -MATLAB R2025b - Simulink 
Project Structure: - Three_phase_DAB_converter_2_.slx: Main Simulink model - REPORT1_ElectroQuad.pdf: Technical Report (PDF File) - Final_DAB_Presentation.pptx: Presentation File (PPT File) - WAVEFORMS.pdf: Results folder comprising of Waveforms (Voltage, Current) and 
Performance plots - README.pdf: REAADME File (PDF File) 
How to Run 
1. Open the .slx file. 
2. Set the input parameters as mentioned in Key Parameters below. 
3. For powerflow from Battery_1 to Battery_2 set input Delay_1 = 0 and Delay_2 between 
0 and 25ms.  
4. To check the Efficiency, DC Powers and SOC, check 
Measure_efficiency_powers_state_of_charging Subsystem. 
5. To check bridge losses, check Measure_inverter_power_output and 
Measure_rectifier_power_input Subsystems.  
6. For powerflow from Battery_2 to Battery_1 set input Delay_2 = 0 and Delay_1 between 
0 and 25ms. Follow Step 4 and 5.  
7. Whiling running keep Stop Time = 1 and keep powergui block simulation type: 
Discrete and Sampling: 5e-6. 
Key Parameters 
Battery_1: -Type: Lithium-Ion -Nominal Voltage (in V): 48 -Rated Capacity (in Ah): 20 -Initial State-of-charge: 80% -Battery Response Time (in sec): 0.01 
Battery_2: 
README FILE -Type: Lithium-Ion -Nominal Voltage (in V): 44 -Rated Capacity (in Ah): 20 -Initial State-of-charge: 40% -Battery Response Time (in sec): 0.01  
Isolation Transformer: - Units: pu -Nominal power and frequency [Pn(VA), fn(Hz)]: [1e3, 1e4] -Winding 1 parameters [V1 Ph-Ph(Vrms), R1(pu), L1(pu)]: [230, 0.003, 0.01] -Winding 2 parameters [V2 Ph-Ph(Vrms), R2(pu), L2(pu)]: [230, 0.003, 0.01] -Magnetization resistance Rm (pu): 500 -Magnetization inductance Lm (pu): 200 -Saturation characteristic [i1, phi1; i2, phi2; ...] (pu): [0 0; 0.0024 1.2; 1 1.52] 
Triggering Pulse to g1: -Pulse type: Time based -Time (t): Use simulation time -Amplitude: 1 -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): 0 
Triggering Pulse to g3: -Pulse type: Time based -Time (t): Use simulation time -Amplitude: 1 -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): (5e-5)/3 
Triggering Pulse to g5: -Pulse type: Time based -Time (t): Use simulation time -Amplitude: 1 -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): -(5e-5)/3 
Triggering Pulse to g4: -Pulse type: Time based -Time (t): Use simulation time 
-Amplitude: 1 
README FILE -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): (5e-5)/2 
Triggering Pulse to g6: -Pulse type: Time based -Time (t): Use simulation time -Amplitude: 1 -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): -(5e-5)/6 
Triggering Pulse to g2: -Pulse type: Time based -Time (t): Use simulation time -Amplitude: 1 -Period (secs): 5e-5 -Pulse Width (% of period): 50 -Phase delay (secs): (5e-5)/6 
Three Phase Series RL Branch:  -Resistance (in Ohms): 1e-2 -Inductance (in H): 40e-6 
