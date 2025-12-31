#  ROADMAP — **Project Eon**

> ⚠️ **Important Notice**
> The durations listed below are **estimates** based on a small team capacity. 
> This roadmap serves to provide **technical direction and priority**, not to impose rigid deadlines.

---

## Overview

**Project Eon** is a 2D medieval fantasy MMO focused on **meaningful progression**, where **combat and crafting carry equal weight** in character development.

Development follows an incremental approach, ensuring each phase delivers a **playable and validatable** build, minimizing rework and scope creep.

---

## Roadmap Structure

* Development organized into independent phases.
* Each phase has clear, defined deliverables.
* No fixed dates or launch promises.
* Scope remains flexible based on the team's technical decisions.

---

##  PHASE 0 - Preparation & Alignment

**Estimated Duration:** 2–3 weeks

### Objective
Establish a solid technical and organizational foundation before starting gameplay development. Focus on team synchronization and workflow.

### Deliverables
* Organized GitHub repository.
* README (Project pitch and documentation).
* Initial architecture definition.
* Basic folder structure (Client & Server separation).
* Coding conventions and style guides.
* Initial Tech Stack:
  * **Client:** GameMaker Studio 2
  * **Server:** Node.js

📌 *No gameplay features are implemented during this phase.*

---

##  PHASE 1 - Online Technical MVP

**Estimated Duration:** 6–8 weeks

### Objective
Validate the project's multiplayer foundation.

### Features
* Client ↔ Server handshake/connection.
* Simple Login (Temporary Guest ID).
* Player spawning system.
* Synchronized movement (Interpolation/Prediction basics).
* Networked player visibility (Entities).
* Graceful disconnection handling.

### Expected Result
Players can connect and move together within the same map instance.

📌 *This is Project Eon's first major technical milestone.*

---

##  PHASE 2 - Basic Online Combat

**Estimated Duration:** 6–8 weeks

### Objective
Introduce active gameplay and world interaction.

### Features
* Health/Vitality system.
* Basic attack mechanics.
* Server-authoritative AI (Creatures).
* Server-side damage calculation.
* Death and respawn logic.

### Expected Result
Players can engage in cooperative combat against AI entities.

---

##  PHASE 3 - Inventory & Items

**Estimated Duration:** 4–6 weeks

### Objective
Build the framework for progression, crafting, and the in-game economy.

### Features
* Persistent inventory system.
* Item Classifications:
  * Resources
  * Equipment
  * Consumables
* Loot/Drop system.
* Data persistence (Saving progress).

### Expected Result
Players can accumulate and save persistent progress.

---

##  PHASE 4 - Crafting System

**Estimated Duration:** 6–8 weeks

### Objective
Ensure crafting is a first-class citizen in character progression, equivalent to combat.

### Features
* Initial crafting professions.
* Resource gathering/harvesting nodes.
* Recipe/Blueprint system.
* Crafting stations (Workbenches).
* Crafting-based XP gain.
* Viable progression path without mandatory combat.

### Expected Result
Players can progress and level up exclusively through crafting activities.

---

##  PHASE 5 - Character Progression

**Estimated Duration:** 6–8 weeks

### Objective
Unify combat and crafting into a cohesive, balanced progression system.

### Features
* Character leveling system.
* Experience (XP) sources:
  * Combat encounters.
  * Crafting and Gathering.
* Attribute/Stat points.
* Difficulty scaling.
* Balanced progression curve.

### Expected Result
A functional and satisfying core gameplay loop.

---

##  PHASE 6 - Content & Controlled Expansion

**Duration:** Ongoing

### Objective
Scale the game world without compromising stability.

### Potential Additions
* New map regions (Instancing).
* Expanded Bestiary (New creatures).
* Advanced Crafting recipes.
* Balance passes.
* Load testing and optimization.

### Expected Result
A stable, feature-complete Closed Beta version.

---

## Out of Initial Scope

* PvP (Player vs Player).
* Guild systems.
* Massive open world (Seamless).
* Advanced monetization systems.

These elements will be evaluated in the future, only after the core loop is validated.

---

## Final Considerations

This roadmap represents the **initial structured vision** for Project Eon. It is expected to evolve as the team grows, technical hurdles are cleared, and the project matures.

📌 The primary focus is to **build something playable, sustainable, and technically sound.**
