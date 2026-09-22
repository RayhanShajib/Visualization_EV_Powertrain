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
                  │ 3-PHASE DC
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

# Drivetrain and Regeneration (Gearbox, Differential, Braking Energy)
<img width="970" height="437" alt="Screenshot 2026-09-22 153540" src="https://github.com/user-attachments/assets/52005354-9143-4462-bd2f-300e57a57551" />
.
<img width="707" height="352" alt="Screenshot 2026-09-22 154234" src="https://github.com/user-attachments/assets/2723b456-aa3c-4fc0-95b5-97856215d381" />

## Drivetrain and regeneration — Polestar 4

```mermaid
flowchart LR
    A[Battery and inverter<br/>DC to AC] --> B[Motor<br/>343 Nm at shaft]
    B --> C[Reduction gearbox<br/>Ratio 13.8:1]
    C --> D[Differential<br/>Splits torque L/R]
    D --> E[Half-shaft and CV joint<br/>Allows suspension angle]
    E --> F[Wheel hub<br/>~4,700 Nm here]
```

### Driving: battery to wheels
1. **Battery and inverter** — DC converted to AC
2. **Motor** — spins, 343 Nm at shaft
3. **Reduction gearbox** — 13.8:1 ratio, torque × 13.8 ≈ 4,730 Nm
4. **Differential** — splits torque left/right
5. **Half-shaft and CV joint** — carries torque to each wheel, flexes with suspension
6. **Wheel hub** — ~4,700 Nm here, turns the wheel

### Regen braking: wheels to battery
1. **Wheel hub** — spun by the car's momentum
2. **Half-shaft and CV joint** — carries that rotation back
3. **Differential** — recombines rotation from both wheels
4. **Reduction gearbox** — wheel speed × 13.8 = generator speed at motor
5. **Motor** — acts as generator, produces AC
6. **Battery and inverter** — AC converted back to DC, stored in battery

# Cooling, Control and Auxiliary Power

## Cooling System

The Polestar 4 uses a thermal management system to control the temperature of the battery, inverter and electric motors. Cooling is important because these components generate heat during driving and fast charging.

The system uses coolant, pumps and heat exchangers to move heat between different parts of the vehicle.

Main purposes:
- Keep the battery at a suitable operating temperature
- Prevent the motor and inverter from overheating
- Support fast charging
- Improve efficiency and battery life


## Control System

The control system manages the flow of power between the battery, inverter and motor.

Basic power flow:

Battery → Controller/Inverter → Motor → Wheels

The control system receives information from sensors and decides how much power should be delivered to the motor. It also controls regenerative braking and thermal management.


## Auxiliary Power

Not all battery energy is used to move the vehicle. Some energy is required by auxiliary systems.

Examples:
- Cabin heating and air conditioning
- Cooling pumps and fans
- Lights
- Infotainment and displays
- Control electronics
- 12 V electrical system
- Separate battery = 12 V (separate small battery that runs the lights, screens and charging port controls. The 407V pack does not power that directly.)

These auxiliary loads increase total energy consumption and can reduce the driving range.


## Energy Flow

High-Voltage Battery
        │
        ├──→ Inverter → Motor → Wheels
        │
        ├──→ Cooling / Thermal Management
        │
        │──→ Heating / Air Conditioning
        
## Possible Efficiency Improvements

- Better control of battery temperature
- Reduce unnecessary operation of cooling pumps and fans
- Use efficient cabin heating and cooling
- Precondition the battery and cabin while connected to a charger
- Optimize auxiliary power consumption


# Polestar 4

<img width="1536" height="1024" alt="WhatsApp Image 2026-09-22 at 12 28 52" src="https://github.com/user-attachments/assets/adbcbab3-293c-4c35-b20c-f923272ea24c" />







