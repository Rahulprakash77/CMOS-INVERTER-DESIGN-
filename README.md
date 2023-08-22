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



### The contents are organized in the below metioned sequence.

1. **Inverter Schematic**
2. **Test Schematic** 
3. **Transient Analysis** 
4. **DC Analysis: VTC Curve**
5. **Netlist Generation**
6. **Layout**
7. **Swap NMOS and PMOS: Transient Analysis, VTC**

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

### (1) designing circuit in cadence 
using cadence 180 node technology , keeping L lower possible (180 nm ) and width(n) = 2um ,width(p) = 4um , this is intially setup
<img width="327" alt="123095880-277c6980-d44c-11eb-95e7-2a85430fdf51" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/3c45232d-9808-4644-a668-bd7c0193f609">

### (2) test the circuit 

### (3) transient analysis

<img width="824" alt="123097318-ab832100-d44d-11eb-91e8-2a85e8ddade3" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/c5bf1f4f-e1ae-414a-854c-207216950151">

### (4) Dc analysis ; VTC curve
A) Electrically symmetric inverter (Wp=4um; Wn=2um)

<img width="760" alt="123097452-c81f5900-d44d-11eb-8931-64a1b50ec908" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/70216e40-fc5c-4b8b-8f79-d52e2c303f17">


B) Inverter with stronger PMOS (Wp=8um; Wn=2um)

<img width="759" alt="123097515-d8cfcf00-d44d-11eb-8c09-a331b6831b3f" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/53087488-3b41-46fc-99ed-7e672a5a563d">


C) Inverter with stronger NMOS (Wp=2um; Wn=2um)


<img width="760" alt="123097658-f866f780-d44d-11eb-968a-53687020be36" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/b9e20a2d-904f-4e8a-89e8-0a7180928cab">

### Swap NMOS and PMOS: Transient Analysis, VTC

The circuit is modified by swapping NMOS and PMOS with each other. The expected behaviour of the circuit is a buffer with weak output logics. 

Input and Output waveform for transient analysis:

<img width="818" alt="123412772-9d5d0e00-d5cf-11eb-84e6-1a0b863aa091" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/7a3da847-0dc7-46d7-9f35-0b77bc3fc8f5">

Notably, we can observe reduction in the voltage swing as expected.

VTC - Plot between input and output:

<img width="755" alt="123412816-a8b03980-d5cf-11eb-9a7c-c137d22600d8" src="https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/4f75c101-1bf6-4a11-a156-c58bf636a54b">















