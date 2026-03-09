# 03 — Characters

---

## Player Character

### Solen — The Lamplighter

**Role:** Protagonist, playable character

**Physical Description:**
Solen is a nineteen-year-old woman of average height (5'4" in-world, 16px tall in sprite) with a wiry, athletic build — lean from years of walking long roads carrying heavy lanterns. She has short, messy auburn hair that sticks out at angles (she cuts it herself with shears because long hair catches fire near lanterns). Her skin is warm tan with faint freckles across her nose. Her eyes are amber-gold, matching the color of Hearthstone light.

She wears the Lamplighter apprentice uniform: a dark teal long-coat that falls to her knees, belted at the waist with a leather tool belt. Underneath is a cream-colored tunic and brown trousers tucked into scuffed leather boots. She wears fingerless gloves (dark brown) and a short shoulder cape on her left side — a half-cape in faded orange, which is the traditional Lamplighter color. Her mother's lantern staff is taller than she is — a dark wood walking stick topped with a brass lantern housing a glowing amber Hearthstone shard.

**Personality and Backstory:**
Solen is stubborn, practical, and dry-humored. She hides her fear behind sarcasm and her grief behind constant motion — if she stops moving, she'll start thinking, and if she starts thinking, she'll remember her mother turning to stone. She is not naturally brave; she is naturally determined, which looks like bravery from the outside but feels like panic from the inside. She talks to herself constantly (a habit from walking dark roads alone) and has a tendency to name inanimate objects (she calls the lantern staff "Old Mare" after her mother, though she'd never admit this to anyone).

She grew up as the daughter of a Lamplighter and a carpenter in the small village of Cinderhearth. Her father Edric died in a mine collapse when she was seven, and she was raised primarily by her mother Maren and the village community. She apprenticed as a Lamplighter at fifteen — not because of any grand ambition but because it was the family trade and she liked walking at dusk. She has no combat training; everything she knows about fighting she learns on the journey through trial and error.

**Dialogue Samples:**
1. *(Examining a locked door)* "Locked. Of course it's locked. Nothing in this entire world is ever just slightly ajar."
2. *(After defeating the first boss)* "I just beat a giant plant monster with a stick and a lantern. Mother would either be proud or furious. Probably both."
3. *(Talking to herself in a dark cave)* "It's fine. It's just dark. I'm a Lamplighter. Dark is literally my job. I'm fine. I'm completely fine."
4. *(Responding to Varek)* "Changed isn't alive. I'd rather light a candle every day for the rest of my life than let you blow out the sun."
5. *(To Fern, after seeing petrified villagers)* "How many? How many people are like this across Lumara?"

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 4 | Solen stands, lantern sways gently, hair ruffles |
| Walk | 6 | Lantern bobs with each step, coat sways |
| Run | 6 | Faster stride, lantern trails light particles |
| Jump | 2 | Upward launch, coat billows, lantern raised |
| Fall | 2 | Descending, coat flutters up, lantern held forward |
| Hurt | 2 | Knocked back, lantern flickers |
| Death | 4 | Collapses, lantern falls and dims to black |
| Attack | 3 | Swings lantern staff in forward arc |
| Wall Slide | 2 | Pressed against wall, sliding down, lantern held out |
| Dash | 2 | Horizontal burst, afterimage trail |
| Climb (Ladder) | 4 | Alternating hand-over-hand, lantern on back |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Teal | `#1B3A4B` | Coat, boots, hair shadow |
| Color 2 | Warm Tan | `#C8956C` | Skin, belt, staff |
| Color 3 | Amber Gold | `#F5C842` | Lantern glow, hair highlights, cape |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a young woman with short messy auburn hair, wearing a dark teal longcoat belted at the waist, cream tunic underneath, brown trousers and boots, fingerless gloves, and a faded orange half-cape on her left shoulder. She carries a tall wooden staff topped with a glowing amber brass lantern. Sprite rows: idle (4 frames), walk (6 frames), run (6 frames), jump (2 frames), fall (2 frames), hurt (2 frames), death (4 frames), attack with staff swing (3 frames), wall slide (2 frames), dash (2 frames), ladder climb (4 frames). GBC style, 4-color palette: transparent, dark teal #1B3A4B, warm tan #C8956C, amber gold #F5C842. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a young woman with short messy auburn hair, warm tan skin with freckles, amber-gold eyes, and a determined expression. Slight smirk. Dark teal collar of a longcoat visible at bottom. Faint amber glow from off-screen lantern illuminating her face from below-right. GBC style, 4-color palette: transparent, dark teal #1B3A4B, warm tan #C8956C, amber gold #F5C842. Clean pixel art, no anti-aliasing.

---

## NPCs

### Maren — Solen's Mother

**Role:** NPC, catalyst for the story, appears in prologue and endings

**Physical Description:**
Maren is in her mid-forties, tall (5'8"), with a sturdy, broad-shouldered build that comes from decades of walking mountain roads in all weather. She has long auburn hair (darker than Solen's) pulled back in a practical braid, warm brown eyes, and weathered skin with deep laugh lines. She wears the full Lamplighter uniform: a long dark teal coat like Solen's but with an orange full-cape and brass rank insignia on her lapel. Her expression is calm, warm, and steady — the face of someone who has walked dark roads so many times that the dark doesn't scare her anymore.

**Personality and Backstory:**
Maren is the emotional anchor of the story even though she appears on-screen for only a few minutes. She is patient, warm, and unflinching — the kind of person who hums while doing dangerous work. She raised Solen alone after Edric's death and never remarried. She became one of the senior Lamplighters in the Verdant Hollow and was known for never losing a lantern to the wind, no matter how bad the storm. Her decision to push Solen out of the way during the Hollow Tide surge is not heroic in the dramatic sense — it is instinctive, maternal, and utterly in character.

**Dialogue Samples:**
1. *(Opening scene, before the Hollow Tide)* "Last lantern of the night, Solen. Light it clean — a crooked flame smokes out by midnight."
2. *(During petrification)* "The lantern... keep it lit... find the Hearthstones..."
3. *(Normal ending, after being restored)* "You walked the whole road? All five?" *(pause)* "That's my girl."
4. *(True ending)* "Hearthstone or matchstick, the job's the same."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Standing, staff held upright, cape gently swaying |
| Petrifying | 4 | Stone creeps up body from feet, final frame fully petrified |
| Restored | 4 | Stone cracks and falls away, color returns, she blinks |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Teal | `#1B3A4B` | Coat, boots, braid shadow |
| Color 2 | Warm Brown | `#A0704B` | Skin, hair, belt, staff |
| Color 3 | Burnt Orange | `#D4782F` | Full cape, lantern, rank insignia |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a middle-aged woman with long auburn hair in a braid, sturdy build, wearing a dark teal longcoat with a full burnt orange cape and brass insignia. She carries a lantern staff. Sprite rows: idle (2 frames), petrifying sequence (4 frames showing stone creeping up body), restored sequence (4 frames showing stone cracking away). GBC style, 4-color palette: transparent, dark teal #1B3A4B, warm brown #A0704B, burnt orange #D4782F. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a middle-aged woman with long auburn hair in a braid, warm brown eyes, weathered skin with laugh lines, calm and steady expression. Dark teal coat collar and burnt orange cape visible. Warm lantern light on face. GBC style, 4-color palette: transparent, dark teal #1B3A4B, warm brown #A0704B, burnt orange #D4782F. Clean pixel art, no anti-aliasing.

---

### Brennan — The Village Elder

**Role:** NPC, quest-giver in the prologue

**Physical Description:**
Brennan is in his seventies, short and stooped with age, but still sharp-eyed. He has a bald head with a ring of white hair around the sides, a thick white beard, and deep-set blue eyes behind round spectacles. He wears a heavy brown robe with a faded Lamplighter sash across his chest (he was a Lamplighter in his youth). He walks with a gnarled wooden cane and has a slight tremor in his hands.

**Personality and Backstory:**
Brennan is the eldest surviving member of the Lamplighter Order in Cinderhearth. He is wise, gentle, and devastatingly honest — he will not sugarcoat the danger or pretend the odds are good. He knew Varek before the fall and considers the Hollow King's betrayal the greatest failure of his generation. He gives Solen the map and the mission not because he believes she can succeed, but because someone has to try, and she's the only one still standing with a lit lantern.

**Dialogue Samples:**
1. "I won't lie to you, child. The roads are dark, the Hearthstones are dying, and the man responsible has ten years of power on you. But you have something he lost a long time ago."
2. "Your mother's lantern still burns. That means there's still time. Take this map. The Hearthstones are marked. Relight them all and the Hollow Tide will break."
3. "I trained alongside Varek when we were young. He was brilliant. Kind, even. That's what makes this so hard."
4. *(If spoken to after returning to Cinderhearth)* "Still alive? Good. The village is holding. Barely. Go — we'll keep the home fires burning."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Standing with cane, slight sway, spectacles glint |
| Talk | 2 | Gestures with free hand, beard bobs |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Brown | `#3B2216` | Robe shadow, cane, boots |
| Color 2 | Warm Cream | `#D9C4A0` | Skin, beard, robe highlights |
| Color 3 | Faded Blue | `#5B7B99` | Eyes, sash, spectacle frames |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of an elderly man, short and stooped, bald with white side-hair and thick white beard, round spectacles, wearing a heavy brown robe with a faded blue sash across his chest. He walks with a gnarled wooden cane. Sprite rows: idle (2 frames), talking (2 frames). GBC style, 4-color palette: transparent, dark brown #3B2216, warm cream #D9C4A0, faded blue #5B7B99. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of an elderly man, bald with white side-hair, thick white beard, deep-set blue eyes behind round spectacles, wise and gentle expression. Brown robe collar visible. Warm interior light on face. GBC style, 4-color palette: transparent, dark brown #3B2216, warm cream #D9C4A0, faded blue #5B7B99. Clean pixel art, no anti-aliasing.

---

### Fern — The Herbalist

**Role:** NPC ally, World 1 (Verdant Hollow)

**Physical Description:**
Fern is seventeen, small and slight (5'1"), with a round face, large green eyes, and a messy bob of dark green hair (she dyes it with plant extracts — a quirk that makes her stand out). She has light olive skin and a perpetual smudge of dirt or plant residue on her cheek. She wears an oversized patchwork vest covered in pockets over a simple white blouse, knee-length brown shorts, and bare feet (she insists shoes dampen her "root sense," which is not a real thing, but she believes it deeply). She carries a woven basket overflowing with herbs, mushrooms, and stoppered vials.

**Personality and Backstory:**
Fern is cheerful, talkative, and slightly scatterbrained — the kind of person who will interrupt a conversation about mortal danger to point out a rare mushroom. She's an orphan raised by the herbalist guild in a neighboring village and was on a plant-gathering expedition when the Hollow Tide struck. She survived by hiding in a hollow tree and covering herself in strongbark sap, which the shadow creatures avoid because of its bitter scent. She is braver than she appears and fiercely loyal once she decides someone is a friend, which she does almost instantly.

**Dialogue Samples:**
1. "Oh! A person! A real, not-stone, not-shadow person! I haven't seen one in four days! I'm Fern. Please don't be a hallucination."
2. "Here, take this. It's a healing tincture — bitterbark and moonpetal extract. Tastes like dirt and regret, but it'll close a wound in seconds."
3. "You can't carry them all at once. But you can carry the light to the next stone. And the next. That's how lamplighters work, isn't it? One lantern at a time."
4. "The Thornveil Thicket? Oh, it's terrible. Thorns as long as your arm, vines that grab, pollen that makes you sneeze for an hour. I love it in there."
5. *(If revisited later)* "Solen! You're alive! The forest is coming back — I found three new mushroom species this morning. Three! The Hollow Tide was terrible for people but apparently great for fungi."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Bouncing slightly on bare feet, basket on arm |
| Talk | 2 | Gestures excitedly with both hands, basket swings |
| Give Item | 2 | Reaches into basket, holds out a vial |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Forest Green | `#1E3B2C` | Hair, vest shadow, basket |
| Color 2 | Light Olive | `#A8B87A` | Skin, blouse, herb highlights |
| Color 3 | Warm Brown | `#8B6D4B` | Vest, shorts, basket, dirt smudge |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a small teenage girl with a messy bob of dark green hair, round face, large eyes, wearing an oversized patchwork vest with many pockets over a white blouse, knee-length brown shorts, bare feet. She carries a woven basket full of herbs. Sprite rows: idle (2 frames bouncing on feet), talking (2 frames gesturing), give item (2 frames). GBC style, 4-color palette: transparent, dark forest green #1E3B2C, light olive #A8B87A, warm brown #8B6D4B. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a young girl with messy dark green bob hair, large bright green eyes, round face, light olive skin with a dirt smudge on her cheek, cheerful excited expression, slight open-mouth smile. Patchwork vest collar visible. Soft forest light. GBC style, 4-color palette: transparent, dark forest green #1E3B2C, light olive #A8B87A, warm brown #8B6D4B. Clean pixel art, no anti-aliasing.

---

### Orin — The Retired Lamplighter

**Role:** NPC ally, World 2 (Frostfang Peaks)

**Physical Description:**
Orin is in his sixties, tall and gaunt with a weathered, craggy face. He has long gray hair pulled into a loose ponytail, a short salt-and-pepper beard, and sharp, pale blue eyes that look perpetually angry (he's usually just squinting against the cold). He wears a battered old Lamplighter coat that has been patched so many times it's more patch than coat, heavy fur-lined boots, and a thick wool scarf wrapped several times around his neck. He carries no lantern staff — he broke his years ago in a fit of despair and never replaced it.

**Personality and Backstory:**
Orin is bitter, gruff, and deeply guilt-ridden. He was Varek's mentor in the Lamplighter Order, and he blames himself for not recognizing the signs of Varek's radicalization. When Varek began extinguishing Hearthstones, Orin didn't fight — he ran. He retreated to a cabin on the Frostfang Peaks and has lived in self-imposed exile for years, convinced that he failed the world and that nothing he does can fix it. Meeting Solen forces him to confront his guilt: she is doing exactly what he should have done, and she's half his age with a fraction of his experience.

**Dialogue Samples:**
1. "Another Lamplighter? Thought you were all dead or turned to stone. You're either very brave or very stupid. Same thing, really."
2. "Varek was my student. My best student. I taught him everything — how to read the wind, how to keep a flame steady in a blizzard, how to listen to the Hearthstones. And he used all of it to snuff them out. That's my legacy."
3. "Take my old climbing gear. I don't need it anymore — I'm not going anywhere. And before you ask, no, I'm not coming with you. I've done enough damage."
4. *(If revisited after World 3)* "You're still going? Even after what that shadow told you — that Varek's been using you? ... Heh. You're more stubborn than your mother. She was the same way. Maren never could let a dark road stay dark."
5. "I failed Varek. I failed the Order. But maybe I don't have to fail you. Here — this is the path to the summit. Watch the wind on the east face. It'll throw you right off the edge."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Standing with arms crossed, scarf blowing in wind |
| Talk | 2 | Uncrosses arms, gestures dismissively |
| Give Item | 2 | Reaches behind him, tosses item to Solen |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Slate | `#2D3848` | Coat, boots, hair shadow |
| Color 2 | Pale Gray | `#B0BEC5` | Skin, hair, scarf |
| Color 3 | Icy Blue | `#78B8D4` | Eyes, coat patches, highlights |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a tall gaunt elderly man with long gray hair in a ponytail, short salt-and-pepper beard, wearing a heavily patched dark Lamplighter coat, fur-lined boots, thick wool scarf wrapped around neck. Arms crossed, surly expression. Sprite rows: idle (2 frames, scarf blowing), talking (2 frames gesturing), give item (2 frames tossing). GBC style, 4-color palette: transparent, dark slate #2D3848, pale gray #B0BEC5, icy blue #78B8D4. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a gaunt elderly man with long gray hair, short beard, sharp pale blue eyes, craggy weathered face, scowling expression hiding sadness underneath. Dark patched coat collar and wool scarf visible. Cold mountain light on face. GBC style, 4-color palette: transparent, dark slate #2D3848, pale gray #B0BEC5, icy blue #78B8D4. Clean pixel art, no anti-aliasing.

---

### Coral — The Salvager

**Role:** NPC ally, World 3 (Sunken Brine)

**Physical Description:**
Coral is in her late twenties, medium height (5'5"), with a muscular swimmer's build. She has dark brown skin, close-cropped black hair, and bright hazel eyes that seem to catch light even in dark caverns. She wears a fitted diving suit made of treated leather — dark blue-green with lighter panels — and a brass-and-glass diving mask pushed up onto her forehead. Around her neck hangs a collection of trinkets on cords: shells, gears, small crystals — salvage trophies. She has a wide, easy smile and a scar across her left cheekbone from a close encounter with a cave eel.

**Personality and Backstory:**
Coral is the emotional counterpoint to the game's melancholy — she is genuinely happy, even in terrible circumstances. She has lived in the Sunken Brine ruins for years, long before the Hollow Tide, exploring and cataloguing First Keeper artifacts for a university that probably doesn't exist anymore. She loved someone — a fellow diver named Tomas — who was lost in the deep ruins two years ago. She still wears his locket (now empty; the portrait inside was water-damaged and she wants to find a replacement). Coral's cheerfulness is not denial; it's a conscious choice. She knows the world is ending. She just refuses to be miserable about it.

**Dialogue Samples:**
1. "A surface-dweller! In my ruins! This is the best day I've had since the cavern ceiling didn't collapse on Tuesday. I'm Coral. Welcome to the wet and deeply unsafe Sunken Brine."
2. "I need to find Tomas's locket — the real one, the one I dropped in the Keeper cathedral when the floor gave way. It's not about the locket, really. It's about... finishing something. You know?"
3. "The water's safe to swim in. Probably. The glowing fish are harmless. The non-glowing ones... stay away from the non-glowing ones."
4. "Varek's research chamber is down there. I've read his journals. He's not mad — that's what's scary. He's completely, terrifyingly rational."
5. *(If revisited later)* "The Brine is clearing up beautifully since you relit the Hearthstone. I found three new chambers yesterday. Also, I found the locket. Thanks for the help down there — I owe you one. Or several."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Standing with diving mask on forehead, trinkets swaying |
| Talk | 2 | Smiling, gesturing with both hands |
| Swim | 4 | Breaststroke animation, mask down |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Sea Blue | `#0E3250` | Diving suit shadow, hair |
| Color 2 | Dark Brown | `#6B4832` | Skin, leather, trinkets |
| Color 3 | Aqua Teal | `#48C8B0` | Suit highlights, mask glass, water reflections |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a muscular woman with dark brown skin, close-cropped black hair, wearing a fitted dark blue-green diving suit with lighter panels, brass-and-glass diving mask pushed onto forehead, collection of trinkets on cords around neck. Wide smile, scar on left cheek. Sprite rows: idle (2 frames), talking (2 frames), swimming breaststroke (4 frames). GBC style, 4-color palette: transparent, deep sea blue #0E3250, dark brown #6B4832, aqua teal #48C8B0. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a woman with dark brown skin, close-cropped black hair, bright hazel eyes, wide easy smile, scar across left cheekbone. Brass diving mask frame visible on forehead, trinkets on cords at neck. Underwater blue-green light on face. GBC style, 4-color palette: transparent, deep sea blue #0E3250, dark brown #6B4832, aqua teal #48C8B0. Clean pixel art, no anti-aliasing.

---

### Wrench — The Mechanist

**Role:** NPC ally, World 4 (Cinderforge Depths)

**Physical Description:**
Wrench is in his fifties, short and stocky (4'10"), with a barrel chest and arms thick from decades of forge work. He has ruddy, soot-stained skin, a bushy red-gray beard braided into two forks, small dark eyes behind thick brass goggles pushed up on his forehead, and a bald head covered in burn scars. He wears heavy leather overalls with metal rivets, thick gloves (one of which has mechanical finger extensions for fine work), and steel-toed boots. He carries a massive wrench (his namesake and weapon) slung over one shoulder.

**Personality and Backstory:**
Wrench is gruff, pragmatic, and privately terrified. He masks his fear with competence — as long as he's fixing something, he doesn't have to think about the shadow creatures outside his barricade. He was the head mechanist of the Cinderforge mining operation and was underground when the Hollow Tide consumed the depths. He survived by sealing himself in a maintenance bay and rigging mining turrets to shoot anything that moved. He has been alone for weeks and is deeply relieved to see Solen, though he would rather swallow hot slag than admit it.

He knew Solen's father Edric. They worked the same mine. Wrench signed off on the tunnel inspection that led to the collapse — a decision that has haunted him for twelve years. Giving Solen the unfinished figurine Edric was carving is his attempt at atonement.

**Dialogue Samples:**
1. "Who— how did you get past my turrets?! ... Oh. They ran out of ammo three days ago, didn't they. Well, that's terrifying."
2. "The forges are overrun. Shadow things everywhere — used to be miners, some of them. I don't like to think about that part. You want to get to the Hearthstone? Fine. Help me clear my escape route first."
3. "I knew your father. Edric. Good man. Good hands — could feel a weak beam just by touching it. I should have listened to him about that tunnel."
4. "He was carving this for you. A little wooden lantern. Kept it in his pocket. I... I found it after. Never could figure out who to give it to. Guess now I know."
5. *(If revisited later)* "Forges are running again. First thing I made? A new turret. Second thing? A lock for the door. I'm not getting trapped down here twice."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 2 | Standing with wrench on shoulder, goggles glinting |
| Talk | 2 | Points with wrench, beard bobs |
| Work | 4 | Hammering at an anvil or turning a valve |
| Give Item | 2 | Reaches into overalls, extends hand with item |

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Iron | `#2C1E14` | Overalls shadow, boots, goggles frame |
| Color 2 | Ruddy Tan | `#B87844` | Skin, beard, leather |
| Color 3 | Forge Orange | `#E8752A` | Forge glow, rivets, goggles lens, wrench |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a short stocky man with ruddy soot-stained skin, bushy red-gray forked beard, bald head with burn scars, thick brass goggles on forehead, wearing heavy leather overalls with metal rivets, thick gloves with mechanical finger extensions, steel-toed boots. Carries a massive wrench over one shoulder. Sprite rows: idle (2 frames), talking (2 frames), working at anvil (4 frames), give item (2 frames). GBC style, 4-color palette: transparent, dark iron #2C1E14, ruddy tan #B87844, forge orange #E8752A. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a stocky man with ruddy soot-stained skin, bushy red-gray forked beard, small dark eyes, thick brass goggles pushed up on bald head with burn scars, gruff expression hiding worry. Leather overalls collar and metal rivets visible. Warm orange forge light on face. GBC style, 4-color palette: transparent, dark iron #2C1E14, ruddy tan #B87844, forge orange #E8752A. Clean pixel art, no anti-aliasing.

---

### Shade / Aldric — The Shadow Agent

**Role:** Recurring antagonist NPC, mini-boss in World 5

**Physical Description:**
As Shade: a tall, lean figure wrapped entirely in a dark purple-black cloak with a featureless white mask covering the face. Only sharp, glowing violet eyes are visible through the mask's eye slits. The cloak seems to move independently, as if made of living shadow — tendrils of darkness drift off the hem and shoulders like smoke.

As Aldric (unmasked): a man in his thirties with gaunt, hollow features. He has lank black hair, sunken dark eyes with faint purple veins radiating from the corners, and pale skin stretched tight over sharp cheekbones. He wears a corrupted Lamplighter uniform — the same dark teal coat, but the orange cape has turned black and the brass insignia has tarnished to a dull purple.

**Personality and Backstory:**
Aldric was a Lamplighter who served alongside Maren. He was quiet, thoughtful, and idealistic — he joined the Order because he believed in protecting people. When Varek revealed the truth about the Hearthstones, Aldric's idealism cracked. He couldn't bear the idea that the Order he'd devoted his life to was maintaining a prison. He joined Varek not out of malice but out of disillusionment. The Hollow's corruption has been slowly consuming him; by the time Solen fights him, he is more shadow than man, held together by willpower and bitterness.

**Dialogue Samples:**
1. *(World 3 reveal)* "Surprised? You shouldn't be. Every Hearthstone you relight sends a pulse of energy through the ley lines — and Varek is waiting at the other end with open hands. You've been feeding him, Lamplighter."
2. *(World 5, before fight)* "I didn't want this fight, Solen. But you won't stop, and he needs time. I'll give him that much."
3. *(Dying)* "He's not wrong about the chains, Solen. He's just wrong about what happens when you break them."

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle (Shade) | 4 | Cloak billows, shadow tendrils drift, eyes glow |
| Walk (Shade) | 4 | Glides forward, cloak trailing |
| Attack (Shade) | 3 | Shadow tendril lash from cloak |
| Dodge (Shade) | 2 | Dissolves into shadow, reappears |
| Unmasked | 2 | Mask shatters, reveals Aldric's face |
| Death | 4 | Shadow drains away, Aldric collapses |

**Sprite Size:** 16×16 px (standard) as Shade; 16×16 px as Aldric

**Palette (Shade form):**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Deep Purple-Black | `#1A0A2E` | Cloak body, shadow tendrils |
| Color 2 | Dark Violet | `#5B2D8E` | Cloak highlights, mask edges |
| Color 3 | Ghost White | `#E0D8F0` | Mask face, eye glow |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel character sprite of a tall cloaked figure wrapped in a dark purple-black cloak that moves like living shadow, wearing a featureless white mask with glowing violet eyes visible through slits. Shadow tendrils drift from cloak edges. Sprite rows: idle (4 frames cloak billowing), walk/glide (4 frames), attack with shadow tendril lash (3 frames), dodge/dissolve (2 frames), mask shattering reveal (2 frames), death collapse (4 frames). GBC style, 4-color palette: transparent, deep purple-black #1A0A2E, dark violet #5B2D8E, ghost white #E0D8F0. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait (Shade masked):**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up of a featureless white mask with narrow eye slits showing glowing violet eyes. Dark purple-black cloak hood frames the mask, shadow tendrils wisping off edges. Ominous dark background. GBC style, 4-color palette: transparent, deep purple-black #1A0A2E, dark violet #5B2D8E, ghost white #E0D8F0. Clean pixel art, no anti-aliasing.

---

### Varek — The Hollow King

**Role:** Primary antagonist, final boss

**Physical Description:**
Varek is in his early fifties but looks older — the Hollow has aged him. He is tall (6'1") and gaunt, almost skeletal, with sharp features and hollow cheeks. His skin is deathly pale with visible purple-black veins running beneath the surface, especially along his neck, temples, and hands. His hair is long, white, and unkempt, falling past his shoulders. His eyes are solid violet — no iris, no pupil, just flat glowing purple light. He wears a corrupted version of the Lamplighter Grand Keeper robe: originally white and gold, now stained to deep purple and black. A crown of crystallized shadow sits on his brow — jagged, asymmetrical, like frozen lightning. When he speaks, his voice has a faint echo, as if a second, deeper voice is speaking half a beat behind him.

**Personality and Backstory:**
Varek was the most brilliant Lamplighter of his generation — a prodigy who understood the Hearthstones on an intuitive level. He could feel their pulse, hear their hum, and sense when they were weakening. This sensitivity is what led him to the First Keeper ruins in the Sunken Brine, where he discovered the truth: the Hearthstones were not benevolent gifts but chains forged to imprison the Hollow, a vast consciousness that predated Lumara itself.

The discovery broke something in Varek. He could not reconcile the Order's mission ("protect the light") with the reality ("maintain the prison"). He spent years trying to find a compromise and failed. Eventually, the Hollow began speaking to him — not in words, but in feelings: images of a world without fear, without fragile crystals, without the constant anxiety of the next dimming. The Hollow offered permanence. Shadow doesn't burn out. Shadow doesn't need fuel. Shadow simply is.

Varek is not evil in the traditional sense. He is a man who found a real problem and chose the worst possible solution. He genuinely believes he is liberating the world. The tragedy is that he's partially right about the problem — the Hearthstones are an imperfect, fragile system — but catastrophically wrong about the solution.

**Dialogue Samples:**
1. "Ah, the little Lamplighter. Maren's daughter, yes? I knew her. She was the best of us. She understood the Hearthstones better than anyone — she just couldn't take the final step."
2. "You've reignited four Hearthstones. Impressive. And each one sent a pulse of energy directly to me. Did you know that? Every light you've lit has made my darkness stronger. There's a poetry in it."
3. "I'm not your enemy, Solen. The Hearthstones are. They're chains — beautiful, warm chains, but chains all the same. I'm offering freedom."
4. "What happens when the Hearthstones dim again? In a hundred years? In ten? Will there be another Lamplighter brave enough to walk the dark roads? Or will the light just... quietly go out, and everyone will pretend they didn't notice?"
5. *(Final phase, weakened)* "The Hollow... it promised... it said the world would be free... why does it feel like falling?"

**Animation States:**

| State | Frames | Description |
|---|---|---|
| Idle | 4 | Floating slightly, robe billowing, shadow tendrils orbit |
| Walk | 4 | Glides, feet barely touching ground |
| Attack — Shadow Bolt | 3 | Extends hand, fires bolt of purple energy |
| Attack — Hollow Wave | 4 | Slams ground, wave of shadow radiates outward |
| Attack — Summon | 3 | Raises arms, shadow creatures emerge from floor |
| Phase Transition | 4 | Absorbs shadow energy, grows larger, crown expands |
| Hurt | 2 | Flinches, shadow armor cracks showing light beneath |
| Defeat | 6 | Shadow drains, Varek shrinks to human size, collapses |

**Sprite Size:** 16×32 px (tall) — Phase 1; 16×32 px — Phase 2

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Abyssal Black | `#0D0221` | Robe body, shadow tendrils, crown |
| Color 2 | Deep Violet | `#6A1B9A` | Robe highlights, veins, energy effects |
| Color 3 | Pale Bone | `#E8D8C8` | Skin, hair, crack-light in defeat |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x32 pixel tall character sprite of a gaunt skeletal man with long white unkempt hair, deathly pale skin with visible purple-black veins, solid glowing violet eyes with no pupils, wearing a flowing corrupted robe — deep purple and black — with a jagged crown of crystallized shadow on his brow. Shadow tendrils orbit his body. He floats slightly above the ground. Sprite rows: idle floating (4 frames), glide walk (4 frames), shadow bolt attack (3 frames), ground slam hollow wave (4 frames), summon creatures (3 frames), phase transition growing larger (4 frames), hurt with cracks showing light (2 frames), defeat sequence collapsing (6 frames). GBC style, 4-color palette: transparent, abyssal black #0D0221, deep violet #6A1B9A, pale bone #E8D8C8. Clean pixel art, no anti-aliasing, indexed color.

**PIXEL ART GENERATION PROMPT — 16×16 Dialogue Portrait:**
> Pixel art 16x16 portrait for Game Boy Color dialogue box. Close-up face of a gaunt man with long white hair, deathly pale skin with purple-black veins along temples and neck, solid glowing violet eyes with no iris or pupil, hollow cheeks, thin lips in a calm almost gentle expression. Jagged crystallized shadow crown on brow. Dark purple robe collar visible. Eerie violet glow from eyes illuminating face. GBC style, 4-color palette: transparent, abyssal black #0D0221, deep violet #6A1B9A, pale bone #E8D8C8. Clean pixel art, no anti-aliasing.

---

## Supporting Characters (Non-Speaking)

### Petrified Villagers

**Role:** Environmental storytelling, background NPCs

**Physical Description:** Generic villager sprites frozen in mid-action — reaching, running, shielding children. Rendered in a gray-stone palette to indicate petrification.

**Sprite Size:** 16×16 px (standard)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Stone | `#3C3C3C` | Shadow areas |
| Color 2 | Medium Stone | `#808080` | Body, clothing |
| Color 3 | Light Stone | `#C0C0C0` | Highlights, faces |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art spritesheet for a Game Boy Color platformer. 16x16 pixel sprites of petrified stone villagers in various frozen poses: one reaching forward, one running, one shielding a child, one looking up in fear. Each is a single static frame. They look like stone statues of ordinary people caught mid-motion. GBC style, 4-color palette: transparent, dark stone #3C3C3C, medium stone #808080, light stone #C0C0C0. Clean pixel art, no anti-aliasing, indexed color.

---

### Edric's Figurine (Item Sprite)

**Role:** Key item, story object

**Physical Description:** A tiny carved wooden lantern, about 2 inches tall in-world. The carving is clearly hand-done — slightly rough, with visible knife marks. It's unfinished in the main game; in the true ending post-credits scene, it appears completed and sits on a mantelpiece.

**Sprite Size:** 8×16 px (small)

**Palette:**

| Slot | Color | Hex | Usage |
|---|---|---|---|
| Color 0 | Transparent | — | Background |
| Color 1 | Dark Wood | `#4A3020` | Shadow, knife marks |
| Color 2 | Light Wood | `#C8A878` | Body of figurine |
| Color 3 | Amber | `#F5C842` | Lantern glow detail (finished version) |

**PIXEL ART GENERATION PROMPT — Spritesheet:**
> Pixel art sprite for a Game Boy Color platformer. 8x16 pixel small item sprite of a tiny carved wooden lantern figurine. Hand-carved look with visible rough edges. Two versions side by side: unfinished (rough, no glow) and finished (smooth, amber glow in lantern window). GBC style, 4-color palette: transparent, dark wood #4A3020, light wood #C8A878, amber #F5C842. Clean pixel art, no anti-aliasing, indexed color.
