# Technical MVP - Project Eon

> This document defines the **initial technical MVP** for Project Eon.
> The goal of this MVP is to **validate the MMO architecture**, rather than delivering final content or visual polish.

---

## MVP Objectives

The technical MVP must prove that:

* Client and server communicate correctly.
* Character progression functions as intended.
* Skills evolve through usage.
* Crafting and combat coexist within the same gameplay loop.
* Data persistence is reliable.

If these points function correctly, the project is considered **technically viable**.

---

## Initial Stack

> Suggested initial stack - subject to adjustment by the team.

* **Client:** GameMaker Studio 2
* **Server:** Node.js
* **Communication:** WebSockets
* **Persistence:** JSON or a simple database

---

## Client (GameMaker Studio 2)

### Movement and Player State

* Basic 2D movement.
* Server synchronization:
  * Position
  * Direction
  * HP
  * Class (fixed for the MVP)

---

### Initial Class

* **Warrior** (the only class in the MVP).

**Rationale:**
* Simplicity.
* Validation of melee combat.

---

### Basic Combat

* 1 active skill: **Melee Attack**.
* Server-validated attacks.
* Simple damage calculation.

#### Progression

* Skill usage grants skill XP.
* Defeating creatures grants character XP.
* Skill level is capped by the character level.

---

## MVP World

* 1 small map.
* 1 safe zone.
* 1 danger zone.
* 1 type of hostile creature.

The focus is validation, not variety.

---

## Crafting (Minimum Scope)

### Available Profession

* **Mining**

### Workflow

1. Player collects ore.
2. Player receives 1 crafting order.
3. Player delivers the order.
4. Player receives:
   * Character XP
   * Gold

> Crafting only grants profession-specific XP.

---

## Order System (Simplified)

* Single order.
* Simple item.
* Fixed NPC.

The system exists only to validate the crafting loop.

---

## Server

### Mandatory Functionalities

* Simple login.
* Player sessions.
* Connection management.
* Position synchronization.
* Combat validation.
* XP and skill calculation.
* Basic order system.

---

## Data Persistence

Save on the server:

* Character level
* Character XP
* Combat skill
* Mining skill
* Gold

Persistence must occur during:
* Logout
* Regular intervals

---

## Full MVP Loop

1. Player enters the game.
2. Moves through the map.
3. Engages a creature.
4. Earns combat XP.
5. Evolves skill through usage.
6. Collects ore.
7. Delivers order.
8. Earns character XP + gold.
9. Data is saved.

---

## 🚫 Out of MVP Scope

* PvP
* Multiple classes
* Guild systems
* Advanced economy
* Final UI
* Balancing

---

## Development Estimate

> Considering a team of 3 people.

* Client base: 2–3 weeks
* Server base: 2–3 weeks
* Combat: 1 week
* Crafting: 1 week
* Persistence and testing: 1 week

**Total estimate:** ~6–8 weeks

---

## Final Note

This MVP represents the **technical foundation of Project Eon**.

Only after the validation of this MVP should the project expand into content, advanced systems, and visual polish.
