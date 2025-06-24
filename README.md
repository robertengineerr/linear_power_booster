# Linear Power Booster | Guitar Pedal
Linear guitar signal booster with BJT amplification, true bypass switching, and power input protection.

![image](https://github.com/user-attachments/assets/b890c126-4d2c-4b30-824b-5c6aebb7c321)

[![View PCB in KiCanvas](https://img.shields.io/badge/VIEW%20PCB-KiCanvas-blue?logo=github)](https://kicanvas.org/?github=https://github.com/robertengineerr/linear_power_booster/blob/main/linear_power_booster.kicad_pcb)

[![View Schematic in KiCanvas](https://img.shields.io/badge/VIEW%20Schematic-KiCanvas-blue?logo=github)](https://kicanvas.org/?github=https://github.com/robertengineerr/linear_power_booster/blob/main/linear_power_booster.kicad_sch)

BJT Amplifier
This is the core amplification stage. A single NPN BJT (Q1) amplifies the input signal from a guitar or similar audio source. Capacitors C1 and C2 act as AC coupling (DC-blocking) caps, allowing only the AC signal through. R1 and R2 form a voltage divider to bias the base of Q1, while R3 sets emitter current for gain stability. The amplified signal is output through C2, with a variable resistor (RV1) used to control output volume. This design provides a clean linear boost to the input signal.

Power
This section manages power input and protection. It accepts either a 9V barrel jack or battery input, with diode D2 preventing reverse polarity damage. The capacitor C3 provides basic filtering to smooth out voltage spikes, and the TVS0500DRV IC (U1) protects downstream components from overvoltage by clamping any input above ~9V. The design ensures safe and clean power delivery to the circuit.

Bypass System
This section allows toggling between the amplified signal and the unprocessed (dry) signal. It uses a 3PDT switch (S1) to route the signal either through the amplifier or directly from input to output. Capacitor C4 provides AC coupling for the bypassed signal. This system is commonly used in audio pedals to allow true bypass functionality, preserving the original signal when the effect is disengaged.
