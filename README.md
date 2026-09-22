EV POWERTRAIN OPTIMISATION PROJECT

#Introduction
This project explores how an EV powertrain works and investigates ways to improve its efficiency.

#Project Goal
Understand the system, identify energy losses, establish baseline performance, and evaluate possible improvements.

#Project Details
Course: Designing and implementing data pipeline 
Duration: _______
Supervisor: Leo & JP
Vehicle / Model: Polestar 4

#Project Scope
Charging, battery, inverter, motor, mechanical drivetrain, regenerative braking, cooling and control systems.

#Tools and Data
Software and tools: 
Specifications and data sources: 

#Expected Outcomes
Powertrain diagrams, a baseline model or analysis, evaluation of efficiency improvements, and documented results.



WEEKLY UPDATES

Week 1: Understanding the Powertrain
Dates: ____________________

Planned Work
Nayeem: Study charging, battery and BMS.

Rayhan: Study inverter and motor operation.

Shahriar: Study drivetrain and regenerative braking.

Sadia: Study cooling, control and auxiliary power.

Everyone: Combine findings and diagrams.

Completed Work:
Battery - the cars main battery is a lithium-ion pack made of 110 smaller cells connected together. Cells are connected in series so the voltages add up. Each cell is about 3.7 volt makes the whole pack equivalent of 407 volt. A higher voltage means the same power can be delivered with less current which keeps cables and components smaller and cooler. 
Cells = 110
Nominal voltage = 407 V 
Total capacity = 100 kWh
Usable capacity = 94 kWh
DC charging (10% - 80%) = 135 kW
DC charging(Max.) = 200 kW
AC charging = 22 kW(Max.)
Separate battery = 12 V (separate small battery that runs the lights, screens and charging port controls. The 407V pack does not power that directly.)
Why is DC charging faster than AC charging- with DC the conversion from AC to DC is done in the big external charger, so the energy goes directly into the battery. With AC, the cars own smaller onboard charger has do the conversion, so the power is limited. 
Mathematical Calculations:
V cell = V pack / N
       = 407V / 110
       = 3.7 V (Approx.)
Usable Energy:
Usable percentage = usable energy / total energy * 100
                  = 94kWh / 100kWh * 100
                  = 94%
Reserve = 100kWh - 94kWh
        = 6kWh (this energy is reserved as buffer so that the battery life remain safe.)
Current during Fast Charging:
Formula: I = P / V
Working:
At 135kW: 135000W / 407V = 331.7A
At 200kW: 200000W / 407V = 491.4A
Charging Time from 10% to 80%(DC):
Formula: Energy = (80% - 10%) * Capacity, and t = E / P
Energy = 0.70 * 100kWh = 70kWh
t = 70kWh / 135kW = 0.519h = 31.1min
(If the usable energy is 94kWh than the approximate time is 29 minutes.)
AC charging time from 0% to 100%(Usable Energy)
Formula: t = E / P
           = 94kWh / 22kW
           = 4.27 Hour = 4 hour and 16 minutes
Summary of Results:
Voltage per cell = 3.7 V
Usable Share / Reserve = 94% / 6kWh
Capacity = 231Ah(Usable)
Current at 135kW / 200kW = 332 A / 491 A
DC charging 10-80% = Approx. 31 minute
AC charging 0-100%(Usable) = Approx. 4 hour 16 minute


# Inverter and Motor

```text
                 Inverter and Motor
                         
        ┌───────────────────┐
        │   HIGH-VOLTAGE    │
        │      BATTERY      │
        │                   │
        │      DC POWER     │
        └─────────┬─────────┘
                  │
                  │ DC
                  ▼
        ┌───────────────────┐
        │      INVERTER     │
        │                   │
        │     DC → AC       │
        │                   │
        │  Power switches   │
        │       + PWM       │
        └─────────┬─────────┘
                  │
                  │ 3-PHASE AC
                  ▼
        ┌───────────────────┐
        │     PMSM MOTOR    │
        │                   │
        │     STATOR        │
        │       ↓           │
        │ Rotating magnetic │
        │      field        │
        │       ↓           │
        │      ROTOR        │
        │   Permanent       │
        │     magnets       │
        └─────────┬─────────┘
                  │
                  │ Rotation
                  │ + Torque
                  ▼
        ┌───────────────────┐
        │   REDUCTION GEAR  │
        └─────────┬─────────┘
                  │
                  ▼
              ┌───────┐
              │ WHEELS│
              └───────┘
                  │
                  ▼
             CAR MOVES
```


           
# PMSM Motor:

<img width="800" height="600" alt="oSobgcMlYnns2PwhHLF6nqvhcVGvVHhfbh0Hodj5ZTU5mGYm1gDeecdZZcUys93eUCfOfEjXwMSrGfFUcsET865axTNW5xOmsi78qyL8UE4m_cKla8eIKu_l7VZyn3wQDLIaTQXhkt7JxmiGl1x4dPfk5Yfa5UQP68lYHwckXq8" src="https://github.com/user-attachments/assets/78ff5733-6049-4b06-b3f2-3c41d61ac272" />


# Polestar 4

<img width="800" height="600" alt="oSobgcMlYnns2PwhHLF6nqvhcVGvVHhfbh0Hodj5ZTU5mGYm1gDeecdZZcUys93eUCfOfEjXwMSrGfFUcsET865axTNW5xOmsi78qyL8UE4m_cKla8eIKu_l7VZyn3wQDLIaTQXhkt7JxmiGl1x4dPfk5Yfa5UQP68lYHwckXq8" src="https://github.com/user-attachments/assets/297e5d09-2cf3-4b47-bbf7-021d2faf1b3e" />






