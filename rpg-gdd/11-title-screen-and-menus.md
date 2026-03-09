# 11 — Title Screen and Menus

---

## Title Screen

### Full Description

The title screen is a single 160x144 pixel background image displayed when the game boots up. It serves as the first impression of the game and must communicate the tone, setting, and genre immediately.

**Visual Composition:**

The background depicts the Chronospire silhouetted against a twilight sky, viewed from across the Stillwater Basin. The tower rises from the center-right of the image, impossibly tall and narrow, with glowing Aether lines tracing its surface. The sky transitions from deep indigo at the top to warm amber at the horizon, suggesting both sunset and foreboding. Cracks of pale blue Aether energy fracture the sky around the tower — the visible scars of the Shattering.

In the foreground (bottom third of the image), the Stillwater Basin's calm water reflects the tower and sky. A small silhouette of a boat is visible on the water in the lower-left — a subtle foreshadowing of the final journey.

The game logo, "CHRONOSPIRE," is positioned in the upper-left quadrant, rendered in a stylized pixel font with a clock-gear motif integrated into the letter O. Below the logo, the subtitle "The Shattered Meridian" is rendered in a smaller, elegant script-style pixel font.

A slow 2-frame animation cycles the Aether cracks in the sky (subtle brightness pulse), giving the static screen a sense of life.

### Layout

```
+--------------------------------------+
|  CHRONOSPIRE                         |
|  The Shattered Meridian              |
|                                      |
|                    [Chronospire      |
|                     Tower            |
|                     Silhouette]      |
|           [Aether cracks in sky]     |
|  ~~~~~~~~~~~~~~~~~~~~~~~~~horizon~~~~|
|  ~~[boat]~~~water reflection~~~~~~~~~|
|--------------------------------------|
|     > New Game                       |
|       Continue                       |
|                    (c) 2026          |
+--------------------------------------+
```

- **Logo Position:** Top-left quadrant, y:8 to y:32.
- **Tower:** Center-right, from y:24 to y:104.
- **Horizon:** y:104.
- **Water/Reflection:** y:104 to y:128.
- **Menu:** Bottom, y:120 to y:140.
- **Copyright:** Bottom-right, y:136.

### Palette (Title Screen Background)

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#0A0A1A` | Deep indigo (sky top, water) |
| Color 2 | `#2A2A5A` | Medium indigo (sky, tower) |
| Color 3 | `#C08030` | Warm amber (horizon glow) |
| Color 4 | `#80C0E0` | Pale Aether blue (cracks, reflections) |

### Menu Options

| Option | Description |
|--------|-------------|
| New Game | Starts a new game from the opening cutscene |
| Continue | Loads saved game data (only visible if save data exists) |

### Menu Flow

1. **On boot:** Title screen background fades in over 1 second. Title theme music begins.
2. **Logo animation:** The game logo fades in letter by letter (or simply appears after a brief delay if animation is too complex for GB Studio).
3. **Menu appears:** After 2 seconds or on any button press, the menu options appear at the bottom of the screen.
4. **Navigation:** D-pad Up/Down to toggle between New Game and Continue. A to confirm.
5. **New Game selected:** Fade to black. Initialize all variables to default values (HP, level, gold, etc.). Load opening cutscene scene. Begin game.
6. **Continue selected:** Execute GB Studio "Load Data" event. Read saved scene ID and position. Switch to saved scene. Resume gameplay.
7. **If no save data exists:** "Continue" option is either hidden or grayed out. Only "New Game" is available.

### Copyright and Version

Bottom of screen: `(c) 2026` and version number (e.g., `v1.0`), rendered in the smallest readable pixel font size.

---

## Game Logo

### Description

The game logo reads "CHRONOSPIRE" in a custom pixel font with integrated thematic elements. The word is rendered in two tones — the main letters in warm gold with a dark indigo shadow/outline. The letter "O" in CHRONOSPIRE is replaced with (or contains within it) a small clock gear icon, reinforcing the clockwork theme. The gear has four spokes and a center dot.

Below the main title, "The Shattered Meridian" is rendered in a smaller, thinner pixel font in pale Aether blue, slightly italic to contrast with the blocky title font.

### Logo Dimensions

- **Full logo area:** 128x32 pixels (fits within the 160-pixel screen width with margins).
- **"CHRONOSPIRE" text:** 128x16 pixels, centered.
- **"The Shattered Meridian" text:** 112x8 pixels, centered below.

### Logo Palette

| Color | Hex | Role |
|-------|-----|------|
| Main Text | `#D0A030` | Warm gold |
| Shadow/Outline | `#1A1A2A` | Deep indigo |
| Gear Detail | `#C08030` | Amber |
| Subtitle | `#80C0E0` | Pale Aether blue |

### Pixel Art Generation Prompt — Title Screen Background (160x144)

> "160x144 pixel art title screen background for a Game Boy Color RPG called 'Chronospire: The Shattered Meridian'. Scene: tall clock tower (the Chronospire) silhouetted against a twilight sky, viewed across a calm inland sea. Sky transitions from deep indigo at top to warm amber at horizon. Pale blue Aether energy cracks fracture the sky around the tower. Calm water in foreground reflects the tower. Small boat silhouette on the water. Space in upper-left for game logo, space at bottom for menu text. GBC 4-color palette: #0A0A1A (deep indigo), #2A2A5A (medium indigo), #C08030 (warm amber), #80C0E0 (pale Aether blue). Clean pixel art, no anti-aliasing, indexed color, atmospheric and somber."

### Pixel Art Generation Prompt — Game Logo

> "128x32 pixel art game logo for a Game Boy Color RPG titled 'CHRONOSPIRE'. Blocky custom pixel font with a clock gear integrated into the letter O. Main text in warm gold with deep indigo shadow/outline. Below in smaller thinner pale Aether blue text: 'The Shattered Meridian'. Logo area: 128x32 pixels. Palette: #D0A030 (gold), #1A1A2A (indigo shadow), #C08030 (amber gear), #80C0E0 (blue subtitle). Clean pixel art, no anti-aliasing, transparent background for overlay use."

---

## New Game Initialization

When the player selects "New Game":

1. **Fade to black** (1 second).
2. **Initialize all variables:**
   - Player stats: Level 1, HP 28, ATK 8, DEF 6, SPD 10, MP 12.
   - Gold: 0.
   - Inventory: All items set to 0.
   - Equipment: Apprentice Wrench (weapon), Linen Shirt (armor), Brass Goggles (accessory).
   - Story flags: All set to 0 (no quests started, no Meridians restored).
   - Companion flags: None active.
   - Keeper Fragments: None collected.
3. **Switch to opening cutscene scene** (`alaric_workshop` for the opening sequence).
4. **Fade in.** Opening cutscene begins.

---

## Continue / Load Game

When the player selects "Continue":

1. **Execute Load Data event** (GB Studio's built-in SRAM load).
2. **All variables restored** from saved state.
3. **Read `VAR_SAVE_SCENE`** to determine which scene to load.
4. **Switch to saved scene.** Set player position to saved X/Y coordinates.
5. **Fade in.** Gameplay resumes.

---

## Options

The game does not include a separate Options menu in the initial release. Sound can be controlled through the Game Boy's physical volume wheel. A potential future update could add:
- Text speed setting (Slow / Normal / Fast)
- Button remapping (limited by GB hardware)
- Sound toggle (Music On/Off, SFX On/Off)

These would be implemented as additional variables saved to SRAM.

---

*Chronospire: The Shattered Meridian — Title Screen and Menus Document*
