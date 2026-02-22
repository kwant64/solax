# SolaX Energy Toolkit
## Manual Control for SolaX X1-Hybrid G4 via Modbus (Node-RED)

A fully local, Modbus-based manual control toolkit for the SolaX X1-Hybrid G4 inverter.

No cloud.
No API.
No EMS gateway.
Direct register-level control.

---

# 🎯 What This Project Does

This toolkit provides a safe and transparent way to manually control:

- Self Use mode
- Manual mode
- Force Charge
- Force Discharge
- Charge current limit
- Discharge current limit

All communication happens via Modbus TCP using official G4 registers.

---

# ⚙️ Supported Inverter

- SolaX X1-Hybrid G4  
(Other G4 models may work but are not tested)

---

# 🧠 Control Philosophy

This project intentionally keeps logic simple and explicit.

You execute manual steps in the correct order:

### To Charge
1. Set Manual Mode (Register 31 → 3)
2. Set Charge Current (Register 36)
3. Set Direction (Register 32 → 1)

### To Discharge
1. Set Manual Mode (Register 31 → 3)
2. Set Discharge Current (Register 37)
3. Set Direction (Register 32 → 2)

### To Stop
- Register 32 → 0

### To Return to Self Use
- Register 31 → 0

No automation is hidden.
No background watchdog.
No implicit state machine.

This is intentional.

---

# 📦 Installation

## Requirements

- Node-RED
- node-red-dashboard
- node-red-contrib-modbus
- Modbus TCP access to inverter
  (example: Waveshare TCP → RS485 gateway)

## Import Flow

1. Open Node-RED
2. Menu → Import
3. Select:
