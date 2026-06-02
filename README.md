# TapSafe-Women-Safety-System
Adhesive touch-sensor based emergency response system for discreet SOS activation, GPS location tracking, and GSM based alert transmission.

## Overview

TapSafe is a prototype emergency response module developed to provide a discreet and easily accessible method of sending emergency alerts during critical situations.

Unlike conventional safety devices that rely on wearable accessories, visible panic buttons, internet connectivity or smartphone interaction, TapSafe introduces an adhesive touch-based activation mechanism that can be attached to personal belongings such as smartphones, handbags, wallets, helmets, vehicles, or other everyday objects.

The system uses a capacitive touch sensor to trigger an emergency sequence. Upon activation, the device obtains the user's location through GPS and transmits an SOS message using GSM communication while providing haptic feedback through a vibration motor.

------

## Problem Statement

Many existing personal safety solutions face several limitations:

* Dependence on smartphones and internet connectivity.
* Visible emergency buttons that may expose the device.
* Wearable designs that can be forgotten, removed, or damaged.
* Time-consuming activation during stressful situations.
* Bulky form factors that reduce portability.

TapSafe aims to address these challenges through a compact, touch-activated emergency alert system that can be integrated into everyday objects.

---

## How TapSafe Works

1. The user touches the capacitive touch sensor.
2. The microcontroller detects the touch event.
3. GPS coordinates are acquired from the NEO-6M GPS module.
4. The GSM module prepares and sends an SOS message.
5. The emergency message is transmitted to predefined contacts.
6. A vibration motor confirms successful activation.

Emergency Flow:

Touch Sensor → Controller → GPS Location Acquisition → GSM Alert Transmission → Emergency Contact

---

## Applications

Although initially designed as a women safety solution, the concept can be extended to multiple emergency scenarios.

### Personal Safety

* Women safety during emergencies.
* Students travelling alone.
* Night-time commuters.
* Outdoor travelers and hikers.

### Elderly Care

The module can be configured with emergency contacts such as:

* Family members
* Caregivers
* Nearest hospitals
* Ambulance services

allowing elderly individuals living alone to quickly request assistance.

### Vehicle Emergencies

The system can be mounted inside:

* Cars
* Motorcycles
* Trucks

to enable emergency notification after accidents or medical emergencies.

### Medical Emergency Assistance

The device can be configured to notify:

* Hospitals
* Ambulance providers
* Family members

during sudden health emergencies.

---

## Key Features

* Capacitive touch-based activation.
* GPS location tracking.
* GSM-based SOS alert transmission.
* Standalone operation without smartphone dependency.
* Haptic feedback through vibration motor.
* Portable prototype architecture.
* Low-cost implementation.
* Adaptable to multiple emergency scenarios.

---

## How TapSafe Differs from Existing Safety Devices

| Existing Systems              | TapSafe                            |
| ----------------------------- | ---------------------------------- |
| Mostly wearable devices       | Adhesive deployment concept        |
| Visible panic buttons         | Discreet touch activation          |
| Often smartphone dependent    | Independent operation              |
| Bulky accessories             | Compact prototype architecture     |
| Limited placement flexibility | Can be attached to various objects |
| Obvious activation mechanism  | Covert activation approach         |

---

## Prototype Hardware

### Components Used in Prototype

| Component               | Purpose           | Approx. Cost (INR) |
| ----------------------- | ----------------- | ------------------ |
| Arduino Uno             | Main Controller   | 350                |
| GSM 900A                | SMS Communication | 1000               |
| NEO-6M GPS Module       | Location Tracking | 800                |
| Capacitive Touch Sensor | Emergency Trigger | 90                 |
| Vibration Motor         | Haptic Feedback   | 20                 |
| Batteries (2 x 2A)      | Power Supply      | 200                |
| Connecting Wires        | Interconnections  | 40                 |

**Total Cost:** Approximately ₹2500

---

## Proposed Product Components

The original system architecture was intended to use components better suited for miniaturization and commercialization.

| Proposed Component   | Prototype Component    | Reason for Change                                                 |
| -------------------- | ---------------------- | ----------------------------------------------------------------- |
| STM32L0              | Arduino Uno            | STM32CubeIDE software and debugging challenges during development |
| Thin Li-Po Battery   | 2 x 2A Batteries       | Easier availability during prototype testing                      |
| Compact Embedded PCB | Breadboard-based setup | Faster proof-of-concept implementation                            |

The hardware prototype was developed using readily available components while maintaining the intended system functionality.

---

## Challenges Faced During Development

### GPS Satellite Acquisition Delay

The NEO-6M GPS module required a clear outdoor environment for reliable satellite acquisition.

Challenges observed:

* Slow initial GPS lock.
* Difficulty obtaining coordinates indoors.
* Weather and surrounding structures affecting reception.

### GSM Power Requirements

The GSM module demanded significantly higher current during transmission.

Challenges observed:

* Voltage drops during SMS transmission.
* Unstable behavior with insufficient power supply.
* Multiple power optimization attempts before achieving stable operation.

### Compact Design Constraints

The project concept targets an adhesive phone-mounted module.

Challenges observed:

* Arduino Uno occupies substantial space.
* Prototype wiring increases overall size.
* Commercial implementation would require PCB miniaturization.

### Controller Migration Challenges

The original design considered STM32L0 due to its low-power characteristics.

Challenges observed:

* STM32CubeIDE learning curve.
* Configuration and debugging difficulties.
* Limited development time.

As a result, Arduino Uno was selected for prototype validation.

---

## Prototype Results

The developed prototype successfully demonstrated:

* Touch detection through capacitive sensing.
* GPS coordinate acquisition.
* GSM-based SOS message transmission.
* Haptic feedback confirmation.
* Independent emergency alert functionality.

The prototype validated the feasibility of a touch-based emergency response architecture.

---

## Future Scope

Future improvements may include:

* Custom PCB development.
* Migration to STM32L0 or other low-power controllers.
* Thin rechargeable Li-Po battery integration.
* Bluetooth Low Energy (BLE) support.
* Mobile application integration.
* Multi-level touch activation patterns.
* Waterproof enclosure design.
* AI-assisted emergency detection.
* Commercial product miniaturization.

---

## Contributors

### Shreya Thakur

Project Lead and Software Development

### Karan Pandit

Hardware Development and Testing

---

## Disclaimer

This repository presents the project concept, prototype implementation, and development outcomes.

Detailed implementation documents, research manuscripts, and proprietary design information are intentionally excluded from the public repository.
