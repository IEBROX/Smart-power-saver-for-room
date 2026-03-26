# Components List

This document contains the list of all electronic components used in the project **"Motion Detector Using PIR Sensor"** along with their quantities and functions.

---

## 1. Components Required

| Sr. No. | Component Name | Quantity | Function / Purpose |
|--------|----------------|----------|--------------------|
| 1 | PIR Sensor (HC-SR501) | 1 | Detects human motion by sensing infrared radiation |
| 2 | NE555 Timer IC | 1 | Generates time delay in monostable mode |
| 3 | BC547 NPN Transistor | 1 | Works as a switching transistor to drive relay |
| 4 | 5V Relay Module / Relay | 1 | Controls the connected load (light/fan/appliance) |
| 5 | Potentiometer (100KΩ) | 1 | Adjusts the output ON-time delay |
| 6 | Electrolytic Capacitor (470µF / 25V) | 1 | Used in RC timing network with 555 timer |
| 7 | Resistor (10KΩ) | 1 | Base resistor for BC547 transistor |
| 8 | Resistor (1KΩ) | 1 | Current limiting resistor for LED |
| 9 | LED (Red or Green) | 1 | Indicates output/load ON condition |
| 10 | 10nF Capacitor (0.01µF) | 1 | Noise filtering capacitor for Pin 5 of 555 timer |
| 11 | Breadboard | 1 | Used for assembling the circuit without soldering |
| 12 | Jumper Wires | As required | Used for making circuit connections |
| 13 | 5V DC Power Supply / USB Supply | 1 | Powers the complete circuit |

---

## 2. Component Details

### 2.1 PIR Sensor (HC-SR501)
The PIR sensor is the main sensing component of the project. It detects infrared radiation emitted by the human body and gives a HIGH output when motion is detected.

**Main Pins:**
- **VCC** → +5V supply
- **OUT** → Output signal
- **GND** → Ground

**Function in this project:**
- Detects human movement
- Sends trigger signal to the timer circuit

---

### 2.2 NE555 Timer IC
The NE555 Timer IC is used in **Monostable Mode** to generate a time-controlled output pulse.

**Function in this project:**
- Produces a HIGH output for a fixed duration after PIR trigger
- Controls how long the load stays ON

**Important Pins Used:**
- **Pin 2** → Trigger
- **Pin 3** → Output
- **Pin 4** → Reset
- **Pin 5** → Control Voltage
- **Pin 6** → Threshold
- **Pin 7** → Discharge
- **Pin 8** → VCC

---

### 2.3 BC547 NPN Transistor
The BC547 transistor is used as a **switching device**.

**Function in this project:**
- Receives signal from the 555 timer output
- Amplifies current to drive the relay coil

**Terminals:**
- **Base (B)**
- **Collector (C)**
- **Emitter (E)**

---

### 2.4 5V Relay Module / Relay
The relay acts as an electrically isolated switch.

**Function in this project:**
- Switches ON/OFF the external load
- Allows low-voltage circuit to control higher-voltage load safely

**Relay Contacts:**
- **NO** → Normally Open
- **NC** → Normally Closed
- **C** → Common

**Used Connection:**
- Load is connected through **NO** and **C**

---

### 2.5 Potentiometer (100KΩ)
The potentiometer is used as a variable resistor in the RC timing network.

**Function in this project:**
- Controls the delay time of the 555 timer output
- Allows adjustment of load ON duration

**Formula used:**
```text
T = 1.1 × R × C
