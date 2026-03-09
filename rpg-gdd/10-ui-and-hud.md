# 10 — UI and HUD

---

## UI Design Philosophy

All UI in Chronospire is rendered using GB Studio's overlay system and Display Dialogue events. The 160x144 pixel screen is the entire canvas. UI elements must be readable at Game Boy Color resolution, using high-contrast color choices and clear iconography. No element should obscure critical gameplay information for more than a moment.

---

## Overworld HUD

### Description

A minimal HUD displayed at the top of the screen during overworld exploration. Shows Edyn's current HP and MP as compact numerical displays. The HUD is toggled on/off by pressing Select (to reduce screen clutter when exploring).

### Layout

```
+--------------------------------------+
| HP:028/028  MP:012/012               |  <- Top 8px overlay bar
|                                      |
|                                      |
|        (gameplay area)               |
|                                      |
|                                      |
|                                      |
+--------------------------------------+
```

- **Position:** Top row, left-aligned. Occupies the top 8 pixels (1 tile row) of the 160x144 screen.
- **Content:** `HP:XXX/XXX  MP:XXX/XXX` in a compact monospace font.
- **Background:** Semi-transparent dark bar (darkest palette color with overlay).

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Text | `#F0F0F0` | White text |
| Background | `#1A1A2A` | Dark bar |
| HP Color | `#60C060` | Green HP number |
| MP Color | `#6080C0` | Blue MP number |

### Trigger in GB Studio

- On scene load: Display Overlay with text showing current HP/MP values.
- Update overlay whenever HP or MP changes (after combat, after item use, after level up).
- Select button toggles overlay visibility.

### Pixel Art Generation Prompt

> "160x8 pixel art HUD bar for a Game Boy Color RPG. Top-of-screen overlay showing HP and MP in compact format. Dark semi-transparent background bar, white text reading 'HP:028/028 MP:012/012', HP numbers in green, MP numbers in blue. GBC style monospace pixel font. Palette: #1A1A2A background, #F0F0F0 white text, #60C060 green, #6080C0 blue. Clean pixel art, no anti-aliasing."

---

## Dialogue Box

### Description

The standard dialogue box used for all NPC conversations, sign reading, item descriptions, and story narration. Appears at the bottom of the screen. Includes a 16x16 pixel character portrait on the left side and text on the right.

### Layout

```
+--------------------------------------+
|                                      |
|        (gameplay area)               |
|                                      |
|                                      |
+--------------------------------------+
| [PORT] Character Name                |  <- Dialogue box top line
| [RAIT] "Dialogue text goes here     |  <- Text lines (up to 3)
|        and can wrap to multiple      |
|        lines as needed."            |
+--------------------------------------+
```

- **Position:** Bottom of screen, occupying the bottom 40 pixels (5 tile rows).
- **Size:** 160 pixels wide × 40 pixels tall.
- **Portrait:** 16x16 pixels, positioned at left edge (x:4, y:104).
- **Text Area:** 136 pixels wide, starting after portrait + 8px gap.
- **Border:** 1-pixel border in medium color, filled with dark background.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Border | `#6080C0` | Steel blue border |
| Background | `#1A1A2A` | Dark indigo fill |
| Text | `#F0F0F0` | White text |
| Name | `#D0A030` | Gold character name |

### Trigger in GB Studio

- Triggered by interacting with an NPC (press A facing actor) or entering a scripted event.
- Uses GB Studio's "Display Dialogue" event with portrait image reference.
- Text advances on A press. Auto-close after final line.
- Portrait changes based on speaking character (set via event parameter).

### Pixel Art Generation Prompt

> "160x40 pixel art dialogue box for a Game Boy Color RPG. Bottom-of-screen text box with 1-pixel steel blue border, dark indigo fill. 16x16 pixel portrait area on the left side. Character name in gold text on first line. White dialogue text in GBC monospace pixel font, up to 3 lines. Palette: #1A1A2A background, #6080C0 border, #F0F0F0 white text, #D0A030 gold name. Clean pixel art, no anti-aliasing."

---

## Battle Screen HUD

### Description

The battle screen layout showing enemy information, party status, and the action menu. This is a full-screen UI displayed during combat scenes.

### Layout

```
+--------------------------------------+
|                                      |
|       [ENEMY SPRITE 16x32]          |  <- Top area: enemy display
|       Enemy Name                     |
|       HP: ██████████░░ 055/080       |
|                                      |
|--------------------------------------|
|  Edyn      HP:080/080  MP:032/032   |  <- Middle: party status
|  Lira      HP:060/060  MP:048/048   |
|--------------------------------------|
|  > Attack    Magic                   |  <- Bottom: action menu
|    Item      Flee                    |
+--------------------------------------+
```

- **Enemy Area:** Top 64 pixels. Enemy sprite centered, name below sprite, HP bar below name.
- **Party Status:** Middle 32 pixels. Two lines showing Edyn and active companion with HP/MP.
- **Action Menu:** Bottom 32 pixels. Four options in 2x2 grid layout. Cursor (>) indicates selection.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Background | `#1A1A2A` | Dark indigo |
| Text | `#F0F0F0` | White |
| HP Bar Full | `#60C060` | Green |
| HP Bar Empty | `#3A3A40` | Dark gray |
| MP Text | `#6080C0` | Blue |
| Menu Cursor | `#D0A030` | Gold |
| Divider | `#4A4A6A` | Medium indigo |

### Trigger in GB Studio

- Displayed on battle scene init. Built using overlay text and actor placement.
- Enemy sprite placed as actor at top-center of battle scene.
- Party stats rendered as overlay text, updated each round.
- Action menu rendered as overlay with cursor position tracked by `VAR_MENU_CURSOR` variable.
- Cursor moves with D-pad input (Up/Down/Left/Right mapped to 2x2 grid positions).
- A button confirms selection, B button cancels sub-menus.

### Pixel Art Generation Prompt

> "160x144 pixel art battle screen layout for a Game Boy Color RPG. Full-screen battle UI. Top area: enemy sprite placeholder (16x32) centered, enemy name text, HP bar (green filled / gray empty). Middle divider line. Party status: two lines with character names, HP and MP values in green and blue. Bottom: 2x2 action menu grid with Attack, Magic, Item, Flee options, gold cursor arrow. Dark indigo background. Palette: #1A1A2A, #F0F0F0, #60C060, #6080C0, #D0A030, #4A4A6A. Clean pixel art, GBC style."

---

## Main Menu / Pause Menu

### Description

Accessed by pressing Start during overworld gameplay. Shows party status, equipment, and options. Overlays the gameplay screen.

### Layout

```
+--------------------------------------+
|  CHRONOSPIRE                         |
|--------------------------------------|
|  Edyn     Lv:12  HP:094/116         |
|  Weapon: Prism Blade                 |
|  Armor:  Crystal Shield Vest         |
|--------------------------------------|
|  [Companion Name]  Lv:11            |
|  HP:080/085  MP:037/060             |
|--------------------------------------|
|  Gold: 1,240                         |
|  Time: 04:32                         |
|--------------------------------------|
|  > Items                             |
|    Equipment                         |
|    Party                             |
|    Save (at save points)             |
|    Close                             |
+--------------------------------------+
```

- **Position:** Full screen overlay (160x144).
- **Sections:** Header, Edyn stats, Companion stats, Gold/Time, Menu options.
- **Navigation:** D-pad Up/Down to select menu option. A to confirm. B or Start to close.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Background | `#1A1A2A` | Dark indigo |
| Text | `#F0F0F0` | White |
| Header | `#D0A030` | Gold |
| Stats | `#60C060` | Green (HP), `#6080C0` (MP) |
| Cursor | `#D0A030` | Gold arrow |
| Divider | `#4A4A6A` | Medium indigo |

### Trigger in GB Studio

- Start button press triggers a custom event that opens the menu overlay.
- Menu is built using Overlay Show/Hide and text rendering.
- Each menu option leads to a sub-screen (Items, Equipment, Party, Save).
- Save option is only functional when `VAR_AT_SAVE_POINT` == 1 (set by save point interaction scripts).

### Pixel Art Generation Prompt

> "160x144 pixel art pause menu screen for a Game Boy Color RPG. Full-screen overlay with game title at top in gold, party member stats showing level, HP, MP, equipped weapon and armor, gold amount, play time, and menu options (Items, Equipment, Party, Save, Close) with gold cursor arrow. Dark indigo background with medium indigo divider lines. Palette: #1A1A2A, #F0F0F0, #D0A030, #60C060, #6080C0, #4A4A6A. GBC monospace pixel font. Clean pixel art."

---

## Inventory Screen

### Description

Sub-screen accessed from the Main Menu > Items. Shows all consumable items with quantities and allows use outside of combat.

### Layout

```
+--------------------------------------+
|  ITEMS                               |
|--------------------------------------|
|  > Potion          x05               |
|    Hi-Potion       x02               |
|    Aether Crystal  x03               |
|    Antidote        x01               |
|    Smoke Bomb      x02               |
|    Herbal Salve    x01               |
|                                      |
|                                      |
|--------------------------------------|
|  Use on: Edyn / Lira / Rook         |
+--------------------------------------+
```

- **Position:** Full screen overlay.
- **Content:** Scrollable list of items with quantities. Only items with quantity > 0 shown.
- **Navigation:** D-pad Up/Down to select item. A to use (opens target selection for healing items). B to go back.

### Palette

Same as Main Menu palette.

### Trigger in GB Studio

- Entered from Main Menu Items option.
- Item list is generated by checking each item variable (`VAR_ITEM_POTION`, etc.) and only displaying items with count > 0.
- Using a healing item outside combat: Select target (Edyn, Lira, or Rook), apply healing, decrement item variable, update display.
- Key items are displayed in a separate section below consumables, marked with a star icon.

### Pixel Art Generation Prompt

> "160x144 pixel art inventory screen for a Game Boy Color RPG. Full-screen item list with 'ITEMS' header, scrollable list of consumable items with quantities (e.g., 'Potion x05'), gold cursor arrow for selection, target selection bar at bottom ('Use on: Edyn / Lira / Rook'). Dark indigo background, white text, gold header and cursor. GBC monospace pixel font. Palette: #1A1A2A, #F0F0F0, #D0A030, #4A4A6A. Clean pixel art."

---

## Equipment Screen

### Description

Sub-screen for viewing and changing equipment. Shows current equipment and available items for each slot.

### Layout

```
+--------------------------------------+
|  EQUIPMENT - Edyn                    |
|--------------------------------------|
|  Weapon:  [Prism Blade      +12 ATK]|
|  Armor:   [Crystal Shield   +10 DEF]|
|  Access.: [Tideborn Relic   Special] |
|--------------------------------------|
|  ATK: 42  DEF: 33  SPD: 43          |
|  HP: 116  MP: 44                     |
|--------------------------------------|
|  > Change Weapon                     |
|    Change Armor                      |
|    Change Accessory                  |
|    Next Character                    |
|    Back                              |
+--------------------------------------+
```

- **Position:** Full screen overlay.
- **Content:** Current character's equipment with stat bonuses. Total stats displayed. Options to change each slot or switch character.

### Palette

Same as Main Menu palette.

### Trigger in GB Studio

- Entered from Main Menu Equipment option.
- Changing equipment: Select slot → Display available items for that slot (from owned equipment variables) → Select new item → Recalculate stats → Update display.
- Stats update in real-time as equipment changes.
- "Next Character" cycles through Edyn → Lira → Rook.

### Pixel Art Generation Prompt

> "160x144 pixel art equipment screen for a Game Boy Color RPG. Full-screen showing character name, three equipment slots (Weapon, Armor, Accessory) with item names and stat bonuses, total stats display (ATK, DEF, SPD, HP, MP), and menu options (Change Weapon/Armor/Accessory, Next Character, Back). Dark indigo background, white text, gold headers and cursor. GBC pixel font. Palette: #1A1A2A, #F0F0F0, #D0A030, #4A4A6A. Clean pixel art."

---

## World Map Screen

### Description

A simplified visual map accessible from the Main Menu (unlocked after obtaining the Meridian Compass). Shows the world layout with icons for visited locations and the current position.

### Layout

```
+--------------------------------------+
|  AETHERMERE                          |
|                                      |
|          [Ashenveil]                 |
|          /        \                  |
|   [Storm]          [Ironpeak]        |
|      \              /                |
|    [Stillwater-Chronospire]          |
|      /              \                |
|   [Verdant]        [Crystal]         |
|     * (you are here)                 |
|                                      |
|  Meridians: 2/5 restored            |
+--------------------------------------+
```

- **Position:** Full screen overlay.
- **Content:** Stylized world map with region names. Current location marked with blinking cursor. Visited locations shown in full; unvisited shown as `???`. Meridian restoration counter at bottom.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Background | `#1A1A2A` | Dark indigo |
| Map Lines | `#4A4A6A` | Medium indigo |
| Visited | `#D0A030` | Gold |
| Unvisited | `#4A4A6A` | Gray |
| Current | `#F0F0F0` | Blinking white |
| Meridian Counter | `#60C060` | Green |

### Trigger in GB Studio

- Accessed from Main Menu or by pressing Select (if overworld HUD is toggled off, Select opens map instead).
- Region visit flags (`VAR_VISITED_VERDANT`, `VAR_VISITED_STORMHAVEN`, etc.) determine display state.
- Meridian counter reads from restoration flag variables.

### Pixel Art Generation Prompt

> "160x144 pixel art world map screen for a Game Boy Color RPG. Stylized top-down map of a crescent-shaped continent with labeled regions connected by paths. Current location marked with blinking dot. Visited locations in gold, unvisited in gray. 'Meridians: 2/5 restored' counter at bottom in green. Dark indigo background. Palette: #1A1A2A, #4A4A6A, #D0A030, #F0F0F0, #60C060. GBC pixel art style."

---

## Save Screen

### Description

Displayed when the player interacts with a save point and confirms they want to save.

### Layout

```
+--------------------------------------+
|  SAVE PROGRESS                       |
|--------------------------------------|
|  Edyn  Lv:12                         |
|  Location: Ironpeak Enclave          |
|  Time: 04:32                         |
|  Meridians: 3/5                      |
|--------------------------------------|
|                                      |
|    Saving...                         |
|                                      |
|    Progress saved!                   |
|                                      |
|  Press A to continue.                |
+--------------------------------------+
```

- **Position:** Full screen overlay.
- **Content:** Summary of save data (level, location, time, progress), saving animation, confirmation.

### Palette

Same as Main Menu palette.

### Trigger in GB Studio

- Triggered by interacting with a save point and selecting "Yes" on the save confirmation dialogue.
- Displays summary, executes GB Studio's Save Data event, displays confirmation.
- A button returns to gameplay.

### Pixel Art Generation Prompt

> "160x144 pixel art save screen for a Game Boy Color RPG. Full-screen overlay showing 'SAVE PROGRESS' header, save data summary (character level, location name, play time, meridian progress counter), 'Saving...' animation text, 'Progress saved!' confirmation, 'Press A to continue' prompt. Dark indigo background, gold header, white text. GBC pixel font. Palette: #1A1A2A, #D0A030, #F0F0F0, #4A4A6A. Clean pixel art."

---

## Shop Screen

### Description

Displayed when interacting with a shopkeeper and selecting Buy or Sell.

### Layout (Buy Mode)

```
+--------------------------------------+
|  WYNN'S WARES          Gold: 1,240   |
|--------------------------------------|
|  > Potion            15G             |
|    Hi-Potion         40G             |
|    Antidote          10G             |
|    Smoke Bomb        30G             |
|    Leather Vest      80G             |
|                                      |
|--------------------------------------|
|  Restores 20 HP to one ally.         |
|  Own: 3                              |
+--------------------------------------+
```

- **Position:** Full screen overlay.
- **Content:** Shop name, player gold, item list with prices, item description at bottom, current owned quantity.
- **Navigation:** D-pad to browse items, A to buy, B to exit.

### Palette

Same as Main Menu palette, with prices in gold color.

### Trigger in GB Studio

- Triggered by shop NPC interaction script.
- Buy: Check gold >= price, subtract gold, increment item variable, display "Purchased!"
- Sell: Display owned items, calculate sell price (50% buy), add gold, decrement item variable.
- Sable's Haggle: If `VAR_SABLE_IN_PARTY` == 1, displayed prices are reduced by 15%.

### Pixel Art Generation Prompt

> "160x144 pixel art shop screen for a Game Boy Color RPG. Full-screen buy interface with shop name header and gold counter, scrollable item list with prices, gold cursor, item description panel at bottom showing effect and owned quantity. Dark indigo background, white item names, gold prices and header. GBC pixel font. Palette: #1A1A2A, #F0F0F0, #D0A030, #4A4A6A. Clean pixel art."

---

## Game Over Screen

### Description

Displayed when the player is defeated in combat.

### Layout

```
+--------------------------------------+
|                                      |
|                                      |
|                                      |
|         GAME  OVER                   |
|                                      |
|    The pocket watch falls silent.    |
|                                      |
|                                      |
|      > Continue from last save       |
|        Return to title               |
|                                      |
|                                      |
+--------------------------------------+
```

- **Position:** Full screen, centered text.
- **Content:** "GAME OVER" in large text, flavor text, two options.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Background | `#0A0A10` | Near black |
| Title Text | `#802020` | Dark red |
| Flavor Text | `#808090` | Dim gray |
| Options | `#F0F0F0` | White |
| Cursor | `#D0A030` | Gold |

### Trigger in GB Studio

- Triggered by `CE_Battle_Lose` custom event when player HP reaches 0.
- Fade to black, then display overlay with Game Over text.
- Menu: Continue loads save data. Title returns to title screen scene.

### Pixel Art Generation Prompt

> "160x144 pixel art game over screen for a Game Boy Color RPG. Nearly black background. 'GAME OVER' in dark red large pixel text centered. Below: 'The pocket watch falls silent.' in dim gray. Two menu options in white: 'Continue from last save' and 'Return to title' with gold cursor. Somber and minimalist. Palette: #0A0A10, #802020, #808090, #F0F0F0, #D0A030. GBC pixel art."

---

## Level Up Notification

### Description

A brief overlay notification that appears after combat when the player levels up.

### Layout

```
+--------------------------------------+
|                                      |
|       LEVEL UP!                      |
|       Edyn is now Level 12!          |
|                                      |
|       HP +8  ATK +2  DEF +1         |
|       SPD +2  MP +3                  |
|                                      |
|       Learned: Chrono Strike!        |
|                                      |
+--------------------------------------+
```

- **Position:** Centered on screen, displayed over the battle victory results.
- **Content:** Level up announcement, stat increases, new ability (if applicable).

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Background | `#1A1A2A` | Dark indigo (with border) |
| Title | `#D0A030` | Gold |
| Stats | `#60C060` | Green (positive increases) |
| Ability | `#6080C0` | Blue |
| Text | `#F0F0F0` | White |

### Trigger in GB Studio

- Triggered by `CE_Check_Level_Up` custom event at end of combat when XP threshold is met.
- Displayed as a sequence of Display Dialogue events showing the level up information.
- Auto-advances after A press.

### Pixel Art Generation Prompt

> "160x80 pixel art level up notification popup for a Game Boy Color RPG. Centered overlay box with gold border. 'LEVEL UP!' in gold text, character name and new level in white, stat increases in green (HP +8, ATK +2, etc.), new ability learned in blue. Dark indigo background. GBC pixel font. Palette: #1A1A2A, #D0A030, #60C060, #6080C0, #F0F0F0. Clean pixel art."

---

*Chronospire: The Shattered Meridian — UI and HUD Document*
