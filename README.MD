# 🏁 My Variant – DartXtract (Concept Race)

**Author:** Likhith Anand  
**Course:** Product Development (IBE4, SS25), THWS  
**Supervisor:** Prof. Dr. Thomas Felsner  

---

## 1. Starting Point
- **Assignment:** Retrieve darts automatically and return them to the player.  
- **Requirements considered:**  
  - Retrieve 3–7 darts per round without bending or posture change.  
  - Safe handling (no injury, no dart tip damage).  
  - Accessible for wheelchair users.  
  - Budget < €200 (prototype level).  
  - Compatible with steel-tip darts.  

---

## 2. Concept Overview (Mode of Operation)

### Detection & Trigger
- **Sensor:** Velostat pressure-sensitive film mounted behind dartboard.  
- **Logic:** Arduino Uno counts impacts, triggers retrieval after 3 darts.  
- **Protection:** Foam ring prevents compression, maintains sensitivity.  

### Control Logic
- Arduino processes sensor signal → triggers tilt, electromagnet, buzzer.  
- Outputs: Servo motor (tilt), Electromagnet (assist), Piezo buzzer (feedback).  

### Extraction Mechanism
- **Tilting Board:** Servo/gear motor tilts dartboard 90° → gravity releases darts.  
- **Electromagnet:** Mounted at 90° to board → 2s pulse → loosens stuck darts.  

### Return System
- Darts slide onto **angled ramp** → pass through **funnel guider** → collected in **slot-based foam tray**.  
- Foam padding at impact zones prevents bounce, noise, and damage.  
- Tray slots hold darts individually for safety and ergonomics.  

### Additional Features
- Adjustable ramp height/angle.  
- Audio feedback via buzzer.  
- Emergency stop (mushroom button) halts system instantly.  

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
- Slightly complex mechanical synchronization.  

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
  <img src="../images/tinkercad_circuit.png" alt="Tinkercad Circuit Diagram" width="500"/>
</p>

---

### 7.2 Arduino Code
The Arduino code handles sensor input, motor control, magnet activation, and feedback.  
You can view the complete code here:  

📄 [Arduino Code (DartXtract)](../code/dartxtract.ino)

---

### 7.3 Simulation Video
The working simulation was tested in **Tinkercad Circuits**.  
The video below demonstrates the retrieval cycle in action (sensor trigger → tilt → magnet → feedback).  

<p align="center">
  <a href="https://www.youtube.com/watch?v=YOUR_VIDEO_ID">
    <img src="https://img.youtube.com/vi/YOUR_VIDEO_ID/0.jpg" alt="DartXtract Simulation Video" width="500"/>
  </a>
</p>

*Click image to watch the full simulation on YouTube.*


## 8. Conclusion
The **DartXtract** variant demonstrates a **structured, feasible, and safe** dart retrieval system.  
- It retrieves darts automatically in under 15 seconds.  
- Accessible and ergonomic for all players.  
- Built from affordable, widely available components.  
- Minor refinements (sensor robustness, foam durability, magnet alternatives) would improve real-world reliability.  

This variant contributed core elements (magnetic assist + funnel return + safety systems) that were later integrated into the **optimized team solution**.

---
