# 🏁 My Variant – DartXtract (Concept Race)

<p align="center">
  <img src="https://github.com/user-attachments/assets/b24b1d0e-303c-4aef-97f6-76a114d7133d" alt="DartXtract Circuit" width="450"/>
</p>

---

## 1. Starting Point
- **Assignment:** Retrieve darts automatically and return them to the player.  
- **Requirements considered:**  
  - Retrieve 3–7 darts per round without bending or posture change.  
  - Safe handling (no injury, no dart tip damage).  
  - Accessible for wheelchair users.  
  - Budget < €200 (prototype level).  
  - Compatible with steel-tip darts.

## 🎥 Project Demo Videos

### Prototype Demo (Final Optimised Solution)
<p align="center">
  <a href="https://www.youtube.com/watch?v=XfCU9qc8eJU">
    <img src="https://img.youtube.com/vi/XfCU9qc8eJU/0.jpg" alt="Prototype Demo Video" width="600">
  </a>
</p>
<p align="center"><em>Watch the final prototype of the Dart Retrieval System in action.</em></p>

---

### Concept Simulation Demo
<p align="center">
  <a href="https://www.youtube.com/watch?v=Dweflsoa8-w">
    <img src="https://img.youtube.com/vi/Dweflsoa8-w/0.jpg" alt="Simulation Demo Video" width="600">
  </a>
</p>
<p align="center"><em>Watch the working simulation of the Dart Retrieval System (Concept Phase).</em></p>

---

##  Subfunctions in My Variant (DartXtract)

The chosen path from the Morphological box 

| **Subfunction**             | **Chosen Solution in My Variant**           |
|------------------------------|---------------------------------------------|
| User Input Information       | Pressure-sensitive film (Velostat)          |
| Process Input Information    | Arduino logic (3 hits trigger)             |
| Extraction Mechanism         | Gravity Tilt Board                         |
| Place Darts in Return Tray   | Electromagnet                              |
| Prevent Bounce               | Rubber Brushings / Foam Damping            |
| Return Darts                 | Gravity Chute                              |
| Align Darts                  | Funnel-shaped loader guide                 |
| Load Darts in Pick-Up Bay    | Slot-based foam tray                       |
| Adjusting Height             | Inclined tray surface (30°–45° adjustable) |
| User Feedback Information    | Piezo Buzzer                               |
| Emergency Stop               | Mushroom Emergency Button                  |

---

## 2. Concept Overview (Mode of Operation)

<p align="center">
  <img src="https://github.com/user-attachments/assets/439c39d8-53ce-451e-aa20-632afa30b2b1" alt="Subfunctions Table" width="500"/>
</p>

---

### Detection & Trigger
- **Sensor:** Velostat pressure-sensitive film mounted behind the dartboard.  
- **Logic:** Arduino Uno counts impacts, triggers retrieval after three darts.  
- **Protection:** Foam ring prevents compression, maintains sensitivity.

<p align="center">
  <img width="500" height="348" alt="image" src="https://github.com/user-attachments/assets/d4b63c18-be3d-4d43-8ce5-024fcd08c982" />
</p>

### Control Logic
- Arduino processes sensor signal → triggers tilt, electromagnet, buzzer.  
- Outputs: Servo motor (tilt), Electromagnet (assist), Piezo buzzer (feedback).

<p align="center">
  <img width="500" height="618" alt="image" src="https://github.com/user-attachments/assets/27379911-8c2a-458e-8aad-ea6df15fbb67" />
 </p>

### Extraction Mechanism
- **Tilting Board:** Servo/gear motor tilts dartboard 90° → gravity releases darts.  
- **Electromagnet:** Mounted at 90° to board → 2s pulse → loosens stuck darts.  

<p align="center">
<img width="500" height="479" alt="image" src="https://github.com/user-attachments/assets/70dd394b-af7f-494a-9579-730af812536b" />
 </p>

<p align="center">
  <img width="508" height="259" alt="image" src="https://github.com/user-attachments/assets/7850f650-0b0b-4821-9daa-1d7e250f2ec7" />
 </p>

### Return System
- Darts slide onto **angled ramp** → pass through **funnel guider** → collected in **slot-based foam tray**.  
- Foam padding at impact zones prevents bounce, noise, and damage.  
- Tray slots hold darts individually for safety and ergonomics.

<p align="center">
  <img width="400" height="649" alt="image" src="https://github.com/user-attachments/assets/2de4b0b7-5dab-4199-98e5-1f6e210969a9" />
   </p>
   <p align="center">
  <img width="400" height="333" alt="image" src="https://github.com/user-attachments/assets/3e587e3f-08b0-407c-95b3-8d293faca4e8" />
    </p>
   <p align="center"> 
  <img width="400" height="620" alt="image" src="https://github.com/user-attachments/assets/9c1a9339-3ad9-476c-919e-cf68ae901a31" />
 </p>

### Additional Features
- Adjustable ramp height/angle.  
- Audio feedback via buzzer.  
- Emergency stop (mushroom button) halts the system instantly.

 <p align="center">
   <img width="499" height="412" alt="image" src="https://github.com/user-attachments/assets/eaa4d469-d190-4ec9-ad81-a545d5503031" />
 </p>

---

## 3. Advantages & Disadvantages

### Advantages
- Hands-free retrieval, no posture change.  
- Faster gameplay flow, user-friendly.  
- Safe design (foam damping, low torque motors).  
- Affordable, modular, and compact.  
- Arduino-based → easy to upgrade.  

### Disadvantages
- Magnet reliance → may not work with non-metal darts.  
- Ramp angle needs precise calibration.  
- Sensor reliability depends on foam wear/calibration.  
- Slightly complex mechanical synchronisation.  

---

## 4. Technical Proofs

### Torque Requirement for Tilt
- Mass of 3 darts = 0.075 kg, distance ~0.15 m.  
- Force ≈ 0.75 N, torque ≈ 0.11 Nm.  
- Well within range of standard servo/DC gear motor (<8 Nm capacity in LoR).  

### Ramp Slope Requirement
- Dart mass = 25 g, μ = 0.2.  
- For sliding: θ ≥ 12°.  
- Conclusion: ramp slope > 12° ensures smooth flow without bounce.  

---

## 5. Parts List & Cost Estimate
| Component | Source | Cost (€) |
|-----------|--------|----------|
| Arduino Uno R3 | Amazon | 13.00 |
| Velostat Sensor Film | Amazon | 11.99 |
| Foam Ring Spacer | Amazon | 15.39 |
| DC Gear Motor (JGA25-370) | Amazon | 15.59 |
| Electromagnet (12 V) | Amazon | 12.00 |
| Jumper wires + Breadboard | Amazon | 16.99 |
| Piezo Buzzer Module | Amazon | 2.75 |
| Foam (ramp, tray inserts) | Amazon | 10.90 |
| Slot-based Tray | Amazon | 9.59 |
| Aluminium Sheet (0.44 m²) | Amazon | 21.65 |
| Emergency Stop Button | Amazon | 8.99 |
| Knob, Screws, Regulators, Resistors | Amazon | ~40.00 |
| **3D Printing (funnel, electronics box, hinge fix)** | Internal | ~50.00 |
| **Total** |   | **≈ €240.44** |

Slightly over €200 budget, but feasible and optimizable.

---

## 6. LoR Compliance
- Retrieval force < 0.8 N  
- Retrieval ≤ 15 s for 3 darts  
- Accessible to wheelchair users  
- Emergency stop included  
- Cost slightly above €200 target  
- Sensor reliability (Velostat wear over time)  

---

## Technical Drawings
<p align="center">
<img width="600" height="634" alt="image" src="https://github.com/user-attachments/assets/83f43da7-d142-47cc-97be-286ca036383c" />
<img width="600" height="581" alt="image" src="https://github.com/user-attachments/assets/2919b94d-5275-4d25-b8fe-844c76a6e55c" />
</p>

---

## 7. Electronics & Control

### 7.1 Tinkercad Circuit Diagram
The control system was designed and tested in **Tinkercad**.  
It includes:  
- Arduino Uno R3 (controller)  
- Velostat pressure sensor (impact detection)  
- Servo/DC gear motor (tilt control)  
- Electromagnet (dart release assist)  
- Piezo buzzer (audio feedback)  
- Emergency stop (safety cutoff)

<p align="center">
<img width="1000" height="1396" alt="Screenshot 2025-09-21 184115" src="https://github.com/user-attachments/assets/50b925b2-3c2f-4d0b-9023-7e0897db760d" 
</p>
<p align="center">
<img width="1000" height="1610" alt="Screenshot 2025-09-21 184137" src="https://github.com/user-attachments/assets/20591755-46da-4448-9069-de2b757516d9" />
</p>

---

### 7.2 Arduino Code
The Arduino code handles sensor input, motor control, magnet activation, and feedback.  
You can view the complete code here:  

📄 [Arduino Code (DartXtract)](./Code/dartxtract.ino)

---

## 8. Conclusion
The **DartXtract** variant demonstrates a **structured, feasible, and safe** dart retrieval system.  
- It retrieves darts automatically in under 15 seconds.  
- Accessible and ergonomic for all players.  
- Built from affordable, widely available components.  
- Minor refinements (sensor robustness, foam durability, magnet alternatives) would improve real-world reliability.  

This variant contributed core elements (magnetic assist + funnel return + safety systems) that were later integrated into the **optimised team solution**.

---
