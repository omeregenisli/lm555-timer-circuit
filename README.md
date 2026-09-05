# ⏱️ LM555 Astable Timer Circuit & Variable-Frequency Pulse Generator

A hardware prototyping and circuit analysis project focused on configuring the versatile **LM555 timer IC** in **astable multivibrator mode** to generate continuous square wave pulses with real-time frequency modulation.

---

## 🎥 Video Presentation & Hardware Demo
▶️ **[Watch Full English Presentation & Circuit Demonstration on YouTube (6:48)](https://www.youtube.com/watch?v=IWLITI55ebI)**

*(The video includes a comprehensive technical walkthrough followed by a live breadboard demonstration showing real-time frequency tuning via potentiometer).*

---

## 📌 Circuit Overview & Operation

The circuit operates as a free-running relaxation oscillator (astable mode). The external timing capacitor ($C$) charges through $(R_1 + R_2)$ and discharges through $R_2$ via pin 7 (Discharge). This cyclic charge/discharge between $\frac{1}{3}V_{CC}$ and $\frac{2}{3}V_{CC}$ triggers the internal flip-flop, producing an alternating high/low square wave at pin 3 (Output).

An integrated **10kΩ potentiometer** allows real-time adjustment of the equivalent timing resistance, dynamically modulating the oscillation period and LED flash rate.

### Mathematical Formulation
The period ($T$) and frequency ($f$) are governed by:
$$T = \frac{1}{f} \approx 0.693 \times (R_1 + 2R_2) \times C$$

---

## 🛠️ Circuit Elements & Specifications

| Component | Design Value / Model | Function |
|---|---|---|
| **Timer IC** | LM555 (Texas Instruments) | Core precision timing pulse generator |
| **Resistors** | 2× 1.6 kΩ | Base timing threshold & current limiting |
| **Potentiometer** | 10 kΩ (Rotary) | Real-time frequency / duty cycle modulation |
| **Capacitor** | 47 µF (25 V Electrolytic) | Timing charging/discharging tank |
| **Output Indicator** | Red 5mm LED | Visual verification of pulse train |
| **Power Source** | 9 V DC Battery | System supply voltage ($V_{CC}$) |

---

## ⚠️ Challenges & Engineering Solutions

1. **LED Overcurrent & Thermal Runaway:**  
   * *Problem:* In early breadboard tests, inadequate current limiting caused an LED to burn out under direct 9V switching.
   * *Solution:* Recalculated and placed a dedicated current-limiting resistor in series with output pin 3 to ensure operating current remains safely below 20mA.
2. **Breadboard Contact Resistance:**  
   * *Problem:* Loose jumper wire contacts caused intermittent signal drops.
   * *Solution:* Re-routed and trimmed jumpers close to the breadboard plane to eliminate stray capacitance and loose joints.
3. **High-Frequency Visual Aliasing:**  
   * *Problem:* At minimum potentiometer resistance, oscillation frequency surpassed human eye persistence of vision (~50–60Hz), making the LED appear solid ON.
   * *Solution:* Calibrated the timing capacitor value ($47\mu\text{F}$) so the dynamic frequency range spans clearly distinguishable slow blinks up to continuous illumination.

---

## 💰 Budget Analysis

The entire prototype was built with reusable laboratory equipment and highly accessible consumables:
- **Total Prototype Cost:** ~120 ₺
- **Reusable Assets:** LM555 IC, Breadboard, Potentiometer, Jumper Wires
- **Consumables:** Resistors, Capacitor, LED

---

## 📄 Documentation

The complete slide deck covering theoretical background, pinout configurations, and troubleshooting steps is available in this repository:
- 📑 [LM555_TIMER_CIRCUIT_GROUP_PROJECT.pdf](LM555_TIMER_CIRCUIT_GROUP_PROJECT.pdf)

---

## 👥 Project Team

- **Ömer Ege Nişli** (Student ID: 2024502054)
- **Çağrı Can** (Student ID: 2024502030)

*Department of Electrical & Electronics Engineering, Dokuz Eylül University (January 2025)*
