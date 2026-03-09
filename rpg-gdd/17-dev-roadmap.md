# 17 — Dev Roadmap

---

## Development Philosophy

The build is structured in 9 phases, progressing from engine fundamentals to final polish. Each phase produces a playable (or testable) milestone. The combat system is built early because it is the most technically complex subsystem and benefits from extended testing. World building is done region by region to maintain momentum and allow iterative refinement.

**Estimated Total Development Time:** 6–12 months (solo developer, part-time)

---

## Phase 1: Engine Setup, Core Movement, Save System, Camera

**Duration:** 2–3 weeks

**Goal:** A working GB Studio project with player movement, scene transitions, save/load functionality, and the camera system. The player can walk around Millhaven and save their game.

### Tasks

| # | Task | Details |
|---|------|---------|
| 1.1 | Create GB Studio project | New project, set to GBC mode, Top Down 2D scene type |
| 1.2 | Configure build settings | GBC Only, MBC5 + SRAM, 160x144 resolution |
| 1.3 | Create placeholder tileset | Basic grass/path/wall tiles for testing |
| 1.4 | Build Millhaven Town Square scene | 32x32 tile background using placeholder tileset |
| 1.5 | Set up player sprite | Import Edyn spritesheet (idle + walk, 4 directions) |
| 1.6 | Configure grid-based movement | 16px grid, Top Down 2D movement |
| 1.7 | Build Alaric's Workshop interior scene | 20x18 tile interior scene |
| 1.8 | Implement door transitions | Scene switch on door interaction (A to enter, collision exit) |
| 1.9 | Implement save system | Save point actor at town well, Save Data event on interaction |
| 1.10 | Test save/load cycle | Save in Millhaven, close, reload, verify position and variables |
| 1.11 | Set up camera follow | Camera follows player, locks at scene edges |
| 1.12 | Create variable template | Initialize all core player stat variables with default values |
| 1.13 | Build title screen | Title screen background, New Game / Continue menu |
| 1.14 | Implement New Game initialization | Set all variables to defaults, switch to opening scene |
| 1.15 | Implement Continue / Load | Load saved data, switch to saved scene |

### Milestone Deliverable
Player can start a new game, walk around Millhaven, enter the workshop, save at the well, quit, reload, and continue from the save.

---

## Phase 2: Combat System Scripting

**Duration:** 3–4 weeks

**Goal:** A fully functional turn-based combat system with all core mechanics: attack, magic, items, flee, enemy AI, damage formulas, win/lose conditions. Testable against placeholder enemies.

### Tasks

| # | Task | Details |
|---|------|---------|
| 2.1 | Build battle arena scene | 20x18 tile battle backdrop, placeholder enemy actor |
| 2.2 | Create CE_Init_Battle | Custom event: store return scene, load enemy stats, set up HUD |
| 2.3 | Create CE_Load_Enemy_Stats | Conditional chain loading stats by VAR_ENEMY_ID |
| 2.4 | Create CE_Display_Battle_HUD | Overlay text showing HP/MP for all combatants |
| 2.5 | Create CE_Player_Action_Menu | 4-option menu: Attack, Magic, Item, Flee |
| 2.6 | Create CE_Calculate_Damage | Physical damage formula implementation |
| 2.7 | Implement Player Attack | Full attack flow: menu → damage calc → apply → display |
| 2.8 | Create CE_Apply_Damage_To_Enemy | Subtract damage, check for defeat |
| 2.9 | Create CE_Apply_Damage_To_Player | Subtract damage, check for death |
| 2.10 | Implement Enemy AI (standard) | CE_Enemy_AI_Standard: weighted random decision tree |
| 2.11 | Implement turn order | SPD comparison, slow status override |
| 2.12 | Create CE_Battle_Win | XP, Gold, loot awards, transition back to overworld |
| 2.13 | Create CE_Battle_Lose | Game Over screen, Continue/Title menu |
| 2.14 | Implement Magic submenu | Spell selection, MP check, damage/effect application |
| 2.15 | Implement Item submenu | Item selection, usage, quantity decrement |
| 2.16 | Implement Flee | Success calculation, boss flag check |
| 2.17 | Implement status effects | Poison, Slow, Stun, Guard — application and end-of-round processing |
| 2.18 | Create CE_Check_Level_Up | XP threshold check, stat increase, spell unlocks |
| 2.19 | Implement companion combat | Companion action menu, companion damage/healing |
| 2.20 | Create CE_Transition_To_Battle | Overworld enemy touch → fade → battle scene |
| 2.21 | Create CE_Return_From_Battle | Battle win → fade → return to overworld, remove enemy |
| 2.22 | Test full combat loop | 10+ test battles against various stat configurations |
| 2.23 | Implement boss flag system | VAR_BOSS_FLAG disables flee, enables phase transitions |
| 2.24 | Implement phase transitions | HP threshold checks, stat changes, dialogue mid-fight |

### Milestone Deliverable
Player can encounter an enemy on the overworld, enter combat, fight using all four menu options, win or lose, and return to the overworld. Level up works. Boss phase transitions work.

---

## Phase 3: World 1 Complete (Verdant Reach)

**Duration:** 3–4 weeks

**Goal:** The entire Verdant Reach is playable from the opening cutscene through the Verdant Meridian boss fight, including Lira joining the party.

### Tasks

| # | Task | Details |
|---|------|---------|
| 3.1 | Create Verdant Overworld tileset | Final pixel art tileset for outdoor scenes |
| 3.2 | Create Verdant Town tileset | Final tileset for Millhaven |
| 3.3 | Create Verdant Interior tileset | Final tileset for Workshop and Shop |
| 3.4 | Create Meridian Dungeon tileset | Final tileset for Verdant Meridian |
| 3.5 | Build final Millhaven scene | Replace placeholder with final art, place all NPCs |
| 3.6 | Script opening cutscene | Shattering sequence: dialogue, screen shake, palette change |
| 3.7 | Build Wynn's Shop | Interior scene, shop NPC with buy/sell script |
| 3.8 | Implement shop system | CE_Shop_Buy, CE_Shop_Sell custom events |
| 3.9 | Build Verdant South Road | Overworld scene with enemy encounters |
| 3.10 | Create enemy sprites | Aether Wisp, Temporal Beetle spritesheets |
| 3.11 | Populate enemies on overworld | Place enemy actors with On Touch combat triggers |
| 3.12 | Build Oakwatch Grove Entrance | Scene with Serea and Lira NPCs |
| 3.13 | Script Serea quest dialogue | Quest give, compass reward |
| 3.14 | Script Lira party join | Lira introduces herself, joins party, set VAR_COMP_ACTIVE |
| 3.15 | Build Verdant Meridian F1 | Dungeon scene with Gear Sprites, puzzle |
| 3.16 | Create Gear Sprite enemy | Spritesheet and combat stats |
| 3.17 | Implement gear puzzle | Interact with gear to open passage |
| 3.18 | Build Verdant Meridian F2 | Dungeon scene with time-dilation room |
| 3.19 | Create Corroded Automaton enemy | Spritesheet and combat stats |
| 3.20 | Build Verdant Meridian Vault | Boss room scene |
| 3.21 | Create Corroded Timekeeper boss | 16x32 spritesheet, boss AI script |
| 3.22 | Script boss fight (Timekeeper) | 2-phase fight with dialogue, rewards |
| 3.23 | Script Meridian restoration cutscene | Calibration Key use, compass award |
| 3.24 | Implement Keeper Fragment 1 | Hidden interactable after boss defeat |
| 3.25 | Build Verdant West Road | Connector scene to Stormhaven |
| 3.26 | Create all NPC portraits | 16x16 portraits for Edyn, Bram, Wynn, Serea, Lira |
| 3.27 | Compose Millhaven theme | Track 02 in hUGETracker |
| 3.28 | Compose Verdant Overworld theme | Track 03 |
| 3.29 | Compose Dungeon theme | Track 04 |
| 3.30 | Compose Battle theme | Track 09 |
| 3.31 | Playtest full Act 1 opening | Complete run from game start through Verdant Meridian |

### Milestone Deliverable
The game is playable from the title screen through the first dungeon and boss, with final art, music, and dialogue. Approximately 1–1.5 hours of content.

---

## Phase 4: Full World Build

**Duration:** 6–8 weeks

**Goal:** All remaining regions (Stormhaven, Ashenveil, Crystalfall, Ironpeak, Chronospire) are built with backgrounds, tilesets, NPC placement, enemy placement, and scene transitions.

### Tasks

| # | Task | Details |
|---|------|---------|
| 4.1 | Create Stormhaven Town tileset | Final art |
| 4.2 | Build all Stormhaven scenes (4) | Town, Harbor, Warehouse, Cliff Path |
| 4.3 | Create Tidal Dungeon tileset | Final art |
| 4.4 | Build Tidal Meridian scenes (3) | F1, F2, Sanctum |
| 4.5 | Create all Stormhaven enemies | Coastal Crab, Storm Gull, Tide Lurker, Aether Jellyfish sprites |
| 4.6 | Place NPCs and enemies in all Stormhaven scenes | Full population |
| 4.7 | Create Ashenveil Overworld tileset | Final art |
| 4.8 | Create Hollow Dungeon tileset | Final art |
| 4.9 | Build all Ashenveil scenes (6) | North Road, Outer Bog, Ruins, Approach, F1, F2, Depths |
| 4.10 | Create all Ashenveil enemies | Bog Rat, Rot Vine, Decay Phantom, Fungal Creep sprites |
| 4.11 | Place NPCs and enemies in all Ashenveil scenes | Full population |
| 4.12 | Create Crystalfall Overworld tileset | Final art |
| 4.13 | Create Prism Dungeon tileset | Final art |
| 4.14 | Build all Crystalfall scenes (7) | Border, Expanse, Caravan, Canyon, F1, F2, Sanctum |
| 4.15 | Create all Crystalfall enemies | Sand Sentinel, Crystal Scarab, Prism Wisp, Refracted Shard |
| 4.16 | Create Ironpeak tilesets (3) | Overworld, Town, Interior |
| 4.17 | Build all Ironpeak scenes (4) | Pass, Enclave, Forge, Archives |
| 4.18 | Create Ironpeak enemies | Mountain Wolf, Frost Golem sprites |
| 4.19 | Create Chronospire tileset | Main dungeon tileset + Heart gold variant |
| 4.20 | Build all Chronospire scenes (8) | Base, F1–F5, Stasis, Heart |
| 4.21 | Create Chronospire enemies | Temporal Shade, Aether Construct, Loop Wraith sprites |
| 4.22 | Create Stillwater tileset and scene | Basin crossing |
| 4.23 | Build Battle Arena scene | Generic battle backdrop with palette swap |
| 4.24 | Connect all scenes | Scene transitions (N/S/E/W/door) between every connected scene |
| 4.25 | Walk-through test | Walk the entire game world from Millhaven to Chronospire |

### Milestone Deliverable
The entire world is traversable. All scenes exist with final art. All enemies are placed. No story scripting yet for Regions 2–6 (that's Phase 5), but the physical world is complete.

---

## Phase 5: Story, Cutscenes, Full Dialogue

**Duration:** 4–5 weeks

**Goal:** All story events, cutscenes, NPC dialogue, and quest scripts are implemented across the full game.

### Tasks

| # | Task | Details |
|---|------|---------|
| 5.1 | Script Stormhaven story sequence | Captain Maren dialogue, storm loop events, Pip reunion |
| 5.2 | Script Corwin encounter and post-fight | Maddened dialogue, pocket watch healing, Meridian restore |
| 5.3 | Script Lira/Pip reunion cutscene | Warehouse scene auto-trigger |
| 5.4 | Script Millhaven return visit | Council plea, Bram's gift |
| 5.5 | Script Ashenveil story sequence | Rook intro, joins party |
| 5.6 | Script Architect Ruins lore | 3 tablet interactions, scroll for Rook's quest |
| 5.7 | Script Dead Keeper's journal and cache | Hollow Meridian F2 lore events |
| 5.8 | Script Crystalfall story sequence | Frozen world, Sable unfreezing, Sable joins |
| 5.9 | Script Illion moral choice | Dialogue tree with branching based on player choice |
| 5.10 | Script desert unfreeze cutscene | Montage after Prism Meridian restore |
| 5.11 | Script Ironpeak preparation | Dara lore, Forge crafting dialogue, shop NPCs |
| 5.12 | Script Rook/Haldric confrontation | Conditional on SQ03 evidence, dialogue branches |
| 5.13 | Script Stillwater crossing | Party dialogue on the boat |
| 5.14 | Script Chronospire F1–F4 events | Flashback rooms, loop puzzle, speed corridors, lore crystals |
| 5.15 | Script Vasael pre-fight cutscene | Full confrontation dialogue |
| 5.16 | Script Vasael post-fight | Transition to Stasis Chamber |
| 5.17 | Script Alaric rescue (normal ending) | Stasis release, reunion, Master Core repair |
| 5.18 | Script normal ending montage | Region recovery scenes, workshop finale |
| 5.19 | Script true ending gate | Fragment check on F4, hidden door opening |
| 5.20 | Script Heart of Chronospire dialogue | Tower consciousness speaks |
| 5.21 | Script pocket watch sacrifice | Cutscene event |
| 5.22 | Script true ending extended epilogue | Vasael release, golden Chronospire, new watch crafting |
| 5.23 | Implement all NPC dialogue trees | Condition-based dialogue (before quest / during / after) for all NPCs |
| 5.24 | Implement all sign text | All overworld signs |
| 5.25 | Implement all lore objects | Books, tablets, notes, crystal records |
| 5.26 | Implement all chest interactions | Open/closed states, item rewards |
| 5.27 | Create all remaining NPC portraits | All speaking characters need 16x16 portraits |
| 5.28 | Full dialogue playtest | Read through every dialogue path in the game |

### Milestone Deliverable
The game is fully playable as a narrative experience from start to finish, with both endings accessible.

---

## Phase 6: All Bosses

**Duration:** 2–3 weeks

**Goal:** All boss fights are fully implemented with unique AI, phase transitions, dialogue, and rewards.

### Tasks

| # | Task | Details |
|---|------|---------|
| 6.1 | Finalize Corroded Timekeeper | Polish Phase 2, test balance |
| 6.2 | Create Keeper Corwin boss sprite | 16x32 spritesheet |
| 6.3 | Script Corwin boss fight | Non-lethal, water mechanics, 2 phases |
| 6.4 | Create Marsh Colossus boss sprite | 16x32 spritesheet |
| 6.5 | Script Marsh Colossus fight | 2 phases, regeneration mechanic |
| 6.6 | Create Refracted Guardian boss sprite | 16x32 spritesheet |
| 6.7 | Script Refracted Guardian fight | Copy/decoy mechanic, 2 phases |
| 6.8 | Create Vasael boss sprite | 16x32 spritesheet |
| 6.9 | Script Vasael boss fight | 3 phases, Temporal Collapse mechanic, pocket watch counter |
| 6.10 | Implement final boss music switching | Phase-specific music sections |
| 6.11 | Create Heart of Chronospire boss sprite | 16x32 spritesheet |
| 6.12 | Script Heart boss fight | 3 phases, no items, HP drain mechanic |
| 6.13 | Compose Boss Battle theme | Track 10 |
| 6.14 | Compose Final Boss theme | Track 11 (multi-section) |
| 6.15 | Compose Secret Boss theme | Track 12 |
| 6.16 | Balance test all bosses | Multiple playthroughs at expected level ranges |

### Milestone Deliverable
All 6 boss fights are functional, balanced, and fully scripted with unique mechanics, dialogue, and music.

---

## Phase 7: Side Quests, Secrets, Items

**Duration:** 2–3 weeks

**Goal:** All side quests, optional content, hidden items, and the Keeper Fragment collection system are implemented.

### Tasks

| # | Task | Details |
|---|------|---------|
| 7.1 | Implement SQ01 Stormhaven Fishing | Timing-based fish catch, Loopfin, Lucky Coin reward |
| 7.2 | Implement SQ02 Lost Traveler | NPC follow mechanic, escort to road |
| 7.3 | Implement SQ03 Rook's Redemption | Evidence finding, conditional confrontation |
| 7.4 | Implement SQ04 Lira's Herbs | 3 collectible herb patches, crafting cutscene |
| 7.5 | Implement SQ05 Sable's Delivery | Item pickup and delivery between scenes |
| 7.6 | Implement SQ06 Dead Keeper's Legacy | Hidden bookshelf cache |
| 7.7 | Implement SQ07 Tideborn Blessing | Return-visit NPC dialogue and reward |
| 7.8 | Implement SQ08 Alaric's Notes | 5 interactable notes across the game |
| 7.9 | Place all hidden chests | Equipment, gold, consumables in non-obvious locations |
| 7.10 | Implement Keeper Fragment system | 5 fragment collection, true ending gate check |
| 7.11 | Implement companion affinity | Track dialogue choices, display affinity-dependent text |
| 7.12 | Implement Sable's passive bonuses | Haggle discount, item identification |
| 7.13 | Implement equipment crafting at Ironpeak | Material check, gold cost, item creation |
| 7.14 | Place all loot drops in enemy tables | Assign drop chances per enemy type |
| 7.15 | Implement all equipment | Ensure all weapons, armor, accessories are obtainable and equippable |
| 7.16 | Test all side quest flows | Complete every side quest start to finish |

### Milestone Deliverable
All optional content is functional. A completionist playthrough is possible. True ending path is fully accessible.

---

## Phase 8: Music, SFX, Polish

**Duration:** 3–4 weeks

**Goal:** All music tracks and sound effects are composed, implemented, and triggered correctly. Visual polish, screen effects, and animation refinement.

### Tasks

| # | Task | Details |
|---|------|---------|
| 8.1 | Compose remaining music tracks | Title, Stormhaven, Ashenveil, Crystalfall, Ironpeak, Chronospire, Victory, Ending, Stillwater |
| 8.2 | Create all sound effects | 30 SFX in VGM format |
| 8.3 | Assign music to all scenes | Correct track plays on each scene load |
| 8.4 | Assign SFX to all events | Menu, combat, puzzle, story triggers |
| 8.5 | Implement screen shake effects | Boss attacks, Shattering, phase transitions |
| 8.6 | Implement palette flash effects | Boss ultimate attacks, lightning, Aether surges |
| 8.7 | Implement fade in/out on all transitions | Smooth scene transitions throughout |
| 8.8 | Polish NPC movement patterns | Ensure all overworld NPCs have natural-looking patrol routes |
| 8.9 | Polish enemy movement patterns | Ensure enemies patrol in interesting, avoidable patterns |
| 8.10 | Refine dialogue pacing | Adjust text speed, pause lengths, portrait timing |
| 8.11 | Add ambient details | Animated tiles (water flow, torch flicker, crystal pulse) |
| 8.12 | Polish combat animations | Enemy flash on hit, attack motion, spell effects |
| 8.13 | Implement victory fanfare correctly | Plays on win, transitions to results |
| 8.14 | Polish title screen | Logo animation, Aether crack pulse, menu timing |
| 8.15 | Polish ending sequences | Timing, music sync, emotional pacing |
| 8.16 | Full visual consistency pass | Ensure palette consistency across all scenes |

### Milestone Deliverable
The game looks and sounds complete. All audiovisual elements are in place. The game feels polished and professional.

---

## Phase 9: Final ROM Build, Testing, Bugfix

**Duration:** 2–3 weeks

**Goal:** The game is thoroughly tested, all bugs are fixed, and a final ROM is built for release.

### Tasks

| # | Task | Details |
|---|------|---------|
| 9.1 | Full playthrough — normal ending | Play the entire game start to finish, normal ending |
| 9.2 | Full playthrough — true ending | Play with all fragments, true ending |
| 9.3 | Side quest regression test | Complete every side quest, verify rewards |
| 9.4 | Combat balance test | Fight every enemy type, every boss, at various levels |
| 9.5 | Edge case testing | Empty inventory in combat, 0 MP magic attempt, flee from every enemy type |
| 9.6 | Save/load stress test | Save at every save point, load each, verify data integrity |
| 9.7 | Scene transition test | Walk through every scene transition in both directions |
| 9.8 | Variable overflow check | Ensure no variable exceeds expected ranges (gold cap, HP cap) |
| 9.9 | Actor limit verification | Verify no scene exceeds 20 actors (10 visible) |
| 9.10 | ROM size check | Build ROM, verify under 4 MB |
| 9.11 | Emulator compatibility | Test on BGB, mGBA, and SameBoy emulators |
| 9.12 | Hardware test (if possible) | Test on real GBC hardware via flash cart |
| 9.13 | Fix all identified bugs | Prioritized by severity: crash > game-breaking > visual > minor |
| 9.14 | Final build | Export final .gbc ROM |
| 9.15 | Create release package | ROM file, README, manual (if desired), screenshots |
| 9.16 | Backup and archive | Archive final project files and ROM |

### Milestone Deliverable
A tested, polished, release-ready Game Boy Color ROM under 4 MB.

---

## Phase Summary

| Phase | Focus | Duration | Cumulative |
|-------|-------|----------|------------|
| 1 | Engine, movement, save | 2–3 weeks | 2–3 weeks |
| 2 | Combat system | 3–4 weeks | 5–7 weeks |
| 3 | Verdant Reach (World 1) | 3–4 weeks | 8–11 weeks |
| 4 | Full world build | 6–8 weeks | 14–19 weeks |
| 5 | Story, cutscenes, dialogue | 4–5 weeks | 18–24 weeks |
| 6 | All bosses | 2–3 weeks | 20–27 weeks |
| 7 | Side quests, secrets | 2–3 weeks | 22–30 weeks |
| 8 | Music, SFX, polish | 3–4 weeks | 25–34 weeks |
| 9 | Testing, bugfix, release | 2–3 weeks | 27–37 weeks |

**Total: 27–37 weeks (6–9 months)**

---

## Stretch Goals (Post-Release)

| Goal | Description |
|------|-------------|
| New Game Plus | Carry over equipment and level to a new playthrough with harder enemies |
| Additional Side Quests | 3–5 more side quests exploring companion backstories |
| Arena Mode | Repeatable combat challenges in the Ironpeak Enclave |
| Developer Commentary | Interactable objects that provide behind-the-scenes design notes |
| Speed Run Timer | Built-in timer for speedrun community |

---

*Chronospire: The Shattered Meridian — Dev Roadmap Document*
