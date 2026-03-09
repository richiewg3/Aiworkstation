# 09 — Tilesets and Environments

---

## Tileset Overview

All tilesets use 8x8 pixel tiles arranged in a tileset sheet. GB Studio supports up to 8 background palettes in GBC mode, each with 4 colors. Each tileset is designed for a specific visual environment and can be shared across multiple scenes within that environment.

**Technical constraints:**
- Tile size: 8x8 pixels
- Background palettes per scene: up to 8, each with 4 colors
- Tileset sheets are organized as a grid of 8x8 tiles
- Tilesets must include all necessary tile types for the scene: ground, walls, transitions, decorations, interactive objects

---

## Tileset 1: Verdant Overworld Tileset

### Used In
- Verdant South Road
- Oakwatch Grove Entrance
- Verdant West Road

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Grass | Standard green grass, 2 variants (plain, with tiny flowers) |
| Ground — Dirt Path | Brown dirt road, straight, corners, and T-intersections |
| Ground — Cobblestone | Gray cobblestone path variant |
| Wall — Tree (Oak) | Large golden-leaved oak tree, 4 tiles (2x2 arrangement of 8x8 tiles) |
| Wall — Bush | Small green bush, 1 tile |
| Wall — Fence | Wooden fence segments: horizontal, vertical, corner, end post |
| Water — Stream | Flowing water tiles: horizontal, vertical, edges. 2-frame animation (subtle flow) |
| Decoration — Fallen Leaves | Scattered golden leaves on ground (overlay on grass) |
| Decoration — Flower Patch | Small wildflower clusters (purple, yellow) |
| Decoration — Rock | Small gray stones, 2 variants |
| Interactive — Sign | Wooden signpost |
| Interactive — Chest | Treasure chest (closed state, open state) |
| Transition — Cave Entrance | Dark opening in hillside |
| Transition — Path Edge | Grass-to-dirt transition tiles |
| Ambient — Time Distortion | Tiles with subtle color shift (represents temporal anomaly areas) |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A5E2A` | Dark green (tree trunks, shadows) |
| Color 2 | `#7BAE5E` | Medium green (grass, leaves) |
| Color 3 | `#D4A847` | Gold (autumn leaves, path) |
| Color 4 | `#F5E6C8` | Cream (highlights, sky) |

### Visual Style
Warm autumnal countryside. Golden-leaved trees, green grass transitioning to brown dirt paths, wooden fences marking farm boundaries. The overall feel is pastoral and nostalgic — a place you would want to call home.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG overworld. Warm autumnal countryside theme. Grid of tiles including: green grass (2 variants), dirt path (straight, corners, T-junction), cobblestone path, large golden oak trees (4-tile 2x2 arrangement), green bushes, wooden fence segments, flowing stream tiles, fallen golden leaves, wildflowers, rocks, wooden signpost, treasure chest (open/closed), cave entrance, grass-to-dirt transitions. GBC 4-color palette: #2A5E2A (dark green), #7BAE5E (medium green), #D4A847 (gold), #F5E6C8 (cream). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 2: Verdant Town Tileset

### Used In
- Millhaven Town Square

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Cobblestone | Town square paving, 2 variants |
| Ground — Grass Patch | Small grass areas between buildings |
| Wall — Building (Thatch Roof) | Thatched-roof house walls, front, side, roof tiles |
| Wall — Building (Stone) | Stone building walls for the town hall |
| Wall — Well | Town well structure (2x2 tiles) |
| Wall — Market Stall | Wooden stall with awning |
| Decoration — Barrel | Wooden barrel |
| Decoration — Crate | Wooden crate |
| Decoration — Lamp Post | Iron lamp with warm light |
| Decoration — Potted Plant | Small plant pot outside buildings |
| Interactive — Door | Wooden door (house entrance, shop entrance) |
| Interactive — Sign | Shop sign hanging from bracket |
| Transition — Town Gate | Wooden arch at town entrance (south gate) |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#4A3020` | Dark brown (building frames, shadows) |
| Color 2 | `#8B6040` | Medium brown (wood, thatch) |
| Color 3 | `#D4B880` | Tan (walls, cobblestone) |
| Color 4 | `#F0E8D0` | Cream (highlights, sky) |

### Visual Style
Cozy medieval village. Stone and wood buildings with thatched roofs, cobblestone central square, warm earthy tones. Market stalls and barrels give a lived-in feel.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG village town. Medieval village theme. Grid of tiles including: cobblestone ground (2 variants), grass patches, thatched-roof house walls (front, side, roof), stone town hall walls, town well (2x2), market stall with awning, wooden barrels, crates, iron lamp posts, potted plants, wooden doors, hanging shop signs, wooden gate arch. GBC 4-color palette: #4A3020 (dark brown), #8B6040 (medium brown), #D4B880 (tan), #F0E8D0 (cream). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 3: Verdant Interior Tileset

### Used In
- Alaric's Workshop (interior)
- Wynn's General Store (interior)

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Wood Floor | Wooden plank floor, 2 variants |
| Wall — Interior Wall | Plaster/stone interior walls |
| Wall — Shelf | Wall-mounted shelves with items |
| Decoration — Workbench | Large workbench with tools (2x1 tiles) |
| Decoration — Clock | Wall-mounted clock |
| Decoration — Gear Display | Clockwork gear on wall |
| Decoration — Counter | Shop counter |
| Decoration — Rug | Small woven rug |
| Decoration — Barrel (Indoor) | Indoor storage barrel |
| Decoration — Book | Stack of books/papers |
| Interactive — Door | Interior door to exit |
| Interactive — Table | Table with items |
| Decoration — Chair | Wooden chair |
| Decoration — Window | Small window showing outside |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#3A2A1E` | Dark brown (shadows, furniture) |
| Color 2 | `#8B6040` | Medium brown (wood floor, shelves) |
| Color 3 | `#C0A070` | Warm tan (walls, counter) |
| Color 4 | `#F0E8D0` | Cream (highlights, paper) |

### Visual Style
Warm interior of rustic buildings. Wooden plank floors, plastered walls, cluttered with tools and merchandise. Cozy and functional.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG building interior. Rustic workshop/shop theme. Grid of tiles including: wooden plank floor (2 variants), plaster interior walls, wall-mounted shelves, workbench with tools, wall clocks, clockwork gears on walls, shop counter, woven rug, indoor barrels, book stacks, interior door, table, wooden chair, small window. GBC 4-color palette: #3A2A1E (dark brown), #8B6040 (medium brown), #C0A070 (warm tan), #F0E8D0 (cream). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 4: Meridian Dungeon Tileset

### Used In
- Verdant Meridian F1, F2, Vault

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Stone Floor | Gray-green stone floor tiles, 2 variants |
| Ground — Brass Inlay | Stone with brass gear inlay pattern |
| Wall — Stone Wall | Dungeon stone wall, upper and lower halves |
| Wall — Gear Wall | Wall with large decorative gears |
| Wall — Conduit Wall | Wall with glowing Aether conduits |
| Decoration — Large Gear | Massive gear mechanism (2x2 tiles) |
| Decoration — Small Gear | Single-tile gear decoration |
| Decoration — Aether Crystal | Small crystal formation on floor |
| Decoration — Torch | Wall-mounted torch with green Aether flame |
| Interactive — Chest | Dungeon treasure chest |
| Interactive — Lever | Wall lever for puzzles |
| Interactive — Gear Puzzle | Rotatable gear mechanism |
| Transition — Stairs | Stairs going up/down |
| Transition — Door (Locked) | Heavy stone door, locked state |
| Transition — Door (Open) | Heavy stone door, open state |
| Wall — Clock Face | Large decorative clock face on wall (2x2 tiles) |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A3A2A` | Dark green-gray (shadows) |
| Color 2 | `#607060` | Medium stone green |
| Color 3 | `#C0A840` | Brass (gears, mechanisms) |
| Color 4 | `#A0D8B0` | Aether green (glowing elements) |

### Visual Style
Ancient clock tower interior. Stone corridors with brass mechanical elements embedded in the walls. Aether-powered conduits glow with soft green light. Gears of various sizes are visible on walls and ceilings. The atmosphere is mechanical and rhythmic.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG clock tower dungeon. Ancient mechanical tower interior. Grid of tiles including: stone floor (2 variants), brass inlay floor, stone dungeon walls (upper/lower), gear wall decoration, glowing Aether conduit walls, large gear mechanism (2x2), small gears, Aether crystal formations, wall torches with green flame, treasure chest, wall lever, rotatable gear puzzle, stairs, heavy stone doors (locked/open), large clock face (2x2). GBC 4-color palette: #2A3A2A (dark green-gray), #607060 (medium stone), #C0A840 (brass), #A0D8B0 (Aether green glow). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 5: Stormhaven Town Tileset

### Used In
- Stormhaven Town Center
- Harbor District

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Wet Cobblestone | Rain-slicked cobblestone, darker than Verdant cobblestone |
| Ground — Wooden Boardwalk | Dock/boardwalk planks |
| Wall — Stone Building (Slate Roof) | Cliff-side buildings with dark slate roofs |
| Wall — Cliff Edge | Rocky cliff edge tiles |
| Wall — Rope Railing | Rope fence/railing along cliff paths |
| Water — Ocean | Deep blue-gray ocean water, 2-frame animation (wave motion) |
| Decoration — Barrel (Weathered) | Salt-worn barrel |
| Decoration — Crate (Stacked) | Stacked shipping crates |
| Decoration — Rope Coil | Coiled rope on dock |
| Decoration — Anchor | Ship anchor leaning on wall |
| Decoration — Lantern | Hanging oil lantern |
| Interactive — Door | Reinforced wooden door |
| Interactive — Message Board | Community message board (save point) |
| Transition — Ladder | Ladder between cliff levels |
| Ambient — Rain | Rain overlay tiles (sprite-based) |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A3A4A` | Dark blue-gray (shadows, wet stone) |
| Color 2 | `#5A7080` | Medium steel blue (stone, slate) |
| Color 3 | `#A0B8C8` | Light blue-gray (highlights, sky) |
| Color 4 | `#D0D8E0` | Pale gray-white (foam, rain) |

### Visual Style
Harsh coastal town built into cliffs above a stormy sea. Dark stone buildings with slate roofs, weathered by salt and wind. Wooden boardwalks and rope bridges connect levels. Everything is wet and wind-battered.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG coastal cliff town. Stormy harbor town theme. Grid of tiles including: wet cobblestone, wooden boardwalk planks, stone buildings with slate roofs, cliff edges, rope railings, deep ocean water (animated waves), weathered barrels, stacked shipping crates, coiled rope, ship anchor, hanging oil lanterns, reinforced doors, message board, ladder. GBC 4-color palette: #2A3A4A (dark blue-gray), #5A7080 (steel blue), #A0B8C8 (light blue-gray), #D0D8E0 (pale gray-white). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 6: Stormhaven Interior Tileset

### Used In
- Stormhaven Warehouse (interior)
- Tully's Shop (interior, shares with Verdant Interior + color swap)

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Damp Wood Floor | Wet wooden planks, darker than Verdant interior |
| Wall — Stone Interior | Rough stone interior walls |
| Decoration — Crate Stack | Large stacked crates |
| Decoration — Barrel Row | Row of storage barrels |
| Decoration — Lantern (Indoor) | Hanging indoor lantern, warm glow |
| Decoration — Netting | Fishing nets on walls |
| Decoration — Ship Wheel | Decorative ship wheel on wall |
| Interactive — Door | Interior door |
| Decoration — Counter (Fish Shop) | Counter with fish display |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A2A30` | Near black (deep shadows) |
| Color 2 | `#5A5050` | Dark brown-gray (wet wood) |
| Color 3 | `#A09080` | Medium warm gray (stone, crates) |
| Color 4 | `#D8C8A0` | Warm lamp glow (highlights) |

### Visual Style
Dark, damp warehouse and shop interiors. Low light from hanging lanterns. Rough stone walls, wet wooden floors, stacked crates and barrels. Fishing nets and nautical decorations.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG warehouse interior. Dark damp coastal warehouse theme. Grid of tiles including: damp wooden plank floor, rough stone walls, large stacked crates, barrel rows, hanging lanterns with warm glow, fishing nets on walls, decorative ship wheel, interior door, fish shop counter. GBC 4-color palette: #2A2A30 (near black), #5A5050 (dark gray-brown), #A09080 (warm gray), #D8C8A0 (lamp glow). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 7: Tidal Dungeon Tileset

### Used In
- Tidal Meridian F1, F2, Sanctum

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Wet Stone | Water-logged stone floor, reflective surface |
| Ground — Shallow Water | Ankle-deep water with visible floor beneath |
| Wall — Barnacle Stone | Stone walls encrusted with barnacles and seaweed |
| Wall — Water Channel | Channeled water flowing through walls |
| Water — Deep Pool | Deep water (impassable), animated ripple |
| Decoration — Coral | Coral formations on walls/floor |
| Decoration — Water Wheel | Large water wheel mechanism (2x2 tiles) |
| Decoration — Shell Cluster | Cluster of shells on floor |
| Decoration — Aether Crystal (Blue) | Glowing blue Aether crystal |
| Interactive — Chest | Waterlogged treasure chest |
| Interactive — Valve | Water valve puzzle mechanism |
| Transition — Stairs | Wet stone stairs |
| Transition — Flood Gate | Gate that opens/closes based on water level |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A3040` | Deep teal-black (deep water, shadows) |
| Color 2 | `#3A7080` | Medium teal (wet stone, barnacles) |
| Color 3 | `#80C0D0` | Aqua (shallow water, highlights) |
| Color 4 | `#D0F0F8` | Pale ice blue (foam, Aether glow) |

### Visual Style
Underwater-themed clock tower dungeon. Stone corridors flooded with seawater. Barnacles and coral encrust the ancient walls. Water wheels and channels serve as puzzle mechanisms. Aqua-blue lighting from Aether crystals and bioluminescent marine life.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG water dungeon. Flooded clock tower interior with tidal theme. Grid of tiles including: wet reflective stone floor, shallow water with visible floor, barnacle-encrusted stone walls, water channel walls, deep water pool (animated ripple), coral formations, large water wheel (2x2), shell clusters, blue Aether crystals, waterlogged chest, water valve mechanism, wet stairs, flood gate. GBC 4-color palette: #1A3040 (deep teal-black), #3A7080 (medium teal), #80C0D0 (aqua), #D0F0F8 (pale ice blue). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 8: Ashenveil Overworld Tileset

### Used In
- Ashenveil North Road
- Outer Bog
- Architect Ruins
- Hollow Meridian Approach

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Mud | Soft brown mud, 2 variants |
| Ground — Marsh Grass | Sparse, sickly green-yellow grass |
| Ground — Decay Patch | Visibly rotting ground (hazard tile — damages player) |
| Wall — Twisted Tree | Gnarled, mossy tree, multiple tile arrangement |
| Wall — Thick Brush | Dense, dark swamp brush |
| Water — Bog Water | Still, murky green-brown water |
| Decoration — Moss Cluster | Hanging moss on trees |
| Decoration — Mushroom | Bioluminescent mushroom cluster |
| Decoration — Bone | Animal bones protruding from mud |
| Decoration — Ruined Wall | Crumbling stone wall fragment (Architect ruins) |
| Decoration — Tablet | Inscribed stone tablet (Architect lore) |
| Interactive — Chest | Moss-covered chest |
| Interactive — Sign | Decayed wooden sign |
| Transition — Wooden Walkway | Rickety plank walkway over bog |
| Ambient — Fog | Fog overlay tiles (semi-transparent) |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A2A1A` | Very dark green (deep shadow) |
| Color 2 | `#4A5A3A` | Dark olive (trees, brush) |
| Color 3 | `#7A6A8A` | Muted purple (decay, mushrooms) |
| Color 4 | `#A0C060` | Sickly green (luminescence, marsh grass) |

### Visual Style
Oppressive swampland. Twisted trees draped in moss, murky water, patches of accelerated decay where the ground itself rots and reforms. Bioluminescent mushrooms provide eerie light. Crumbling Architect ruins emerge from the bog. Fog hangs over everything.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG swamp overworld. Dark decaying marsh theme. Grid of tiles including: soft mud (2 variants), sickly marsh grass, decay hazard patches, gnarled twisted mossy trees (multi-tile), thick dark brush, still murky bog water, hanging moss, bioluminescent mushrooms, animal bones in mud, crumbling stone ruins, inscribed tablets, moss-covered chest, decayed sign, rickety plank walkway, fog overlay. GBC 4-color palette: #1A2A1A (very dark green), #4A5A3A (dark olive), #7A6A8A (muted purple), #A0C060 (sickly green). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 9: Hollow Dungeon Tileset

### Used In
- Hollow Meridian F1, F2, Depths

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Decayed Stone | Crumbling stone floor with visible cracks |
| Ground — Flooded Floor | Waist-deep water over stone (cosmetic) |
| Ground — Crumbling Tile | Floor that visually crumbles (hazard/puzzle mechanic) |
| Wall — Moss-Covered Stone | Ancient stone wall thick with moss and fungus |
| Wall — Root Wall | Walls broken through by tree roots |
| Decoration — Fungus Cluster | Large bioluminescent fungus on walls |
| Decoration — Dripping Water | Water dripping from ceiling (animated) |
| Decoration — Broken Mechanism | Rusted, decayed Meridian gear mechanisms |
| Decoration — Skeleton | Ancient skeleton (Architect-era) |
| Interactive — Bookshelf | Keeper's bookshelf (lore/hidden cache) |
| Interactive — Chest | Decayed wooden chest |
| Transition — Stairs (Descending) | Stairs going deeper |
| Transition — Collapsed Passage | Partially collapsed corridor |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A1A20` | Near black (deep shadow) |
| Color 2 | `#3A4A3A` | Dark mossy green |
| Color 3 | `#7A5A8A` | Decay purple (fungus, corruption) |
| Color 4 | `#80C080` | Bioluminescent green (light sources) |

### Visual Style
Deeply decayed Meridian interior. Everything is crumbling, flooded, and overgrown. Bioluminescent fungus replaces the torches. Tree roots have broken through walls. The architecture is still recognizable as Architect-built but has been claimed by the marsh. An atmosphere of beautiful ruin.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG decayed dungeon. Submerged ruined clock tower overrun by nature. Grid of tiles including: crumbling stone floor, flooded floor with shallow water, crumbling hazard tiles, moss-covered stone walls, root-broken walls, bioluminescent fungus clusters, dripping water (animated), broken rusted gear mechanisms, ancient skeleton, bookshelf, decayed chest, descending stairs, collapsed passage. GBC 4-color palette: #1A1A20 (near black), #3A4A3A (dark mossy green), #7A5A8A (decay purple), #80C080 (bioluminescent green). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 10: Crystalfall Overworld Tileset

### Used In
- Crystalfall Border Pass
- Frozen Expanse
- Frozen Caravan
- Crystal Canyon

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — White Sand | Pale white desert sand, 2 variants |
| Ground — Crystal Formation | Floor-level crystal growth |
| Wall — Crystal Pillar | Tall crystallized Aether pillar (multi-tile) |
| Wall — Frozen Sand Dune | Sand dune frozen mid-wave |
| Wall — Canyon Wall | Crystal canyon cliff face |
| Decoration — Suspended Sand | Sand particles frozen mid-air (animated sparkle) |
| Decoration — Frozen Bird | Bird suspended in flight (small decoration) |
| Decoration — Frozen Wagon | Caravan wagon frozen in place (multi-tile) |
| Decoration — Crystal Flower | Small Aether crystal flower formation |
| Interactive — Chest | Crystal-encased chest |
| Interactive — Crystal Formation (Interactable) | Aether crystal that can be examined |
| Transition — Canyon Entrance | Opening in crystal canyon wall |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#4A5060` | Dark blue-gray (shadows, canyon wall) |
| Color 2 | `#A0B0C0` | Medium gray-blue (sand shadows, rock) |
| Color 3 | `#D0E8F0` | Pale ice blue (crystal, frozen elements) |
| Color 4 | `#F0F8F8` | Near white (sand, highlights) |

### Visual Style
Stark, ethereal frozen desert. White sand stretches to the horizon, with everything suspended in temporal stasis. Crystallized Aether formations rise from the ground like frozen geysers, refracting light into subtle rainbow spectra. The silence is visually palpable — suspended particles, motionless wildlife, frozen caravans. A landscape of alien beauty.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG frozen crystal desert. Time-frozen desert with crystallized Aether formations. Grid of tiles including: white sand (2 variants), crystal floor formations, tall crystal Aether pillars (multi-tile), frozen sand dunes, crystal canyon walls, suspended sand particles (sparkle animation), frozen bird decoration, frozen wagon (multi-tile), crystal flowers, crystal-encased chest, interactable crystal formation, canyon entrance. GBC 4-color palette: #4A5060 (dark blue-gray), #A0B0C0 (medium gray-blue), #D0E8F0 (pale ice blue), #F0F8F8 (near white). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 11: Prism Dungeon Tileset

### Used In
- Prism Meridian F1, F2, Sanctum

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Crystal Floor | Translucent crystal floor with faceted pattern |
| Ground — Light Beam Path | Floor illuminated by a light beam (puzzle element) |
| Wall — Crystal Wall | Translucent crystallized Aether walls |
| Wall — Refraction Panel | Panel that redirects light beams |
| Decoration — Light Beam (Horizontal) | Frozen Aether light beam going horizontally |
| Decoration — Light Beam (Vertical) | Frozen Aether light beam going vertically |
| Decoration — Prism Block | Movable block that redirects light (puzzle) |
| Decoration — Rainbow Refraction | Small rainbow effect from light passing through crystal |
| Interactive — Crystal Switch | Light-activated switch |
| Interactive — Chest | Crystal chest |
| Transition — Crystal Stairs | Stairs made of translucent crystal |
| Transition — Crystal Door | Door that opens when correct light pattern is achieved |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A2A3A` | Dark indigo (deep crystal shadow) |
| Color 2 | `#60C0D0` | Cyan (crystal, light beams) |
| Color 3 | `#D0A0E0` | Prismatic purple/pink (refractions) |
| Color 4 | `#F0F8F8` | Bright white (light, highlights) |

### Visual Style
Interior of a crystal Meridian. Everything is translucent, faceted, and refractive. Light beams criss-cross the rooms, creating a kaleidoscopic effect. The architecture is geometric and precise — the Architects at their most elegant. Light is both decoration and puzzle mechanic.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG crystal dungeon. Translucent crystalline Meridian tower interior. Grid of tiles including: faceted crystal floor, light beam illuminated path, translucent crystal walls, refraction panels, horizontal and vertical light beams, movable prism blocks, rainbow refraction effects, light-activated switches, crystal chest, crystal stairs, crystal doors. GBC 4-color palette: #2A2A3A (dark indigo), #60C0D0 (cyan), #D0A0E0 (prismatic purple-pink), #F0F8F8 (bright white). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 12: Ironpeak Overworld Tileset

### Used In
- Ironpeak Mountain Pass

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Snow | White snow ground, 2 variants (fresh, packed) |
| Ground — Rocky Path | Gray mountain path |
| Wall — Mountain Rock | Rocky outcrop, cliff face |
| Wall — Pine Tree | Snow-dusted pine tree (multi-tile) |
| Wall — Snow Drift | Deep snow bank (impassable) |
| Decoration — Ice Patch | Slippery ice formation |
| Decoration — Mining Cart | Abandoned mining cart |
| Decoration — Pickaxe | Pickaxe embedded in rock |
| Interactive — Chest | Snow-covered chest |
| Transition — Cave Entrance | Mine/cave entrance in rock face |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#3A3A40` | Dark gray (rock, shadows) |
| Color 2 | `#808890` | Medium gray (stone path) |
| Color 3 | `#C0C8D0` | Light gray-blue (snow shadow) |
| Color 4 | `#F0F0F8` | Near white (fresh snow, highlights) |

### Visual Style
Cold mountain pass. Snow-covered ground with exposed gray rock. Sparse pine trees dusted with snow. Mining infrastructure (carts, tracks) hints at the Ironpeak Enclave below. The path is narrow and exposed, with wind-blown snow particles.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG snowy mountain pass. Cold mountain theme. Grid of tiles including: white snow ground (2 variants), gray rocky path, mountain rock outcrops, snow-dusted pine trees (multi-tile), deep snow drift banks, ice patches, abandoned mining cart, pickaxe in rock, snow-covered chest, mine cave entrance. GBC 4-color palette: #3A3A40 (dark gray), #808890 (medium gray), #C0C8D0 (light blue-gray), #F0F0F8 (near white). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 13: Ironpeak Town Tileset

### Used In
- Ironpeak Enclave Main Hall

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Carved Stone | Smooth carved stone floor (underground town) |
| Ground — Metal Grating | Steel grating over underground channels |
| Wall — Carved Rock | Carved mountain rock walls |
| Wall — Steel Support | Steel beam support structure |
| Wall — Forge Chimney | Forge chimney rising into ceiling |
| Decoration — Forge Fire | Active forge with orange fire (animated glow) |
| Decoration — Anvil | Blacksmith's anvil |
| Decoration — Steel Catwalk | Elevated metal walkway |
| Decoration — Crystal Lamp | Aether crystal lamp mounted on wall |
| Decoration — Gear Decoration | Decorative engineering gear |
| Decoration — Blueprint Table | Table with blueprints |
| Interactive — Door | Heavy metal door |
| Interactive — Market Stall (Metal) | Steel-framed market stall |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A2020` | Near black (deep shadow, iron) |
| Color 2 | `#5A5A60` | Steel gray (metal, grating) |
| Color 3 | `#D08030` | Orange-brass (forge fire, copper) |
| Color 4 | `#E0D0B0` | Warm light (lamp glow, highlights) |

### Visual Style
Underground industrial town carved into a mountain. Orange forge light contrasts with cool steel gray of the engineering infrastructure. Metal catwalks, heavy doors, and crystal-lit tunnels. The warmth of the forges makes it feel like a sanctuary despite being underground.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG underground forge town. Industrial dwarven-style mountain enclave. Grid of tiles including: smooth carved stone floor, metal grating, carved rock walls, steel support beams, forge chimney, active forge with fire (animated glow), blacksmith anvil, steel catwalks, Aether crystal lamps, decorative gears, blueprint table, heavy metal doors, steel-framed market stalls. GBC 4-color palette: #2A2020 (near black), #5A5A60 (steel gray), #D08030 (orange-brass), #E0D0B0 (warm light). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 14: Ironpeak Interior Tileset

### Used In
- Enclave Deep Forge (interior)
- Enclave Archives (interior)

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Stone Floor (Polished) | Smoother stone floor for interior rooms |
| Wall — Carved Wall (Interior) | Interior carved rock with smoother finish |
| Decoration — Smelter | Large smelting apparatus |
| Decoration — Weapon Rack | Wall rack displaying weapons |
| Decoration — Scroll Shelf | Shelf of scrolls and blueprints |
| Decoration — Display Case | Glass case with Architect artifact |
| Decoration — Reading Table | Large table with open books |
| Interactive — Door | Interior heavy door |
| Interactive — Anvil (Interactive) | Crafting anvil |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#2A1A10` | Very dark brown-black |
| Color 2 | `#5A4A3A` | Dark warm brown |
| Color 3 | `#C07030` | Copper-orange (metal, warmth) |
| Color 4 | `#F0E0C0` | Warm cream (parchment, light) |

### Visual Style
Interior workshops and libraries of the Ironpeak Enclave. Polished stone floors, weapon racks, display cases with Architect artifacts, large tables covered in blueprints. Warmer and more refined than the exterior areas.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG forge interior and library. Industrial workshop and archive rooms. Grid of tiles including: polished stone floor, smooth carved walls, smelting apparatus, weapon rack, scroll shelves, glass display cases, reading table with books, heavy interior door, crafting anvil. GBC 4-color palette: #2A1A10 (very dark brown), #5A4A3A (dark warm brown), #C07030 (copper-orange), #F0E0C0 (warm cream). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 15: Chronospire Dungeon Tileset

### Used In
- Chronospire F1, F2, F3, F4, Warden's Sanctum, Stasis Chamber

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Architect Stone | Pristine, precisely cut stone with glowing inscription lines |
| Ground — Aether Flow | Floor with visible Aether energy flowing beneath translucent surface |
| Wall — Architect Wall | Massive stone walls with luminous inscriptions |
| Wall — Inscription Panel | Wall section with dense glowing text |
| Wall — Time Distortion | Wall that appears warped/glitched (visual distortion) |
| Decoration — Floating Fragment | Master Core fragment hovering (animated bob) |
| Decoration — Aether Conduit (Active) | Large active Aether conduit, pulsing |
| Decoration — Broken Mechanism | Shattered Architect mechanism |
| Decoration — Crystal Record | Frozen Aether record crystal (lore interactable) |
| Decoration — Vasael's Notes | Scattered papers and instruments |
| Interactive — Chest | Architect-style chest |
| Interactive — Crystal Terminal | Interactable Architect terminal |
| Transition — Grand Stairs | Wide, ornate staircase |
| Transition — Sealed Door | Door with Architect seal (requires key/event) |
| Ambient — Aether Distortion | Shimmering distortion overlay |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A1A2A` | Deep indigo-black (shadows) |
| Color 2 | `#4A4A6A` | Medium indigo (stone) |
| Color 3 | `#8080C0` | Soft blue-purple (inscriptions) |
| Color 4 | `#C0C0E0` | Pale lavender (Aether glow, highlights) |

### Visual Style
The ultimate dungeon — the Architects' masterwork. Pristine stone corridors with luminous inscriptions that glow softly in indigo and lavender. The architecture is grand and alien — perfectly geometric, impossibly precise. Aether flows visibly through channels in the floor and walls. Time distortions manifest as visual glitches. The atmosphere oscillates between awe and dread.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG ancient tower dungeon. Grand alien architecture with glowing inscriptions. Grid of tiles including: precisely cut stone floor with glowing lines, translucent Aether flow floor, massive inscribed walls, dense glowing text panels, time-distortion warped walls, floating Core fragments (animated), active Aether conduits, broken mechanisms, frozen crystal records, scattered notes, Architect chest, crystal terminal, grand ornate staircase, sealed Architect door, shimmering distortion overlay. GBC 4-color palette: #1A1A2A (deep indigo), #4A4A6A (medium indigo), #8080C0 (soft blue-purple), #C0C0E0 (pale lavender). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 16: Chronospire Heart Tileset (True Ending — Gold Variant)

### Used In
- Chronospire Heart (Floor 6, secret boss)

### Tile Types

Same tile types as the Chronospire Dungeon Tileset, but with a warm golden palette swap to represent the tower's awakened, benevolent state.

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#3A2A10` | Dark amber (shadows) |
| Color 2 | `#806030` | Medium amber (stone) |
| Color 3 | `#D0A030` | Warm gold (inscriptions, conduits) |
| Color 4 | `#F0E0A0` | Light gold (glow, highlights) |

### Visual Style
The same architecture as the Chronospire, but bathed in warm golden light. The inscriptions glow gold instead of indigo. The atmosphere shifts from dread to reverence. This is the tower's true form — alive, benevolent, and beautiful.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG sacred golden tower interior. Same grand alien architecture as a clock tower dungeon but bathed in warm golden light. Glowing gold inscriptions instead of indigo. Grid of tiles including: golden-lit stone floor, warm Aether flow, golden inscribed walls, floating golden crystal formations, active golden conduits, crystal records. GBC 4-color palette: #3A2A10 (dark amber), #806030 (medium amber), #D0A030 (warm gold), #F0E0A0 (light gold). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 17: Stillwater Tileset

### Used In
- Stillwater Basin Crossing

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Water — Calm Sea | Calm deep blue water, gentle 2-frame animation |
| Decoration — Boat | Small rowing boat (player sprite occupies) |
| Decoration — Island Silhouette | Chronospire island in distance |
| Decoration — Wake | Boat wake trail on water |
| Ground — Dock | Wooden dock at shore edge |

### Palette

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A2A3A` | Deep navy (deep water) |
| Color 2 | `#3A5A7A` | Medium blue (water surface) |
| Color 3 | `#80A0C0` | Light blue (wave highlights) |
| Color 4 | `#D0D8E8` | Pale blue-white (foam, sky reflection) |

### Visual Style
Calm inland sea crossing. Deep blue water with gentle ripples. A small boat carries the party toward the Chronospire island, which dominates the horizon as a silhouette. Somber and final in tone.

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color top-down RPG calm sea crossing. Inland sea transition scene. Grid of tiles including: calm deep blue water (animated gentle ripple), small rowing boat, island silhouette in distance, boat wake trail, wooden dock. GBC 4-color palette: #1A2A3A (deep navy), #3A5A7A (medium blue), #80A0C0 (light blue), #D0D8E8 (pale blue-white). Clean pixel art, no anti-aliasing, indexed color, top-down perspective."

---

## Tileset 18: Battle Arena Tileset

### Used In
- `battle_arena` (generic battle scene, palette swapped per region)

### Tile Types

| Tile Type | Description |
|-----------|-------------|
| Ground — Arena Floor | Simple tiled floor for battle standing area |
| Background — Region Backdrop | Upper portion showing environment (changes per region via palette) |
| UI — Divider Line | Horizontal line separating enemy area from party area |

### Palette (Default — swapped per region)

| Color | Hex | Role |
|-------|-----|------|
| Color 1 | `#1A1A2A` | Dark (background) |
| Color 2 | `#4A4A5A` | Medium (floor, details) |
| Color 3 | `#8A8AA0` | Light (highlights) |
| Color 4 | `#D0D0E0` | Brightest (text area, contrast) |

### Pixel Art Generation Prompt — Tileset Sheet

> "8x8 pixel tile tileset sheet for a Game Boy Color RPG battle arena background. Simple battle scene backdrop. Grid of tiles including: tiled arena floor, upper backdrop area (generic, will be palette-swapped), horizontal divider line, empty space for UI overlay. Neutral palette: #1A1A2A (dark), #4A4A5A (medium), #8A8AA0 (light), #D0D0E0 (bright). Clean pixel art, no anti-aliasing, indexed color."

---

## Tileset Summary Table

| # | Tileset Name | Palette Colors | Scenes Used In |
|---|-------------|---------------|----------------|
| 1 | Verdant Overworld | `#2A5E2A` `#7BAE5E` `#D4A847` `#F5E6C8` | South Road, Oakwatch, West Road |
| 2 | Verdant Town | `#4A3020` `#8B6040` `#D4B880` `#F0E8D0` | Millhaven Town Square |
| 3 | Verdant Interior | `#3A2A1E` `#8B6040` `#C0A070` `#F0E8D0` | Alaric's Workshop, Wynn's Shop |
| 4 | Meridian Dungeon | `#2A3A2A` `#607060` `#C0A840` `#A0D8B0` | Verdant Meridian F1/F2/Vault |
| 5 | Stormhaven Town | `#2A3A4A` `#5A7080` `#A0B8C8` `#D0D8E0` | Stormhaven Town, Harbor |
| 6 | Stormhaven Interior | `#2A2A30` `#5A5050` `#A09080` `#D8C8A0` | Warehouse |
| 7 | Tidal Dungeon | `#1A3040` `#3A7080` `#80C0D0` `#D0F0F8` | Tidal Meridian F1/F2/Sanctum |
| 8 | Ashenveil Overworld | `#1A2A1A` `#4A5A3A` `#7A6A8A` `#A0C060` | Ashenveil areas, Ruins |
| 9 | Hollow Dungeon | `#1A1A20` `#3A4A3A` `#7A5A8A` `#80C080` | Hollow Meridian F1/F2/Depths |
| 10 | Crystalfall Overworld | `#4A5060` `#A0B0C0` `#D0E8F0` `#F0F8F8` | Desert areas, Canyon |
| 11 | Prism Dungeon | `#2A2A3A` `#60C0D0` `#D0A0E0` `#F0F8F8` | Prism Meridian F1/F2/Sanctum |
| 12 | Ironpeak Overworld | `#3A3A40` `#808890` `#C0C8D0` `#F0F0F8` | Mountain Pass |
| 13 | Ironpeak Town | `#2A2020` `#5A5A60` `#D08030` `#E0D0B0` | Ironpeak Enclave |
| 14 | Ironpeak Interior | `#2A1A10` `#5A4A3A` `#C07030` `#F0E0C0` | Deep Forge, Archives |
| 15 | Chronospire Dungeon | `#1A1A2A` `#4A4A6A` `#8080C0` `#C0C0E0` | Chronospire F1–F5, Stasis |
| 16 | Chronospire Heart | `#3A2A10` `#806030` `#D0A030` `#F0E0A0` | Chronospire Heart (secret) |
| 17 | Stillwater | `#1A2A3A` `#3A5A7A` `#80A0C0` `#D0D8E8` | Basin Crossing |
| 18 | Battle Arena | `#1A1A2A` `#4A4A5A` `#8A8AA0` `#D0D0E0` | Battle scenes |

---

*Chronospire: The Shattered Meridian — Tilesets and Environments Document*
