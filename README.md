# Dart Retrieval System – Product Development Project (SS25)

This repository documents the **Product Development Project (IBE4, SS25)** at **Technische Hochschule Würzburg-Schweinfurt (THWS)**.  
Our team of 5 students was tasked with designing and prototyping a **Dart Retrieval System** — a mechanism that extracts darts from the dartboard and returns them safely to the player.

---

## Introduction & Story

This project was developed as part of the **Product Development course (IBE4, SS25)** at THWS.  

In this course, students are grouped randomly into interdisciplinary teams and assigned an engineering challenge.  
Our challenge: **develop a prototype Dart Retrieval System**.  

The mission:  
- Create a system that **retrieves darts automatically** after each throw and **returns them to the player** — all without requiring the player to move or change posture.  

---

## Project Story

- At the start, we were provided with strict **guidelines and a scriptum** outlining the entire development process.  
- We followed a structured methodology — from **task clarification and research**, to **List of Requirements (LoR)**, **function structures**, **morphological box**, and eventually the **Concept Race** where each team member designed an individual variant.  
- Using technical–economic assessment, we evaluated the variants and merged the strongest features to design an **optimised solution**.  
- The optimized design was modeled in **Fusion 360** and integrated with an **Arduino + L293D motor driver** for electronic control.  
- Across 10 weeks, we documented every step: Gantt chart, LoR, Morph Box, variant assessment, optimised solution description, and **final product manual**.  

The result:  
A **working prototype** backed by complete documentation and a **Blender animation** **CAD Model** showcasing the final design.  

---

## Project Objectives
- Retrieve darts automatically from the board.  
- Return darts to the player without requiring a posture change.  
- Ensure safe, reliable, and low-cost operation.  
- Apply structured **product development methodology** from task clarification to prototype.

## Goal of the Project

While the technical task was to design a **Dart Retrieval System**,  
The true objective of this course project was to **demonstrate how a structured product development methodology leads to better, optimised solutions**.

By following the official guideline and scriptum step by step —  
from **task clarification and research**, to **List of Requirements (LoR)**,  
then through **Black Box, Subfunctions, Morphological Box, Concept Race, and technical–economic assessment** —  
We showed how systematic design methods can transform a rough idea into a validated, optimised prototype.

## 📐 Development Process (Guideline-Based)

The Product Development Project followed the official **six-step methodology**.  
Below is the process we applied, with my **individual contributions** highlighted.

---

### Step 1: Organisation & Project Management
- Established project framework via **Project Agreement**.  
- Assigned responsibilities using an RSI-matrix.  
- Defined milestones and weekly Quality Gates (QG01–QG06).
    
---
**My Contribution:** Created the **Gantt Chart** (10-week project timeline with milestones and supervised meetings).

- **Gantt Chart Design** – Created from scratch in **ProjectLibre**.  
- Defined project timeline (March 24 – June 5, 2025) with all major phases:
  - Project kickoff & organisation  
  - Task clarification, research, LoR  
  - Design methodology (Black Box, Subfunctions, Morphological Box)  
  - Concept Race (variants) & assessment  
  - Optimised solution (CAD, proofs, description)  
  - Additional work packages (FMEA, product manual, prototype)  
  - Final presentation  
- Established **weekly Quality Gates (QG0–QG6)** and milestones.  
- Scheduled both **supervised meetings with professor** and **unsupervised team meetings**.  
- Aligned individual submissions (e.g., research, LoR, active principles, variant) with deadlines to ensure smooth consolidation into team deliverables.  


---

### Step 2: Task Clarification, Research & List of Requirements (LoR)

#### What is “Extensive Research & LoR”?
In the Product Development methodology, this step ensures that the design process is grounded in facts and realistic constraints.  
- **Extensive Research** involves studying existing solutions, market gaps, technical analogies, and user needs.  
- The **List of Requirements (LoR)** then translates this research into a structured set of *demands* (must-haves) and *wishes* (nice-to-haves) that guide all later design phases.  
This step prevents “random designing” and ensures the final product is optimized, safe, and manufacturable.

---

#### My Contributions
- **Task Clarification:** Defined the challenge as *“Retrieve darts automatically and return them to the player without requiring posture change.”*  
- **Extensive Research Conducted:**  
  - Studied state-of-the-art systems (ball return machines, arcade retrieval systems, vending dispensers, magnetic release mechanisms).  
  - Performed a **market analysis** → identified user groups (pro players, clubs, accessibility users, premium hobbyists) and estimated ~300 units/year potential sales.  
  - Analysed **existing dart-related products** (*Scolia*, *FIDODARTS*, TU Wien demonstrator) and identified that no true dart retrieval system currently exists.  
  - Proposed a feasible **concept idea**: hybrid system with pressure sensor film detection, sudden fall release, magnetic assist, and ramp return.  
- **List of Requirements (LoR) Authored:**  
  - **Geometry:** Regulation dartboard diameter 451 mm, thickness 38–45 mm, weight 4.5–5.5 kg.  
  - **Kinematics:** Ramp tilt 10–45°, retrieval ≤ 15 s for 3 darts, board must remain stationary during throws.  
  - **Forces:** Dart removal < 0.8 N, electromagnet holding force 5–10 kgf.  
  - **Energy:** Arduino + Li-ion supply, electromagnet pulse duration ~2 sec, servo motors at 5 V regulated.  
  - **Safety:** No injury risk (rounded edges ≥ 3 mm), CE conformity, emergency stop ≤ 300 mm reach, overheat protection for electromagnets.  
  - **Ergonomics:** Usable without changing stance, wheelchair accessible (tray/button height 60–120 cm), noise level ≤ 50 dB.  
  - **Production:** Designed for small-batch manufacturing (300–500 units/year).  
  - **Costs:** Max production cost ≤ €200.  
- **Deliverables:** Submitted my **research document** and **LoR**, which were merged into the team’s consolidated requirement list and used as the foundation for design.  

📄 **Files:**  
- [Extensive Technical Research (PDF)](../docs/Extensive_Research.pdf)  
- [List of Requirements (PDF)](../docs/LOR.pdf)

---
### Step 3: Design Methodology (Black Box, Subfunctions, Morphological Box)

#### What is this step?
In the product development methodology, after task clarification and LoR, the system must be broken down into functions and solution principles:  
- **Black Box (BB):** Represents the system as a whole (inputs → transformation → outputs) without detailing the internals.  
- **Subfunctions:** Break down the system into smaller logical operations (detect, extract, transport, return, safety).  
- **Morphological Box (MB):** A structured matrix listing multiple possible solution principles for each subfunction, enabling systematic variant generation.  
- **Creativity Techniques:** Brainstorming, analogies, bionics, and systematic variation were applied to maximise solution diversity.

---

#### My Contributions
- **Black Box Development:**  
  - Contributed to defining the system’s Black Box for both *dart retrieval* and *dart return*.  
  - Identified **inputs** (material = darts, signal = button press, energy = electric/mechanical), **outputs** (darts in tray, audio/visual feedback), **internal disturbances** (misalignment, jamming, vibrations), and **external disturbances** (power fluctuations, dust, temperature, pets).  
  - Helped set **system boundaries** (only retrieves darts from the board, not portable, limited by tray capacity).

<p align="center">
  <img src="https://github.com/user-attachments/assets/98a0e966-258a-4961-a0d1-75e403e702f4" alt="Screenshot 4" width="500"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/b0d9d11e-92ae-4b7d-a6e6-917d4bcca836" alt="Screenshot 5" width="400"/>
</p>

- **Subfunctions & Function Structures:**  
  - Worked on both **hierarchical** and **dynamic function structures**:  
    - SF1 – Detect user input (button/pedal)  
    - SF2 – Process input signal (Arduino, debounce circuit)  
    - SF3 – Activate extraction mechanism (servo hinge, gravity tilt, magnet)  
    - SF4 – Place darts in return tray (funnel, ramp, slide)  
    - SF5 – Prevent bounce & ensure safe return  
    - SF6 – Load darts in pickup tray  
    - SF7 – Provide user feedback (LED/buzzer)  
    - SF8 – Safety (emergency stop)  
  - Created diagrams to connect subfunctions (hierarchical and dynamic view) logically.

<p align="center">
  <img src="https://github.com/user-attachments/assets/df1b679e-e347-43b9-a0ae-19d451bcbfe2" alt="Screenshot 1" width="400"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/c65e9fda-2b14-40ad-9866-c25894a2527e" alt="Screenshot 2" width="350"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/2e51e6e0-7f37-4282-920a-121ed01bc578" alt="Screenshot 3" width="500"/>
</p>

- **Active Principles & Morphological Box:**  
  - Generated **individual active principles** for subfunctions (gravity tilt, magnetic assist, funnel loader, Arduino-based logic, emergency stop relay).  
  - Integrated my ideas into the **team Morphological Box**, ensuring broad coverage of possible technical solutions.  
  - Example MB entries:  
    - **Trigger:** Button, pedal, IR sensor  
    - **Extraction:** Gravity tilt, servo, magnetic pull  
    - **Transport:** Ramp, chute, conveyor  
    - **Feedback:** LED, buzzer, RGB indicator  
    - **Safety:** Emergency stop, power cut relay  
  - This MB was the foundation for the **Concept Race**, where each member created an individual variant.

---
**File:** [Active Principles & Morphological Box (PDF)]

---

### Step 4: Concept Race (Variants)
- Each team member developed an **individual variant** by selecting solution principles from the Morphological Box.  
- Prepared concept documentation: sketches, function description, pros/cons, cost estimate, feasibility check.  
- Conducted a **Variant Assessment**:  
  - Weighted criteria derived from the LoR.  
  - Technical/economic evaluation (paired comparison, strength diagrams).  
- **My Contribution:**  
  - Designed my **own variant** — combining a **sudden fall mechanism** with a **magnetic backup plate**, plus funnel and chute return.  
  - This was my **highlight contribution**, and I have documented it separately in [`/concept_race`](./concept_race/README.md).


#### What is this step?
In the product development methodology, once multiple concepts (variants) are generated from the Morphological Box, they are systematically evaluated.  
- Each **team member develops one variant**.  
- All variants are then compared using **technical and economic weighting criteria**, often with a **paired comparison** or **weighted scoring method**.  
- The goal is to identify the **optimal concept** for further development.

---

#### My Contributions
- **Individual Variant:**  
  - Developed my own variant (**DartXtract**) by selecting the most promising principles from the Morphological Box:  
    - Extraction → Sudden fall mechanism with magnetic backup.  
    - Transport → Funnel + chute return.  
    - Feedback → LED + buzzer.  
    - Safety → Emergency stop.  
  - Documented initial situation, function, sketches, pros/cons, and feasibility.  
  - My variant was included in the **Concept Race** and compared against four others from teammates.

- **Variant Assessment:**  
  - Participated in creating the **technical and economic criteria weighting** tables.  
  - Contributed weight factors (WF) for critical requirements such as retrieval time, bounce prevention, alignment accuracy, and safety.  
  - Helped normalise scores and calculate **percentage fulfilment** for each variant.  

- **Results:**  
  - **Technical Criteria Ranking:**  
    - My variant (DartXtract) → 54.7% fulfilment.  
      
  - **Economic Criteria Ranking:**  
    - My variant (DartXtract) → 51.6%.  
---

**Visual Deliverables:** 
<p align="center">
  <img src="https://github.com/user-attachments/assets/0822006c-0ed7-4e0b-a855-d30164b61882" alt="Optimized Solution 1" width="450"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/d49aaf86-760b-411e-85d2-afb85e65d68a" alt="Optimized Solution 2" width="450"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/8b5bba8c-c49e-4b73-bd42-f52af52c4aad" alt="Optimized Solution 3" width="450"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/73b19571-cac7-4bf2-973c-b801eaeafa3b" alt="Optimized Solution 4" width="450"/>
  <br><br>
  <img src="https://github.com/user-attachments/assets/a44c5c5f-d9a7-4e7c-abd5-8e042b113c70" alt="Optimized Solution 5" width="350"/>
</p>

### Step 5: Optimal Solution
- Selected and optimised the best variant by merging the strongest features of all concepts.  
- Implemented superior sub-solutions (e.g., magnetic assist from my concept, ergonomic funnel return from another).  
- Created detailed **3D CAD model (Fusion 360)**.  
- Integrated **Arduino + L293D motor driver** for control, with emergency stop and LED/buzzer.  
- **My Contribution:** Authored the **Optimized Solution Description**, consolidating all features into a clear narrative.
<p align="center">
  <img src="https://github.com/user-attachments/assets/0634574b-b038-49e5-971a-24db24cb6488" alt="Screenshot" width="450"/>
</p>
---

### Step 6: Additional Work Packages
- Prepared the following deliverables for the optimised solution:  
  - **Set-up structure** (modules, assemblies, parts).  
  - **FMEA** (failure mode and effects analysis).  
  - **Product Description (manual-style)** — description, setup, function, technical data, maintenance.  
  - Prototype model for demonstration.  
- **My Contribution:** Wrote the **Product Description** for the optimised solution, including structure, function, technical data, and maintenance guidelines.

---
## Project Demo (Video)

<p align="center">
  <a href="https://www.youtube.com/watch?v=b0rMb7xxSCo">
    <img src="https://img.youtube.com/vi/b0rMb7xxSCo/0.jpg" alt="Dart Retrieval System Demo" width="600">
  </a>
</p>

<p align="center"><em>Credits: Blender animation by Prithvi, based on our team’s final prototype design.</em></p>

5. **Prototype & Documentation**  
   - Built physical prototype with extraction, return, and safety features.  
   - Authored **Product Description (manual-style)** covering setup, function, technical data, and maintenance.  
   - Delivered final presentation and project folder.  

---

## System Features
- Automated dart extraction mechanism (motor-driven + funnel return system).  
- Guided tray for safe dart delivery.  
- Electronic control (Arduino) with emergency stop.  
- Visual/audio feedback during operation.  
- Low-cost prototype (budget €200).  

---

## Team & Roles
- **Likhith Anand** – Project scheduling (Gantt), Extensive research, LoR, Active Principles, Subfunctions, Morphological Box, Brainstorm Techniques, concept race variant, optimised solution description, product description.  

---

