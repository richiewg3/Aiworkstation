# 08 — Tilesets & Backgrounds

---

## Tileset Overview

All tilesets are designed as grids of 8×8 pixel tiles, organized into 128×128 px sheets (16×16 tile grid). Each tileset uses a single 4-color GBC palette. Multiple tilesets can be combined in a scene (GB Studio supports multiple tileset references per background).

| Tileset Name | Used In | Primary Purpose |
|---|---|---|
| `ts_cinderhearth` | Prologue (0-1) | Village, cobblestone, houses, lanterns |
| `ts_cinderhearth_dark` | Prologue (0-2) | Corrupted village variant |
| `ts_verdant_hollow` | World 1 (1-1, 1-3, 1-4, 1-B) | Forest, trees, moss, mushrooms |
| `ts_mushroom_grotto` | World 1 (1-2) | Underground cavern, bioluminescent mushrooms |
| `ts_thornveil` | World 1 (1-3) | Thorns, thick vines, vertical shaft |
| `ts_frostfang_peaks` | World 2 (all scenes) | Mountain rock, snow, ice, pine trees |
| `ts_rimehaven_village` | World 2 (2-2) | Frozen village buildings |
| `ts_ice_shelf` | World 2 (2-3) | Exposed ledge, cloud platforms |
| `ts_sunken_brine` | World 3 (3-1, 3-4) | Cavern stone, water, bioluminescent algae |
| `ts_first_keeper_ruins` | World 3 (3-2, 3-3) | Ancient carved stone, runes, glowing panels |
| `ts_research_chamber` | World 3 (3-3) | Desk, journals, devices |
| `ts_keeper_cathedral` | World 3 (3-4, 3-B) | Massive underwater columns, mosaic floor |
| `ts_cinderforge` | World 4 (all scenes) | Volcanic rock, magma, mining equipment |
| `ts_forge_machinery` | World 4 (4-2) | Conveyor belts, gears, chains, anvils |
| `ts_obsidian_core` | World 4 (4-3) | Obsidian formations, First Keeper white stone |
| `ts_spire_ascent` | World 5 (5-1, 5-2) | Floating rock platforms, chains, sky elements |
| `ts_shadow_dome` | World 5 (5-2) | Dark distortion tiles, shadow tendrils |
| `ts_spire_interior` | World 5 (5-3, 5-4, 5-5) | Marble halls, stained glass, banners |
| `ts_hearthstone_chamber` | Worlds 1–5 boss areas | Hearthstone crystal housing, pedestal |
| `ts_boss_arena` | All boss scenes | Arena boundaries, elevated platforms |
| `ts_chamber_of_origin` | Secret area (6-1) | Pristine white stone, First Keeper murals |

---

## Detailed Tileset Profiles

---

### ts_cinderhearth

**Used In:** Scene 0-1 (Cinderhearth Village — Evening Round)

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Cobblestone road (3 variants), dirt path, grass edge |
| Wall | Wooden house wall, stone wall, window (lit), door |
| Platform | Wooden fence top, well rim, roof edge |
| Hazard | — (none in tutorial) |
| Decoration | Lamp post, flower box, barrel, crate, signpost, well bucket |
| Animated | Lantern flame flicker (2-frame cycle), window light shimmer (2-frame) |
| Foreground | Lamp post with light halo |
| Background | House interior glow (behind windows) |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Dusk Sky | `#483860` | Background sky, shadows |
| Color 1 | Warm Stone | `#887058` | Cobblestone, house walls, wood |
| Color 2 | Cream | `#D8C8A0` | House fronts, path highlights, fences |
| Color 3 | Lantern Gold | `#F8D878` | Lantern glow, window light, flower accents |

**Visual Description:** A cozy village at dusk. Warm tones dominate — golden lantern light spills across cobblestone streets. Houses have simple wooden construction with stone foundations and shuttered windows that glow from within. The palette shifts from dusky purple in the shadows to warm gold in the light pools, creating a feeling of safety and warmth that will be violently disrupted in the next scene.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Cozy village at dusk. Includes: cobblestone road tiles (3 variants with different stone patterns), dirt path, grass edges, wooden house walls, stone walls, lit windows with warm glow, wooden doors, fence tops, well rim and bucket, roof edge tiles, lamp post pieces, flower boxes, barrels, crates, signpost. Animated frames: lantern flame flicker (2 frames), window shimmer (2 frames). GBC style, 4-color palette: dusk sky #483860, warm stone #887058, cream #D8C8A0, lantern gold #F8D878. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** The background is a 160×144 px image showing a dusky orange-pink sky transitioning to deep purple at the top. Silhouettes of rolling hills fill the lower third. On a hill to the left, the Verdant Hearthstone is visible as a faint green glow. Slow-moving cloud wisps cross the sky.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Dusky evening sky — gradient from warm orange-pink at the horizon to deep purple at the top. Silhouettes of gentle rolling hills in dark purple. On a hill to the left, a faint green crystal glow (distant Hearthstone). Thin cloud wisps in peach and lavender crossing the sky. Peaceful, warm, nostalgic mood. GBC style, 4-color palette: deep purple #483860, warm stone #887058, peach cream #D8C8A0, sunset gold #F8D878. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_cinderhearth_dark

**Used In:** Scene 0-2 (Cinderhearth — The Hollow Surge)

**Tile Types Needed:** Same layout as `ts_cinderhearth` but with corrupted palette. Windows are dark or flickering. Lanterns are shattered. Additional tiles: broken glass on ground, shadow tendrils on surfaces, cracked cobblestone.

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Void Dark | `#180828` | Deep shadow, corruption |
| Color 1 | Shadow Purple | `#483058` | Corrupted stone, shadow-stained surfaces |
| Color 2 | Ash Gray | `#908880` | Desaturated house fronts, broken cobblestone |
| Color 3 | Dying Amber | `#C89830` | Flickering remnant light, shattered lantern embers |

**Visual Description:** The same village, transformed. The warm palette has been drained and replaced with cold purples and grays. Lanterns are broken, their glass scattered as tiles on the ground. Shadow tendrils creep along walls and ground. The occasional flicker of dying amber light creates an unsettling contrast with the overwhelming darkness.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Same village layout as a cozy village tileset but corrupted by darkness. Cobblestone cracked and stained purple-black, house walls desaturated and shadow-streaked, windows dark or flickering with dying light, lanterns shattered with glass shards on ground, shadow tendrils creeping along surfaces, broken fences, toppled barrels. GBC style, 4-color palette: void dark #180828, shadow purple #483058, ash gray #908880, dying amber #C89830. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Dark violet sky, no sunset. The Hearthstone on the hill flickers violently — alternating between faint green and dark. A wall of purple-black shadow (the Hollow Tide) is visible approaching from the left, consuming the horizon.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Dark violet sky with no stars. On a hill to the left, a crystal flickers between faint green and darkness. A massive wall of purple-black shadow (Hollow Tide) approaches from the left side, consuming the horizon. The sky above the shadow wall is pure black. Ominous, threatening, apocalyptic mood. GBC style, 4-color palette: void dark #180828, shadow purple #483058, ash gray #908880, dying amber #C89830. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_verdant_hollow

**Used In:** Scenes 1-1, 1-3, 1-4, 1-B

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Mossy earth (3 variants), root-covered ground, fallen leaves |
| Wall | Tree bark wall, stone wall with moss, hollow log |
| Platform | Tree branch (thick), tree branch (thin/crumbling), moss-covered ledge |
| Hazard | Shadow puddle tile, thorn tile |
| Decoration | Bioluminescent mushroom (small), fern, hanging vine, fallen log, tree stump |
| Animated | Mushroom glow pulse (2 frames), firefly sparkle (2 frames), dripping sap (2 frames) |
| Foreground | Overhanging leaf canopy, branch silhouettes |
| Background | Deep forest tree trunks, distant foliage layers |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Deep Forest | `#102818` | Darkest shadows, deep background |
| Color 1 | Bark Brown | `#485030` | Tree trunks, earth, roots, wood |
| Color 2 | Moss Green | `#68A048` | Leaves, moss, platforms, ferns |
| Color 3 | Glow Teal | `#A8E8B8` | Mushroom bioluminescence, fireflies, highlights |

**Visual Description:** A dense, ancient forest with towering trees whose trunks are thick and gnarled. The canopy above filters light into shafts of dim green. The ground is soft moss and fallen leaves. Bioluminescent mushrooms cluster near tree roots, providing pockets of teal-green light. The overall feeling is of a forest that was once vibrant but is now dimming — the colors are muted, the shadows deep, but life persists in the glowing fungi and the occasional firefly.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Dense ancient forest theme. Includes: mossy earth ground (3 variants), root-covered ground, fallen leaves, thick tree bark walls, stone with moss, hollow logs, thick and thin tree branch platforms (thin ones crumbling), shadow puddle hazard tiles (dark purple-tinged), thorn hazard tiles, small bioluminescent mushrooms, ferns, hanging vines, fallen logs, tree stumps. Animated: mushroom glow pulse (2 frames), firefly sparkle (2 frames). GBC style, 4-color palette: deep forest #102818, bark brown #485030, moss green #68A048, glow teal #A8E8B8. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Multiple layers of forest depth. The far background is nearly black with faint vertical tree trunk lines. The mid background shows tree trunks in dark green with occasional mushroom glows. Shafts of pale light angle down from the upper left.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Deep ancient forest interior. Layered tree trunks receding into dark background — nearest trunks in brown-green, distant trunks as dark silhouettes. Faint shafts of pale green light angling down from upper left through the canopy. Small clusters of teal bioluminescent mushrooms glowing at the base of distant trees. Atmospheric, dim, mysterious but not hostile. GBC style, 4-color palette: deep forest #102818, bark brown #485030, moss green #68A048, glow teal #A8E8B8. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_mushroom_grotto

**Used In:** Scene 1-2

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Wet stone floor, shallow water, dry stone |
| Wall | Cavern rock wall, stalagmite, root-covered ceiling |
| Platform | Large mushroom cap (walkable), stone ledge, hanging root (ladder) |
| Hazard | Poison pool (green-tinged water), dripping stalactite |
| Decoration | Small mushroom cluster, glowing algae, water reflection tile, stalagmite column |
| Animated | Mushroom cap glow cycle (2 frames), water ripple (2 frames), drip from stalactite (2 frames) |
| Foreground | Large translucent mushroom cap overlay |
| Background | Deep cavern recesses, distant mushroom groves |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Cavern Dark | `#081018` | Deep shadow, cave recesses |
| Color 1 | Wet Stone | `#384048` | Rock walls, floor, stalagmites |
| Color 2 | Biolume Teal | `#48A088` | Mushroom caps, algae, water |
| Color 3 | Glow Yellow-Green | `#C8F0A0` | Mushroom spots, glow highlights, reflections |

**Visual Description:** An underground cavern lit entirely by bioluminescent life. Giant mushroom caps serve as platforms, their undersides glowing soft teal. Pools of still water reflect the light. The ceiling is low, covered in hanging roots and stalactites. The atmosphere is damp, enclosed, and otherworldly — like being inside a living creature.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Underground bioluminescent mushroom cavern. Includes: wet stone floor, shallow water tiles, dry stone, cavern rock walls, stalagmites, root-covered ceiling, large mushroom cap platform tiles, stone ledges, hanging root ladder tiles, poison pool hazard (green-tinged), dripping stalactite hazard, small mushroom clusters, glowing algae, water reflection tiles. Animated: mushroom glow cycle (2 frames), water ripple (2 frames), stalactite drip (2 frames). GBC style, 4-color palette: cavern dark #081018, wet stone #384048, biolume teal #48A088, glow yellow-green #C8F0A0. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Dark cavern with distant mushroom groves glowing in teal. No sky visible — enclosed underground. Faint moisture particles in the air.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Underground mushroom cavern. Dark rock walls receding into shadow. Distant clusters of large bioluminescent mushrooms glowing teal and yellow-green. Still water pools reflecting the glow. Stalactites hanging from ceiling. No sky — fully enclosed. Damp, ethereal, alive. GBC style, 4-color palette: cavern dark #081018, wet stone #384048, biolume teal #48A088, glow yellow-green #C8F0A0. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_frostfang_peaks

**Used In:** All World 2 scenes

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Snow-covered rock, bare rock, packed snow, ice surface (slippery) |
| Wall | Mountain cliff face, ice wall, frozen waterfall, pine trunk |
| Platform | Rock outcropping, ice ledge (crumble), pine branch with snow |
| Hazard | Icicle (ceiling), thin ice platform, wind gust indicator |
| Decoration | Snow drift, frozen shrub, icicle cluster, frost crystal, pine tree silhouette |
| Animated | Snowflake fall (2 frames), icicle shimmer (2 frames), wind particle (2 frames) |
| Foreground | Blowing snow overlay |
| Background | Distant mountain peaks, cloud layer |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Mountain Dark | `#182838` | Rock shadow, deepest crevices |
| Color 1 | Cold Stone | `#506878` | Rock face, pine trunks, dark ice |
| Color 2 | Snow Blue | `#A0C0D8` | Snow, ice surfaces, frost |
| Color 3 | Bright White | `#E8F0F8` | Snow highlights, icicle tips, frost crystals |

**Visual Description:** A stark, beautiful mountain landscape. The palette is predominantly cool blues and whites, with dark slate rock providing contrast. Snow covers every horizontal surface. Ice catches faint light and glimmers. Pine trees are sparse, their branches heavy with snow. The environment feels vast, exposed, and cold — the opposite of the Verdant Hollow's enclosed warmth.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Mountain ice and snow theme. Includes: snow-covered rock ground, bare rock, packed snow, ice surface tiles (smooth for slippery mechanic), mountain cliff face walls, ice walls, frozen waterfall, pine tree trunk, rock outcropping platforms, crumbling ice ledge, snow-laden pine branch platform, ceiling icicle hazard, thin ice platform hazard, snow drifts, frozen shrubs, icicle clusters, frost crystals. Animated: snowflake fall (2 frames), icicle shimmer (2 frames). GBC style, 4-color palette: mountain dark #182838, cold stone #506878, snow blue #A0C0D8, bright white #E8F0F8. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** A panoramic mountain vista. Multiple mountain peaks recede into the distance, each paler than the last. A low cloud layer sits at mid-height. The sky is pale gray-blue, overcast but bright. Far-off peaks catch faint light.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Mountain panorama. Multiple snow-capped mountain peaks receding into distance, each progressively paler. Low cloud layer at mid-height. Pale gray-blue overcast sky. Faint light catching the highest peaks. Vast, cold, isolating, beautiful. GBC style, 4-color palette: mountain dark #182838, cold stone #506878, snow blue #A0C0D8, bright white #E8F0F8. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_sunken_brine

**Used In:** Scenes 3-1, 3-4

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Wet cavern floor, sand, submerged stone, coral |
| Wall | Damp rock wall, barnacle-covered wall, algae-streaked stone |
| Platform | Rock shelf, coral ledge, chain (ladder) |
| Hazard | Deep water (swim zone), acid drip source, shadow current |
| Decoration | Bioluminescent algae, shell cluster, hanging chain, anchor, seaweed |
| Animated | Algae glow pulse (2 frames), water flow (2 frames), bubble rise (2 frames) |
| Foreground | Water surface ripple overlay, bubble particles |
| Background | Deep cavern, underwater light shafts |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Abyss Blue | `#081020` | Deep water, shadow, cavern depth |
| Color 1 | Brine Stone | `#284050` | Rock, barnacles, chains |
| Color 2 | Sea Teal | `#509088` | Water, algae, coral, seaweed |
| Color 3 | Phosphor Green | `#88E8C0` | Bioluminescence, light shafts, highlights |

**Visual Description:** An underground sea cavern with a pervasive blue-teal palette. The stone is damp and encrusted with marine life. Bioluminescent algae provides the primary light source, casting shimmering green-teal light across wet surfaces. Water is everywhere — pools, streams, and fully submerged sections. The atmosphere is heavy, mysterious, and ancient.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Underground sea cavern theme. Includes: wet cavern floor, sand, submerged stone, coral patches, damp rock walls, barnacle-covered walls, algae-streaked stone, rock shelf platforms, coral ledge, chain ladder tiles, deep water swim zone, acid drip source, shadow current hazard, bioluminescent algae decorations, shell clusters, hanging chains, seaweed. Animated: algae glow pulse (2 frames), water flow (2 frames), bubble rise (2 frames). GBC style, 4-color palette: abyss blue #081020, brine stone #284050, sea teal #509088, phosphor green #88E8C0. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Deep underwater cavern. Shafts of green light penetrate from cracks in the ceiling far above. Schools of small luminescent fish form streaks of light. The depth fades to pure blackness below.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Deep underground sea cavern. Shafts of green-teal light filtering down from cracks in the distant ceiling. Dark rock walls receding into blue-black depth. Small luminescent fish visible as dots of light. Seaweed silhouettes swaying. Fading to pure darkness at the bottom. Eerie, vast, ancient, mysterious. GBC style, 4-color palette: abyss blue #081020, brine stone #284050, sea teal #509088, phosphor green #88E8C0. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_first_keeper_ruins

**Used In:** Scenes 3-2, 3-3

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Carved stone floor, mosaic tile, cracked floor tile |
| Wall | Carved stone wall with rune inscriptions, column segment, archway |
| Platform | Broken walkway, stone pedestal, column top |
| Hazard | Crumbling walkway (collapses) |
| Decoration | Rune panel (interactive — glows near lantern), broken statue, scroll shelf, First Keeper device |
| Animated | Rune glow activation (2 frames), device pulse (2 frames) |
| Foreground | Column shadow, archway curve |
| Background | Deep ruin corridors, distant carved walls |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Ruin Shadow | `#101828` | Deep shadow, water |
| Color 1 | Ancient Stone | `#485868` | Walls, floor, columns |
| Color 2 | Pale Marble | `#98A8B8` | Carved surfaces, statues, pedestals |
| Color 3 | Rune Glow | `#68D8D8` | Rune inscriptions, device glow, interactive panels |

**Visual Description:** Ancient, precise architecture — carved stone with geometric patterns and rune inscriptions that glow teal when illuminated. Columns and archways suggest grand halls now half-submerged. The craftsmanship is clearly superior to anything in modern Lumara, lending a sense of lost greatness. The glowing runes react to Solen's lantern, creating an interactive sense of discovery.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Ancient ruins theme. Includes: carved stone floor tiles, mosaic tiles with geometric patterns, cracked floor, carved stone walls with rune inscriptions, column segments (base, middle, top, capital), archway tiles, broken walkway platforms, stone pedestals, crumbling walkway hazard, rune panels (inactive and active glow variants), broken statue fragments, scroll shelves, First Keeper device components. Animated: rune glow activation (2 frames), device pulse (2 frames). GBC style, 4-color palette: ruin shadow #101828, ancient stone #485868, pale marble #98A8B8, rune glow #68D8D8. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Deep corridors receding into darkness, lined with faintly glowing rune panels. Broken columns cast long shadows. Water reflections shimmer on the distant floor.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Ancient ruins interior. Long corridor receding into darkness. Tall carved columns lining both sides. Faint teal rune inscriptions glowing on distant walls. Broken archway in the middle distance. Water on the floor reflecting the rune glow. Dark, mysterious, reverent, ancient. GBC style, 4-color palette: ruin shadow #101828, ancient stone #485868, pale marble #98A8B8, rune glow #68D8D8. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_cinderforge

**Used In:** All World 4 scenes

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Rough stone, metal grate, scorched earth, cooled magma crust |
| Wall | Volcanic rock wall, metal panel, support beam, pipe |
| Platform | Metal walkway, stone bridge over lava, scaffolding plank |
| Hazard | Magma surface (instant death), steam vent tile, shadow pool |
| Decoration | Abandoned mining cart, pickaxe, helmet, lantern (dead), ore pile, anvil |
| Animated | Magma flow (2 frames), steam vent burst (2 frames), ember float up (2 frames) |
| Foreground | Heat shimmer overlay, ash particles |
| Background | Magma rivers, distant forge structures |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Volcanic Dark | `#180808` | Deepest shadow, obsidian |
| Color 1 | Forge Stone | `#483828` | Rock, metal, pipes, equipment |
| Color 2 | Hot Metal | `#886038` | Metal surfaces, walkways, grates |
| Color 3 | Magma Orange | `#F08828` | Lava, embers, forge glow, fire |

**Visual Description:** A hellish industrial environment. The dominant feature is magma — rivers of it flowing through channels, glowing behind grates, pooling in pits. Metal mining infrastructure — scaffolding, rails, carts — provides the platforming surfaces. The air is thick with ash and heat shimmer. Shadow corruption adds purple-black veins to everything, making the already dangerous environment feel actively hostile.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Volcanic forge and mining theme. Includes: rough stone ground, metal grate floor, scorched earth, cooled magma crust, volcanic rock walls, metal panels, wooden support beams, pipes, metal walkway platforms, stone bridge tiles, scaffolding planks, magma surface hazard (orange glow), steam vent tiles, shadow pool hazard, mining cart, pickaxe, helmet, dead lantern, ore piles, anvil. Animated: magma flow (2 frames), steam vent burst (2 frames), ember particles floating up (2 frames). GBC style, 4-color palette: volcanic dark #180808, forge stone #483828, hot metal #886038, magma orange #F08828. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** A vast volcanic cavern. Rivers of magma glow in the distance. Massive forge structures — chimneys, furnaces, cranes — sit as dark silhouettes against the orange glow. Ash and embers float upward.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Volcanic forge cavern interior. Rivers of bright orange magma flowing in the far distance. Massive forge structure silhouettes — chimneys, furnaces, crane arms — in dark tones against the magma glow. Cavern ceiling high above with stalactites. Embers and ash particles floating upward. Intense, industrial, dangerous. GBC style, 4-color palette: volcanic dark #180808, forge stone #483828, hot metal #886038, magma orange #F08828. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_spire_ascent

**Used In:** Scenes 5-1, 5-2

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Floating rock platform, chain-anchored platform, cloud-edge tile |
| Wall | Chain link (climbable), rock face fragment |
| Platform | Small floating rock, bobbing platform, crumble platform (one-use) |
| Hazard | Shadow wisp hazard tile, platform edge (void) |
| Decoration | Chain segments, floating debris, distant Hearthstone glow markers |
| Animated | Platform bob (2 frames), chain sway (2 frames), shadow wisp drift (2 frames) |
| Foreground | Chain links, floating rock fragments |
| Background | Dark sky, cloud layer below, Spire above |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Void Dark | `#0C0420` | Deep sky void, shadow dome |
| Color 1 | Storm Purple | `#382858` | Sky, clouds, shadow energy |
| Color 2 | Worn Stone | `#888078` | Rock platforms, chains, debris |
| Color 3 | Ember Light | `#E8C060` | Hearthstone glow markers, lantern light, highlights |

**Visual Description:** An open-sky vertical environment dominated by the dark purple shadow dome above and a cloud layer below. Floating rock platforms of varying sizes form the ascending path. Heavy chains anchor some platforms. The Spire looms above, obscured by shadow energy. Far below, faint colored glows mark the reignited Hearthstones on the horizon. The mood is epic and exposed — nothing between Solen and the void but stone and determination.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Sky ascent and floating platform theme. Includes: floating rock platform surfaces (various sizes), chain-anchored platform, cloud-edge tiles, chain link wall tiles (climbable), rock face fragments, small floating rocks, bobbing platform, crumble platform (one-use with crack variants), shadow wisp hazard, void/edge tiles, chain segments, floating debris. Animated: platform bob up and down (2 frames), chain sway (2 frames), shadow wisp drift (2 frames). GBC style, 4-color palette: void dark #0C0420, storm purple #382858, worn stone #888078, ember light #E8C060. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Dark purple-black sky with swirling shadow energy above (the dome). Below, a layer of gray-purple clouds lit faintly from beneath. On the distant horizon, four colored glows mark the reignited Hearthstones (green, blue, teal, orange). The Spire is a white-stone silhouette above, partially obscured by shadow.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Open sky with dark purple-black void above and swirling shadow energy. Cloud layer in lower third lit faintly from below. On the distant horizon, four tiny colored glows — green, blue, teal, orange — marking reignited Hearthstones. Above, a white stone citadel (the Spire) partially visible through shadow dome. Epic, desperate, vertigo-inducing. GBC style, 4-color palette: void dark #0C0420, storm purple #382858, worn stone #888078, ember light #E8C060. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_spire_interior

**Used In:** Scenes 5-3, 5-4, 5-5

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Marble floor, cracked marble, shadow-stained marble |
| Wall | Marble wall, stained glass window (broken), pillar segment, archway |
| Platform | Balcony ledge, banner cloth (climbable ladder), scaffolding |
| Hazard | Shadow vein floor (pulse damage), broken glass floor (collapses) |
| Decoration | Torn Lamplighter banner, candelabra (unlit), Varek portrait in stained glass, throne |
| Animated | Shadow vein pulse (2 frames), glass shard fall (2 frames), banner flutter (2 frames) |
| Foreground | Column foreground, glass shard particles |
| Background | Grand hall interior, shattered windows |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Shadow Depth | `#100820` | Deepest shadow, corruption |
| Color 1 | Corrupted Marble | `#484058` | Stained walls, floor, pillars |
| Color 2 | Faded White | `#A8A0B0` | Marble highlights, banner remnants, glass |
| Color 3 | Varek Violet | `#B870E0` | Shadow veins, stained glass glow, energy |

**Visual Description:** A once-grand citadel interior, corrupted but still recognizable. Vaulted marble halls with cracked floors and shadow-stained walls. Broken stained-glass windows let in purple light. Torn Lamplighter banners hang from pillars. The architecture speaks of lost grandeur — this was a place of beauty and purpose, now defiled. The violet glow of shadow energy pulses through floor veins like a heartbeat.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Corrupted grand citadel interior. Includes: marble floor tiles (clean, cracked, shadow-stained variants), marble walls, broken stained glass window fragments (violet glow), pillar segments (base, middle, capital), archway tiles, balcony ledge platforms, banner cloth ladder tiles, scaffolding, shadow vein floor hazard (pulsing purple), broken glass floor hazard, torn Lamplighter banner decorations, unlit candelabra, throne pieces. Animated: shadow vein pulse (2 frames), glass shard fall (2 frames), banner flutter (2 frames). GBC style, 4-color palette: shadow depth #100820, corrupted marble #484058, faded white #A8A0B0, varek violet #B870E0. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** A grand interior hall receding into shadow. Tall pillars line the sides. Broken stained-glass windows at the back emit violet light. The far wall shows a massive corrupted mural of Varek's face assembled from broken glass.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Corrupted grand citadel hall interior. Tall marble pillars lining both sides receding into distance. Broken stained-glass windows in the back wall emitting violet light. Torn banners hanging from ceiling. Shadow energy veins running along walls. Massive corrupted mural of a face assembled from broken glass fragments. Dark, imposing, fallen grandeur. GBC style, 4-color palette: shadow depth #100820, corrupted marble #484058, faded white #A8A0B0, varek violet #B870E0. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_chamber_of_origin

**Used In:** Scene 6-1 (Secret area)

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Pristine white stone floor, golden inlay, mosaic tile |
| Wall | White stone wall with First Keeper murals, crystal-embedded wall |
| Platform | Stone pedestal (Lantern of Origin sits here) |
| Hazard | None |
| Decoration | First Keeper mural panels (creation, Hearthstones, sealing), crystal formations, light beams |
| Animated | Crystal shimmer (2 frames), light mote float (2 frames) |
| Foreground | Light beam overlay, dust motes |
| Background | Pure white chamber, mural walls |

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Soft Shadow | `#C8C0D0` | Lightest shadow (this palette is inverted — no true dark) |
| Color 1 | Warm Stone | `#D8D0C0` | Floor, walls, pedestals |
| Color 2 | Pure White | `#F0F0F0` | Wall highlights, crystal, light |
| Color 3 | Origin Gold | `#F8E078` | Inlay, mural accents, Lantern glow, crystal tips |

**Visual Description:** A stark contrast to every other environment in the game. The Chamber of Origin is pristine, untouched by time or corruption. The white stone is smooth and warm. Murals in perfect condition cover every wall, depicted in gold and white — the creation of Lumara, the planting of the Hearthstones, and the sealing of the Hollow. In the center, a small crystal lantern on a pedestal glows with pure white-gold light. The chamber feels sacred, hopeful, and final.

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Pristine ancient chamber theme — stark white and gold. Includes: clean white stone floor tiles, golden inlay floor patterns, mosaic tiles, white stone walls with carved mural panels (depicting figures planting crystals, sealing darkness), crystal-embedded wall sections, stone pedestal platform, crystal formations, light beam tiles. Animated: crystal shimmer (2 frames), light mote float (2 frames). No hazard tiles. Inverted palette — very bright. GBC style, 4-color palette: soft shadow #C8C0D0, warm stone #D8D0C0, pure white #F0F0F0, origin gold #F8E078. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** A bright, warm chamber. White stone walls with golden murals. Soft light emanates from everywhere — no single source. The Lantern of Origin glows at the center. Dust motes drift in warm light beams.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Pristine ancient chamber interior. Smooth white stone walls with golden mural carvings depicting figures, crystals, and cosmic events. Warm soft light filling the space from no single source. A central pedestal in the middle distance with a small glowing crystal lantern. Golden dust motes drifting in light beams. Sacred, pristine, hopeful, final. GBC style, 4-color palette: soft shadow #C8C0D0, warm stone #D8D0C0, pure white #F0F0F0, origin gold #F8E078. Clean pixel art, no anti-aliasing, indexed color.

---

### ts_hearthstone_chamber

**Used In:** Boss arenas and pre-boss scenes in all worlds

**Tile Types Needed:**

| Category | Tiles |
|---|---|
| Ground | Circular stone floor, mosaic ring pattern |
| Wall | Crystal housing base, pedestal column |
| Platform | Elevated observation ledge |
| Hazard | Variable per boss |
| Decoration | Hearthstone crystal (large background element), light ray tiles, energy particle |
| Animated | Crystal pulse (2 frames), light ray shimmer (2 frames) |

**Palette:** Variable per world — takes on the Hearthstone's color:
- World 1: Green tones
- World 2: Blue tones
- World 3: Teal tones
- World 4: Orange tones
- World 5: White/violet tones

**PIXEL ART GENERATION PROMPT — Tileset Sheet:**
> Pixel art tileset for a Game Boy Color platformer. 128x128 pixel sheet of 8x8 tiles (16x16 grid). Hearthstone chamber — shared across boss arenas. Includes: circular stone floor tiles with concentric mosaic ring pattern, crystal housing base tiles, pedestal column tiles, elevated observation ledge platform, large Hearthstone crystal background element tiles (arranged as a ~3x4 tile crystal shape), light ray tiles, energy particle tiles. Animated: crystal glow pulse (2 frames), light ray shimmer (2 frames). Designed in neutral gray tones to be palette-swapped per world: green for forest, blue for ice, teal for underwater, orange for volcanic, white for sky. GBC style, 4-color palette base: dark gray #282828, medium gray #686868, light gray #A8A8A8, white #E8E8E8. Clean pixel art, no anti-aliasing, indexed color, each tile exactly 8x8 pixels.

**Background Layer Description:** Variable per world — the Hearthstone itself is the focal point of the background, a massive crystal shape dominating the scene with light rays emanating from it.

**PIXEL ART GENERATION PROMPT — Background Image:**
> Pixel art background for a Game Boy Color platformer. 160x144 pixels. Hearthstone chamber — a massive glowing crystal (Hearthstone) dominating the center background. Light rays emanating outward from the crystal. Circular stone chamber walls receding behind it. The crystal is depicted in a neutral palette to be color-swapped: gray crystal with white glow and light rays. Dramatic, sacred, powerful. GBC style, 4-color palette: dark gray #282828, medium gray #686868, light gray #A8A8A8, white #E8E8E8. Clean pixel art, no anti-aliasing, indexed color.
