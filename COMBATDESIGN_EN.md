# Combat System - Project Eon

> Combat System Design Document.
> Defines **classes, usage-based skill progression, and combat philosophy**; final balancing numbers are TBD.

---

## System Objectives

Combat in **Project Eon** is a core pillar of character development and functions **in tandem with the crafting system**.

The system is designed to:
- Support skill-based progression.
- Reward active skill usage.
- Encourage player cooperation.
- Integrate directly with the game's craft-driven economy.

---

## Core Philosophy

1. Combat grants **Character Experience (XP)**.
2. Combat skills evolve through **active battlefield use**.
3. Classes define a playstyle without strictly limiting overall growth.
4. Equipment has a direct impact on combat performance.
5. Cooperation between combatants and crafters is essential.

---

## Combat Classes

Players choose a base class at the beginning of their journey.

### Available Classes

- **Warrior**
  - Melee combat specialist.
  - Proficient with swords, axes, and spears.
  - High durability/tanking capabilities.

- **Mage**
  - Ranged magical combat.
  - Utilizes offensive and utility spells.
  - High damage output, low durability (Glass Cannon).

- **Healer**
  - Support and restoration focus.
  - Defensive and recovery magic.
  - Essential role for group content.

- **Archer**
  - Ranged physical combat.
  - Proficient with bows and crossbows.
  - High mobility and precision damage.

**Classes define:**
- Starting skill sets.
- Available aptitudes.
- General playstyle.

---

## Skills and Aptitudes

Each class features:
- Active abilities.
- Passive abilities.
- Class-specific combat aptitudes.

**Skills:**
- Are unlocked through progression.
- Level up through usage.
- Scale based on skill level, character level, or equipment.

---

## Combat Skill Progression

The combat system utilizes a **Usage-Based Progression** (Learn-by-doing) model.

### Core Concept

- Each combat type has a specific associated skill.
- Using a skill grants experience specifically to that skill.
- Skills level up independently of the overall Character Level.

> **Note:** A skill's maximum level is capped by the current Character Level.

---

### Example — Archer

- Character Level: 50.
- Ranged Combat Skill: Level 40 (35% XP).

**When attacking a creature:**
- The character earns overall Combat XP.
- The Ranged Combat skill receives specific XP.
- The skill progresses gradually through active use.

This progress is tracked separately from the character's general level experience.

---

## Skill Caps

- Every skill has its own level.
- **Maximum Skill Level = Character Level**.

**Example:**
- At Character Level 50:
  - Archery Skill: Max 50.
  - Sword Skill: Max 50.

**This system:**
- Ensures consistent progression.
- Prevents extreme specialization too early in the game.
- Maintains the value of the overall Character Level.

---

## Equipment and Crafting

Combat performance is heavily dictated by gear.

### Guidelines

- High-tier equipment offers a clear competitive advantage.
- Advanced gear is dependent on the crafting system.
- Combatants must rely on crafters to optimize their progression.

This creates a symbiotic relationship between **Combat Progression**, **Crafting Progression**, and **Player Cooperation**.

---

## Group Combat

Combat is designed to be most efficient when playing in a party.

### Natural Roles

- **Warrior:** Frontline / Tank.
- **Mage:** Area of Effect (AoE) damage.
- **Healer:** Support and survival.
- **Archer:** Ranged DPS and crowd control.

Specialized players are significantly more effective together than in isolation.

---

## Combat Loop

1. World exploration.
2. Creature encounter.
3. Active skill usage.
4. Character XP gain.
5. Evolution of the utilized skills.
6. Resource gathering or quest progression.

---

## Balancing Guidelines

- No class is entirely self-sufficient.
- Equipment quality is a major power differentiator.
- Consistent skill usage is directly rewarded.
- Group play is incentivized as the most efficient path.

---

## Out of Initial Scope

- Complex PvP systems.
- Extensive talent trees.
- Advanced combo mechanics.

These features may be evaluated for future updates.

---

## Final Note

Project Eon’s combat system is designed to be transparent, progressive, and cooperative. It is built to integrate seamlessly with crafting and character growth. Numerical details and final balancing will be tuned during the MVP development and internal testing phases.
