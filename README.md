# Auto-Irrigation-system
A basic automatic irrigation system that uses a soil sensor and transistor to control a water pump based on soil dryness.

# 🌱 Auto-Irrigation System

A simple, low-cost plant-watering circuit that turns a small DC pump on when the soil is dry and switches it off (in future versions) once the soil is moist.  
Built with an analog soil-moisture probe, a BC547 transistor, and a 9 V power source.

---

## 🧰 Components

| Qty | Component                     |
|-----|------------------------------|
| 1   | Soil-moisture sensor (analog) |
| 1   | BC547 NPN transistor          |
| 1   | Diode (1N4148 or 1N4007)      |
| 1   | DC mini water pump            |
| 1   | 9 V battery (or 5 V supply)   |
| 1   | Resistor (10 kΩ pull-down)    |
| –   | Breadboard & jumper wires     |
| –   | Tubing + container for water  |

## ⚙️ Working Principle

1. **Soil probe** senses moisture as a variable resistance.  
2. When the soil is **dry**, the probe’s voltage output rises.  
3. That voltage biases the **BC547** into saturation, powering the **pump**.  
4. When the soil becomes wet, the voltage should fall and the pump should turn off (see “Known Issue” below).

## 🚧 Known Issue

At present, the pump doesn’t always turn off after watering.  
Possible causes:
- Sensor hysteresis too small  
- Transistor staying latched  

## 🔧 Planned Improvements

- Add an **LM393 comparator** for precise threshold control  
- Upgrade to a **capacitive moisture sensor** (more stable)  
- Drive the pump with a **MOSFET or relay** for higher current  
- Introduce **Arduino/Pico** control for smarter timing & data logging

## 📚 What I Learned

- Using transistors as high-side switches  
- Reading analog sensor output and setting bias points  
- Protecting inductive loads with a fly-back diode  
- Debugging real-world noise and latch-up problems
