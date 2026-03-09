# 16 — GB Studio Project Structure

---

## Folder and File Structure

```
chronospire-project/
├── project.gbsproj                    # GB Studio project file
├── assets/
│   ├── backgrounds/
│   │   ├── title_screen.png           # 160x144 title screen background
│   │   ├── game_over.png             # 160x144 game over screen
│   │   ├── battle_arena.png          # 160x144 battle scene background
│   │   ├── millhaven_town_square.png  # 256x256 town background
│   │   ├── alaric_workshop.png       # 160x144 interior
│   │   ├── wynns_shop.png            # 160x144 interior
│   │   ├── verdant_south_road.png    # 256x224 overworld
│   │   ├── oakwatch_grove.png        # 256x256 overworld
│   │   ├── verdant_meridian_f1.png   # 256x256 dungeon
│   │   ├── verdant_meridian_f2.png   # 256x256 dungeon
│   │   ├── verdant_meridian_vault.png # 160x144 boss room
│   │   ├── verdant_west_road.png     # 256x224 connector
│   │   ├── stormhaven_town.png       # 256x256 town
│   │   ├── stormhaven_harbor.png     # 256x224 town
│   │   ├── stormhaven_warehouse.png  # 160x144 interior
│   │   ├── cliff_path_tidal.png      # 256x224 overworld
│   │   ├── tidal_meridian_f1.png     # 256x256 dungeon
│   │   ├── tidal_meridian_f2.png     # 256x256 dungeon
│   │   ├── tidal_meridian_sanctum.png # 160x144 boss room
│   │   ├── ashenveil_north_road.png  # 256x224 connector
│   │   ├── ashenveil_outer_bog.png   # 256x256 overworld
│   │   ├── architect_ruins.png       # 256x224 landmark
│   │   ├── hollow_meridian_approach.png # 160x144
│   │   ├── hollow_meridian_f1.png    # 256x256 dungeon
│   │   ├── hollow_meridian_f2.png    # 256x256 dungeon
│   │   ├── hollow_meridian_depths.png # 160x144 boss room
│   │   ├── crystalfall_border.png    # 256x224 connector
│   │   ├── crystalfall_expanse.png   # 256x256 overworld
│   │   ├── frozen_caravan.png        # 160x144 event
│   │   ├── crystal_canyon.png        # 256x256 overworld
│   │   ├── prism_meridian_f1.png     # 256x256 dungeon
│   │   ├── prism_meridian_f2.png     # 256x256 dungeon
│   │   ├── prism_meridian_sanctum.png # 160x144 boss room
│   │   ├── ironpeak_pass.png         # 256x224 connector
│   │   ├── ironpeak_enclave.png      # 256x256 town
│   │   ├── enclave_deep_forge.png    # 160x144 interior
│   │   ├── enclave_archives.png      # 160x144 interior
│   │   ├── stillwater_crossing.png   # 256x144 transition
│   │   ├── chronospire_base.png      # 256x224 overworld
│   │   ├── chronospire_f1.png        # 256x256 dungeon
│   │   ├── chronospire_f2.png        # 256x256 dungeon
│   │   ├── chronospire_f3.png        # 256x256 dungeon
│   │   ├── chronospire_f4.png        # 256x256 dungeon
│   │   ├── chronospire_f5_warden.png # 160x144 boss room
│   │   ├── chronospire_stasis.png    # 160x144 cutscene
│   │   └── chronospire_heart.png     # 160x144 secret boss
│   │
│   ├── sprites/
│   │   ├── player/
│   │   │   └── edyn.png              # 48x64 (3 cols x 4 rows for idle/walk)
│   │   ├── party/
│   │   │   ├── lira.png
│   │   │   ├── rook.png
│   │   │   └── sable.png
│   │   ├── npcs/
│   │   │   ├── alaric.png
│   │   │   ├── bram.png
│   │   │   ├── serea.png
│   │   │   ├── corwin.png
│   │   │   ├── illion.png
│   │   │   ├── pip.png
│   │   │   ├── captain_maren.png
│   │   │   ├── dara.png
│   │   │   ├── haldric.png
│   │   │   ├── wynn.png
│   │   │   ├── forge_blacksmith.png
│   │   │   ├── tully.png
│   │   │   ├── kira.png
│   │   │   ├── fisherman_garl.png
│   │   │   ├── nessa.png
│   │   │   ├── lost_traveler.png
│   │   │   └── generic_villager.png  # Reusable for minor NPCs
│   │   ├── enemies/
│   │   │   ├── aether_wisp.png
│   │   │   ├── temporal_beetle.png
│   │   │   ├── gear_sprite.png
│   │   │   ├── corroded_automaton.png
│   │   │   ├── coastal_crab.png
│   │   │   ├── storm_gull.png
│   │   │   ├── tide_lurker.png
│   │   │   ├── aether_jellyfish.png
│   │   │   ├── bog_rat.png
│   │   │   ├── rot_vine.png
│   │   │   ├── decay_phantom.png
│   │   │   ├── fungal_creep.png
│   │   │   ├── sand_sentinel.png
│   │   │   ├── crystal_scarab.png
│   │   │   ├── prism_wisp.png
│   │   │   ├── refracted_shard.png
│   │   │   ├── mountain_wolf.png
│   │   │   ├── frost_golem.png
│   │   │   ├── temporal_shade.png
│   │   │   ├── aether_construct.png
│   │   │   └── loop_wraith.png
│   │   └── bosses/
│   │       ├── corroded_timekeeper.png    # 16x32 boss sprite
│   │       ├── keeper_corwin_boss.png     # 16x32
│   │       ├── marsh_colossus.png         # 16x32
│   │       ├── refracted_guardian.png     # 16x32
│   │       ├── vasael_overworld.png       # 16x16 overworld sprite
│   │       ├── vasael_boss.png            # 16x32 boss sprite
│   │       └── heart_chronospire.png      # 16x32
│   │
│   ├── avatars/                           # 16x16 dialogue portraits
│   │   ├── edyn_portrait.png
│   │   ├── lira_portrait.png
│   │   ├── rook_portrait.png
│   │   ├── sable_portrait.png
│   │   ├── alaric_portrait.png
│   │   ├── vasael_portrait.png
│   │   ├── serea_portrait.png
│   │   ├── corwin_portrait.png
│   │   ├── illion_portrait.png
│   │   ├── bram_portrait.png
│   │   ├── pip_portrait.png
│   │   ├── maren_portrait.png
│   │   ├── dara_portrait.png
│   │   ├── haldric_portrait.png
│   │   ├── wynn_portrait.png
│   │   └── forge_portrait.png
│   │
│   ├── music/
│   │   ├── 01_title_theme.uge
│   │   ├── 02_millhaven.uge
│   │   ├── 03_verdant_overworld.uge
│   │   ├── 04_dungeon.uge
│   │   ├── 05_stormhaven.uge
│   │   ├── 06_ashenveil.uge
│   │   ├── 07_crystalfall.uge
│   │   ├── 08_ironpeak.uge
│   │   ├── 09_battle.uge
│   │   ├── 10_boss_battle.uge
│   │   ├── 11_final_boss.uge
│   │   ├── 12_secret_boss.uge
│   │   ├── 13_victory.uge
│   │   ├── 14_chronospire.uge
│   │   ├── 15_ending.uge
│   │   └── 16_stillwater.uge
│   │
│   ├── sounds/
│   │   ├── menu_select.vgm
│   │   ├── menu_cancel.vgm
│   │   ├── cursor_move.vgm
│   │   ├── text_advance.vgm
│   │   ├── chest_open.vgm
│   │   ├── item_get.vgm
│   │   ├── save.vgm
│   │   ├── player_attack.vgm
│   │   ├── enemy_attack.vgm
│   │   ├── magic_cast.vgm
│   │   ├── heal.vgm
│   │   ├── heavy_hit.vgm
│   │   ├── enemy_defeat.vgm
│   │   ├── level_up.vgm
│   │   ├── door_open.vgm
│   │   ├── puzzle_solve.vgm
│   │   ├── clock_tick.vgm
│   │   ├── shattering.vgm
│   │   ├── watch_glow.vgm
│   │   ├── storm_loop.vgm
│   │   ├── decay_damage.vgm
│   │   ├── freeze_unfreeze.vgm
│   │   ├── boss_phase.vgm
│   │   ├── flee_success.vgm
│   │   ├── flee_fail.vgm
│   │   ├── poison_tick.vgm
│   │   ├── game_over.vgm
│   │   ├── epoch_fracture.vgm
│   │   └── heart_pulse.vgm
│   │
│   └── ui/
│       ├── font.png                       # Game font spritesheet
│       ├── cursor.png                     # Menu cursor sprite
│       └── frame.png                      # Dialogue box frame
│
└── README.md                              # Project build notes
```

---

## Full Variable List

### Player Stats

| Variable | Purpose |
|----------|---------|
| `VAR_PLAYER_LEVEL` | Current level (1–30) |
| `VAR_PLAYER_XP` | Total accumulated XP |
| `VAR_PLAYER_LEVEL_THRESHOLD` | XP needed for next level |
| `VAR_PLAYER_HP` | Current HP |
| `VAR_PLAYER_MAX_HP` | Maximum HP |
| `VAR_PLAYER_ATK` | Current ATK (base + equipment) |
| `VAR_PLAYER_DEF` | Current DEF (base + equipment) |
| `VAR_PLAYER_SPD` | Current SPD (base + equipment) |
| `VAR_PLAYER_MP` | Current MP |
| `VAR_PLAYER_MAX_MP` | Maximum MP |
| `VAR_PLAYER_GOLD` | Gold currency |
| `VAR_PLAYER_BASE_ATK` | Base ATK from level (before equipment) |
| `VAR_PLAYER_BASE_DEF` | Base DEF from level |
| `VAR_PLAYER_BASE_SPD` | Base SPD from level |

### Equipment

| Variable | Purpose |
|----------|---------|
| `VAR_EQUIP_WEAPON_EDYN` | Edyn's equipped weapon ID (1–7) |
| `VAR_EQUIP_ARMOR_EDYN` | Edyn's equipped armor ID (1–7) |
| `VAR_EQUIP_ACCESSORY_EDYN` | Edyn's equipped accessory ID (1–9) |
| `VAR_EQUIP_WEAPON_LIRA` | Lira's weapon ID |
| `VAR_EQUIP_ARMOR_LIRA` | Lira's armor ID |
| `VAR_EQUIP_ACCESSORY_LIRA` | Lira's accessory ID |
| `VAR_EQUIP_WEAPON_ROOK` | Rook's weapon ID |
| `VAR_EQUIP_ARMOR_ROOK` | Rook's armor ID |
| `VAR_EQUIP_ACCESSORY_ROOK` | Rook's accessory ID |

### Companion Stats

| Variable | Purpose |
|----------|---------|
| `VAR_COMP_ACTIVE` | Active companion (0=none, 1=Lira, 2=Rook) |
| `VAR_LIRA_LEVEL` | Lira's level |
| `VAR_LIRA_XP` | Lira's XP |
| `VAR_LIRA_HP` | Lira's current HP |
| `VAR_LIRA_MAX_HP` | Lira's max HP |
| `VAR_LIRA_ATK` | Lira's ATK |
| `VAR_LIRA_DEF` | Lira's DEF |
| `VAR_LIRA_SPD` | Lira's SPD |
| `VAR_LIRA_MP` | Lira's current MP |
| `VAR_LIRA_MAX_MP` | Lira's max MP |
| `VAR_ROOK_LEVEL` | Rook's level |
| `VAR_ROOK_XP` | Rook's XP |
| `VAR_ROOK_HP` | Rook's HP |
| `VAR_ROOK_MAX_HP` | Rook's max HP |
| `VAR_ROOK_ATK` | Rook's ATK |
| `VAR_ROOK_DEF` | Rook's DEF |
| `VAR_ROOK_SPD` | Rook's SPD |
| `VAR_ROOK_MP` | Rook's MP |
| `VAR_ROOK_MAX_MP` | Rook's max MP |
| `VAR_LIRA_AFFINITY` | Lira affinity score (0–20) |
| `VAR_ROOK_AFFINITY` | Rook affinity score (0–20) |

### Inventory (Consumables)

| Variable | Purpose |
|----------|---------|
| `VAR_ITEM_POTION` | Potion quantity |
| `VAR_ITEM_HI_POTION` | Hi-Potion quantity |
| `VAR_ITEM_MEGA_POTION` | Mega Potion quantity |
| `VAR_ITEM_AETHER_SMALL` | Small Aether Crystal quantity |
| `VAR_ITEM_AETHER_LARGE` | Large Aether Crystal quantity |
| `VAR_ITEM_ANTIDOTE` | Antidote quantity |
| `VAR_ITEM_SMOKE_BOMB` | Smoke Bomb quantity |
| `VAR_ITEM_HERBAL_SALVE` | Herbal Salve quantity |
| `VAR_ITEM_REVIVE_LEAF` | Revive Leaf quantity |
| `VAR_ITEM_AETHER_TONIC` | Aether Tonic quantity |

### Inventory (Equipment Owned Flags)

| Variable | Purpose |
|----------|---------|
| `VAR_OWN_WEAPON_02` through `VAR_OWN_WEAPON_15` | Flags: owns weapon (0/1) |
| `VAR_OWN_ARMOR_02` through `VAR_OWN_ARMOR_15` | Flags: owns armor (0/1) |
| `VAR_OWN_ACC_02` through `VAR_OWN_ACC_09` | Flags: owns accessory (0/1) |

### Key Items

| Variable | Purpose |
|----------|---------|
| `VAR_HAS_POCKET_WATCH` | Has pocket watch (always 1 until true ending sacrifice) |
| `VAR_HAS_TRAVEL_PACK` | Has travel pack |
| `VAR_HAS_MERIDIAN_COMPASS` | Has Meridian Compass |
| `VAR_HAS_CALIBRATION_KEY` | Has Calibration Key (consumed on use) |
| `VAR_HAS_STORM_LANTERN` | Has Storm Lantern |
| `VAR_HAS_IRON_COG` | Has Iron Cog |
| `VAR_HAS_PRISM_LENS` | Has Prism Lens |
| `VAR_ITEM_ARCHITECT_ALLOY` | Architect Alloy quantity (material, can have multiple) |
| `VAR_HAS_ENERGY_CELL` | Has Rook's Energy Cell |
| `VAR_HAS_HALDRIC_ORDERS` | Has Haldric's Orders |
| `VAR_HAS_WARDEN_SEAL` | Has Warden's Seal |
| `VAR_HAS_SABLE_SATCHEL` | Has Sable's Satchel |
| `VAR_HAS_LOOPFIN` | Has Loopfin (fishing quest) |

### Keeper Fragments

| Variable | Purpose |
|----------|---------|
| `VAR_FRAGMENT_VERDANT` | Has Verdant Fragment (0/1) |
| `VAR_FRAGMENT_TIDAL` | Has Tidal Fragment (0/1) |
| `VAR_FRAGMENT_HOLLOW` | Has Hollow Fragment (0/1) |
| `VAR_FRAGMENT_PRISM` | Has Prism Fragment (0/1) |
| `VAR_FRAGMENT_CHRONO` | Has Chronospire Fragment (0/1) |

### Story/Quest Flags

| Variable | Purpose |
|----------|---------|
| `VAR_MQ01_SHATTERING` | Main quest 1 state (0–2) |
| `VAR_MQ02_VERDANT` | Main quest 2 state (0–3) |
| `VAR_MQ03_STORMHAVEN` | Main quest 3 state (0–3) |
| `VAR_MQ04_HOLLOW` | Main quest 4 state (0–4) |
| `VAR_MQ05_PRISM` | Main quest 5 state (0–5) |
| `VAR_MQ06_IRONPEAK` | Main quest 6 state (0–3) |
| `VAR_MQ07_CHRONOSPIRE` | Main quest 7 state (0–5) |
| `VAR_MQ08_HEART` | Main quest 8 state (0–3) |
| `VAR_SQ01_FISHING` | Side quest: Fishing (0–3) |
| `VAR_SQ02_LOST` | Side quest: Lost Traveler (0–3) |
| `VAR_SQ03_ROOK` | Side quest: Rook's Redemption (0–3) |
| `VAR_SQ04_HERBS` | Side quest: Lira's Herbs (0–4) |
| `VAR_SQ05_DELIVERY` | Side quest: Sable's Delivery (0–2) |
| `VAR_SQ06_KEEPER_LEGACY` | Side quest: Dead Keeper's Legacy (0–2) |
| `VAR_SQ07_BLESSING` | Side quest: Tideborn Blessing (0–2) |
| `VAR_SQ08_NOTES` | Side quest: Alaric's Notes (0–5) |

### Meridian Status

| Variable | Purpose |
|----------|---------|
| `VAR_MERIDIAN_VERDANT` | Verdant Meridian restored (0/1) |
| `VAR_MERIDIAN_TIDAL` | Tidal Meridian restored (0/1) |
| `VAR_MERIDIAN_HOLLOW` | Hollow Meridian restored (0/1) |
| `VAR_MERIDIAN_PRISM` | Prism Meridian restored (0/1) |

### Spell Unlock Flags

| Variable | Purpose |
|----------|---------|
| `VAR_SPELL_AETHER_BOLT` | Edyn: Aether Bolt unlocked (always 1) |
| `VAR_SPELL_TEMPORAL_SLOW` | Edyn: Temporal Slow unlocked |
| `VAR_SPELL_CHRONO_STRIKE` | Edyn: Chrono Strike unlocked |
| `VAR_SPELL_CHRONO_SHIELD` | Edyn: Chrono Shield unlocked (requires Tideborn Relic) |
| `VAR_SPELL_EPOCH_BURST` | Edyn: Epoch Burst unlocked |

### Combat Variables

| Variable | Purpose |
|----------|---------|
| `VAR_ENEMY_ID` | Current enemy type ID |
| `VAR_ENEMY_HP` | Enemy current HP |
| `VAR_ENEMY_MAX_HP` | Enemy max HP |
| `VAR_ENEMY_ATK` | Enemy ATK |
| `VAR_ENEMY_DEF` | Enemy DEF |
| `VAR_ENEMY_SPD` | Enemy SPD |
| `VAR_ENEMY_XP` | XP reward |
| `VAR_ENEMY_GOLD` | Gold reward |
| `VAR_ENEMY_PHASE` | Boss phase (1–3) |
| `VAR_TURN_ORDER` | Turn order (0=player first, 1=enemy first) |
| `VAR_PLAYER_ACTION` | Player selected action (1–4) |
| `VAR_COMP_ACTION` | Companion selected action |
| `VAR_MAGIC_SELECT` | Selected spell ID |
| `VAR_ITEM_SELECT` | Selected item ID |
| `VAR_DAMAGE_CALC` | Damage calculation temp |
| `VAR_TEMP_1` | General temp variable 1 |
| `VAR_TEMP_2` | General temp variable 2 |
| `VAR_BATTLE_STATE` | Battle flow state |
| `VAR_STATUS_PLAYER` | Player status (0=none, 1=poison, 2=slow, 3=guard) |
| `VAR_STATUS_COMP` | Companion status |
| `VAR_STATUS_ENEMY` | Enemy status |
| `VAR_FLEE_SUCCESS` | Flee result |
| `VAR_BOSS_FLAG` | Boss fight flag (0=normal, 1=boss, 2=secret boss) |
| `VAR_GUARD_ACTIVE` | Guard state for damage halving |
| `VAR_ENEMY_DEFEATED` | ID of defeated overworld enemy (for removal) |
| `VAR_COMP_HP` | Active companion HP (combat copy) |
| `VAR_COMP_MAX_HP` | Active companion max HP (combat copy) |
| `VAR_COMP_ATK` | Active companion ATK (combat copy) |
| `VAR_COMP_DEF` | Active companion DEF (combat copy) |
| `VAR_COMP_SPD` | Active companion SPD (combat copy) |
| `VAR_COMP_MP` | Active companion MP (combat copy) |
| `VAR_COMP_MAX_MP` | Active companion max MP (combat copy) |

### System Variables

| Variable | Purpose |
|----------|---------|
| `VAR_RETURN_SCENE` | Scene to return to after battle |
| `VAR_RETURN_X` | Player X position to return to |
| `VAR_RETURN_Y` | Player Y position to return to |
| `VAR_CURRENT_REGION` | Current region (1–6) for palette/music |
| `VAR_SAVE_SCENE` | Scene ID for save data |
| `VAR_AT_SAVE_POINT` | Is player at save point (0/1) |
| `VAR_SABLE_IN_PARTY` | Is Sable in party (0/1) |
| `VAR_ILLION_CHOICE` | Illion moral choice result |
| `VAR_VISITED_VERDANT` | Visited Verdant region |
| `VAR_VISITED_STORMHAVEN` | Visited Stormhaven |
| `VAR_VISITED_ASHENVEIL` | Visited Ashenveil |
| `VAR_VISITED_CRYSTALFALL` | Visited Crystalfall |
| `VAR_VISITED_IRONPEAK` | Visited Ironpeak |
| `VAR_VISITED_CHRONOSPIRE` | Visited Chronospire |
| `VAR_PLAYTIME_MINUTES` | Play time tracker (minutes) |
| `VAR_PLAYTIME_HOURS` | Play time tracker (hours) |
| `VAR_MENU_CURSOR` | Menu cursor position |
| `VAR_RANDOM_SEED` | Cycling pseudo-random value (0–99) |

**Total estimated variables: ~150**

GB Studio 4.2 supports up to 512 variables, so this is well within limits.

---

## Scene List with GB Studio Scene Names

| # | Scene Name | Type | Background Size |
|---|-----------|------|----------------|
| 1 | `title_screen` | Title | 160x144 |
| 2 | `millhaven_town_square` | Top Down | 256x256 |
| 3 | `alaric_workshop` | Top Down | 160x144 |
| 4 | `wynns_shop` | Top Down | 160x144 |
| 5 | `verdant_south_road` | Top Down | 256x224 |
| 6 | `oakwatch_grove_entrance` | Top Down | 256x256 |
| 7 | `verdant_meridian_f1` | Top Down | 256x256 |
| 8 | `verdant_meridian_f2` | Top Down | 256x256 |
| 9 | `verdant_meridian_vault` | Top Down | 160x144 |
| 10 | `verdant_west_road` | Top Down | 256x224 |
| 11 | `stormhaven_town` | Top Down | 256x256 |
| 12 | `stormhaven_harbor` | Top Down | 256x224 |
| 13 | `stormhaven_warehouse` | Top Down | 160x144 |
| 14 | `cliff_path_tidal` | Top Down | 256x224 |
| 15 | `tidal_meridian_f1` | Top Down | 256x256 |
| 16 | `tidal_meridian_f2` | Top Down | 256x256 |
| 17 | `tidal_meridian_sanctum` | Top Down | 160x144 |
| 18 | `ashenveil_north_road` | Top Down | 256x224 |
| 19 | `ashenveil_outer_bog` | Top Down | 256x256 |
| 20 | `architect_ruins` | Top Down | 256x224 |
| 21 | `hollow_meridian_approach` | Top Down | 160x144 |
| 22 | `hollow_meridian_f1` | Top Down | 256x256 |
| 23 | `hollow_meridian_f2` | Top Down | 256x256 |
| 24 | `hollow_meridian_depths` | Top Down | 160x144 |
| 25 | `crystalfall_border` | Top Down | 256x224 |
| 26 | `crystalfall_expanse` | Top Down | 256x256 |
| 27 | `frozen_caravan` | Top Down | 160x144 |
| 28 | `crystal_canyon` | Top Down | 256x256 |
| 29 | `prism_meridian_f1` | Top Down | 256x256 |
| 30 | `prism_meridian_f2` | Top Down | 256x256 |
| 31 | `prism_meridian_sanctum` | Top Down | 160x144 |
| 32 | `ironpeak_pass` | Top Down | 256x224 |
| 33 | `ironpeak_enclave` | Top Down | 256x256 |
| 34 | `enclave_deep_forge` | Top Down | 160x144 |
| 35 | `enclave_archives` | Top Down | 160x144 |
| 36 | `stillwater_crossing` | Top Down | 256x144 |
| 37 | `chronospire_base` | Top Down | 256x224 |
| 38 | `chronospire_f1` | Top Down | 256x256 |
| 39 | `chronospire_f2` | Top Down | 256x256 |
| 40 | `chronospire_f3` | Top Down | 256x256 |
| 41 | `chronospire_f4` | Top Down | 256x256 |
| 42 | `chronospire_f5_warden` | Top Down | 160x144 |
| 43 | `chronospire_stasis` | Top Down | 160x144 |
| 44 | `chronospire_heart` | Top Down | 160x144 |
| 45 | `battle_arena` | Top Down | 160x144 |

**Total Scenes: 45** (43 gameplay + 1 title + 1 battle)

---

## Custom Events and Reusable Scripts

| Custom Event | Purpose |
|--------------|---------|
| `CE_Calculate_Damage` | Physical damage calculation |
| `CE_Calculate_Magic_Damage` | Magic damage calculation |
| `CE_Apply_Damage_To_Enemy` | Apply damage, check defeat |
| `CE_Apply_Damage_To_Player` | Apply damage, check death |
| `CE_Apply_Damage_To_Companion` | Apply damage, check KO |
| `CE_Load_Enemy_Stats` | Load stats by enemy ID |
| `CE_Display_Battle_HUD` | Update battle overlay display |
| `CE_Player_Action_Menu` | Show 4-option battle menu |
| `CE_Magic_Submenu` | Show spell selection |
| `CE_Item_Submenu` | Show item selection in battle |
| `CE_Enemy_AI_Standard` | Standard enemy decision tree |
| `CE_Enemy_AI_Boss` | Boss-specific AI with phases |
| `CE_Apply_Status_Effects` | End-of-round status processing |
| `CE_Check_Level_Up` | XP threshold check and stat update |
| `CE_Battle_Win` | Victory processing (XP, gold, loot) |
| `CE_Battle_Lose` | Game over screen |
| `CE_Flee_Attempt` | Flee calculation and result |
| `CE_Init_Battle` | Full battle initialization sequence |
| `CE_Shop_Buy` | Shop buy flow |
| `CE_Shop_Sell` | Shop sell flow |
| `CE_Equip_Item` | Equipment change and stat recalculation |
| `CE_Use_Item_Overworld` | Consumable use outside combat |
| `CE_Save_Game` | Save point interaction and data save |
| `CE_Load_Game` | Load data and scene transition |
| `CE_Update_Overworld_HUD` | Refresh HP/MP overlay on overworld |
| `CE_Transition_To_Battle` | Store position, fade, switch to battle |
| `CE_Return_From_Battle` | Restore position, remove enemy, fade in |
| `CE_Party_Menu` | Main pause menu |
| `CE_Inventory_Menu` | Item viewing/using submenu |
| `CE_Equipment_Menu` | Equipment viewing/changing submenu |
| `CE_Recalculate_Stats` | Rebuild final stats from base + equipment |

---

## Suggested Plugins

| Plugin | Purpose |
|--------|---------|
| Variable Operations Extended | Advanced math operations beyond GB Studio defaults (multiply, divide) |
| Screen Shake | Enhanced screen shake with configurable intensity |
| Palette Swap | Runtime palette swapping for regional battle backdrops |
| Timer Events | Frame-accurate timer events for storm loop and timed puzzles |

---

## Build Settings

| Setting | Value |
|---------|-------|
| Target Platform | Game Boy Color |
| Color Mode | GBC Only (recommended) |
| Player Speed | 1 (grid-based movement, 16px steps) |
| Default Scene Type | Top Down 2D |
| Cart Type | MBC5 with SRAM (for save data) |
| ROM Size Target | < 4MB |

---

## Estimated ROM Size

| Category | Estimated Size |
|----------|---------------|
| Background images (45 scenes) | ~1.2 MB |
| Sprite sheets (all characters, enemies, bosses) | ~300 KB |
| Music tracks (16 .uge files) | ~100 KB |
| Sound effects (30 .vgm files) | ~50 KB |
| Script data (dialogue, events, custom events) | ~200 KB |
| Tileset data | ~150 KB |
| Portrait images (16 avatars) | ~20 KB |
| Font and UI assets | ~10 KB |
| Engine overhead and headers | ~200 KB |
| **Estimated Total** | **~2.2 MB** |

This leaves approximately 1.8 MB of headroom under the 4 MB limit, which allows for:
- Additional scenes or expanded backgrounds
- More detailed sprite animations
- Additional music tracks
- Future content additions

### Staying Under 4 MB

- Reuse background tiles aggressively (tilesets shared across multiple scenes)
- Keep sprite animations to 2–3 frames per direction
- Limit music track length (16–48 bars per track)
- Use palette swaps instead of unique assets where possible (battle arena backdrop)
- Compress dialogue text (GB Studio handles this automatically)

---

*Chronospire: The Shattered Meridian — GB Studio Project Structure Document*
