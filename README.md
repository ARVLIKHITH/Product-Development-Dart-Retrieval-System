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
- Return darts to the player without requiring posture change.  
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
- Clarified the assigned task (“Retrieve darts automatically and return to the player”).  
- Conducted **extensive research**:  
  - State-of-the-art systems (e.g., ball return machines, arcade retrieval systems).  
  - Technical analogies (gravity chutes, vending dispensers, magnetic release systems).  
  - Market gap analysis → no comparable dart retrieval system exists.  
- Developed a **List of Requirements (LoR):**  
  - Fixed Demands: safe dart retrieval, return without posture change, budget <€200, emergency stop, simple maintenance.  
  - Wishes: ergonomic design, low noise, compact footprint.  
- **My Contribution:** Performed **extensive research** and prepared my **own LoR**, which was later merged into the team’s consolidated LoR.

---

### Step 3: Design Methodology
- **Black Box:** Defined the system’s overall function (inputs → transformation → outputs).  
- **Subfunctions (SF):** Identified critical subfunctions (trigger, extract, guide, transport, feedback, safety).  
- **Active Principles:** Each member proposed individual physical/technical solution principles for the subfunctions.  
- **Morphological Box (MB):** Combined all individual principles into a team Morph Box to visualize solution space.  
- **My Contribution:**  
  - Worked with the team on **Black Box** and **Subfunctions**.  
  - Generated **individual active principles** (e.g., sudden fall, magnetic assist for extraction, gravity-based transport).  
  - Contributed to the **team Morphological Box** by integrating my proposed principles.

---

### Step 4: Concept Race (Variants)
- Each team member developed an **individual variant** by selecting solution principles from the Morphological Box.  
- Prepared concept documentation: sketches, function description, pros/cons, cost estimate, feasibility check.  
- Conducted a **Variant Assessment**:  
  - Weighted criteria derived from the LoR.  
  - Technical/economic evaluation (paired comparison, strength diagrams).  
- **My Contribution:**  
  - Designed my **own variant** — combining a **sudden fall mechanism** with a **magnetic backup plate**, plus funnel and chute return.  
  - This was my **highlight contribution**, and I will document it separately in [`/concept_race`](./concept_race/README.md).

---

### Step 5: Optimal Solution
- Selected and optimized the best variant by merging the strongest features of all concepts.  
- Implemented superior sub-solutions (e.g., magnetic assist from my concept, ergonomic funnel return from another).  
- Created detailed **3D CAD model (Fusion 360)**.  
- Integrated **Arduino + L293D motor driver** for control, with emergency stop and LED/buzzer.  
- **My Contribution:** Authored the **Optimized Solution Description**, consolidating all features into a clear narrative.

---

### Step 6: Additional Work Packages
- Prepared the following deliverables for the optimized solution:  
  - **Set-up structure** (modules, assemblies, parts).  
  - **FMEA** (failure mode and effects analysis).  
  - **Product Description (manual-style)** — description, setup, function, technical data, maintenance.  
  - Prototype model for demonstration.  
- **My Contribution:** Wrote the **Product Description** for the optimized solution, including structure, function, technical data, and maintenance guidelines.

---
## 🎥 Project Demo (Video)

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

