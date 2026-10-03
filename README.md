# Discrete MOSFET Audio Amplifier

> **Course:** Electronic Devices (TEC Weeks 9–15)  
> **Institution:** Costa Rica Institute of Technology (TEC)  
> **Technology:** Discrete MOSFET Transistors  
> **Construction Type:** Breadboard Prototype  

## 📋 Table of Contents

* [Project Overview](#-project-overview)
* [Key Specifications & Requirements](#-key-specifications--requirements)
* [Work Plan & Strategy](#-work-plan--strategy)
* [Team Roles & Responsibilities](#-team-roles--responsibilities)
* [Team Working Rules](#-team-working-rules)
* [Project Timeline & Schedule](#-project-timeline--schedule)
* [Five-MOSFET Control Matrix](#-five-mosfet-control-matrix)
* [Preliminary Component List & Budget](#-preliminary-component-list--budget)
* [Key Milestones](#-key-milestones)

---

## 🔊 Project Overview

This repository contains the complete development, organization, and verification plan for a **Discrete Audio Amplifier** designed and built using **5 MOSFET transistors** on a breadboard.

The main goal is to design, simulate, construct, integrate, and experimentally verify a functional audio amplifier that reproduces audio signals clearly with proper amplification stages.

---

## ⚙️ Key Specifications & Requirements

* **Power Supply:** Dual symmetric $\pm12\text{ V}$ power supply.
* **Active Devices:** Exactly 5 discrete MOSFET transistors (topology & device functions must be technically justified).
* **Output Load:** Loudspeaker matching project specifications.
* **Prototyping Medium:** Breadboard construction.
* **Validation Criteria:**
  * Audio signal reproduction and audibility tests.
  * Experimental verification (gain, clipping, frequency response, temperature, and noise).
  * Documentation of all components and datasheets.

---

## 🎯 Work Plan & Strategy

The internal design cycle follows a standard structured sequence:

$$\text{Requirements} \longrightarrow \text{Design} \longrightarrow \text{Simulation} \longrightarrow \text{Construction} \longrightarrow \text{Integration} \longrightarrow \text{Testing} \longrightarrow \text{Delivery}$$

* **Target Goal:** Obtain a fully functional amplifier prototype by **Project Week 5 (TEC Week 13)**.
* **Final Polish:** Weeks 6 & 7 focus on validation, bug fixes, thermal/electrical testing, documentation, and the final presentation.

---

## 👥 Team Roles & Responsibilities

| Role | Responsibility |
| ----- | ----- |
| **Leader** | Project planning, task distribution, weekly progress tracking, purchasing coordination, results review, team integration, and client communication. |
| **Developer 1** | Audio input, volume control, signal conditioning, and compatibility with the audio source. |
| **Developer 2** | Preamplification, voltage amplification, driver stage, biasing, and MOSFET analysis. |
| **Developer 3** | Power stage, $\pm12\text{ V}$ power distribution, loudspeaker load, output current handling, thermal dissipation, and heat sink management. |
| **Verifier** | Test plan execution, independent measurements, simulation vs. practical measurement comparisons, datasheet review, and requirement verification. |

---

## 📜 Team Working Rules

1. Every member is strictly responsible for completing their assigned weekly tasks.
2. Blockers must be communicated immediately to the team to find a solution before the next meeting.
3. **Modular Testing:** Each developer must test their block independently before system integration.
4. Focus on continuous, functional progress over unnecessary documentation.
5. Issues found during physical construction must be resolved in the originating stage before altering other blocks.
6. **Integration Rule:** Unstable or non-functional stages will **not** be integrated into the main circuit.
7. Any critical circuit modification must be communicated to the entire team to maintain version control.
8. Each client meeting should demonstrate functional progress relative to the previous week.

---

## 📅 Project Timeline & Schedule

### 🔹 Week 1 (TEC W9) — Definition & Requirements
* **Leader/Team:** Define project requirements, block diagrams, client questions, and organize shared repository.
* **Dev 1:** Research audio source, input level, connectors, volume control, and signal conditioning.
* **Dev 2:** Research MOSFET voltage amplification topologies, preamplifier structure, and device allocation.
* **Dev 3:** Research power stage, $\pm12\text{ V}$ limits, load current, thermal dissipation, and breadboard constraints.
* **Verifier:** Create preliminary test plan (voltage, gain, power, frequency, clipping, temperature, audibility).
* **Deliverables:** Block diagram, preliminary architecture, MOSFET research, task distribution, test plan.

### 🔹 Week 2 (TEC W10) — Design & Simulation
* **Leader:** Interface check between blocks, coordinate purchase list, verify 5-MOSFET requirement.
* **Dev 1:** Simulate input stage, volume control, and input/output signal integrity.
* **Dev 2:** Simulate preamplifier and driver stages; establish DC operating points ($Q$-points).
* **Dev 3:** Simulate power stage (output current, thermal dissipation, load power).
* **Verifier:** Independent simulation review, theoretical values table.
* **Deliverables:** Full schematic, functional simulations, preliminary 5-MOSFET matrix, component list.

### 🔹 Week 3 (TEC W11) — Modular Construction
* **Dev 1:** Build & test input + volume control block on breadboard.
* **Dev 2:** Build & test preamplifier + driver stages; measure DC biasing and gain vs. simulation.
* **Dev 3 & Verifier:** Build power stage, verify power wiring, perform small-signal tests, measure thermal behavior and DC voltages.
* **Completion Criterion:** A stage is tagged `READY FOR INTEGRATION` only when operating stably on its own.

### 🔹 Week 4 (TEC W12) — Integration
* **Integration Sequence:** $\text{Input} \rightarrow \text{Preamplifier} \rightarrow \text{Driver} \rightarrow \text{Power Stage} \rightarrow \text{Loudspeaker}$
* **Leader:** Fault tracking list and problem assignments.
* **Dev 1–3:** Progressive module integration, solving inter-stage loading, saturation, clipping, or bias shift issues.
* **Verifier:** Measure total system gain, power supply draw, noise floor, distortion, and temperatures.
* **Deliverables:** First live demonstration of complete audio playback.

### 🔹 Week 5 (TEC W13) — Testing & Refinement
* **Primary Goal:** Achieve full circuit functionality.
* **Testing Checklist:**
  1. Power supply limits ($\pm12\text{ V}$)
  2. DC Biasing points
  3. Voltage & Power Gain
  4. Max output power
  5. Clipping thresholds
  6. Frequency response ($100\text{ Hz}$ to $10\text{ kHz}$)
  7. Noise floor
  8. Thermal stability
  9. Audio reproduction & clarity
* **Deliverables:** Corrected schematic, test results comparison, updated compliance matrix.

### 🔹 Week 6 (TEC W14) — Final Validation
* Final adjustments to wiring, signal quality, and stability.
* Verification of test repeatability across all criteria.
* **Acceptance Matrix Review:**
  * [ ] $\pm12\text{ V}$ Dual Power Supply
  * [ ] 5 Justified MOSFETs
  * [ ] Target Gain & Power
  * [ ] Frequency Response
  * [ ] Thermal & Audio Stability
  * [ ] Clean Breadboard Wiring

### 🔹 Week 7 (TEC W15) — Presentation & Closing
* Final documentation polish.
* Complete system presentation and live demonstration.
* Final deliverable submission: Working breadboard prototype, complete report, measurement logs, datasheets, and presentation slides.

---

## 🎛️ Five-MOSFET Control Matrix

Each MOSFET transistor must perform a technically justified role within the system architecture.

| ID | Transistor Model | Stage / Module | Technical Justification & Function |
| ----- | ----- | ----- | ----- |
| **Q1** | *TBD* | Preamplifier | Signal preamplification / low-noise input stage |
| **Q2** | *TBD* | Voltage Amplifier | Main voltage amplification stage |
| **Q3** | *TBD* | Driver / Phase Splitter | Driver stage for power section |
| **Q4** | *TBD* | Output Power Stage | High side / Push-pull output stage |
| **Q5** | *TBD* | Output Power Stage | Low side / Push-pull output stage |

---

## 🛒 Preliminary Component List & Budget

> **Currency:** Costa Rican Colón ($\text{CRC} / \text{₡}$)

| Component | Qty | Estimated Unit Price | Estimated Subtotal | Intended Use |
| ----- | ----- | ----- | ----- | ----- |
| **MOSFET Transistors** | 5 | TBD | TBD | Amplification & power output stages |
| **Large Breadboards** | 2–3 | $\sim\text{₡}5,900$ | $\text{₡}11,800 - \text{₡}17,700$ | Circuit construction |
| **Resistors (Assorted)** | Various | - | $\text{₡}1,500 - \text{₡}3,000$ | Biasing, feedback, gain control |
| $10\ \mu\text{F}$ **Capacitors** | 4 | $\sim\text{₡}89$ | $\sim\text{₡}356$ | AC coupling & filtering |
| $100\ \mu\text{F}$ **Capacitors** | 4 | $\sim\text{₡}199$ | $\sim\text{₡}796$ | Filtering & decoupling |
| $470\ \mu\text{F}$ **Capacitors** | 2 | $\sim\text{₡}295$ | $\sim\text{₡}590$ | Power filtering |
| $2200\ \mu\text{F}$ **Capacitors** | 2 | $\sim\text{₡}520$ | $\sim\text{₡}1,040$ | Main power supply filtering |
| $0.1\ \mu\text{F}$ **Capacitors** | 6 | $\sim\text{₡}110$ | $\sim\text{₡}660$ | High-frequency decoupling |
| **Potentiometers** | 1–2 | TBD | $\text{₡}500 - \text{₡}1,500$ | Volume & gain adjustment |
| **Heat Sinks** | As needed | $\sim\text{₡}420$ | TBD | MOSFET thermal management |
| **Jumper Wire Kit** | 1 set | TBD | $\text{₡}1,500 - \text{₡}3,000$ | Prototyping interconnections |
| **Audio Connectors** | As needed | TBD | TBD | Audio source input jack/terminal |
| **Loudspeaker** | 1 | TBD | TBD | Output load |
| $\pm12\text{ V}$ **Power Supply** | 1 | TBD | TBD | Dual DC supply |

*Note: Final costs for MOSFETs, loudspeaker, and power supply will be updated once device models are finalized in Week 2.*

---

## 🚩 Key Milestones

```text
[TEC W9]  Milestone 1: Requirements & System Architecture Defined
   │
[TEC W10] Milestone 2: Complete Circuit Simulation & MOSFET Selection
   │
[TEC W11] Milestone 3: Individual Modules Constructed & Tested on Breadboard
   │
[TEC W12] Milestone 4: First Complete Integrated Audio Playback
   │
[TEC W13] Milestone 5: Fully Functional Prototype & Complete Testing
   │
[TEC W14] Milestone 6: Final Validation & Documentation Completed
   │
[TEC W15] Milestone 7: Final Presentation & Project Delivery