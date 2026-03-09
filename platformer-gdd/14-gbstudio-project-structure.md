# 14 — GB Studio Project Structure

---

## Project Folder Structure

The following is the file and folder organization inside the GB Studio 4.2 project directory.

```
ember-tide/
├── project.gbsproj                    # GB Studio project file
├── assets/
│   ├── backgrounds/
│   │   ├── bg_cinderhearth_dusk.png
│   │   ├── bg_cinderhearth_dark.png
│   │   ├── bg_verdant_hollow.png
│   │   ├── bg_mushroom_grotto.png
│   │   ├── bg_frostfang_peaks.png
│   │   ├── bg_ice_shelf_sky.png
│   │   ├── bg_sunken_brine.png
│   │   ├── bg_first_keeper_ruins.png
│   │   ├── bg_cinderforge.png
│   │   ├── bg_spire_ascent_sky.png
│   │   ├── bg_spire_interior.png
│   │   ├── bg_chamber_of_origin.png
│   │   ├── bg_hearthstone_chamber.png
│   │   ├── bg_title_screen.png
│   │   ├── bg_credits_normal.png
│   │   ├── bg_credits_true.png
│   │   └── bg_world_map.png
│   ├── sprites/
│   │   ├── player/
│   │   │   └── spr_solen.png           # Full spritesheet: all animation states
│   │   ├── npcs/
│   │   │   ├── spr_maren.png
│   │   │   ├── spr_brennan.png
│   │   │   ├── spr_fern.png
│   │   │   ├── spr_orin.png
│   │   │   ├── spr_coral.png
│   │   │   ├── spr_wrench.png
│   │   │   └── spr_petrified_villagers.png
│   │   ├── enemies/
│   │   │   ├── spr_shadow_hare.png
│   │   │   ├── spr_gloom_bat.png
│   │   │   ├── spr_sporecap.png
│   │   │   ├── spr_thorn_creeper.png
│   │   │   ├── spr_frost_fang.png
│   │   │   ├── spr_ice_shard.png
│   │   │   ├── spr_hollow_wisp.png
│   │   │   ├── spr_brine_crawler.png
│   │   │   ├── spr_jelly_drift.png
│   │   │   ├── spr_ruin_guardian.png
│   │   │   ├── spr_abyssal_eel.png
│   │   │   ├── spr_slag_crawler.png
│   │   │   ├── spr_ember_wisp.png
│   │   │   ├── spr_shadow_smith.png
│   │   │   ├── spr_spire_sentry.png
│   │   │   └── spr_shadow_stalker.png
│   │   ├── bosses/
│   │   │   ├── spr_briar_sentinel.png
│   │   │   ├── spr_glacial_wyrm.png
│   │   │   ├── spr_glacial_wyrm_body.png
│   │   │   ├── spr_abyssal_leviathan_tentacle.png
│   │   │   ├── spr_abyssal_leviathan_eye.png
│   │   │   ├── spr_molten_warden.png
│   │   │   ├── spr_shade.png
│   │   │   └── spr_varek.png
│   │   ├── projectiles/
│   │   │   ├── spr_spore_projectile.png
│   │   │   ├── spr_ice_shard_proj.png
│   │   │   ├── spr_energy_orb.png
│   │   │   ├── spr_fire_trail.png
│   │   │   ├── spr_shadow_bolt.png
│   │   │   ├── spr_shadow_tendril.png
│   │   │   ├── spr_ink_blob.png
│   │   │   ├── spr_magma_glob.png
│   │   │   └── spr_javelin.png
│   │   ├── items/
│   │   │   ├── spr_flame_coin.png
│   │   │   ├── spr_ember_shard.png
│   │   │   ├── spr_heart_crystal_piece.png
│   │   │   ├── spr_lore_stone.png
│   │   │   ├── spr_healing_tincture.png
│   │   │   ├── spr_corals_locket.png
│   │   │   ├── spr_aldrics_badge.png
│   │   │   ├── spr_edrics_figurine.png
│   │   │   └── spr_lantern_of_origin.png
│   │   └── effects/
│   │       ├── spr_explosion_shadow.png
│   │       ├── spr_heal_sparkle.png
│   │       ├── spr_lantern_glow.png
│   │       ├── spr_checkpoint_flame.png
│   │       └── spr_interaction_arrow.png
│   ├── tilesets/
│   │   ├── ts_cinderhearth.png
│   │   ├── ts_cinderhearth_dark.png
│   │   ├── ts_verdant_hollow.png
│   │   ├── ts_mushroom_grotto.png
│   │   ├── ts_thornveil.png
│   │   ├── ts_frostfang_peaks.png
│   │   ├── ts_rimehaven_village.png
│   │   ├── ts_ice_shelf.png
│   │   ├── ts_sunken_brine.png
│   │   ├── ts_first_keeper_ruins.png
│   │   ├── ts_research_chamber.png
│   │   ├── ts_keeper_cathedral.png
│   │   ├── ts_cinderforge.png
│   │   ├── ts_forge_machinery.png
│   │   ├── ts_obsidian_core.png
│   │   ├── ts_spire_ascent.png
│   │   ├── ts_shadow_dome.png
│   │   ├── ts_spire_interior.png
│   │   ├── ts_hearthstone_chamber.png
│   │   ├── ts_boss_arena.png
│   │   └── ts_chamber_of_origin.png
│   ├── music/
│   │   ├── mus_title_screen.uge
│   │   ├── mus_cinderhearth.uge
│   │   ├── mus_hollow_comes.uge
│   │   ├── mus_verdant_hollow.uge
│   │   ├── mus_thornveil_ascent.uge
│   │   ├── mus_frostfang_peaks.uge
│   │   ├── mus_ice_shelf.uge
│   │   ├── mus_sunken_brine.uge
│   │   ├── mus_first_keeper_archives.uge
│   │   ├── mus_cinderforge.uge
│   │   ├── mus_spire_ascent.uge
│   │   ├── mus_hollow_king.uge
│   │   ├── mus_dawn_returns.uge
│   │   ├── mus_starlight.uge
│   │   ├── mus_boss_battle.uge
│   │   └── mus_victory_jingle.uge
│   ├── sounds/
│   │   ├── sfx_jump.vgm
│   │   ├── sfx_double_jump.vgm
│   │   ├── sfx_land.vgm
│   │   ├── sfx_attack.vgm
│   │   ├── sfx_hit_enemy.vgm
│   │   ├── sfx_enemy_death.vgm
│   │   ├── sfx_player_hurt.vgm
│   │   ├── sfx_player_death.vgm
│   │   ├── sfx_coin_collect.vgm
│   │   ├── sfx_shard_collect.vgm
│   │   ├── sfx_heal.vgm
│   │   ├── sfx_checkpoint.vgm
│   │   ├── sfx_dialogue_open.vgm
│   │   ├── sfx_dialogue_char.vgm
│   │   ├── sfx_menu_move.vgm
│   │   ├── sfx_menu_select.vgm
│   │   ├── sfx_menu_cancel.vgm
│   │   ├── sfx_wall_jump.vgm
│   │   ├── sfx_dash.vgm
│   │   ├── sfx_hearthstone_reignite.vgm
│   │   ├── sfx_petrify.vgm
│   │   ├── sfx_boss_roar.vgm
│   │   ├── sfx_splash.vgm
│   │   ├── sfx_ladder_climb.vgm
│   │   ├── sfx_crumble.vgm
│   │   ├── sfx_wind_gust.vgm
│   │   ├── sfx_lore_stone.vgm
│   │   └── sfx_lantern_upgrade.vgm
│   ├── avatars/
│   │   ├── avatar_solen.png
│   │   ├── avatar_maren.png
│   │   ├── avatar_brennan.png
│   │   ├── avatar_fern.png
│   │   ├── avatar_orin.png
│   │   ├── avatar_coral.png
│   │   ├── avatar_wrench.png
│   │   ├── avatar_shade.png
│   │   └── avatar_varek.png
│   ├── fonts/
│   │   └── font_ember_tide.png         # Custom pixel font
│   └── ui/
│       ├── ui_frame.png                 # Dialogue box frame
│       ├── ui_cursor.png               # Menu cursor arrow
│       └── ui_hearts.png               # Heart icons (filled, empty, flash)
└── plugins/
    └── (see Suggested Plugins below)
```

---

## Full Variable List

All game state is tracked via GB Studio global variables. Variable names use a prefix system for organization.

### Player State Variables

| Variable Name | Type | Purpose |
|---|---|---|
| `VAR_PLAYER_HP` | Number (0–8) | Current player HP |
| `VAR_PLAYER_MAX_HP` | Number (5–8) | Maximum player HP (increases with Heart Crystals) |
| `VAR_PLAYER_TINCTURES` | Number (0–4) | Current healing tinctures |
| `VAR_PLAYER_MAX_TINCTURES` | Number (3–4) | Max tinctures (increases with Coral's quest) |
| `VAR_PLAYER_FLAME_COINS` | Number (0–999) | Flame Coin count |
| `VAR_PLAYER_FACING` | Number (0–1) | 0 = right, 1 = left |
| `VAR_PLAYER_INVINCIBLE` | Number (0–60) | Invincibility frame counter (counts down from 60) |

### Ability Flags

| Variable Name | Type | Purpose |
|---|---|---|
| `FLAG_HAS_WALL_JUMP` | Boolean | Wall jump ability unlocked |
| `FLAG_HAS_WALL_JUMP_PLUS` | Boolean | Enhanced wall jump (Orin's gear) |
| `FLAG_HAS_DASH` | Boolean | Dash ability unlocked |
| `FLAG_HAS_DOUBLE_JUMP` | Boolean | Double jump ability unlocked |
| `VAR_LANTERN_LEVEL` | Number (1–5) | Current lantern upgrade level |

### Collectible Tracking

| Variable Name | Type | Purpose |
|---|---|---|
| `VAR_EMBER_SHARDS` | Number (0–25) | Total Ember Shards collected |
| `FLAG_SHARD_01` through `FLAG_SHARD_25` | Boolean (×25) | Individual shard collection flags |
| `VAR_LORE_STONES` | Number (0–5) | Total Lore Stones collected |
| `FLAG_LORE_01` through `FLAG_LORE_05` | Boolean (×5) | Individual lore stone flags |
| `VAR_HEART_PIECES` | Number (0–12) | Heart Crystal Pieces collected |
| `FLAG_HEART_01` through `FLAG_HEART_12` | Boolean (×12) | Individual heart piece flags |
| `FLAG_HAS_LOCKET` | Boolean | Coral's Locket found |
| `FLAG_LOCKET_RETURNED` | Boolean | Locket returned to Coral |
| `FLAG_HAS_BADGE` | Boolean | Aldric's Badge obtained |
| `FLAG_HAS_FIGURINE` | Boolean | Edric's Figurine obtained |

### Story Progression Flags

| Variable Name | Type | Purpose |
|---|---|---|
| `FLAG_PROLOGUE_COMPLETE` | Boolean | Prologue finished (Maren petrified, Solen has lantern) |
| `FLAG_WORLD1_CLEAR` | Boolean | Verdant Hearthstone reignited |
| `FLAG_WORLD2_CLEAR` | Boolean | Frost Hearthstone reignited |
| `FLAG_WORLD3_CLEAR` | Boolean | Brine Hearthstone reignited |
| `FLAG_WORLD4_CLEAR` | Boolean | Forge Hearthstone reignited |
| `FLAG_WORLD5_CLEAR` | Boolean | Spire Hearthstone reignited / Varek defeated |
| `FLAG_TRUE_ENDING` | Boolean | True ending triggered |
| `FLAG_SHADE_REVEALED` | Boolean | Shade's betrayal dialogue seen (World 3) |
| `FLAG_SHADE_DEFEATED` | Boolean | Shade/Aldric mini-boss defeated |
| `FLAG_MURAL_SEEN` | Boolean | First Keeper mural discovered (World 2) |

### NPC Interaction Flags

| Variable Name | Type | Purpose |
|---|---|---|
| `FLAG_MET_FERN` | Boolean | First dialogue with Fern complete |
| `FLAG_MET_ORIN` | Boolean | First dialogue with Orin complete |
| `FLAG_MET_CORAL` | Boolean | First dialogue with Coral complete |
| `FLAG_MET_WRENCH` | Boolean | First dialogue with Wrench complete |
| `VAR_FERN_TALK_COUNT` | Number | Tracks how many times Fern has been spoken to (easter egg) |
| `VAR_WELL_INTERACT_COUNT` | Number | Tracks well interactions (easter egg) |

### Scene and Checkpoint Variables

| Variable Name | Type | Purpose |
|---|---|---|
| `VAR_CURRENT_SCENE` | Number | Current scene index |
| `VAR_CHECKPOINT_SCENE` | Number | Last checkpoint scene index |
| `VAR_CHECKPOINT_X` | Number | Last checkpoint X position |
| `VAR_CHECKPOINT_Y` | Number | Last checkpoint Y position |

### Boss State Variables

| Variable Name | Type | Purpose |
|---|---|---|
| `VAR_BOSS_HP` | Number | Current boss HP (used during boss fights) |
| `VAR_BOSS_PHASE` | Number (1–3) | Current boss phase |
| `VAR_BOSS_ATTACK_TIMER` | Number | Timer between boss attacks |
| `VAR_BOSS_PATTERN_INDEX` | Number | Tracks position in attack pattern sequence |

### Settings

| Variable Name | Type | Purpose |
|---|---|---|
| `FLAG_MUSIC_ON` | Boolean | Music enabled/disabled |
| `FLAG_SFX_ON` | Boolean | Sound effects enabled/disabled |
| `FLAG_GAME_COMPLETE` | Boolean | Game completed at least once (unlocks credits on title screen) |

**Total Variables: ~85**

---

## Scene List

All scenes in the game, matching GB Studio scene names. Scene type for all gameplay scenes is PLATFORMER.

| Scene ID | GB Studio Scene Name | Type | World |
|---|---|---|---|
| S_00_01 | `Cinderhearth_EveningRound` | PLATFORMER | Prologue |
| S_00_02 | `Cinderhearth_HollowSurge` | PLATFORMER | Prologue |
| S_01_01 | `VerdantHollow_AshenCanopy` | PLATFORMER | World 1 |
| S_01_02 | `VerdantHollow_MushroomGrotto` | PLATFORMER | World 1 |
| S_01_03 | `VerdantHollow_ThornveilThicket` | PLATFORMER | World 1 |
| S_01_04 | `VerdantHollow_HearthstoneClearing` | PLATFORMER | World 1 |
| S_01_B | `VerdantHollow_BossArena` | PLATFORMER | World 1 |
| S_02_01 | `FrostfangPeaks_LowerSlopes` | PLATFORMER | World 2 |
| S_02_02 | `FrostfangPeaks_Rimehaven` | PLATFORMER | World 2 |
| S_02_03 | `FrostfangPeaks_IceShelf` | PLATFORMER | World 2 |
| S_02_04 | `FrostfangPeaks_SummitShrine` | PLATFORMER | World 2 |
| S_02_B | `FrostfangPeaks_BossArena` | PLATFORMER | World 2 |
| S_03_01 | `SunkenBrine_CavernMouth` | PLATFORMER | World 3 |
| S_03_02 | `SunkenBrine_FloodedRuins` | PLATFORMER | World 3 |
| S_03_03 | `SunkenBrine_ResearchChamber` | PLATFORMER | World 3 |
| S_03_04 | `SunkenBrine_KeeperCathedral` | PLATFORMER | World 3 |
| S_03_B | `SunkenBrine_BossArena` | PLATFORMER | World 3 |
| S_04_01 | `CinderforgeDepts_MagmaTunnels` | PLATFORMER | World 4 |
| S_04_02 | `CinderforgeDepts_ForgeFloor` | PLATFORMER | World 4 |
| S_04_03 | `CinderforgeDepts_ObsidianCore` | PLATFORMER | World 4 |
| S_04_04 | `CinderforgeDepts_HearthstoneVault` | PLATFORMER | World 4 |
| S_04_B | `CinderforgeDepts_BossArena` | PLATFORMER | World 4 |
| S_05_01 | `SpireAscent_FloatingPlatforms` | PLATFORMER | World 5 |
| S_05_02 | `SpireAscent_ShadowDome` | PLATFORMER | World 5 |
| S_05_03 | `Spire_GrandHall` | PLATFORMER | World 5 |
| S_05_04 | `Spire_ShadeChamber` | PLATFORMER | World 5 |
| S_05_05 | `Spire_HearthstoneChamber` | PLATFORMER | World 5 |
| S_06_01 | `ChamberOfOrigin` | PLATFORMER | Secret |
| S_TITLE | `TitleScreen` | — | Menu |
| S_MAP | `WorldMap` | — | Menu |
| S_CREDITS_N | `Credits_Normal` | — | Menu |
| S_CREDITS_T | `Credits_True` | — | Menu |

**Total: 32 scenes**

---

## Custom Events and Reusable Scripts

GB Studio 4.2 supports Custom Events — reusable script blocks that can be called from any scene. The following custom events should be built:

### Player Systems

| Custom Event Name | Purpose | Parameters |
|---|---|---|
| `CE_PlayerDamage` | Apply damage to player, trigger i-frames, knockback, check death | `damage_amount`, `knockback_direction` |
| `CE_PlayerHeal` | Heal player HP, play heal SFX, flash hearts | `heal_amount` |
| `CE_PlayerDeath` | Play death animation, fade to black, respawn at checkpoint | — |
| `CE_PlayerRespawn` | Reload checkpoint scene, set position, restore HP/tinctures | — |
| `CE_UseTincture` | Consume a tincture, heal 2 HP, play SFX | — |
| `CE_CheckpointSave` | Save current scene, position, and all progress variables to SRAM | — |

### Collectible Systems

| Custom Event Name | Purpose | Parameters |
|---|---|---|
| `CE_CollectFlameCoin` | Increment coin counter, play SFX, check 50-coin heal | — |
| `CE_CollectEmberShard` | Increment shard counter, set individual flag, play splash animation | `shard_id` |
| `CE_CollectLoreStone` | Increment stone counter, set flag, display incantation fragment | `stone_id`, `text_fragment` |
| `CE_CollectHeartPiece` | Increment piece counter, check if 4 = upgrade, increase max HP | `piece_id` |

### Combat Systems

| Custom Event Name | Purpose | Parameters |
|---|---|---|
| `CE_EnemyDamage` | Apply damage to an enemy, check HP, trigger death if 0 | `enemy_actor`, `damage_amount` |
| `CE_EnemyDeath` | Play death animation, spawn drops, remove actor | `enemy_actor`, `drop_type` |
| `CE_SpawnProjectile` | Create a projectile actor at a position with a direction and speed | `x`, `y`, `direction`, `speed`, `damage` |
| `CE_BossPhaseCheck` | Check boss HP, trigger phase transition if threshold reached | `phase_threshold` |

### UI and Dialogue

| Custom Event Name | Purpose | Parameters |
|---|---|---|
| `CE_UpdateHUD` | Refresh HUD display — hearts, coins, tinctures | — |
| `CE_ShowDialogue` | Display dialogue with portrait, typewriter text, advance on A | `portrait_id`, `text` |
| `CE_ShowNarration` | Display text without portrait (environmental/narration) | `text` |
| `CE_SceneNameDisplay` | Show scene name for 3 seconds on entry, then fade | `scene_name` |
| `CE_EmberShardSplash` | Full-screen shard collection animation | `current_count` |

### World and Progression

| Custom Event Name | Purpose | Parameters |
|---|---|---|
| `CE_HearthstoneReignite` | Play reignition SFX/animation, set world clear flag, upgrade lantern | `world_number` |
| `CE_CheckTrueEnding` | Check if all 25 shards + 5 stones are collected, set flag | — |
| `CE_TransitionToScene` | Fade out, change scene, fade in, call scene name display | `target_scene`, `entry_x`, `entry_y` |

---

## Suggested Plugins

GB Studio 4.2 supports community plugins. The following are recommended:

| Plugin | Purpose | Notes |
|---|---|---|
| **Platformer Plus** | Enhanced platformer physics — coyote time, wall slide, variable jump height | Core gameplay plugin. Provides the advanced movement mechanics not available in base GB Studio platformer. |
| **Actor Limit Extender** | Optimizes actor rendering to maximize visible actors on screen | Helps maintain stable 10 visible actors. |
| **Save Manager** | Enhanced SRAM management with multiple save operations and data validation | Prevents save corruption. |
| **Screen Shake** | Adds screen shake effect for boss attacks, impacts, and dramatic moments | Visual juice. |
| **Fade Effects** | Custom fade transitions (iris wipe, dissolve, flash) beyond the default linear fade | Used for scene transitions and Hearthstone reignition sequences. |
| **Timer Plugin** | Adds countdown/count-up timer functionality for breath mechanics underwater | Required for the Sunken Brine breath timer. |

---

## Build Settings

| Setting | Value | Notes |
|---|---|---|
| Target Platform | GBC Only | Game Boy Color only — uses GBC color palettes and extended features. NOT DMG compatible. |
| Color Mode | GBC | 8 BG palettes, 8 sprite palettes, 4 colors each |
| ROM Size Target | 2 MB (est.) | Target: well under the 4 MB limit for comfortable margin |
| Cartridge Type | MBC5 + RAM + Battery | MBC5 for ROM banking, RAM for save data, Battery for SRAM persistence |
| Player Sprite Type | Platformer | Uses the PLATFORMER scene type for all gameplay scenes |
| Starting Scene | `TitleScreen` | The game begins on the title screen scene |
| Default Font | `font_ember_tide.png` | Custom pixel font at 8px height |
| Music Driver | hUGEDriver | Standard GB Studio music driver for hUGETracker files |

---

## Estimated ROM Size Breakdown

| Category | Estimated Size | Notes |
|---|---|---|
| Tile Data (21 tilesets × ~2 KB avg) | ~42 KB | Each tileset is a 128×128 PNG compressed to tile data |
| Background Maps (32 scenes × ~1 KB avg) | ~32 KB | Scene background tile map data |
| Background Images (17 images × ~2 KB avg) | ~34 KB | Parallax/background layer images |
| Sprite Data (~40 spritesheets × ~2 KB avg) | ~80 KB | All character, enemy, boss, item, effect spritesheets |
| Music (16 tracks × ~4 KB avg) | ~64 KB | hUGETracker modules |
| Sound Effects (28 SFX × ~0.5 KB avg) | ~14 KB | VGM sound effect data |
| Script/Dialogue Data | ~100 KB | All scene scripts, dialogue text, event logic |
| Avatar/Portrait Data (9 portraits × ~0.5 KB) | ~5 KB | 16×16 dialogue portraits |
| Font Data | ~2 KB | Custom font tileset |
| Engine Code (GB Studio runtime) | ~128 KB | Base engine, platformer physics, plugin code |
| Custom Event Scripts | ~30 KB | All reusable script logic |
| Variable/Flag Storage | ~1 KB | SRAM data structure |
| **ESTIMATED TOTAL** | **~532 KB** | **Well within the 4 MB (4,096 KB) limit** |

The estimated total of ~532 KB leaves substantial room for expansion. Even doubling the content would remain under 2 MB. The 4 MB limit is not a concern for this project.
