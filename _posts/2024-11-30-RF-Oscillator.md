---
title: A 5.4GHz Integrated Circuit Oscillator
categories: []
tags: [RF, Keysight ADS, Colpitts]
pin: false
math: true
mermaid: true
image: 
  path: /assets/img/RF_oscillator/thumbnail.jpg
---

## Introduction

This solo project focuses on the theory, design, and simulation to verify a **5.4GHz Colpitts RF oscillator**. The design aimed for **high efficiency, low power consumption, and stable oscillation**, with verification through simulations and analytical calculations.

## Requirements

- **Supply Voltage:** 3.5V
- **Lowest possible current consumption**  
- **Output Voltage:** as large as possible, min 1.5Vpp  
- **Load Resistance:** 1kΩ  
- **Oscillation Frequency:** 5.4GHz  

## Circuit Conversion

### Topology Conversion
The given oscillator topology was a **balanced Colpitts oscillator**, which was converted into a standard **single-ended configuration** to simplify analysis and design. Key transformations included:
- Splitting the shared **capacitor C2** into two individual capacitors.
- Adjusting the **load resistor** from **R_L** to **0.5R_L** for single-sided operation.
![image](/assets/img/RF_oscillator/schematic_manipulation.jpeg)
## Design Considerations

### Biasing
![class_C](/assets/img/RF_oscillator/classes.jpg){: width="400" height="300" }{: .right }
A **high-efficiency Class C biasing scheme** was chosen to ensure minimal power consumption while maintaining stable oscillation. The selected **biasing current was 5mA**, which provided an optimal trade-off between gain and efficiency.


Using:
\begin{align}  R_e = \frac{V_{cc} - V_{ce}}{I_c(1 + \frac{1}{h_{FE}})}\end{align}

I determined **R_e = 300Ω** and **R_1 = 1.7kΩ** through analytical calculations and simulation verification.

### Frequency Determination
The Colpitts oscillator's frequency is given by:
$$ f_0 = \frac{1}{2\pi\sqrt{L C_{ser}}} $$
where **L = 1.06nH** and calculated capacitor values **C1 = 3pF, C2 = 1pF** were selected to achieve the **5.4GHz target frequency**.

### Decoupling and Stability
To ensure circuit stability:
- **Decoupling capacitors** were selected based on reactance constraints, with **C_cpl1 = 2pF**.
- **Parasitic effects** were analyzed and included in the final model to account for real-world performance deviations.

## Simulation and Testing

### Transient Simulation
The design was simulated in **Keysight ADS**, verifying the following:
- **Oscillation frequency:** ~5GHz (slightly lower than the 5.4GHz target due to parasitics).
- **Output voltage swing:** 2Vpp, exceeding the minimum 1.5Vpp requirement.
- **Stability:** Rapid stabilization within **4ns**.

### Efficiency Analysis
Using Fourier analysis and Bessel functions, the **conduction angle θ** was found to be **95°**, leading to an estimated **efficiency >90%**.

## Conclusion

The **5.4GHz Colpitts oscillator** achieved:
✅ **Stable oscillation** with low power consumption  
✅ **High output voltage (~2Vpp)**  
✅ **Efficiency exceeding 90%**  
❌ **Frequency needs further investigation**

Minor frequency deviations were attributed to **parasitic capacitances**, suggesting future iterations could incorporate **tuning capacitors** for fine adjustments. This design successfully met its performance targets and demonstrated **key RF design principles** in practical implementation.

![Simulation Result](/assets/img/RF_oscillator/sim_results.png)

