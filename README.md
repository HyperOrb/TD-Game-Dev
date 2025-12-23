# 🃏 Card Cast! — Roguelike Tower Defense

A **roguelike tower defense** game built in Unity where players use a card-based system to place towers, cast spells, and survive escalating enemy waves. Each run is unique — draft your deck, manage your mana, and outlast the horde.

---

## 🎮 Gameplay Overview

The game is divided into three alternating phases each round:

| Phase | Description |
|---|---|
| **Draw & Build** | Draw cards from your deck and place towers on the grid |
| **Enemy Wave** | Enemies follow a waypoint path — defend your base! |
| **Shop** | Spend gold to buy new cards and upgrade your deck |

Survive all waves to win. Lose all your HP and it's game over.

---

## 🃏 Card System

Cards are the core mechanic of the game. Each card has a **type**, **mana cost**, and **rarity**:

### Card Types
- **Tower** — Places a turret on the battlefield grid
- **Spell** — Casts an area or targeted effect on enemies
- **Utility** — Special effects that buff your run or alter the game state

### Rarities
- Common → Uncommon → Rare → Epic

### Deck Mechanics
- Start with a **starting deck** of cards
- Draw cards each round (configurable hand size & draw count)
- Cards cycle through **Draw Pile → Hand → Discard Pile → shuffled back**
- Acquire new cards from the **Shop** or **Reward Screen** after waves

---

## 🗼 Turret System

Turrets are placed on grid **nodes** via Tower cards. Each turret supports:

### Attack Modes
- 🔫 **Bullet** — Standard projectile with optional modifiers:
  - **Seeking** — Homes in on the target
  - **Piercing** — Passes through multiple enemies
  - **Bouncing** — Ricochets to nearby enemies
- ⚡ **Laser** — Continuous beam with **AoE (Area of Effect)** damage
- 💣 **Catapult** — Arc-based projectile with splash radius
- 👾 **Summoner** — Spawns AI-controlled minion units

### Targeting Modes
- **First** — Enemies furthest along the path
- **Last** — Enemies nearest to the start
- **Closest** — Nearest enemy to the turret
- **Highest HP** — The tankiest enemy in range

### Features
- Range indicator on selection
- Visual & audio feedback (place sound, shoot sound, laser hum)
- Camera shake on impact

---

## 👾 Enemy System

- Enemies follow a **waypoint-based path** across the map
- Each wave spawns enemies with varying types and stats
- Enemies drop **gold** on death for spending in the shop
- **HP bars** display above each enemy
- Damage popups appear on hit

---

## 💰 Economy

| Resource | Source | Usage |
|---|---|---|
| **Mana** | Regenerates each round | Play cards from hand |
| **Gold** | Earned from killing enemies | Buy cards in the Shop |
| **HP** | Starting pool | Lost when enemies reach the end |

---

## 🛒 Shop & Rewards

- After each wave, a **Reward Screen** offers card choices to add to your deck
- The **Shop** sells cards with a configurable spawn chance per slot
- Manage your deck size wisely — the max deck size is capped

---

## 🛠️ Built With

- **Engine**: Unity (Universal Render Pipeline)
- **Language**: C#
- **UI**: TextMesh Pro
- **Audio**: Unity Audio + 2D SFX Player
- **Assets**: Low-poly 3D art packs, particle effects

---

## 🚀 How to Play

### ▶️ Play the Build (Recommended)
Download the pre-built game — no Unity required!

**🎮 [Download Card Cast! on Google Drive](https://drive.google.com/drive/folders/1xmo2d5sflHQd9Ym_rbtCH2rakYv7156c)**

### 🛠️ Run from Source
1. Clone this repository
2. Open the project in **Unity 6** (or the version used in `ProjectSettings/`)
3. Open the main scene from `Assets/Scenes/`
4. Press **Play** in the Unity Editor