# 03 — Characters

---

## Player Character: Edyn

### Identity

| Field | Detail |
|-------|--------|
| Name | Edyn |
| Role | Protagonist, Clockmaker's Apprentice |
| Age | 17 |
| Hometown | Millhaven, Verdant Reach |
| Relationship | Player-controlled character |

### Physical Description

Edyn has short, tousled auburn hair and large, determined green eyes. They wear a cream-colored linen shirt under a dark brown leather vest with brass buckles. Their trousers are olive green, tucked into scuffed brown boots. A belt at their waist holds a small pouch of clockwork tools and the pocket watch on a brass chain. Their build is lean and wiry—not a fighter's physique, but someone used to precise, dexterous work. A pair of brass-rimmed goggles rests on their forehead (a gift from Alaric, used for fine detail work). Their expression defaults to focused determination.

### Personality, Backstory, and Motivation

Edyn is stubborn, resourceful, and emotionally guarded. They lost their parents at age six and were raised by Alaric, the town clockmaker. This upbringing gave them exceptional mechanical aptitude but also a deep fear of abandonment. They deflect emotional vulnerability with dry humor and a tendency to focus on the task at hand rather than discuss feelings.

Their motivation is singular: find Alaric and bring him home. The world-saving is incidental. Over the course of the journey, Edyn grows to accept that they care about more than just Alaric—they care about Lira, Rook, the people of Stormhaven, the Keepers—but they never fully let go of the personal core of their quest.

### Stats

| Stat | Starting | Max (Lv 30) |
|------|----------|-------------|
| HP | 28 | 180 |
| ATK | 8 | 52 |
| DEF | 6 | 40 |
| SPD | 10 | 55 |
| MP | 12 | 65 |

Edyn is a balanced character with a slight lean toward speed. Their Aether abilities (channeled through the pocket watch) provide utility and moderate damage.

### Dialogue Samples

1. **Greeting (to NPCs):** "I'm Edyn, from Millhaven. I'm looking for someone—have you seen an older man, gray hair, always smells like machine oil?"
2. **Quest Give (self-motivation):** "The compass says north. Through the marsh. ...Great. Alaric, you'd better be worth the mud in my boots."
3. **Quest Complete (restoring a Meridian):** "That's three. Two more cores, and the Chronospire opens. Hold on, Alaric. I'm getting closer."
4. **Lore (examining Architect ruins):** "These gears haven't turned in a thousand years, but the mechanism is flawless. Whoever built this... they understood time the way I understand clockwork. No—better."
5. **Emotional Moment (after Alaric's rescue):** "I kept telling myself I'd know what to say when I found you. But I don't. I just... I wasn't going to leave you here. That's all."
6. **Battle (low HP):** "Not yet. I didn't come this far to stop now."
7. **Interacting with the Pocket Watch:** "Still ticking. Still ticking. That's all I need."

### Animation States

- Idle: 4 directions (N, S, E, W) — standing, slight breathing animation
- Walk: 4 directions (N, S, E, W) — 2-frame walk cycle per direction
- Interact: Holding up pocket watch (single direction, facing forward)
- Hurt: Flinch animation (1 frame, slight recoil)

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#2B1B0E` (dark brown), `#D4A847` (brass/gold), `#7BAE5E` (olive green), `#F5E6C8` (cream) |

### Portrait Description (16x16px)

A close-up of Edyn's face: auburn hair swept to the right, green eyes, slight smirk. Brass goggles visible on forehead. Brown vest collar visible at bottom edge. Cream shirt beneath. Expression is determined but approachable.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG protagonist. Young character with short auburn hair, brass goggles on forehead, cream shirt, dark brown leather vest with brass buckles, olive green trousers, brown boots. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). Additional row for interact animation (holding up a glowing pocket watch). GBC color palette: dark brown #2B1B0E, brass gold #D4A847, olive green #7BAE5E, cream #F5E6C8. Clean pixel art style, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for a Game Boy Color RPG dialogue box. Close-up face of a young character with short auburn hair, green eyes, brass goggles on forehead, slight determined smile. Brown vest collar visible. GBC palette: #2B1B0E, #D4A847, #7BAE5E, #F5E6C8. Clean pixel art, no anti-aliasing, black outline."

---

## Party Member: Lira

### Identity

| Field | Detail |
|-------|--------|
| Name | Lira |
| Role | Party Member — Healer/Support |
| Age | 19 |
| Hometown | Boghollow, Ashenveil Marsh |
| Relationship | Companion, joins in Act 1 at Oakwatch Grove |

### Physical Description

Lira has long dark hair tied in a loose braid, with a few small wildflowers woven into it. Her skin is a warm brown. She wears a deep teal tunic over a pale lavender undershirt, with a wide leather belt holding herb pouches. Her skirt is dark gray, and she wears leather sandals wrapped with cloth ties up to mid-calf. She carries a gnarled wooden staff topped with a small Aether crystal that glows faintly. Her eyes are dark brown and kind, with visible worry lines despite her youth.

### Personality, Backstory, and Motivation

Lira is a traveling herbalist and healer from the Ashenveil Marsh, trained by her grandmother in traditional medicine enhanced with minor Aether crystal applications. She is compassionate to a fault—she cannot ignore suffering, even when helping would put her at risk. She is also anxious and prone to overthinking, which manifests as quiet muttering and fidgeting with her herb pouches.

She was traveling through the Verdant Reach when the Shattering hit, searching for her younger brother Pip, who was apprenticed to a merchant ship heading to Stormhaven. After finding Pip safe in Stormhaven, she stays with Edyn because she believes her healing skills are needed and because, quietly, she has found in Edyn a purpose larger than herself.

### Stats

| Stat | Starting | Max (Lv 30) |
|------|----------|-------------|
| HP | 22 | 140 |
| ATK | 5 | 30 |
| DEF | 5 | 35 |
| SPD | 8 | 45 |
| MP | 18 | 85 |

Lira has the highest MP in the party and access to the strongest healing abilities. Her ATK is low; she relies on Aether-based support magic.

### Dialogue Samples

1. **Greeting:** "Hello! I'm Lira—I'm a healer, if you need one. I have poultices, tinctures, and a very persistent need to make sure everyone around me is okay."
2. **Quest Give:** "My brother Pip was on a ship to Stormhaven. The harbor's locked down because of the storm loop. I have to find him—please, can we go there next?"
3. **Quest Complete (finding Pip):** "Pip! Oh, thank the tides. You're safe. Don't you EVER get on a boat without telling me again, do you hear me?"
4. **Lore (examining marsh ruins):** "My grandmother told stories about the old builders—the ones who made the towers. She said they left because the world got too small for them. I always thought it was just a fairy tale."
5. **Emotional Moment (Ashenveil Marsh breakdown):** "I watched a fox give birth and die of old age in the same minute. I couldn't... I couldn't do anything. What's the point of being a healer if time takes everything anyway?"
6. **Battle (casting heal):** "Hold still—I've got you."
7. **To Vasael (true ending):** "You're right that we can't save everyone. But you stopped trying, and that's not the same as there being no way."

### Animation States

- Idle: 4 directions — standing, staff at side
- Walk: 4 directions — 2-frame walk cycle, braid swaying
- Interact: Raising staff with crystal glowing
- Heal Cast: Staff raised overhead, crystal flashes (battle animation)

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#1A3A3A` (dark teal), `#5EC4B8` (light teal), `#C8A2D4` (lavender), `#F2E8D5` (pale cream) |

### Portrait Description (16x16px)

Lira's face: warm brown skin, dark brown eyes with a gentle expression, long dark braid falling over one shoulder with tiny flowers in it. Teal collar visible. Slight, worried smile.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG healer party member. Young woman with long dark braided hair with small flowers, warm brown skin, deep teal tunic, lavender undershirt, dark gray skirt, leather sandals, carrying a gnarled wooden staff with a small glowing blue-white crystal on top. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). Additional row for interact and heal cast animations. GBC palette: #1A3A3A, #5EC4B8, #C8A2D4, #F2E8D5. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Young woman, warm brown skin, dark brown eyes, gentle worried expression, long dark braid with tiny flowers over one shoulder, teal tunic collar visible. GBC palette: #1A3A3A, #5EC4B8, #C8A2D4, #F2E8D5. Clean pixel art, no anti-aliasing, black outline."

---

## Party Member: Rook

### Identity

| Field | Detail |
|-------|--------|
| Name | Rook |
| Role | Party Member — Tank/Physical DPS |
| Age | 28 |
| Hometown | Ironpeak Enclave |
| Relationship | Companion, joins in Act 2 at Ashenveil Marsh |

### Physical Description

Rook is broad-shouldered and stocky, with a square jaw and a permanent scowl. He has short-cropped black hair and a scar running from his left temple to his jawline. His skin is pale, weathered by mountain cold. He wears a heavy dark iron-gray coat with riveted shoulders over a rust-red shirt. His trousers are dark brown, tucked into steel-toed boots. He carries a large wrench-like weapon—a miner's pick modified for combat, with a gear mechanism that allows the head to shift for different attack types. A small Ironpeak Enclave insignia (a gear within a mountain silhouette) is stitched onto his coat but partially ripped—he tore it half off after his discharge.

### Personality, Backstory, and Motivation

Rook is blunt, cynical, and protective despite himself. He was a soldier in the Ironpeak Enclave's defense corps, assigned to a scouting mission in the Ashenveil Marsh that went catastrophically wrong due to bad intelligence from his commanding officer, Haldric. Several members of Rook's squad were killed. Rook was blamed and discharged. The Enclave sent him back to the marsh on a "recovery mission"—retrieve Architect tech from the Hollow Meridian—knowing the mission was likely suicide.

Rook doesn't trust institutions, authority, or optimism. He trusts competence. He begins to respect Edyn not because of their idealism but because Edyn keeps solving problems that should be impossible. Over time, Rook's cynicism cracks, and he admits that traveling with Edyn's group is the first time he's felt like he belongs since his squad.

### Stats

| Stat | Starting | Max (Lv 30) |
|------|----------|-------------|
| HP | 35 | 220 |
| ATK | 12 | 65 |
| DEF | 10 | 58 |
| SPD | 5 | 30 |
| MP | 6 | 30 |

Rook has the highest HP and ATK. He is slow and has minimal MP, relying on physical attacks and a single defensive ability (Iron Guard: reduces damage taken for one turn).

### Dialogue Samples

1. **Greeting:** "Name's Rook. No, I don't want to talk about it. You need muscle, I need a guide through this swamp. That's the deal."
2. **Quest Give:** "The Enclave wants a power cell from the Hollow Meridian. It's deep in the marsh, probably guarded by something awful. You're going that way anyway, right? Convenient."
3. **Quest Complete (retrieving the cell):** "Got it. One Architect energy cell, intact. The Enclave can choke on their gratitude for all I care, but a deal's a deal."
4. **Lore (in the Ironpeak Enclave):** "I grew up in these tunnels. The sound of hammers on steel—that's what home sounds like. Or it used to."
5. **Emotional Moment (standing up to Haldric):** "I followed your orders, Haldric. Every single one. And people died because you couldn't be bothered to verify your own intel. I'm done following. I'm done apologizing."
6. **Battle (taking heavy damage):** "That all you've got? I've been hit harder by falling rocks."
7. **To Edyn (Chronospire approach):** "For what it's worth, kid... you're the most annoyingly persistent person I've ever met. Don't stop now."

### Animation States

- Idle: 4 directions — standing with weapon resting on shoulder
- Walk: 4 directions — 2-frame heavy walk cycle
- Interact: Slamming wrench-pick into ground
- Attack: Overhead swing (battle animation)

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#3A3A40` (iron gray), `#8B3A2A` (rust red), `#C0B090` (pale tan), `#1A1A1E` (near black) |

### Portrait Description (16x16px)

Rook's face: pale skin, square jaw, scar from left temple to jaw, short black hair, permanent scowl, dark iron-gray coat collar with riveted shoulder detail visible. Rust-red shirt beneath. Expression is stern and guarded.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG tank/warrior party member. Stocky man with short black hair, scar on left face, iron-gray heavy coat with riveted shoulders, rust-red shirt, dark brown trousers, steel-toed boots, carrying a large modified miner's pick weapon. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). Additional row for attack animation (overhead swing). GBC palette: #3A3A40, #8B3A2A, #C0B090, #1A1A1E. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Stocky man's face, pale skin, square jaw, facial scar from left temple to jawline, short black hair, scowling expression, iron-gray coat collar with metal rivets. GBC palette: #3A3A40, #8B3A2A, #C0B090, #1A1A1E. Clean pixel art, no anti-aliasing, black outline."

---

## Support Character: Sable

### Identity

| Field | Detail |
|-------|--------|
| Name | Sable |
| Role | Support Character — Non-Combat Merchant/Advisor |
| Age | 21 |
| Hometown | Nomadic (Crystalfall Desert trade routes) |
| Relationship | Joins party in Act 2 at Crystalfall Desert |

### Physical Description

Sable has sandy blonde hair cut short and practical, with a brightly colored scarf (orange and gold) wrapped around her neck and lower face to keep out desert sand. Her eyes are hazel. She wears a long sandy-tan traveling coat with many pockets over a burnt orange tunic. Her boots are high-laced desert walkers in dark tan leather. She carries a large merchant's satchel covered in patches from various trade stops.

### Personality, Backstory, and Motivation

Sable is cheerful, talkative, and relentlessly curious. She was raised by a merchant caravan family that travels the desert trade routes, and she has an encyclopedic knowledge of Aether Crystals, regional currencies, and gossip. She talks constantly—a defense mechanism against the loneliness of desert travel. She is deeply practical and has no combat training, but her knowledge of items, prices, and trade routes makes her invaluable as a party advisor.

She joins the party after being unfrozen in the Crystalfall Desert, initially because Edyn's time bubble is the only way she can move. She stays because she genuinely likes the group and because, as a merchant, she recognizes the economic devastation the Shattering has caused—if the world doesn't get fixed, there won't be anyone left to trade with.

### Stats

Sable does not participate in combat. She provides passive bonuses:
- **Haggle:** 15% discount at all shops when Sable is in the party
- **Appraise:** Reveals hidden item stats and identifies unknown items
- **Caravan Network:** Unlocks fast travel between previously visited towns (after Act 2)

### Dialogue Samples

1. **Greeting:** "Sable! Merchant extraordinaire, crystal connoisseur, and the only person in this party who knows how to negotiate! At your service!"
2. **Quest Give:** "That shop in Ironpeak is selling Conduit Blades for twice what they're worth. If we bring them some raw Aether from the desert, I bet I can talk them down."
3. **Quest Complete:** "See? That's the art of the deal. We got the blade, they got the crystal, everybody's happy. Mostly me, but still."
4. **Lore (examining Aether Crystals):** "Premium grade, naturally formed. See how the lattice catches the light? That's at least a thousand years of slow crystallization. Worth more than this whole town, probably. Don't tell anyone I said that."
5. **Emotional Moment (after being unfrozen):** "How long was I frozen? It felt like... nothing. No dreams, no thoughts, just nothing. That's what scares me. Not dying—just stopping."
6. **At camp:** "Who wants trail rations? I traded for some spiced jerky two towns back. It's not gourmet, but it's better than whatever Rook calls cooking."
7. **At a shop:** "Let me handle this. You'll pay three times what it's worth if I let you talk to the shopkeeper alone."

### Animation States

- Idle: 4 directions — standing with satchel, scarf blowing slightly
- Walk: 4 directions — 2-frame walk cycle, satchel bouncing
- Interact: Opening satchel and examining an item

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#D4A44B` (sandy gold), `#E86A20` (burnt orange), `#F5E6C8` (cream/sand), `#5C3A1E` (dark brown) |

### Portrait Description (16x16px)

Sable's face: sandy blonde short hair, hazel eyes, big smile, orange-gold scarf wrapped around lower face and neck, sandy tan coat collar. Warm and approachable expression.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG merchant support character. Young woman with short sandy blonde hair, orange and gold scarf around neck and lower face, sandy-tan long coat with many pockets, burnt orange tunic underneath, high-laced desert boots, large patched merchant satchel. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). Additional row for interact animation (opening satchel). GBC palette: #D4A44B, #E86A20, #F5E6C8, #5C3A1E. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Young woman's face, short sandy blonde hair, hazel eyes, big cheerful smile, orange-gold scarf around lower face and neck, sandy tan coat collar. GBC palette: #D4A44B, #E86A20, #F5E6C8, #5C3A1E. Clean pixel art, no anti-aliasing, black outline."

---

## Major NPC: Alaric

### Identity

| Field | Detail |
|-------|--------|
| Name | Alaric |
| Role | Major NPC — Edyn's Mentor, Millhaven's Master Clockmaker |
| Age | 58 |
| Hometown | Millhaven, Verdant Reach |
| Relationship | Surrogate father to Edyn |

### Physical Description

Alaric is tall and thin, slightly stooped from decades of leaning over workbenches. He has gray hair swept back from a high forehead, a neatly trimmed gray beard, and sharp blue eyes behind wire-rimmed spectacles. He wears a long, deep blue coat (his "work coat") covered in tool-loop pockets, over a white shirt and dark trousers. His hands are permanently stained with oil and brass polish. He carries no weapon; his tools are always at his belt.

### Personality, Backstory, and Motivation

Alaric is patient, meticulous, and quietly warm. He took Edyn in after their parents disappeared, not out of obligation but because he saw a kindred spirit—someone who understood that the world worked through mechanisms, visible or hidden, and that fixing broken things was a worthy life's work. He is respected in Millhaven as the person who fixes everything, from clocks to fences to relationships (he is an informal mediator for town disputes).

He traveled to the Chronospire for what he believed was a routine Meridian calibration—a task he performs every five years. He discovered Vasael's plan and tried to stop him, but was overpowered and placed in stasis. He is present in the game only through his absence and the objects he left behind: notes in his handwriting, tools with his mark, NPCs who quote his sayings.

### Stats

Alaric does not participate in combat. He appears in the ending sequence only.

### Dialogue Samples

1. **Flashback (opening scene):** "Every clock has a heart, Edyn. A mechanism that keeps the rest honest. Find the heart, and you understand the whole machine."
2. **NPC quoting Alaric:** "Old Alaric used to say, 'If it ticks, it can be fixed. If it doesn't tick, you just haven't found the right gear yet.'"
3. **Written note (found in Architect ruins):** "The Architects didn't disappear—they left. The question isn't where they went, but what they knew that made them go. —A."
4. **Written note (found in Chronospire):** "Vasael is wrong. Not about the depletion—he's right about that. He's wrong about the solution. You can't save a garden by encasing it in glass. —A."
5. **Reunion (normal ending):** "You came for me. Of course you did. You never did know when to stop."
6. **Reunion (true ending):** "The watch? ...You gave it to the tower. Edyn, that was—that was exactly the right thing to do. Clocks can be rebuilt. You can't."

### Animation States

- Idle: 4 directions — standing, slightly stooped, hands clasped behind back
- Walk: 4 directions — 2-frame slow walk cycle
- Interact: Adjusting spectacles

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#1E3A5E` (deep blue), `#C0C0C8` (silver/gray), `#F5F0E0` (off-white), `#3A2A1E` (dark brown) |

### Portrait Description (16x16px)

Alaric's face: high forehead, swept-back gray hair, neat gray beard, wire-rimmed spectacles, sharp blue eyes, kind expression. Deep blue coat collar visible. Slightly weathered features.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG elderly mentor NPC. Tall thin man, gray swept-back hair, gray beard, wire-rimmed spectacles, deep blue long coat with tool pockets, white shirt, dark trousers. Slightly stooped posture. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). Additional row for interact animation (adjusting spectacles). GBC palette: #1E3A5E, #C0C0C8, #F5F0E0, #3A2A1E. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Elderly man's face, high forehead, swept-back gray hair, neat gray beard, wire-rimmed spectacles, sharp blue eyes, kind gentle expression. Deep blue coat collar. GBC palette: #1E3A5E, #C0C0C8, #F5F0E0, #3A2A1E. Clean pixel art, no anti-aliasing, black outline."

---

## Villain: Vasael, the Epoch Warden

### Identity

| Field | Detail |
|-------|--------|
| Name | Vasael |
| Role | Primary Antagonist — the Epoch Warden |
| Age | 45 (appears older due to Aether exposure) |
| Former Role | Keeper of the Chronospire |
| Relationship | Alaric's captor, philosophical foil to Edyn |

### Physical Description

Vasael is gaunt and angular, with hollow cheeks and deep-set silver eyes that glow faintly with Aether energy. His hair is white, long, and unkempt—once neatly maintained, now wild from weeks of obsessive work inside the Chronospire. He wears a Keeper's robe—originally white and gold, now stained and torn, hanging loosely from his thin frame. Aether crystal growths protrude from his forearms and shoulders—not armor, but a side effect of prolonged direct contact with the Master Core. They pulse with pale blue light. His hands shake constantly unless he is channeling Aether.

### Personality, Backstory, and Motivation

Vasael is brilliant, desperate, and tragic. He genuinely discovered the Aether depletion problem and genuinely tried to solve it through legitimate means. Every institution failed him. His decision to shatter the Chronospire was not impulsive—it was the culmination of a decade of research, petitions, arguments, and despair. He does not enjoy causing suffering; he believes it is a necessary cost.

He is not insane. He is exhausted and committed beyond the point of return. When he speaks to Edyn, he is calm, logical, and even sympathetic. He understands why Edyn opposes him. He simply believes Edyn is wrong—that hope without a plan is just a slower form of surrender.

His motivation: "The Aether runs out in two hundred years. No one else will act. I will preserve this world, even if the world hates me for it."

### Stats (Boss Fight)

| Stat | Phase 1 | Phase 2 | Phase 3 |
|------|---------|---------|---------|
| HP | 120 | 120 | 60 |
| ATK | 22 | 30 | 40 |
| DEF | 18 | 14 | 10 |
| SPD | 12 | 16 | 20 |
| MP | 50 | 50 | 30 |

### Dialogue Samples

1. **First mention (Keeper Serea):** "The Warden of the Chronospire... Vasael. He was the most gifted Keeper in three centuries. Something broke in him, though. Not his mind—his patience."
2. **Confrontation:** "Alaric's apprentice. He spoke of you. He said you were stubborn. I said stubborn people break. He said stubborn people mend."
3. **Pre-fight:** "I gave this world every chance to save itself. Every council, every Keeper, every scholar—they all chose comfort over survival. I chose neither."
4. **Mid-fight (Phase 2):** "You don't understand what I've seen! Two hundred years, Edyn. That's all we have!"
5. **Defeat:** "Then what do you do about the depletion? What happens in two hundred years?"
6. **True ending (release from cell):** "...You found another way. The tower told you. It never told me. Perhaps it knew I wouldn't listen."
7. **True ending (joining Keepers):** "I don't deserve this chance. But I won't waste it."

### Animation States

- Idle: 4 directions — standing, robes billowing, Aether crystals pulsing
- Walk: 4 directions — 2-frame gliding walk (barely lifts feet)
- Attack: Arm extended, Aether blast from crystal growths
- Special: Both arms raised, massive Aether surge (Temporal Collapse)
- Defeat: Falling to knees, crystals dimming

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels (overworld), 16x32 pixels (boss fight) |
| Palette | `#E8E8F0` (pale white), `#6080C0` (steel blue), `#C0A040` (faded gold), `#2A2A3A` (dark indigo) |

### Portrait Description (16x16px)

Vasael's face: gaunt, hollow cheeks, deep-set silver glowing eyes, long wild white hair, torn white-and-gold Keeper robe collar. Aether crystal growth visible on one shoulder. Expression is tired but resolute.

### Pixel Art Generation Prompt — Spritesheet (Overworld)

> "16x16 pixel art spritesheet for a Game Boy Color RPG antagonist NPC. Gaunt man with long wild white hair, glowing silver eyes, torn white-and-gold Keeper robes, pale blue crystal growths on forearms and shoulders. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk frame 1, walk frame 2). GBC palette: #E8E8F0, #6080C0, #C0A040, #2A2A3A. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — Boss Spritesheet (16x32)

> "16x32 pixel art boss spritesheet for a Game Boy Color RPG final boss. Gaunt man with long wild white hair, glowing silver eyes, flowing torn white-and-gold Keeper robes, prominent pale blue crystal growths on arms and shoulders pulsing with energy. Taller imposing proportions. Animation states: idle (facing forward), attack (arm extended with Aether blast), special (both arms raised, massive energy surge), defeat (falling to knees). GBC palette: #E8E8F0, #6080C0, #C0A040, #2A2A3A. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Gaunt man's face, hollow cheeks, deep-set glowing silver eyes, long wild white hair, torn white-and-gold robe collar, crystal growth visible on shoulder. Tired but resolute expression. GBC palette: #E8E8F0, #6080C0, #C0A040, #2A2A3A. Clean pixel art, no anti-aliasing, black outline."

---

## Major NPC: Keeper Serea

### Identity

| Field | Detail |
|-------|--------|
| Name | Serea |
| Role | Keeper of the Verdant Meridian |
| Age | 72 |
| Location | Oakwatch Grove |
| Relationship | Quest giver, lore source, first Keeper Edyn meets |

### Physical Description

Serea is small and elderly, with white hair pulled into a tight bun. She wears a green-and-gold Keeper robe, simpler than Vasael's, with embroidered leaf patterns. Her face is lined but her eyes are sharp and green. She walks with a wooden cane topped with a tiny brass gear—a symbol of her role.

### Personality, Backstory, and Motivation

Serea has been the Verdant Keeper for forty years. She is calm, knowledgeable, and slightly sardonic. She has seen Keepers come and go and remembers Vasael as a young initiate. She is the one who explains the Meridian system to Edyn and provides the Meridian Compass. She is shaken by the Shattering but refuses to panic—she has survived too much for that.

### Stats

Non-combat NPC.

### Dialogue Samples

1. **Greeting:** "You're Alaric's apprentice. I can tell by the grease under your fingernails. He always said you'd come to one of these towers eventually."
2. **Quest Give:** "The Calibration Key is in the vault below. The vault is overrun. I'm too old for stairs and monsters. You, however, are not."
3. **Quest Complete:** "Well done. The Verdant Meridian ticks again. Four more to go. Take this compass—it will guide you to the others."
4. **Lore:** "The Architects built five Meridians to regulate time. The Chronospire coordinates them all. It's elegant, really—like a clock within a clock within a clock."
5. **Emotional Moment:** "I knew Vasael when he was young. Brilliant, driven, impatient. I should have listened to him about the depletion. We all should have."

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#2A5E2A` (forest green), `#C0A040` (gold), `#F0E8D0` (pale cream), `#4A3A2A` (dark brown) |

### Portrait Description (16x16px)

Elderly woman, white hair in tight bun, sharp green eyes, lined face with knowing expression, green-and-gold Keeper robe collar with leaf embroidery.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG elderly female NPC. Small old woman with white hair in tight bun, green-and-gold Keeper robes with leaf embroidery, walking with a wooden cane topped with brass gear. Spritesheet layout: 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #2A5E2A, #C0A040, #F0E8D0, #4A3A2A. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Elderly woman's face, white hair in tight bun, sharp green eyes, kindly lined face, knowing expression, green-and-gold robe collar. GBC palette: #2A5E2A, #C0A040, #F0E8D0, #4A3A2A. Clean pixel art, no anti-aliasing, black outline."

---

## Major NPC: Keeper Corwin

### Identity

| Field | Detail |
|-------|--------|
| Name | Corwin |
| Role | Keeper of the Tidal Meridian / Mini-boss |
| Age | 38 |
| Location | Stormhaven Coast, Tidal Meridian |
| Relationship | Antagonist-turned-ally in Act 1 |

### Physical Description

Corwin has a weathered, salt-stained appearance. Brown hair hangs in lank, wet strands. His Keeper robes are blue-and-silver but soaked and tattered. His eyes are wild and bloodshot. After being subdued and healed by Edyn, his appearance improves—hair pulled back, robes somewhat mended, eyes clear.

### Personality, Backstory, and Motivation

Corwin was a dedicated Keeper who heard the Chronospire "scream" when it shattered. The psychic shock, combined with the temporal loop driving him through the same storm over and over, broke his concentration and convinced him the Shattering was divine punishment. He sabotaged the Meridian's repair systems out of guilt and confusion. After Edyn defeats him and uses the pocket watch to stabilize his mind, he is deeply remorseful and cooperates fully.

### Stats (Mini-Boss)

| Stat | Value |
|------|-------|
| HP | 60 |
| ATK | 14 |
| DEF | 10 |
| SPD | 11 |
| MP | 20 |

### Dialogue Samples

1. **Pre-fight (maddened):** "The tower screamed! Can't you hear it?! It's still screaming! The storm is the punishment—we built these towers and now the sky punishes us!"
2. **Post-fight (subdued):** "I... the screaming stopped. What did you... your watch. It silenced the noise. Oh gods, what have I been doing?"
3. **Quest Complete:** "Thank you. I'll restore the Tidal Core now. Take this—a Tideborn relic. It will help your watch grow stronger."
4. **Lore:** "The Tideborn say the sea has its own time—older than the Meridians, older than the Architects. Sometimes I think they're right."
5. **Return visit:** "The storm broke. Ships are sailing again. Stormhaven remembers how to breathe. Go. Fix the others."

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#2A4A6E` (storm blue), `#A0B8C8` (silver-gray), `#F0F0F0` (white), `#3A2A1E` (dark brown) |

### Portrait Description (16x16px)

Man's face: weathered, lank wet brown hair, wild bloodshot eyes (pre-fight) or clear calm eyes (post-fight), blue-and-silver Keeper robe collar, salt-stained appearance.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG Keeper NPC / mini-boss. Weathered man with lank wet brown hair, blue-and-silver Keeper robes soaked and tattered, wild expression. Spritesheet layout: 4 rows (down, up, left, right), 3 columns (idle, walk, attack). GBC palette: #2A4A6E, #A0B8C8, #F0F0F0, #3A2A1E. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Weathered man's face, lank wet brown hair, wild eyes, blue-and-silver Keeper robe collar, salt stains. GBC palette: #2A4A6E, #A0B8C8, #F0F0F0, #3A2A1E. Clean pixel art, no anti-aliasing, black outline."

---

## Major NPC: Keeper Illion

### Identity

| Field | Detail |
|-------|--------|
| Name | Illion |
| Role | Keeper of the Prism Meridian |
| Age | 55 |
| Location | Crystalfall Desert, Prism Meridian |
| Relationship | Moral choice NPC in Act 2 |

### Physical Description

Illion is tall and ethereal. Prolonged exposure to frozen Aether has left his skin with a faint crystalline sheen. His hair is silver-white and floats slightly as if weightless. His Keeper robes are white-and-cyan, pristine despite the desert, with crystalline clasps. His eyes are a striking pale blue, almost transparent.

### Personality, Backstory, and Motivation

Illion is calm to the point of eerie detachment. Living in temporal stasis has given him a perspective outside normal time—he speaks in the present tense about events that haven't happened yet and the past tense about the current moment. He has been studying the stasis and believes he can see the "shape" of time. He is not villainous but is so absorbed in his research that he has lost sight of the human cost of the desert's freeze.

### Stats

Non-combat NPC.

### Dialogue Samples

1. **Greeting:** "Ah. You arrived. I saw you arriving yesterday, which is also tomorrow. Forgive me—frozen time makes verb tenses unreliable."
2. **Quest Give (moral choice):** "I can show you a vision of the Chronospire—Alaric's exact location, his condition, the path to reach him. But this Meridian must stay frozen for the vision to exist. Choose."
3. **If player chose to restore immediately:** "Interesting. You chose blindly, on faith. The Architects would have approved. Take this fragment—you've earned it."
4. **If player chose the vision first:** "The vision shows what you already know. He's alive. He's waiting. Now fix the tower. I'll do it myself if I must."
5. **Lore:** "Time is not a line. It is a crystal—infinite facets, each reflecting a different angle of the same moment. The Meridians just choose which facet we see."

### Sprite Details

| Property | Value |
|----------|-------|
| Sprite Size | 16x16 pixels |
| Palette | `#E0F0F8` (ice white), `#60C0D0` (cyan), `#A0A8C0` (pale lavender-gray), `#2A2A3A` (dark indigo) |

### Portrait Description (16x16px)

Ethereal man's face: faintly crystalline skin, silver-white floating hair, pale blue near-transparent eyes, serene detached expression, white-and-cyan pristine Keeper robe with crystal clasps.

### Pixel Art Generation Prompt — Spritesheet

> "16x16 pixel art spritesheet for a Game Boy Color RPG ethereal Keeper NPC. Tall man with silver-white floating hair, faintly crystalline shimmering skin, white-and-cyan pristine Keeper robes with crystal clasps, serene expression. Spritesheet layout: 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #E0F0F8, #60C0D0, #A0A8C0, #2A2A3A. Clean pixel art, no anti-aliasing, indexed color."

### Pixel Art Generation Prompt — 16x16 Dialogue Portrait

> "16x16 pixel art portrait for GBC RPG dialogue box. Ethereal man's face, faintly crystalline skin, silver-white floating hair, pale blue transparent eyes, serene expression, white-and-cyan robe collar with crystal clasp. GBC palette: #E0F0F8, #60C0D0, #A0A8C0, #2A2A3A. Clean pixel art, no anti-aliasing, black outline."

---

## Minor NPCs

### Bram (Millhaven Neighbor)

| Field | Detail |
|-------|--------|
| Role | Tutorial NPC, emotional anchor |
| Sprite Size | 16x16 |
| Palette | `#5A7A3E` (green), `#D4B880` (tan), `#F0E8D0` (cream), `#3A2A1E` (dark brown) |
| Description | Middle-aged farmer, ruddy face, straw hat, green overalls, friendly but worried expression |

**Dialogue Samples:**
1. "Edyn! Your mentor's been gone three weeks now. The Council's talking about reassigning his workshop."
2. "I didn't mean to upset you. I just... I worry. Alaric was good to this town."
3. (After Shattering) "The sky cracked, Edyn. The SKY. What in the name of the Architects is happening?"
4. (Return visit) "You look like you've been through the Ashenveil and back. Here—take this. It was Alaric's favorite wrench. He'd want you to have it."
5. "Come home safe, you hear? Millhaven's not the same without you two."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG minor NPC. Middle-aged farmer with ruddy face, straw hat, green overalls, tan shirt, friendly expression. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #5A7A3E, #D4B880, #F0E8D0, #3A2A1E. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Middle-aged farmer, ruddy face, straw hat, friendly worried expression, green overalls collar. GBC palette: #5A7A3E, #D4B880, #F0E8D0, #3A2A1E. Clean pixel art, black outline."

---

### Pip (Lira's Brother)

| Field | Detail |
|-------|--------|
| Role | Subplot NPC (Stormhaven) |
| Sprite Size | 16x16 |
| Palette | `#1A3A3A` (dark teal), `#5EC4B8` (teal), `#F2E8D5` (cream), `#8B6040` (warm brown) |
| Description | Young boy (age 12), dark hair, wide scared eyes, oversized teal sailor coat, bare feet |

**Dialogue Samples:**
1. "L-Lira? LIRA! You found me! The storm keeps coming back and the sailors said we can't leave and I was so scared—"
2. "The ship captain said the storm would stop eventually. But it didn't. It just keeps happening over and over."
3. "Is it true you're going to fix the towers? Can you make the storms stop?"
4. (After Tidal Meridian repair) "The sky is clear! I can see the stars! Lira, look—STARS!"
5. "Be careful out there, okay? Lira worries enough for ten people, but I do too."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG minor NPC child. Young boy with dark hair, wide eyes, oversized teal sailor coat, bare feet, scared but hopeful expression. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #1A3A3A, #5EC4B8, #F2E8D5, #8B6040. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Young boy, dark hair, wide scared eyes, oversized teal sailor coat collar, small face. GBC palette: #1A3A3A, #5EC4B8, #F2E8D5, #8B6040. Clean pixel art, black outline."

---

### Captain Maren (Stormhaven Harbor Master)

| Field | Detail |
|-------|--------|
| Role | Town authority NPC (Stormhaven) |
| Sprite Size | 16x16 |
| Palette | `#2A4060` (navy), `#C0A040` (gold), `#D0C8B8` (stone gray), `#F0E8D0` (cream) |
| Description | Stocky woman, gray streaked dark hair under navy captain's hat, gold-trimmed navy coat, commanding posture |

**Dialogue Samples:**
1. "Welcome to Stormhaven—or what's left of it. I'm Captain Maren. I run this harbor, such as it is."
2. "The storm loops every four hours. Board the windows, wait it out, rebuild. That's life now."
3. "The Tidal Meridian? That Keeper Corwin locked himself in there the day the sky broke. Nobody's gotten through."
4. "You fixed it. You actually fixed it. I owe you a debt I can't repay. The harbor is open—ships sail at dawn."
5. "If you ever need passage across the Stillwater Basin, Stormhaven's fleet is at your disposal."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG authority NPC. Stocky woman with gray-streaked dark hair under navy captain's hat, gold-trimmed navy coat, commanding posture. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #2A4060, #C0A040, #D0C8B8, #F0E8D0. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Stocky woman, gray-streaked dark hair under navy captain's hat, gold-trimmed coat collar, stern but fair expression. GBC palette: #2A4060, #C0A040, #D0C8B8, #F0E8D0. Clean pixel art, black outline."

---

### Dara (Ironpeak Engineer)

| Field | Detail |
|-------|--------|
| Role | Lore NPC, final preparation hub |
| Sprite Size | 16x16 |
| Palette | `#5A5A60` (steel), `#C07030` (copper), `#F0E0C0` (warm cream), `#2A2A30` (charcoal) |
| Description | Lean older woman, copper-red hair in a messy bun, soot-stained leather apron, steel-rimmed magnifying goggles pushed up on forehead, calloused hands |

**Dialogue Samples:**
1. "You're asking about Vasael? I worked with him. Fifteen years ago. He was the smartest person I ever met, and the most frightening."
2. "He brought data, Edyn. Hard numbers. The Aether is depleting. In two hundred years, the Meridians fail permanently. Nobody wanted to hear it."
3. "The Chronospire entrance needs all five cores active simultaneously. Your watch is the key—literally. Alaric designed it that way."
4. "I can upgrade your conduit weapon at the forge. Bring me Architect alloy from the ruins and I'll make it sing."
5. "Be careful in that tower. Vasael isn't the only danger—the Chronospire itself is... aware. The Architects built it that way."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG engineer NPC. Lean older woman with copper-red messy bun hair, soot-stained leather apron, steel magnifying goggles on forehead, calloused hands. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #5A5A60, #C07030, #F0E0C0, #2A2A30. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Lean older woman, copper-red messy bun, soot stains, steel goggles on forehead, shrewd expression. GBC palette: #5A5A60, #C07030, #F0E0C0, #2A2A30. Clean pixel art, black outline."

---

### Haldric (Rook's Former Commander)

| Field | Detail |
|-------|--------|
| Role | Subplot antagonist NPC (Ironpeak Enclave) |
| Sprite Size | 16x16 |
| Palette | `#3A3A40` (iron gray), `#C0A040` (gold insignia), `#E0D8C8` (pale), `#1A1A20` (near black) |
| Description | Tall, rigid posture, clean-shaven, slicked-back dark hair, pristine iron-gray Enclave officer uniform with gold insignia, cold expression |

**Dialogue Samples:**
1. "Rook. I see you survived the marsh. How... unfortunate."
2. "The Enclave has no use for soldiers who can't follow orders without breaking."
3. "That 'clockmaker's brat' you're escorting—they're going to get themselves killed in that tower. And you'll watch, like always."
4. (If evidence found) "Those reports are... that's classified Enclave intelligence. Where did you—how dare you—"
5. (If disgraced) "This isn't over, Rook. The Enclave doesn't forget."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG military antagonist NPC. Tall man with slicked-back dark hair, clean-shaven, rigid posture, pristine iron-gray officer uniform with gold insignia, cold expression. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #3A3A40, #C0A040, #E0D8C8, #1A1A20. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Tall man's face, slicked-back dark hair, clean-shaven, cold arrogant expression, iron-gray officer uniform collar with gold insignia. GBC palette: #3A3A40, #C0A040, #E0D8C8, #1A1A20. Clean pixel art, black outline."

---

### Millhaven Shopkeeper (Wynn)

| Field | Detail |
|-------|--------|
| Role | Shop NPC (Millhaven General Store) |
| Sprite Size | 16x16 |
| Palette | `#8B6040` (warm brown), `#E8C868` (yellow), `#F0E8D0` (cream), `#4A3020` (dark brown) |
| Description | Plump, cheerful woman, curly brown hair under yellow kerchief, brown apron, rosy cheeks |

**Dialogue Samples:**
1. "Welcome to Wynn's Wares! Best prices in Millhaven—well, only prices in Millhaven."
2. "Heading out on an adventure? You'll want potions. Trust me—everyone thinks they won't need potions."
3. "Alaric always bought his oil from me. Said my stock was 'acceptably viscous.' That's high praise from him."
4. (After Shattering) "Half my stock aged to dust in an instant. The other half looks factory-fresh. I don't know what to price anymore."
5. "Come back anytime! And try not to die out there—dead customers don't buy anything."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG shopkeeper NPC. Plump cheerful woman with curly brown hair under yellow kerchief, brown apron, rosy cheeks. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #8B6040, #E8C868, #F0E8D0, #4A3020. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Plump cheerful woman, curly brown hair, yellow kerchief, rosy cheeks, warm smile, brown apron collar. GBC palette: #8B6040, #E8C868, #F0E8D0, #4A3020. Clean pixel art, black outline."

---

### Ironpeak Blacksmith (Forge)

| Field | Detail |
|-------|--------|
| Role | Shop NPC / Weapon Upgrade NPC (Ironpeak Enclave) |
| Sprite Size | 16x16 |
| Palette | `#5A3A2A` (dark rust), `#D08030` (orange-brass), `#E0D0B0` (light tan), `#2A1A10` (very dark brown) |
| Description | Huge muscular man with shaved head, burn scars on arms, leather blacksmith apron, holding a hammer, dark rust-colored shirt |

**Dialogue Samples:**
1. "I'm Forge. Don't ask if that's my real name—it's the only one that matters in the Enclave."
2. "Bring me Architect alloy and I'll make you a weapon that'll split time itself. Figuratively. Mostly."
3. "Rook? Yeah, I know Rook. Good man. The Enclave did him dirty. Tell him I said that."
4. "Your conduit blade's alignment is off by two degrees. Give it here—I'll fix it while you wait."
5. "Best of luck in the Chronospire. If you don't come back, can I have your tools? ...Kidding. Mostly."

**Pixel Art Generation Prompt — Spritesheet:**
> "16x16 pixel art spritesheet for a GBC RPG blacksmith NPC. Huge muscular man, shaved head, burn scars on arms, leather blacksmith apron over dark rust shirt, holding a hammer. 4 rows (down, up, left, right), 2 columns (idle, walk). GBC palette: #5A3A2A, #D08030, #E0D0B0, #2A1A10. Clean pixel art, indexed color."

**Pixel Art Generation Prompt — 16x16 Portrait:**
> "16x16 pixel art portrait for GBC RPG dialogue box. Huge muscular man, shaved head, burn scars, intense but friendly expression, leather apron strap visible. GBC palette: #5A3A2A, #D08030, #E0D0B0, #2A1A10. Clean pixel art, black outline."

---

## Full Character Summary Table

| Character | Role | Sprite Size | Combat Role | Joins |
|-----------|------|-------------|-------------|-------|
| Edyn | Protagonist | 16x16 | Balanced DPS/Utility | Start |
| Lira | Party Member | 16x16 | Healer/Support | Act 1 (Oakwatch Grove) |
| Rook | Party Member | 16x16 | Tank/Physical DPS | Act 2 (Ashenveil Marsh) |
| Sable | Support Character | 16x16 | Non-Combat (Passive Bonuses) | Act 2 (Crystalfall Desert) |
| Alaric | Major NPC | 16x16 | Non-Combat | Ending only |
| Vasael | Antagonist/Boss | 16x16 / 16x32 | Final Boss | Boss Fight |
| Serea | Keeper NPC | 16x16 | Non-Combat | Act 1 |
| Corwin | Keeper/Mini-Boss | 16x16 | Mini-Boss | Act 1 |
| Illion | Keeper NPC | 16x16 | Non-Combat | Act 2 |
| Bram | Minor NPC | 16x16 | Non-Combat | Millhaven |
| Pip | Minor NPC | 16x16 | Non-Combat | Stormhaven |
| Captain Maren | Minor NPC | 16x16 | Non-Combat | Stormhaven |
| Dara | Minor NPC | 16x16 | Non-Combat | Ironpeak |
| Haldric | Subplot Antagonist | 16x16 | Non-Combat | Ironpeak |
| Wynn | Shopkeeper | 16x16 | Non-Combat | Millhaven |
| Forge | Shopkeeper/Smith | 16x16 | Non-Combat | Ironpeak |

---

*Chronospire: The Shattered Meridian — Characters Document*
