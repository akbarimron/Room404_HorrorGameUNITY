# 🚪 Room 404 — Survival Horror Game (OOP Project)

![Unity](https://img.shields.io/badge/Unity-2022.3+-black?style=for-the-badge&logo=unity)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Course](https://img.shields.io/badge/Project-Object--Oriented%20Programming-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> **Room 404** is a 3D *First-Person Survival Horror* game developed using Unity Engine and C#. This project was created as a final term project for the **Object-Oriented Programming (OOP)** course, focusing on clean architecture, modular game mechanics, and core OOP principles.

---

## 📖 Synopsis & Setting

You wake up stranded inside an eerie, abandoned 4-story boarding house (*kos-kosan*). Dim corridors, unsettling silence, and a freezing aura permeate every corner. A restless entity roams the hallways, waiting for any sign of panic.

To escape alive, you must explore all 4 floors, collect **3 cursed dolls**, and reach the exit door safely before the haunting entity catches you.

---

## 🎮 Core Gameplay Mechanics

| Mechanic | Description |
| :--- | :--- |
| 🏃 **Movement & Stamina** | Players can walk silently or sprint. Sprinting quickly drains stamina and creates loud footstep sounds that alert nearby threats. |
| 👻 **Dynamic Enemy AI** | The ghost utilizes sound and movement detection:<br>• **Passive / Patrol Mode**: Ignores the player while they walk or crouch normally.<br>• **Chase Mode**: The ghost detects sprinting footsteps and immediately initiates a high-speed pursuit! |
| 🚪 **Hiding Spots (Lockers)** | Players can hide inside lockers to break line-of-sight and shake off the pursuing ghost. |
| 🎒 **Inventory & Consumables** | An inventory system allows players to collect and consume items to replenish stamina during critical escape moments. |
| 🧸 **Objective-Driven Escape** | Locate all **3 hidden dolls** across the building, then unlock and reach the exit door to win. |

---

## 🏢 Level Structure (4 Floors)

- **Floor 1**: Reception area, main exit gate (locked), and introductory corridors.
- **Floor 2**: Standard residential rooms, narrow hallways, and early hiding spots.
- **Floor 3**: Low-visibility layout with maze-like sections and consumable stamina items.
- **Floor 4**: The attic / top floor with the most aggressive enemy presence where the final clues and doll reside.

---

## ⌨️ Controls

| Key / Input | Action |
| :---: | :--- |
| `W` `A` `S` `D` | Character Movement |
| `Mouse` | Look around (First-person camera) |
| `Left Shift` | Sprint (Consumes stamina; triggers ghost chase) |
| `E` | Interact (Open doors, hide in lockers, pick up items/dolls) |
| `Tab` / `I` | Open / Close Inventory |
| `Esc` | Pause Menu |

---

## 🧱 OOP Architecture & Implementation

This game was engineered to showcase core **Object-Oriented Programming (OOP)** paradigms in Unity:

1. **Encapsulation**:
   - Vital player stats (`currentStamina`, `health`, `movementState`) and AI properties are kept `private` / `protected`, exposed only via safe properties and getter/setter methods.
2. **Inheritance**:
   - Interactive world entities inherit from an abstract `InteractableObject` base class (e.g., `Locker`, `Door`, `DollItem`).
   - Collectibles derive from a shared `ItemBase` class.
3. **Polymorphism**:
   - `Interact()` methods are marked `virtual` and overridden across different interactable objects, allowing custom interaction behavior while sharing a unified caller interface.
4. **Abstraction & Interfaces**:
   - Buffer & command execution separation (`IBaseCommandBuffer`, `IComputeCommandBuffer`, `IRasterCommandBuffer`).
   - Modular Finite State Machine (FSM) managing enemy behaviors (`PatrolState`, `ChaseState`, `SearchState`).

---

## 🛠️ Tech Stack & Tools

- **Engine**: Unity Engine (Built-in RP / Universal Render Pipeline)
- **Language**: C# (.NET)
- **IDE**: Visual Studio / Visual Studio Code / JetBrains Rider
- **Version Control**: Git & GitHub

---

## 👥 Authors & Contributors

- **Muhamad Akbar Imron** ([@akbarimron](https://github.com/akbarimron))
- **Ryan Yanuar Pradana** ([@Rynr615](https://github.com/Rynr615))

---

## 📦 Getting Started & Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/akbarimron/Room404_PBO.git
