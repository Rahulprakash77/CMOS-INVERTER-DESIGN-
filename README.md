# CMOS-INVERTER-DESIGN-
I choose this design because ,The CMOS inverter is the fundamental building block of digital ICs. It serves as the basis for constructing more complex logic gates and circuits. Understanding its characteristics and behavior is crucial for designing and analyzing more intricate digital systems.

## importance of cmos inverter 


**Importance of CMOS Inverter in Digital Design:**

1. **Basic Logic Element:** CMOS inverters are the basic building blocks of digital logic circuits. They enable the creation of more complex logic gates and circuits by combining multiple inverters.

2. **Logical Operations:** Inverters perform the NOT operation, a fundamental logical function. They are crucial for implementing logical operations such as AND, OR, and XOR, forming the basis of digital computations.

3. **Voltage Level Shifting:** CMOS inverters are used for voltage level shifting in digital circuits, enabling smooth communication between different logic families or voltage domains.

4. **Signal Restoration:** In digital systems, CMOS inverters can be used to regenerate and restore digital signals, helping to mitigate signal degradation and noise effects.

5. **Clock Signal Generation:** Inverters are used in clock signal generation and distribution, ensuring synchronized timing across digital circuits.

6. **Low Power Consumption:** CMOS inverters consume minimal power due to their inherent design, making them vital for energy-efficient digital systems.

**Importance of CMOS Inverter in Analog Design:**

1. **Voltage Amplification:** CMOS inverters can be used as voltage amplifiers in analog circuits, amplifying weak input signals while maintaining a linear response.

2. **Voltage-to-Current Conversion:** CMOS inverters are used to convert voltage signals into current signals, a common requirement in analog design.

3. **Buffering and Isolation:** In analog design, CMOS inverters are employed as buffers and isolators to prevent signal distortion and ensure proper impedance matching.

4. **Biasing and Level Shifting:** Inverters are used for biasing and level shifting in analog circuits, aiding in setting operating points and signal ranges.

5. **Oscillator and Filter Design:** CMOS inverters are integral to designing oscillators and filters in analog circuits, helping generate stable oscillations and filter signals.

6. **Mixed-Signal Integration:** In mixed-signal circuits, CMOS inverters enable seamless integration of digital and analog components, bridging the gap between these two domains.

In both digital and analog design, CMOS inverters serve as versatile components that underpin a wide range of circuit functionalities. Their low power consumption, robustness, and flexibility make them indispensable tools for modern electronic circuit design.





#### Software of Use: Cadence Virtuoso

## Theory ( know about inverter)
A simple inverter inverts the logically high input to low output and vice versa. It is of immense significance in clock generation, generation of delays, memories to store the data, improving the circuit's noise immunity, and much more. It is a simple two transistor device. For input 0, PMOS turns ON, and NMOS stays OFF. This charges the output capacitance, thus making output logic HIGH. Whereas for input 1, PMOS is OFF, and NMOS is ON. The charged capacitance now discharges, making output logic LOW. On a periodic application of pulse, an inverted pulse is obtained at the output. The in-depth analysis of the output on logic 0 to 1 at the input is summed up by its Voltage Transfer Characteristics (VTC).



## What is CMOS Inverter?

CMOS inverter definition is a device that is used to generate logic functions is known as CMOS inverter and is the essential component in all integrated circuits. A CMOS inverter is a MOSFET (metal oxide semiconductor field effect transistor), composed of a metal gate that lies on top of oxygen’s insulating layer on top of a semiconductor. These inverters are used in most electronic devices which are accountable for generating data n small circuits.

![cmos](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/6c2dc6a6-cc44-43f4-a1b9-54401752d7b9)


## CMOS Inverter Schematic Diagram

The logic element like an inverter reverses the applied input signal. In digital logic circuits, binary arithmetic & switching or logic function’s mathematical manipulation are best performed through the symbols 0 & 1. The CMOS inverter truth table is shown above. If the input logic is zero (0) then the output will be high (1) whereas, if the input logic is one (1), then the output will be low (0).

![CMOS-Inverter-Circuit](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/3604d303-3762-4a75-964f-e26f110329f1)

## Inverter Dynamic Characteristics

The CMOS inverter dynamic characteristics are shown below. So, some of the following formal definitions of different parameters are discussed below. Here, all the percentage (%) values are the steady-state values

![Dynamic-Characteristics-of-CMOS-Inverter](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/987134c6-beae-4ee9-a833-bb57e0db2df3)

Rise Time or tr: Rise time is the time used to increase the signal from 10% to 90%.
Fall Time or tf: Fall time is the time used to drop the signal from 90% to 10%
Edge Rate or trf : It is (tr + tf )/2.
The propagation delay from high to low or tpHL: The time used to drop from VOH – 50%.
The propagation delay from low to high or tpLH: The time used to increase from 50%- VOL.
Propagation Delay or tp: It is (tpHL + tpLH)/2.
Contamination Delay or tcd: It is the smallest time from the 50% input crossing to the 50% output crossing

## MY WORK 

I used the gpdk 90nm library in Cadence virtuoso, conducting transient and DC analysis on the inverter. I calculated parameters such as noise margin, power consumption, rise time, and propagation delay for the inverter.
Fun part was analysing the effect of W/L ratio, Power supply and fanout on these parameters. Some of the notable conclusions are:
**Propagation delay:**
upon increasing W/L ratio, propagation delay decreases (values calculated for T rise = 10ps)
W/L= 120/100; Tpd = 4.6223ps
W/L = 240/100; Tpd = 3.7765ps

**Effect of W/L ratio :**
W/L(pmos) >W/L(nmos) then cmos acts as a strong pullup network.
W/L(pmos) < W/L(nmos) then cmos acts as a strong pulldown network.

**Power consumption :**
- upon reducing W/L ratio power consumption decreases.
- upon reducing Vdd power consumption reduces.

Three golden methods to increase speed of the inverter (rise time reduction) :

🔸Increase W/L ratio: More W/L = more current = faster load capacitance charging.

🔸Increase power supply (Vdd): Higher Vdd = higher current flow = faster load capacitance charging.

🔸Reduce load capacitance: Less capacitance = quicker charging = faster circuit response.

I also made the Physical layout of the inverter and then performed the LVS. Implementing the theoretical concepts on an industry level tool was a great learning experience 
### (1) designing circuit in cadence 


using cadence 90 node technology , keeping L lower possible (100 nm )  , this is intially setup

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/b295309f-f321-49cb-926d-c76a77f6e9f6)


### (2) test the circuit 

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/f25fa154-f99f-4a16-934c-34e5d0b4e6f3)



### (3) LVS

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/f536f938-2b71-44cf-8f29-7a67ad754a3e)

### (4) Effect of W/L ratio
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/ce2fc74a-7068-42c9-aa7f-9e8c0933164c)

### (5) Effect of W/L on Transfer charecteristics

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/0d18fb88-b305-4ac4-b7d4-801ae2c579b2)
### (6) Effect of W/L on Power consumption
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/ef8dd65e-c751-416d-b72a-f348a65d5be8)
### (7) Effect of Vdd on power consumption
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/d1ab45e3-041f-47c4-99b9-a9c8a28f507e)

### (8) Effect of load capacitance on rise time
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/911da1cc-a54a-488b-9a6b-1720f2f94af4)

### (9) Noise Margin parameter
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/f225c53c-a186-4604-ae54-24ecf12a4016)

### (10) Layout
![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/5a15f023-bfce-48c4-8c33-c29c1a9c713e)

















