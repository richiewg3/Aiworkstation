# 11 — Sound & Music

---

## Music Overview

All music is composed for hUGETracker, the 4-channel Game Boy audio tracker used by GB Studio 4.2. The four available channels are:

| Channel | Type | Role |
|---|---|---|
| Pulse 1 | Square wave (12.5%, 25%, 50%, 75% duty) | Lead melody |
| Pulse 2 | Square wave (12.5%, 25%, 50%, 75% duty) | Harmony / counter-melody |
| Wave | Custom 4-bit waveform | Bass / pad / texture |
| Noise | Noise generator | Percussion / ambience |

All tracks loop seamlessly. Tempo and style vary by world and scene to match the emotional arc of the game.

---

## Music Tracks

---

### Track 01: "The Lamplighter's Road" — Title Screen Theme

**Plays In:** Title screen

**Mood:** Melancholy, hopeful, gentle. The opening melody should feel like remembering something you've lost but haven't given up on finding.

**BPM:** 80

**Key:** D minor

**Style:** Slow waltz feel (3/4 time). Simple, memorable melody that becomes the game's main motif — variations of this melody appear throughout the soundtrack.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Lead melody | A descending phrase in D minor, simple and singable — think a lullaby with weight. 50% duty cycle for warm tone. The melody uses mostly quarter and half notes with one dotted rhythm for gentle forward motion. |
| Pulse 2 | Arpeggiated harmony | Soft broken chords underneath the melody, cycling through Dm – F – C – Gm. 25% duty cycle for thinner, more ethereal tone. |
| Wave | Sustained bass | Long, held bass notes following the chord progression. Smooth sine-ish waveform. Provides warmth and foundation. |
| Noise | Ambient texture | Very sparse — a soft cymbal-like hiss on the downbeat of every other measure. No aggressive percussion. |

**Real GBC OST Reference:** The mood and pacing of the title theme from *The Legend of Zelda: Link's Awakening DX* — that sense of a story waiting to be told. Also draws from the softer moments of the *Shantae* (GBC) soundtrack for its melodic warmth.

**Looping:** Loops seamlessly after 32 measures. The last measure's final note resolves into the first measure's pickup note.

---

### Track 02: "Cinderhearth" — Prologue / Village Theme

**Plays In:** Scene 0-1 (Cinderhearth Village — Evening Round)

**Mood:** Warm, homey, safe — with a subtle undercurrent of tension that the player won't notice on first listen but will recognize on replay.

**BPM:** 104

**Key:** G major

**Style:** Light folk feel (4/4 time). Bouncy but not frantic. The melody should feel like a walk through a familiar village at sunset.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Lead melody | A cheerful, skipping melody in G major. Uses 50% duty cycle. Eighth note runs with occasional sixteenth note flourishes. The main motif from Track 01 appears briefly at the end of each 8-measure phrase, hinting at the larger story. |
| Pulse 2 | Counter-melody | A simple response phrase that echoes the lead, offset by 2 beats. 25% duty cycle. |
| Wave | Walking bass | Steady bass line following root notes of G – C – D – Em progression. Light, pizzicato-style waveform with quick attack and decay. |
| Noise | Light percussion | Soft kick on beats 1 and 3 (low-pitch noise), closed hi-hat on beats 2 and 4 (high-pitch noise). Very restrained — the village is quiet. |

**Real GBC OST Reference:** Kakariko Village theme from *Link's Awakening DX* for the warm village vibe. *Kirby's Dream Land 2* overworld themes for the lightness.

**Looping:** Loops after 16 measures.

---

### Track 03: "The Hollow Comes" — Prologue / Hollow Tide Surge

**Plays In:** Scene 0-2 (Cinderhearth — The Hollow Surge), petrification cutscene

**Mood:** Sudden terror, chaos, despair. The music should make the player's stomach drop.

**BPM:** 140

**Key:** D minor (same root as the title theme — the motif is twisted)

**Style:** Urgent, driving, dissonant. The main motif from Track 01 appears but in a distorted, panicked form — faster, minor key, with clashing harmonics.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Distorted main motif | The title theme melody played at double speed in D minor, with 12.5% duty for a thin, desperate tone. Rapid staccato. |
| Pulse 2 | Alarm harmony | Alternating tritone intervals (D–G#) creating a dissonant alarm-like pattern. 75% duty for harsh tone. |
| Wave | Rumbling bass | Deep, droning bass note on D, with rapid pitch modulation creating a "trembling ground" effect. |
| Noise | Chaos percussion | Rapid-fire noise — snare rolls, crash cymbal hits, creating a sense of stampede and collapse. |

**Real GBC OST Reference:** The dungeon danger themes from *Gargoyle's Quest* for the sudden shift to dread. The urgency of boss encounter openings from *Mega Man V* (GB).

**Looping:** Does not loop — plays once during the cutscene, ends on a sustained dissonant chord that fades to silence as Maren turns to stone.

---

### Track 04: "Verdant Hollow" — World 1 Theme

**Plays In:** Scenes 1-1, 1-2, 1-4

**Mood:** Wistful, adventurous, slightly sad. The forest is beautiful but wounded.

**BPM:** 112

**Key:** E minor

**Style:** Moderate tempo adventure theme (4/4). A melody that feels like walking through a forest at twilight — there's wonder, but also awareness of danger.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Lead melody | A flowing E minor melody with a mix of stepwise motion and leaps. 50% duty. The "lamplighter motif" (from Track 01) appears as a brief quote at the midpoint of the loop. |
| Pulse 2 | Harmonized thirds | Follows the lead a third below, creating a rich harmonic texture. 25% duty. Drops out during the motif quote to let it stand alone. |
| Wave | Warm bass | Root-fifth bass pattern, steady and grounding. Smooth waveform. |
| Noise | Nature percussion | Very light: a soft shaker pattern on eighth notes (high-pitch noise at low volume) evoking rustling leaves. Occasional deeper hit on beat 1 like a distant footstep. |

**Real GBC OST Reference:** *Shantae* (GBC) town themes for melodic warmth. Forest themes from *Donkey Kong Land III* for the natural rhythm.

**Looping:** Loops after 24 measures.

---

### Track 05: "Thornveil Ascent" — World 1 Vertical Challenge

**Plays In:** Scene 1-3 (Thornveil Thicket)

**Mood:** Tense, focused, climbing. The player is working hard and the music reflects it.

**BPM:** 128

**Key:** A minor

**Style:** Driving action theme (4/4). The ascending melody mirrors the vertical level design.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Ascending lead | A melody that climbs in pitch over 8-measure phrases, using rising scale passages in A minor. 50% duty. Quick, athletic feel. |
| Pulse 2 | Rhythmic stabs | Short, accented chords on the off-beats creating forward momentum. 25% duty. |
| Wave | Pulsing bass | Driving eighth-note bass line, mostly on the root (A) with chromatic movement. Creates urgency. |
| Noise | Tight percussion | Kick on 1 and 3, snare on 2 and 4, hi-hat on all eighth notes. Tight, athletic rhythm. |

**Real GBC OST Reference:** *Mega Man V* (GB) stage themes for the climbing, athletic energy.

**Looping:** Loops after 16 measures.

---

### Track 06: "Frostfang Peaks" — World 2 Theme

**Plays In:** Scenes 2-1, 2-2, 2-4

**Mood:** Stark, beautiful, lonely. The cold is in the music — sparse, open, with wide intervals.

**BPM:** 88

**Key:** B minor

**Style:** Slow, sparse (4/4). Wide intervals and open harmonics evoke vast mountain spaces.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Lead melody | A sparse, open melody with wide leaps (5ths and octaves). Long notes with occasional quick grace notes. 50% duty. |
| Pulse 2 | Echoed response | Same melody delayed by 1 measure, quieter, creating an echo effect like sound bouncing off mountains. 25% duty. |
| Wave | Sustained pad | Long, sustained chords providing a bed of harmony. Smooth waveform at low volume. Bm – D – F#m – A progression. |
| Noise | Wind texture | Continuous low-level noise shaped to sound like wind — long, filtered sweeps. Very sparse percussion: a single deep hit every 4 measures like a distant avalanche. |

**Real GBC OST Reference:** Ice World themes from *Donkey Kong Land III*. The desolate beauty of *Link's Awakening DX* mountain areas.

**Looping:** Loops after 32 measures.

---

### Track 07: "Ice Shelf" — World 2 Platforming Challenge

**Plays In:** Scene 2-3

**Mood:** Precarious, thrilling, vertigo. One wrong step and you fall.

**BPM:** 132

**Key:** F# minor

**Style:** Fast, tense (4/4). Staccato notes and sudden rests create a "stepping on thin ice" feeling.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Staccato lead | Short, clipped notes in rapid patterns with sudden silences (rests on beat 3 every other measure). Creates uncertainty. 50% duty. |
| Pulse 2 | Tremolo harmony | Rapid tremolo on held notes, creating a shimmering, cold-wind effect. 12.5% duty. |
| Wave | Anxious bass | Syncopated bass that avoids the downbeat, landing on the "and" of each beat. Unsettling. |
| Noise | Crisp percussion | Sharp, high-pitched clicks on off-beats (ice cracking). Sparse kick drum. |

**Real GBC OST Reference:** The faster, more intense moments of *Mega Man V* (GB) ice stages.

**Looping:** Loops after 16 measures.

---

### Track 08: "Sunken Brine" — World 3 Theme

**Plays In:** Scenes 3-1, 3-2, 3-4

**Mood:** Mysterious, submerged, ancient. The weight of water and history.

**BPM:** 76

**Key:** C minor

**Style:** Slow, aquatic (4/4 with a triplet feel). Notes have long sustains and slow attack, as if heard through water.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Drifting melody | A slow, meandering melody in C minor with lots of held notes and slow bends. 50% duty with pitch vibrato. |
| Pulse 2 | Bubbling arpeggios | Quick, quiet arpeggiated figures that rise and fall, evoking bubbles. 25% duty at low volume. |
| Wave | Deep bass drone | Very low, sustained bass drone with occasional slow movement. Deep waveform. Creates a sense of enormous depth. |
| Noise | Underwater ambience | Filtered noise creating a constant "underwater hiss." Occasional deep thud like distant pressure shifts. No clear percussion. |

**Real GBC OST Reference:** Underwater themes from *Donkey Kong Land III*. The mysterious underwater areas of *Shantae* (GBC).

**Looping:** Loops after 32 measures.

---

### Track 09: "First Keeper Archives" — World 3 Research Chamber

**Plays In:** Scene 3-3 (Varek's Research Chamber)

**Mood:** Unsettling, intellectual, obsessive. You're in the mind of the antagonist.

**BPM:** 92

**Key:** D# diminished (unstable, shifting)

**Style:** Creeping, dissonant (4/4). The music feels like it's trying to resolve but never does.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Wandering melody | A melody that starts phrases but never finishes them, trailing off into silence or dissonance. 50% duty. |
| Pulse 2 | Counterpoint | A second voice that sometimes moves in parallel, sometimes in opposition, creating unease. 25% duty. |
| Wave | Unresolved bass | Bass that moves chromatically, never settling on a root. Creates constant tonal instability. |
| Noise | Scribbling texture | Rapid, quiet, irregular noise — like the sound of frantic writing. Occasionally punctuated by a louder hit (a book dropping, a chair scraping). |

**Real GBC OST Reference:** The unsettling interior themes from *Gargoyle's Quest*. Haunted house themes from *Link's Awakening DX*.

**Looping:** Loops after 24 measures.

---

### Track 10: "Cinderforge Depths" — World 4 Theme

**Plays In:** Scenes 4-1, 4-2, 4-3, 4-4

**Mood:** Intense, industrial, defiant. Fire fighting back against darkness.

**BPM:** 136

**Key:** G minor

**Style:** Driving, heavy (4/4). Strong downbeats, aggressive bass, and a melody that feels like hammering on an anvil.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Forceful melody | A bold, angular melody in G minor with hammer-like accented notes on beats 1 and 3. 75% duty for thick, aggressive tone. |
| Pulse 2 | Power chords | Block chord stabs on the off-beats, creating a driving, industrial rhythm. 50% duty. |
| Wave | Heavy bass | Deep, driving bass line with a lot of low-end presence. Follows the chord roots with occasional chromatic runs. Aggressive sawtooth-style waveform. |
| Noise | Industrial percussion | Heavy kick on 1 and 3, sharp snare on 2 and 4, rapid hi-hat sixteenths. Additional metallic noise hits on off-beats evoking hammer strikes and machinery. |

**Real GBC OST Reference:** *Mega Man V* (GB) action stage themes for the industrial energy. *Gargoyle's Quest* dungeon themes for the aggression.

**Looping:** Loops after 16 measures.

---

### Track 11: "The Spire Ascent" — World 5 Theme

**Plays In:** Scenes 5-1, 5-2

**Mood:** Epic, desperate, final. Everything has been building to this.

**BPM:** 144

**Key:** E minor (the key of World 1 — the journey comes full circle)

**Style:** Fast, heroic, intense (4/4). The main motif from Track 01 returns in full force, transformed from a gentle waltz into a battle hymn.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Heroic lead | The main "Lamplighter" motif played at double speed, full force, in E minor. 50% duty. Triumphant and determined. |
| Pulse 2 | Driving harmony | Rapid arpeggiated figures underneath the lead, creating a sense of urgency and upward momentum. 25% duty. |
| Wave | Power bass | Aggressive octave bass hits on every beat. Deep, driving, propulsive. |
| Noise | Battle percussion | Full kit: kick on every beat, snare on 2 and 4, open hi-hat on all eighth notes, crash cymbal at phrase starts. Maximum energy. |

**Real GBC OST Reference:** Final stage themes from *Mega Man V* (GB). The climactic energy of *Shantae* (GBC) boss rush areas.

**Looping:** Loops after 16 measures.

---

### Track 12: "The Hollow King" — Final Boss Theme

**Plays In:** Scene 5-5 (Varek boss fight — both phases)

**Mood:** Phase 1: Tense confrontation. Phase 2: Full-scale desperate battle.

**BPM:** 152 (Phase 1: half-time feel at 76, Phase 2: full speed 152)

**Key:** D minor (the title theme's key — the final confrontation mirrors the beginning)

**Style:** The ultimate track. Phase 1 is a tense, controlled arrangement that quotes the title theme in a dark, distorted form. Phase 2 drops the restraint and becomes an all-out assault of sound.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Dark motif / heroic counter | Phase 1: The title theme motif played slowly, in minor, with dissonant alterations. Phase 2: The motif returns in its original form but at double speed, fighting against the darkness. 50% duty. |
| Pulse 2 | Varek's theme | A new counter-melody representing Varek — cold, logical, descending where Solen's motif ascends. In Phase 2, the two melodies interweave and clash. 25% duty. |
| Wave | Rumbling bass | Phase 1: Low, ominous pedal tone on D. Phase 2: Aggressive chromatic bass runs. |
| Noise | Escalating percussion | Phase 1: Sparse, heavy hits (impact sounds). Phase 2: Full double-time drums, crash cymbals, maximum intensity. |

**Real GBC OST Reference:** Final boss themes from *Mega Man V* (GB) for intensity. *Gargoyle's Quest* final confrontation for the dark-vs-light musical clash.

**Looping:** Phase 1 section loops after 16 measures. Phase 2 section loops after 16 measures. Transition between phases is triggered by a game event (script changes the music).

---

### Track 13: "Dawn Returns" — Normal Ending Theme

**Plays In:** Normal ending montage and cutscene

**Mood:** Relief, joy, earned peace. The weight lifts.

**BPM:** 88

**Key:** G major (the Cinderhearth key — home again)

**Style:** Gentle, warm, swelling (3/4 waltz time, like the title theme). The main motif returns in major key — its original form, but now it feels different because of everything the player has experienced. It should bring tears.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Main motif (major) | The "Lamplighter" motif in G major, played slowly and gently. 50% duty. Every note feels earned. |
| Pulse 2 | Harmony | Warm thirds and sixths above the melody. 25% duty. Gentle, supportive. |
| Wave | Full bass | Warm, round bass following the G – C – D – Em progression. Provides a deep sense of resolution. |
| Noise | Soft texture | Barely-there cymbal wash. The world is quiet. Peace. |

**Real GBC OST Reference:** Ending themes from *Link's Awakening DX* — that specific feeling of completing a journey and finding it was worth it.

**Looping:** Does not loop — plays once through (approximately 2 minutes), ends on a sustained G major chord that fades to silence.

---

### Track 14: "Starlight" — True Ending Theme

**Plays In:** True ending sequence and alternate credits

**Mood:** Awe, transcendence, bittersweet beauty. Something old has ended and something new has begun.

**BPM:** 72

**Key:** D major (the title theme key, but major — the ultimate resolution)

**Style:** Ethereal, sparse, profoundly peaceful (3/4). Even gentler than the normal ending. The motif is barely there — just fragments, like a memory of a melody, surrounded by silence and starlight.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Fragmented motif | Isolated notes from the main motif, with long silences between them. Each note feels like a star appearing in a dark sky. 50% duty with slow volume envelope. |
| Pulse 2 | Celestial arpeggios | Very quiet, slow arpeggios rising and falling — like the breathing of a sleeping world. 12.5% duty for maximum ethereal quality. |
| Wave | Deep warmth | A single, sustained bass note (D) that holds for the entire piece, providing grounding amid the floating melody. |
| Noise | Silence-shaped | Almost nothing. The faintest hiss, like the sound of stars. A single soft chime every 8 measures. |

**Real GBC OST Reference:** The secret ending music from *Link's Awakening DX* — that rare, precious feeling of completing something truly, permanently.

**Looping:** Does not loop — plays once (approximately 3 minutes), fading to complete silence.

---

### Track 15: "Boss Battle" — Standard Boss Theme

**Plays In:** All boss fights except the final boss (Briar Sentinel, Glacial Wyrm, Abyssal Leviathan, Molten Warden, Shade)

**Mood:** Intense, rhythmic, dangerous. A fight for survival.

**BPM:** 148

**Key:** A minor

**Style:** Fast, aggressive action (4/4). Driving rhythm with a memorable melodic hook.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Boss melody | A fierce, angular melody with rapid staccato passages and dramatic pauses. 75% duty for an aggressive, thick tone. |
| Pulse 2 | Rhythmic counter | Quick chord stabs and arpeggiated fills creating a sense of danger. 50% duty. |
| Wave | Aggressive bass | Fast, driving bass line with lots of motion — the bass never rests. Sawtooth waveform. |
| Noise | Battle drums | Relentless: kick on every beat, snare on 2 and 4, rapid hi-hat, tom fills at phrase endings. |

**Real GBC OST Reference:** Boss themes from *Mega Man V* (GB) for the intensity and memorable melody. *Shantae* (GBC) boss themes for the rhythm.

**Looping:** Loops after 16 measures.

---

### Track 16: "Victory" — Boss Defeat Jingle

**Plays In:** After defeating any boss

**Mood:** Triumphant, relieved, brief.

**BPM:** 120

**Key:** C major

**Style:** Short fanfare (4 measures). Bright, ascending, resolving.

**4-Channel Breakdown:**

| Channel | Role | Description |
|---|---|---|
| Pulse 1 | Fanfare melody | Ascending C major scale run ending on a held high C. Bright and clear. |
| Pulse 2 | Harmony | Major third harmony following the lead. |
| Wave | Bass resolution | C bass pedal into a final C octave hit. |
| Noise | Cymbal crash | Single crash cymbal on the final note. |

**Real GBC OST Reference:** *Mega Man* series victory jingles.

**Looping:** Does not loop — plays once (~3 seconds).

---

## Sound Effects

| # | Name | Trigger Event | Description |
|---|---|---|---|
| 1 | sfx_jump | Player jumps | Short upward-sweeping tone (Pulse channel). Bright, light, ~0.1s. |
| 2 | sfx_double_jump | Player double-jumps | Higher-pitched version of sfx_jump with a quick echo effect. ~0.15s. |
| 3 | sfx_land | Player lands on ground | Low thud (Noise channel). Soft, ~0.05s. |
| 4 | sfx_attack | Player swings lantern staff | Quick whoosh followed by a bright metallic ping (Noise + Pulse). ~0.15s. |
| 5 | sfx_hit_enemy | Attack connects with enemy | Sharp impact sound — a brief burst of noise with a descending tone (Noise + Pulse). ~0.1s. |
| 6 | sfx_enemy_death | Enemy defeated | Ascending dissolve — a quick upward arpeggio (Pulse) followed by a soft pop (Noise). ~0.2s. |
| 7 | sfx_player_hurt | Player takes damage | Harsh buzz + descending tone (Noise + Pulse). Uncomfortable, attention-getting. ~0.2s. |
| 8 | sfx_player_death | Player dies | Low descending tone followed by silence. The "lantern going out" sound — a slow fade-down of a held note. ~0.5s. |
| 9 | sfx_coin_collect | Flame Coin collected | Bright two-note chime — ascending major second (Pulse). ~0.1s. Classic "coin" sound. |
| 10 | sfx_shard_collect | Ember Shard collected | Longer, more dramatic version of the coin sound — ascending arpeggio + shimmer (Pulse + Wave). ~0.3s. |
| 11 | sfx_heal | Player uses Healing Tincture | Warm, ascending three-note arpeggio (Wave). Gentle and restorative. ~0.3s. |
| 12 | sfx_checkpoint | Checkpoint lamppost lit | A warm "whoosh" followed by a held, glowing tone — like a flame igniting (Noise into sustained Pulse). ~0.4s. |
| 13 | sfx_dialogue_open | Dialogue box appears | Soft page-turn sound — quick burst of filtered noise. ~0.1s. |
| 14 | sfx_dialogue_char | Each character of dialogue text | Tiny blip (Pulse at very low volume). Varies slightly in pitch based on the speaking character. ~0.02s. |
| 15 | sfx_menu_move | Cursor moves in menu | Quick, clean blip — single high-pitched pulse. ~0.05s. |
| 16 | sfx_menu_select | Menu option selected | Two-note ascending confirmation tone (Pulse). ~0.1s. |
| 17 | sfx_menu_cancel | Menu closed / B pressed | Single descending tone (Pulse). ~0.1s. |
| 18 | sfx_wall_jump | Player wall-jumps | Quick scratch + upward tone (Noise + Pulse). Like feet scraping off a surface. ~0.1s. |
| 19 | sfx_dash | Player dashes | Sharp burst of noise + whoosh (Noise). Fast, aggressive. ~0.15s. |
| 20 | sfx_hearthstone_reignite | Hearthstone reignited | Long, swelling chord — all channels. Starts low and rises to a bright, sustained major chord. The most dramatic SFX in the game. ~1.5s. |
| 21 | sfx_petrify | Character turns to stone | Cracking, grinding sound — low-frequency noise with rhythmic pulsing, slowing down as the petrification completes. ~1.0s. |
| 22 | sfx_boss_roar | Boss appears / phase transition | Deep, distorted growl (Wave channel at max volume with rapid pitch modulation). Impactful. ~0.5s. |
| 23 | sfx_splash | Player enters/exits water | Quick burst of noise shaped like a water splash — white noise with quick decay. ~0.15s. |
| 24 | sfx_ladder_climb | Player climbs ladder (each rung) | Alternating two-tone blips (Pulse) — low-high-low-high matching the hand-over-hand animation. ~0.05s per blip. |
| 25 | sfx_crumble | Platform crumbles | Descending noise burst + low rumble (Noise + Wave). Like rocks falling. ~0.3s. |
| 26 | sfx_wind_gust | Wind gust pushes player | Filtered noise sweep — a "whooo" sound (Noise). ~0.5s. |
| 27 | sfx_lore_stone | Lore Stone collected | Ethereal three-note descending chord (Wave) followed by a shimmer (Pulse). Feels ancient and significant. ~0.5s. |
| 28 | sfx_lantern_upgrade | Lantern power increases | Warm ascending tone that grows brighter, ending in a flash-like pop (Pulse + Noise). ~0.4s. |
