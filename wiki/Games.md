# 🎮 Games Documentation

## How Games Work in AWE_Forge

AWE_Forge integrates the **AWEGame** library — 23 web games. The Games page displays all games with icons, descriptions, and developer tags. Clicking a game opens it in an iframe player.

---

## Inferno Forge 🔥
**Genre:** Incremental / Idle | **Theme:** Blacksmith / Forging | **Prestige:** Phoenix Flame Rebirth

- **Ember Energy**: Main resource, click to generate
- **Forge Upgrades**: 8 tiers (Bellows → Phoenix Anvil)
- **Temper Bar**: Fills for TEMPEST bonus
- **Prestige**: Phoenix Flame rebirth (+25% per Phoenix Core)

---

## BioGenesis Lab 🧬
**Genre:** Idle / Evolution | **Theme:** Artificial Life / DNA | **Prestige:** Species Evolution

- **DNA Strands**: Main resource, synthesize to generate
- **Lab Equipment**: 8 tiers (Microscope → Genesis Chamber)
- **10 Species Stages**: Single Cell → Cosmic Entity
- **Mutations**: Random events that boost/hinder progress

---

## Storm Chaser 🌪️
**Genre:** Incremental | **Theme:** Weather / Storms | **Prestige:** Eye of the Storm

- **Volts**: Main resource, strike lightning to generate
- **Storm Gear**: 8 tiers (Lightning Rod → Storm Nexus)
- **Storm Intensity**: Increases over time
- **Prestige**: Eye of the Storm (+25% per Storm Core)

---

## Phantom Seas 🏴‍☠️
**Genre:** Idle / Pirate | **Theme:** Ghost Pirates | **Prestige:** Davy Jones' Locker

- **Doubloons**: Main resource, plunder to earn
- **Ship Upgrades**: 8 tiers (Ghost Ship → Leviathan)
- **Curse Mechanic**: Speeds progress with consequences
- **Prestige**: Davy Jones' Locker for Cursed Coins

---

## Nebula Architect 🌌
**Genre:** Incremental | **Theme:** Space / Universe | **Prestige:** Big Bang

- **Stardust**: Main resource, shape into celestial objects
- **Celestial Tools**: 8 tiers (Nebula Seeds → The Multiverse)
- **Star Systems**: Progressively larger cosmic structures
- **Prestige**: Big Bang for Universe Seeds

---

## Game Architecture
Each game (~8-23KB) is a self-contained HTML with:
- Embedded CSS + JS
- 10-language i18n (`const L = {en:{...}, hy:{...}, ...}`)
- localStorage save/load
- Prestige/rebirth system
- Click-to-generate + auto-generation
- Upgrade tiers with exponential scaling
- Language selector + back-to-library navigation