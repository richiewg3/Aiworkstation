# 05 — Combat System

---

## Combat Style: Turn-Based

### Choice and Justification

Chronospire uses a **turn-based combat system** implemented entirely through GB Studio scripts, variables, and scene switches. This choice is made for three reasons:

1. **GB Studio Compatibility:** GB Studio 4.2 has no built-in battle engine. Turn-based combat maps cleanly to GB Studio's event scripting model: each turn is a sequence of conditional checks, variable math, and Display Dialogue events. Real-time combat would require frame-precise scripting that is unreliable within GB Studio's event system.

2. **Thematic Fit:** A game about time and patience benefits from a combat system that asks the player to think before acting. Each turn is a "moment" — fitting the game's meditation on how time is spent.

3. **Design Depth:** Turn-based combat allows for meaningful player choice (attack, magic, item, flee), enemy AI variety, status effects, and boss phase transitions — all achievable with variables and conditionals.

### Party System

The player controls Edyn plus up to 1 active companion (Lira or Rook). Sable is non-combat and does not appear in battle scenes. The active companion is selected via the party menu outside of combat. Companion actions are player-controlled, not AI-driven.

---

## How Encounters Trigger

### Overworld Encounters

Enemies are visible on the overworld as actor sprites. There are no random encounters. Combat triggers in one of three ways:

1. **Touch Trigger:** Player walks into an enemy actor's collision zone. The enemy actor has an "On Touch" script that initiates combat.
2. **Interact Trigger:** Player presses A facing an enemy (used for stationary enemies like Rot Vine ambushes).
3. **Scripted Event:** Story-triggered fights (bosses, Keeper Corwin) begin via cutscene scripts that transition to the battle scene automatically.

### Transition to Battle

When combat triggers:
1. Screen fades to black (using Fade Out event)
2. Store current scene ID and player position in variables (`VAR_RETURN_SCENE`, `VAR_RETURN_X`, `VAR_RETURN_Y`)
3. Set enemy ID variable (`VAR_ENEMY_ID`) to identify which enemy was touched
4. Switch to the battle scene (`battle_arena`)
5. Battle scene "On Init" script reads `VAR_ENEMY_ID` and loads appropriate enemy stats

---

## Battle Scene Layout

The battle scene (`battle_arena`) is a single reusable scene (20x18 tiles, 160x144 px) used for all standard combat. The layout:

```
+------------------------------------------+
|  [Enemy Sprite Area]                      |  Top 48px: Enemy sprite centered
|  Enemy Name         HP: XX/XX             |
|------------------------------------------|
|                                          |  Middle: Status area
|  Edyn      HP: XX/XX  MP: XX/XX         |
|  [Companion] HP: XX/XX  MP: XX/XX       |
|------------------------------------------|
|  > Attack    Magic                       |  Bottom 32px: Action menu
|    Item      Flee                        |  (overlay text)
+------------------------------------------+
```

The scene background is a generic battle backdrop that changes palette based on the region (set via `VAR_CURRENT_REGION`). The enemy sprite is placed as an actor in the top-center. Player and companion stats are rendered using overlay text.

---

## Full Variable List for Combat

| Variable Name | Type | Purpose |
|---------------|------|---------|
| `VAR_ENEMY_ID` | Integer | Identifies which enemy type is being fought (1–20) |
| `VAR_ENEMY_HP` | Integer | Current enemy HP |
| `VAR_ENEMY_MAX_HP` | Integer | Enemy's maximum HP |
| `VAR_ENEMY_ATK` | Integer | Enemy's attack stat |
| `VAR_ENEMY_DEF` | Integer | Enemy's defense stat |
| `VAR_ENEMY_SPD` | Integer | Enemy's speed stat |
| `VAR_ENEMY_XP` | Integer | XP reward on defeat |
| `VAR_ENEMY_GOLD` | Integer | Gold reward on defeat |
| `VAR_ENEMY_PHASE` | Integer | Boss phase tracker (1, 2, or 3) |
| `VAR_PLAYER_HP` | Integer | Edyn's current HP |
| `VAR_PLAYER_MAX_HP` | Integer | Edyn's max HP |
| `VAR_PLAYER_ATK` | Integer | Edyn's attack stat |
| `VAR_PLAYER_DEF` | Integer | Edyn's defense stat |
| `VAR_PLAYER_SPD` | Integer | Edyn's speed stat |
| `VAR_PLAYER_MP` | Integer | Edyn's current MP |
| `VAR_PLAYER_MAX_MP` | Integer | Edyn's max MP |
| `VAR_COMP_ACTIVE` | Integer | Which companion is active (0=none, 1=Lira, 2=Rook) |
| `VAR_COMP_HP` | Integer | Active companion's current HP |
| `VAR_COMP_MAX_HP` | Integer | Companion's max HP |
| `VAR_COMP_ATK` | Integer | Companion's attack stat |
| `VAR_COMP_DEF` | Integer | Companion's defense stat |
| `VAR_COMP_SPD` | Integer | Companion's speed stat |
| `VAR_COMP_MP` | Integer | Companion's current MP |
| `VAR_COMP_MAX_MP` | Integer | Companion's max MP |
| `VAR_TURN_ORDER` | Integer | Who goes first this round (0=player first, 1=enemy first) |
| `VAR_PLAYER_ACTION` | Integer | Player's chosen action (1=Attack, 2=Magic, 3=Item, 4=Flee) |
| `VAR_COMP_ACTION` | Integer | Companion's chosen action |
| `VAR_MAGIC_SELECT` | Integer | Which spell is selected (1–8) |
| `VAR_ITEM_SELECT` | Integer | Which item is selected from inventory |
| `VAR_DAMAGE_CALC` | Integer | Temporary variable for damage calculation |
| `VAR_TEMP_1` | Integer | General-purpose temp variable |
| `VAR_TEMP_2` | Integer | General-purpose temp variable |
| `VAR_BATTLE_STATE` | Integer | Battle flow state (0=menu, 1=player turn, 2=companion turn, 3=enemy turn, 4=win, 5=lose) |
| `VAR_STATUS_PLAYER` | Integer | Player status effect (0=none, 1=poison, 2=slow, 3=guard) |
| `VAR_STATUS_COMP` | Integer | Companion status effect |
| `VAR_STATUS_ENEMY` | Integer | Enemy status effect (0=none, 1=poison, 2=stun) |
| `VAR_FLEE_SUCCESS` | Integer | Whether flee attempt succeeds (0=fail, 1=success) |
| `VAR_RETURN_SCENE` | Integer | Scene ID to return to after battle |
| `VAR_RETURN_X` | Integer | Player X position to return to |
| `VAR_RETURN_Y` | Integer | Player Y position to return to |
| `VAR_CURRENT_REGION` | Integer | Current region (affects battle backdrop palette) |
| `VAR_BOSS_FLAG` | Integer | Is this a boss fight? (0=no, 1=yes — disables Flee) |
| `VAR_GUARD_ACTIVE` | Integer | Is the Guard ability active? (0=no, 1=yes — halves damage) |
| `VAR_ENEMY_DEFEATED` | Integer | Tracks which overworld enemy actor was defeated (for removal) |

---

## Step-by-Step Script Logic for a Full Combat Round

### Phase 0: Battle Initialization (On Scene Init)

1. **Load enemy stats:** Using `VAR_ENEMY_ID`, run a series of `If Variable == Value` checks. For each enemy ID, set `VAR_ENEMY_HP`, `VAR_ENEMY_ATK`, `VAR_ENEMY_DEF`, `VAR_ENEMY_SPD`, `VAR_ENEMY_XP`, `VAR_ENEMY_GOLD`, and `VAR_ENEMY_MAX_HP` to that enemy's values. Set the enemy actor's sprite sheet based on the ID.
2. **Load player stats:** Copy the persistent player stat variables into the battle variables (they should already be current from the overworld).
3. **Load companion stats:** If `VAR_COMP_ACTIVE` > 0, load the appropriate companion's stats. If 0, skip companion turns entirely.
4. **Set battle backdrop palette:** Use `VAR_CURRENT_REGION` to set the background palette (green for Verdant, blue for Stormhaven, purple for Ashenveil, white for Crystalfall, gray for Ironpeak, indigo for Chronospire).
5. **Display initial text:** Show enemy name and "A [Enemy Name] appears!" using Display Dialogue.
6. **Set `VAR_BATTLE_STATE` to 0** (menu phase).
7. **Proceed to Turn Order calculation.**

### Phase 1: Determine Turn Order

1. **Compare speeds:** If `VAR_PLAYER_SPD` >= `VAR_ENEMY_SPD`, set `VAR_TURN_ORDER` to 0 (player first). Else set to 1 (enemy first).
2. **If slow status on player:** Override `VAR_TURN_ORDER` to 1.
3. **If stun status on enemy:** Override `VAR_TURN_ORDER` to 0 and skip enemy turn this round.

### Phase 2: Player Action Selection

1. **Display action menu using overlay text:**
   - Line 1: `> Attack    Magic`
   - Line 2: `  Item      Flee`
2. **Wait for player input using a menu script:**
   - Use Display Menu event or a scripted input loop (if GB Studio 4.2 supports Display Menu with 4 choices, use that; otherwise use a variable-driven cursor with directional input checks).
   - On A press, set `VAR_PLAYER_ACTION` to the selected option (1/2/3/4).
3. **If Attack selected (1):** Proceed to Player Attack execution.
4. **If Magic selected (2):** Open magic sub-menu. Display available spells based on Edyn's current abilities (checked via unlock flag variables). Player selects a spell, setting `VAR_MAGIC_SELECT`. Check if `VAR_PLAYER_MP` >= spell cost. If not, display "Not enough MP!" and return to menu. If yes, proceed to Magic execution.
5. **If Item selected (3):** Open item sub-menu. Display usable items from inventory variables. Player selects an item, setting `VAR_ITEM_SELECT`. Proceed to Item execution.
6. **If Flee selected (4):** Check `VAR_BOSS_FLAG`. If 1, display "Can't flee from this fight!" and return to menu. If 0, calculate flee success: generate a pseudo-random value (use a frame counter or cycling variable), compare to a threshold based on `VAR_PLAYER_SPD` vs `VAR_ENEMY_SPD`. If success, set `VAR_FLEE_SUCCESS` to 1. If fail, display "Couldn't get away!" and lose the player's turn.

### Phase 3: Player Attack Execution

1. **Calculate damage:**
   - `VAR_DAMAGE_CALC` = `VAR_PLAYER_ATK` - (`VAR_ENEMY_DEF` / 2)
   - Use GB Studio Math events: Set `VAR_TEMP_1` = `VAR_ENEMY_DEF`. Divide `VAR_TEMP_1` by 2. Set `VAR_DAMAGE_CALC` = `VAR_PLAYER_ATK`. Subtract `VAR_TEMP_1` from `VAR_DAMAGE_CALC`.
   - If `VAR_DAMAGE_CALC` < 1, set `VAR_DAMAGE_CALC` to 1 (minimum 1 damage).
2. **Apply damage:** Subtract `VAR_DAMAGE_CALC` from `VAR_ENEMY_HP`.
3. **Display result:** "Edyn attacks! [Enemy] takes [X] damage!"
4. **Play attack animation:** Move enemy actor sprite briefly (flash/shake effect using Actor Move events).
5. **Check if enemy defeated:** If `VAR_ENEMY_HP` <= 0, jump to Win Condition.

### Phase 4: Magic Execution

Each spell is handled by a conditional block based on `VAR_MAGIC_SELECT`:

**Spell 1 — Aether Bolt (Edyn)**
- Cost: 4 MP
- Subtract 4 from `VAR_PLAYER_MP`
- Damage: `VAR_PLAYER_ATK` + 4 - (`VAR_ENEMY_DEF` / 2)
- Display: "Edyn casts Aether Bolt! [X] damage!"

**Spell 2 — Temporal Slow (Edyn)**
- Cost: 6 MP
- Set `VAR_STATUS_ENEMY` to 2 (slow — reduces enemy SPD for this battle)
- Reduce `VAR_ENEMY_SPD` by 5
- Display: "Edyn casts Temporal Slow! [Enemy]'s speed falls!"

**Spell 3 — Chrono Strike (Edyn, unlocked Act 2)**
- Cost: 8 MP
- Damage: (`VAR_PLAYER_ATK` * 2) - `VAR_ENEMY_DEF`
- Display: "Edyn channels the pocket watch! Chrono Strike deals [X] damage!"

**Spell 4 — Mending Light (Lira)**
- Cost: 5 MP
- Heals `VAR_PLAYER_HP` by 20 (or to max, whichever is less)
- Display: "Lira casts Mending Light! Edyn recovers [X] HP!"

**Spell 5 — Purify (Lira)**
- Cost: 3 MP
- Clears `VAR_STATUS_PLAYER` and `VAR_STATUS_COMP` to 0
- Display: "Lira casts Purify! Status effects cleared!"

**Spell 6 — Aether Bloom (Lira, unlocked Act 2)**
- Cost: 10 MP
- Heals both Edyn and companion for 30 HP
- Display: "Lira casts Aether Bloom! The party is healed!"

**Spell 7 — Iron Guard (Rook)**
- Cost: 4 MP
- Sets `VAR_GUARD_ACTIVE` to 1 (halves damage to Rook this round)
- Display: "Rook braces! Iron Guard active!"

**Spell 8 — Shatter Blow (Rook, unlocked Act 2)**
- Cost: 8 MP
- Damage: (`VAR_COMP_ATK` * 2) - (`VAR_ENEMY_DEF` / 4) — pierces defense
- Display: "Rook unleashes Shatter Blow! [X] damage!"

### Phase 5: Item Execution

Based on `VAR_ITEM_SELECT`:

1. **Potion (Item 1):** Restore 20 HP to selected target. Decrement `VAR_ITEM_POTION` by 1. Display: "Used Potion! [Target] recovers 20 HP!"
2. **Hi-Potion (Item 2):** Restore 50 HP. Decrement `VAR_ITEM_HI_POTION`. Display accordingly.
3. **Aether Crystal (Item 3):** Restore 15 MP to selected target. Decrement `VAR_ITEM_AETHER_CRYSTAL`.
4. **Antidote (Item 4):** Clear poison status. Decrement `VAR_ITEM_ANTIDOTE`.
5. **Smoke Bomb (Item 5):** Guaranteed flee from non-boss battles. Decrement `VAR_ITEM_SMOKE_BOMB`. Set `VAR_FLEE_SUCCESS` to 1.

### Phase 6: Companion Turn

If `VAR_COMP_ACTIVE` > 0 and companion HP > 0:
1. Display companion action menu (same structure as player: Attack, Magic, Item, Defend).
2. Companion attack uses `VAR_COMP_ATK` for damage calculation.
3. Companion magic uses companion-specific spells (see Phase 4 above).
4. Companion Defend: Sets `VAR_GUARD_ACTIVE` to 1, reducing damage taken by companion by 50% this round.

### Phase 7: Enemy Turn

1. **Enemy AI Decision:**
   - Standard enemies use a simple weighted random: 70% Attack, 20% Special Move, 10% nothing (hesitate).
   - The "random" is simulated using a cycling variable (`VAR_TEMP_1` increments each frame on the overworld and wraps at 100). Read `VAR_TEMP_1` at the start of the enemy turn.
   - If `VAR_TEMP_1` < 70: Enemy uses basic attack.
   - If `VAR_TEMP_1` >= 70 and < 90: Enemy uses special move (defined per enemy type via `VAR_ENEMY_ID` conditionals).
   - If `VAR_TEMP_1` >= 90: Enemy hesitates. Display "[Enemy] is watching carefully..." No damage dealt.
2. **Enemy Attack Calculation:**
   - `VAR_DAMAGE_CALC` = `VAR_ENEMY_ATK` - (`VAR_PLAYER_DEF` / 2)
   - If `VAR_GUARD_ACTIVE` == 1 (target is guarding), divide `VAR_DAMAGE_CALC` by 2.
   - If `VAR_DAMAGE_CALC` < 1, set to 1.
   - Subtract from target's HP (`VAR_PLAYER_HP` or `VAR_COMP_HP` — enemy targets the character with lowest HP, checked via comparison).
3. **Display result:** "[Enemy] attacks [Target]! [X] damage!"
4. **Check if player defeated:** If `VAR_PLAYER_HP` <= 0, jump to Lose Condition.
5. **Check if companion defeated:** If `VAR_COMP_HP` <= 0, display "[Companion] is knocked out!" Companion can no longer act this battle (but is revived at 1 HP after battle).
6. **Reset `VAR_GUARD_ACTIVE` to 0** at end of enemy turn.

### Phase 8: End of Round

1. **Apply status effects:**
   - If `VAR_STATUS_PLAYER` == 1 (poison): Subtract 3 from `VAR_PLAYER_HP`. Display "Edyn takes poison damage!"
   - If `VAR_STATUS_COMP` == 1 (poison): Subtract 3 from `VAR_COMP_HP`.
   - If `VAR_STATUS_ENEMY` == 1 (poison): Subtract 3 from `VAR_ENEMY_HP`. Check defeat.
2. **Update overlay display** with current HP/MP values.
3. **Loop back to Phase 1** (new round).

---

## Player Action Menu Details

### Attack

The basic physical attack. Uses the equipped weapon's ATK bonus (already factored into `VAR_PLAYER_ATK` when equipment is changed). Always available. Cannot miss (no accuracy system — kept simple for GB Studio variable math).

### Magic

Opens a sub-menu listing available spells. Spells are unlocked via flag variables:
- `VAR_SPELL_AETHER_BOLT` (unlocked: game start)
- `VAR_SPELL_TEMPORAL_SLOW` (unlocked: after Verdant Meridian)
- `VAR_SPELL_CHRONO_STRIKE` (unlocked: after Hollow Meridian)

Companion spells are tied to the companion:
- Lira's spells are available when `VAR_COMP_ACTIVE` == 1
- Rook's spells are available when `VAR_COMP_ACTIVE` == 2

The sub-menu is implemented as a Display Menu with up to 4 choices (GB Studio's menu limit). If the player has more than 4 spells, pagination is handled by a "More..." option.

### Item

Opens inventory sub-menu showing consumable items with quantity > 0. Uses variables `VAR_ITEM_POTION`, `VAR_ITEM_HI_POTION`, `VAR_ITEM_AETHER_CRYSTAL`, `VAR_ITEM_ANTIDOTE`, `VAR_ITEM_SMOKE_BOMB`. Each is checked; only items with quantity > 0 are displayed.

### Flee

Attempts to escape combat. Success rate: `base 50% + (VAR_PLAYER_SPD - VAR_ENEMY_SPD) * 5%`. Capped at 90% max, 10% min. Boss fights (`VAR_BOSS_FLAG` == 1) disable Flee entirely.

Implementation: Read `VAR_TEMP_1` (cycling 0–99). Calculate threshold: 50 + (SPD difference * 5). If `VAR_TEMP_1` < threshold, flee succeeds. On success: Fade Out, switch to return scene using `VAR_RETURN_SCENE`, restore player position.

---

## Enemy AI Logic

### Standard Enemy AI

Standard enemies follow a simple priority system:

1. If enemy HP < 25% of max: 50% chance to use special move, 50% attack.
2. If player HP < 25% of max: 80% attack (tries to finish player off).
3. Otherwise: 70% attack, 20% special, 10% hesitate.

Special moves vary by enemy type and are defined in per-enemy conditional blocks within the enemy turn script.

### Boss AI

Boss AI is significantly more complex and hand-scripted per boss. Each boss has a dedicated AI script within the battle scene that overrides the standard logic when `VAR_BOSS_FLAG` == 1.

Boss AI features:
- **Phase transitions:** When boss HP drops below thresholds, `VAR_ENEMY_PHASE` increments, changing available attacks, stats, and behavior.
- **Pattern attacks:** Bosses follow partially predictable patterns (e.g., Attack, Attack, Special, Attack, Ultimate) that players can learn and plan around.
- **Dialogue triggers:** At phase transitions, Display Dialogue events show boss dialogue mid-fight.
- **Scripted events:** Some bosses trigger screen effects (palette flash, screen shake) during ultimate attacks.

---

## Damage Formula

### Physical Damage

```
Damage = Attacker_ATK - (Defender_DEF / 2)
Minimum Damage = 1
```

**GB Studio Implementation:**
1. `Set VAR_TEMP_1 to VAR_ENEMY_DEF` (or `VAR_PLAYER_DEF` if enemy attacking)
2. `Divide VAR_TEMP_1 by 2`
3. `Set VAR_DAMAGE_CALC to VAR_PLAYER_ATK` (or `VAR_ENEMY_ATK`)
4. `Subtract VAR_TEMP_1 from VAR_DAMAGE_CALC`
5. `If VAR_DAMAGE_CALC < 1, Set VAR_DAMAGE_CALC to 1`
6. `Subtract VAR_DAMAGE_CALC from target HP variable`

### Magic Damage

```
Damage = (Attacker_ATK + Spell_Power) - (Defender_DEF / 2)
Minimum Damage = 1
```

Spell Power is a constant added per spell (e.g., Aether Bolt adds 4, Chrono Strike adds ATK again effectively doubling it).

### Healing

```
Heal Amount = Fixed value per spell/item
New HP = Current HP + Heal Amount
If New HP > Max HP, set New HP = Max HP
```

---

## Status Effects

| Status | Effect | Duration | How to Script |
|--------|--------|----------|---------------|
| Poison | -3 HP per round end | Until cured (Antidote or Purify) | Set `VAR_STATUS_[TARGET]` to 1. At end of each round, if status == 1, subtract 3 from HP. |
| Slow | -5 SPD, enemy always goes first | Rest of battle | Set `VAR_STATUS_[TARGET]` to 2. Reduce SPD variable by 5. Override turn order. |
| Stun | Skip one turn | 1 round | Set `VAR_STATUS_ENEMY` to 3. On enemy turn, if status == 3, display "[Enemy] is stunned!" and skip. Set status to 0 at end of round. |
| Guard | Halve incoming damage | 1 round | Set `VAR_GUARD_ACTIVE` to 1. Divide damage by 2 during damage application. Reset to 0 at round end. |

Status effects are kept minimal to avoid variable bloat. Each character has one status variable that holds a single status (0–3). Only one status can be active at a time; new statuses overwrite old ones.

---

## Win Condition

When `VAR_ENEMY_HP` <= 0:

1. **Display victory message:** "[Enemy Name] is defeated!"
2. **Award XP:** Add `VAR_ENEMY_XP` to `VAR_PLAYER_XP`. Display "Gained [X] XP!"
3. **Award Gold:** Add `VAR_ENEMY_GOLD` to `VAR_PLAYER_GOLD`. Display "Found [X] Gold!"
4. **Check loot drop:** Each enemy has a loot table. Use `VAR_TEMP_1` (cycling random) to determine if a drop occurs. If yes, increment the appropriate item variable. Display "Obtained [Item Name]!"
5. **Check level up:** Compare `VAR_PLAYER_XP` against `VAR_PLAYER_LEVEL_THRESHOLD`. If XP >= threshold, trigger level up (see 06-progression-and-rpg-systems.md).
6. **Heal companion:** If companion was knocked out, set `VAR_COMP_HP` to 1 (revived but weak).
7. **Mark enemy as defeated:** Set `VAR_ENEMY_DEFEATED` to the enemy actor's ID so the overworld script can hide it.
8. **Transition back:** Fade Out, switch to `VAR_RETURN_SCENE`, set player position to `VAR_RETURN_X`, `VAR_RETURN_Y`. Fade In.
9. **Remove overworld enemy actor:** On the return scene's Init script, check `VAR_ENEMY_DEFEATED` and hide the corresponding actor.

---

## Lose Condition

When `VAR_PLAYER_HP` <= 0 (and Edyn is the last standing party member):

1. **Display defeat message:** "Edyn falls..."
2. **Fade to black.**
3. **Display Game Over text overlay:** "GAME OVER" centered on screen.
4. **Display menu:** "Continue from last save? Yes / No"
   - **Yes:** Load save data (restore all variables from save slots), switch to saved scene.
   - **No:** Return to title screen.

There is no death penalty beyond returning to the last save. This is a deliberate design choice for accessibility — the game's challenge comes from boss strategy, not resource attrition.

---

## How Boss Fights Differ from Standard Combat

| Aspect | Standard Combat | Boss Combat |
|--------|----------------|-------------|
| Flee | Available | Disabled (`VAR_BOSS_FLAG` = 1) |
| Enemy Phases | 1 phase | 2–3 phases with stat changes and new attacks |
| AI | Simple random-weighted | Hand-scripted patterns with phase transitions |
| Dialogue | None during combat | Boss speaks at phase transitions |
| Screen Effects | None | Screen shake, palette flash on ultimate attacks |
| Rewards | XP + Gold + chance loot | XP + Gold + guaranteed unique item + story progression |
| Music | Standard battle theme | Unique boss battle theme |
| Arena | Generic battle_arena scene | Unique boss arena scene with themed background |
| Post-Fight | Return to overworld | Cutscene plays before return |

### Boss Phase Transitions

When a boss's HP drops below a threshold:
1. Set `VAR_ENEMY_PHASE` to next phase.
2. Display boss dialogue (mid-fight cutscene).
3. Update boss stats: `VAR_ENEMY_ATK`, `VAR_ENEMY_DEF`, `VAR_ENEMY_SPD` change per phase.
4. Change boss actor animation state (if applicable).
5. Optional: Screen effect (shake, flash).
6. Resume combat with new phase behavior.

Thresholds are boss-specific (detailed in 08-bosses.md) but follow a general pattern:
- Phase 1: 100% to 50% HP
- Phase 2: 50% to 20% HP (or 0% for 2-phase bosses)
- Phase 3: 20% to 0% HP (final bosses only)

---

## Combat Scene Custom Events (Reusable Scripts)

To keep the battle system manageable, the following should be built as GB Studio Custom Events:

| Custom Event Name | Purpose |
|-------------------|---------|
| `CE_Calculate_Damage` | Takes attacker ATK and defender DEF, outputs damage to `VAR_DAMAGE_CALC` |
| `CE_Apply_Damage_To_Enemy` | Subtracts `VAR_DAMAGE_CALC` from `VAR_ENEMY_HP`, checks for defeat |
| `CE_Apply_Damage_To_Player` | Subtracts `VAR_DAMAGE_CALC` from `VAR_PLAYER_HP`, checks for defeat |
| `CE_Apply_Damage_To_Companion` | Subtracts `VAR_DAMAGE_CALC` from `VAR_COMP_HP`, checks for KO |
| `CE_Load_Enemy_Stats` | Reads `VAR_ENEMY_ID` and sets all enemy stat variables |
| `CE_Display_Battle_HUD` | Updates the overlay text with current HP/MP for all combatants |
| `CE_Player_Action_Menu` | Shows the 4-option action menu and sets `VAR_PLAYER_ACTION` |
| `CE_Magic_Submenu` | Shows available spells and handles selection |
| `CE_Item_Submenu` | Shows inventory and handles item use |
| `CE_Enemy_AI_Standard` | Standard enemy AI decision tree |
| `CE_Enemy_AI_Boss` | Boss-specific AI with phase checks |
| `CE_Apply_Status_Effects` | Applies end-of-round status damage and checks |
| `CE_Check_Level_Up` | Compares XP to threshold and applies stat increases |
| `CE_Battle_Win` | Handles victory: XP, Gold, loot, transition |
| `CE_Battle_Lose` | Handles defeat: Game Over screen, continue/quit |
| `CE_Flee_Attempt` | Calculates flee success and handles result |

---

*Chronospire: The Shattered Meridian — Combat System Document*
