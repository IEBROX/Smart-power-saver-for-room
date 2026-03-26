# Timing Calculation

This document explains how the output ON-time of the **NE555 Timer IC** is calculated in the **Motion Detector Using PIR Sensor** project.

---

## 1. Purpose of Timing Calculation

In this project, the **555 Timer IC** is configured in **Monostable Mode**.

This means:

- when motion is detected,
- the output of the 555 timer goes **HIGH**,
- and remains HIGH for a fixed time,
- after which it automatically returns **LOW**.

This time duration determines how long the:

- **LED remains ON**
- **relay remains activated**
- **load stays ON**

So naturally we need math. Humanity’s favorite punishment.

---

## 2. Monostable Mode Timing Formula

The output pulse duration of a 555 timer in monostable mode is given by:

```text
T = 1.1 × R × C
