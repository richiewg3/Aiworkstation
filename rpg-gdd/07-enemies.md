# 07 — Enemies

---

## Enemy Index

All enemies in Chronospire: The Shattered Meridian are listed below, organized by region. Each enemy is visible on the overworld as a sprite actor. There are no random encounters.

---

## Region 1: Verdant Reach Enemies

### Aether Wisp

| Stat | Value |
|------|-------|
| ID | 1 |
| HP | 10 |
| ATK | 5 |
| DEF | 2 |
| SPD | 8 |
| XP Reward | 8 |
| Gold Drop | 5 |

**Visual Description:** A small, floating orb of pale blue Aether energy with a faint trailing glow. Roughly 12x12 pixels within the 16x16 sprite frame, with translucent-looking edges and a bright core.

**Overworld Behavior:** Drifts in a slow, random patrol pattern. Changes direction every 2–3 seconds. Does not chase the player. Triggers combat on touch.

**Combat Behavior:** Basic attack only (70% chance). 20% chance to use Aether Flicker (deals ATK+2 magic damage). 10% hesitate.

**Special Moves:**
- Aether Flicker: Light magic damage (ATK+2).

**Areas:** Verdant South Road, Oakwatch Grove Entrance, Verdant Meridian F1, Verdant West Road.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Small Aether Crystal | 20% |
| Nothing | 80% |

**Sprite Size:** 16x16 pixels

**Palette:** `#C0E0F8` (pale blue), `#6090D0` (medium blue), `#F8F8F8` (white core), `#2A3A5A` (dark blue shadow)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG floating energy wisp enemy. Small pale blue glowing orb with trailing energy particles, bright white core, translucent edges. 4 directional sprites (all similar since it's a sphere, with slight trail direction change). 2 animation frames per direction (pulsing glow). GBC palette: #C0E0F8, #6090D0, #F8F8F8, #2A3A5A. Clean pixel art, no anti-aliasing, indexed color."

---

### Temporal Beetle

| Stat | Value |
|------|-------|
| ID | 2 |
| HP | 14 |
| ATK | 7 |
| DEF | 5 |
| SPD | 6 |
| XP Reward | 10 |
| Gold Drop | 7 |

**Visual Description:** A round, armored beetle with an iridescent shell that shifts between green and gold. Small legs, prominent mandibles, and tiny Aether crystal growths on its back.

**Overworld Behavior:** Patrols in a set horizontal or vertical line. Reverses direction at path endpoints. Moderate speed. Triggers combat on touch.

**Combat Behavior:** 70% basic attack. 20% Shell Tuck (raises DEF by 3 for one round, skips attack). 10% hesitate.

**Special Moves:**
- Shell Tuck: Raises DEF by 3 for one round.

**Areas:** Verdant South Road, Oakwatch Grove Entrance.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Antidote | 15% |
| Nothing | 85% |

**Sprite Size:** 16x16 pixels

**Palette:** `#4A7A2A` (forest green), `#D4A847` (gold), `#2A3A1A` (dark green), `#F0E8D0` (cream highlight)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG armored beetle enemy. Round beetle with iridescent green-gold shell, small legs, prominent mandibles, tiny crystal growths on back. 4 directional sprites, 2 animation frames per direction (walking motion). GBC palette: #4A7A2A, #D4A847, #2A3A1A, #F0E8D0. Clean pixel art, no anti-aliasing, indexed color."

---

### Gear Sprite

| Stat | Value |
|------|-------|
| ID | 3 |
| HP | 16 |
| ATK | 8 |
| DEF | 6 |
| SPD | 7 |
| XP Reward | 14 |
| Gold Drop | 10 |

**Visual Description:** A living clockwork mechanism — a small brass gear with spindly mechanical legs and a single glowing red eye in the center. It clatters as it moves.

**Overworld Behavior:** Patrols inside the Verdant Meridian dungeon. Moves in a square pattern. Medium speed. Triggers combat on touch.

**Combat Behavior:** 60% basic attack. 30% Gear Spin (ATK+3 damage). 10% hesitate.

**Special Moves:**
- Gear Spin: Spinning attack dealing ATK+3 damage.

**Areas:** Verdant Meridian F1, Verdant Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Small Aether Crystal | 25% |
| Potion | 10% |
| Nothing | 65% |

**Sprite Size:** 16x16 pixels

**Palette:** `#C0A040` (brass), `#E0D0A0` (light brass), `#802020` (red eye), `#3A2A1A` (dark brown)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG mechanical gear creature enemy. Small brass gear with spindly mechanical legs, single glowing red eye in center hub, clockwork details. 4 directional sprites, 2 animation frames per direction (legs scuttling, gear rotating). GBC palette: #C0A040, #E0D0A0, #802020, #3A2A1A. Clean pixel art, no anti-aliasing, indexed color."

---

### Corroded Automaton

| Stat | Value |
|------|-------|
| ID | 4 |
| HP | 30 |
| ATK | 11 |
| DEF | 9 |
| SPD | 4 |
| XP Reward | 25 |
| Gold Drop | 18 |

**Visual Description:** A larger clockwork humanoid, roughly 16x16 pixels but with a hunched, heavy appearance. Rusted brass plating, one arm ending in a gear-blade, the other hanging limp. Aether corrosion (green-black discoloration) covers its torso. A cracked clock face is embedded in its chest.

**Overworld Behavior:** Stationary until the player enters its detection range (2 tiles). Then slowly moves toward the player. Triggers combat on touch.

**Combat Behavior:** 60% Heavy Slam (ATK+4 damage, slow). 30% basic attack. 10% Malfunction (damages itself for 3 HP, skips turn).

**Special Moves:**
- Heavy Slam: ATK+4 physical damage.
- Malfunction: Self-inflicts 3 damage, wastes turn.

**Areas:** Verdant Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Potion | 30% |
| Small Aether Crystal | 20% |
| Nothing | 50% |

**Sprite Size:** 16x16 pixels

**Palette:** `#8A7A50` (rusted brass), `#405040` (corroded green), `#D0C0A0` (light brass), `#1A1A1A` (near black)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG corroded automaton enemy. Hunched clockwork humanoid with rusted brass plating, green-black corrosion, one gear-blade arm, cracked clock face in chest, heavy stance. 4 directional sprites, 2 animation frames per direction (slow lumbering walk). GBC palette: #8A7A50, #405040, #D0C0A0, #1A1A1A. Clean pixel art, no anti-aliasing, indexed color."

---

## Region 2: Stormhaven Coast Enemies

### Coastal Crab

| Stat | Value |
|------|-------|
| ID | 5 |
| HP | 18 |
| ATK | 9 |
| DEF | 8 |
| SPD | 5 |
| XP Reward | 14 |
| Gold Drop | 10 |

**Visual Description:** A large crab with a blue-gray shell and oversized pincers. Covered in barnacles. Moves sideways.

**Overworld Behavior:** Patrols in a horizontal line, moving sideways. Moderate speed. Triggers on touch.

**Combat Behavior:** 70% Pinch (basic attack). 20% Shell Guard (+4 DEF for one round). 10% hesitate.

**Special Moves:**
- Shell Guard: +4 DEF for one round.

**Areas:** Verdant West Road, Cliff Path to Tidal Meridian.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Potion | 20% |
| Nothing | 80% |

**Sprite Size:** 16x16 pixels

**Palette:** `#5A7A8A` (blue-gray), `#A0B8C8` (light blue-gray), `#C8A080` (barnacle tan), `#2A3A40` (dark blue)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG crab enemy. Large crab with blue-gray shell, oversized pincers, barnacle details, moves sideways. 4 directional sprites (including sideways-dominant walk), 2 animation frames. GBC palette: #5A7A8A, #A0B8C8, #C8A080, #2A3A40. Clean pixel art, no anti-aliasing, indexed color."

---

### Storm Gull

| Stat | Value |
|------|-------|
| ID | 6 |
| HP | 12 |
| ATK | 10 |
| DEF | 3 |
| SPD | 14 |
| XP Reward | 16 |
| Gold Drop | 12 |

**Visual Description:** A seagull-like bird with dark storm-gray plumage and crackling Aether energy along its wings. Glowing white eyes.

**Overworld Behavior:** Flies in a circular pattern. Fast movement. Hard to avoid. Triggers on touch.

**Combat Behavior:** 60% Dive Attack (ATK+2 damage, always goes first). 30% basic peck. 10% Screech (reduces player DEF by 2 for the round).

**Special Moves:**
- Dive Attack: ATK+2, priority (always first regardless of SPD).
- Screech: Reduces target DEF by 2 for one round.

**Areas:** Cliff Path, Tidal Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Smoke Bomb | 10% |
| Nothing | 90% |

**Sprite Size:** 16x16 pixels

**Palette:** `#606870` (storm gray), `#A0A8B0` (light gray), `#F8F8F8` (white eyes/flash), `#2A2A30` (dark)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG storm bird enemy. Seagull-like bird with dark storm-gray plumage, crackling energy on wings, glowing white eyes. 4 directional flying sprites, 2 animation frames per direction (wing flap). GBC palette: #606870, #A0A8B0, #F8F8F8, #2A2A30. Clean pixel art, no anti-aliasing, indexed color."

---

### Tide Lurker

| Stat | Value |
|------|-------|
| ID | 7 |
| HP | 22 |
| ATK | 10 |
| DEF | 6 |
| SPD | 7 |
| XP Reward | 18 |
| Gold Drop | 14 |

**Visual Description:** A humanoid figure made of semi-transparent water, with dark seaweed-like strands throughout. Vaguely fish-like face. Drips constantly.

**Overworld Behavior:** Patrols near water areas in the Tidal Meridian. Rises from floor when player approaches (ambush-style). Triggers on touch.

**Combat Behavior:** 60% Tide Slam (basic attack). 30% Water Spray (ATK+2 damage, 20% chance to apply Slow). 10% Reform (heals self for 5 HP).

**Special Moves:**
- Water Spray: ATK+2, 20% slow chance.
- Reform: Self-heal 5 HP.

**Areas:** Tidal Meridian F1, Tidal Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal | 20% |
| Antidote | 15% |
| Nothing | 65% |

**Sprite Size:** 16x16 pixels

**Palette:** `#3A6A8A` (deep teal), `#80C0D0` (aqua), `#2A4050` (dark water), `#C0E0E8` (light foam)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG water elemental enemy. Humanoid figure made of semi-transparent water, dark seaweed strands throughout, vague fish-like face, dripping. 4 directional sprites, 2 animation frames (wobbling water form). GBC palette: #3A6A8A, #80C0D0, #2A4050, #C0E0E8. Clean pixel art, no anti-aliasing, indexed color."

---

### Aether Jellyfish

| Stat | Value |
|------|-------|
| ID | 8 |
| HP | 15 |
| ATK | 8 |
| DEF | 3 |
| SPD | 9 |
| XP Reward | 15 |
| Gold Drop | 11 |

**Visual Description:** A floating jellyfish made of translucent Aether. Bell-shaped top with trailing tentacles that crackle with energy. Soft blue-white glow.

**Overworld Behavior:** Drifts slowly in vertical patterns. Does not chase player. Triggers on touch.

**Combat Behavior:** 60% Tentacle Sting (basic attack, 15% poison chance). 30% Aether Discharge (ATK+3 magic damage to all party members). 10% drift (no action).

**Special Moves:**
- Tentacle Sting: Basic attack + 15% poison.
- Aether Discharge: ATK+3 magic damage to all party members.

**Areas:** Tidal Meridian F1, Tidal Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Antidote | 25% |
| Small Aether Crystal | 15% |
| Nothing | 60% |

**Sprite Size:** 16x16 pixels

**Palette:** `#D0E8F8` (pale ice blue), `#80A0D0` (medium blue), `#F8F8FF` (white glow), `#4060A0` (deep blue)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG jellyfish enemy. Translucent Aether jellyfish with bell-shaped top, trailing crackling tentacles, soft blue-white glow. 4 directional sprites, 2 animation frames (tentacles pulsing). GBC palette: #D0E8F8, #80A0D0, #F8F8FF, #4060A0. Clean pixel art, no anti-aliasing, indexed color."

---

## Region 3: Ashenveil Marsh Enemies

### Bog Rat

| Stat | Value |
|------|-------|
| ID | 9 |
| HP | 20 |
| ATK | 11 |
| DEF | 5 |
| SPD | 10 |
| XP Reward | 18 |
| Gold Drop | 12 |

**Visual Description:** An oversized rat with matted dark fur and glowing purple eyes. Patches of decayed skin are visible. Its tail is unnaturally long and segmented.

**Overworld Behavior:** Moves in quick, erratic patterns. Changes direction frequently. Fast. Triggers on touch.

**Combat Behavior:** 70% Gnaw (basic attack). 20% Plague Bite (ATK+1, 30% poison chance). 10% Skitter (increases SPD by 3 for the round).

**Special Moves:**
- Plague Bite: ATK+1, 30% poison.
- Skitter: +3 SPD for one round.

**Areas:** Ashenveil North Road, Outer Bog, Hollow Meridian Approach.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Antidote | 20% |
| Herbal Salve | 10% |
| Nothing | 70% |

**Sprite Size:** 16x16 pixels

**Palette:** `#4A3A4A` (dark purple-gray), `#8060A0` (purple), `#C0A080` (sickly tan), `#1A1A20` (near black)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG giant rat enemy. Oversized rat with matted dark fur, glowing purple eyes, patches of decayed skin, long segmented tail. 4 directional sprites, 2 animation frames (scurrying). GBC palette: #4A3A4A, #8060A0, #C0A080, #1A1A20. Clean pixel art, no anti-aliasing, indexed color."

---

### Rot Vine

| Stat | Value |
|------|-------|
| ID | 10 |
| HP | 25 |
| ATK | 12 |
| DEF | 4 |
| SPD | 3 |
| XP Reward | 20 |
| Gold Drop | 14 |

**Visual Description:** A cluster of dark green, decaying vines that have animated into a writhing mass. Small purple flowers dot the mass, and a central bulb pulses with sickly green light.

**Overworld Behavior:** Stationary. Appears as normal swamp vegetation until the player walks adjacent (1 tile away), then "springs" to life (ambush trigger). Cannot be avoided once triggered.

**Combat Behavior:** 50% Vine Lash (basic attack). 30% Entangle (skips player's next action — functionally a stun). 20% Toxic Spore (ATK+2, guaranteed poison).

**Special Moves:**
- Entangle: Stuns target for 1 round.
- Toxic Spore: ATK+2, guaranteed poison.

**Areas:** Ashenveil North Road, Outer Bog, Hollow Meridian F1.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Herbal Salve | 25% |
| Antidote | 20% |
| Nothing | 55% |

**Sprite Size:** 16x16 pixels

**Palette:** `#3A5A2A` (dark green), `#7A4A8A` (purple flower), `#80C060` (sickly green glow), `#1A2A1A` (very dark green)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG animated vine plant enemy. Writhing mass of dark green decaying vines with small purple flowers and central pulsing sickly green bulb. Stationary enemy with 2 animation frames (vines writhing), all 4 directions identical. GBC palette: #3A5A2A, #7A4A8A, #80C060, #1A2A1A. Clean pixel art, no anti-aliasing, indexed color."

---

### Decay Phantom

| Stat | Value |
|------|-------|
| ID | 11 |
| HP | 28 |
| ATK | 14 |
| DEF | 6 |
| SPD | 11 |
| XP Reward | 30 |
| Gold Drop | 22 |

**Visual Description:** A ghostly humanoid shape made of swirling purple-black mist with glowing white pinpoint eyes. Its form constantly shifts and decays, with pieces crumbling away and reforming.

**Overworld Behavior:** Drifts slowly through walls and obstacles (sprite moves over tiles the player can't cross). Rare spawn. Triggers on touch.

**Combat Behavior:** 50% Wither Touch (basic attack, 25% poison). 30% Decay Pulse (ATK+4 magic damage to all party members). 20% Phase (becomes immune to next attack — dodge state).

**Special Moves:**
- Wither Touch: Basic attack + 25% poison.
- Decay Pulse: ATK+4 magic damage to all targets.
- Phase: Immune to next attack (dodge).

**Areas:** Outer Bog (rare), Architect Ruins, Hollow Meridian F2, Chronospire F3.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal | 30% |
| Herbal Salve | 15% |
| Nothing | 55% |

**Sprite Size:** 16x16 pixels

**Palette:** `#4A2A5A` (dark purple), `#8A60A0` (medium purple), `#F0F0F0` (white eyes), `#1A0A1A` (near black)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG ghost phantom enemy. Ghostly humanoid shape of swirling purple-black mist, pinpoint white eyes, form constantly shifting and crumbling. 4 directional sprites, 2 animation frames (swirling mist, form shifting). GBC palette: #4A2A5A, #8A60A0, #F0F0F0, #1A0A1A. Clean pixel art, no anti-aliasing, indexed color."

---

### Fungal Creep

| Stat | Value |
|------|-------|
| ID | 12 |
| HP | 22 |
| ATK | 10 |
| DEF | 7 |
| SPD | 5 |
| XP Reward | 20 |
| Gold Drop | 15 |

**Visual Description:** A short, waddling mushroom creature with a spotted purple cap, stubby legs, and beady dark eyes. Trails spore clouds behind it.

**Overworld Behavior:** Slow patrol in small areas. Leaves a trail of spore particles (cosmetic). Triggers on touch.

**Combat Behavior:** 60% Headbutt (basic attack). 30% Spore Cloud (ATK+2, 30% poison to all targets). 10% Hunker Down (+3 DEF for one round).

**Special Moves:**
- Spore Cloud: ATK+2, 30% poison to all party members.
- Hunker Down: +3 DEF for one round.

**Areas:** Hollow Meridian F1, Hollow Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Antidote | 30% |
| Herbal Salve | 15% |
| Nothing | 55% |

**Sprite Size:** 16x16 pixels

**Palette:** `#6A3A7A` (purple cap), `#C090C0` (light purple spots), `#A09060` (tan body), `#2A1A2A` (dark)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG mushroom creature enemy. Short waddling mushroom with spotted purple cap, stubby legs, beady dark eyes, trailing spore cloud particles. 4 directional sprites, 2 animation frames (wobbling walk). GBC palette: #6A3A7A, #C090C0, #A09060, #2A1A2A. Clean pixel art, no anti-aliasing, indexed color."

---

## Region 4: Crystalfall Desert Enemies

### Sand Sentinel

| Stat | Value |
|------|-------|
| ID | 13 |
| HP | 30 |
| ATK | 14 |
| DEF | 10 |
| SPD | 6 |
| XP Reward | 28 |
| Gold Drop | 20 |

**Visual Description:** A humanoid figure made of compacted sand and crystallized Aether shards. Angular, armored appearance with glowing cyan lines tracing its body. Frozen in mid-stride until activated by Edyn's time bubble.

**Overworld Behavior:** Completely still until the player comes within 3 tiles. Edyn's time bubble "unfreezes" it, and it immediately patrols toward the player. Moderate speed. Triggers on touch.

**Combat Behavior:** 60% Sand Strike (basic attack). 30% Crystal Spike (ATK+4, pierces 25% of DEF). 10% Petrify Gaze (30% chance to stun target for 1 round).

**Special Moves:**
- Crystal Spike: ATK+4, ignores 25% of target DEF.
- Petrify Gaze: 30% stun chance.

**Areas:** Crystalfall Border, Frozen Expanse.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal | 25% |
| Hi-Potion | 15% |
| Nothing | 60% |

**Sprite Size:** 16x16 pixels

**Palette:** `#D8D0B0` (sand), `#60C8D0` (cyan crystal lines), `#F0E8D0` (light sand), `#4A4030` (dark sand)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG sand golem sentinel enemy. Humanoid figure of compacted sand with crystallized cyan Aether shards embedded, angular armored appearance, glowing cyan lines. 4 directional sprites, 2 animation frames (heavy stepping walk). GBC palette: #D8D0B0, #60C8D0, #F0E8D0, #4A4030. Clean pixel art, no anti-aliasing, indexed color."

---

### Crystal Scarab

| Stat | Value |
|------|-------|
| ID | 14 |
| HP | 20 |
| ATK | 12 |
| DEF | 8 |
| SPD | 12 |
| XP Reward | 24 |
| Gold Drop | 18 |

**Visual Description:** A scarab beetle made entirely of crystallized Aether, with a translucent body that refracts light into rainbow spectra. Fast-moving with sharp crystal legs.

**Overworld Behavior:** Fast patrol. Moves quickly in diagonal patterns near crystal formations. Hard to avoid. Triggers on touch.

**Combat Behavior:** 60% Crystal Bite (basic attack). 30% Refract (creates a "mirror image" — next attack against it has 50% miss chance). 10% Shatter Burst (ATK+5, but scarab takes 5 recoil damage).

**Special Moves:**
- Refract: 50% dodge chance for next incoming attack.
- Shatter Burst: ATK+5, self-damage 5 HP.

**Areas:** Frozen Expanse, Crystal Canyon, Prism Meridian F1.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal | 30% |
| Small Aether Crystal | 20% |
| Nothing | 50% |

**Sprite Size:** 16x16 pixels

**Palette:** `#E0F0F8` (ice white crystal), `#80D0E0` (cyan), `#D0A0E0` (prismatic purple), `#4060A0` (deep crystal blue)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG crystal scarab beetle enemy. Scarab made of translucent crystallized Aether, refracting rainbow light, sharp crystal legs, fast. 4 directional sprites, 2 animation frames (scurrying). GBC palette: #E0F0F8, #80D0E0, #D0A0E0, #4060A0. Clean pixel art, no anti-aliasing, indexed color."

---

### Prism Wisp

| Stat | Value |
|------|-------|
| ID | 15 |
| HP | 18 |
| ATK | 13 |
| DEF | 4 |
| SPD | 14 |
| XP Reward | 26 |
| Gold Drop | 16 |

**Visual Description:** Similar to the Aether Wisp but larger and multicolored — cycles through red, blue, green, and white, leaving a prismatic trail. More aggressive appearance with sharper energy edges.

**Overworld Behavior:** Fast circular patrol around crystal formations. Aggressive — moves toward player when within 4 tiles. Triggers on touch.

**Combat Behavior:** 50% Prism Bolt (ATK+3 magic damage). 30% basic attack. 20% Split (creates a decoy; next attack targeting the Wisp has 50% chance to hit the decoy instead, wasting the turn).

**Special Moves:**
- Prism Bolt: ATK+3 magic damage.
- Split: 50% dodge via decoy for next attack.

**Areas:** Crystal Canyon, Prism Meridian F1, Prism Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal (Large) | 15% |
| Small Aether Crystal | 25% |
| Nothing | 60% |

**Sprite Size:** 16x16 pixels

**Palette:** `#E0A0A0` (prismatic red), `#A0E0A0` (prismatic green), `#A0A0E0` (prismatic blue), `#F8F8F8` (white core)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG prismatic energy wisp enemy. Larger energy orb cycling through rainbow colors (red, green, blue, white), sharp energy edges, prismatic trail. 4 directional sprites, 2 animation frames (color cycling pulse). GBC palette: #E0A0A0, #A0E0A0, #A0A0E0, #F8F8F8. Clean pixel art, no anti-aliasing, indexed color."

---

### Refracted Shard

| Stat | Value |
|------|-------|
| ID | 16 |
| HP | 24 |
| ATK | 11 |
| DEF | 9 |
| SPD | 8 |
| XP Reward | 22 |
| Gold Drop | 17 |

**Visual Description:** A floating angular crystal shard, roughly diamond-shaped, with jagged edges and an inner glow. Rotates slowly in place.

**Overworld Behavior:** Stationary, hovering near crystal walls. Activates when player approaches. Triggers on touch.

**Combat Behavior:** 60% Shard Fling (basic attack). 30% Refraction Beam (ATK+4 magic damage). On defeat: splits into 2 Mini Shards (each with 8 HP, 6 ATK, 2 DEF, 6 SPD).

**Special Moves:**
- Refraction Beam: ATK+4 magic damage.
- Split on Death: Spawns 2 Mini Shards.

**Areas:** Prism Meridian F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal | 35% |
| Nothing | 65% |

**Sprite Size:** 16x16 pixels

**Palette:** `#C0D8E8` (pale crystal), `#60A0C0` (blue crystal), `#F8F0E0` (warm inner glow), `#304060` (dark crystal)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG floating crystal shard enemy. Angular diamond-shaped crystal with jagged edges, inner warm glow, slowly rotating. 4 directional sprites (identical, rotation frames), 2 animation frames. GBC palette: #C0D8E8, #60A0C0, #F8F0E0, #304060. Clean pixel art, no anti-aliasing, indexed color."

---

## Region 5: Ironpeak Mountains Enemies

### Mountain Wolf

| Stat | Value |
|------|-------|
| ID | 17 |
| HP | 28 |
| ATK | 15 |
| DEF | 7 |
| SPD | 13 |
| XP Reward | 30 |
| Gold Drop | 20 |

**Visual Description:** A large wolf with thick gray-white fur, piercing amber eyes, and frost-coated snout. Lean and muscular, clearly adapted to mountain cold.

**Overworld Behavior:** Patrols in wide arcs. Fast movement. Chases player when within 3 tiles. Triggers on touch.

**Combat Behavior:** 60% Fang Strike (basic attack). 30% Howl (buffs own ATK by +3 for 2 rounds). 10% Pack Instinct (if second wolf on map, both are fought simultaneously — rare double encounter).

**Special Moves:**
- Fang Strike: Standard physical.
- Howl: Self-buff ATK+3 for 2 rounds.

**Areas:** Ironpeak Mountain Pass.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Hi-Potion | 20% |
| Warm Cloak | 5% (rare) |
| Nothing | 75% |

**Sprite Size:** 16x16 pixels

**Palette:** `#A0A8B0` (gray-white fur), `#D0A040` (amber eyes), `#E0E0E8` (frost/highlight), `#3A3A40` (dark gray)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG mountain wolf enemy. Large wolf with thick gray-white fur, piercing amber eyes, frost on snout, lean muscular build. 4 directional sprites, 2 animation frames (loping run). GBC palette: #A0A8B0, #D0A040, #E0E0E8, #3A3A40. Clean pixel art, no anti-aliasing, indexed color."

---

### Frost Golem

| Stat | Value |
|------|-------|
| ID | 18 |
| HP | 45 |
| ATK | 14 |
| DEF | 16 |
| SPD | 3 |
| XP Reward | 40 |
| Gold Drop | 30 |

**Visual Description:** A large humanoid figure made of ice-covered rock, with Aether crystal veins running through its body. Massive fists, slow and imposing. Frost constantly radiates from it.

**Overworld Behavior:** Very slow patrol. Easy to avoid. Triggers on touch.

**Combat Behavior:** 40% Frost Smash (ATK+5, slow but devastating). 30% basic attack. 20% Ice Armor (raises own DEF by +5 for 2 rounds). 10% Frozen Ground (reduces all party SPD by 3 for 2 rounds).

**Special Moves:**
- Frost Smash: ATK+5 heavy physical.
- Ice Armor: +5 DEF for 2 rounds.
- Frozen Ground: -3 SPD to all party members for 2 rounds.

**Areas:** Ironpeak Mountain Pass.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal (Large) | 25% |
| Hi-Potion | 20% |
| Architect Alloy | 5% (rare) |
| Nothing | 50% |

**Sprite Size:** 16x16 pixels

**Palette:** `#A0C0D0` (ice blue), `#D0E8F0` (frost white), `#607080` (dark rock), `#60C8D0` (Aether cyan veins)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG ice golem enemy. Large humanoid of ice-covered rock with Aether crystal veins, massive fists, frost radiating from body, slow and imposing. 4 directional sprites, 2 animation frames (slow heavy step). GBC palette: #A0C0D0, #D0E8F0, #607080, #60C8D0. Clean pixel art, no anti-aliasing, indexed color."

---

## Region 6: Chronospire Enemies

### Temporal Shade

| Stat | Value |
|------|-------|
| ID | 19 |
| HP | 35 |
| ATK | 16 |
| DEF | 8 |
| SPD | 12 |
| XP Reward | 40 |
| Gold Drop | 25 |

**Visual Description:** A humanoid silhouette made of dark indigo energy, with a cracked clock face hovering where its head should be. Hands end in elongated claw-like points. Moves with jerky, time-skipping animations.

**Overworld Behavior:** Teleports short distances (2–3 tiles) every few seconds. Unpredictable patrol. Triggers on touch.

**Combat Behavior:** 50% Chrono Slash (basic attack + 15% slow). 30% Time Skip (teleports behind the party for guaranteed hit, ATK+3). 20% Temporal Drain (drains 5 MP from target, heals self 5 HP).

**Special Moves:**
- Chrono Slash: Basic attack, 15% slow.
- Time Skip: Guaranteed hit ATK+3.
- Temporal Drain: -5 MP to target, +5 HP to self.

**Areas:** Chronospire F1, F2, F4.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Aether Crystal (Large) | 25% |
| Mega Potion | 15% |
| Nothing | 60% |

**Sprite Size:** 16x16 pixels

**Palette:** `#2A2A5A` (dark indigo), `#6060A0` (medium indigo), `#C0C0D0` (cracked clock face), `#F0F0F0` (white clock hands)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG temporal shadow creature enemy. Dark indigo humanoid silhouette with cracked clock face for head, elongated claw hands, jerky time-glitch animation. 4 directional sprites, 2 animation frames (glitchy teleport flicker). GBC palette: #2A2A5A, #6060A0, #C0C0D0, #F0F0F0. Clean pixel art, no anti-aliasing, indexed color."

---

### Aether Construct

| Stat | Value |
|------|-------|
| ID | 20 |
| HP | 40 |
| ATK | 15 |
| DEF | 12 |
| SPD | 7 |
| XP Reward | 45 |
| Gold Drop | 28 |

**Visual Description:** An angular clockwork automaton built by the Architects. Pristine brass and silver, unlike the corroded versions in the Verdant Meridian. Geometric precision, glowing Aether conduits, and functional joints. A small holographic projection of the Chronospire logo hovers above its head.

**Overworld Behavior:** Patrols fixed paths within the Chronospire. Does not deviate. Triggers on touch.

**Combat Behavior:** 50% Precision Strike (basic attack, never misses). 30% Aether Beam (ATK+5 magic damage). 20% Repair Protocol (heals self 10 HP if below 50% HP; otherwise uses basic attack instead).

**Special Moves:**
- Precision Strike: Guaranteed hit.
- Aether Beam: ATK+5 magic damage.
- Repair Protocol: Self-heal 10 HP (conditional).

**Areas:** Chronospire F1, F3, F4.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Mega Potion | 20% |
| Aether Crystal (Large) | 20% |
| Architect Alloy | 10% |
| Nothing | 50% |

**Sprite Size:** 16x16 pixels

**Palette:** `#C0A840` (polished brass), `#D0D0D8` (silver), `#80C0E0` (Aether blue conduits), `#3A3020` (dark joint)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG clockwork automaton enemy. Angular pristine brass-and-silver construct, geometric precision, glowing blue Aether conduits, small holographic symbol above head. 4 directional sprites, 2 animation frames (precise mechanical walk). GBC palette: #C0A840, #D0D0D8, #80C0E0, #3A3020. Clean pixel art, no anti-aliasing, indexed color."

---

### Loop Wraith

| Stat | Value |
|------|-------|
| ID | 21 |
| HP | 30 |
| ATK | 18 |
| DEF | 5 |
| SPD | 16 |
| XP Reward | 45 |
| Gold Drop | 25 |

**Visual Description:** A translucent, looping ghostly figure — appears to be the same entity repeated in a time loop, with 2–3 overlapping "copies" of itself slightly offset. The copies flicker in and out. Deep blue-purple color with white trailing edges.

**Overworld Behavior:** Teleports frequently, appearing and disappearing. Hard to track or avoid. Only found on Chronospire F2 (Looping Corridors). Triggers on touch.

**Combat Behavior:** 40% Loop Strike (attacks twice in one turn at half damage each). 30% Phase Shift (fully dodges next attack). 20% Temporal Rip (ATK+6, heavy damage). 10% Reset (restores own HP to 50% of max — can only do this once per fight).

**Special Moves:**
- Loop Strike: Two hits at 50% damage each.
- Phase Shift: Dodge next attack.
- Temporal Rip: ATK+6 heavy damage.
- Reset: Restore own HP to 50% (once per fight).

**Areas:** Chronospire F2.

**Loot Table:**

| Item | Drop Chance |
|------|-------------|
| Temporal Ring | 5% (rare) |
| Aether Crystal (Large) | 30% |
| Nothing | 65% |

**Sprite Size:** 16x16 pixels

**Palette:** `#3030A0` (deep blue-purple), `#6060C0` (medium purple), `#E0E0F8` (white trail), `#101030` (near black)

**Pixel Art Generation Prompt — Spritesheet:**

> "16x16 pixel art spritesheet for a Game Boy Color RPG time-loop ghost enemy. Translucent ghostly figure with 2-3 overlapping time-loop copies slightly offset, flickering. Deep blue-purple with white trailing edges. 4 directional sprites, 2 animation frames (copies phasing in/out). GBC palette: #3030A0, #6060C0, #E0E0F8, #101030. Clean pixel art, no anti-aliasing, indexed color."

---

## Complete Enemy Stats Summary Table

| ID | Name | HP | ATK | DEF | SPD | XP | Gold | Region |
|----|------|----|-----|-----|-----|----|------|--------|
| 1 | Aether Wisp | 10 | 5 | 2 | 8 | 8 | 5 | Verdant Reach |
| 2 | Temporal Beetle | 14 | 7 | 5 | 6 | 10 | 7 | Verdant Reach |
| 3 | Gear Sprite | 16 | 8 | 6 | 7 | 14 | 10 | Verdant Meridian |
| 4 | Corroded Automaton | 30 | 11 | 9 | 4 | 25 | 18 | Verdant Meridian |
| 5 | Coastal Crab | 18 | 9 | 8 | 5 | 14 | 10 | Stormhaven Coast |
| 6 | Storm Gull | 12 | 10 | 3 | 14 | 16 | 12 | Stormhaven Coast |
| 7 | Tide Lurker | 22 | 10 | 6 | 7 | 18 | 14 | Tidal Meridian |
| 8 | Aether Jellyfish | 15 | 8 | 3 | 9 | 15 | 11 | Tidal Meridian |
| 9 | Bog Rat | 20 | 11 | 5 | 10 | 18 | 12 | Ashenveil Marsh |
| 10 | Rot Vine | 25 | 12 | 4 | 3 | 20 | 14 | Ashenveil Marsh |
| 11 | Decay Phantom | 28 | 14 | 6 | 11 | 30 | 22 | Ashenveil Marsh |
| 12 | Fungal Creep | 22 | 10 | 7 | 5 | 20 | 15 | Hollow Meridian |
| 13 | Sand Sentinel | 30 | 14 | 10 | 6 | 28 | 20 | Crystalfall Desert |
| 14 | Crystal Scarab | 20 | 12 | 8 | 12 | 24 | 18 | Crystalfall Desert |
| 15 | Prism Wisp | 18 | 13 | 4 | 14 | 26 | 16 | Prism Meridian |
| 16 | Refracted Shard | 24 | 11 | 9 | 8 | 22 | 17 | Prism Meridian |
| 17 | Mountain Wolf | 28 | 15 | 7 | 13 | 30 | 20 | Ironpeak Mountains |
| 18 | Frost Golem | 45 | 14 | 16 | 3 | 40 | 30 | Ironpeak Mountains |
| 19 | Temporal Shade | 35 | 16 | 8 | 12 | 40 | 25 | Chronospire |
| 20 | Aether Construct | 40 | 15 | 12 | 7 | 45 | 28 | Chronospire |
| 21 | Loop Wraith | 30 | 18 | 5 | 16 | 45 | 25 | Chronospire |

---

*Chronospire: The Shattered Meridian — Enemies Document*
