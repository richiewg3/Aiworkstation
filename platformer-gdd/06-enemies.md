# 06 — Enemies

---

## Enemy Summary Table

| Enemy | Type | HP | Damage | Speed | Worlds |
|---|---|---|---|---|---|
| Shadow Hare | Ground Patrol | 1 | 1 | 80 | 1 |
| Gloom Bat | Air Patrol | 1 | 1 | 72 | 1, 2, 5 |
| Sporecap | Stationary Shooter | 2 | 1 (spore) | 0 | 1 |
| Thorn Creeper | Wall Patrol | 2 | 1 | 48 | 1 |
| Frost Fang | Ground Patrol (fast) | 2 | 1 | 112 | 2 |
| Ice Shard | Stationary Shooter | 2 | 1 (projectile) | 0 | 2 |
| Hollow Wisp | Air Follow | 1 | 1 | 56 | 2, 5 |
| Brine Crawler | Ground Patrol (fast) | 2 | 1 | 104 | 3 |
| Jelly Drift | Air Patrol (vertical) | 1 | 1 | 40 | 3 |
| Ruin Guardian | Stationary Shooter | 3 | 2 (orb) | 0 | 3 |
| Abyssal Eel | Ground/Water Patrol (long) | 3 | 2 | 88 | 3 |
| Slag Crawler | Ground Patrol + Trail | 3 | 1 (contact) / 1 (trail) | 64 | 4 |
| Ember Wisp | Air Chase | 1 | 1 | 96 | 4 |
| Shadow Smith | Ground Patrol + Attack | 4 | 2 | 72 | 4 |
| Spire Sentry | Ground Patrol + Ranged | 3 | 2 (javelin) | 80 | 5 |
| Shadow Stalker | Stealth + Lunge | 2 | 2 | 128 (lunge) | 5 |

---

## Detailed Enemy Profiles

---

### Shadow Hare

**Visual Description:** A small rabbit-like creature consumed by shadow. Its body is a dark purple-black silhouette with two glowing red eyes and faint wisps of shadow trailing from its ears and feet. It looks like a normal rabbit that has been dipped in liquid darkness — the outline is recognizably animal, but all detail has been replaced by void. Occasionally, a flicker of the original brown fur shows through the shadow coating.

**Behavior Pattern:** Patrol — hops left and right on a set platform, turning at edges. Does not chase the player. Speeds up slightly (from 80 to 96) when the player is within 3 tiles but does not leave its patrol platform.

| Stat | Value |
|---|---|
| HP | 1 |
| Damage Dealt | 1 (contact) |
| Movement Speed | 80 (patrol) / 96 (alerted) |
| Aggression Trigger | Player within 3 tiles — speeds up but stays on platform |

**Death Animation:** The shadow coating bursts off the hare in a puff of dark particles, briefly revealing the normal rabbit underneath (brown, startled expression) before it dissolves into light motes and vanishes. This reinforces that the creatures are corrupted, not inherently evil.

**Drop/Reward:** 3 Flame Coins

**Appears In:** World 1 — Scenes 1-1, 1-2

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Shadow | `#120820` | Body shadow |
| Color 2 | Dark Purple | `#3D1A5E` | Body, ears |
| Color 3 | Ember Red | `#E03030` | Eyes, trail wisps |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a small shadow-corrupted rabbit. Dark purple-black silhouette body with glowing red eyes and shadow wisps trailing from long ears and feet. Recognizable rabbit shape but filled with void darkness. Sprite rows: idle hop (2 frames), patrol hop left (4 frames), patrol hop right (4 frames), alerted faster hop (2 frames), death burst — shadow explodes off revealing brown rabbit briefly before dissolving into light motes (4 frames). GBC style, 4-color palette: transparent, deep shadow #120820, dark purple #3D1A5E, ember red #E03030. Clean pixel art, no anti-aliasing, indexed color.

---

### Gloom Bat

**Visual Description:** A bat-shaped shadow creature larger than a real bat — about the size of Solen's head. Its wings are tattered sheets of shadow that don't quite connect to its body, trailing darkness as it flies. It has a round body, oversized pointed ears, and two beady yellow eyes. Its mouth is a constant open screech showing a row of tiny white fangs. When it flaps, shadow particles shed from the wing tips.

**Behavior Pattern:** Air Patrol — flies in a horizontal sine-wave pattern, oscillating up and down ~2 tiles while moving left to right and back. Turns at set boundaries. In World 2 and World 5, the Gloom Bat has an upgraded behavior: when the player is within 4 tiles vertically, it dive-bombs at a 45-degree angle, then returns to patrol altitude.

| Stat | Value |
|---|---|
| HP | 1 |
| Damage Dealt | 1 (contact) |
| Movement Speed | 72 (patrol) / 128 (dive-bomb) |
| Aggression Trigger | World 1: none (pure patrol). World 2/5: Player within 4 tiles vertically triggers dive-bomb. |

**Death Animation:** Wings fold in, body spins, shadow dissolves upward like smoke. Small flash of yellow light where it was.

**Drop/Reward:** 2 Flame Coins

**Appears In:** World 1 — Scenes 1-1, 1-3. World 2 — Scene 2-3. World 5 — Scene 5-1.

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Shadow | `#120820` | Body shadow, wing interior |
| Color 2 | Midnight Purple | `#2E1248` | Body, ears, wing frames |
| Color 3 | Sickly Yellow | `#D4C840` | Eyes, fang highlights |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a shadow bat creature. Round body, oversized pointed ears, tattered shadow wings that trail darkness, beady yellow eyes, open screeching mouth with tiny white fangs. Sprite rows: flying patrol with flapping wings (4 frames sine-wave), dive-bomb angled attack (2 frames), death spin dissolving upward as smoke (3 frames). GBC style, 4-color palette: transparent, deep shadow #120820, midnight purple #2E1248, sickly yellow #D4C840. Clean pixel art, no anti-aliasing, indexed color.

---

### Sporecap

**Visual Description:** A corrupted mushroom the size of a small stool. Its cap is bulbous and dark purple with faintly glowing teal spots (remnants of the healthy bioluminescence). Its stem is thick and pale, rooted into the ground. Two small dark eyes peer out from under the cap. Periodically, the cap inflates slightly and releases a cloud of greenish spores upward in a small arc.

**Behavior Pattern:** Stationary Shooter — rooted in place, cannot move. Fires a spore projectile every 3 seconds in an upward arc that falls ~3 tiles away. Spore projectile moves at speed 80 and follows a parabolic arc. The Sporecap always faces the player's direction (flips sprite) but the arc is fixed — it always shoots the same distance.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 1 (spore projectile contact) |
| Movement Speed | 0 (stationary) |
| Aggression Trigger | Always active — fires spores on a timer regardless of player position |

**Death Animation:** Cap deflates with a wheeze, the whole mushroom tilts to one side, and collapses into a pile of spores that dissipate.

**Drop/Reward:** 2 Flame Coins + chance of Healing Tincture ingredient (visual-only flavor; mechanically just coins)

**Appears In:** World 1 — Scene 1-2

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Purple | `#2D1040` | Cap shadow, eyes |
| Color 2 | Pale Stem | `#C8B898` | Stem, cap underside |
| Color 3 | Toxic Teal | `#40C8A0` | Cap spots, spore glow |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a corrupted mushroom creature. Bulbous dark purple cap with faintly glowing teal spots, thick pale stem rooted in ground, two small dark eyes under the cap. Sprite rows: idle breathing (2 frames cap pulsing), spore launch — cap inflates and releases green spore cloud upward (3 frames), death — cap deflates and mushroom collapses to one side dissolving (3 frames). Spore projectile: separate 8x8 sprite of a glowing green spore puff. GBC style, 4-color palette: transparent, dark purple #2D1040, pale stem #C8B898, toxic teal #40C8A0. Clean pixel art, no anti-aliasing, indexed color.

---

### Thorn Creeper

**Visual Description:** A vine-like creature that clings to walls. Its body is a thick, dark green tendril with sharp thorns protruding at regular intervals. At its center is a single large red eye. It moves along wall surfaces, leaving a faint trail of sap. Periodically, it extends a thorny tendril outward ~2 tiles from the wall in a quick whip motion.

**Behavior Pattern:** Wall Patrol — clings to wall surfaces and moves vertically up and down. Pauses every 2 seconds to extend a thorny tendril horizontally outward (2-tile reach) for 0.5 seconds before retracting. The tendril has a 0.3-second windup (the eye glows brighter) as a telegraph.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 1 (contact or tendril) |
| Movement Speed | 48 (wall patrol) |
| Aggression Trigger | Always active — patrols and whips on timer regardless of player |

**Death Animation:** The vine curls in on itself like a dying plant, the eye closes, and it drops off the wall, shrinking as it falls.

**Drop/Reward:** 3 Flame Coins

**Appears In:** World 1 — Scene 1-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Vine Green | `#1A3012` | Body shadow, thorns |
| Color 2 | Sickly Green | `#5E8838` | Body, sap |
| Color 3 | Thorn Red | `#C83030` | Eye, thorn tips, tendril whip glow |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a vine creature clinging to a wall. Thick dark green tendril body with sharp thorns protruding, single large red eye at center. Sprite rows: wall patrol climbing up (4 frames), wall patrol climbing down (4 frames), tendril whip extending outward — eye glows bright then thorny arm extends horizontally (3 frames), death — vine curls inward, eye closes, drops off wall (3 frames). GBC style, 4-color palette: transparent, dark vine green #1A3012, sickly green #5E8838, thorn red #C83030. Clean pixel art, no anti-aliasing, indexed color.

---

### Frost Fang

**Visual Description:** A wolf-like shadow creature, sleeker and faster than the Shadow Hare. Its body is a dark blue-gray silhouette with ice crystals forming along its spine and tail. Its eyes glow icy blue. Frost breath visible as small white particles near its muzzle. Its legs are long and its gait is a loping run rather than a hop. Shadow wisps trail from its body but are tinged with blue rather than purple.

**Behavior Pattern:** Ground Patrol (fast) — runs left and right on a platform at high speed, turning at edges. When the player is within 5 tiles, it breaks into a sprint (speed increases from 112 to 144) and lunges forward ~2 tiles. After a lunge, it pauses for 1 second before resuming patrol. The lunge is its most dangerous move because of the speed and distance.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 1 (contact or lunge) |
| Movement Speed | 112 (patrol) / 144 (sprint/lunge) |
| Aggression Trigger | Player within 5 tiles — sprints and lunges |

**Death Animation:** Ice crystals shatter off the body first, then the shadow coating explodes off revealing a gray wolf silhouette that dissolves into blue-white motes.

**Drop/Reward:** 4 Flame Coins

**Appears In:** World 2 — Scenes 2-1, 2-2, 2-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Blue-Gray | `#1A2838` | Body shadow |
| Color 2 | Frost Gray | `#8898A8` | Body, legs |
| Color 3 | Ice Blue | `#78D8F0` | Eyes, spine crystals, frost breath |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a shadow-corrupted wolf creature. Sleek dark blue-gray silhouette body with ice crystals along spine and tail, glowing icy blue eyes, frost breath particles near muzzle, shadow wisps with blue tinge trailing from body. Long-legged loping gait. Sprite rows: patrol run left (4 frames), patrol run right (4 frames), sprint lunge forward (3 frames — windup, lunge, recover), pause after lunge (1 frame), death — ice crystals shatter then shadow bursts off revealing gray wolf dissolving into blue-white motes (4 frames). GBC style, 4-color palette: transparent, deep blue-gray #1A2838, frost gray #8898A8, ice blue #78D8F0. Clean pixel art, no anti-aliasing, indexed color.

---

### Ice Shard

**Visual Description:** A cluster of sharp ice crystals growing from a surface (usually a ledge or ceiling). At the center of the cluster is a small dark core — the corrupted fragment that gives it life. The crystals glow faintly blue-white. Periodically, one crystal detaches and fires as a projectile at a downward or horizontal angle.

**Behavior Pattern:** Stationary Shooter — cannot move. Fires an ice shard projectile every 2.5 seconds in the direction of the player. Projectile travels in a straight line at speed 96. The cluster glows brighter for 0.5 seconds before firing (telegraph). Maximum range: 8 tiles.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 1 (ice shard projectile) |
| Movement Speed | 0 (stationary) |
| Aggression Trigger | Always active — fires toward player position on timer |

**Death Animation:** All crystals crack simultaneously, the dark core pulses once, then the entire cluster shatters and falls as harmless fragments.

**Drop/Reward:** 3 Flame Coins

**Appears In:** World 2 — Scenes 2-1, 2-2, 2-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Ice | `#183848` | Crystal shadow, dark core |
| Color 2 | Ice Body | `#88C0D8` | Crystal body |
| Color 3 | White Glow | `#E0F0FF` | Crystal tips, glow, projectile |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a cluster of sharp ice crystals growing from a surface. Multiple pointed ice shards radiating outward from a small dark corrupted core at the center. Crystals glow faintly blue-white. Sprite rows: idle pulsing glow (2 frames), charging to fire — glow intensifies (2 frames), firing — one crystal detaches and launches (2 frames), death — all crystals crack and shatter falling as fragments (3 frames). Projectile: separate 8x8 sprite of a single ice shard, pointed, glowing. GBC style, 4-color palette: transparent, dark ice #183848, ice body #88C0D8, white glow #E0F0FF. Clean pixel art, no anti-aliasing, indexed color.

---

### Hollow Wisp

**Visual Description:** A small, translucent orb of purple-white light with a trailing tail of shadow particles. It resembles a will-o'-the-wisp or ghost light. The orb pulses rhythmically, brightening and dimming. No distinct features — no eyes, no face — just a ball of corrupt light. When close to the player, the orb's color shifts from white-purple to angry red-purple.

**Behavior Pattern:** Air Follow — drifts slowly toward the player's position at all times. Ignores walls and platforms (passes through them). Cannot be blocked or redirected. The player must either destroy it or outrun it. When within 2 tiles of the player, its speed increases from 56 to 80.

| Stat | Value |
|---|---|
| HP | 1 |
| Damage Dealt | 1 (contact) |
| Movement Speed | 56 (following) / 80 (close pursuit) |
| Aggression Trigger | Always follows player. Speed increase within 2 tiles. |

**Death Animation:** The orb flickers rapidly, then pops like a soap bubble — a brief flash of white light and a ring of dissipating particles.

**Drop/Reward:** 2 Flame Coins

**Appears In:** World 2 — Scene 2-2. World 5 — Scenes 5-1, 5-2, 5-3.

**Sprite Size:** 8×16 px (small)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Violet | `#2A0845` | Shadow trail, outer glow edge |
| Color 2 | Wisp Purple | `#9848C8` | Orb body |
| Color 3 | Ghost White | `#E8D8F8` | Orb center, pulse glow |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 8x16 pixel small enemy sprite of a floating wisp — a translucent orb of purple-white light with a trailing tail of shadow particles. No face or features, just a pulsing ball of corrupt light. Sprite rows: floating idle pulse — orb brightens and dims (4 frames), following player — orb drifts with trail (4 frames), close pursuit — orb turns red-purple and speeds up (2 frames), death pop — flickers rapidly then bursts like a bubble with white flash (3 frames). GBC style, 4-color palette: transparent, deep violet #2A0845, wisp purple #9848C8, ghost white #E8D8F8. Clean pixel art, no anti-aliasing, indexed color.

---

### Brine Crawler

**Visual Description:** A crab-like creature the size of a dog, with a flat, armored carapace in dark teal and six skittering legs. Its eyes are on stalks and glow green. Shadow corruption manifests as purple-black barnacles growing on its shell. Its pincers are oversized relative to its body, snapping open and shut as it patrols. When on dry land, it's fast and aggressive. When in water, it's even faster.

**Behavior Pattern:** Ground Patrol (fast) — scuttles left and right on ground surfaces at high speed. Turns at edges. When the player is within 4 tiles, it charges directly at them. Unlike the Frost Fang, the Brine Crawler does not pause after its charge — it keeps going until it hits an edge, then turns and charges again. In water sections, its speed increases by 50%.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 1 (contact/pincer) |
| Movement Speed | 104 (land patrol) / 156 (water) / 128 (land charge) |
| Aggression Trigger | Player within 4 tiles — charges directly at player |

**Death Animation:** Flips onto its back, legs twitching, then the shadow barnacles pop off and the shell cracks, dissolving into teal-green particles.

**Drop/Reward:** 4 Flame Coins

**Appears In:** World 3 — Scenes 3-1, 3-2, 3-4

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Teal | `#0C2830` | Shell shadow, legs |
| Color 2 | Brine Shell | `#488880` | Carapace, pincers |
| Color 3 | Stalk Green | `#60D858` | Eye stalks, eye glow, barnacle highlights |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a shadow-corrupted crab creature. Flat dark teal armored carapace with purple-black barnacles growing on shell, six skittering legs, oversized snapping pincers, green glowing eyes on stalks. Sprite rows: patrol scuttle left (4 frames), patrol scuttle right (4 frames), charge attack (3 frames — pincers forward), death — flips on back, legs twitch, barnacles pop off, shell cracks dissolving (4 frames). GBC style, 4-color palette: transparent, deep teal #0C2830, brine shell #488880, stalk green #60D858. Clean pixel art, no anti-aliasing, indexed color.

---

### Jelly Drift

**Visual Description:** A jellyfish-like creature the size of a cantaloupe, with a translucent dome-shaped bell and trailing tentacles. The bell is pale blue-teal and pulses with bioluminescent light. The tentacles are thin, wispy, and glow faintly. Shadow corruption is subtle — dark purple veins visible inside the bell. It drifts slowly up and down, tentacles trailing below.

**Behavior Pattern:** Air Patrol (vertical) — drifts up and down in a slow, rhythmic pattern (2-tile range). Does not chase the player. Does not change direction based on player position. Pure obstacle — the player must time their movement to pass when the Jelly Drift is at the top or bottom of its cycle.

| Stat | Value |
|---|---|
| HP | 1 |
| Damage Dealt | 1 (tentacle contact) |
| Movement Speed | 40 (vertical drift) |
| Aggression Trigger | None — pure patrol obstacle |

**Death Animation:** Bell deflates with a soft squish, tentacles curl up, the whole creature shrinks and pops into a small splash of bioluminescent particles.

**Drop/Reward:** 2 Flame Coins

**Appears In:** World 3 — Scenes 3-1, 3-2, 3-4

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Water | `#0C2040` | Tentacle shadow, bell interior veins |
| Color 2 | Pale Teal | `#68A8B8` | Bell body, tentacles |
| Color 3 | Bioluminescent Glow | `#A0F0D8` | Bell highlights, pulse glow, tentacle tips |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a bioluminescent shadow-corrupted jellyfish. Translucent dome-shaped bell in pale blue-teal with dark purple veins inside, trailing thin wispy glowing tentacles below. Sprite rows: floating drift up (4 frames — bell pulses, tentacles trail), floating drift down (4 frames), death — bell deflates, tentacles curl, shrinks and pops into bioluminescent splash (3 frames). GBC style, 4-color palette: transparent, deep water #0C2040, pale teal #68A8B8, bioluminescent glow #A0F0D8. Clean pixel art, no anti-aliasing, indexed color.

---

### Ruin Guardian

**Visual Description:** A stone construct built by the First Keepers — a squat, humanoid torso (no legs) mounted on a stone pedestal. Its body is white-gray stone with teal First Keeper runes carved into its chest and arms. Its head is a featureless dome with a single glowing teal eye in the center. Its arms end in open palms from which it fires slow-moving energy orbs. Shadow corruption has cracked its stone and caused dark purple growths to sprout from the cracks.

**Behavior Pattern:** Stationary Shooter — cannot move. Fires a slow-moving teal energy orb every 3 seconds toward the player's position at the moment of firing. The orb travels in a straight line at speed 64 and passes through platforms but not walls. The Guardian's eye tracks the player before firing (0.5-second telegraph — the eye glows brighter). Maximum range: 10 tiles.

| Stat | Value |
|---|---|
| HP | 3 |
| Damage Dealt | 2 (energy orb) |
| Movement Speed | 0 (stationary) |
| Aggression Trigger | Always active — tracks and fires at player on timer |

**Death Animation:** Runes flash rapidly, the eye flickers and goes dark, cracks spread across the body, and the construct crumbles into a pile of stone blocks. A faint teal light rises from the rubble and dissipates (the Guardian's spirit released).

**Drop/Reward:** 5 Flame Coins

**Appears In:** World 3 — Scene 3-2

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Stone | `#303838` | Shadow, cracks, corruption growths |
| Color 2 | White Stone | `#C0C8C8` | Body, arms, pedestal |
| Color 3 | Rune Teal | `#40C8C8` | Eye, runes, energy orb glow |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of an ancient stone construct guardian. Squat humanoid torso with no legs, mounted on a stone pedestal. White-gray stone body with teal glowing runes carved into chest and arms. Featureless dome head with a single large teal glowing eye. Arms with open palms. Cracks in stone with dark purple corruption growths. Sprite rows: idle — eye scanning (2 frames), charging to fire — eye glows bright, palm opens (2 frames), firing energy orb from palm (2 frames), death — runes flash, eye dies, body crumbles into stone blocks with teal light rising (4 frames). Energy orb: separate 8x8 sprite, teal glowing sphere. GBC style, 4-color palette: transparent, dark stone #303838, white stone #C0C8C8, rune teal #40C8C8. Clean pixel art, no anti-aliasing, indexed color.

---

### Abyssal Eel

**Visual Description:** A long, serpentine creature (~3 tiles long) that undulates through water and across underwater floors. Its body is dark blue-black with a row of faint bioluminescent blue spots along its sides. Its head is angular with a wide mouth full of needle teeth and two small, cold white eyes. Shadow corruption is evident in purple-black patches along its body and a purple glow from within its mouth.

**Behavior Pattern:** Water Patrol — swims in a set pattern through a section of the underwater area. Moves in long, swooping arcs. When the player enters its patrol zone, it redirects toward them, increasing speed. It cannot leave its designated zone (limited by invisible boundaries). Its long body means the player must dodge not just the head but the trailing body segments.

| Stat | Value |
|---|---|
| HP | 3 |
| Damage Dealt | 2 (contact — any body segment) |
| Movement Speed | 88 (patrol) / 112 (chasing) |
| Aggression Trigger | Player enters patrol zone (~6 tile radius) |

**Death Animation:** Body goes rigid, then segments disconnect one by one from tail to head, each dissolving into dark water particles. The head is last — its mouth opens in a silent shriek before dissolving.

**Drop/Reward:** 6 Flame Coins

**Appears In:** World 3 — Scene 3-4

**Sprite Size:** 16×16 px per segment (head + 2 body segments = 3 actors)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Abyssal Blue-Black | `#08182C` | Body shadow, mouth interior |
| Color 2 | Deep Sea Blue | `#284868` | Body, head |
| Color 3 | Bio Blue | `#58A8D0` | Bioluminescent spots, eyes, teeth highlights |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite segments of a long serpentine eel creature. Three segments: HEAD — angular head with wide mouth full of needle teeth, two small cold white eyes, purple glow from mouth; BODY — undulating segment with row of faint bioluminescent blue spots along sides, purple-black corruption patches; TAIL — tapered end with fin. Each segment is a separate 16x16 sprite that chains together. Sprite rows per segment: swimming undulation (4 frames), chasing faster undulation (4 frames), death — body goes rigid then dissolves segment by segment into dark particles (3 frames per segment). GBC style, 4-color palette: transparent, abyssal blue-black #08182C, deep sea blue #284868, bio blue #58A8D0. Clean pixel art, no anti-aliasing, indexed color.

---

### Slag Crawler

**Visual Description:** A hunched, turtle-like creature made of cooled volcanic rock and molten slag. Its shell is rough dark stone with cracks that glow orange-red from the magma within. Its legs are stubby and its body leaves a trail of small embers and molten drips as it moves. Two dim orange eyes peer from beneath the shell. Shadow corruption is visible as purple-black veins running through the orange glow in the cracks.

**Behavior Pattern:** Ground Patrol + Trail — crawls slowly left and right on a platform. Behind it, it leaves a fire trail (glowing ground tiles) that persists for 3 seconds and deals 1 HP on contact. The trail effectively makes the Slag Crawler's patrol path a hazard zone. When the player is within 3 tiles, the Crawler retracts into its shell and becomes invulnerable for 2 seconds (cannot be damaged), then emerges and resumes patrol.

| Stat | Value |
|---|---|
| HP | 3 |
| Damage Dealt | 1 (contact) / 1 (fire trail) |
| Movement Speed | 64 (patrol) |
| Aggression Trigger | Player within 3 tiles — retracts into shell (defensive, not aggressive) |

**Death Animation:** Shell cracks open, magma spills out, the body sinks into the puddle of cooling lava, and hardens into a small obsidian lump that then crumbles.

**Drop/Reward:** 5 Flame Coins

**Appears In:** World 4 — Scenes 4-1, 4-2

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Basalt | `#1C1410` | Shell shadow, legs |
| Color 2 | Cooled Rock | `#685040` | Shell body, body |
| Color 3 | Magma Orange | `#F08020` | Crack glow, eyes, fire trail, ember drips |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a volcanic rock turtle creature. Hunched body with rough dark stone shell, cracks in shell glowing orange-red with magma inside, stubby legs, two dim orange eyes under shell edge. Purple-black corruption veins through the glow. Leaves trail of embers. Sprite rows: patrol crawl left (4 frames with ember drip trail), patrol crawl right (4 frames), shell retract — pulls into shell becoming invulnerable smooth rock dome (2 frames), death — shell cracks, magma spills, body sinks and hardens into obsidian lump that crumbles (4 frames). Fire trail: separate 8x8 tile sprite of glowing orange ground embers. GBC style, 4-color palette: transparent, dark basalt #1C1410, cooled rock #685040, magma orange #F08020. Clean pixel art, no anti-aliasing, indexed color.

---

### Ember Wisp

**Visual Description:** A small, flickering ball of orange-red fire corrupted by shadow. Resembles the Hollow Wisp but in fire colors — an orb of flame with a dark purple core visible through the flickering. Tiny sparks shed from it as it moves. It's erratic, jittering slightly as it flies.

**Behavior Pattern:** Air Chase — more aggressive than the Hollow Wisp. Actively pursues the player at higher speed. Unlike the Hollow Wisp, the Ember Wisp does NOT pass through walls — it pathfinds around obstacles, making it more predictable but harder to shake. It pauses for 0.5 seconds when it hits a wall before redirecting.

| Stat | Value |
|---|---|
| HP | 1 |
| Damage Dealt | 1 (contact) |
| Movement Speed | 96 (chasing) |
| Aggression Trigger | Always chasing player — no passive state |

**Death Animation:** The flame sputters, the purple core is briefly visible, then the whole wisp explodes in a small burst of orange sparks.

**Drop/Reward:** 3 Flame Coins

**Appears In:** World 4 — Scenes 4-1, 4-2, 4-3

**Sprite Size:** 8×16 px (small)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Core | `#301020` | Core shadow, purple corruption |
| Color 2 | Flame Orange | `#E06828` | Flame body |
| Color 3 | Bright Yellow | `#F8D848` | Flame tip, sparks |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 8x16 pixel small enemy sprite of a corrupted fire wisp. Flickering ball of orange-red flame with a dark purple core visible through the fire, tiny sparks shedding from it, erratic jittering motion. Sprite rows: chasing player with jitter (4 frames flickering), hitting wall and pausing (2 frames), death — flame sputters, core visible, explodes in orange spark burst (3 frames). GBC style, 4-color palette: transparent, dark core #301020, flame orange #E06828, bright yellow #F8D848. Clean pixel art, no anti-aliasing, indexed color.

---

### Shadow Smith

**Visual Description:** A humanoid shadow figure the size of a large man, wearing the remnants of a miner's outfit — a tattered leather apron, a dented helmet, and heavy boots. Its body is dark purple-black shadow with faint details of the original person visible as lighter patches — a face frozen in a silent scream, hands gripping a massive shadow-forged hammer. Purple-orange embers drift from its body. It moves with a shuffling, mechanical gait, as if the shadow is puppeting a body it doesn't quite fit.

**Behavior Pattern:** Ground Patrol + Attack — patrols a set area with a slow, shuffling walk. When the player is within 3 tiles, it stops, raises its hammer (1-second telegraph — hammer glows), and slams it down in a 2-tile arc in front of it. The slam deals high damage and creates a small shockwave that travels 1 tile along the ground. After slamming, it pauses for 1.5 seconds (recovery), then resumes patrol.

| Stat | Value |
|---|---|
| HP | 4 |
| Damage Dealt | 2 (hammer slam) / 1 (shockwave) |
| Movement Speed | 72 (patrol) |
| Aggression Trigger | Player within 3 tiles — stops and attacks |

**Death Animation:** The hammer dissolves first, then the shadow body collapses like a puppet with its strings cut. The miner's helmet clinks to the ground and remains for a moment before fading.

**Drop/Reward:** 8 Flame Coins

**Appears In:** World 4 — Scenes 4-2, 4-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Shadow | `#140C20` | Body shadow, hammer |
| Color 2 | Miner Gray | `#707070` | Apron remnants, helmet, boots |
| Color 3 | Ember Glow | `#E86838` | Body embers, hammer glow, shockwave |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a shadow-possessed miner. Humanoid dark purple-black shadow body with remnants of a miner's outfit — tattered leather apron, dented helmet, heavy boots. Faint original face visible as lighter patch frozen in silent scream. Grips a massive shadow-forged hammer. Purple-orange embers drift from body. Shuffling mechanical gait. Sprite rows: patrol shuffle left (4 frames), patrol shuffle right (4 frames), attack — stops, raises hammer with glow (2 frames), slams hammer down with shockwave (2 frames), recovery pause (1 frame), death — hammer dissolves, body collapses like puppet, helmet clinks to ground (4 frames). GBC style, 4-color palette: transparent, deep shadow #140C20, miner gray #707070, ember glow #E86838. Clean pixel art, no anti-aliasing, indexed color.

---

### Spire Sentry

**Visual Description:** An armored humanoid figure in corrupted Lamplighter Order ceremonial armor. The armor is dark purple-black with tarnished silver trim. A crested helmet with a visor covers the face — only faint violet light is visible through the eye slits. It carries a javelin in one hand and a small round shield in the other. The cape is torn and trails shadow wisps. It stands at rigid attention when idle, like a guard at a post.

**Behavior Pattern:** Ground Patrol + Ranged — patrols a set platform at moderate speed. When the player is within 6 tiles, it stops, braces, and throws a shadow javelin. The javelin is a fast projectile (speed 128) that travels in a straight horizontal line. After throwing, the Sentry draws a new javelin from its back (1.5-second cooldown). The shield provides a defensive mechanic: the Sentry blocks attacks from the front. The player must attack from behind or above.

| Stat | Value |
|---|---|
| HP | 3 |
| Damage Dealt | 2 (javelin projectile) / 1 (contact) |
| Movement Speed | 80 (patrol) |
| Aggression Trigger | Player within 6 tiles — stops and throws javelin |

**Death Animation:** The javelin and shield clatter to the ground. The armor buckles inward as the shadow inside dissipates — the helmet falls off revealing nothing inside. The empty armor crumples to the ground.

**Drop/Reward:** 6 Flame Coins

**Appears In:** World 5 — Scenes 5-1, 5-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Corrupted Armor | `#1A1028` | Armor shadow, cape |
| Color 2 | Tarnished Silver | `#888898` | Armor body, helmet, shield |
| Color 3 | Violet Glow | `#A060D8` | Eye slit glow, javelin energy, trim highlights |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a corrupted armored guard. Dark purple-black ceremonial armor with tarnished silver trim, crested helmet with visor showing violet light through eye slits, torn shadow-trailing cape. Carries a javelin in one hand and a small round shield in other. Rigid military posture. Sprite rows: idle at attention (2 frames), patrol march left (4 frames), patrol march right (4 frames), throw javelin — braces and hurls (3 frames), death — armor buckles inward, helmet falls revealing emptiness, armor crumples (4 frames). Javelin projectile: separate 8x16 sprite, glowing violet energy spear. GBC style, 4-color palette: transparent, corrupted armor #1A1028, tarnished silver #888898, violet glow #A060D8. Clean pixel art, no anti-aliasing, indexed color.

---

### Shadow Stalker

**Visual Description:** A creature that is nearly invisible — a humanoid shape made entirely of shadow, visible only as a faint distortion in the air, like heat haze. When within Solen's lantern light radius, it becomes partially visible: a crouching, long-limbed figure with elongated arms and legs, a featureless smooth head, and two burning violet eyes. It moves on all fours like a predator.

**Behavior Pattern:** Stealth + Lunge — invisible and stationary until the player is within 3 tiles OR within the lantern light radius. Once detected (visible to the player), it crouches for 0.5 seconds (telegraph — eyes glow brighter), then lunges at the player at high speed (128) in a straight line. If it misses, it skids to a stop and becomes invisible again after 2 seconds, then repositions randomly.

| Stat | Value |
|---|---|
| HP | 2 |
| Damage Dealt | 2 (lunge contact) |
| Movement Speed | 0 (stealth) / 128 (lunge) |
| Aggression Trigger | Player within 3 tiles or lantern light radius — reveals and lunges |

**Death Animation:** The shadow figure distorts, stretches upward as if being pulled from above, thins into a wisp, and vanishes with a faint pop of violet light.

**Drop/Reward:** 5 Flame Coins

**Appears In:** World 5 — Scenes 5-2, 5-3

**Sprite Size:** 16×16 px

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Near-Invisible | `#0C0818` | Body (barely visible against dark BG) |
| Color 2 | Shadow Form | `#2C1848` | Body when revealed, limbs |
| Color 3 | Violet Eyes | `#C868F8` | Eyes, lunge streak |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel enemy sprite of a shadow stalker creature. Crouching humanoid figure made of shadow, long-limbed with elongated arms and legs, featureless smooth head, two burning violet eyes. Moves on all fours. Nearly invisible in darkness, partially visible in light. Sprite rows: stealth idle — nearly invisible with faint distortion (2 frames), revealed in light — crouching predator with glowing eyes (2 frames), lunge windup — eyes brighten, body tenses (2 frames), lunge attack — high-speed horizontal dash (2 frames), miss and skid — slides to stop (2 frames), death — stretches upward, thins to wisp, pops with violet flash (3 frames). GBC style, 4-color palette: transparent, near-invisible #0C0818, shadow form #2C1848, violet eyes #C868F8. Clean pixel art, no anti-aliasing, indexed color.
