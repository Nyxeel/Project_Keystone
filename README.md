# Keystone – Server Concept (Work in Progress)

Keystone is a modular multiplayer server focused on citybuilding, player-driven economy,
controlled PvP, and long-term progression.
The goal is a server that regulates itself through systems rather than constant admin intervention.

---

## 1. Server Structure & Worlds

### 1.1 Keystone Hub (Main World / Citybuild)

- Persistent world (no reset)
- Central social and economic hub
- Players can claim land plots
- Building similar to a classic Citybuild server

**Plots**
- Size: 32×32 blocks
- Maximum of 4 plots per account
- Each plot has configurable flags:
  - PvP flag (on / off)
  - Teleport flag (on / off)
- Teleporting into a plot requires permission (owner or trusted player)

Plots can be used for:
- Housing
- Shops and businesses
- Player-designed games (e.g. parkour / jumping puzzles)

---

### 1.2 Farm Worlds (Weekly Reset)

#### PvE Farm World
- Resources, mobs, and vanilla loot
- All vanilla items can be brought back to the hub
- Primary purpose: supply the player economy

#### PvP Farm World
- PvP always enabled
- Additional ores and resources
- These resources add a **PvP damage reduction bonus** to existing equipment
- No new gear tiers; bonuses modify existing items

**PvP Bonus Rules**
- Applies only against player damage
- No effect in PvE
- Bonus degrades on PvP death

**Death in the PvP Farm World**
- Inventory items drop on the ground
- Weapons and armor are retained
- PvP bonus may be reduced or damaged

**Entry Protection**
- Time-based protection after entering the PvP farm world
- Protection ends:
  - after a short time period
  - when the player attacks another player
- While protected:
  - no PvP
  - no looting

---

### 1.3 Minigame Server

- Completely separated from hub and farm worlds
- No items or equipment carried over
- Independent progression system:
  - points
  - titles
  - ranks
- Rewards are cosmetic or social only (no power advantages)

---

## 2. Claim & Decay System (Core Mechanic)

### 2.1 Claim Crystal

Each plot contains a **Claim Crystal** as its central management object.

Properties:
- Visibly placed within the plot
- Cannot be broken while active
- Not tradeable
- Not automatable
- The only interface for managing the plot

The crystal displays:
- Remaining time until decay
- Resource consumption per day
- Color state (green → yellow → red)
- Last resource contribution

---

### 2.2 Decay Resource

- Must be actively inserted into the Claim Crystal
- Consumed per plot per day
- The more plots a crystal covers, the higher the daily consumption
- Resource can be deposited by:
  - the owner
  - trusted players
  - guild members

**Capacity**
- Limited storage capacity (no unlimited stockpiling)
- Example: enough for 7–10 real-life days
- Encourages active upkeep rather than “set and forget”

---

### 2.3 Decay Phases

1. **Active**
   - Crystal is green
   - Full protection enabled

2. **Warning Phase**
   - Crystal turns yellow / orange
   - Visible countdown (e.g. 24 hours)

3. **Decayed**
   - Crystal turns red
   - For approximately 3 days:
     - blocks can be broken
     - containers can be looted

4. **Release**
   - Claim is removed
   - Plot becomes available for reclaiming

---

### 2.4 Decay Visibility

- Color changes and particle effects on the Claim Crystal
- UI tooltip when nearby
- Subtle map indicators for decayed claims

Goal: transparency and fairness instead of surprise or frustration.

---

## 3. Economy System

### 3.1 Currencies

- 100 Copper = 1 Silver
- 100 Silver = 1 Gold

---

### 3.2 Voting Rewards

- Voting rewards **Copper only**
- No Silver
- No Gold
- No equipment
- No progression materials

Voting is meant for early support and convenience, not progression acceleration.

---

### 3.3 Income Sources

- Player shops
- Services
- PvP farm world activities
- Instances and dangerous biomes
- Player-created games

---

### 3.4 Gold Sinks

- Plot maintenance fees
- Upkeep costs
- NPC services:
  - cosmetic effects
  - scrolls
  - emotes
  - convenience features (e.g. /home)
- Exclusive prestige locations for high-wealth players

---

## 4. Shops, Businesses & Player Games

### Shops & Businesses
- Located on standard plots
- Use modified merchant chests
- Transparent trading mechanics

**Costs**
- Base plot fee
- Additional small transaction tax (e.g. 1–2%)
- No fixed additional rent for shops

---

### Player Games
- Skill-based content (parkour, puzzles, arenas)
- Entry fee paid in in-game currency
- No RNG-based gambling
- Clear rules:
  - maximum entry cost
  - minimum payout
- Enforcement:
  - Discord ticket system
  - rule violations result in loss of permission to host player games

---

## 5. Scrolls & Consumable Items

### Allowed
- Teleporting to players with consent
- Visual effects (fireworks, glow, particles)
- Short-duration buffs (invisibility, speed, night vision)

### Forbidden
- Teleporting without consent
- Teleporting into protected claims
- Escaping PvP or death situations

Core principle:
Attention and convenience are allowed.
Power, exploits, and conflict avoidance are not.

---

## 6. Design Principles

- Clear separation of systems (Hub / Farm Worlds / Minigames)
- Players generate meaningful content
- Economy is regulated through sinks, not admin intervention
- Progression through activity, not voting or shortcuts
- Transparency over hidden mechanics

---

## Status
**Work in Progress – Design Phase**

Next focus: technical specification of the Claim Crystal system.

