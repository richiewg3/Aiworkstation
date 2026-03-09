# 07 — Bosses

---

## Boss Summary Table

| Boss | World | HP (Total) | Phases | Sprite Size | Story Connection |
|---|---|---|---|---|---|
| Briar Sentinel | World 1 | 16 (8+8) | 2 | 16×32 (tall) | Corrupted guardian of the Verdant Hearthstone |
| Glacial Wyrm | World 2 | 20 (10+10) | 2 | 16×32 (tall) | Corrupted ice dragon of the Frostfang Peaks |
| Abyssal Leviathan | World 3 | 24 (12+12) | 2 | 16×32 (tall) | Shadow-born kraken guarding the Brine Hearthstone |
| Molten Warden | World 4 | 30 (10+10+10) | 3 | 16×32 (tall) | Corrupted master smith of the Cinderforge |
| Shade (Mini-Boss) | World 5 | 12 | 1 | 16×16 (standard) | Aldric, fallen Lamplighter and Varek's agent |
| Varek, the Hollow King | World 5 | 32 (16+16) | 2 | 16×32 (tall) | Final boss, the man who extinguished the Hearthstones |

---

## Boss 1: Briar Sentinel

### Overview

**Name:** Briar Sentinel

**Visual Description:** A towering plant creature made of twisted vines, bark, and thorns. Its body is roughly humanoid but hunched — broad shoulders, long arms that drag on the ground, and a wide, flat head with a single glowing green eye surrounded by petal-like growths. Its torso is a mass of intertwined roots wrapped around a core of pulsing green light (the Hearthstone's residual energy, corrupted). Thorns protrude from every surface. Purple-black shadow veins run through the vine body, pulsing with each heartbeat. It is rooted in the ground but can shift its position by extending and retracting roots.

**Story Connection:** The Briar Sentinel was the Verdant Hearthstone's natural guardian — a being grown from the Hearthstone's own energy to protect it from harm. The Hollow Tide corrupted it, turning its protective instinct into blind aggression. It cannot distinguish Solen from a threat. Defeating it doesn't kill it — it purifies it, restoring it to its original dormant state once the Hearthstone is reignited.

### Boss Arena Layout

A flat main platform spanning ~14 tiles. The Hearthstone is in the background center, pulsing weakly. Two raised mossy platforms (3 tiles wide, 3 tiles above ground) on the left and right sides. The Briar Sentinel occupies the right-center of the arena. Side walls allow wall-jumping. The floor has root veins running along it that glow during the root attack telegraph.

### Phase 1 — The Rooted Guardian (8 HP)

**Behavior:**
- The Sentinel is rooted in place at the right-center of the arena and cannot move.
- **Root Strike:** Every 3 seconds, roots burst from the ground at the player's current position (1-second telegraph — the floor glows green at the target location). Roots deal 2 HP on contact and create a 1-tile hazard zone for 2 seconds after emerging.
- **Vine Sweep:** Every 8 seconds, the Sentinel sweeps one of its long arms across the ground in a wide arc covering ~6 tiles. The sweep is telegraphed by the arm raising for 0.5 seconds. Deals 2 HP and heavy knockback. Can be ducked under on the raised platforms or jumped over.
- **Thorn Spit:** Every 5 seconds, the Sentinel spits 3 thorn projectiles in a spread pattern from its mouth. Projectiles travel at speed 96 and deal 1 HP each. The telegraph is the Sentinel opening its mouth wide for 0.3 seconds.

**Weak Point:** The glowing green eye. It can only be hit when the Sentinel opens its eye wide — which it does for 2 seconds after each Vine Sweep (it tracks the player to aim the next Root Strike, momentarily exposing the eye). The player must hit the eye during this window. Each hit deals normal attack damage.

**How to Defeat Phase 1:** Land enough hits on the eye to deplete 8 HP. After the 8th HP of damage, the Sentinel roars, the vines around its lower body shatter, and it enters Phase 2.

### Phase 2 — The Unleashed Tangle (8 HP)

**Behavior:**
- The Sentinel tears free from the ground and becomes mobile, shuffling left and right slowly (speed 48).
- **Root Eruption:** Roots burst from the ground in a wave pattern — three sequential eruptions traveling left or right across the arena. Must be jumped over. 2 HP per root hit.
- **Slam:** The Sentinel raises both arms and slams the ground, causing falling bramble debris from above (3 random positions). Debris deals 2 HP. The slam itself creates a 3-tile shockwave along the ground. Telegraph: arms raised for 1 second.
- **Thorn Spray:** Same as Phase 1 but 5 projectiles in a wider spread.
- **Enrage (below 3 HP):** Attacks speed up by 25%. Eye opens more frequently but for shorter windows (1.5 seconds instead of 2).

**Weak Point:** Same — the green eye, now exposed more frequently due to the Sentinel's more aggressive posture. The eye is visible during the recovery after each Slam (1.5-second window).

**How to Defeat Phase 2:** Land enough hits on the eye to deplete the remaining 8 HP. Upon defeat, the Sentinel collapses, the shadow veins drain from its body, and it reverts to a dormant mound of healthy green vines. The eye closes peacefully.

### Pre-Fight Cutscene Dialogue

*[The ground trembles. Roots burst from the earth around the Hearthstone. The Briar Sentinel rises, towering over Solen. Its single green eye fixes on her.]*

**Text Box:** *"The ground splits — a massive guardian rises from the roots. Its eye burns with corrupted light. It doesn't see a Lamplighter. It sees a threat."*

**Solen:** "Easy, big guy. I'm here to help. I just need to—"

*[The Sentinel roars. Vines lash the ground.]*

**Solen:** "Okay, not the talking type. Fine."

### Post-Fight Cutscene Dialogue

*[The Sentinel collapses. Its shadow veins drain. The body softens into dormant vines. The Hearthstone glows brighter. Solen approaches and touches her lantern to the crystal.]*

*[Flash of green light. The forest around the clearing blooms — leaves unfurl, mushrooms glow, flowers open.]*

**Solen:** "That's one. Four more to go."

*[She turns and sees petrified villagers scattered through the now-blooming forest. A farmer, a child, a couple holding hands.]*

**Solen:** "...Oh."

*[Fern appears from the Thornveil path.]*

**Fern:** "The light brought the forest back, but... they're still stone."

**Solen:** "They need all five Hearthstones. I have to keep going."

**Fern:** "You can't carry them all at once. But you can carry the light to the next stone. And the next. That's how lamplighters work, isn't it? One lantern at a time."

*[Solen nods. She looks at the petrified farmer one more time, then turns and walks toward the exit. Her lantern burns brighter than before.]*

### Animation States

| State | Frames | Description |
|---|---|---|
| Idle (rooted) | 2 | Slight sway, eye scanning, thorns pulsing |
| Root Strike | 3 | Body tenses, roots erupt from ground |
| Vine Sweep | 3 | Arm raises, sweeps across arena |
| Thorn Spit | 2 | Mouth opens, thorns fire |
| Phase Transition | 4 | Vines shatter at base, body lurches free |
| Idle (mobile) | 2 | Shuffling in place, arms dragging |
| Slam | 3 | Arms raise, slam ground, shockwave |
| Root Eruption | 3 | Body pulses, roots wave across floor |
| Eye Expose | 2 | Eye opens wide, vulnerable glow |
| Hurt | 2 | Flinch, shadow sparks fly from eye |
| Defeat | 4 | Collapses, shadow drains, reverts to green mound |

**Sprite Size:** 16×32 px (tall)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Bark | `#1C2810` | Body shadow, thorns, roots |
| Color 2 | Vine Green | `#4A7830` | Body, arms, vines |
| Color 3 | Hearthstone Green | `#78E048` | Eye, core glow, petal highlights |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer boss. 16x32 pixel tall boss sprite of a towering plant guardian creature. Hunched humanoid form made of twisted vines, bark, and thorns. Broad shoulders, long dragging arms, wide flat head with single glowing green eye surrounded by petal growths. Torso is intertwined roots around a pulsing green core. Purple-black shadow veins run through the body. Thorns protrude everywhere. Sprite rows: idle rooted (2 frames swaying), root strike attack (3 frames), vine sweep arm attack (3 frames), thorn spit from mouth (2 frames), phase transition — base vines shatter, body lurches free (4 frames), idle mobile shuffling (2 frames), slam both arms — raise and ground pound with shockwave (3 frames), root eruption wave (3 frames), eye expose vulnerable (2 frames), hurt flinch (2 frames), defeat — collapses, shadow drains, reverts to dormant green mound (4 frames). GBC style, 4-color palette: transparent, dark bark #1C2810, vine green #4A7830, hearthstone green #78E048. Clean pixel art, no anti-aliasing, indexed color.

---

## Boss 2: Glacial Wyrm

### Overview

**Name:** Glacial Wyrm

**Visual Description:** A serpentine ice dragon approximately 5 tiles long from head to tail. Its body is segmented — a wedge-shaped head with curved horns, a long sinuous neck, and a coiling body of overlapping ice-crystal scales. Its scales are pale blue-white with a faint inner glow, like light through a glacier. Two large, narrow eyes glow bright ice-blue. Its mouth opens to reveal rows of icicle-like teeth and a blue-white mist (ice breath). Wings — vestigial, crystalline, and translucent — fold against its back. Shadow corruption shows as purple-black frost patterns across its scales and a purple tinge to the ice breath.

**Story Connection:** The Glacial Wyrm is an ancient creature of the Frostfang Peaks, drawn to the Frost Hearthstone's energy and corrupted by the Hollow Tide. Unlike the Briar Sentinel, the Wyrm is not a guardian — it's a predator that claimed the weakened Hearthstone as its nest. Defeating it drives it away; it is not killed but purified and released.

### Boss Arena Layout

A narrow summit ledge (~12 tiles wide). The Hearthstone is at the right side in the stone shrine. Two elevated platforms (shrine pillars, 2 tiles wide, 4 tiles high). The left edge is a bottomless pit (fall = death). Wind pushes the player left constantly (low-strength). The Wyrm coils around the right portion of the arena, with its head positioned at the center-top.

### Phase 1 — The Coiled Storm (10 HP)

**Behavior:**
- The Wyrm's body is coiled around the Hearthstone and only its head and neck are active.
- **Ice Breath:** The Wyrm sweeps its head across the arena floor, exhaling a cone of ice breath. The breath covers ~4 tiles horizontally and freezes the ground tiles it touches (making them slippery for 5 seconds). Deals 2 HP on contact. Telegraph: the Wyrm inhales for 0.5 seconds (mist gathers at mouth).
- **Tail Whip:** The Wyrm's tail lashes out from behind the coil, sweeping the lower portion of the arena. Deals 2 HP and heavy knockback toward the left edge. Telegraph: tail tip vibrates for 0.5 seconds.
- **Icicle Drop:** The Wyrm's movement dislodges icicles from the shrine above. 3 icicles fall at random positions, hitting the ground and shattering. Deal 1 HP if hit. Telegraph: shadows appear on the ground where they'll land.

**Weak Point:** The Wyrm's head. The head is vulnerable for 2 seconds after each Ice Breath while the Wyrm pauses to inhale for the next attack. The player must jump and attack the head during this window (the head is ~3 tiles above ground after the breath sweep).

**How to Defeat Phase 1:** Deplete 10 HP by hitting the head. The Wyrm screeches, uncoils from the Hearthstone, and takes flight.

### Phase 2 — The Airborne Assault (10 HP)

**Behavior:**
- The Wyrm flies above the arena, swooping in for attacks. Only the head is targetable during swoops.
- **Dive Bomb:** The Wyrm flies off-screen to the right, then swoops across the arena from right to left at high speed (~3 tiles above ground). Deals 3 HP on contact. Telegraph: a shadow passes over the arena 1 second before the swoop. The player must duck below 3 tiles (stay on ground) or jump over (very precise timing).
- **Ice Barrage:** The Wyrm hovers at the top of the screen and fires 5 ice shard projectiles downward in a rain pattern. Shards deal 1 HP each. Telegraph: Wyrm opens mouth wide, glowing ice visible inside for 0.5 seconds.
- **Frost Slam:** The Wyrm slams its tail into the arena, creating a frost shockwave along the ground. Deals 2 HP. The shockwave travels the full width of the arena. Must be jumped over. Telegraph: Wyrm rises high, tail visibly winds up for 1 second.

**Weak Point:** The head, during the recovery moment after each Dive Bomb. The Wyrm pauses at the left edge for 1.5 seconds after a swoop before flying back up. The player must be at the left side of the arena to reach it — which is dangerously close to the pit edge with wind pushing.

**How to Defeat Phase 2:** Deplete the remaining 10 HP. Upon defeat, the Wyrm crashes to the arena, the shadow corruption shatters off its scales like ice, and it shrinks to a smaller, docile form. It coils around the Hearthstone gently, then flies away into the clearing sky.

### Pre-Fight Cutscene Dialogue

*[The Glacial Wyrm descends from the clouds with a screech. It coils around the Frost Hearthstone, its body obscuring the dim blue crystal. Its eyes lock on Solen.]*

**Text Box:** *"A serpent of ice descends from the storm. Its coils grip the Hearthstone like a dragon guarding its hoard. Frost breath fills the air."*

**Solen:** "You're between me and that stone, and I'm not going to ask politely twice."

*[The Wyrm screeches. Wind intensifies.]*

**Solen:** "Didn't think so."

### Post-Fight Cutscene Dialogue

*[The Wyrm crashes. Shadow ice shatters from its body. It shrinks, looks at Solen with clear blue eyes, then nuzzles the Hearthstone before flying away.]*

*[Solen touches her lantern to the Frost Hearthstone. Blue light blazes. The blizzard softens to gentle snow.]*

**Solen:** "Two down. It's getting warmer... well, less cold."

*[She notices the hidden passage behind the shrine.]*

**Solen:** "What's this?"

*[She enters the hidden chamber and finds the First Keeper mural.]*

**Solen:** "Five Hearthstones... but what's that in the center? A sixth light? The lore never mentioned a sixth light."

*[She sketches the mural in her journal.]*

**Solen:** "I'll figure this out later. Three more stones to go."

### Animation States

| State | Frames | Description |
|---|---|---|
| Coiled Idle | 2 | Coiled around Hearthstone, head sways, eyes scan |
| Ice Breath | 4 | Inhale, sweep head across arena, exhale cone |
| Tail Whip | 3 | Tail lashes from behind coil |
| Uncoil/Fly | 4 | Screeches, uncoils, wings spread, takes flight |
| Flying Idle | 2 | Circling above arena |
| Dive Bomb | 3 | Off-screen, swoops across arena |
| Ice Barrage | 3 | Hovers, mouth opens, fires shards |
| Frost Slam | 3 | Rises, tail winds up, slams ground |
| Hurt | 2 | Flinch, ice crystals crack on head |
| Defeat | 4 | Crashes, shadow ice shatters, shrinks to docile form |

**Sprite Size:** 16×32 px (tall) — head and upper body; body segments are separate 16×16 actors

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Frost | `#102838` | Body shadow, scale edges, horns |
| Color 2 | Glacier Blue | `#78A8C8` | Scales, body, wings |
| Color 3 | Ice White | `#D8F0FF` | Eye glow, breath, scale highlights, crystal tips |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer boss. 16x32 pixel tall boss sprite of a serpentine ice dragon. Wedge-shaped head with curved horns, narrow glowing ice-blue eyes, mouth with icicle teeth and blue-white frost breath mist. Long sinuous neck. Overlapping ice-crystal scales in pale blue-white with inner glow. Vestigial translucent crystalline wings. Purple-black frost corruption patterns on scales. Sprite rows: coiled idle head sway (2 frames), ice breath sweep — inhale then exhale cone (4 frames), tail whip lash (3 frames), uncoil and take flight — screech, wings spread (4 frames), flying idle circling (2 frames), dive bomb swoop (3 frames), ice barrage hovering — mouth opens, fires shards (3 frames), frost tail slam (3 frames), hurt flinch with cracking crystals (2 frames), defeat crash — shadow ice shatters, shrinks to docile form (4 frames). Separate body segment sprite: 16x16 coiling body section with scales. GBC style, 4-color palette: transparent, deep frost #102838, glacier blue #78A8C8, ice white #D8F0FF. Clean pixel art, no anti-aliasing, indexed color.

---

## Boss 3: Abyssal Leviathan

### Overview

**Name:** Abyssal Leviathan

**Visual Description:** A massive kraken-like creature — only its tentacles and a single enormous eye are visible in the arena. The body lurks in the deep water below the arena. Each tentacle is a thick, rubbery appendage in dark blue-black with rows of glowing purple suckers. The eye is huge (~3 tiles wide), set in a mass of dark flesh at the bottom of the arena, with a slit pupil that glows violet. When the eye is closed, only a crescent of purple light is visible. Shadow corruption manifests as pulsing purple veins running along each tentacle and a corona of shadow energy around the eye.

**Story Connection:** The Abyssal Leviathan is a creature of the deep Abyssal Sea — one of the Hollow's extensions into Lumara. It is not a corrupted animal but a manifestation of the Hollow itself, sent to guard the Brine Hearthstone after Varek weakened it. It is the first enemy in the game that is purely of the Hollow rather than a corrupted natural creature.

### Boss Arena Layout

An underwater cathedral alcove. The arena is fully submerged. A main platform (mosaic floor) spans the bottom ~8 tiles wide. Two seaweed ladders on the sides allow vertical movement. Two air bubble pockets near the ceiling provide air (the player must surface periodically). The Leviathan's eye is at the bottom center, below the main platform, visible through gaps in the floor mosaic. Tentacles enter from the bottom and sides of the screen.

### Phase 1 — The Grasping Deep (12 HP)

**Behavior:**
- Three tentacles are active, entering the arena from the bottom and sides.
- **Tentacle Slam:** One tentacle rises from below and slams down on a platform section (3-tile impact zone). Deals 2 HP and creates a shockwave through the water. Telegraph: the tentacle tip appears below the platform 1 second before slamming. Player must not be standing in the impact zone.
- **Tentacle Sweep:** A tentacle enters from the side and sweeps horizontally across the arena at a set height. Deals 2 HP. Telegraph: tentacle tip visible at the screen edge for 0.5 seconds, then sweeps. Must be above or below the sweep height.
- **Ink Cloud:** The Leviathan releases a cloud of dark ink that obscures ~4 tiles of the arena for 3 seconds. Player can still move through the cloud but cannot see hazards within it. Telegraph: water around the eye darkens 0.5 seconds before release.

**Weak Point:** The eye. It opens wide for 3 seconds after every third attack (counted per attack cycle). The eye is below the main platform — the player must swim down through a gap in the mosaic floor to reach it and attack. Each hit deals normal damage. The window is tight because the player must also manage air supply.

**How to Defeat Phase 1:** Deplete 12 HP. The Leviathan screeches (bubbles erupt from below), tentacles retract, and the eye closes. Then it opens with a furious violet blaze — Phase 2 begins.

### Phase 2 — The Awakened Maw (12 HP)

**Behavior:**
- Four tentacles now active. The eye remains below but is now actively defensive.
- **Tentacle Cage:** Two tentacles slam down simultaneously on either side of the player, trapping them in a 3-tile zone. A third tentacle then strikes down in the trapped zone after 1 second. Deals 3 HP. Player must dash (if available) or swim upward out of the cage before the third tentacle hits.
- **Ink Barrage:** Multiple small ink projectiles fire upward from below the floor in a spread pattern. 5 projectiles, each dealing 1 HP. Telegraph: purple glow visible through the floor gaps 0.5 seconds before firing.
- **Constrict:** A tentacle wraps around a seaweed ladder, destroying it temporarily (5 seconds). If the player is on the ladder, they take 2 HP and are thrown off. Forces the player to use the remaining ladder for air.
- **Eye Beam (below 4 HP):** The eye fires a beam of concentrated shadow energy in a horizontal line across the bottom of the arena. Deals 3 HP. Telegraph: the eye glows intensely for 1.5 seconds, pupil narrows.

**Weak Point:** Same — the eye, but it opens for shorter windows (2 seconds after every fourth attack). Additionally, when the eye charges the Eye Beam, it is vulnerable during the charge-up (1.5 seconds) — rewarding aggressive play.

**How to Defeat Phase 2:** Deplete the remaining 12 HP. The eye widens, the pupil shrinks to a point, and all tentacles go rigid. Then they retract violently, pulling the Leviathan into the deep. The water clears, the Hearthstone glows brighter, and the arena becomes calm.

### Pre-Fight Cutscene Dialogue

*[Solen swims into the cathedral alcove. The water darkens. A massive eye opens below the mosaic floor, purple light flooding the chamber. Tentacles rise from the depths.]*

**Text Box:** *"The deep stirs. An eye the size of a doorway opens in the abyss below. This is no corrupted creature — this is the Hollow itself, reaching up through the water."*

**Solen:** "That's... significantly bigger than a rabbit."

*[Tentacles slam the floor.]*

**Solen:** "Okay. Big and angry. Same plan as always — hit the glowy part."

### Post-Fight Cutscene Dialogue

*[The Leviathan retracts into the abyss. The water clears. The Brine Hearthstone blazes to life, teal light flooding the cathedral.]*

*[Solen swims to the surface, gasping. She pulls herself onto a dry ledge near the exit.]*

**Solen:** "Three down. I'm running out of breath and running out of luck."

*[She moves toward the exit corridor. A figure steps from the shadows.]*

**Shade:** "Impressive. Three Hearthstones. Three pulses of energy — and Varek caught every one."

**Solen:** "Who are you?"

**Shade:** "Someone who's been watching. Someone who needs you to understand: every Hearthstone you relight sends a pulse through the ley lines. Varek is waiting at the other end with open hands. You've been feeding him, Lamplighter."

**Solen:** "You're lying."

**Shade:** "Ask yourself why the road to each Hearthstone was passable. Why nothing truly stopped you. He's been letting you through. You're his battery."

*[Shade dissolves into shadow and vanishes.]*

**Solen:** "..."

**Solen:** "It doesn't matter. Mother is still stone. There's no other way."

### Animation States

| State | Frames | Description |
|---|---|---|
| Tentacle Rise | 3 | Rises from below, suctions visible |
| Tentacle Slam | 2 | Slams down on platform |
| Tentacle Sweep | 3 | Enters from side, sweeps horizontally |
| Tentacle Cage | 4 | Two slam sides, third strikes center |
| Ink Cloud | 2 | Dark cloud billows from below |
| Ink Barrage | 3 | Projectiles fire upward through floor |
| Eye Idle (closed) | 2 | Crescent of light, slight pulse |
| Eye Open (vulnerable) | 2 | Wide open, pupil dilated, violet glow |
| Eye Beam Charge | 2 | Intense glow, pupil narrows |
| Eye Beam Fire | 2 | Horizontal beam across arena bottom |
| Hurt | 2 | Eye flinches, pupil contracts |
| Defeat | 4 | Eye widens, tentacles go rigid, retracts violently |

**Sprite Size:** Tentacles: 16×32 px (tall) each. Eye: 16×16 px (uses 2 actors for full eye at 32×16).

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Abyssal Black | `#06101C` | Tentacle shadow, eye flesh |
| Color 2 | Deep Brine | `#284060` | Tentacle body, eye outer |
| Color 3 | Hollow Violet | `#A848D8` | Suckers, eye pupil, ink projectiles, beam |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer boss. Multiple sprite components for a massive underwater kraken boss. TENTACLE (16x32 tall): thick rubbery dark blue-black tentacle with rows of glowing purple suckers and pulsing purple veins. Sprite rows: rise from below (3 frames), slam down (2 frames), sweep horizontal (3 frames), cage formation (4 frames), constrict wrap (2 frames), retract (2 frames). EYE (32x16 using two 16x16 sprites): enormous eye with dark flesh surround, slit pupil glowing violet, pulsing corona of shadow energy. Sprite rows: closed crescent (2 frames), open vulnerable (2 frames), beam charge intense glow (2 frames), beam fire horizontal (2 frames), hurt flinch (2 frames), defeat — widens then retracts (4 frames). INK: separate 8x8 projectile sprites — ink blob dark purple. GBC style, 4-color palette: transparent, abyssal black #06101C, deep brine #284060, hollow violet #A848D8. Clean pixel art, no anti-aliasing, indexed color.

---

## Boss 4: Molten Warden

### Overview

**Name:** Molten Warden

**Visual Description:** An enormous humanoid figure made of slag metal and shadow-fire. It was once the master smith of the Cinderforge — a living construct created by the First Keepers to operate the forge machinery. Now corrupted, it has grown to twice its original size. Its body is cooled dark metal with cracks that glow molten orange-red. Its head is a featureless dome with a horizontal slit that serves as an eye — a line of orange fire. Its arms end in massive fists — one shaped like a hammer, the other like an anvil. Magma drips from its joints. Shadow corruption manifests as purple-black slag crusting its shoulders and back, and the occasional flash of purple within the orange glow.

**Story Connection:** The Molten Warden was the Cinderforge's protector and chief operator. When Varek extinguished the Forge Hearthstone — the first to go fully dark — the Warden was overwhelmed by the Hollow Tide and corrupted into a mindless destroyer. It represents the Forge's death: the fires that once created now only destroy.

### Boss Arena Layout

Wide platform (~16 tiles) with magma pits on both sides (fall = death). The Forge Hearthstone is at the back center, encased in cracked shadow-obsidian. Two elevated platforms (broken First Keeper pillars, 2 tiles wide, 4 tiles above ground) at left-center and right-center. Two lava geysers built into the floor at set positions erupt on a 5-second timer. The Warden starts at the right side of the arena.

### Phase 1 — The Forge's Fist (10 HP)

**Behavior:**
- The Warden walks slowly toward the player (speed 48). It is always advancing.
- **Hammer Slam:** Raises its hammer-fist and slams the ground. Creates a 3-tile shockwave along the floor. Deals 3 HP (direct hit) or 1 HP (shockwave). Telegraph: arm raises for 1 second, fist glows brighter.
- **Magma Spit:** Opens its eye-slit wide and spits a glob of magma in a parabolic arc toward the player. The glob lands and creates a small lava pool that persists for 5 seconds. Deals 2 HP on direct hit, 1 HP from lava pool. Telegraph: eye slit widens and glows for 0.5 seconds.
- **Charge:** Leans forward and charges across the arena at speed 144. Deals 3 HP on contact. Telegraph: leans forward, metal grinding sound for 0.5 seconds, then charges. Hits the wall at the end and is stunned for 2 seconds (vulnerable).

**Weak Point:** The eye-slit. Vulnerable at all times when in melee range (head is at ~3 tiles high), but the best opportunity is during the 2-second stun after a Charge.

**How to Defeat Phase 1:** Deplete 10 HP. The Warden staggers, its hammer-arm cracks and falls off. It roars, and the broken arm reforms into a whip of molten chains.

### Phase 2 — The Chain Whip (10 HP)

**Behavior:**
- The Warden is faster now (speed 64), more aggressive.
- **Chain Whip:** Lashes the chain-arm in a wide arc — covers ~6 tiles horizontally and ~3 tiles vertically. Deals 2 HP. Much faster than the Vine Sweep, but lower range vertically. Telegraph: chain clinks and pulls back for 0.3 seconds.
- **Anvil Drop:** Raises its anvil-fist and drops it straight down, creating a massive shockwave (full arena width). Must be jumped. Deals 2 HP. Telegraph: rises to full height, anvil-arm raised for 1 second.
- **Magma Eruption:** Slams both arms on the ground, triggering all lava geysers simultaneously plus 2 additional eruptions at random positions. Deals 3 HP per eruption hit. Telegraph: both arms slam ground, camera shakes for 0.5 seconds before eruptions.

**Weak Point:** Eye-slit, same as Phase 1. Vulnerable for 1.5 seconds after the Anvil Drop (recovery animation).

**How to Defeat Phase 2:** Deplete 10 HP. The Warden collapses to one knee. Phase 3 begins.

### Phase 3 — The Dying Fire (10 HP)

**Behavior:**
- The Warden is on one knee, damaged, but desperate. Its body cracks open further, exposing the corrupted core inside — a mass of purple-black shadow swirling around a faintly orange core.
- **Core Blast:** The exposed core fires 3 beams of shadow energy in a fan pattern. Each beam sweeps slowly. Deals 3 HP. Telegraph: core pulses purple for 1 second.
- **Desperation Slam:** Slams the ground with its remaining arm repeatedly — 3 rapid slams, each creating a small shockwave. Deals 2 HP per slam. Less telegraph (0.3 seconds per slam).
- **Meltdown (below 3 HP):** The Warden's body begins to dissolve. Magma drips constantly from every crack, creating hazard zones around the Warden. The arena effectively shrinks as magma pools form.

**Weak Point:** The exposed core. It glows orange between attacks and is vulnerable for 2 seconds after each Core Blast. The player must get close to the Warden (past the dripping magma) to hit it.

**How to Defeat Phase 3:** Deplete the final 10 HP. The Warden freezes, its core collapses inward, and the entire body cools to dark stone and crumbles.

### Pre-Fight Cutscene Dialogue

*[The shadow-obsidian shell around the Hearthstone cracks from the redirected magma. The cracks spread to the floor. The Molten Warden erupts from the broken ground, magma and shadow fire cascading off its body.]*

**Text Box:** *"The forge's master rises — a colossus of slag and shadow, its fires turned to destruction. The hammer-arm rises. The eye-slit burns."*

**Solen:** "You used to build things, didn't you? I'm sorry about what comes next."

*[The Warden roars — a sound of grinding metal and rushing magma.]*

### Post-Fight Cutscene Dialogue

*[The Warden crumbles. The Forge Hearthstone is exposed, pulsing weakly. Solen touches her lantern to it.]*

*[Flash of orange light. The forges ignite with clean fire. Magma returns to natural orange-gold. The machinery hums.]*

*[Wrench appears, climbing over debris.]*

**Wrench:** "You did it! The forge — it's alive again! I haven't heard that hum in months."

**Solen:** "Wrench? You made it out?"

**Wrench:** "Your route was clear enough. Solen... I need to tell you something. I knew your father. Edric."

**Solen:** "...You knew my father?"

**Wrench:** "We worked the same mine. I was the one who signed off on the tunnel. The one that collapsed. It was my inspection, my stamp. I've carried that for twelve years."

**Solen:** "..."

**Wrench:** "He was carving this for you. A little wooden lantern. Kept it in his pocket. I found it after. I never knew who to give it to."

*[He hands Solen the small, unfinished wooden figurine. She holds it. Her hands shake.]*

**Solen:** "He... he never got to finish it."

**Wrench:** "No. He didn't."

*[Silence. Solen presses the figurine to her chest. A tear. Then she wipes her face, puts the figurine in her pack, and straightens.]*

**Solen:** "One more stone. The Spire."

**Wrench:** "Give Varek hell, kid."

### Animation States

| State | Frames | Description |
|---|---|---|
| Walk Forward | 4 | Heavy stomping gait, magma drips with each step |
| Hammer Slam | 3 | Arm raises, slams, shockwave radiates |
| Magma Spit | 3 | Eye-slit widens, glob fires in arc |
| Charge | 3 | Lean, charge, hit wall stunned |
| Phase 2 Transition | 4 | Arm breaks, reforms as chain whip |
| Chain Whip | 3 | Chain pulls back, lashes in arc |
| Anvil Drop | 3 | Rise, arm up, drop with full-arena shockwave |
| Magma Eruption | 3 | Both arms slam, geysers erupt |
| Phase 3 Transition | 4 | Collapses to knee, body cracks, core exposed |
| Core Blast | 3 | Core pulses, fires beam fan |
| Desperation Slam | 4 | Rapid repeated arm slams |
| Hurt | 2 | Flinch, sparks from eye-slit or core |
| Defeat | 4 | Freezes, core collapses, body cools to stone, crumbles |

**Sprite Size:** 16×32 px (tall)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Slag | `#181010` | Body shadow, cooled metal |
| Color 2 | Iron Gray | `#605048` | Body surface, arms, legs |
| Color 3 | Molten Orange | `#F08828` | Eye-slit, cracks, magma drips, core glow |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer boss. 16x32 pixel tall boss sprite of a massive humanoid construct made of slag metal and shadow-fire. Featureless dome head with horizontal orange fire eye-slit. One arm is a massive hammer shape, the other an anvil shape. Body is cooled dark metal with glowing orange-red cracks. Magma drips from joints. Purple-black shadow slag on shoulders. Sprite rows: walk forward heavy stomp (4 frames), hammer slam with shockwave (3 frames), magma spit from eye-slit (3 frames), charge forward and stunned at wall (3 frames), phase transition — arm breaks and reforms as chain whip (4 frames), chain whip lash (3 frames), anvil drop with full-width shockwave (3 frames), magma eruption both arms slam (3 frames), phase 3 transition — collapse to knee, body cracks open exposing purple-orange core (4 frames), core blast beam fan (3 frames), desperation rapid slams (4 frames), hurt flinch (2 frames), defeat — freezes, core collapses, crumbles to stone (4 frames). GBC style, 4-color palette: transparent, dark slag #181010, iron gray #605048, molten orange #F08828. Clean pixel art, no anti-aliasing, indexed color.

---

## Mini-Boss: Shade

### Overview

**Name:** Shade (Aldric)

**Visual Description:** See 03-characters.md for full description. As a combat encounter: Shade is fast and agile, teleporting via shadow dissolution and reforming. His attacks use shadow tendrils extending from his cloak.

**Story Connection:** Aldric is a former Lamplighter who followed Varek. He is the last line of defense before Varek's chamber. The fight is emotional — Solen recognizes pieces of Lamplighter technique in his movements.

### Boss Arena Layout

Circular chamber, ~12 tiles wide. Flat floor, no platforms, no hazards. Sealed doors on both sides. The simplicity of the arena makes this fight about pure combat skill, not environmental navigation.

### Phase 1 (12 HP — single phase)

**Behavior:**
- Shade is highly mobile, teleporting every 5 seconds.
- **Shadow Lash:** Extends a shadow tendril from his cloak in a horizontal line, reaching ~4 tiles. Deals 2 HP. Fast attack with minimal telegraph (arm gesture 0.3 seconds before).
- **Shadow Pool Drop:** After teleporting, he leaves a shadow pool at his departure point. The pool persists for 4 seconds and deals 1 HP on contact. This limits the player's safe space over time.
- **Teleport Slash:** Dissolves into shadow, reappears directly behind the player, and slashes immediately. Deals 2 HP. Telegraph: the dissolution takes 0.5 seconds (the player sees him fading). The reappearance is at the player's back, so the player must move or turn quickly.
- **Shadow Barrage (below 4 HP):** Fires 5 shadow bolts in a rapid spread. Each deals 1 HP. Telegraph: cloak flares for 0.5 seconds.

**Weak Point:** Shade's body is vulnerable at all times, but his teleporting makes him hard to hit. The best windows are: immediately after he reappears from a Teleport Slash (0.5-second recovery), and during the Shadow Lash attack (his body is stationary for the 0.5-second arm extension).

**How to Defeat:** Deplete 12 HP. Shade collapses, his mask cracks and falls off, revealing Aldric.

### Pre-Fight Cutscene Dialogue

**Shade:** "You made it this far. I won't pretend I'm not impressed."

**Solen:** "Get out of my way."

**Shade:** "I can't. Varek needs time. I'll give him that."

**Solen:** "You don't have to do this."

**Shade:** "I didn't want this fight, Solen. But you won't stop, and he needs time. I'll give him that much."

### Post-Fight Cutscene Dialogue

*[Shade collapses. His mask cracks and falls away. Solen sees the face beneath — gaunt, hollow-eyed, but recognizable.]*

**Solen:** "Aldric? You're... you were a Lamplighter. You served with my mother."

**Aldric:** *(coughing)* "She... she was the best of us. I'm sorry, Solen. I thought Varek had the answer."

**Solen:** "Why? Why did you follow him?"

**Aldric:** "Because the Hearthstones are chains. He was right about that. We spent our whole lives maintaining a prison and calling it protection. I couldn't live with that."

**Solen:** "And this is better?"

**Aldric:** "No. He's not wrong about the chains, Solen. He's just wrong about what happens when you break them."

*[Aldric's eyes close. The shadow drains from his body. He is still.]*

*[Solen kneels. She takes the Lamplighter badge from his coat and puts it in her pack.]*

**Solen:** "I'll remember. I promise."

### Animation States

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Cloak billows, slight float, eyes glow |
| Shadow Lash | 3 | Arm extends, tendril whips forward |
| Teleport Out | 3 | Dissolves into shadow particles, shadow pool left behind |
| Teleport In | 2 | Reforms from shadow behind player |
| Teleport Slash | 2 | Immediate slash upon reforming |
| Shadow Barrage | 3 | Cloak flares, 5 bolts fire in spread |
| Hurt | 2 | Staggers, mask cracks |
| Defeat | 4 | Collapses, mask falls off, shadow drains, Aldric revealed |

**Sprite Size:** 16×16 px (standard)

**Palette:** Same as Shade in 03-characters.md

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Purple-Black | `#1A0A2E` | Cloak body, shadow tendrils |
| Color 2 | Dark Violet | `#5B2D8E` | Cloak highlights, bolt energy |
| Color 3 | Ghost White | `#E0D8F0` | Mask, eye glow, slash trail |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer mini-boss. 16x16 pixel sprite of a cloaked shadow agent. Tall figure in dark purple-black cloak that moves like living shadow, featureless white mask with glowing violet eye slits, shadow tendrils from cloak edges. Sprite rows: idle billowing cloak (2 frames), shadow lash — arm extends shadow tendril whip forward (3 frames), teleport out — dissolves into shadow particles (3 frames), teleport in — reforms from shadow (2 frames), teleport slash — immediate strike on reform (2 frames), shadow barrage — cloak flares, 5 bolts fire (3 frames), hurt stagger with mask cracking (2 frames), defeat — collapses, mask falls revealing gaunt human face, shadow drains (4 frames). GBC style, 4-color palette: transparent, deep purple-black #1A0A2E, dark violet #5B2D8E, ghost white #E0D8F0. Clean pixel art, no anti-aliasing, indexed color.

---

## Final Boss: Varek, the Hollow King

### Overview

**Name:** Varek, the Hollow King

**Visual Description:** See 03-characters.md for full description. In combat, Varek is a floating figure wreathed in shadow energy. His Phase 1 form is his human-sized self. In Phase 2, he absorbs the Hollow's energy and grows to fill the upper portion of the screen, his crown expanding into a massive corona of shadow crystals.

**Story Connection:** Varek is the game's primary antagonist, the Hollow King, the man who extinguished the Hearthstones to free the Hollow. This fight is the emotional climax of the game.

### Boss Arena Layout

The Spire's Hearthstone Chamber. Wide circular platform (~16 tiles). The Spire Hearthstone is at the back center, encased in Hollow energy. The ceiling is open to the swirling shadow dome above. In Phase 2, the arena tiles begin to crack and fall, reducing the safe area. No side walls — the edges of the platform are a fall to oblivion.

### Phase 1 — The Hollow King (16 HP)

**Behavior:**
- Varek floats ~2 tiles above the ground, moving left and right at moderate speed (80).
- **Shadow Bolt:** Fires a bolt of purple energy at the player. Speed 112, straight line. Deals 2 HP. Telegraph: hand extends, bolt charges for 0.3 seconds. Fires every 3 seconds.
- **Hollow Wave:** Descends to ground level and slams his hand to the floor, sending a wave of shadow energy across the arena. The wave is a ground-level hazard, 2 tiles tall. Deals 2 HP. Must be jumped. Telegraph: Varek descends for 0.5 seconds, hand glows.
- **Shadow Summon:** Raises both arms, summoning 2 Hollow Wisps from the floor. The Wisps function as normal enemies (1 HP, follow player). This adds pressure and forces the player to manage adds while focusing on Varek. Cooldown: 10 seconds between summons. Max 4 Wisps alive at once.
- **Teleport:** Every 8 seconds, Varek dissolves and reappears at a random position in the arena. Brief i-frames during teleport.

**Weak Point:** Varek's body. He is vulnerable at all times but hard to reach because he floats above the ground. The player must use elevated platforms (Phase 1 has two small floating platforms in the arena) or time their jumps/double jumps to reach him. He descends during the Hollow Wave attack, making that the easiest window (but also the most dangerous).

**How to Defeat Phase 1:** Deplete 16 HP. Varek staggers in the air, then laughs. He ascends toward the shadow dome, absorbs a massive amount of Hollow energy, and transforms.

### Phase 2 — The Hollow Incarnate (16 HP)

**Behavior:**
- Varek has grown to 16×32 and fills the upper-center of the screen. He no longer moves horizontally — he is stationary in the center. The arena tiles begin cracking and falling away (the edges of the arena crumble 2 tiles inward over the course of the phase, reducing safe area).
- **Shadow Storm:** Varek raises his arms and shadow bolts rain from above — 6 bolts at random positions across the arena. Each deals 2 HP. Telegraph: arms raise, shadow dome above churns for 1 second. Interval: every 6 seconds.
- **Hollow Beam:** Varek fires a wide beam of shadow energy horizontally across the arena. The beam is ~2 tiles tall and sweeps from one side to the other over 2 seconds. Deals 3 HP. Telegraph: his crown glows, and a line of light appears at one edge of the arena 1 second before the beam fires. Must be ducked under (if beam is high) or jumped over (if beam is low). The height alternates.
- **Void Grasp:** Shadow hands erupt from the crumbling arena floor at the player's position. 3 hands in sequence, each appearing 0.5 seconds apart. Each deals 2 HP. Telegraph: floor tile darkens at target position 0.5 seconds before the hand appears.
- **Desperation (below 4 HP):** All attacks speed up by 30%. Shadow Storm fires 8 bolts. Arena has lost 4 tiles from edges total.

**Weak Point:** Varek's core — a glowing weak point in his chest that becomes visible through cracks in his shadow armor. The core is always the target, but it's high up. The player must use the floating platforms (which also start to crumble in Phase 2) or chain double-jump + dash to reach the core. When Varek takes damage, his shadow armor cracks further, and the core light grows — visually showing progress.

**How to Defeat Phase 2:** Deplete the remaining 16 HP. Varek's shadow armor shatters completely. The Hollow energy dissipates. He shrinks back to human size and collapses on the arena floor. The shadow dome above dissipates. Light breaks through.

### Pre-Fight Cutscene Dialogue

*[Solen enters the Hearthstone Chamber. Varek floats before the Spire Hearthstone, arms spread, absorbing its light.]*

**Varek:** "Ah. The little Lamplighter. Maren's daughter."

**Solen:** "You know my mother."

**Varek:** "I knew her. She was the best of us. She understood the Hearthstones better than anyone — she just couldn't take the final step."

**Solen:** "The step you took? Extinguishing them? Drowning the world in darkness?"

**Varek:** "Freeing the world. The Hearthstones are chains, Solen. Beautiful, warm chains — but chains all the same. The Hollow is the natural state of this world. The First Keepers imprisoned it out of fear."

**Solen:** "And everyone who was turned to stone? My mother? What about them?"

**Varek:** *(pause)* "They would become part of the new world. Not dead. Changed."

**Solen:** "Changed isn't alive. I'd rather light a candle every day for the rest of my life than let you blow out the sun."

**Varek:** "Then we have nothing more to discuss."

*[Varek raises his hands. Shadow energy surges.]*

### Post-Fight Cutscene Dialogue (Normal Ending Path)

*[Varek collapses. His crown shatters. He lies on the floor, human again — gaunt, trembling, the purple fading from his eyes.]*

**Varek:** *(weakly)* "The Hollow... it promised... it said the world would be free..."

**Solen:** "You were wrong, Varek. But I understand why you believed it."

*[Solen walks past him to the Spire Hearthstone. She touches her lantern to the crystal. White light blazes — the fifth and final Hearthstone reignites.]*

*[The five Hearthstones pulse in unison. A wave of golden light sweeps across Lumara.]*

*[Normal ending montage begins.]*

### Post-Fight Cutscene Dialogue (True Ending Path)

*[After the normal post-fight sequence, if the player has all 25 Ember Shards and all 5 Lore Stones:]*

*[The floor behind the Hearthstone opens, revealing a stairway descending into white light.]*

**Solen:** "The sixth light... the mural was real."

*[She descends into the Chamber of Origin. True ending sequence plays — see 02-story-narrative.md.]*

### Animation States

| State | Frames | Description |
|---|---|---|
| Idle (P1) | 4 | Floating, robe billowing, shadow tendrils orbiting |
| Shadow Bolt | 3 | Hand extends, bolt charges, fires |
| Hollow Wave | 3 | Descends, hand to floor, wave radiates |
| Shadow Summon | 3 | Arms raise, Wisps emerge from floor |
| Teleport | 3 | Dissolves, reappears |
| Phase Transition | 4 | Ascends, absorbs Hollow energy, grows, crown expands |
| Idle (P2) | 2 | Massive form, shadow pulsing, crown flickering |
| Shadow Storm | 3 | Arms raise, bolts rain from above |
| Hollow Beam | 3 | Crown glows, beam sweeps horizontally |
| Void Grasp | 3 | Shadow hands erupt from floor |
| Hurt (P1) | 2 | Flinch, shadow sparks |
| Hurt (P2) | 2 | Shadow armor cracks, core light grows |
| Defeat | 6 | Armor shatters, shrinks, collapses, crown dissolves, human form revealed |

**Sprite Size:** 16×32 px (tall) — both phases

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Abyssal Black | `#0D0221` | Robe body, shadow tendrils, crown |
| Color 2 | Deep Violet | `#6A1B9A` | Robe highlights, veins, energy effects, bolts |
| Color 3 | Pale Bone | `#E8D8C8` | Skin, hair, core light, crack-light |

**PIXEL ART GENERATION PROMPT — Full Boss Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer final boss. 16x32 pixel tall boss sprite in two forms. PHASE 1 — HOLLOW KING: gaunt floating man with long white hair, pale skin with purple veins, solid violet glowing eyes, flowing deep purple-black robe, jagged crystallized shadow crown. Shadow tendrils orbit body. Floats above ground. Sprite rows: idle floating (4 frames), shadow bolt — hand extends and fires purple energy bolt (3 frames), hollow wave — descends, hand to floor, wave of shadow (3 frames), shadow summon — arms raise (3 frames), teleport dissolve and reform (3 frames). PHASE 2 — HOLLOW INCARNATE: same figure but grown massive, filling upper screen. Crown expanded into huge corona of shadow crystals. Body has shadow armor with cracks showing glowing core in chest. Sprite rows: idle pulsing (2 frames), shadow storm — arms raise, bolts rain (3 frames), hollow beam — crown glows, horizontal sweep beam (3 frames), void grasp — shadow hands from floor (3 frames). SHARED: hurt flinch phase 1 (2 frames), hurt phase 2 armor cracking (2 frames), defeat — armor shatters, shrinks, collapses to human, crown dissolves (6 frames). GBC style, 4-color palette: transparent, abyssal black #0D0221, deep violet #6A1B9A, pale bone #E8D8C8. Clean pixel art, no anti-aliasing, indexed color.
