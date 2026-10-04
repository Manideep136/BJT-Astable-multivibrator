# BJT-Astable-multivibrator


## 📌 Project Overview

The **BJT Astable Multivibrator** is a transistor-based oscillator circuit that continuously switches between two states without using an IC.

The circuit is built using two **2N3904 NPN transistors**, two LEDs, resistors, and capacitors. The two transistor stages are cross-coupled through capacitors, causing the transistors to turn ON and OFF alternately.

As a result, the two LEDs blink alternately, demonstrating the basic principles of **transistor switching, capacitor charging/discharging, feedback, and oscillation**.

The complete circuit and PCB were designed using **KiCad 9.0**.

---

## 🎯 Objectives

The main objectives of this project are:

- Understand the working principle of an astable multivibrator.
- Learn transistor switching using NPN transistors.
- Understand capacitor charging and discharging.
- Study cross-coupled transistor circuits.
- Design a complete schematic using KiCad.
- Assign appropriate footprints to components.
- Design and route a PCB.
- Perform ERC and DRC checks.
- Understand the relationship between resistor/capacitor values and oscillation frequency.

---

## ⚙️ Circuit Overview

The circuit consists of two **2N3904 NPN transistors** connected in a cross-coupled configuration.

Each transistor has:

- A collector resistor
- A base resistor
- An LED in the collector branch
- A coupling capacitor connected to the opposite transistor

The circuit is powered by a **3.7 V DC supply**.

### Basic Circuit Structure

```text
              +3.7V
                │
          ┌─────┴─────┐
          │           │
         R1          R4
        1 kΩ        1 kΩ
          │           │
         LED1        LED2
          │           │
         Q1          Q2
      2N3904      2N3904
          │           │
         GND         GND

       Cross-Coupled
       Capacitor Network

        Q1 Collector
             │
             C1
             │
        Q2 Base

        Q2 Collector
             │
             C2
             │
        Q1 Base
