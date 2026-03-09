# 15 — Dev Roadmap

---

## Overview

The full development of Ember Tide is broken into 6 phases. Each phase builds on the previous one and results in a testable milestone. The estimated total development time is **16–24 weeks** for a solo developer working part-time, or **8–12 weeks** full-time.

| Phase | Focus | Estimated Duration | Milestone |
|---|---|---|---|
| 1 | Core Mechanics Prototype | 2–3 weeks | Solen moves, jumps, attacks, and interacts with a test scene |
| 2 | First World Complete | 3–4 weeks | World 1 (Verdant Hollow) fully playable with boss, NPCs, collectibles |
| 3 | All Worlds and Enemies | 4–6 weeks | All 5 worlds playable with all enemies and bosses |
| 4 | Story, Cutscenes, Dialogue | 2–3 weeks | Full narrative layer integrated: cutscenes, dialogue, endings |
| 5 | Polish, Sound, Secrets | 2–4 weeks | Music, SFX, secrets, easter eggs, balancing, bug fixes |
| 6 | Final ROM Build and Testing | 1–2 weeks | Gold master ROM ready for distribution |

---

## Phase 1: Core Mechanics Prototype

**Goal:** Build the fundamental platformer systems in a single test scene. Everything in the game depends on these systems feeling right.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 1.1 | Project Setup | Create GB Studio 4.2 project, configure GBC mode, set up folder structure per 14-gbstudio-project-structure.md | Critical |
| 1.2 | Player Sprite (Placeholder) | Create a basic 16×16 Solen sprite with idle, walk, jump, fall, and attack animations. Can be rough/placeholder art. | Critical |
| 1.3 | Basic Movement | Implement walk (speed 96), gravity (128), and jump (height 160) using GB Studio's platformer scene type. Test feel and responsiveness. | Critical |
| 1.4 | Coyote Time | Implement 6-frame coyote time window. Test with various platform edge scenarios. | High |
| 1.5 | Attack System | Implement A-button attack with the lantern staff. 3-frame animation, 1.5-tile reach, hitbox active on frame 2. | Critical |
| 1.6 | Health System | Implement HP variable (start at 5), damage function with i-frames (60 frames), knockback, and HUD heart display. | Critical |
| 1.7 | Checkpoint System | Build the checkpoint lamppost save/respawn loop. Test death → respawn flow. | High |
| 1.8 | Test Scene | Build a single test scene with ground tiles, platforms, gaps, a ladder, and one enemy to validate all mechanics. | Critical |
| 1.9 | Basic Enemy | Implement one enemy type (Shadow Hare) with patrol behavior, contact damage, HP, and death animation. | High |
| 1.10 | Collectible Pickup | Implement Flame Coin collection with counter and SFX. | Medium |
| 1.11 | Interaction System | Build the A-button NPC/sign interaction with text display. | Medium |
| 1.12 | Custom Events | Build the core custom events: `CE_PlayerDamage`, `CE_PlayerDeath`, `CE_PlayerRespawn`, `CE_CollectFlameCoin`, `CE_UpdateHUD`. | High |

### Milestone Criteria

- [ ] Solen walks, jumps (with coyote time), and attacks in a test scene
- [ ] At least one enemy with patrol, HP, and death exists
- [ ] Player takes damage, has i-frames, and can die/respawn
- [ ] Checkpoints work (save/load position and HP)
- [ ] HUD displays hearts and coin count
- [ ] Interaction with at least one text-only sign works

---

## Phase 2: First World Complete

**Goal:** Build World 1 (Verdant Hollow) as a vertical slice — the complete player experience for one world, proving the game's design works end to end.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 2.1 | Prologue Scenes | Build Scenes 0-1 and 0-2 (Cinderhearth). Implement the opening tutorial and Hollow Surge cutscene. | Critical |
| 2.2 | Cinderhearth Tileset | Create `ts_cinderhearth` and `ts_cinderhearth_dark` tilesets with all required tiles. | Critical |
| 2.3 | Verdant Hollow Tileset | Create `ts_verdant_hollow`, `ts_mushroom_grotto`, and `ts_thornveil` tilesets. | Critical |
| 2.4 | Background Art (World 1) | Create all background images for Prologue and World 1 scenes. | High |
| 2.5 | Solen Final Sprite | Finalize Solen's full spritesheet with all animation states. | High |
| 2.6 | NPC Sprites (Prologue/W1) | Create sprites for Maren, Brennan, Fern. | High |
| 2.7 | NPC Portraits | Create 16×16 dialogue portraits for Maren, Brennan, Fern, Solen. | High |
| 2.8 | Enemy Sprites (W1) | Create sprites for Shadow Hare, Gloom Bat, Sporecap, Thorn Creeper. | High |
| 2.9 | Level Design (W1) | Build all 4 World 1 scenes + boss arena with tile placement, actor placement, and transitions. | Critical |
| 2.10 | Wall Jump Mechanic | Implement wall jump ability. Triggered by Fern in Scene 1-3. Test in Thornveil Thicket. | Critical |
| 2.11 | Ladder Mechanic | Implement ladder climbing on designated tiles. | High |
| 2.12 | Briar Sentinel Boss | Implement the boss with both phases, attack patterns, weak point, and defeat sequence. | Critical |
| 2.13 | Boss Arena System | Build the boss arena lock/unlock system, boss HP tracking, phase transitions. | Critical |
| 2.14 | Hearthstone Reignition | Implement the `CE_HearthstoneReignite` event with animation and lantern upgrade. | High |
| 2.15 | Dialogue System | Implement full Display Dialogue events with portraits for all Prologue and World 1 characters. | High |
| 2.16 | Collectibles (W1) | Place all Flame Coins, Ember Shards, Heart Crystal Pieces, and Lore Stone in World 1. Implement collection events. | Medium |
| 2.17 | Healing Tincture | Implement the tincture item — inventory count, use mechanic (heal 2 HP), refill at checkpoints. | Medium |
| 2.18 | World Map (Basic) | Build a basic world map scene showing Cinderhearth and World 1 nodes. | Medium |
| 2.19 | Pause Menu | Implement the pause menu with Resume, Inventory, Map, Options, Quit. | Medium |
| 2.20 | Title Screen | Build the title screen with background, logo, and New Game / Continue options. | Medium |
| 2.21 | Music (Prototype) | Compose or source placeholder tracks for: title screen, Cinderhearth, Hollow Tide surge, Verdant Hollow, boss battle. | Medium |

### Milestone Criteria

- [ ] Complete playthrough from title screen through prologue to end of World 1
- [ ] All World 1 enemies and the Briar Sentinel boss are functional
- [ ] Wall jump and ladder mechanics work correctly
- [ ] Dialogue with portraits works for all World 1 characters
- [ ] Collectibles are placed and collectible
- [ ] Pause menu and world map are functional
- [ ] The game feels good to play — movement is responsive, combat is satisfying

---

## Phase 3: All Worlds and Enemies

**Goal:** Build the remaining four worlds. Each world adds new mechanics, enemies, and a boss.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 3.1 | World 2 Tilesets | Create `ts_frostfang_peaks`, `ts_rimehaven_village`, `ts_ice_shelf`. | Critical |
| 3.2 | World 2 Backgrounds | Create all background images for World 2 scenes. | High |
| 3.3 | World 2 Level Design | Build all 4 World 2 scenes + boss arena. Implement ice physics (slippery tiles), wind gusts. | Critical |
| 3.4 | World 2 Enemies | Create and implement Frost Fang, Ice Shard, Hollow Wisp (World 2 variants). | Critical |
| 3.5 | Glacial Wyrm Boss | Implement with both phases, arena wind mechanic. | Critical |
| 3.6 | Orin NPC | Create sprite, portrait, dialogue. Implement wall jump upgrade. | High |
| 3.7 | World 3 Tilesets | Create `ts_sunken_brine`, `ts_first_keeper_ruins`, `ts_research_chamber`, `ts_keeper_cathedral`. | Critical |
| 3.8 | World 3 Backgrounds | Create all background images for World 3 scenes. | High |
| 3.9 | World 3 Level Design | Build all 4 World 3 scenes + boss arena. Implement swimming mechanics, breath timer, floating physics. | Critical |
| 3.10 | World 3 Enemies | Create and implement Brine Crawler, Jelly Drift, Ruin Guardian, Abyssal Eel. | Critical |
| 3.11 | Abyssal Leviathan Boss | Implement with both phases, underwater combat. | Critical |
| 3.12 | Coral NPC | Create sprite, portrait, dialogue. Implement locket fetch quest. | High |
| 3.13 | World 4 Tilesets | Create `ts_cinderforge`, `ts_forge_machinery`, `ts_obsidian_core`. | Critical |
| 3.14 | World 4 Backgrounds | Create all background images for World 4 scenes. | High |
| 3.15 | World 4 Level Design | Build all 4 World 4 scenes + boss arena. Implement conveyor belts, steam vents, magma redirect puzzles. | Critical |
| 3.16 | Dash Mechanic | Implement dash ability. Triggered by Wrench in Scene 4-1. | Critical |
| 3.17 | World 4 Enemies | Create and implement Slag Crawler, Ember Wisp, Shadow Smith. | Critical |
| 3.18 | Molten Warden Boss | Implement with all three phases. | Critical |
| 3.19 | Wrench NPC | Create sprite, portrait, dialogue. Implement figurine story moment. | High |
| 3.20 | World 5 Tilesets | Create `ts_spire_ascent`, `ts_shadow_dome`, `ts_spire_interior`. | Critical |
| 3.21 | World 5 Backgrounds | Create all background images for World 5 scenes. | High |
| 3.22 | World 5 Level Design | Build all 5 World 5 scenes + boss arenas. Implement double jump, shadow dome visibility. | Critical |
| 3.23 | Double Jump Mechanic | Implement double jump ability. Triggered at start of World 5. | Critical |
| 3.24 | World 5 Enemies | Create and implement Spire Sentry, Shadow Stalker. | Critical |
| 3.25 | Shade Mini-Boss | Implement with teleport mechanics and post-fight reveal. | Critical |
| 3.26 | Varek Final Boss | Implement with both phases, arena crumbling mechanic. | Critical |
| 3.27 | Shared Tilesets | Create `ts_hearthstone_chamber`, `ts_boss_arena`. | High |
| 3.28 | Collectibles (W2–W5) | Place all remaining Flame Coins, Ember Shards, Heart Pieces, Lore Stones across Worlds 2–5. | High |
| 3.29 | World Map (Full) | Expand world map to show all 5 worlds + Cinderhearth with proper node states. | Medium |
| 3.30 | Backtracking | Ensure all earlier worlds are accessible from the world map and that new abilities (dash, double jump) work in earlier scenes for secret access. | Medium |

### Milestone Criteria

- [ ] All 5 worlds fully playable from start to finish
- [ ] All enemies and bosses functional
- [ ] All movement mechanics (walk, jump, wall jump, dash, double jump, swim, climb) working
- [ ] All collectibles placed and collectible
- [ ] Backtracking to earlier worlds works and new abilities open secret areas
- [ ] World map reflects progress accurately

---

## Phase 4: Story, Cutscenes, Dialogue

**Goal:** Integrate the full narrative layer — all cutscenes, NPC dialogue, story beats, and endings.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 4.1 | Opening Text Crawl | Implement the scrolling text introduction. | High |
| 4.2 | Prologue Cutscene | Polish the Cinderhearth opening: lantern-lighting tutorial, Hollow Surge, Maren's petrification, Brennan's exposition. | Critical |
| 4.3 | All Boss Cutscenes | Implement all pre-fight and post-fight dialogue for every boss (Briar Sentinel, Glacial Wyrm, Abyssal Leviathan, Molten Warden, Shade, Varek). | Critical |
| 4.4 | Story Beat Scenes | Implement the 5 major story beats as in-game moments with full dialogue and emotional weight. | Critical |
| 4.5 | All NPC Dialogue | Implement complete dialogue trees for Fern, Orin, Coral, Wrench — first meeting, revisit after each world, and special dialogue. | High |
| 4.6 | Sign Text | Place and script all sign/hint text throughout every world. | Medium |
| 4.7 | Normal Ending | Implement the full normal ending sequence: Hearthstone reignition, montage, Cinderhearth reunion, ending text, credits. | Critical |
| 4.8 | True Ending | Implement the Chamber of Origin scene, Lantern of Origin activation, alternate ending sequence, alternate credits. | Critical |
| 4.9 | True Ending Gate | Implement the condition check (25 shards + 5 stones) that opens the stairway to the Chamber of Origin. | Critical |
| 4.10 | Chamber of Origin | Build Scene 6-1 with `ts_chamber_of_origin` tileset, murals, and Lantern of Origin interaction. | High |
| 4.11 | Credits Screens | Build normal and true ending credits scenes with scrolling text and appropriate backgrounds. | Medium |
| 4.12 | Varek's Journals | Implement the 3 interactive journal entries in Scene 3-3. | Medium |
| 4.13 | Environmental Text | Add all interaction text for petrified villagers, frozen villagers, and environmental objects. | Medium |
| 4.14 | Shade Dialogue (W3) | Implement the betrayal reveal dialogue after the Abyssal Leviathan fight. | High |
| 4.15 | All Portraits | Ensure all 9 character portraits are finalized and display correctly in dialogue boxes. | High |

### Milestone Criteria

- [ ] Complete playthrough from title screen to normal ending with full story
- [ ] Complete playthrough to true ending with all collectibles
- [ ] All NPC dialogue fully implemented and triggered correctly
- [ ] All cutscenes play at the right moments
- [ ] Story beats land emotionally — the writing works in the game context
- [ ] Both endings play correctly with appropriate credits

---

## Phase 5: Polish, Sound, Secrets

**Goal:** Add the final layer of quality — music, sound effects, secret content, balance adjustments, and visual polish.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 5.1 | Music Composition | Compose all 16 music tracks in hUGETracker. Test in-engine. | Critical |
| 5.2 | Sound Effects | Create all 28 sound effects. Test triggers and volumes. | Critical |
| 5.3 | Music Integration | Assign tracks to scenes, implement scene-change music transitions. | High |
| 5.4 | SFX Integration | Wire all SFX to their trigger events throughout the game. | High |
| 5.5 | Easter Eggs | Implement all 6 easter eggs (Lamplighter's Song, Fern's Encyclopedia, Wrench's Turrets, Developer's Message, Orin's Regret, Hidden Melody). | Medium |
| 5.6 | Hidden Rooms | Verify all 18 hidden rooms are accessible and reward correctly. | High |
| 5.7 | Balance Pass — Enemies | Playtest every enemy encounter. Adjust HP, damage, speed, and aggression triggers as needed. | High |
| 5.8 | Balance Pass — Bosses | Playtest every boss fight multiple times. Adjust phase HP, attack timing, telegraph windows, and weak point exposure times. | Critical |
| 5.9 | Balance Pass — Economy | Verify Flame Coin distribution: are there enough to buy needed tinctures? Too many? Adjust placement. | Medium |
| 5.10 | Balance Pass — Difficulty | Playtest the full critical path. Ensure it's completable by a moderately skilled player. Identify frustration points and add checkpoints or adjust hazard timing. | High |
| 5.11 | Art Polish | Review all sprites and tilesets for consistency. Fix any palette errors, alignment issues, or animation glitches. | High |
| 5.12 | Transition Polish | Ensure all scene transitions are smooth — correct fade timing, no visual glitches during loads. | Medium |
| 5.13 | Save System Testing | Test the save/load cycle extensively. Verify all flags and variables persist correctly. Test edge cases (save during boss fight, save with full inventory, etc.). | Critical |
| 5.14 | Performance Testing | Run the game on actual GBC hardware (or accurate emulator). Check for slowdown in actor-heavy scenes. Reduce actor counts if needed. | High |
| 5.15 | Backtracking Polish | Verify all backtracking paths work correctly. Ensure new abilities grant access to all intended secret areas. | Medium |
| 5.16 | HUD Polish | Verify HUD displays correctly in all scenes, doesn't overlap with important visual elements, and updates in real-time. | Medium |
| 5.17 | Dialogue Proofreading | Review all dialogue text for typos, line-break issues, and portrait alignment. | Medium |

### Milestone Criteria

- [ ] All music and SFX are in the game and playing correctly
- [ ] All easter eggs are functional
- [ ] Game has been fully playtested on GBC hardware/emulator
- [ ] No major bugs remaining
- [ ] Difficulty feels fair on the critical path
- [ ] All secret content is accessible and rewarding
- [ ] The game is fun to play from start to finish

---

## Phase 6: Final ROM Build and Testing

**Goal:** Produce the final, distributable Game Boy Color ROM file.

### Tasks

| # | Task | Description | Priority |
|---|---|---|---|
| 6.1 | Feature Freeze | No new features or content. Only bug fixes from this point. | Critical |
| 6.2 | Full Regression Test | Complete playthrough of the entire game (critical path + all secrets) looking for bugs. | Critical |
| 6.3 | Save Integrity Test | Load a save at every possible checkpoint. Verify all data loads correctly. | Critical |
| 6.4 | Edge Case Testing | Test unusual player behaviors: dying at exact moment of boss defeat, collecting items while taking damage, pausing during transitions, etc. | High |
| 6.5 | Hardware Test | Run the final build on real GBC hardware via flash cart. Verify all visual, audio, and gameplay elements. | Critical |
| 6.6 | Emulator Compatibility | Test on at least 3 major emulators: BGB, SameBoy, mGBA. Verify consistent behavior. | High |
| 6.7 | ROM Header | Verify ROM header data: game title ("EMBER TIDE"), color flag (GBC), MBC type (MBC5+RAM+BAT), ROM/RAM size. | High |
| 6.8 | Final Build | Export the final .gbc ROM from GB Studio. Verify file size is within 4 MB. | Critical |
| 6.9 | Checksum Verification | Verify ROM checksum is correct (some emulators/flash carts validate this). | Medium |
| 6.10 | Distribution Package | Prepare the distribution package: ROM file, README, manual/guide, screenshots. | Medium |
| 6.11 | Backup | Archive the complete project files, all assets, and the final ROM in at least 2 separate locations. | Critical |

### Milestone Criteria

- [ ] Final .gbc ROM exported and verified
- [ ] ROM runs correctly on real GBC hardware
- [ ] ROM runs correctly on BGB, SameBoy, and mGBA emulators
- [ ] No known game-breaking bugs
- [ ] Save system is reliable
- [ ] Project files are archived
- [ ] The game is complete

---

## Development Tools Required

| Tool | Purpose | Version |
|---|---|---|
| GB Studio | Game engine, scene editor, script editor | 4.2 |
| hUGETracker | Music composition | Latest |
| Aseprite (or similar) | Pixel art creation for all sprites, tilesets, backgrounds, and UI | Latest |
| BGB | Primary emulator for testing and debugging | Latest |
| SameBoy | Secondary emulator for compatibility testing | Latest |
| mGBA | Tertiary emulator for compatibility testing | Latest |
| Git | Version control | Latest |
| GB flash cart (e.g., EverDrive) | Hardware testing on real Game Boy Color | — |
