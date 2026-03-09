# 09 — UI & HUD

---

## UI Element Overview

| Element | Type | When Visible |
|---|---|---|
| Health Bar (Hearts) | HUD | Always during gameplay |
| Flame Coin Counter | HUD | Always during gameplay |
| Tincture Counter | HUD | Always during gameplay |
| Scene Name | HUD | 3 seconds on scene entry |
| Dialogue Box | Overlay | During NPC/sign interactions |
| Pause Menu | Overlay | When START is pressed |
| Inventory Screen | Sub-menu | Accessed from Pause Menu |
| World Map | Sub-menu | Accessed from Pause Menu |
| Title Screen | Full screen | Game start |
| Game Over / Death | Overlay | On player death |

---

## Health Bar (Hearts)

### Visual Description

A row of heart icons displayed at the top-left of the screen. Each heart represents 1 HP. Filled hearts are bright red with a darker red outline. Empty hearts (lost HP) are gray outlines only. When the player takes damage, the lost heart flashes white for 0.25 seconds before turning to an empty outline. When the player heals, the gained heart fills from left to right with a quick red pulse animation.

The hearts are compact — each heart is 8×8 pixels with 1px spacing between them, for a total of up to 72 pixels wide (8 hearts × 9px including spacing). At maximum HP (8 hearts), the bar extends about 45% across the screen width.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| X Position | 2 px from left edge |
| Y Position | 2 px from top edge |
| Heart Size | 8×8 px each |
| Spacing | 1 px between hearts |
| Total Width (5 hearts) | 44 px |
| Total Width (8 hearts) | 71 px |
| Total Height | 8 px |

### Colors

| Element | Color | Hex |
|---|---|---|
| Filled Heart | Bright Red | `#FF2020` |
| Heart Outline | Dark Red | `#8B0000` |
| Empty Heart | Dark Gray Outline | `#505050` |
| Flash (damage) | White | `#FFFFFF` |
| Flash (heal) | Pink | `#FF8080` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer HUD. 8x8 pixel heart icon in multiple states: filled heart (bright red #FF2020 fill with dark red #8B0000 outline), empty heart (dark gray #505050 outline only, no fill), damage flash heart (white #FFFFFF), heal flash heart (pink #FF8080). Simple, clean heart shape — rounded top bumps, pointed bottom. Arrange all 4 states in a single row (32x8 pixel strip). GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Flame Coin Counter

### Visual Description

A small flame icon (8×8 px) followed by a multiplication sign and a 3-digit number in a clean small font. The flame icon is animated — a 2-frame flicker between two slightly different flame shapes. The number updates instantly when coins are collected, with no roll animation (keeping it simple for GB hardware). The text is white on transparent background.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| X Position | 88 px from left edge |
| Y Position | 2 px from top edge |
| Icon Size | 8×8 px |
| Text Area | ~24 px wide (×000) |
| Total Width | ~34 px |
| Total Height | 8 px |

### Colors

| Element | Color | Hex |
|---|---|---|
| Flame Icon (inner) | Bright Orange | `#F08828` |
| Flame Icon (outer) | Dark Orange | `#A04010` |
| Counter Text | White | `#FFFFFF` |
| Multiplication Sign | Light Gray | `#C0C0C0` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer HUD. 8x8 pixel flame coin icon — small stylized flame shape, bright orange #F08828 inner with dark orange #A04010 outer edge. Two frames for flicker animation side by side (16x8 total). Also include sample counter text "×023" in a clean 4px-wide pixel font, white #FFFFFF on transparent background. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Tincture Counter

### Visual Description

A small bottle icon (8×8 px) showing a round-bottomed potion vial with a cork stopper. The liquid inside is green (healing tincture). Followed by a multiplication sign and a 1-digit number. Same text style as the Flame Coin counter.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| X Position | 130 px from left edge |
| Y Position | 2 px from top edge |
| Icon Size | 8×8 px |
| Text Area | ~12 px wide (×3) |
| Total Width | ~22 px |
| Total Height | 8 px |

### Colors

| Element | Color | Hex |
|---|---|---|
| Bottle Glass | Light Blue | `#A0C8E0` |
| Liquid | Healing Green | `#40C848` |
| Cork | Brown | `#886840` |
| Counter Text | White | `#FFFFFF` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer HUD. 8x8 pixel healing potion bottle icon — small round-bottomed vial with brown #886840 cork stopper, light blue #A0C8E0 glass, green #40C848 liquid inside filling the bottom two-thirds. Include sample counter text "×3" in clean pixel font, white #FFFFFF. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Scene Name Display

### Visual Description

A brief text label that appears when the player enters a new scene. The text shows the scene's name (e.g., "Verdant Hollow — Ashen Canopy") in a clean pixel font. It appears below the HUD bar, fades in over 0.5 seconds, remains visible for 2 seconds, then fades out over 0.5 seconds. The text has a dark shadow offset to ensure readability against any background.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| X Position | Centered horizontally |
| Y Position | 12 px from top edge (below HUD) |
| Text Height | 8 px |
| Max Width | 152 px (leaving 4px margin on each side) |

### Colors

| Element | Color | Hex |
|---|---|---|
| Scene Name Text | White | `#FFFFFF` |
| Text Shadow | Dark (1px offset down-right) | `#202020` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI text element for a Game Boy Color platformer. Scene name label "Verdant Hollow" in a clean 5px-wide pixel font, white #FFFFFF with dark #202020 shadow offset 1 pixel down and right. Text centered on a transparent background, 160px wide, 8px tall. GBC style, clean pixel art, no anti-aliasing.

---

## Dialogue Box

### Visual Description

The dialogue box occupies the bottom portion of the screen when active. It consists of two parts: a 16×16 character portrait on the left side and a text area filling the remaining space. The box has a dark background with a lighter border. Text appears character by character (typewriter effect) at a rate of ~3 characters per frame. The player presses A to advance to the next line or dismiss the box. A small downward-pointing triangle blinks at the bottom-right of the text area when the text is complete, indicating the player can press A.

The portrait changes based on who is speaking. When a non-character entity is "speaking" (environmental text, narration), no portrait is shown and the text area expands to full width.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Box X | 0 px (full width) |
| Box Y | 96 px from top (bottom 48 px of screen) |
| Box Width | 160 px |
| Box Height | 48 px |
| Portrait X | 4 px from left |
| Portrait Y | 100 px from top (4px inside box) |
| Portrait Size | 16×16 px |
| Text Area X | 24 px from left (after portrait + spacing) |
| Text Area Y | 100 px from top |
| Text Area Width | 132 px |
| Text Area Height | 40 px |
| Max Characters Per Line | ~18 characters |
| Max Lines Visible | 3 |

### Colors

| Element | Color | Hex |
|---|---|---|
| Box Background | Near Black | `#101018` |
| Box Border | Light Gray | `#A0A0A8` |
| Text | White | `#FFFFFF` |
| Advance Triangle | White (blinking) | `#FFFFFF` |
| Portrait Border | Gold | `#D8A830` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Dialogue box occupying the bottom 48 pixels of a 160x144 screen. Dark near-black #101018 background with light gray #A0A0A8 border (1px). On the left side, a 16x16 portrait frame with gold #D8A830 border containing a sample character portrait. To the right of the portrait, white #FFFFFF text in clean pixel font reading "The lantern still\nburns. That means\nthere's still time." with a small blinking down-triangle at bottom-right. GBC style, clean pixel art, no anti-aliasing, indexed color. Show the full 160x48 dialogue box.

---

## Pause Menu

### Visual Description

A centered window overlaid on the dimmed gameplay screen. The window has a dark background with a light border, matching the dialogue box style. The title "PAUSED" is centered at the top in a slightly larger font. Menu options are listed vertically with a cursor arrow (►) indicating the current selection. The cursor moves up and down with D-pad input. Pressing A selects the highlighted option. Pressing START or B closes the menu and resumes gameplay.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Window X | 32 px from left (centered: 96px wide) |
| Window Y | 20 px from top |
| Window Width | 96 px |
| Window Height | 104 px |
| Title Y | 26 px from top |
| First Option Y | 44 px from top |
| Option Spacing | 14 px between options |
| Cursor X | 36 px from left |
| Text X | 46 px from left |

### Menu Options

| # | Option | Action |
|---|---|---|
| 1 | RESUME | Close menu |
| 2 | INVENTORY | Open inventory sub-screen |
| 3 | MAP | Open world map sub-screen |
| 4 | OPTIONS | Open options sub-screen |
| 5 | QUIT | Return to title screen |

### Colors

| Element | Color | Hex |
|---|---|---|
| Window Background | Dark Blue-Black | `#101028` |
| Window Border | Silver | `#A8A8B8` |
| Title Text | Gold | `#D8A830` |
| Option Text (normal) | White | `#FFFFFF` |
| Option Text (selected) | Gold | `#D8A830` |
| Cursor Arrow | Gold | `#D8A830` |
| Gameplay Dim Overlay | Black 50% | `#000000` at 50% opacity (or dithered) |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Pause menu window, 96x104 pixels centered on a dimmed background. Dark blue-black #101028 background with silver #A8A8B8 border (1px). Title "PAUSED" centered at top in gold #D8A830 pixel font. Five menu options listed vertically in white #FFFFFF: RESUME, INVENTORY, MAP, OPTIONS, QUIT. Gold cursor arrow ► next to the first option (RESUME) which is highlighted in gold. Clean, minimal, retro. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Inventory Screen

### Visual Description

Accessed from the Pause Menu. Replaces the pause menu window with a larger display showing collectible progress. The layout is a vertical list of collectible categories with icons and counts.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Window X | 16 px from left |
| Window Y | 8 px from top |
| Window Width | 128 px |
| Window Height | 128 px |

### Layout

```
┌──────────────────────────────────────┐
│  ══ INVENTORY ══                     │
│                                      │
│  🔶 Ember Shards    12 / 25         │
│  📘 Lore Stones      3 / 5          │
│  💗 Heart Crystals   7 / 12         │
│  🔥 Flame Coins       147           │
│  🧪 Tinctures        2 / 3          │
│                                      │
│  ── STORY ITEMS ──                   │
│  🏷 Aldric's Badge                   │
│  🪵 Edric's Figurine                │
│                                      │
│           [B] BACK                   │
└──────────────────────────────────────┘
```

### Colors

Same as Pause Menu window. Icons use the same colors as their HUD counterparts.

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Inventory screen, 128x128 pixels. Dark blue-black #101028 background with silver #A8A8B8 border. Title "INVENTORY" centered at top in gold #D8A830. Vertical list of collectible items each with a small 8x8 icon and count: orange crystal "Ember Shards 12/25", blue stone "Lore Stones 3/5", pink heart "Heart Crystals 7/12", flame icon "Flame Coins 147", green bottle "Tinctures 2/3". Separator line. Section "STORY ITEMS" with badge and figurine icons. "B BACK" at bottom. White #FFFFFF text. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## World Map

### Visual Description

Accessed from the Pause Menu. Shows a top-down stylized map of Lumara. The map is primarily a dark background with the five world regions drawn as simplified terrain icons connected by dotted path lines. Each world node is a circle or shape representing the world's theme. Lit Hearthstones glow with their world color; unlit ones are gray. The player's current position is indicated by a blinking Solen icon. Cinderhearth is at the bottom center.

### Position on 160×144 Screen

The map fills the entire 160×144 screen.

### Layout (Approximate Node Positions)

```
                [SPIRE]          ← Top center (floating, Y:16)
                  |
              ....│....
             /         \
        [FROST]     [BRINE]      ← Upper (Y:48)
            \         /
         [VERDANT]               ← Middle-left (Y:80)
              \
            [FORGE]              ← Lower-right (Y:96)
              |
          [CINDER]               ← Bottom center (Y:120)
```

### Colors

| Element | Color | Hex |
|---|---|---|
| Map Background | Dark Blue-Black | `#081020` |
| Path Lines (uncleared) | Dark Gray Dots | `#404040` |
| Path Lines (cleared) | White Dots | `#C0C0C0` |
| Verdant Node (lit) | Green | `#78E048` |
| Frost Node (lit) | Ice Blue | `#78D8F0` |
| Brine Node (lit) | Teal | `#48C8B0` |
| Forge Node (lit) | Orange | `#F08828` |
| Spire Node (lit) | White | `#E0E0F0` |
| Unlit Node | Gray | `#505050` |
| Cinderhearth | Amber | `#F8D878` |
| Player Icon | Blinking Gold | `#F5C842` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color world map screen. 160x144 pixels. Dark blue-black #081020 background. Stylized top-down map of a fantasy world. Bottom center: warm amber village icon (Cinderhearth). Connected by dotted white lines to five world nodes arranged upward: green circle labeled "Verdant" at middle-left, ice blue circle "Frost" at upper-left, teal circle "Brine" at upper-right, orange circle "Forge" at lower-right, white circle "Spire" floating at top center. Lit nodes glow with their color; one gray unlit node for contrast. A small blinking gold arrow marks player position. Simplified terrain between nodes — tiny trees near Verdant, mountain shapes near Frost, water waves near Brine, flame wisps near Forge. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Game Over / Death Overlay

### Visual Description

There is no traditional "GAME OVER" screen. Instead, when the player dies:

1. Solen's death animation plays (lantern dims, she collapses)
2. Screen fades to black (1 second linear fade)
3. Text appears centered: "The lantern flickers..." in a gentle serif-style pixel font, white on black
4. Holds for 1.5 seconds
5. Screen fades back in at the last checkpoint with Solen's respawn animation

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Text X | Centered horizontally |
| Text Y | 68 px from top (vertically centered) |
| Fade Duration | 1 second in, 1.5 second hold, 1 second out |

### Colors

| Element | Color | Hex |
|---|---|---|
| Fade Background | Black | `#000000` |
| Death Text | Soft White | `#D8D8D8` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Death/respawn screen. 160x144 pixels of pure black #000000 background. Centered text in soft white #D8D8D8 pixel font reading "The lantern flickers..." in a slightly ornate but readable pixel typeface. Simple, somber, minimal. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Checkpoint Lamppost Indicator

### Visual Description

When the player touches a checkpoint lamppost, a brief visual indicator appears above the lamppost: a small lantern icon with a glow effect and the text "SAVED" that fades after 1.5 seconds. The lamppost itself transitions from unlit (dark, no flame) to lit (flame animation, warm glow halo on surrounding tiles).

### Position on 160×144 Screen

The indicator appears above the lamppost actor's position, approximately 16 px above the lamppost sprite.

### Colors

| Element | Color | Hex |
|---|---|---|
| Save Text | Gold | `#F8D878` |
| Lantern Glow | Amber | `#F5C842` |
| Unlit Lamppost | Dark Gray | `#404040` |
| Lit Lamppost | Warm Brown + Amber Flame | `#886840` / `#F5C842` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Checkpoint lamppost in two states side by side. UNLIT: 16x16 dark gray #404040 lamppost — tall thin post with a boxy lantern housing at top, no flame, no glow. LIT: same 16x16 lamppost but with an amber #F5C842 flame inside the housing and a warm glow halo around it. Above the lit version, small text "SAVED" in gold #F8D878 pixel font. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Interaction Prompt Arrow

### Visual Description

When the player is near an interactive object (NPC, sign, mechanism), a small downward-pointing arrow appears above the object, bouncing gently up and down (2-frame animation: offset 0px, offset 2px). The arrow indicates that pressing A will trigger an interaction.

### Position on 160×144 Screen

Appears 4 px above the interactive actor's top edge. Centered horizontally above the actor.

### Colors

| Element | Color | Hex |
|---|---|---|
| Arrow | White | `#FFFFFF` |
| Arrow Shadow | Dark | `#202020` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Interaction prompt arrow. 8x8 pixel small downward-pointing triangle/arrow in white #FFFFFF with a 1px dark #202020 shadow. Two animation frames: frame 1 at base position, frame 2 offset 2 pixels upward (bouncing). Simple, clean, universally readable. GBC style, clean pixel art, no anti-aliasing, indexed color.

---

## Ember Shard Collection Splash

### Visual Description

When the player collects an Ember Shard, a brief splash animation plays: the shard icon enlarges to the center of the screen (32×32 px), a circular burst of light radiates outward, and the text "EMBER SHARD" and the current count "X / 25" appear below the icon. The splash holds for 1.5 seconds, then fades. Gameplay pauses during this splash.

### Position on 160×144 Screen

| Property | Value |
|---|---|
| Shard Icon | Centered: 64px from left, 48px from top (32×32 enlarged icon) |
| Text "EMBER SHARD" | Centered, 88px from top |
| Counter "X / 25" | Centered, 100px from top |

### Colors

| Element | Color | Hex |
|---|---|---|
| Shard Icon | Orange Crystal | `#F08828` with `#F8D878` glow |
| Light Burst | White → Transparent | `#FFFFFF` radiating outward |
| Title Text | Gold | `#F8D878` |
| Counter Text | White | `#FFFFFF` |

### PIXEL ART GENERATION PROMPT

> Pixel art UI element for a Game Boy Color platformer. Ember Shard collection splash. 160x144 pixels. Center: a 32x32 enlarged orange crystal #F08828 with golden #F8D878 glow radiating outward in a circular burst pattern. Below the crystal: text "EMBER SHARD" in gold #F8D878 pixel font, and below that "15 / 25" in white #FFFFFF. Background is gameplay dimmed to ~50% with the splash overlaid. Celebratory, rewarding. GBC style, clean pixel art, no anti-aliasing, indexed color.
