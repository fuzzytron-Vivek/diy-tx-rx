# Receiver Module

## Overview
This module implements the **receiver-side firmware** for the custom RC link.  
It is responsible for **decoding control packets**, validating link integrity, and generating **safe, predictable actuator outputs**.

---

## Core Responsibilities
- Receive and parse RF control packets  
- Map decoded values to PWM signals for servos and ESC  
- Maintain deterministic update timing  
- Enforce safe default states on signal loss (**failsafe**)

---

## Failsafe Behavior
In the absence of valid packets beyond a defined timeout:
- Control outputs are driven to predefined safe values  
- Throttle is reduced to a non-driving state  
- Actuator outputs remain stable to avoid oscillations  

This ensures predictable behavior under link degradation or loss.

---

## Testing Notes
Receiver behavior was validated through **bench testing**, including:
- Packet loss simulation  
- Power cycling scenarios  
 

---

## Scope
This module is intended for **experimental and educational use** and was developed with an emphasis on **robust signal handling and safety-aware design**, rather than flight performance.
