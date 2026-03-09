# 06 — Progression and RPG Systems

---

## XP and Leveling

### Level Cap

The maximum level for all characters is **Level 30**. The game is balanced so that a player who fights most encounters and completes side quests will reach approximately Level 22–25 by the final boss. Reaching Level 30 requires thorough grinding or completion of all optional content, and is primarily useful for the secret boss in the true ending path.

### XP Thresholds

XP is a cumulative total stored in `VAR_PLAYER_XP`. When the total meets or exceeds the threshold for the next level, a level-up triggers. Companion XP is tracked separately in `VAR_COMP_XP_LIRA` and `VAR_COMP_XP_ROOK` and uses the same thresholds. Companions gain XP even when not the active companion, but at 50% rate (to prevent one companion from falling hopelessly behind).

| Level | Total XP Required | XP to Next Level |
|-------|-------------------|-----------------|
| 1 | 0 | 20 |
| 2 | 20 | 30 |
| 3 | 50 | 40 |
| 4 | 90 | 55 |
| 5 | 145 | 70 |
| 6 | 215 | 90 |
| 7 | 305 | 110 |
| 8 | 415 | 135 |
| 9 | 550 | 160 |
| 10 | 710 | 190 |
| 11 | 900 | 220 |
| 12 | 1120 | 260 |
| 13 | 1380 | 300 |
| 14 | 1680 | 350 |
| 15 | 2030 | 400 |
| 16 | 2430 | 460 |
| 17 | 2890 | 520 |
| 18 | 3410 | 590 |
| 19 | 4000 | 660 |
| 20 | 4660 | 740 |
| 21 | 5400 | 830 |
| 22 | 6230 | 920 |
| 23 | 7150 | 1020 |
| 24 | 8170 | 1130 |
| 25 | 9300 | 1250 |
| 26 | 10550 | 1380 |
| 27 | 11930 | 1520 |
| 28 | 13450 | 1670 |
| 29 | 15120 | 1880 |
| 30 | 17000 | — (max) |

### Stat Increases per Level — Edyn

| Level | HP | ATK | DEF | SPD | MP |
|-------|----|-----|-----|-----|----|
| 1 | 28 | 8 | 6 | 10 | 12 |
| 2 | 33 | 9 | 7 | 11 | 14 |
| 3 | 38 | 11 | 8 | 12 | 16 |
| 4 | 43 | 12 | 9 | 14 | 18 |
| 5 | 49 | 14 | 10 | 15 | 20 |
| 6 | 55 | 15 | 11 | 17 | 22 |
| 7 | 61 | 17 | 13 | 18 | 25 |
| 8 | 67 | 18 | 14 | 20 | 27 |
| 9 | 74 | 20 | 15 | 21 | 29 |
| 10 | 80 | 22 | 17 | 23 | 32 |
| 11 | 87 | 23 | 18 | 24 | 34 |
| 12 | 94 | 25 | 19 | 26 | 37 |
| 13 | 101 | 27 | 21 | 27 | 39 |
| 14 | 108 | 28 | 22 | 29 | 42 |
| 15 | 116 | 30 | 24 | 31 | 44 |
| 16 | 123 | 32 | 25 | 32 | 47 |
| 17 | 131 | 34 | 27 | 34 | 49 |
| 18 | 138 | 35 | 28 | 36 | 52 |
| 19 | 146 | 37 | 30 | 37 | 54 |
| 20 | 153 | 39 | 31 | 39 | 57 |
| 21 | 156 | 40 | 32 | 40 | 58 |
| 22 | 159 | 42 | 33 | 42 | 59 |
| 23 | 162 | 43 | 34 | 43 | 60 |
| 24 | 165 | 45 | 35 | 45 | 61 |
| 25 | 168 | 46 | 36 | 47 | 62 |
| 26 | 171 | 47 | 37 | 48 | 63 |
| 27 | 174 | 49 | 38 | 50 | 64 |
| 28 | 176 | 50 | 39 | 52 | 64 |
| 29 | 178 | 51 | 39 | 53 | 65 |
| 30 | 180 | 52 | 40 | 55 | 65 |

### Stat Increases per Level — Lira

| Level | HP | ATK | DEF | SPD | MP |
|-------|----|-----|-----|-----|----|
| 1 | 22 | 5 | 5 | 8 | 18 |
| 5 | 38 | 9 | 8 | 14 | 30 |
| 10 | 60 | 14 | 14 | 22 | 48 |
| 15 | 85 | 18 | 20 | 30 | 60 |
| 20 | 110 | 22 | 25 | 36 | 72 |
| 25 | 128 | 26 | 30 | 40 | 80 |
| 30 | 140 | 30 | 35 | 45 | 85 |

### Stat Increases per Level — Rook

| Level | HP | ATK | DEF | SPD | MP |
|-------|----|-----|-----|-----|----|
| 1 | 35 | 12 | 10 | 5 | 6 |
| 5 | 62 | 22 | 18 | 9 | 10 |
| 10 | 100 | 34 | 28 | 14 | 15 |
| 15 | 140 | 44 | 38 | 18 | 20 |
| 20 | 175 | 52 | 46 | 22 | 24 |
| 25 | 200 | 60 | 53 | 26 | 27 |
| 30 | 220 | 65 | 58 | 30 | 30 |

### Level-Up Script Implementation

When `VAR_PLAYER_XP` >= the threshold for the next level:

1. Increment `VAR_PLAYER_LEVEL` by 1.
2. Look up the new level in a conditional chain (If `VAR_PLAYER_LEVEL` == 2, set stats to level 2 values; if == 3, set to level 3 values; etc.).
3. Update `VAR_PLAYER_MAX_HP`, `VAR_PLAYER_ATK`, `VAR_PLAYER_DEF`, `VAR_PLAYER_SPD`, `VAR_PLAYER_MAX_MP`.
4. Restore HP and MP to full (level-up heal).
5. Display: "Level Up! Edyn is now Level [X]!"
6. Display stat changes.
7. Check for spell unlocks: If new level matches a spell unlock threshold, set the spell flag variable. Display: "Learned [Spell Name]!"
8. Update `VAR_PLAYER_LEVEL_THRESHOLD` to the next level's XP requirement.

---

## Equipment System

### Equipment Slots

Each character has 3 equipment slots:
- **Weapon** — Affects ATK
- **Armor** — Affects DEF
- **Accessory** — Provides special bonuses (SPD, HP, status immunity, etc.)

Equipment is tracked via variables:
- `VAR_EQUIP_WEAPON_EDYN` (integer, references weapon ID)
- `VAR_EQUIP_ARMOR_EDYN`
- `VAR_EQUIP_ACCESSORY_EDYN`
- `VAR_EQUIP_WEAPON_LIRA` / `VAR_EQUIP_ARMOR_LIRA` / `VAR_EQUIP_ACCESSORY_LIRA`
- `VAR_EQUIP_WEAPON_ROOK` / `VAR_EQUIP_ARMOR_ROOK` / `VAR_EQUIP_ACCESSORY_ROOK`

When equipment changes, the stat bonuses are recalculated: base stats (from level) + weapon ATK bonus + armor DEF bonus + accessory bonus = final stat stored in the combat variables.

### Weapons

| ID | Name | User | ATK Bonus | Special | Where Found |
|----|------|------|-----------|---------|-------------|
| 1 | Apprentice Wrench | Edyn | +2 | — | Starting equipment |
| 2 | Alaric's Wrench | Edyn | +5 | — | Gift from Bram (return visit) |
| 3 | Wave Conduit Blade | Edyn | +8 | Enables Tidal Slash (bonus water damage vs certain enemies) | Tidal Meridian F2 chest |
| 4 | Decay Edge | Edyn | +10 | 10% chance to poison enemy on attack | Hollow Meridian F2 chest |
| 5 | Prism Blade | Edyn | +12 | Light-element damage | Prism Meridian F2 chest |
| 6 | Chronoblade | Edyn | +14 | +3 SPD bonus | Chronospire F1 chest |
| 7 | Epoch Saber | Edyn | +18 | +5 ATK when HP < 50% | Crafted at Ironpeak Forge (Architect Alloy + 500 Gold) |
| 8 | Healer's Staff | Lira | +3 | Healing spells +10 HP bonus | Starting equipment |
| 9 | Aether Staff | Lira | +6 | MP cost reduced by 1 for all spells | Purchased in Stormhaven |
| 10 | Bloom Rod | Lira | +9 | Healing spells +20 HP bonus | Ashenveil side quest reward |
| 11 | Crystal Wand | Lira | +12 | Magic damage +5 | Prism Meridian chest |
| 12 | Miner's Pick | Rook | +6 | — | Starting equipment |
| 13 | Ironpeak Maul | Rook | +10 | +3 DEF bonus | Purchased in Ironpeak |
| 14 | Shatter Hammer | Rook | +14 | Shatter Blow damage +10 | Crafted at Ironpeak Forge |
| 15 | Warden's Bane | Rook | +18 | +5 ATK vs bosses | Chronospire F3 chest |

### Armor

| ID | Name | User | DEF Bonus | Special | Where Found |
|----|------|------|-----------|---------|-------------|
| 1 | Linen Shirt | Edyn | +2 | — | Starting equipment |
| 2 | Leather Vest | Edyn | +4 | — | Purchased in Millhaven |
| 3 | Sailor's Coat | Edyn | +6 | — | Purchased in Stormhaven |
| 4 | Marsh Hide | Edyn | +8 | Poison resistance (50% chance to resist) | Ashenveil side quest |
| 5 | Crystal Shield Vest | Edyn | +10 | — | Crystalfall Desert chest |
| 6 | Keeper's Robe | Edyn | +12 | +5 MP bonus | Chronospire F3 chest |
| 7 | Epoch Plate | Edyn | +15 | +3 SPD bonus | Crafted at Ironpeak |
| 8 | Herbalist Wrap | Lira | +3 | — | Starting equipment |
| 9 | Woven Cloak | Lira | +5 | — | Purchased in Millhaven |
| 10 | Tidal Shawl | Lira | +7 | MP regen (+2 MP per battle round) | Stormhaven side quest |
| 11 | Ironweave Robe | Lira | +10 | — | Purchased in Ironpeak |
| 12 | Soldier's Plate | Rook | +5 | — | Starting equipment |
| 13 | Reinforced Coat | Rook | +8 | — | Purchased in Stormhaven |
| 14 | Ironpeak Armor | Rook | +12 | — | Purchased in Ironpeak |
| 15 | Forge Master Plate | Rook | +16 | Iron Guard effectiveness +25% | Crafted at Ironpeak |

### Accessories

| ID | Name | User | Bonus | Where Found |
|----|------|------|-------|-------------|
| 1 | Brass Goggles | Edyn | +2 SPD | Starting equipment |
| 2 | Sailor's Charm | Any | +2 DEF | Cliff Path chest (Stormhaven) |
| 3 | Warm Cloak | Any | Immunity to cold status | Ironpeak Pass chest |
| 4 | Temporal Ring | Any | +5 SPD | Chronospire F2 chest |
| 5 | Aether Pendant | Any | +10 MP | Hidden in Architect Ruins |
| 6 | Tideborn Relic | Edyn | Pocket watch power +1 (enables Chrono Shield in battle) | Given by Corwin |
| 7 | Vitality Band | Any | +15 HP | Purchased in Ironpeak |
| 8 | Lucky Coin | Any | +10% Gold from battles | Stormhaven fishing quest reward |
| 9 | Keeper's Seal | Any | +5 DEF, +5 MP | Collected with all 5 Keeper Fragments (true ending path) |

---

## Magic / Ability System

### Edyn's Abilities

| Ability | MP Cost | Effect | Unlock Condition |
|---------|---------|--------|-----------------|
| Aether Bolt | 4 | Single target: ATK+4 magic damage | Available from start |
| Temporal Slow | 6 | Single target: -5 SPD to enemy for rest of battle | After restoring Verdant Meridian |
| Chrono Strike | 8 | Single target: ATK×2 magic damage | After restoring Hollow Meridian |
| Chrono Shield | 5 | Self: Halves damage taken for 1 round | Requires Tideborn Relic equipped |
| Epoch Burst | 12 | All enemies (boss phases count as 1): ATK×2+10 magic damage | After restoring all 5 Meridians |

### Lira's Abilities

| Ability | MP Cost | Effect | Unlock Condition |
|---------|---------|--------|-----------------|
| Mending Light | 5 | Single ally: Heals 20 HP (30 with Bloom Rod) | Available when Lira joins |
| Purify | 3 | All allies: Clears all status effects | Available when Lira joins |
| Aether Bloom | 10 | All allies: Heals 30 HP each | After restoring Tidal Meridian |
| Rejuvenate | 8 | Single ally: Heals 50 HP | After restoring Hollow Meridian |
| Guardian Light | 12 | All allies: +5 DEF for rest of battle | After restoring Prism Meridian |

### Rook's Abilities

| Ability | MP Cost | Effect | Unlock Condition |
|---------|---------|--------|-----------------|
| Iron Guard | 4 | Self: Halves damage taken for 1 round | Available when Rook joins |
| Shatter Blow | 8 | Single target: ATK×2 - DEF/4 (pierces defense) | After restoring Hollow Meridian |
| Earthbreaker | 10 | Single target: ATK×2+8 physical damage, 30% stun chance | After restoring Prism Meridian |
| Last Stand | 6 | Self: If HP < 25%, ATK doubles for 3 rounds | After reaching Ironpeak Enclave |

---

## Gold / Currency System

### Earning Gold

| Source | Amount |
|--------|--------|
| Standard enemy drops | 5–30 Gold (varies by enemy) |
| Boss defeat | 100–500 Gold |
| Treasure chests | 50–300 Gold |
| Quest rewards | 50–200 Gold |
| Selling items to shops | 50% of buy price |

### Spending Gold

| Use | Typical Cost Range |
|-----|-------------------|
| Consumable items (Potions, etc.) | 15–100 Gold |
| Weapons | 100–800 Gold |
| Armor | 80–600 Gold |
| Accessories | 100–500 Gold |
| Crafting (Ironpeak Forge) | 300–500 Gold + materials |
| Inn rest (full HP/MP restore) | 20–50 Gold |

### Economy Balance

The game's economy is designed so that a player who fights most enemies and opens most chests will have enough gold to buy key upgrades at each town without needing to grind specifically for money. Sable's Haggle passive (15% discount) provides a meaningful advantage for players who recruit her.

---

## Shop System

### Shop Locations and Inventories

#### Wynn's General Store (Millhaven)

| Item | Price |
|------|-------|
| Potion | 15 Gold |
| Antidote | 10 Gold |
| Smoke Bomb | 30 Gold |
| Leather Vest | 80 Gold |
| Woven Cloak (Lira) | 60 Gold |

#### Stormhaven Supplies (Tully's Shop)

| Item | Price |
|------|-------|
| Potion | 15 Gold |
| Hi-Potion | 40 Gold |
| Antidote | 10 Gold |
| Aether Crystal | 25 Gold |
| Sailor's Coat | 150 Gold |
| Reinforced Coat (Rook) | 180 Gold |
| Aether Staff (Lira) | 200 Gold |

#### Ironpeak Market (Kira's Stall)

| Item | Price |
|------|-------|
| Hi-Potion | 40 Gold |
| Mega Potion | 100 Gold |
| Aether Crystal (Large) | 60 Gold |
| Antidote | 10 Gold |
| Smoke Bomb | 30 Gold |
| Vitality Band | 400 Gold |
| Ironpeak Armor (Rook) | 500 Gold |
| Ironweave Robe (Lira) | 450 Gold |
| Ironpeak Maul (Rook) | 400 Gold |

#### Ironpeak Deep Forge (Blacksmith Forge)

| Craft | Cost | Materials |
|-------|------|-----------|
| Epoch Saber (Edyn) | 500 Gold | Architect Alloy ×1 |
| Shatter Hammer (Rook) | 500 Gold | Architect Alloy ×1 |
| Epoch Plate (Edyn) | 450 Gold | Architect Alloy ×1 |
| Forge Master Plate (Rook) | 450 Gold | Architect Alloy ×1 |

### Shop Implementation in GB Studio

Shops use a combination of Display Dialogue and Display Menu events:

1. Player interacts with shopkeeper NPC (press A).
2. Shopkeeper greeting dialogue.
3. Display Menu: "Buy / Sell / Leave"
4. **Buy:** Display Menu with up to 4 items per page (GB Studio menu limit). Each item shows name and price. On selection, check if `VAR_PLAYER_GOLD` >= price. If yes, subtract gold, add item to inventory variable, display "Purchased [Item]!" If no, display "Not enough Gold!"
5. **Sell:** Display Menu with items from inventory (quantity > 0). Sell price = 50% buy price. Add gold, decrement item variable.
6. **Leave:** Return to overworld interaction.

Sable's Haggle: When `VAR_SABLE_IN_PARTY` == 1, all prices in the Buy menu are reduced by 15% (calculated before displaying price).

---

## Save System

### Save Method

GB Studio 4.2 supports saving game data to battery-backed SRAM. The game uses a **manual save system** — the player must interact with a save point to save.

### Save Points

Save points are specific interactable objects placed in safe locations throughout the game:

| Save Point Location | Visual |
|--------------------|--------|
| Millhaven Town Square — Town Well | Stone well with glowing Aether trim |
| Oakwatch Grove — Campfire | Campfire with blue Aether flame |
| Stormhaven — Message Board | Wooden message board with Aether crystal |
| Ashenveil Marsh — Hollow Meridian Approach | Glowing marsh flower |
| Crystalfall Desert — Crystal Canyon | Crystal formation |
| Ironpeak Enclave — Central Forge | Forge anvil with Aether glow |
| Chronospire — Base | Stone pedestal |
| Chronospire F4 — Before boss | Aether crystal cluster |

### Save Data Structure

When the player saves, the following variables are written to SRAM:

| Category | Variables Saved |
|----------|----------------|
| Player Stats | Level, XP, HP, Max HP, ATK, DEF, SPD, MP, Max MP |
| Equipment | Weapon/Armor/Accessory IDs for all 3 characters |
| Inventory | All item quantity variables (Potion, Hi-Potion, etc.) |
| Gold | `VAR_PLAYER_GOLD` |
| Story Progress | All quest flag variables, Meridian restoration flags |
| Companion | Active companion, Lira level/XP, Rook level/XP |
| Location | Current scene ID, player position X/Y |
| Keeper Fragments | Fragment collection flags (1–5) |
| Affinity | Lira affinity, Rook affinity |
| Misc | Playtime counter, party composition flags |

### Save Implementation

1. Player interacts with save point (press A facing it).
2. Display Dialogue: "Save your progress? Yes / No"
3. If Yes: Execute GB Studio's "Save Data" event (saves all variable states to SRAM).
4. Display: "Progress saved."
5. If No: Return to gameplay.

### Loading

On the title screen, if save data exists:
- "Continue" option loads saved data (GB Studio "Load Data" event).
- Game resumes at the saved scene with all variables restored.
- "New Game" starts fresh, optionally offering to overwrite existing save.

---

*Chronospire: The Shattered Meridian — Progression and RPG Systems Document*
