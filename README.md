# ENGR 120/121 Design Project

## 1. Project Overview  
This project involved the design, integration, and demonstration of a mobile robot capable of performing a target approach, object placement, and task completion signaling. The robot was designed to integrate **mechanical, structural, electrical, and software systems** into one cohesive solution.  

The final system demonstrates the following:  
- Autonomous movement towards a beacon/target.  
- Controlled and precise placement of an object onto the target without disturbing it.  
- Post-task signaling and safe movement to the arena’s side.

![1](/screenshots/1.jpg)  
![2](/screenshots/2.jpg)  

---

## 2. Objectives  
- Integrate mechanical, structural, electrical, and software systems.  
- Demonstrate task completion without external intervention.  
- Showcase system robustness under varied beacon/target placements.  

---

## 3. System Architecture  

### 3.1 Mechanical & Structural  
- **Chassis**: Lightweight, stable base designed to minimize vibrations.  
- **Drive System**: Two DC motors with differential drive for maneuverability.  
- **Object Placement Mechanism**: Servo-driven arm/gripper system to deliver the object precisely onto the target.  

### 3.2 Electrical  
- **Microcontroller**: Arduino Uno (main controller).  
- **Motor Drivers**: L298N dual H-bridge.  
- **Sensors**:  
  - IR beacon detector for target localization.  
  - Limit switches for arm/gripper control.  
- **Power Supply**: Rechargeable Li-ion battery pack with regulated outputs.  
- **Wiring**: Routed for neatness and easy debugging (per grading requirement).  

### 3.3 Software  
- **Finite State Machine (FSM)**: Controls robot behavior across the following states:  
  1. **Idle/Initialize** – Await power-up or button trigger.  
  2. **Search/Localize** – Detect beacon and orient towards target.  
  3. **Approach** – Controlled movement towards beacon.  
  4. **Place Object** – Arm/gripper delivers object without moving target.  
  5. **Retreat** – Robot moves aside safely.  
  6. **Signal Completion** – LED indicator + sound buzzer.  

- **Programming Language**: Arduino C++.  
- **Code Features**:  
  - Modular functions for readability.  
  - Clear traceability from FSM diagram to code implementation.  
  - Extensive inline comments for maintainability.  

---

## 4. Testing Strategy  
- Incremental subsystem tests (mechanical, electrical, software).  
- Full-system dry runs under multiple beacon/target placements.  
- Debugging and optimization for smooth localization and controlled approach.  
