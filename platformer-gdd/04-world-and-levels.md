# 04 — World & Levels

---

## World Overview

Ember Tide contains **5 worlds** plus a **Prologue** area and a **hidden endgame area**, for a total of **7 distinct zones**. Each world consists of 3–5 playable scenes plus a boss arena scene, giving the game approximately **25–30 unique scenes** in total.

| # | World Name | Theme | Levels | Boss |
|---|---|---|---|---|
| 0 | Cinderhearth (Prologue) | Village / Tutorial | 2 | — |
| 1 | Verdant Hollow | Forest / Overgrown | 4 + Boss | Briar Sentinel |
| 2 | Frostfang Peaks | Ice / Mountain | 4 + Boss | Glacial Wyrm |
| 3 | Sunken Brine | Underwater Ruins | 4 + Boss | Abyssal Leviathan |
| 4 | Cinderforge Depths | Volcanic Caverns | 4 + Boss | Molten Warden |
| 5 | The Spire Ascent | Sky Citadel | 5 + Mini-Boss + Boss | Shade (Mini), Varek (Final) |
| 6 | Chamber of Origin (Secret) | Ancient / White Stone | 1 | — |

---

## World Map Layout Description

The world map is a top-down stylized representation of Lumara, oriented vertically. Cinderhearth sits at the bottom center. The Verdant Hollow spreads to the left and upward through a forested valley. Frostfang Peaks rise to the upper left with jagged mountain silhouettes. The Sunken Brine is accessed through a cave mouth at the base of the mountains, descending underground to the center-right of the map. The Cinderforge Depths connect from the Brine's deepest point and run along the bottom-right with glowing magma veins. The Spire floats at the very top center of the map, connected to the ground by a chain of floating platforms (the Ascent). The Chamber of Origin is hidden and does not appear on the map until unlocked.

Each world node on the map glows with its Hearthstone color when reignited (green, blue, teal, orange, white) and appears dim/gray when unlit. Cinderhearth glows warm amber. Paths between worlds are drawn as dotted lines that become solid as the player clears them.

---

## Prologue: Cinderhearth

### Scene 0-1: Cinderhearth Village — Evening Round

**Visual Theme:** Warm, cozy village at dusk. Cobblestone road, wooden houses with lit windows, hanging lanterns, a well at the center, Maren's house at the far right.

**Platformer Physics Enabled:**
- Gravity: YES
- Jump: YES
- Double Jump: NO
- Wall Jump: NO
- Dash: NO
- Coyote Time: YES (forgiving, tutorial)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_cinderhearth`

**Background:** Dusky orange-pink sky with silhouettes of distant hills and the faint glow of the Verdant Hearthstone on a hill to the left. Parallax scrolling: slow clouds in the upper portion.

**Foreground:** Occasional lamp posts in the foreground layer, casting warm light pools.

**Enemy Types:** None (tutorial scene)

**Hazards:** None

**Collectibles and Secrets:**
- 1 Ember Shard hidden behind Maren's house (requires jumping onto the roof from the well platform)
- 3 Flame Coins along the main road (currency tutorial)

**Scripted Events:**
- Opening: Solen walks right, player gains control. First lantern-lighting interaction teaches the A-button interact.
- Lighting 5 lanterns along the road triggers Maren's dialogue at the house.
- After the last lantern, the ground shakes — transition to cutscene.

**Exit/Transition:** Right edge leads to Scene 0-2 (Cinderhearth — The Hollow Surge).

---

### Scene 0-2: Cinderhearth — The Hollow Surge

**Visual Theme:** Same village, now in chaos. Lanterns shatter, purple-black shadow tendrils creep across the ground, the sky turns dark violet. The Hearthstone on the hill in the background flickers violently.

**Platformer Physics Enabled:**
- Gravity: YES
- Jump: YES
- Double Jump: NO
- Wall Jump: NO
- Dash: NO
- Coyote Time: YES
- Ladders: NO
- Floating: NO

**Tileset:** `ts_cinderhearth_dark` (same layout as 0-1 but with corrupted palette — darker, purple-tinged)

**Background:** Dark violet sky, Hearthstone flickering, shadow wave visible as a moving wall of darkness approaching from the left.

**Foreground:** Shattered lantern glass on the ground, fallen sign posts.

**Enemy Types:** None (cutscene scene — player runs right, no combat)

**Hazards:**
- Shadow tendrils on the ground deal 1 HP damage on contact (teaches the player about hazards)

**Collectibles and Secrets:** None

**Scripted Events:**
- Player must run right to reach Maren's house.
- At the house: full petrification cutscene (Maren → stone). Dialogue event with portraits.
- After cutscene: Brennan appears, gives map and exposition. Dialogue event.
- Solen receives the Lantern Staff (equip event — weapon tutorial).

**Exit/Transition:** Right edge transitions to World 1, Scene 1-1.

---

## World 1: Verdant Hollow

### Scene 1-1: Hollow Entrance — Ashen Canopy

**Visual Theme:** A forest path under towering trees. The canopy above filters dim, gray-green light. Fallen leaves cover the ground. Some trees are half-consumed by shadow — their bark is streaked with purple-black veins. Small clusters of bioluminescent mushrooms provide faint teal light near the path.

**Platformer Physics Enabled:**
- Gravity: YES (standard — value 128)
- Jump: YES (height value 160)
- Double Jump: NO
- Wall Jump: NO
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: YES (vine-covered tree trunks)
- Floating: NO

**Tileset:** `ts_verdant_hollow`

**Background:** Deep forest with layered tree silhouettes in dark green and gray-green. Faint light beams from above. Parallax: two layers (far trees stationary, mid trees slow scroll).

**Foreground:** Overhanging branches and leaves in the upper portion of the screen, mushroom clusters at ground level.

**Enemy Types:**
- Shadow Hare (2 per scene, patrol left-right on ground)
- Gloom Bat (2 per scene, patrol left-right in air, sine-wave pattern)

**Hazards:**
- Shadow Puddles: dark patches on the ground that deal 1 HP on contact
- Crumbling Branches: platforms that fall 1 second after the player steps on them

**Collectibles and Secrets:**
- 3 Flame Coins (along main path)
- 1 Ember Shard (hidden on a high platform accessible by ladder + precise jump)
- 1 Heart Crystal Piece (behind a destructible wall at the bottom — attack the cracked bark)

**Scripted Events:**
- First enemy encounter: brief camera pause and exclamation mark over Solen's head (teaches player that enemies exist).

**Exit/Transition:** Right edge → Scene 1-2.

---

### Scene 1-2: Verdant Hollow — Mushroom Grotto

**Visual Theme:** A low-ceilinged cavern beneath the forest floor, lit entirely by bioluminescent mushrooms in teal, green, and soft yellow. Pools of still water on the ground reflect the mushroom light. Roots hang from the ceiling. The air feels damp and close.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: NO
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: YES (hanging roots)
- Floating: NO

**Tileset:** `ts_mushroom_grotto`

**Background:** Dark cavern walls with scattered glowing mushroom clusters. Dripping water particles. No parallax (enclosed space).

**Foreground:** Large mushroom caps in the foreground, translucent with glow.

**Enemy Types:**
- Sporecap (3 per scene — stationary mushroom enemy, shoots spore projectiles)
- Shadow Hare (1 per scene)

**Hazards:**
- Poison Pools: green-tinged water patches that deal 1 HP on contact
- Dripping Stalactites: drop from ceiling when player passes underneath (2-second warning wobble)

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (hidden in a pool — player must drop into a specific water section and swim left into a hidden alcove)

**Scripted Events:**
- Meeting Fern: she appears near the grotto entrance, dialogue event with portrait. She gives the Healing Tincture recipe (first healing item) and tells the player about the Thornveil Thicket.

**Exit/Transition:** Right edge → Scene 1-3.

---

### Scene 1-3: Verdant Hollow — Thornveil Thicket

**Visual Theme:** Dense bramble and vine-choked vertical passage. The thorns are thick, sharp, and everywhere. This is the game's first wall-jump teaching area. The scene scrolls primarily vertically rather than horizontally — the player must ascend through a tight shaft of bramble and vine.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES (INTRODUCED HERE — Fern explains it at the entrance: "The vines are sticky — you can kick off them!")
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: YES (vines)
- Floating: NO

**Tileset:** `ts_verdant_hollow` + `ts_thornveil` overlay (thorns and thick vines)

**Background:** Narrow vertical shaft of twisted wood and vine. Light at the top. Dark at the bottom.

**Foreground:** Thorn branches crossing the screen at angles — visual only, no collision (collision is on the wall tiles).

**Enemy Types:**
- Thorn Creeper (2 per scene — vine-like enemy that clings to walls and extends thorny tendrils periodically)
- Gloom Bat (2 per scene — fly in the vertical shaft)

**Hazards:**
- Thorn Walls: contact with thorned tiles deals 1 HP. Player must use wall jump on the smooth vine sections, not the thorny sections.
- Falling Bramble: sections of the vertical wall that collapse after being wall-jumped off (one-use platforms)

**Collectibles and Secrets:**
- 3 Flame Coins (spaced vertically along the ascent)
- 1 Lore Stone (World 1) — hidden in an alcove halfway up the shaft, requiring a precise wall-jump to reach a side passage. The Lore Stone contains the first fragment of the First Keeper incantation.

**Scripted Events:** None (pure platforming challenge)

**Exit/Transition:** Top of the shaft → Scene 1-4.

---

### Scene 1-4: Verdant Hollow — Hearthstone Clearing

**Visual Theme:** A wide clearing in the forest. The Verdant Hearthstone — a massive green crystal the size of a house — sits at the center, pulsing with faint, sickly light. The trees around the clearing are healthier than those in the rest of the forest, kept alive by the Hearthstone's residual energy. Fireflies drift in the air. The ground is soft moss.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_verdant_hollow` + `ts_hearthstone_chamber`

**Background:** Large Hearthstone crystal dominating the background, pulsing green. Soft light rays. Circular clearing with tree line.

**Foreground:** Floating pollen particles, fireflies.

**Enemy Types:** None (pre-boss area — enemies cleared to maintain actor budget for boss)

**Hazards:** None

**Collectibles and Secrets:**
- 1 Ember Shard (on a high tree branch at the left side of the clearing — requires wall jump off the Hearthstone's base)

**Scripted Events:**
- Approaching the Hearthstone triggers a cutscene: the Briar Sentinel emerges from the ground around the crystal. Brief dialogue (the Sentinel roars — no words, but a text description: *"The guardian stirs — its eyes glow with corrupted light. It doesn't recognize you as friend."*).

**Exit/Transition:** Defeating the boss → post-boss cutscene → World Map (World 2 unlocked). Returning later: exit right → World 1 hub.

---

### Scene 1-B: Verdant Hollow — Boss Arena (Briar Sentinel)

**Visual Theme:** Same clearing as 1-4, but the camera is locked and the arena is defined: a flat platform with the Hearthstone in the background center. Two raised moss-covered platforms on either side provide verticality. Roots and vines frame the edges.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES (on arena side walls)
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_verdant_hollow` + `ts_boss_arena`

**Background:** Hearthstone crystal, clearing, dramatic lighting.

**Enemy Types:** Briar Sentinel (boss — see 07-bosses.md)

**Hazards:**
- Thorn Roots: the Sentinel summons root attacks from the ground (Phase 1)
- Falling Bramble Debris: falls from above during Phase 2

**Collectibles and Secrets:** None (boss arena)

**Scripted Events:**
- Boss intro cutscene
- Boss defeat: Hearthstone reignition sequence (flash of green light, the forest blooms)
- Post-boss: Solen's reaction to petrified villagers. Fern's dialogue. Story Beat 1.

**Exit/Transition:** Post-boss → World Map.

---

## World 2: Frostfang Peaks

### Scene 2-1: Frostfang Peaks — Lower Slopes

**Visual Theme:** Rocky mountain trail with patches of snow. Pine trees with frosted needles line the path. The sky is pale gray-white. Wind particles blow left-to-right across the screen. The path ascends gradually from left to right with rocky outcroppings serving as platforms.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: YES (rock faces with handholds)
- Floating: NO

**Tileset:** `ts_frostfang_peaks`

**Background:** Distant mountain range with snow-capped peaks. Pale sky with slow-moving clouds. Parallax: far mountains stationary, mid mountains slow scroll.

**Foreground:** Snowflake particles, occasional pine branches.

**Enemy Types:**
- Frost Fang (wolf-like shadow creature, 2 per scene — patrol, faster than Shadow Hares)
- Ice Shard (2 per scene — stationary enemy on ledges, fires ice projectiles at intervals)

**Hazards:**
- Ice Patches: slippery ground tiles that reduce player traction (Solen slides further when stopping)
- Wind Gusts: periodic left-to-right push that nudges the player — can knock them off ledges

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (hidden in a cave behind a false wall on the left side — attack the cracked rock)

**Scripted Events:**
- Meeting Orin: he appears at his cabin (a wooden structure partway up the slope). Full dialogue event with portrait. He gives the Climbing Gear (wall jump upgrade — increased height).

**Exit/Transition:** Right edge → Scene 2-2.

---

### Scene 2-2: Frostfang Peaks — Rimehaven

**Visual Theme:** A frozen village on a mountain shelf. Small houses with icicle-covered roofs, frozen fountains, and streets covered in deep snow. The village is eerily silent. Frozen villagers stand throughout — a child reaching for a door, a merchant behind a cart, two friends mid-conversation. The lighting is blue-white, cold and still.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: YES (frozen scaffolding)
- Floating: NO

**Tileset:** `ts_frostfang_peaks` + `ts_rimehaven_village`

**Background:** Frozen village buildings in background layer. Icicles hanging from rooftops. Pale blue sky.

**Foreground:** Falling snow particles, icicle clusters.

**Enemy Types:**
- Frost Fang (2 per scene)
- Ice Shard (1 per scene — on a rooftop)
- Hollow Wisp (1 per scene — new enemy, floats in air, follows player slowly)

**Hazards:**
- Icicle Drops: triggered by player walking underneath, fall after 1-second warning shimmer
- Thin Ice: platforms that crack and break after 1.5 seconds of standing on them

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (inside a frozen house — enter through the chimney by jumping on the roof and pressing Down)
- 1 Heart Crystal Piece (hidden in the frozen fountain — attack the ice three times to break it)

**Scripted Events:**
- Environmental storytelling: interacting with frozen villagers triggers brief descriptive text ("A child, frozen mid-step. Their hand is stretched toward the door. So close.").

**Exit/Transition:** Right edge → Scene 2-3.

---

### Scene 2-3: Frostfang Peaks — The Ice Shelf

**Visual Theme:** A narrow, exposed mountain ledge high above the clouds. The path is treacherous — thin platforms of ice and rock jut out over a vast drop. Wind is strongest here. The sky above is clear but dark, almost starless. Far below, clouds shift like a white ocean.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_frostfang_peaks` + `ts_ice_shelf`

**Background:** Vast open sky, cloud layer below the level, distant peaks barely visible. Vertical scrolling area.

**Foreground:** Wind-blown snow particles, occasional rock debris.

**Enemy Types:**
- Frost Fang (1 — patrols a narrow ledge)
- Gloom Bat (3 — fly in the open air, sine-wave pattern, more aggressive than forest version)
- Ice Shard (2 — on narrow ledges, projectiles more dangerous with knockback near edges)

**Hazards:**
- Wind Gusts: stronger here — can push the player two tiles, making precision platforming critical
- Bottomless Pit: falling off the ledge = instant death, respawn at checkpoint
- Crumbling Rock: platforms that break after 1 second

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (on a tiny platform far to the right, reachable only with a precise wall-jump chain off two rock outcroppings)

**Scripted Events:** None (pure platforming challenge)

**Exit/Transition:** Top/right edge → Scene 2-4.

---

### Scene 2-4: Frostfang Peaks — Summit Shrine

**Visual Theme:** The mountain summit — a flat, windswept plateau with the Frost Hearthstone at the center inside an open-air stone shrine. The shrine's pillars are cracked and coated in ice. The Hearthstone glows a weak, flickering blue. The sky above is dark gray, heavy with unfallen snow.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_frostfang_peaks` + `ts_hearthstone_chamber`

**Background:** Summit panorama, Hearthstone shrine, dark sky.

**Foreground:** Blowing snow, ice particles.

**Enemy Types:** None (pre-boss — actor budget reserved)

**Hazards:**
- Wind Gusts (constant, low-intensity push toward left edge)

**Collectibles and Secrets:**
- 1 Lore Stone (World 2) — hidden behind the shrine. After approaching the Hearthstone, go left and wall-jump up the back of the shrine's outer wall to reach a small alcove.

**Scripted Events:**
- Approaching the Hearthstone: the Glacial Wyrm descends from the sky and coils around the crystal. Cutscene with roar (descriptive text).

**Exit/Transition:** Boss defeat → post-boss cutscene → Hidden shrine discovery (Story Beat 2) → World Map.

---

### Scene 2-B: Frostfang Peaks — Boss Arena (Glacial Wyrm)

**Visual Theme:** Summit plateau locked arena. Narrow ledge with the Hearthstone at the right side. The Wyrm coils around the right portion of the arena. Two elevated platforms (ice-covered shrine pillars) provide height advantage. Wind blows constantly.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES (on shrine pillars)
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_frostfang_peaks` + `ts_boss_arena`

**Background:** Summit sky, Hearthstone.

**Enemy Types:** Glacial Wyrm (boss)

**Hazards:**
- Ice Breath: Wyrm's attack covers ground tiles in slippery ice
- Wind Gusts: push player toward left edge (bottomless pit)
- Falling Icicles: dislodged by Wyrm's movements

**Collectibles and Secrets:** None

**Scripted Events:**
- Boss intro/outro cutscenes
- Post-boss: hidden shrine mural discovery, Solen's journal sketch moment.

**Exit/Transition:** Post-boss → World Map.

---

## World 3: Sunken Brine

### Scene 3-1: Sunken Brine — Cavern Mouth

**Visual Theme:** The entrance to the underground sea. A massive cave opening in the mountainside leads down through a series of wet, dripping tunnels. Stalactites and stalagmites frame the path. Pools of teal-green water cover the floor in places. Bioluminescent algae line the walls, providing eerie light.

**Platformer Physics Enabled:**
- Gravity: YES (slightly reduced — value 112 — to evoke the heavy, damp atmosphere)
- Jump: YES (height 144, slightly floaty)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (8 frames — more forgiving due to the floaty physics)
- Ladders: YES (rock formations with handholds, chains hanging from ceiling)
- Floating: NO

**Tileset:** `ts_sunken_brine`

**Background:** Deep cavern with bioluminescent algae clusters, dripping water, dark recesses.

**Foreground:** Stalactite silhouettes, dripping water particles.

**Enemy Types:**
- Brine Crawler (2 per scene — crab-like, patrols ground, fast)
- Jelly Drift (2 per scene — jellyfish-like, floats up and down, contact damage)

**Hazards:**
- Deep Water Pools: player can swim but movement is slowed; must surface for air (10-second breath timer)
- Dripping Acid: green drops from certain stalactites, damage on contact

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (underwater — in a submerged alcove at the bottom of the first deep pool)

**Scripted Events:**
- Meeting Coral: she appears at the entrance, dialogue event with portrait. She joins as a guide (narrative only — she doesn't follow as an on-screen actor to save actor slots).

**Exit/Transition:** Down/right → Scene 3-2.

---

### Scene 3-2: Sunken Brine — Flooded Ruins

**Visual Theme:** Ancient First Keeper ruins half-submerged in teal water. Stone columns rise from the water, connected by crumbling walkways. Carved walls depict faded murals of the First Keepers. Glowing symbols on certain wall panels activate when Solen's lantern passes near them. The water level fills the bottom third of the scene; the player alternates between platforming above water and swimming below.

**Platformer Physics Enabled:**
- Gravity: YES (112 above water; 80 underwater)
- Jump: YES (height 144 above water; 96 underwater — reduced)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (8 frames)
- Ladders: YES (chains, carved wall handholds)
- Floating: YES (underwater sections — player floats slowly upward when not pressing down)

**Tileset:** `ts_sunken_brine` + `ts_first_keeper_ruins`

**Background:** Submerged ruin walls, glowing symbols, deep water fading to dark below.

**Foreground:** Fish swimming, water surface ripple effect, bubbles.

**Enemy Types:**
- Brine Crawler (2 on dry platforms)
- Jelly Drift (2 in water sections)
- Ruin Guardian (1 — a stone construct that activates when Solen approaches, fires slow energy orbs)

**Hazards:**
- Deep Water (breath timer)
- Crumbling Walkways: collapse when stepped on, dropping player into water
- Energy Orbs: fired by Ruin Guardians, travel slowly in a straight line

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (behind a glowing wall panel — interact with it using the lantern to reveal a hidden passage)
- 1 Heart Crystal Piece (deep underwater in a hidden room beneath the ruins — requires swimming down through a narrow passage)

**Scripted Events:**
- Coral (via dialogue pop-up) comments on the First Keeper architecture and hints at the location of her lost locket.

**Exit/Transition:** Right edge → Scene 3-3.

---

### Scene 3-3: Sunken Brine — Varek's Research Chamber

**Visual Theme:** A dry, intact chamber deep in the ruins. This is where Varek spent years studying the First Keeper inscriptions. The room is cluttered: a stone desk covered in journals and scrolls, diagrams carved into the walls, a partially dismantled First Keeper device in the corner. The walls are covered in Varek's handwriting — notes, equations, fragments of the Hollow's "language." The atmosphere is unsettling — this is a room where obsession lived.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128 — dry room)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_first_keeper_ruins` + `ts_research_chamber`

**Background:** Stone walls covered in carved text and diagrams. Shelves of journals. Flickering purple-tinted light from a partially active First Keeper device.

**Foreground:** Dust particles, paper scraps.

**Enemy Types:** None (narrative scene)

**Hazards:** None

**Collectibles and Secrets:**
- 3 Flame Coins (scattered on shelves)
- 1 Lore Stone (World 3) — hidden inside the dismantled First Keeper device. Interact with the device three times (each interaction reveals a text fragment) and the Lore Stone is ejected.

**Scripted Events:**
- Reading Varek's journals: three interactive points on the desk, each triggering a dialogue box with journal text that reveals Varek's perspective and descent into obsession.
- Coral's commentary on the journals via dialogue.

**Exit/Transition:** Right edge → Scene 3-4.

---

### Scene 3-4: Sunken Brine — Keeper Cathedral

**Visual Theme:** A massive underwater cathedral — the largest single scene in the game. The cathedral is fully submerged, with towering columns rising into murky darkness above and a floor of ancient mosaic tiles far below. Shafts of bioluminescent light illuminate sections, leaving others in deep shadow. The Brine Hearthstone sits at the far end in an alcove, glowing weakly through the water. Schools of fish swim in formation. Seaweed sways from every surface.

**Platformer Physics Enabled:**
- Gravity: YES (80 — fully underwater)
- Jump: YES (96 — underwater jumps are slow, floaty pushes)
- Double Jump: NO
- Wall Jump: YES (on column surfaces)
- Dash: NO
- Coyote Time: YES (8 frames)
- Ladders: YES (seaweed strands — climbable)
- Floating: YES (constant gentle upward drift)

**Tileset:** `ts_sunken_brine` + `ts_keeper_cathedral`

**Background:** Massive underwater space, columns fading into darkness, mosaic floor, Hearthstone glow at far end.

**Foreground:** Fish, bubbles, floating debris, seaweed.

**Enemy Types:**
- Jelly Drift (3 — spread throughout)
- Brine Crawler (2 — on the mosaic floor)
- Abyssal Eel (1 — new enemy, long serpentine creature that patrols a section of the cathedral)

**Hazards:**
- Breath Timer (extended to 15 seconds due to scene length — air bubble pockets exist at column tops)
- Shadow Currents: streams of Hollow-tainted water that push the player in a direction and deal 1 HP if in contact for more than 2 seconds

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (hidden in the mosaic floor — a specific tile looks different; interact with it to reveal a hidden alcove)
- Coral's Locket: found in a side passage. Returning it to Coral (in the post-scene) unlocks additional dialogue.

**Scripted Events:**
- Approaching the Hearthstone triggers the Abyssal Leviathan boss intro.

**Exit/Transition:** Boss defeat → post-boss corridor → Shade confrontation (Story Beat 3) → World Map.

---

### Scene 3-B: Sunken Brine — Boss Arena (Abyssal Leviathan)

**Visual Theme:** The Keeper Cathedral altar, locked arena. The Hearthstone is at the back. The arena is underwater with air pockets at two points near the ceiling. The Leviathan's tentacles emerge from the darkness below.

**Platformer Physics Enabled:**
- Gravity: YES (80 — underwater)
- Jump: YES (96)
- Double Jump: NO
- Wall Jump: YES
- Dash: NO
- Coyote Time: YES (8 frames)
- Ladders: YES (seaweed)
- Floating: YES

**Tileset:** `ts_keeper_cathedral` + `ts_boss_arena`

**Background:** Cathedral alcove, Hearthstone, deep water fading to black below.

**Enemy Types:** Abyssal Leviathan (boss)

**Hazards:**
- Tentacle Slams: from below, hitting the floor platform
- Ink Clouds: obscure vision temporarily
- Breath Timer (air pockets available)

**Collectibles and Secrets:** None

**Scripted Events:**
- Boss intro/outro cutscenes
- Post-boss: Shade appears in the exit corridor. Full betrayal dialogue. Story Beat 3.

**Exit/Transition:** Post-boss → World Map.

---

## World 4: Cinderforge Depths

### Scene 4-1: Cinderforge Depths — Magma Tunnels

**Visual Theme:** Narrow mining tunnels lit by rivers of magma. The walls are rough-hewn stone with support beams. Magma flows through channels cut into the floor. The air shimmers with heat. Abandoned mining equipment — carts, picks, helmets — litters the scene. Everything has a reddish-orange cast. Shadow corruption is heavy: purple-black veins run through the rock and the magma has taken on a sickly purple tint in corrupted areas.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: YES (INTRODUCED HERE — Wrench modifies Solen's boots with a "quick-step" mechanism. Dash allows crossing lava gaps.)
- Coyote Time: YES (6 frames)
- Ladders: YES (mine shaft scaffolding)
- Floating: NO

**Tileset:** `ts_cinderforge`

**Background:** Magma rivers, cave walls, distant forge glow, rising heat haze.

**Foreground:** Ash particles, ember particles floating upward, heat shimmer.

**Enemy Types:**
- Slag Crawler (2 per scene — molten rock creature, slow patrol, leaves fire trail)
- Ember Wisp (2 per scene — small floating fire creature, chases player when close)

**Hazards:**
- Magma Rivers: instant death on contact, respawn at checkpoint
- Steam Vents: periodic jets of steam from floor, deal 2 HP and knock player upward
- Falling Rocks: triggered by proximity, fall from ceiling

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (on a platform across a wide lava gap — requires the newly acquired dash)

**Scripted Events:**
- Meeting Wrench: he appears behind his barricade. Full dialogue with portrait. He gives the Dash Boots upgrade and asks for help clearing his escape route.

**Exit/Transition:** Right edge → Scene 4-2.

---

### Scene 4-2: Cinderforge Depths — The Forge Floor

**Visual Theme:** A massive open cavern serving as the main forge complex. Giant anvils, cold furnaces, and chains hang from the ceiling. Conveyor belts (moving platforms) transport ore carts across lava pits. Gear-driven elevators connect upper and lower levels. The forge was once a place of incredible industry; now it's dark, corrupted, and dangerous. Purple-black shadow crusts the machinery.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: YES (chains)
- Floating: NO

**Tileset:** `ts_cinderforge` + `ts_forge_machinery`

**Background:** Massive forge cavern, giant machinery silhouettes, distant magma glow.

**Foreground:** Chains, gear silhouettes, ash.

**Enemy Types:**
- Slag Crawler (2)
- Ember Wisp (2)
- Shadow Smith (1 — humanoid shadow creature, formerly a miner, swings a hammer, patrols near anvils)

**Hazards:**
- Conveyor Belts: move the player left or right automatically, can push into magma if not countered
- Gear Crushers: rotating gears that deal 2 HP on contact
- Magma Pits: between conveyor sections

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (hidden inside a cold furnace — dash through a cracked furnace door)
- 1 Heart Crystal Piece (on top of a chain, reachable by riding a conveyor belt to its end and wall-jumping up)

**Scripted Events:** None (gameplay-focused scene)

**Exit/Transition:** Right edge → Scene 4-3.

---

### Scene 4-3: Cinderforge Depths — Obsidian Core

**Visual Theme:** The deepest part of the Cinderforge, where raw obsidian formations jut from the walls and the magma is brightest (and most corrupted). The environment is a mix of natural volcanic cave and First Keeper engineering — the First Keepers built the Forge Hearthstone's housing here, and their white stone contrasts sharply with the dark obsidian. The Hearthstone is visible in the background, encased in a shell of cooled shadow-obsidian.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 160)
- Double Jump: NO
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: YES
- Floating: NO

**Tileset:** `ts_cinderforge` + `ts_obsidian_core`

**Background:** Obsidian formations, Hearthstone in shadow-shell, magma rivers, First Keeper white stone.

**Foreground:** Obsidian shards, ember particles.

**Enemy Types:**
- Ember Wisp (3 — more aggressive in the core)
- Shadow Smith (1)

**Hazards:**
- Magma Geysers: erupt from specific floor tiles on a timer, 3 HP damage
- Obsidian Shards: sharp crystal formations on walls, damage on contact
- Shadow Pools: corrupted magma that sends up shadow tendrils on proximity

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Lore Stone (World 4) — hidden behind an obsidian formation. Use dash to break through a cracked obsidian wall.

**Scripted Events:**
- Environmental puzzle: three magma redirect valves must be turned (interact) to divert magma flow toward the shadow-obsidian shell, weakening it for the boss fight.

**Exit/Transition:** Completing the puzzle → Scene 4-4 (pre-boss) → Scene 4-B (boss).

---

### Scene 4-4: Cinderforge Depths — Hearthstone Vault

**Visual Theme:** The chamber directly around the Forge Hearthstone. White stone First Keeper architecture partially melted and fused with volcanic rock. The shadow-obsidian shell around the Hearthstone has cracked from the redirected magma but hasn't broken. The Molten Warden stands between Solen and the Hearthstone.

**Platformer Physics Enabled:** Same as 4-3.

**Tileset:** `ts_cinderforge` + `ts_hearthstone_chamber`

**Background:** Forge Hearthstone in cracked shadow shell, white stone and obsidian.

**Enemy Types:** None (pre-boss)

**Hazards:** None

**Collectibles and Secrets:**
- 1 Ember Shard (on a high ledge — requires dash + wall jump combo)

**Scripted Events:**
- The Molten Warden emerges from the shadow-obsidian shell. Boss intro cutscene.

**Exit/Transition:** → Scene 4-B.

---

### Scene 4-B: Cinderforge Depths — Boss Arena (Molten Warden)

**Visual Theme:** Hearthstone vault, locked arena. Wide platform with magma pits on either side. The Hearthstone is at the back center. Two elevated platforms (broken First Keeper pillars). Lava geysers at set positions.

**Platformer Physics Enabled:**
- Gravity: YES (128)
- Jump: YES (160)
- Double Jump: NO
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_cinderforge` + `ts_boss_arena`

**Enemy Types:** Molten Warden (boss — 3 phases)

**Hazards:**
- Magma Pits (sides of arena)
- Lava Geysers (timed eruptions on arena floor)
- Falling Slag: chunks of molten metal flung by the Warden's attacks

**Collectibles and Secrets:** None

**Scripted Events:**
- Boss intro/outro
- Post-boss: Wrench's reunion scene. Edric's figurine. Story Beat 4.

**Exit/Transition:** Post-boss → World Map.

---

## World 5: The Spire Ascent

### Scene 5-1: The Spire Ascent — Floating Platforms

**Visual Theme:** A vertical ascent through open sky. Floating rock platforms, anchored by ancient chains to the ground far below, provide the path upward. The platforms are irregular — some rotate, some bob up and down, some are one-way crumble platforms. The sky is dark purple, dominated by the Spire above, which is surrounded by a dome of swirling shadow energy. Below, the clouds are visible, lit faintly by the reignited Hearthstones.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (height 176 — UPGRADED — all four Hearthstones empowering the lantern increases Solen's jump)
- Double Jump: YES (INTRODUCED HERE — the combined power of four Hearthstones grants Solen a double jump through the lantern)
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_spire_ascent`

**Background:** Dark purple sky, Spire silhouette above, cloud layer below, distant Hearthstone glows on the horizon.

**Foreground:** Chain links, floating debris, shadow wisps.

**Enemy Types:**
- Hollow Wisp (3 — more aggressive than previous versions, follow player)
- Gloom Bat (2 — dive-bomb pattern)
- Spire Sentry (1 — new enemy, armored humanoid on a platform, throws shadow javelins)

**Hazards:**
- Bottomless Pit: falling below the cloud layer = death
- Crumbling Platforms: one-use, break after 0.5 seconds
- Shadow Wisps: environmental — wisps of Hollow energy that deal 1 HP on contact, drift in patterns

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (on a far-off floating platform, requires double jump + dash to reach)

**Scripted Events:**
- First use of double jump: brief camera focus and text ("The lantern pulses — you feel lighter. The combined power of four Hearthstones surges through you.").

**Exit/Transition:** Top edge → Scene 5-2.

---

### Scene 5-2: The Spire Ascent — Shadow Dome

**Visual Theme:** Passing through the shadow dome surrounding the Spire. The environment is visually oppressive: the screen darkens significantly, visibility is reduced to a small radius around Solen's lantern, and shadow tendrils reach toward the player from all directions. The platforms here are chunks of Spire stone that have been torn loose and float in the shadow dome's energy.

**Platformer Physics Enabled:**
- Gravity: YES (128)
- Jump: YES (176)
- Double Jump: YES
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_spire_ascent` + `ts_shadow_dome`

**Background:** Near-black with faint purple swirls. Visibility limited to lantern radius.

**Foreground:** Shadow tendrils reaching from edges, particles of darkness.

**Enemy Types:**
- Hollow Wisp (3)
- Shadow Stalker (2 — new enemy, invisible until within lantern light radius, then lunges)

**Hazards:**
- Reduced Visibility: the player can only see ~4 tiles around the lantern
- Shadow Tendrils: environmental hazard at screen edges, deal 1 HP if player strays too far from the center path
- Crumbling Platforms

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (hidden in the darkest corner — only visible when the player is standing on an adjacent platform and the lantern illuminates the alcove)

**Scripted Events:** None (atmosphere and tension)

**Exit/Transition:** Right/up edge → Scene 5-3.

---

### Scene 5-3: The Spire — Grand Hall

**Visual Theme:** The interior of the Spire's main hall. Once magnificent — marble floors, vaulted ceilings, stained-glass windows depicting the First Keepers — now corrupted. The marble is cracked and stained purple-black. The stained glass is shattered, with fragments rearranged to show Varek's face. Lamplighter banners hang in tatters. Shadow energy pulses through the hall like veins.

**Platformer Physics Enabled:**
- Gravity: YES (128)
- Jump: YES (176)
- Double Jump: YES
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: YES (banner cloth, scaffolding)
- Floating: NO

**Tileset:** `ts_spire_interior`

**Background:** Vaulted hall, broken stained glass, torn banners, shadow veins.

**Foreground:** Falling glass shards (decorative), dust particles.

**Enemy Types:**
- Spire Sentry (2)
- Shadow Stalker (2)
- Hollow Wisp (1)

**Hazards:**
- Broken Glass Floor: certain tiles shatter when stepped on, dropping player to a lower section
- Shadow Vein Pulses: periodic energy pulses along floor/wall veins that deal 2 HP

**Collectibles and Secrets:**
- 3 Flame Coins
- 1 Ember Shard (behind a torn Lamplighter banner — attack the banner to reveal an alcove)
- 1 Lore Stone (World 5) — in a hidden room accessed by dashing through a cracked stained-glass window

**Scripted Events:**
- Environmental: interacting with torn Lamplighter banners triggers brief text memories from Solen.

**Exit/Transition:** Right edge → Scene 5-4.

---

### Scene 5-4: The Spire — Shade's Chamber (Mini-Boss)

**Visual Theme:** A circular chamber with a high domed ceiling. The room is empty except for shadow energy swirling in the center. When Solen enters, the doors seal behind her. Shade materializes from the shadow energy. The lighting is dramatic: a single shaft of lantern light against swirling purple darkness.

**Platformer Physics Enabled:**
- Gravity: YES (128)
- Jump: YES (176)
- Double Jump: YES
- Wall Jump: YES (on chamber walls)
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_spire_interior` + `ts_boss_arena`

**Background:** Circular domed chamber, shadow energy, sealed doors.

**Enemy Types:** Shade/Aldric (mini-boss)

**Hazards:**
- Shadow Pools: Shade leaves pools of shadow on the ground that linger for 3 seconds

**Collectibles and Secrets:** None

**Scripted Events:**
- Pre-fight: Shade confronts Solen. Full dialogue.
- Post-fight: Shade's mask breaks. Aldric revealed. Death dialogue. Solen takes his Lamplighter badge.

**Exit/Transition:** Doors unseal → Scene 5-5.

---

### Scene 5-5: The Spire — Hearthstone Chamber

**Visual Theme:** The pinnacle of the Spire. A vast circular chamber with the Spire Hearthstone — the largest, a towering white crystal — at the center, encased in a massive shell of Hollow energy. The ceiling is open to the sky (the shadow dome swirls above). Varek floats before the Hearthstone, arms spread, absorbing its energy. The room is lit by competing lights: Solen's amber lantern and Varek's violet Hollow energy.

**Platformer Physics Enabled:**
- Gravity: YES (128)
- Jump: YES (176)
- Double Jump: YES
- Wall Jump: YES
- Dash: YES
- Coyote Time: YES (6 frames)
- Ladders: NO
- Floating: NO

**Tileset:** `ts_spire_interior` + `ts_hearthstone_chamber` + `ts_boss_arena`

**Background:** Spire Hearthstone in Hollow shell, open sky with shadow dome, Varek floating.

**Enemy Types:** Varek / The Hollow King (final boss — 2 phases)

**Hazards:**
- Phase 1: Shadow bolts, hollow waves, summoned shadow creatures
- Phase 2: Arena tiles crack and fall, revealing void beneath; Varek grows larger and attacks cover more area

**Collectibles and Secrets:** None

**Scripted Events:**
- Pre-fight: Varek's full dialogue with Solen. The philosophical confrontation.
- Phase transition: cutscene of Varek absorbing more Hollow energy, growing.
- Defeat: Varek collapses, Hollow energy dissipates from Hearthstone. Reignition sequence.
- Normal ending plays if true ending conditions not met.
- If true ending conditions ARE met: after Varek's defeat, a stairway opens in the floor leading to Scene 6-1.

**Exit/Transition:** Normal ending → Credits. True ending → Scene 6-1.

---

## Secret Area: Chamber of Origin

### Scene 6-1: Chamber of Origin

**Visual Theme:** A hidden chamber beneath the Spire Hearthstone, accessible only with all 25 Ember Shards and all 5 Lore Stones. The chamber is pristine white stone — the only place in Lumara untouched by the Hollow or the passage of time. First Keeper murals in perfect condition cover every wall, depicting the creation of Lumara, the Hearthstones, and the sealing of the Hollow. At the center of the room, on a pedestal, sits the Lantern of Origin — a small, perfectly crafted crystal lantern that glows with pure white light.

**Platformer Physics Enabled:**
- Gravity: YES (standard 128)
- Jump: YES (160)
- Double Jump: YES
- Wall Jump: NO (smooth walls)
- Dash: NO (peaceful scene)
- Coyote Time: YES
- Ladders: NO
- Floating: NO

**Tileset:** `ts_chamber_of_origin`

**Background:** Pristine white stone, First Keeper murals, soft white glow.

**Foreground:** Gentle light particles, motes of dust in light beams.

**Enemy Types:** None

**Hazards:** None

**Collectibles and Secrets:**
- The Lantern of Origin (key item — interact with pedestal to acquire)

**Scripted Events:**
- Entering: Solen reads the murals (dialogue events explaining the Lantern of Origin's purpose and cost).
- Acquiring the Lantern: dialogue choice — "Activate the Lantern of Origin?" YES/NO. Choosing YES triggers the true ending sequence.
- True ending cinematic plays.

**Exit/Transition:** True ending → Credits (alternate version).
