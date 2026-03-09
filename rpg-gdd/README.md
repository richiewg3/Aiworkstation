# Chronospire: The Shattered Meridian

**A GB Studio 4.2 Top-Down RPG for Game Boy Color**

> *"Time fractures. Memory fades. Only the brave dare mend what the tower has broken."*

**Genre:** Narrative Action RPG | **Platform:** Game Boy Color (via GB Studio 4.2) | **Resolution:** 160x144 | **Estimated Playtime:** 8–12 hours

---

## Summary

In the world of Aethermere, colossal clock towers known as Meridians regulate the flow of time across every region. When the central Chronospire shatters—fracturing time itself—a young clockmaker's apprentice named Edyn must journey across a land torn between frozen moments and accelerated decay. Armed with a broken pocket watch left behind by their missing mentor, Edyn must repair the five Meridian Cores, confront the Epoch Warden who shattered time on purpose, and rescue the one person who believed in them. The journey spans lush forests locked in eternal autumn, coastal towns reliving the same storm, crystallized deserts where sand hangs motionless in the air, and the twisted corridors of the Chronospire itself. Every battle is fought through a fully scripted turn-based combat system, every item tracked through variable-driven inventory, and every choice etched into a world that remembers what you did—and what you failed to do.

---

## Table of Contents

| # | Document | Description |
|---|----------|-------------|
| 1 | [Game Identity](01-game-identity.md) | Title, genre, tone, inspirations, and audience |
| 2 | [Story and World Lore](02-story-and-world-lore.md) | Full world building, story beats, and endings |
| 3 | [Characters](03-characters.md) | Player, party, NPCs, villains — stats, sprites, dialogue |
| 4 | [World Map and Areas](04-world-map-and-areas.md) | Every scene, region, and dungeon described in full |
| 5 | [Combat System](05-combat-system.md) | Full scripted turn-based battle system for GB Studio |
| 6 | [Progression and RPG Systems](06-progression-and-rpg-systems.md) | Leveling, equipment, magic, shops, and saving |
| 7 | [Enemies](07-enemies.md) | All enemy types with stats, behavior, and sprites |
| 8 | [Bosses](08-bosses.md) | All boss encounters with phases, dialogue, and arenas |
| 9 | [Tilesets and Environments](09-tilesets-and-environments.md) | Every tileset with palettes and pixel art prompts |
| 10 | [UI and HUD](10-ui-and-hud.md) | All interface elements, layouts, and triggers |
| 11 | [Title Screen and Menus](11-title-screen-and-menus.md) | Title screen, logo, and menu flow |
| 12 | [Items and Equipment](12-items-and-equipment.md) | Full master item list with stats, locations, and prices |
| 13 | [Quests and Progression](13-quests-and-progression.md) | Main quest line and all side quests with flag variables |
| 14 | [Dialogue and Script](14-dialogue-and-script.md) | Full scripts for cutscenes, NPCs, signs, shops |
| 15 | [Sound and Music](15-sound-and-music.md) | All music tracks and sound effects |
| 16 | [GB Studio Project Structure](16-gbstudio-project-structure.md) | Variables, scenes, custom events, build settings |
| 17 | [Dev Roadmap](17-dev-roadmap.md) | Phased development plan |
| 18 | [Asset Prompts](asset-prompts.md) | All pixel art generation prompts in one place |

---

## Technical Specifications

| Spec | Value |
|------|-------|
| Engine | GB Studio 4.2 |
| Export Format | Game Boy Color ROM (.gbc) |
| Resolution | 160x144 pixels |
| Tile Size | 8x8 pixels |
| Movement Grid | 16x16 pixels |
| Scene Type | Top Down 2D |
| Color Mode | GBC — 8 BG palettes, 8 sprite palettes, 4 colors each |
| Max Actors/Scene | 20 (stable), 10 visible on screen |
| Max Background Size | 32x32 tiles (256x256 pixels) |
| ROM Limit | 4MB |
| Standard Sprite Size | 16x16 pixels |
| Boss Sprite Size | 16x32 pixels |
| Spritesheet States | Idle (4 dir), Walk (4 dir), Interact |
| Music Format | hUGETracker, 4-channel GB audio |
| Audio Channels | Pulse 1, Pulse 2, Wave, Noise |
| Combat System | Fully scripted (variables, conditionals, scene switches) |
| Dialogue | Display Dialogue event, 16x16 portrait |
| Inventory | Variable-driven with overlay/menu scripts |
| Art Style | Pixel art, indexed color, GBC palette |

---

*Chronospire: The Shattered Meridian — Game Design Document v1.0*
