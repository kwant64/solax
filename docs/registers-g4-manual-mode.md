# SolaX G4 Manual Mode Registers

This document describes the registers used for manual control.

## Register 31 (0x001F)
SolarChargerUseMode

0 = Self Use  
3 = Manual Mode

---

## Register 32 (0x0020)
Manual Mode Direction

0 = Stop  
1 = Force Charge  
2 = Force Discharge  

---

## Register 36 (0x0024)
Max Charge Current

Unit: 0.1A  
Range: 0 – 300 (0.0A – 30.0A)

---

## Register 37 (0x0025)
Max Discharge Current

Unit: 0.1A  
Range: 0 – 300

---

## Important

Discharge does NOT require negative values.

Direction is determined by Register 32.
