# 05 — Gameplay Mechanics

---

## Core Movement Values

All values use GB Studio 4.2's internal 0–255 scale unless otherwise specified.

| Parameter | Value | Notes |
|---|---|---|
| Walk Speed | 96 | Comfortable pace, responsive but not twitchy |
| Run Speed | N/A | No separate run — Solen walks at a consistent speed. Dash provides burst movement. |
| Jump Height | 160 (base) / 176 (upgraded) | Base jump clears ~3 tiles. Upgraded jump (after World 4) clears ~3.5 tiles. |
| Gravity | 128 (standard) / 112 (Brine caverns) / 80 (underwater) | Standard in most scenes. Reduced in Sunken Brine for a heavier atmosphere. Minimal underwater for floaty swimming. |
| Jump Velocity (Initial) | 192 | Sharp upward launch, decelerating arc |
| Fall Speed (Terminal) | 160 | Capped to prevent unfair deaths |
| Wall Slide Speed | 48 | Slow slide down walls, giving player time to wall-jump |
| Wall Jump Horizontal | 128 | Kicks player away from wall ~2 tiles |
| Wall Jump Vertical | 176 | Slightly higher than standard jump to enable vertical ascent |
| Dash Speed | 224 | Fast horizontal burst |
| Dash Duration | 8 frames | Covers ~3 tiles horizontally |
| Dash Cooldown | 30 frames (~0.5 seconds) | Prevents dash spam |
| Coyote Time | 6 frames (standard) / 8 frames (underwater) | Grace period after leaving a platform edge where jump is still valid |
| Double Jump Height | 144 | Slightly lower than first jump, adds ~2.5 tiles of height |
| Ladder Climb Speed | 64 | Slow, deliberate, safe |
| Swim Speed | 72 | Slower than walking, directional (8-way) |

---

## Platformer Features — Enabled Per World

| Feature | Prologue | World 1 | World 2 | World 3 | World 4 | World 5 |
|---|---|---|---|---|---|---|
| Gravity | YES | YES | YES | YES (reduced) | YES | YES |
| Jump | YES | YES | YES | YES (reduced UW) | YES | YES |
| Double Jump | NO | NO | NO | NO | NO | YES |
| Wall Jump | NO | YES (from 1-3) | YES | YES | YES | YES |
| Dash | NO | NO | NO | NO | YES (from 4-1) | YES |
| Coyote Time | YES | YES | YES | YES (extended) | YES | YES |
| Ladders | NO | YES | YES | YES | YES | YES |
| Floating | NO | NO | NO | YES (underwater) | NO | NO |

### How Each Feature Is Used in Level Design

**Gravity:** Standard gravity creates the baseline feel. Reduced gravity in the Sunken Brine makes the player feel the weight of water and atmosphere. Underwater gravity is minimal, creating a floaty, vulnerable feeling.

**Jump:** The primary movement tool. Level design ensures all gaps in Worlds 1–3 are clearable with the base jump. The upgraded jump in World 5 is needed for the taller gaps in the Spire Ascent.

**Double Jump:** Introduced at the start of World 5 when the combined Hearthstone energy empowers Solen. Used to reach higher floating platforms in the Ascent and to dodge Phase 2 Varek attacks. Also enables backtracking to earlier worlds for previously unreachable Ember Shards.

**Wall Jump:** Introduced in World 1, Scene 1-3 (Thornveil Thicket). Used for vertical ascent sections in every subsequent world. The Frostfang Peaks use wall jump + ice physics for challenging climbs. The Spire's vertical sections require chained wall jumps.

**Dash:** Introduced in World 4, Scene 4-1 via Wrench's boot upgrade. Used to cross lava gaps, break cracked walls, dodge boss attacks, and reach distant platforms. Combined with wall jump for advanced movement. Enables backtracking to break walls in earlier worlds.

**Coyote Time:** A forgiving design choice. The 6-frame window means the player can jump slightly after leaving a platform edge, reducing frustration on tight jumps. Extended to 8 frames underwater where the floaty physics make precise jumps harder.

**Ladders:** Contextual climbing surfaces (vines, roots, chains, scaffolding, seaweed). Used for slow, safe vertical traversal in contrast to the fast, risky wall jump. Often placed near collectibles or as an alternative path for less skilled players.

**Floating:** Underwater-only mechanic. The player drifts slowly upward unless pressing Down. Creates a unique movement challenge: the player must actively manage vertical position while navigating horizontal hazards.

---

## Health System

### HP Count

| Stat | Value |
|---|---|
| Starting Max HP | 5 hearts |
| Maximum Possible HP | 8 hearts (with all Heart Crystal upgrades) |
| Heart Crystal Pieces per upgrade | 4 pieces = 1 new heart |
| Total Heart Crystal Pieces in game | 12 (= 3 extra hearts) |

### How Damage Works

| Source | Damage |
|---|---|
| Enemy contact (basic enemies) | 1 HP |
| Enemy projectile | 1 HP |
| Environmental hazard (shadow puddle, thorns, dripping acid) | 1 HP |
| Boss attack (standard) | 2 HP |
| Boss attack (heavy / Phase 2) | 3 HP |
| Magma / Bottomless Pit | Instant death (respawn at checkpoint) |
| Steam Vent | 2 HP + knockback |

**Invincibility Frames:** After taking damage, Solen has 60 frames (~1 second) of invincibility. During this time, her sprite flashes (alternates visible/invisible every 4 frames). She can still move and attack during i-frames.

**Knockback:** Taking damage knocks Solen backward ~1.5 tiles in the direction opposite the damage source. During knockback, the player has no control for 8 frames, then regains control during the remaining i-frames. Knockback near edges is a primary source of pit deaths.

### How Healing Works

| Item | Healing | Source |
|---|---|---|
| Healing Tincture | 2 HP | Crafted by Fern (given after World 1 meeting). Player carries up to 3. Refilled at checkpoints. |
| Flame Coin Heal | 1 HP | Collecting 50 Flame Coins restores 1 HP automatically |
| Checkpoint Heal | Full HP | Touching a checkpoint lamppost fully restores HP and refills tinctures |
| Hearthstone Reignition | Full HP | After each boss victory, HP is fully restored |

---

## Checkpoint System

Ember Tide uses a **checkpoint lamppost** system rather than lives.

- **Lampposts** are placed at the start of every scene and at midpoints in longer scenes.
- Touching a lamppost lights it (Solen's lantern flares briefly) and sets the respawn point.
- Upon death, the player respawns at the last touched lamppost with full HP and full tinctures.
- There is no "lives" counter or Game Over in the traditional sense. The game never forces the player back to the start of a world.
- **Flame Coins collected before death are retained.** This prevents frustration and allows incremental progress even on difficult sections.
- **Enemies respawn when the player dies and respawns.** This prevents the player from trivially clearing rooms by trading deaths.
- Boss fights have a single checkpoint at the start of the fight. Dying during a boss fight restarts the fight from Phase 1.

---

## Inventory and Collectible System

### Collectible Types

| Collectible | Icon | Total in Game | Purpose |
|---|---|---|---|
| Flame Coins | Small flame icon | ~300 | Currency — used to buy tinctures and upgrades at Fern's shop (accessible from World Map after World 1) |
| Ember Shards | Orange crystal icon | 25 | Key collectible — required for true ending. 5 per world. |
| Heart Crystal Pieces | Pink heart fragment | 12 | 4 pieces = 1 max HP upgrade. 3 full upgrades total. |
| Lore Stones | Blue rune stone | 5 | 1 per world. Contains a fragment of the First Keeper incantation. Required for true ending. |
| Coral's Locket | Locket icon | 1 | Optional fetch quest. Return to Coral for bonus dialogue and a reward (permanent tincture capacity +1). |
| Aldric's Badge | Lamplighter badge | 1 | Story item. Obtained after defeating Shade. No gameplay effect — lore/emotional significance. |
| Edric's Figurine | Wooden lantern | 1 | Story item. Obtained from Wrench. No gameplay effect — emotional significance. |

### Inventory Screen

The inventory is not a separate screen in the traditional sense. Collectible counts are visible on the pause menu:

- Ember Shards: X / 25
- Lore Stones: X / 5
- Heart Crystals: X / 12 pieces (Y / 3 full)
- Flame Coins: XXX
- Tinctures: X / 3 (or X / 4 after Coral's quest)

---

## Power-Ups

Power-ups in Ember Tide are permanent ability upgrades rather than temporary buffs. Each is tied to a story moment and an NPC.

### 1. Wall Jump — "Sticky Soles"

| Property | Detail |
|---|---|
| Given by | Fern (World 1, Scene 1-3) / Orin improves height (World 2) |
| Description | Solen can jump off walls by pressing Jump while sliding against a wall surface. |
| Where it appears | World 1, Scene 1-3 (Thornveil Thicket). Orin's climbing gear in World 2 increases wall jump height by ~1 tile. |
| Level design use | Vertical ascent sections, reaching high platforms, navigating narrow vertical shafts, accessing secrets in earlier worlds via backtracking. |

### 2. Dash — "Quick-Step Boots"

| Property | Detail |
|---|---|
| Given by | Wrench (World 4, Scene 4-1) |
| Description | Solen dashes horizontally at high speed for 8 frames. Invincible during dash frames. Can be used in air. Cooldown of 30 frames. |
| Where it appears | World 4, Scene 4-1 (Magma Tunnels). |
| Level design use | Crossing lava gaps, breaking cracked walls/doors, dodging boss attacks, reaching distant platforms. Combined with wall jump for advanced traversal. Enables backtracking to break walls in Worlds 1–3. |

### 3. Double Jump — "Hearthstone Resonance"

| Property | Detail |
|---|---|
| Given by | Automatically unlocked at start of World 5 (narrative: four Hearthstones empowering the lantern) |
| Description | Solen can jump a second time in mid-air. Second jump is slightly lower than the first. |
| Where it appears | World 5, Scene 5-1 (Floating Platforms). |
| Level design use | Reaching high floating platforms in the Spire Ascent, dodging Varek's arena attacks, accessing previously unreachable Ember Shards in earlier worlds via backtracking. |

### 4. Lantern Upgrades (Passive)

| Upgrade | Trigger | Effect |
|---|---|---|
| Lantern Level 1 (Base) | Game start | Lantern provides small light radius. Attack deals 1 HP to enemies. |
| Lantern Level 2 | Verdant Hearthstone reignited | Light radius increases. Attack deals 2 HP. Illuminates hidden passages. |
| Lantern Level 3 | Frost Hearthstone reignited | Light radius increases further. Attack deals 2 HP + slight knockback. |
| Lantern Level 4 | Brine Hearthstone reignited | Light radius near-maximum. Attack deals 3 HP. Reveals invisible enemies in lantern radius. |
| Lantern Level 5 | Forge Hearthstone reignited | Maximum light radius. Attack deals 3 HP + fire trail (brief damage zone on ground after swing). |

---

## HUD Layout

The HUD must fit within the 160×144 pixel screen without obscuring gameplay. All HUD elements are positioned at the top of the screen in a 160×16 pixel strip, leaving 160×128 pixels for gameplay.

```
┌─────────────────────────────────────────┐
│ ♥♥♥♥♥○○○  ⬡23  🔥×2  [WORLD 1-3]     │  ← HUD strip (160×16px)
├─────────────────────────────────────────┤
│                                         │
│                                         │
│           GAMEPLAY AREA                 │
│           (160×128 px)                  │
│                                         │
│                                         │
│                                         │
│                                         │
└─────────────────────────────────────────┘
```

| Element | Position (from left) | Size | Description |
|---|---|---|---|
| Health Hearts | X: 2px, Y: 2px | 10×10 px per heart, up to 8 | Filled hearts for current HP, empty outlines for lost HP. Red when full, gray outline when empty. Flash white when hit. |
| Flame Coin Counter | X: 88px, Y: 2px | 8×8 icon + 3-digit number | Small flame icon followed by count (e.g., "×023"). Uses small font. |
| Tincture Counter | X: 124px, Y: 2px | 8×8 icon + 1-digit number | Small bottle icon followed by count (e.g., "×2"). |
| Scene Name | X: 2px, Y: 8px | Variable width, small font | Brief scene identifier shown for 3 seconds on scene entry, then fades. |

### HUD Palette

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background (gameplay shows through) |
| Color 1 | Dark Red | `#8B0000` | Heart outlines, text shadow |
| Color 2 | Bright Red | `#FF2020` | Filled hearts |
| Color 3 | White | `#FFFFFF` | Coin count text, tincture count, UI highlights |

---

## Pause Menu

Pressing START during gameplay pauses the game and opens the pause menu overlay. The pause menu is a centered box on the screen.

### Pause Menu Layout

```
┌─────────────────────────────────────────┐
│                                         │
│         ┌───────────────────┐           │
│         │    ═══ PAUSED ═══ │           │
│         │                   │           │
│         │  > RESUME         │           │
│         │    INVENTORY      │           │
│         │    MAP            │           │
│         │    OPTIONS        │           │
│         │    QUIT           │           │
│         │                   │           │
│         └───────────────────┘           │
│                                         │
└─────────────────────────────────────────┘
```

### Pause Menu Options

| Option | Action |
|---|---|
| Resume | Closes pause menu, returns to gameplay |
| Inventory | Shows collectible counts: Ember Shards, Lore Stones, Heart Crystal Pieces, Flame Coins, Tinctures, Story Items |
| Map | Shows the world map with current position, lit/unlit Hearthstones, and available paths |
| Options | Sound volume (SFX/Music toggles — ON/OFF), Button mapping display |
| Quit | Returns to title screen (progress is auto-saved at last checkpoint) |

---

## Game Over Screen

There is no traditional Game Over screen because the game uses a checkpoint system with no lives. However, upon death:

1. Solen's death animation plays (collapses, lantern dims).
2. Screen fades to black over 1 second.
3. Text appears: *"The lantern flickers..."*
4. Screen fades back in at the last checkpoint lamppost.
5. Solen's respawn animation plays (lantern relights, she stands).

This keeps the player in the flow without punishing them with a Game Over screen. The game never truly "ends" due to failure — only due to quitting or completing the story.

---

## Save System

- **Auto-Save:** The game auto-saves at every checkpoint lamppost.
- **Save Data:** One save slot. Saves: current scene, checkpoint position, HP, all collectibles, all abilities unlocked, all Hearthstones reignited, story flags.
- **RAM Save:** GB Studio uses SRAM for save data. The save is written to the cartridge's battery-backed RAM (or emulator save state).
- **Continue:** On the title screen, "Continue" loads the last auto-save. "New Game" overwrites the save.

---

## Combat

### Attack

Solen attacks by swinging her lantern staff with the A button. The attack is a forward arc that covers ~1.5 tiles in front of her.

| Property | Value |
|---|---|
| Attack animation | 3 frames (~0.18 seconds) |
| Hitbox active frames | Frame 2 only |
| Damage | 1 HP (Level 1) → 3 HP (Level 5) per hit |
| Cooldown | 12 frames (~0.2 seconds) between swings |
| Direction | Horizontal only (the direction Solen faces) |
| Special (Level 5) | Leaves a fire trail on the ground for 30 frames, dealing 1 HP to enemies that walk through it |

### Attack Strategy

Combat in Ember Tide is simple by design. Enemies are primarily obstacles to be avoided or dispatched quickly, not complex combat encounters. The skill expression is in **positioning** — hitting enemies without taking contact damage, managing knockback near edges, and timing attacks between enemy patterns. Boss fights are the exception, requiring pattern recognition and precise timing.

---

## Interaction System

Pressing the A button near an interactive object (NPC, sign, item, mechanism) triggers an interaction event. Interactive objects display a small arrow icon above them when the player is in range.

| Interaction Type | Trigger | Result |
|---|---|---|
| NPC Talk | A button near NPC | Display Dialogue event with portrait |
| Sign Read | A button near sign | Display text box (no portrait) |
| Item Pickup | A button near item or walk over item | Item collected, counter updated, brief text |
| Mechanism | A button near valve/lever/switch | Mechanism activates, environmental change |
| Checkpoint Lamppost | Walk through | Lamppost lights, save triggered, HP restored |
| Destructible Wall | Attack near cracked surface | Wall breaks, reveals hidden area |

---

## Difficulty Considerations

Ember Tide is designed to be **accessible on the critical path** and **challenging for completionists**.

| Aspect | Critical Path | Completionist Path |
|---|---|---|
| Platforming difficulty | Moderate — generous platforms, coyote time | High — tight jumps, hidden areas, backtracking puzzles |
| Enemy difficulty | Low-moderate — enemies are avoidable, damage is manageable | Moderate — more enemies in secret rooms, tougher enemy combos |
| Boss difficulty | Moderate — clear patterns, forgiving hitboxes | N/A (same bosses) |
| Collectible accessibility | Flame Coins and Tinctures are plentiful | Ember Shards and Lore Stones require exploration and advanced movement |
| True ending requirement | N/A (normal ending is default) | High — requires all 25 Ember Shards and all 5 Lore Stones |
