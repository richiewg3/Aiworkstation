# 10 — Title Screen & Menus

---

## Title Screen

### Full Description

The title screen is the first thing the player sees when the game boots. It establishes the mood, the world, and the stakes before a single button is pressed.

**Background Image:** A 160×144 pixel scene depicting a lone figure (Solen, in silhouette) standing on a hillside at dusk, holding a lantern staff. The lantern is the brightest point on the screen — a warm amber glow against a gradient sky that transitions from deep purple at the top (representing the Hollow Tide) to warm orange-pink at the horizon (representing the fading light of the Hearthstones). In the far background, five faint glows are visible along the horizon line — the five Hearthstones, dim but not yet dead. The foreground hillside has silhouetted grass and wildflowers.

**Game Logo:** "EMBER TIDE" is displayed in a custom pixel art logotype in the upper-center portion of the screen. The letters are styled to evoke both warmth and decay: the left side of each letter is warm amber-gold, transitioning to dark purple on the right, as if the letters themselves are caught between light and shadow. Below the logo, the tagline "Rekindle the light" appears in small white text.

**Animation:** The title screen has subtle animation:
- The lantern flame flickers (2-frame cycle)
- Stars in the upper-purple sky twinkle (random 2-frame cycle)
- The five Hearthstone glows pulse slowly (2-frame cycle, offset from each other)
- Grass on the foreground hill sways gently (2-frame cycle)

**Menu Options:** Below the logo and tagline, two menu options appear:

```
        ═══ EMBER TIDE ═══
         Rekindle the light

           ► NEW GAME
             CONTINUE
```

If no save data exists, "CONTINUE" is grayed out. The cursor (►) moves between options with D-pad Up/Down. Pressing A on "NEW GAME" begins the prologue. Pressing A on "CONTINUE" loads the last auto-save.

### Layout on 160×144 Screen

| Element | X | Y | Size | Alignment |
|---|---|---|---|---|
| Background Image | 0 | 0 | 160×144 px | Full screen |
| Game Logo | Center | 16 px from top | ~120×24 px | Centered horizontally |
| Tagline | Center | 44 px from top | Variable | Centered horizontally |
| "NEW GAME" | Center | 96 px from top | Variable | Centered horizontally |
| "CONTINUE" | Center | 112 px from top | Variable | Centered horizontally |
| Cursor ► | 8 px left of selected option | Aligned with option | 8×8 px | — |
| Solen Silhouette | 72 px from left | 64 px from top | 16×32 px | Center-low |
| Lantern Glow | 76 px from left | 60 px from top | 16×16 px | Above staff |

### Colors (Title Screen Palette)

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Deep Hollow Purple | `#180830` | Top sky, deepest shadow |
| Color 1 | Dusk Rose | `#684058` | Mid sky, silhouette shadow |
| Color 2 | Sunset Orange | `#D88848` | Horizon, Solen silhouette edge |
| Color 3 | Lantern Gold | `#F8D878` | Lantern glow, logo highlights, stars |

### PIXEL ART GENERATION PROMPT — Title Screen Background (160×144 px)

> Pixel art title screen for a Game Boy Color platformer. 160x144 pixels. A lone silhouetted figure (young woman with a staff topped by a glowing lantern) stands on a grassy hillside at right-center. The sky is a gradient: deep hollow purple #180830 at top transitioning through dusk rose #684058 to sunset orange #D88848 at the horizon. The lantern at the top of the staff glows bright lantern gold #F8D878 — the brightest point on screen. Along the distant horizon, five faint colored glows (Hearthstones) are barely visible. Foreground: silhouetted grass and wildflowers on the hill. Stars twinkle in the purple upper sky. Mood: melancholy, determined, beautiful. GBC style, 4-color palette: deep purple #180830, dusk rose #684058, sunset orange #D88848, lantern gold #F8D878. Clean pixel art, no anti-aliasing, indexed color.

### PIXEL ART GENERATION PROMPT — Game Logo/Title Treatment

> Pixel art game logo for a Game Boy Color platformer. Text "EMBER TIDE" in a custom pixel art logotype, approximately 120x24 pixels. Letters are bold, slightly angular, with a serif-influenced design. Each letter has a gradient effect: left side is warm lantern gold #F8D878, transitioning to deep purple #180830 on the right side, as if the letters are being consumed by shadow from the right. The 'E' in EMBER has a small flame flourish on its top stroke. Below the logo, small clean text "Rekindle the light" in white #F8D878 pixel font. Transparent background. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Start Screen Flow

### Boot Sequence

1. **GB Studio splash** (standard, 1 second)
2. **Fade to black** (0.5 seconds)
3. **Title screen fades in** (1 second)
4. **Title music begins** (looping)
5. **"Press START" text blinks** at the bottom of the screen for 3 seconds, then the menu options ("NEW GAME" / "CONTINUE") appear

### New Game Flow

1. Player selects "NEW GAME"
2. Screen fades to black (1 second)
3. Opening text crawl (see 12-dialogue-and-script.md for full text):
   - Black screen, white text
   - "In the world of Lumara, the Hearthstones keep the darkness at bay..."
   - Text scrolls slowly upward
   - 3 paragraphs of lore establishing the world, the Hollow Tide, and the Lamplighters
4. Fade to Scene 0-1: Cinderhearth Village — Evening Round
5. Gameplay begins

### Continue Flow

1. Player selects "CONTINUE"
2. Screen fades to black (0.5 seconds)
3. Fade in at the last checkpoint (saved scene, saved position)
4. Gameplay begins immediately — no text crawl

---

## Options Screen

### Access

The Options screen is accessed from the Pause Menu during gameplay (not from the title screen — the title screen is kept minimal with only NEW GAME and CONTINUE).

### Layout

```
┌──────────────────────────────────────┐
│  ══ OPTIONS ══                       │
│                                      │
│  MUSIC        [ON] / OFF             │
│  SFX          [ON] / OFF             │
│                                      │
│  CONTROLS                            │
│  ─────────                           │
│  A Button    : Attack / Confirm      │
│  B Button    : Jump / Cancel         │
│  START       : Pause                 │
│  SELECT      : Quick Map             │
│  D-Pad       : Move / Climb          │
│                                      │
│           [B] BACK                   │
└──────────────────────────────────────┘
```

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Window X | 8 px from left |
| Window Y | 4 px from top |
| Window Width | 144 px |
| Window Height | 136 px |

### Functionality

| Option | Behavior |
|---|---|
| MUSIC ON/OFF | Toggles background music. Left/Right to change. Saved to SRAM. |
| SFX ON/OFF | Toggles sound effects. Left/Right to change. Saved to SRAM. |
| Controls | Display only — not rebindable on Game Boy. Shows current button mapping. |

### Colors

Same as Pause Menu: dark blue-black background, silver border, gold title, white text, gold selected option.

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Options screen, 144x136 pixels. Dark blue-black #101028 background with silver #A8A8B8 border. Title "OPTIONS" centered at top in gold #D8A830. Two toggle rows: "MUSIC [ON] / OFF" and "SFX [ON] / OFF" with ON highlighted in gold. Below, a "CONTROLS" section listing button mappings in white #FFFFFF text: A=Attack, B=Jump, START=Pause, SELECT=Map, D-Pad=Move. "B BACK" at bottom. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Credits Screen

### Access

The credits screen plays automatically after the ending sequence (normal or true ending). It can also be accessed by pressing SELECT on the title screen after completing the game once (a small "♪" icon appears next to the title to indicate this is unlocked).

### Layout

The credits scroll vertically upward over the background. The background is different depending on which ending was achieved:

**Normal Ending Credits Background:** A slow parallax scroll of Lumara's landscape — the five world regions scrolling by from left to right as the credits scroll up, each region now lit and vibrant. The Hearthstones glow in the background.

**True Ending Credits Background:** A night sky full of stars (the stars that Lumara has never seen before). Constellations slowly form as the credits scroll — outlines of a lantern, a heart, a flame — connecting the stars.

### Credits Content

```
═══ EMBER TIDE ═══

A Game Boy Color Game
Built in GB Studio 4.2

──── DESIGN ────
[Developer Name]

──── PROGRAMMING ────
[Developer Name]

──── ART ────
[Developer Name]

──── MUSIC & SOUND ────
[Developer Name]

──── STORY ────
[Developer Name]

──── TOOLS ────
GB Studio 4.2
hUGETracker
Aseprite

──── SPECIAL THANKS ────
The GB Studio Community
[Additional Thanks]

──── ────

"Hearthstone or matchstick,
 the job's the same."

       — Maren

══════════════════
```

### Scroll Speed

The credits scroll at approximately 1 pixel per 4 frames (slow, readable). Total scroll time: approximately 90 seconds. After the credits complete, the screen holds on the final quote for 5 seconds, then fades to black and returns to the title screen. If the true ending was achieved, the post-credits scene (Edric's finished figurine on the mantelpiece) plays before returning to the title screen.

### Colors (Credits Palette)

**Normal Ending:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Sky Blue | `#283858` | Sky background |
| Color 1 | Landscape Green | `#488848` | Terrain, trees |
| Color 2 | Light | `#C8D8B8` | Clouds, highlights |
| Color 3 | Text White | `#F8F8F8` | All credit text |

**True Ending:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Night Sky | `#080818` | Deep sky |
| Color 1 | Star Dim | `#384868` | Dim stars, constellation lines |
| Color 2 | Star Bright | `#A0B8D8` | Bright stars |
| Color 3 | Text White | `#F8F8F8` | All credit text, constellation highlights |

### PIXEL ART GENERATION PROMPT — Credits Background (Normal Ending)

> Pixel art credits background for a Game Boy Color platformer. 160x144 pixels. Bright, peaceful panoramic landscape of a fantasy world after being saved. Rolling green hills with tiny trees, a blue sky with gentle clouds. Five faint colored glows (green, blue, teal, orange, white) on distant hilltops representing reignited crystals. Warm, hopeful, relieved mood. Designed to scroll horizontally as credits scroll vertically. GBC style, 4-color palette: sky blue #283858, landscape green #488848, light #C8D8B8, text white #F8F8F8. Clean pixel art, no anti-aliasing, indexed color.

### PIXEL ART GENERATION PROMPT — Credits Background (True Ending)

> Pixel art credits background for a Game Boy Color platformer. 160x144 pixels. Night sky full of stars on a deep dark background #080818. Stars in varying brightness — dim blue #384868 and bright white-blue #A0B8D8. Subtle constellation patterns: a lantern shape, a heart shape, a flame shape formed by connected bright stars. Beautiful, serene, awe-inspiring — this is a sky that has never been seen before. Designed for vertical scrolling credits overlay. GBC style, 4-color palette: night sky #080818, star dim #384868, star bright #A0B8D8, text white #F8F8F8. Clean pixel art, no anti-aliasing, indexed color.
