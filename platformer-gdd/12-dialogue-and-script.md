# 12 — Dialogue & Script

---

## Character Portrait Reference

All dialogue uses the GB Studio Display Dialogue event with a 16×16 pixel character portrait on the left side of the dialogue box. Each speaking character has a unique portrait. Non-character text (narration, environmental descriptions, signs) uses no portrait.

| Character | Portrait Description | Palette Reference |
|---|---|---|
| Solen | Auburn hair, amber eyes, determined smirk, teal coat collar | See 03-characters.md |
| Maren | Auburn braid, brown eyes, calm smile, orange cape | See 03-characters.md |
| Brennan | Bald, white beard, spectacles, blue eyes, brown robe | See 03-characters.md |
| Fern | Green bob hair, big green eyes, excited smile, patchwork vest | See 03-characters.md |
| Orin | Gray ponytail, pale blue eyes, scowling, patched coat | See 03-characters.md |
| Coral | Dark skin, cropped black hair, wide smile, diving mask on forehead | See 03-characters.md |
| Wrench | Ruddy skin, red-gray forked beard, goggles on bald head, gruff | See 03-characters.md |
| Shade (masked) | White featureless mask, violet eye slits, dark cloak | See 03-characters.md |
| Varek | Pale skin, white hair, violet glowing eyes, shadow crown | See 03-characters.md |

### PIXEL ART GENERATION PROMPTS — Portraits

All portrait prompts are collected in 03-characters.md and asset-prompts.md. Each is a 16×16 pixel portrait using the character's designated 4-color GBC palette.

---

## Opening Text Crawl

*[Black screen. White text scrolls slowly upward. Track 01 — "The Lamplighter's Road" plays.]*

```
In the world of Lumara, five ancient crystals
called the Hearthstones hold back the darkness.

Their light feeds the forests, calms the storms,
warms the deep places, and keeps the sky aloft.

For centuries, the Lamplighter Order has tended
these crystals — walking the roads at dusk,
carrying lanterns fueled by Hearthstone light,
keeping the shadows at bay.

But the shadows have a name: the Hollow Tide.
And someone has been letting it in.

One by one, the Hearthstones dim.
One by one, the roads go dark.

And in a small village called Cinderhearth,
a young lamplighter's apprentice is about to
discover that the only light left in the world
is the one she's holding.
```

*[Text fades. Screen fades to Scene 0-1: Cinderhearth Village.]*

---

## Full Opening Cutscene Script (Prologue)

### Scene 0-1: Cinderhearth — Evening Round

*[Solen walks right along the cobblestone road. The player has control. The first few lanterns teach the A-button interaction.]*

*[After lighting the 5th lantern, Solen approaches the end of the road. Maren stands at the doorway of their house.]*

**Maren:** "Last lantern of the night, Solen. Light it clean — a crooked flame smokes out by midnight."

**Solen:** "I know, I know. You've told me a thousand times."

**Maren:** "And I'll tell you a thousand more. That's the job."

*[Solen lights the final lantern. A warm glow fills the area.]*

**Maren:** "Good. Come inside. Supper's getting cold and the stew won't forgive you if you're late again."

**Solen:** "Coming, Mother."

*[The ground trembles. A distant rumble. The Hearthstone on the hill in the background flickers violently.]*

**Maren:** "...Solen. Get inside. Now."

### Scene 0-2: Cinderhearth — The Hollow Surge

*[The sky turns dark violet. Lanterns along the road shatter one by one, left to right, approaching. Shadow tendrils creep across the ground. Villagers scream off-screen.]*

*[Solen runs right toward the house. The player has control — must run right while avoiding shadow tendrils on the ground.]*

*[At the house, cutscene triggers.]*

*[Maren stands in the doorway, lantern staff blazing, holding back a massive tendril of shadow.]*

**Maren:** "Solen — take this!"

*[Maren shoves the lantern staff into Solen's hands.]*

**Solen:** "Mother, what are you—"

*[The shadow tendril strikes Maren. The petrification begins at her feet, creeping upward.]*

**Maren:** "Don't touch me — it spreads through contact. Listen to me."

**Solen:** "No — no, no, no—"

**Maren:** "The lantern... keep it lit... find the Hearthstones..."

*[The stone reaches Maren's chest. Her arms freeze at her sides. Her face is the last to go — she looks at Solen with calm, steady eyes.]*

**Maren:** "You can do this. One lantern at a time."

*[Maren turns fully to stone. The lantern staff in Solen's hands flickers, then steadies.]*

**Solen:** "...Mother?"

*[Silence. The shadow tendrils recede slightly — the lantern pushes them back.]*

*[Brennan appears from the left, limping, leaning on his cane.]*

**Brennan:** "Solen. Solen, look at me."

**Solen:** "She's— she's stone, Brennan—"

**Brennan:** "I know, child. I know. But she's not gone. Not yet."

**Solen:** "How do I fix this? How do I bring her back?"

**Brennan:** "The Hearthstones. All five of them. If all five burn bright at once, their combined light will purge the Hollow Tide completely. Everyone it's taken — the petrified, the frozen — they'll come back."

**Solen:** "All five? The Hearthstones are scattered across Lumara—"

**Brennan:** "I won't lie to you, child. The roads are dark, the Hearthstones are dying, and the man responsible has ten years of power on you. But you have something he lost a long time ago."

**Solen:** "What?"

**Brennan:** "A reason to keep the light burning."

*[Brennan gives Solen the map.]*

**Brennan:** "Your mother's lantern still burns. That means there's still time. Take this map. The Hearthstones are marked. Relight them all and the Hollow Tide will break."

**Solen:** "...One lantern at a time."

**Brennan:** "That's a lamplighter talking. Go. We'll keep the home fires burning."

*[Solen turns right. She walks to the edge of the scene. She pauses, looks back at Maren's stone figure one more time. Then she goes.]*

---

## Boss Intro and Outro Dialogue

### Boss 1: Briar Sentinel (World 1)

**Intro:**

*[Narration — no portrait]*
"The ground splits — a massive guardian rises from the roots. Its eye burns with corrupted light. It doesn't see a Lamplighter. It sees a threat."

**Solen:** "Easy, big guy. I'm here to help. I just need to—"

*[The Sentinel roars.]*

**Solen:** "Okay, not the talking type. Fine."

**Outro:**

*[The Sentinel collapses. The Hearthstone blazes green.]*

**Solen:** "That's one. Four more to go."

*[She sees petrified villagers in the clearing.]*

**Solen:** "...Oh."

**Fern:** "The light brought the forest back, but... they're still stone."

**Solen:** "They need all five Hearthstones. I have to keep going."

**Fern:** "You can't carry them all at once. But you can carry the light to the next stone. And the next. That's how lamplighters work, isn't it? One lantern at a time."

**Solen:** "...Yeah. One lantern at a time."

---

### Boss 2: Glacial Wyrm (World 2)

**Intro:**

*[Narration — no portrait]*
"A serpent of ice descends from the storm. Its coils grip the Hearthstone like a dragon guarding its hoard. Frost breath fills the air."

**Solen:** "You're between me and that stone, and I'm not going to ask politely twice."

*[The Wyrm screeches.]*

**Solen:** "Didn't think so."

**Outro:**

*[The Wyrm flies away. The Hearthstone blazes blue. Snow softens to gentle flurries.]*

**Solen:** "Two down. It's getting warmer... well, less cold."

*[She finds the hidden mural.]*

**Solen:** "What's this? Five Hearthstones... but what's that in the center? A sixth light? The lore never mentioned a sixth light."

*[She sketches in her journal.]*

**Solen:** "I'll figure this out later. Three more stones to go."

---

### Boss 3: Abyssal Leviathan (World 3)

**Intro:**

*[Narration — no portrait]*
"The deep stirs. An eye the size of a doorway opens in the abyss below. This is no corrupted creature — this is the Hollow itself, reaching up through the water."

**Solen:** "That's... significantly bigger than a rabbit."

*[Tentacles slam.]*

**Solen:** "Okay. Big and angry. Same plan as always — hit the glowy part."

**Outro:**

*[Leviathan retreats. Hearthstone blazes teal. Water clears.]*

**Solen:** "Three down. I'm running out of breath and running out of luck."

*[She exits. Shade appears.]*

**Shade:** "Impressive. Three Hearthstones. Three pulses of energy — and Varek caught every one."

**Solen:** "Who are you?"

**Shade:** "Someone who's been watching. Someone who needs you to understand: every Hearthstone you relight sends a pulse through the ley lines. Varek is waiting at the other end with open hands. You've been feeding him, Lamplighter."

**Solen:** "You're lying."

**Shade:** "Ask yourself why the road to each Hearthstone was passable. Why nothing truly stopped you. He's been letting you through. You're his battery."

*[Shade vanishes.]*

**Solen:** "..."

**Solen:** "It doesn't matter. Mother is still stone. There's no other way."

---

### Boss 4: Molten Warden (World 4)

**Intro:**

*[Narration — no portrait]*
"The forge's master rises — a colossus of slag and shadow, its fires turned to destruction. The hammer-arm rises. The eye-slit burns."

**Solen:** "You used to build things, didn't you? I'm sorry about what comes next."

*[The Warden roars.]*

**Outro:**

*[The Warden crumbles. Hearthstone blazes orange. Forges ignite.]*

**Wrench:** "You did it! The forge — it's alive again! I haven't heard that hum in months."

**Solen:** "Wrench? You made it out?"

**Wrench:** "Your route was clear enough. Solen... I need to tell you something. I knew your father. Edric."

**Solen:** "...You knew my father?"

**Wrench:** "We worked the same mine. I was the one who signed off on the tunnel. The one that collapsed. It was my inspection, my stamp. I've carried that for twelve years."

**Solen:** "..."

**Wrench:** "He was carving this for you. A little wooden lantern. Kept it in his pocket. I found it after. I never knew who to give it to."

*[He gives Solen the figurine.]*

**Solen:** "He... he never got to finish it."

**Wrench:** "No. He didn't."

*[Pause.]*

**Solen:** "One more stone. The Spire."

**Wrench:** "Give Varek hell, kid."

---

### Mini-Boss: Shade / Aldric (World 5)

**Intro:**

**Shade:** "You made it this far. I won't pretend I'm not impressed."

**Solen:** "Get out of my way."

**Shade:** "I can't. Varek needs time. I'll give him that."

**Solen:** "You don't have to do this."

**Shade:** "I didn't want this fight, Solen. But you won't stop, and he needs time. I'll give him that much."

**Outro:**

*[Shade collapses. Mask cracks. Falls away.]*

**Solen:** "Aldric? You're... you were a Lamplighter. You served with my mother."

**Aldric:** "She... she was the best of us. I'm sorry, Solen. I thought Varek had the answer."

**Solen:** "Why? Why did you follow him?"

**Aldric:** "Because the Hearthstones are chains. He was right about that. We spent our whole lives maintaining a prison and calling it protection. I couldn't live with that."

**Solen:** "And this is better?"

**Aldric:** "No. He's not wrong about the chains, Solen. He's just wrong about what happens when you break them."

*[Aldric closes his eyes. The shadow leaves his body.]*

*[Solen kneels. Takes his Lamplighter badge.]*

**Solen:** "I'll remember. I promise."

---

### Final Boss: Varek, the Hollow King (World 5)

**Intro:**

**Varek:** "Ah. The little Lamplighter. Maren's daughter."

**Solen:** "You know my mother."

**Varek:** "I knew her. She was the best of us. She understood the Hearthstones better than anyone — she just couldn't take the final step."

**Solen:** "The step you took? Extinguishing them? Drowning the world in darkness?"

**Varek:** "Freeing the world. The Hearthstones are chains, Solen. Beautiful, warm chains — but chains all the same. The Hollow is the natural state of this world. The First Keepers imprisoned it out of fear."

**Solen:** "And everyone who was turned to stone? My mother? What about them?"

**Varek:** "They would become part of the new world. Not dead. Changed."

**Solen:** "Changed isn't alive. I'd rather light a candle every day for the rest of my life than let you blow out the sun."

**Varek:** "Then we have nothing more to discuss."

**Phase Transition:**

*[Varek staggers in the air after Phase 1.]*

**Varek:** "You're stronger than I expected. But I didn't come this far to lose to a girl with a candle."

*[He rises, absorbs Hollow energy, transforms.]*

**Varek:** "THE HOLLOW SPEAKS THROUGH ME NOW. I AM THE TIDE."

**Outro:**

*[Varek collapses. Human again. Trembling.]*

**Varek:** "The Hollow... it promised... it said the world would be free..."

**Solen:** "You were wrong, Varek. But I understand why you believed it."

**Varek:** "...Do you?"

**Solen:** "The Hearthstones are fragile. The system is broken. But the answer isn't to destroy everything and start over. The answer is to do the work. Light the lanterns. Walk the roads. Even when it's hard."

**Varek:** "You sound like Maren."

**Solen:** "I'll take that."

*[Solen walks to the Spire Hearthstone.]*

---

## Full NPC Dialogue

### Fern (World 1 — Scene 1-2)

**First Meeting:**

**Fern:** "Oh! A person! A real, not-stone, not-shadow person! I haven't seen one in four days!"

**Fern:** "I'm Fern. Herbalist, mushroom enthusiast, and currently living in a tree because the ground is too scary."

**Solen:** "I'm Solen. Lamplighter. Or... trying to be."

**Fern:** "A Lamplighter! That explains the big glowy stick. Here, take this — it's a healing tincture. Bitterbark and moonpetal extract. Tastes like dirt and regret, but it'll close a wound in seconds."

**Fern:** "If you're heading to the Hearthstone, you'll need to go through the Thornveil Thicket. It's terrible — thorns as long as your arm, vines that grab, pollen that makes you sneeze for an hour. But the shadows can't get through it. Too thick."

**Fern:** "The vines in there are sticky — you can kick off them to climb! I've been doing it for days. Just jump at a vine-covered wall and jump again when you touch it."

**If Revisited After World 1 Clear:**

**Fern:** "Solen! You're alive! The forest is coming back — I found three new mushroom species this morning. Three! The Hollow Tide was terrible for people but apparently great for fungi."

**Fern:** "The petrified villagers... they're still stone. But there's color in the forest again. That's got to count for something, right?"

**If Revisited After World 3:**

**Fern:** "I heard what that shadow person told you. That Varek has been using you. You don't believe it, do you?"

**Solen:** "I don't know what to believe. But I know Mother is still stone."

**Fern:** "Then that's enough. Go light the next one."

---

### Orin (World 2 — Scene 2-1)

**First Meeting:**

**Orin:** "Another Lamplighter? Thought you were all dead or turned to stone."

**Solen:** "Not yet."

**Orin:** "Hm. You're either very brave or very stupid. Same thing, really."

**Solen:** "I need to reach the Frost Hearthstone at the summit."

**Orin:** "Of course you do. Everyone wants to climb the mountain. Nobody wants to think about what happens when they fall."

**Orin:** "Varek was my student. My best student. I taught him everything — how to read the wind, how to keep a flame steady in a blizzard, how to listen to the Hearthstones. And he used all of it to snuff them out."

**Orin:** "Take my old climbing gear. I don't need it anymore — I'm not going anywhere."

**Solen:** "Come with me. You know the mountain better than anyone."

**Orin:** "And do what? Fight shadows with a bad knee and worse conscience? No. I've done enough damage."

**If Revisited After World 2 Clear:**

**Orin:** "You did it. The blizzard stopped. I can see the village from here — the ice is still there, but it's not spreading."

**Orin:** "I should have done what you're doing. Years ago. Before Varek got so far gone."

**Solen:** "It's not too late, Orin."

**Orin:** "For the world, maybe. For me? We'll see."

**If Revisited After World 4:**

**Orin:** "Four Hearthstones. One left. The Spire."

**Solen:** "I know."

**Orin:** "Varek will be waiting for you. He's had ten years to prepare. You've had... weeks?"

**Solen:** "Weeks and a really good stick."

**Orin:** "Heh. You're more stubborn than your mother. She was the same way. Maren never could let a dark road stay dark."

---

### Coral (World 3 — Scene 3-1)

**First Meeting:**

**Coral:** "A surface-dweller! In my ruins! This is the best day I've had since the cavern ceiling didn't collapse on Tuesday."

**Coral:** "I'm Coral. Diver, salvager, and the only person crazy enough to live down here voluntarily."

**Solen:** "Doesn't it bother you? Living underground in the dark?"

**Coral:** "The dark? Solen, look around — there's bioluminescent algae, glowing fish, entire caverns lit up like festival lanterns. The dark is just what you see before you find the light. I should cross-stitch that on a pillow."

**Coral:** "I'll guide you through the flooded sections. In exchange, I need your help finding something. My partner Tomas's locket — I dropped it in the Keeper cathedral months ago. It's not valuable to anyone but me."

**If Spoken to After Finding the Locket:**

**Coral:** "You found it! You actually — oh."

*[She holds the locket. Opens it. The portrait inside is water-damaged, barely visible.]*

**Coral:** "His face is almost gone. I knew it would be. I just... wanted to hold it again."

**Coral:** "Thank you, Solen. Here — I've been hoarding these tincture supplies. You can carry one more now. You'll need it more than I will."

**If Revisited After World 3 Clear:**

**Coral:** "The Brine is clearing up beautifully since you relit the Hearthstone. I found three new chambers yesterday."

**Coral:** "I read more of Varek's journals. He wasn't always like this, was he?"

**Solen:** "No. Apparently he was brilliant once. Kind, even."

**Coral:** "The scary thing about kind people who break is they think breaking is kindness."

---

### Wrench (World 4 — Scene 4-1)

**First Meeting:**

**Wrench:** "Who— how did you get past my turrets?!"

**Solen:** "Your turrets?"

**Wrench:** "The automated defense turrets I built from mining equipment to keep the shadow things out."

**Solen:** "I didn't see any turrets."

**Wrench:** "...Oh. They ran out of ammo three days ago, didn't they. Well, that's terrifying."

**Wrench:** "I'm Wrench. Head mechanist of the Cinderforge, or what's left of it. I've been trapped in this maintenance bay since the Hollow Tide hit."

**Solen:** "I'm heading to the Forge Hearthstone. I need to relight it."

**Wrench:** "The Hearthstone's at the volcanic core, encased in shadow-obsidian. You'll need to redirect the magma flows to crack the shell. I can modify your boots — give them a quick-step mechanism. You'll need it to cross the lava gaps."

**Wrench:** "In exchange, clear my escape route. I've got a map of the forge tunnels. The shadow creatures have taken everything between here and the north exit."

**Solen:** "Deal."

**If Revisited After World 4 Clear:**

**Wrench:** "Forges are running again. First thing I made? A new turret. Second thing? A lock for the door. I'm not getting trapped down here twice."

**Wrench:** "You heading to the Spire next?"

**Solen:** "It's the last one."

**Wrench:** "Then take this. It's a reinforced lantern housing — should protect the crystal inside your staff if you take a hard hit. Edric would have wanted you to have every advantage."

---

## All Sign and Hint Text

### Cinderhearth Signs

**Village Entrance Sign:**
"Welcome to Cinderhearth. Population: Enough. Visitors: Light your own lantern or go home."

**Road Sign Near Well:**
"Cinderhearth Well — Water tastes like minerals and regret. Drink at your own risk."

**Maren's Doorstep Sign:**
"Maren & Solen — Please no visitors after the last lantern."

### World 1 Signs

**Forest Entrance Warning:**
"Verdant Hollow — Lamplighter Patrol Route 7. Report all dimmed lanterns to the nearest station."

**Thornveil Thicket Sign (placed by Fern):**
"Thicket ahead! The vines are grabby but climable. Don't eat the purple mushrooms. — F"

**Near Hearthstone Clearing:**
"The Verdant Hearthstone. Tended by the Briar Guardian since the First Age. Do not disturb."

### World 2 Signs

**Lower Slopes Warning:**
"Frostfang Peaks — Altitude sickness is real. Climb slowly. Tell someone where you're going."

**Rimehaven Village Entrance:**
"Welcome to Rimehaven — Annual Ice Festival postponed indefinitely."

**Near Summit:**
"Summit shrine ahead. The wind never stops. Tie down everything you value."

### World 3 Signs

**Cavern Entrance:**
"Sunken Brine — Authorized divers only. Unauthorized divers become authorized corpses."

**First Keeper Ruins Plaque:**
"Here the First Keepers built. Here they sealed. Here they forgot why. — Inscription, untranslated"

**Near Research Chamber:**
"V. was here. The truth is below. — scratched into the wall in recent handwriting"

### World 4 Signs

**Mine Entrance:**
"Cinderforge Mining Co. — Hard hats required. No smoking near the magma vents. Management."

**Near Forge Floor:**
"Shift change at the third bell. Report all unusual tremors to the foreman. — posted notice, yellowed with age"

**Near Obsidian Core:**
"DANGER — Volcanic core. Beyond this point: no rescue, no refund, no regrets."

### World 5 Signs

**At the Base of the Ascent:**
"The Spire awaits above. This path was walked by the First Keepers. Walk it well."

**Inside the Spire (torn Lamplighter notice):**
"To all Lamplighters: the Spire remains our seat of— [torn] — rek has claimed— [torn] — evacuate immedia— [torn]"

**Near Varek's Chamber:**
"He waits beyond this door. Turn back while you still can. — scratched by an unknown hand"

---

## Full Ending Cutscene Scripts

### Normal Ending

*[Solen touches her lantern to the Spire Hearthstone. White light blazes.]*

*[All five Hearthstones pulse in unison. A wave of golden light sweeps across Lumara.]*

*[Montage — each scene is 3 seconds:]*

*[Verdant Hollow: Trees bloom. Flowers erupt from the ground. A petrified farmer cracks and gasps.]*

*[Frostfang Peaks: The killing blizzard softens. In Rimehaven, the frozen child's fingers twitch. Ice begins to crack.]*

*[Sunken Brine: Water clears to crystal teal. Bioluminescent fish swirl in celebration. Ancient runes blaze on every wall.]*

*[Cinderforge: Magma turns warm orange. Forges hum. A miner petrified mid-swing cracks free and looks around, confused.]*

*[Cinderhearth: Dawn breaks over the village. Lanterns still burn — but they don't need to anymore. The sky is bright.]*

*[Solen runs down from the Spire. Through the Ascent. Across the world map. To Cinderhearth.]*

*[She reaches her doorstep.]*

*[Maren is there. Stone cracking away. Color returning to her skin. She blinks. Sees Solen.]*

*[Maren sees the lantern staff in Solen's hands.]*

**Maren:** "You walked the whole road? All five?"

**Solen:** "All five."

**Maren:** "That's my girl."

*[Solen falls into Maren's arms. They hold each other.]*

*[Fade to black.]*

**Text:** *"The Hearthstones burn bright. The roads are lit. The Lamplighters walk again."*

*[Pause.]*

**Text:** *"But beneath the Abyssal Sea, something patient stirs. The Hollow remembers."*

*[Credits roll. Track 13 — "Dawn Returns" plays.]*

---

### True Ending

*[After defeating Varek with all 25 Ember Shards and 5 Lore Stones, a stairway opens in the Hearthstone Chamber floor.]*

**Solen:** "The sixth light... the mural was real."

*[Solen descends into the Chamber of Origin.]*

*[The chamber is pristine white stone. First Keeper murals in perfect condition line every wall. At the center, the Lantern of Origin glows on a pedestal.]*

*[Solen reads the murals. Three interactive dialogue events:]*

**Mural 1:** "We built the Hearthstones to hold back the Hollow. But we knew they would not last forever."

**Mural 2:** "Should the Hearthstones fail, we built a failsafe: the Lantern of Origin. It will sever Lumara from the Abyssal Sea permanently. The Hollow will never return."

**Mural 3:** "The cost is great: the Hearthstones will be consumed. Lumara will need to find its own light — fire, flame, the simple warmth of human hands. We could not make this choice for you. We leave it in your keeping."

*[Solen approaches the Lantern of Origin.]*

*[Dialogue choice appears:]*

**"Activate the Lantern of Origin?"**

**► YES**

**  NO**

*[If NO: Solen steps back. "Not yet." The player can return later.]*

*[If YES:]*

**Solen:** "No more chains. No more prison. No more dependence on crystals that can fail. Lumara makes its own light now."

*[She picks up the Lantern of Origin.]*

*[A massive beam of white light erupts downward from beneath the Spire — into the earth, through the Abyssal Sea, sealing the crack between Lumara and the void permanently.]*

*[The Hollow screams — not in pain, but in surprise. A distant, vast, alien sound.]*

*[The Hearthstones go dark. All of them. Lumara is plunged into natural night.]*

*[Silence.]*

*[Then: stars. The sky fills with them. They were always there, hidden behind the Hearthstone glow.]*

*[Montage — alternate version:]*

*[Verdant Hollow: Lit by moonlight and fireflies. Trees stand tall under starlight. A petrified farmer cracks free and looks up at the sky — a sky he's never seen before.]*

*[Frostfang Peaks: Aurora borealis dances above the peaks. Rimehaven thaws. The frozen child's hand reaches the door handle and pushes it open.]*

*[Sunken Brine: The caverns glow with natural bioluminescence — brighter than ever, no longer competing with Hearthstone light.]*

*[Cinderforge: Real coal fires burn in the forges, stoked by human hands. Warm orange light fills the tunnels. A miner lights a candle and smiles.]*

*[Cinderhearth: Night. Real night. Warm and dark and peaceful. Lanterns burn with ordinary flame.]*

*[Solen returns to Cinderhearth. Maren is alive, free of stone. She looks at the lantern staff — its Hearthstone crystal is dark, spent.]*

*[Maren takes the staff. Turns it over. Strikes a match. Lights the lantern with an ordinary flame.]*

**Maren:** "Hearthstone or matchstick, the job's the same."

**Solen:** "One lantern at a time."

*[They look at each other and smile.]*

*[Fade to black.]*

**Text:** *"The Hearthstones are silent. The Hollow is gone. And Lumara, for the first time, belongs only to itself."*

*[Credits roll. Track 14 — "Starlight" plays.]*

*[After credits: a single frame. The wooden lantern figurine Edric carved — now finished by Solen's hand — sits on the mantelpiece of their home, lit by warm firelight.]*

*[Fade to black. Return to title screen.]*
