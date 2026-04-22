# Grid Frequency and ROCOF Monitoring System

A real-time embedded system to monitor grid frequency and Rate of Change of Frequency (ROCOF) using the TM4C123GH6PM microcontroller.

**Overview**
Maintaining 50 Hz grid frequency is critical for power system stability.  
This project detects frequency deviations and rapid changes (ROCOF) to identify grid instability and islanding conditions.

**System**
- Input: 230V AC → Step-down transformer (18V)
- Signal conditioning: attenuation + 1.65V DC bias
- Microcontroller: TM4C123GH6PM (12-bit ADC)
- Output: UART (PC terminal)

**Working**
- Zero Crossing Detection (ZCD) for frequency measurement  
- Timer-based period calculation  
- Moving average filtering (reduces noise)  
- ROCOF computed every 1 second  

 **Detection Logic**
- Normal: 49.5 – 50.5 Hz  
- Critical: ROCOF > ±1 Hz/s  
- Alerts via UART + LEDs  

**Results**
- Stable grid: ~49.9 Hz, ROCOF ≈ 0  
- Fault: ROCOF spikes detected, alerts triggered 

**Highlights**
- Real-time monitoring  
- Low-cost embedded solution  
- Fast detection (< 1 sec)
