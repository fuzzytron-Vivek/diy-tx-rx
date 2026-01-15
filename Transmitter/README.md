# Transmitter Module

## Overview
This module implements the **transmitter-side firmware** for the custom RC link.  
It is responsible for **reading user input controls** and transmitting them as structured control data to the receiver.

---

## Core Functionality
- Read analog input values from control interfaces  
- Normalize and map inputs to defined control ranges  
- Package control data into a fixed-format packet  
- Transmit packets at a consistent update rate  

---

## Design Notes
The transmitter logic is intentionally kept **simple and deterministic**.  
No adaptive or autonomous behavior is implemented; all outputs directly reflect user inputs after basic conditioning.

---

## Testing Notes
Functionality was validated through:
- Input range checks  
- Continuous transmission observation  
- End-to-end response verification with the receiver  

---

## Scope
This module is designed for **manual control experimentation** and educational use.  
It prioritizes clarity and predictability over advanced features or optimizations.
