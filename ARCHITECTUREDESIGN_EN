# Architecture Design — Project Eon

> Project Eon’s Client-Server Architecture document.
> Defines **responsibilities, workflows, and technical decisions** for the MVP and future expansions.

---

## Architecture Objectives

The Project Eon architecture was designed to:

- Support a 2D online MMORPG.
- Ensure reliable and secure progression.
- Prevent cheats and inconsistencies.
- Allow for future expansion without a complete rewrite.

The initial focus is to **validate the architecture during the MVP**, not to scale massively.

---

## Core Principle — Authoritative Server

The **server is the sole source of truth**.

This means:
- The client never decides critical outcomes.
- All progression is validated on the server.
- Critical states are calculated server-side.

The client only:
- Sends intentions (input).
- Renders states.
- Displays visual feedback.

---

## Client (GameMaker Studio 2)

### Responsibilities

- Capture player input.
- Send intentions to the server.
- Render the game world.
- Display UI and visual feedback.
- Play animations.

### What the Client Does NOT Do

- Calculate final damage.
- Update XP or skills.
- Validate crafting or combat.
- Persist data.

The client must always assume that the server can **correct or deny** an action.

---

## Server (Node.js)

### Responsibilities

- Manage connections.
- Maintain the true game state.
- Validate movement.
- Process combat logic.
- Process crafting and orders.
- Calculate XP and skills.
- Persist data.

All logic that alters the world **lives on the server**.

---

## Communication

### Protocol

- WebSockets.
- JSON-based messaging.

### Message Types (MVP)

#### Client → Server

- `login`
- `move`
- `attack`
- `gather`
- `deliver_order`

#### Server → Client

- `state_update`
- `combat_result`
- `xp_update`
- `skill_update`
- `error`

---

## Player State (Server)

Each connected player has a state persisted on the server:

- ID.
- Position.
- HP (Health Points).
- Level.
- XP.
- Combat Skills.
- Crafting Skills.
- Gold.
- Current state (idle, combat, gathering).

The client merely **mirrors** this information.

---

## World and Entities

### MVP

- Single map.
- Simple entities:
  - Players.
  - Creatures.
  - Gatherable resources.
  - NPCs.

### Future

The architecture allows for:
- Multiple maps.
- Instancing.
- Danger zones.

Without requiring structural refactoring.

---

## Combat

- Fully validated on the server.
- Client sends only the intent to attack.
- Server:
  - Validates range.
  - Calculates damage.
  - Updates HP.
  - Updates XP and skills.

The client only receives the final result.

---

## Crafting and Orders

- Harvesting is validated on the server.
- Orders are controlled by the server.
- Delivering orders grants Character XP and Gold.
- Crafting grants Profession XP.

No progression logic occurs on the client side.

---

## Persistence

### Persisted Data

- Character progress.
- Skills.
- Gold.
- Base state.

### Persistence Triggers

- Logout.
- Regular intervals (Auto-save).
- Critical events (Level up).

Initial format is simple (JSON), with the possibility of migrating to a database in the future.

---

## Synchronization

### Movement

- Client sends movement intentions.
- Server validates and corrects position when necessary.

### Combat and Skills

- Always server-side.
- No client-side prediction in the MVP.

---

## Scalability (Planned)

Not implemented in the MVP, but anticipated:

- Logical separation by maps.
- Sharding capabilities.
- Dedicated regional servers.

The current architecture does not block these expansions.

---

## Out of MVP Scope

- Load balancing.
- Advanced anti-cheat.
- Data migration tools.
- Automated cloud scaling.

---

## Final Note

This document defines the **technical foundation of Project Eon**.

From this architecture, the project can grow incrementally, maintaining consistency, security, and clarity for the entire team.
