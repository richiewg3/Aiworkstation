# 04 — World Map and Areas

---

## Overworld Map Description

The world of Aethermere is laid out as a crescent-shaped continent curving around the Stillwater Basin, an inland sea. The Chronospire sits on a solitary island at the center of the Basin. Five regions radiate outward from the Basin, connected by roads, mountain passes, and coastal paths. The player navigates between regions via overworld map scenes that connect towns, dungeons, and landmarks.

**Top-Down Layout (North is up):**

```
                 [Ashenveil Marsh]
                  /            \
    [Stormhaven Coast]    [Ironpeak Mountains]
          \                    /
      [Stillwater Basin -- Chronospire Island]
          /                    \
    [Verdant Reach]      [Crystalfall Desert]
        (START)
```

The player begins in the Verdant Reach (south) and progresses clockwise: Stormhaven Coast (west), Ashenveil Marsh (north), Crystalfall Desert (east), Ironpeak Mountains (northeast), then to the Chronospire (center). Overworld travel is handled through connected map scenes, not a freely navigable world map. Each region has 1–2 overworld connector scenes linking it to adjacent regions.

---

## Complete Scene List

### Region 1: The Verdant Reach

---

#### Scene: Millhaven — Town Square

| Property | Detail |
|----------|--------|
| Scene Name | `millhaven_town_square` |
| Type | Town |
| Size | 32x32 tiles (256x256 px) |
| Visual Theme | Warm autumnal village. Cobblestone paths, thatched roofs, golden-leaved trees, small market stalls. |
| Atmosphere | Cozy, familiar, safe — the player's home. Post-Shattering: patches of decay/renewal visible. |
| Tileset | Verdant Town Tileset |
| Connections | N: Millhaven North Road, E: Alaric's Workshop (door), W: Wynn's Shop (door), S: Millhaven South Gate |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Bram | Center square near well | Tutorial dialogue, gives Alaric's Wrench on return visit |
| Wynn (Shopkeeper) | Inside shop (door west) | General goods shop |
| Farmer Hest | Southeast corner near crops | Flavor dialogue, comments on time distortion |
| Old Maren | Northwest near herb garden | Lore about the Shattering's effect on plants |
| Council Elder Doss | Town hall steps (north) | Story gate — asks Edyn to continue after Act 1 |

**Enemy Encounters:** None (safe zone).

**Key Items/Events:**
- Opening cutscene triggers here (the Shattering)
- Alaric's Wrench obtained from Bram on return visit
- Save point at the town well (interact to save)

**Scripted Cutscene Triggers:**
- Game start: Shattering sequence (screen shake, palette swap, NPC panic)
- Post-Verdant Meridian: Council plea cutscene

---

#### Scene: Alaric's Workshop (Interior)

| Property | Detail |
|----------|--------|
| Scene Name | `alaric_workshop` |
| Type | Indoor |
| Size | 20x18 tiles (160x144 px — single screen) |
| Visual Theme | Cluttered clockmaker's shop. Workbenches covered in gears, tools on walls, clocks everywhere. |
| Atmosphere | Intimate, nostalgic. The clocks all stopped after the Shattering. |
| Tileset | Verdant Interior Tileset |
| Connections | Door → Millhaven Town Square |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| (None after game start) | — | — |

**Key Items/Events:**
- Pocket Watch obtained from workbench (story start)
- Alaric's Travel Pack obtained from wall hook
- Examining clocks gives flavor text about Alaric
- Alaric's Note on desk — foreshadows Chronospire visit

---

#### Scene: Wynn's General Store (Interior)

| Property | Detail |
|----------|--------|
| Scene Name | `wynns_shop` |
| Type | Indoor (Shop) |
| Size | 20x18 tiles (160x144 px) |
| Visual Theme | Cozy shop with shelves of goods, barrels, a counter with Wynn behind it. |
| Tileset | Verdant Interior Tileset |
| Connections | Door → Millhaven Town Square |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Wynn | Behind counter (center-north) | Shop: Potions, Antidotes, basic gear |

**Key Items/Events:**
- Shop menu triggered by talking to Wynn
- Post-Shattering: some shelves show aged/fresh items (visual detail)

---

#### Scene: Verdant Reach — South Road

| Property | Detail |
|----------|--------|
| Scene Name | `verdant_south_road` |
| Type | Overworld |
| Size | 32x28 tiles (256x224 px) |
| Visual Theme | Dirt road through golden-leaved forest, fallen leaves on ground, wooden fences along path. |
| Atmosphere | Peaceful but with visible time distortion — trees in different seasons simultaneously. |
| Tileset | Verdant Overworld Tileset |
| Connections | N: Millhaven South Gate, S: Oakwatch Grove Entrance |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Traveling Merchant | Center of road | Sells basic potions (early game convenience) |

**Enemy Encounters:**
- Aether Wisp (patrol, 2 on map)
- Temporal Beetle (random patrol, 1 on map)

**Key Items/Events:**
- Chest near path edge: 50 Gold
- Combat tutorial trigger (first Aether Wisp encounter)

---

#### Scene: Oakwatch Grove — Entrance

| Property | Detail |
|----------|--------|
| Scene Name | `oakwatch_grove_entrance` |
| Type | Overworld |
| Size | 32x32 tiles (256x256 px) |
| Visual Theme | Ancient oak forest, massive trees with golden canopy, stone path leading to a moss-covered clock tower. |
| Atmosphere | Reverent, ancient. The Verdant Meridian is visible in the background, its clock face cracked. |
| Tileset | Verdant Overworld Tileset |
| Connections | N: Verdant South Road, S: Verdant Meridian Entrance (door) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Keeper Serea | In front of Meridian entrance | Quest giver: Retrieve Calibration Key, gives Meridian Compass after |
| Lira | Near grove campfire (east) | Introduces herself, joins party after talking to Serea |

**Enemy Encounters:**
- Aether Wisp (patrol, 1)
- Temporal Beetle (patrol, 1)

**Key Items/Events:**
- Lira joins party
- Meridian Compass obtained after dungeon completion
- Save point at campfire

---

#### Scene: Verdant Meridian — Floor 1

| Property | Detail |
|----------|--------|
| Scene Name | `verdant_meridian_f1` |
| Type | Dungeon |
| Size | 32x32 tiles (256x256 px) |
| Visual Theme | Clock tower interior. Massive gears on walls, stone floors with brass inlays, greenish ambient light from Aether conduits. |
| Atmosphere | Mechanical, rhythmic. Faint ticking echoes. Aether-warped creatures lurk in shadows. |
| Tileset | Meridian Dungeon Tileset |
| Connections | N: Verdant Meridian F2 (stairs up), S: Oakwatch Grove Entrance (door) |

**NPCs:** None.

**Enemy Encounters:**
- Gear Sprite (2 patrols)
- Aether Wisp (1 patrol)

**Key Items/Events:**
- Chest: Small Aether Crystal (restores 10 MP)
- Gear puzzle: Rotate gear to open north passage

---

#### Scene: Verdant Meridian — Floor 2

| Property | Detail |
|----------|--------|
| Scene Name | `verdant_meridian_f2` |
| Type | Dungeon |
| Size | 32x32 tiles (256x256 px) |
| Visual Theme | Deeper tower interior. Larger gears, some spinning. Time-dilated rooms (screen tint changes). |
| Tileset | Meridian Dungeon Tileset |
| Connections | S: Verdant Meridian F1 (stairs down), N: Verdant Meridian Vault (door) |

**NPCs:** None.

**Enemy Encounters:**
- Gear Sprite (2)
- Corroded Automaton (1 — miniboss-tier enemy)

**Key Items/Events:**
- Chest: Iron Cog (key item, opens vault door)
- Time-dilation puzzle: Room where player moves at half speed, requiring careful pathing around enemies

---

#### Scene: Verdant Meridian — Vault (Boss Room)

| Property | Detail |
|----------|--------|
| Scene Name | `verdant_meridian_vault` |
| Type | Dungeon (Boss Arena) |
| Size | 20x18 tiles (160x144 px — single screen) |
| Visual Theme | Circular vault chamber, massive cracked clock face on back wall, Calibration Key on a pedestal at center. |
| Atmosphere | Tense, mechanical. The Corroded Timekeeper blocks the way. |
| Tileset | Meridian Dungeon Tileset |
| Connections | S: Verdant Meridian F2 (door, locked during fight) |

**NPCs:** None.

**Enemy Encounters:**
- **Boss: Corroded Timekeeper** — triggers when player approaches pedestal

**Key Items/Events:**
- Calibration Key obtained after boss defeat
- Keeper Fragment 1 (Verdant) — hidden in alcove, requires examining the cracked clock face after boss fight

---

#### Scene: Verdant Reach — West Road

| Property | Detail |
|----------|--------|
| Scene Name | `verdant_west_road` |
| Type | Overworld (Connector) |
| Size | 32x28 tiles |
| Visual Theme | Road transitioning from golden forest to coastal scrubland. Trees thin out, grass becomes windswept. |
| Tileset | Verdant Overworld Tileset (blending to Stormhaven tiles at edge) |
| Connections | E: Millhaven South Gate, W: Stormhaven Approach |

**Enemy Encounters:**
- Aether Wisp (1)
- Coastal Crab (1 — first Stormhaven-region enemy preview)

**Key Items/Events:**
- Chest: Potion
- Signpost with directions

---

### Region 2: The Stormhaven Coast

---

#### Scene: Stormhaven — Town Center

| Property | Detail |
|----------|--------|
| Scene Name | `stormhaven_town` |
| Type | Town |
| Size | 32x32 tiles (256x256 px) |
| Visual Theme | Cliff-side fishing town. Stone buildings with slate roofs, boardwalks, rope bridges, harbor visible below. Rain effects (sprite-based rain overlays). |
| Atmosphere | Grim resilience. The looping storm has worn the townsfolk down but not broken them. Periodic storm flashes. |
| Tileset | Stormhaven Town Tileset |
| Connections | N: Harbor District (scene transition), E: Stormhaven Approach (overworld), W: Cliff Path to Tidal Meridian |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Captain Maren | Center near message board | Story dialogue, grants passage after Meridian fix |
| Fisherman Garl | South near docks overlook | Side quest: Stormhaven Fishing Quest |
| Storm-Watcher Nessa | Northeast rooftop (accessible via ladder) | Lore about the storm loop timing |
| Stormhaven Shopkeeper (Tully) | Inside shop (door east) | Combat supplies, storm-themed items |

**Enemy Encounters:** None (safe zone).

**Key Items/Events:**
- Storm loop visual/audio event every ~60 seconds of real time (screen flash, brief rain intensification)
- Save point at message board
- Side quest: Storm Fishing (catch a Loopfin during storm phase)

---

#### Scene: Stormhaven — Harbor District

| Property | Detail |
|----------|--------|
| Scene Name | `stormhaven_harbor` |
| Type | Town (sub-area) |
| Size | 32x28 tiles |
| Visual Theme | Lower cliff level. Wooden docks, moored ships rocking, warehouse buildings, crates and barrels. |
| Tileset | Stormhaven Town Tileset |
| Connections | S: Stormhaven Town Center, N: Harbor Warehouse (door) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Pip | Inside warehouse (see below) | Lira's subplot resolution |
| Sailor Wendt | Near docked ship | Flavor dialogue about the storm |

**Key Items/Events:**
- Pip is found inside the warehouse after entering
- Chest on dock: 100 Gold

---

#### Scene: Stormhaven — Harbor Warehouse (Interior)

| Property | Detail |
|----------|--------|
| Scene Name | `stormhaven_warehouse` |
| Type | Indoor |
| Size | 20x18 tiles |
| Visual Theme | Dark, damp warehouse interior. Crates stacked high, lantern light, rain audible through walls. |
| Tileset | Stormhaven Interior Tileset |
| Connections | Door → Harbor District |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Pip | Center, crouching behind crates | Lira's brother — subplot cutscene |

**Key Items/Events:**
- Lira/Pip reunion cutscene triggers automatically on entry
- Chest: Storm Lantern (key item, used to navigate the Tidal Meridian's dark rooms)

---

#### Scene: Cliff Path to Tidal Meridian

| Property | Detail |
|----------|--------|
| Scene Name | `cliff_path_tidal` |
| Type | Overworld |
| Size | 32x28 tiles |
| Visual Theme | Narrow cliff path above crashing waves. Wet stone, sea spray, precarious wooden bridges. |
| Atmosphere | Dangerous, exposed. Storm effects at full intensity during storm phase. |
| Tileset | Stormhaven Overworld Tileset |
| Connections | E: Stormhaven Town Center, W: Tidal Meridian Entrance |

**Enemy Encounters:**
- Coastal Crab (2 patrol)
- Storm Gull (1 patrol — attacks from above, higher SPD)

**Key Items/Events:**
- Path is blocked during storm phase. Player must wait for calm phase (triggered by timer or interacting with a wind-gauge).
- Chest: Sailor's Charm (accessory, +2 DEF)

---

#### Scene: Tidal Meridian — Floor 1

| Property | Detail |
|----------|--------|
| Scene Name | `tidal_meridian_f1` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Stone tower with water-logged floors. Tide pools, barnacle-encrusted walls, channeled water flows. Aquatic blue-green lighting. |
| Tileset | Tidal Dungeon Tileset |
| Connections | E: Cliff Path (door), N: Tidal Meridian F2 (stairs) |

**Enemy Encounters:**
- Tide Lurker (2 patrol)
- Aether Jellyfish (1 patrol)

**Key Items/Events:**
- Rising water mechanic: Water level changes on a timer, opening/closing passages
- Chest: Aether Crystal (restores 15 MP)
- Storm Lantern used to light dark corridors

---

#### Scene: Tidal Meridian — Floor 2

| Property | Detail |
|----------|--------|
| Scene Name | `tidal_meridian_f2` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Upper tower. Massive water wheels, channeled torrents, observation windows showing the storm outside. |
| Tileset | Tidal Dungeon Tileset |
| Connections | S: Tidal Meridian F1, N: Tidal Meridian Sanctum (boss) |

**Enemy Encounters:**
- Tide Lurker (1)
- Storm Gull (1)
- Aether Jellyfish (2)

**Key Items/Events:**
- Water wheel puzzle: Redirect water flow to raise a platform
- Chest: Wave Conduit (weapon for Edyn, +5 ATK, enables Tidal Slash ability)

---

#### Scene: Tidal Meridian — Sanctum (Boss Room)

| Property | Detail |
|----------|--------|
| Scene Name | `tidal_meridian_sanctum` |
| Type | Dungeon (Boss Arena) |
| Size | 20x18 tiles (single screen) |
| Visual Theme | Central Meridian chamber. The Tidal Core hovers above a basin of swirling water. Keeper Corwin stands before it. |
| Tileset | Tidal Dungeon Tileset |
| Connections | S: Tidal Meridian F2 (locked during fight) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Keeper Corwin | Center, before the Core | Mini-boss encounter |

**Key Items/Events:**
- **Boss: Keeper Corwin** — non-lethal fight (Corwin collapses at 0 HP, is not killed)
- Post-fight: Pocket watch stabilization cutscene
- Tideborn Relic obtained
- Keeper Fragment 2 (Tidal) — given by Corwin if player speaks to him again after restoration

---

### Region 3: The Ashenveil Marsh

---

#### Scene: Ashenveil Marsh — North Road

| Property | Detail |
|----------|--------|
| Scene Name | `ashenveil_north_road` |
| Type | Overworld (Connector) |
| Size | 32x28 tiles |
| Visual Theme | Transition from coastal scrub to murky swampland. Fog rolls in, trees become gnarled and draped in moss. |
| Tileset | Ashenveil Overworld Tileset |
| Connections | S: Stormhaven North Path, N: Ashenveil Marsh — Outer Bog |

**Enemy Encounters:**
- Bog Rat (2 patrol)
- Rot Vine (1 stationary — ambush when approached)

**Key Items/Events:**
- Rook encounter: he is fighting off Bog Rats when the player arrives. Cutscene introduces him, he joins the party.

---

#### Scene: Ashenveil Marsh — Outer Bog

| Property | Detail |
|----------|--------|
| Scene Name | `ashenveil_outer_bog` |
| Type | Overworld |
| Size | 32x32 tiles |
| Visual Theme | Dense swamp. Murky water, twisted trees, floating debris, patches of sickly green light. Accelerated decay visible — structures aging in real time. |
| Atmosphere | Oppressive, uneasy. Music is sparse and ambient. |
| Tileset | Ashenveil Overworld Tileset |
| Connections | S: Ashenveil North Road, N: Architect Ruins, E: Hollow Meridian Approach |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Lost Traveler | Southwest corner | Side quest: Guide them back to the road for a reward |

**Enemy Encounters:**
- Bog Rat (2)
- Rot Vine (2)
- Decay Phantom (1 — rare, high XP)

**Key Items/Events:**
- Chest: Herbal Salve (consumable, heals 30 HP)
- Environmental hazard: Decay patches that damage the player if stood on (lose 5 HP per step)

---

#### Scene: Architect Ruins

| Property | Detail |
|----------|--------|
| Scene Name | `architect_ruins` |
| Type | Overworld (Landmark) |
| Size | 32x28 tiles |
| Visual Theme | Crumbling stone structures from the Architect civilization. Murals and tablets on walls, overgrown with marsh vegetation. Eerie beauty. |
| Tileset | Ashenveil Overworld Tileset + Ruins tile additions |
| Connections | S: Outer Bog, (no other exits — dead end with lore) |

**NPCs:** None.

**Enemy Encounters:**
- Decay Phantom (1)

**Key Items/Events:**
- Lore tablets (3 interactable): Tell fragments of Architect history
- Hidden chest behind crumbling wall: Architect Alloy (crafting material for Ironpeak)
- Rook's side quest evidence: Document in ruins proves Haldric sent bad intel (interactable scroll)

---

#### Scene: Hollow Meridian — Approach

| Property | Detail |
|----------|--------|
| Scene Name | `hollow_meridian_approach` |
| Type | Overworld |
| Size | 20x18 tiles |
| Visual Theme | The Hollow Meridian rises from deep bog water. A rickety wooden walkway leads to its entrance. Half the tower is submerged. |
| Tileset | Ashenveil Overworld Tileset |
| Connections | W: Outer Bog, N: Hollow Meridian F1 (door) |

**Enemy Encounters:**
- Bog Rat (1)

**Key Items/Events:**
- Save point at walkway start

---

#### Scene: Hollow Meridian — Floor 1

| Property | Detail |
|----------|--------|
| Scene Name | `hollow_meridian_f1` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Decaying tower interior. Floors crumbling, walls covered in moss and fungus, water seeping through cracks. Sickly purple-green lighting. |
| Tileset | Hollow Dungeon Tileset |
| Connections | S: Approach (door), N: Hollow Meridian F2 (stairs down — descending deeper) |

**Enemy Encounters:**
- Fungal Creep (2 patrol)
- Rot Vine (1 ambush)

**Key Items/Events:**
- Decay mechanic: Some floor tiles crumble after being stepped on once, forcing careful navigation
- Chest: Antidote

---

#### Scene: Hollow Meridian — Floor 2

| Property | Detail |
|----------|--------|
| Scene Name | `hollow_meridian_f2` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Submerged level. Waist-deep water (cosmetic), decayed mechanisms, bioluminescent fungus providing light. |
| Tileset | Hollow Dungeon Tileset |
| Connections | S: Hollow Meridian F1, N: Keeper's Quarters (side room), E: Hollow Meridian Depths (boss) |

**Enemy Encounters:**
- Fungal Creep (2)
- Decay Phantom (1)

**Key Items/Events:**
- Keeper's Quarters: Dead Keeper's journal found here (critical lore: "He was right about the depletion, but wrong about the solution.")
- Keeper Fragment 3 (Hollow) — found in Keeper's hidden cache behind a bookshelf
- Rook's energy cell — located in a side alcove

---

#### Scene: Hollow Meridian — Depths (Boss Room)

| Property | Detail |
|----------|--------|
| Scene Name | `hollow_meridian_depths` |
| Type | Dungeon (Boss Arena) |
| Size | 20x18 tiles |
| Visual Theme | Deepest chamber. The Hollow Core sits in a pool of stagnant, glowing water. Organic matter and Aether crystals merge into a grotesque mass. |
| Tileset | Hollow Dungeon Tileset |
| Connections | W: Hollow Meridian F2 (locked during fight) |

**Key Items/Events:**
- **Boss: Marsh Colossus** — emerges from the pool when player approaches the Core
- Hollow Core restored after victory

---

### Region 4: The Crystalfall Desert

---

#### Scene: Crystalfall Desert — Border Pass

| Property | Detail |
|----------|--------|
| Scene Name | `crystalfall_border` |
| Type | Overworld (Connector) |
| Size | 32x28 tiles |
| Visual Theme | Transition from marsh edge to arid land. Vegetation thins to nothing. The first frozen sand particles are visible, suspended in air. Stark color shift to whites and cyans. |
| Tileset | Crystalfall Overworld Tileset |
| Connections | W: Ashenveil Marsh (east exit), E: Crystalfall Desert — Frozen Expanse |

**Enemy Encounters:**
- Sand Sentinel (1 — frozen in place, activates when Edyn's time bubble reaches it)

**Key Items/Events:**
- First "unfreeze" encounter — tutorial for the time bubble mechanic

---

#### Scene: Crystalfall Desert — Frozen Expanse

| Property | Detail |
|----------|--------|
| Scene Name | `crystalfall_expanse` |
| Type | Overworld |
| Size | 32x32 tiles |
| Visual Theme | White sand desert with everything frozen in time. Sand hangs in mid-air, a caravan of merchants stands motionless, birds suspended in flight. Crystallized Aether formations jut from the ground. |
| Atmosphere | Eerie, silent, beautiful. Only the ticking of Edyn's pocket watch is audible. |
| Tileset | Crystalfall Overworld Tileset |
| Connections | W: Border Pass, E: Crystal Canyon, N: Frozen Caravan (scene transition) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Frozen NPCs (cosmetic) | Various | Cannot interact until desert is unfrozen |

**Enemy Encounters:**
- Sand Sentinel (2 — unfreeze when approached)
- Crystal Scarab (1 patrol — already moving due to Aether crystal proximity)

**Key Items/Events:**
- Chest: Aether Crystal (large, restores 30 MP)
- Frozen birds and sand particles as visual set pieces

---

#### Scene: Frozen Caravan

| Property | Detail |
|----------|--------|
| Scene Name | `frozen_caravan` |
| Type | Overworld (Event) |
| Size | 20x18 tiles |
| Visual Theme | A merchant caravan frozen mid-stride. Wagons, pack animals, merchants — all perfectly still. |
| Tileset | Crystalfall Overworld Tileset |
| Connections | S: Frozen Expanse |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Sable (frozen) | Center of caravan | Unfreezes when Edyn approaches; joins party |
| Frozen Merchants (cosmetic) | Various | Unfreeze only after Prism Meridian is restored |

**Key Items/Events:**
- Sable joins party (cutscene)
- Sable's Satchel obtained (enables shop discount passive)

---

#### Scene: Crystal Canyon

| Property | Detail |
|----------|--------|
| Scene Name | `crystal_canyon` |
| Type | Overworld |
| Size | 32x32 tiles |
| Visual Theme | Narrow canyon carved through massive crystallized Aether formations. Translucent pillars refract light into rainbow spectra. The Prism Meridian entrance is carved into the canyon wall. |
| Tileset | Crystalfall Overworld Tileset |
| Connections | W: Frozen Expanse, N: Prism Meridian Entrance |

**Enemy Encounters:**
- Crystal Scarab (2)
- Prism Wisp (1 — refracts into multiple images when attacked)

**Key Items/Events:**
- Chest: Crystal Shield (armor, +8 DEF)
- Save point at canyon mouth

---

#### Scene: Prism Meridian — Floor 1

| Property | Detail |
|----------|--------|
| Scene Name | `prism_meridian_f1` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Crystalline interior. Walls of translucent Aether, light beams criss-crossing the room, prismatic color effects. |
| Tileset | Prism Dungeon Tileset |
| Connections | S: Crystal Canyon (door), N: Prism Meridian F2 (stairs) |

**Enemy Encounters:**
- Prism Wisp (2)
- Crystal Scarab (1)

**Key Items/Events:**
- Light beam puzzle: Redirect frozen Aether beams using movable crystal blocks to hit switches
- Chest: Prism Lens (key item, allows seeing hidden paths on F2)

---

#### Scene: Prism Meridian — Floor 2

| Property | Detail |
|----------|--------|
| Scene Name | `prism_meridian_f2` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Deeper crystal chambers. More complex light beam networks. Some beams are frozen in time and must be "unfrozen" with the pocket watch (timed sequences). |
| Tileset | Prism Dungeon Tileset |
| Connections | S: Prism Meridian F1, N: Prism Meridian Sanctum (boss) |

**Enemy Encounters:**
- Prism Wisp (2)
- Refracted Shard (1 — splits into 2 smaller enemies on defeat)

**Key Items/Events:**
- Timed light beam puzzle using pocket watch
- Chest: Prism Blade (weapon, +10 ATK, light-element)
- Hidden path (visible with Prism Lens): Leads to chest with Aether Crystal (large)

---

#### Scene: Prism Meridian — Sanctum (Boss Room)

| Property | Detail |
|----------|--------|
| Scene Name | `prism_meridian_sanctum` |
| Type | Dungeon (Boss Arena) |
| Size | 20x18 tiles |
| Visual Theme | Vast circular crystal chamber. The Prism Core floats at center, refracting into a hundred light beams. Keeper Illion stands nearby. |
| Tileset | Prism Dungeon Tileset |
| Connections | S: Prism Meridian F2 (locked during fight) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Keeper Illion | Before the Core | Moral choice dialogue, then departure |

**Key Items/Events:**
- Illion's choice dialogue (affects Keeper Fragment acquisition)
- **Boss: Refracted Guardian** — activates after Illion departs
- Keeper Fragment 4 (Prism) — given by Illion if player chose to restore immediately
- Prism Core restored after boss defeat
- Desert unfreeze cutscene

---

### Region 5: The Ironpeak Mountains

---

#### Scene: Ironpeak Mountain Pass

| Property | Detail |
|----------|--------|
| Scene Name | `ironpeak_pass` |
| Type | Overworld (Connector) |
| Size | 32x28 tiles |
| Visual Theme | Snowy mountain path. Rocky outcrops, sparse pine trees, cold wind visual effects (blowing snow particles). |
| Tileset | Ironpeak Overworld Tileset |
| Connections | S: Crystalfall Desert (north exit), N: Ironpeak Enclave Gate |

**Enemy Encounters:**
- Mountain Wolf (2 patrol)
- Frost Golem (1 — slow, high DEF)

**Key Items/Events:**
- Chest: Warm Cloak (accessory, prevents cold-based status effects)

---

#### Scene: Ironpeak Enclave — Main Hall

| Property | Detail |
|----------|--------|
| Scene Name | `ironpeak_enclave` |
| Type | Town |
| Size | 32x32 tiles |
| Visual Theme | Underground town carved into the mountain. Forge fires glow orange, steel catwalks and support beams, crystal-lit tunnels. Industrial yet cozy. |
| Atmosphere | Safe haven. The last stop before the Chronospire. Warm, busy, the sound of hammering. |
| Tileset | Ironpeak Town Tileset |
| Connections | S: Mountain Pass, N: Enclave Deep Forge (door), E: Enclave Archives (door), W: Enclave Barracks (door) |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Dara | Near central forge | Lore about Vasael, weapon upgrade |
| Forge (Blacksmith) | Inside Deep Forge (door N) | Weapon and armor shop, crafting |
| Haldric | Near barracks entrance (W) | Rook's subplot confrontation |
| Enclave Merchant (Kira) | Market stall (east) | Best consumables shop in the game |

**Enemy Encounters:** None (safe zone).

**Key Items/Events:**
- Rook/Haldric confrontation cutscene (triggers if Rook is in party)
- Save point at central forge
- Best equipment available for purchase
- Weapon crafting: Bring Architect Alloy + Gold to Forge for unique weapons

---

#### Scene: Enclave Deep Forge (Interior)

| Property | Detail |
|----------|--------|
| Scene Name | `enclave_deep_forge` |
| Type | Indoor (Shop/Crafting) |
| Size | 20x18 tiles |
| Visual Theme | Massive underground forge. Anvils, smelters, weapon racks. Orange glow from molten metal. |
| Tileset | Ironpeak Interior Tileset |
| Connections | Door → Ironpeak Enclave Main Hall |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Forge (Blacksmith) | Center, at anvil | Weapon/armor shop and crafting |

---

#### Scene: Enclave Archives (Interior)

| Property | Detail |
|----------|--------|
| Scene Name | `enclave_archives` |
| Type | Indoor |
| Size | 20x18 tiles |
| Visual Theme | Stone library. Shelves of scrolls and blueprints, Architect artifacts in display cases, reading tables. |
| Tileset | Ironpeak Interior Tileset |
| Connections | Door → Ironpeak Enclave Main Hall |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Archivist Vell | At reading table | Lore about Architect civilization, optional dialogue |

**Key Items/Events:**
- Vasael's research notes (interactable bookshelf): Full backstory
- Architect schematics (interactable display): Lore about the Meridian construction

---

### Region 6: The Stillwater Basin and Chronospire

---

#### Scene: Stillwater Basin — Crossing

| Property | Detail |
|----------|--------|
| Scene Name | `stillwater_crossing` |
| Type | Overworld (Transition/Cutscene) |
| Size | 32x18 tiles |
| Visual Theme | Calm inland sea. Small boat crossing toward the Chronospire island. The tower dominates the horizon. |
| Atmosphere | Solemn, final. The party is quiet. |
| Tileset | Stillwater Tileset (water-heavy, boat sprite) |
| Connections | S: Ironpeak (auto-transition), N: Chronospire Island |

**Key Items/Events:**
- Party dialogue cutscene on the boat (each party member speaks)
- No enemies — transition scene
- Point of no return warning

---

#### Scene: Chronospire Island — Base

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_base` |
| Type | Overworld |
| Size | 32x28 tiles |
| Visual Theme | Rocky island with Architect stone paths leading to the massive Chronospire entrance. Aether distortions shimmer around the tower. Inscriptions glow on the walls. |
| Tileset | Chronospire Overworld Tileset |
| Connections | S: Stillwater Crossing, N: Chronospire Entrance (door, locked until pocket watch used) |

**Key Items/Events:**
- Pocket watch activation cutscene (Edyn opens the door)
- Save point (final save before dungeon)
- Chest: Chronospire Key (automatic, opens entrance)

---

#### Scene: Chronospire — Floor 1: Hall of Moments

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_f1` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Grand entrance hall. Tall stone corridors with glowing inscriptions. Rooms frozen at moments in history — palette shifts when entering flashback zones. |
| Tileset | Chronospire Dungeon Tileset |
| Connections | S: Chronospire Base (door), N: Chronospire F2 (stairs) |

**Enemy Encounters:**
- Temporal Shade (2 patrol)
- Aether Construct (1)

**Key Items/Events:**
- 3 flashback rooms: Brief visual vignettes of Architect history (non-interactive cutscenes)
- Chest: Chronoblade (weapon, +14 ATK)

---

#### Scene: Chronospire — Floor 2: Looping Corridors

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_f2` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Identical-looking corridors that loop endlessly. Subtle differences mark the correct path. Disorienting palette cycling. |
| Tileset | Chronospire Dungeon Tileset |
| Connections | S: Chronospire F1, N: Chronospire F3 |

**Enemy Encounters:**
- Temporal Shade (2)
- Loop Wraith (1 — teleports, hard to pin down)

**Key Items/Events:**
- Loop puzzle: Player must identify the correct sequence of 4 turns (L/R/L/R pattern, with visual cues)
- Chest: Temporal Ring (accessory, +5 SPD)

---

#### Scene: Chronospire — Floor 3: Decay Galleries

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_f3` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Rapid-aging corridors. Stone crumbles visibly, Architect murals fade, Aether conduits flicker and die. |
| Tileset | Chronospire Dungeon Tileset |
| Connections | S: Chronospire F2, N: Chronospire F4 |

**Enemy Encounters:**
- Aether Construct (2)
- Decay Phantom (1)

**Key Items/Events:**
- Speed challenge: Some corridors crumble on a timer — player must cross before floor falls
- Chest: Aether Crystal (large)
- Chest: Keeper's Robe (armor, +12 DEF, +5 MP)

---

#### Scene: Chronospire — Floor 4: Frozen Archive

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_f4` |
| Type | Dungeon |
| Size | 32x32 tiles |
| Visual Theme | Crystallized library. Aether records frozen in crystal formations. Beautiful, alien light. |
| Tileset | Chronospire Dungeon Tileset + Prism tiles |
| Connections | S: Chronospire F3, N: Chronospire F5 (Warden's Sanctum), (Hidden) E: Heart of the Chronospire (true ending only) |

**Enemy Encounters:**
- Temporal Shade (1)
- Aether Construct (1)

**Key Items/Events:**
- Lore crystals (5 interactable): Reveal the full truth of the Chronospire's sentience
- **True ending trigger:** If player has all 5 Keeper Fragments, the east wall opens to Floor 6 (Heart)
- Chest: Epoch Shield (armor, +15 DEF)
- Save point (final before boss)

---

#### Scene: Chronospire — Floor 5: Warden's Sanctum (Boss Room)

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_f5_warden` |
| Type | Dungeon (Final Boss Arena) |
| Size | 20x18 tiles |
| Visual Theme | Circular chamber at the tower's peak. The shattered Master Core hovers in fragments above a central dais. Vasael stands before it, surrounded by scattered notes and Aether instruments. |
| Atmosphere | Devastating. The culmination of the journey. |
| Tileset | Chronospire Dungeon Tileset |
| Connections | S: Chronospire F4 (locked during fight), (after fight) N: Stasis Chamber |

**NPCs:**

| NPC | Position | Purpose |
|-----|----------|---------|
| Vasael | Center, before shattered Core | Final boss confrontation |

**Key Items/Events:**
- Pre-fight dialogue cutscene (Vasael's speech)
- **Boss: Vasael, the Epoch Warden** — 3-phase fight
- Post-fight dialogue
- Transition to Stasis Chamber

---

#### Scene: Chronospire — Stasis Chamber

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_stasis` |
| Type | Cutscene |
| Size | 20x18 tiles |
| Visual Theme | Small chamber below the Sanctum. Alaric is suspended in a crystalline stasis field, perfectly preserved. |
| Tileset | Chronospire Dungeon Tileset |
| Connections | Accessed after defeating Vasael |

**Key Items/Events:**
- Alaric rescue cutscene (normal ending)
- Master Core repair sequence
- Ending sequence begins

---

#### Scene: Chronospire — Floor 6: Heart of the Chronospire (True Ending Only)

| Property | Detail |
|----------|--------|
| Scene Name | `chronospire_heart` |
| Type | Dungeon (Secret Boss Arena) |
| Size | 20x18 tiles |
| Visual Theme | Vast crystalline chamber. A massive living crystal structure — the Chronospire's consciousness made manifest. Warm golden light radiates from it. |
| Tileset | Chronospire Dungeon Tileset (gold palette variant) |
| Connections | W: Chronospire F4 (hidden door) |

**Key Items/Events:**
- Chronospire's dialogue (reveals Aether regeneration solution)
- Pocket watch sacrifice cutscene
- **Secret Boss: Heart of the Chronospire**
- True ending sequence begins after victory

---

## Complete Scene Summary Table

| # | Scene Name | Region | Type | Size (tiles) | Enemies | Key Item/Event |
|---|-----------|--------|------|-------------|---------|----------------|
| 1 | `millhaven_town_square` | Verdant Reach | Town | 32x32 | None | Game start, save |
| 2 | `alaric_workshop` | Verdant Reach | Indoor | 20x18 | None | Pocket Watch, Travel Pack |
| 3 | `wynns_shop` | Verdant Reach | Indoor/Shop | 20x18 | None | General goods shop |
| 4 | `verdant_south_road` | Verdant Reach | Overworld | 32x28 | Wisp, Beetle | Combat tutorial |
| 5 | `oakwatch_grove_entrance` | Verdant Reach | Overworld | 32x32 | Wisp, Beetle | Lira joins, Serea quest |
| 6 | `verdant_meridian_f1` | Verdant Reach | Dungeon | 32x32 | Gear Sprite, Wisp | Gear puzzle |
| 7 | `verdant_meridian_f2` | Verdant Reach | Dungeon | 32x32 | Gear Sprite, Automaton | Iron Cog, time-dilation |
| 8 | `verdant_meridian_vault` | Verdant Reach | Boss Arena | 20x18 | Corroded Timekeeper | Calibration Key, Fragment 1 |
| 9 | `verdant_west_road` | Verdant Reach | Connector | 32x28 | Wisp, Crab | Transition to coast |
| 10 | `stormhaven_town` | Stormhaven Coast | Town | 32x32 | None | Storm loop, save |
| 11 | `stormhaven_harbor` | Stormhaven Coast | Town | 32x28 | None | Pip location |
| 12 | `stormhaven_warehouse` | Stormhaven Coast | Indoor | 20x18 | None | Pip reunion, Storm Lantern |
| 13 | `cliff_path_tidal` | Stormhaven Coast | Overworld | 32x28 | Crab, Gull | Storm timing gate |
| 14 | `tidal_meridian_f1` | Stormhaven Coast | Dungeon | 32x32 | Lurker, Jellyfish | Water level puzzle |
| 15 | `tidal_meridian_f2` | Stormhaven Coast | Dungeon | 32x32 | Lurker, Gull, Jelly | Water wheel puzzle |
| 16 | `tidal_meridian_sanctum` | Stormhaven Coast | Boss Arena | 20x18 | Keeper Corwin | Tideborn Relic, Fragment 2 |
| 17 | `ashenveil_north_road` | Ashenveil Marsh | Connector | 32x28 | Rat, Vine | Rook joins |
| 18 | `ashenveil_outer_bog` | Ashenveil Marsh | Overworld | 32x32 | Rat, Vine, Phantom | Decay hazard |
| 19 | `architect_ruins` | Ashenveil Marsh | Landmark | 32x28 | Phantom | Lore, Alloy, Haldric evidence |
| 20 | `hollow_meridian_approach` | Ashenveil Marsh | Overworld | 20x18 | Rat | Save point |
| 21 | `hollow_meridian_f1` | Ashenveil Marsh | Dungeon | 32x32 | Fungal Creep, Vine | Crumbling floors |
| 22 | `hollow_meridian_f2` | Ashenveil Marsh | Dungeon | 32x32 | Creep, Phantom | Journal, Fragment 3, Cell |
| 23 | `hollow_meridian_depths` | Ashenveil Marsh | Boss Arena | 20x18 | Marsh Colossus | Hollow Core |
| 24 | `crystalfall_border` | Crystalfall Desert | Connector | 32x28 | Sand Sentinel | Time bubble tutorial |
| 25 | `crystalfall_expanse` | Crystalfall Desert | Overworld | 32x32 | Sentinel, Scarab | Frozen world |
| 26 | `frozen_caravan` | Crystalfall Desert | Event | 20x18 | None | Sable joins |
| 27 | `crystal_canyon` | Crystalfall Desert | Overworld | 32x32 | Scarab, Prism Wisp | Crystal Shield |
| 28 | `prism_meridian_f1` | Crystalfall Desert | Dungeon | 32x32 | Wisp, Scarab | Light beam puzzle |
| 29 | `prism_meridian_f2` | Crystalfall Desert | Dungeon | 32x32 | Wisp, Shard | Timed light puzzle |
| 30 | `prism_meridian_sanctum` | Crystalfall Desert | Boss Arena | 20x18 | Refracted Guardian | Fragment 4, Prism Core |
| 31 | `ironpeak_pass` | Ironpeak Mountains | Connector | 32x28 | Wolf, Golem | Warm Cloak |
| 32 | `ironpeak_enclave` | Ironpeak Mountains | Town | 32x32 | None | Hub, Rook subplot |
| 33 | `enclave_deep_forge` | Ironpeak Mountains | Indoor/Shop | 20x18 | None | Crafting, best gear |
| 34 | `enclave_archives` | Ironpeak Mountains | Indoor | 20x18 | None | Vasael lore |
| 35 | `stillwater_crossing` | Stillwater Basin | Transition | 32x18 | None | Party dialogue |
| 36 | `chronospire_base` | Chronospire | Overworld | 32x28 | None | Door opening |
| 37 | `chronospire_f1` | Chronospire | Dungeon | 32x32 | Shade, Construct | Flashbacks |
| 38 | `chronospire_f2` | Chronospire | Dungeon | 32x32 | Shade, Wraith | Loop puzzle |
| 39 | `chronospire_f3` | Chronospire | Dungeon | 32x32 | Construct, Phantom | Speed corridors |
| 40 | `chronospire_f4` | Chronospire | Dungeon | 32x32 | Shade, Construct | Lore, true ending gate |
| 41 | `chronospire_f5_warden` | Chronospire | Boss Arena | 20x18 | Vasael | Final boss |
| 42 | `chronospire_stasis` | Chronospire | Cutscene | 20x18 | None | Alaric rescue |
| 43 | `chronospire_heart` | Chronospire | Secret Boss | 20x18 | Heart of Chronospire | True ending |

**Total Scenes: 43**

---

*Chronospire: The Shattered Meridian — World Map and Areas Document*
