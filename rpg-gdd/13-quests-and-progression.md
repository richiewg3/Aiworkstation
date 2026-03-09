# 13 — Quests and Progression

---

## Main Quest Line

### MQ01: The Shattering

| Field | Detail |
|-------|--------|
| Quest Name | The Shattering |
| Given By | Automatic (story event) |
| Objective | Witness the Shattering and leave Millhaven |
| Location | Millhaven (Alaric's Workshop → Town Square) |
| Reward | Pocket Watch, Alaric's Travel Pack |
| Story Advancement | Opens the path to Oakwatch Grove |
| Flag Variable | `VAR_MQ01_SHATTERING` (0=not started, 1=in progress, 2=complete) |

**Description:** The game opens with Edyn in Alaric's Workshop. After the opening dialogue with Bram, the Shattering event triggers: screen shake, clocks stop, sky fractures. Edyn obtains the Pocket Watch and Travel Pack, then must exit the workshop and speak to Bram in the town square to learn the situation. Quest completes when Edyn leaves Millhaven through the south gate.

---

### MQ02: The Verdant Meridian

| Field | Detail |
|-------|--------|
| Quest Name | The Verdant Meridian |
| Given By | Keeper Serea (Oakwatch Grove) |
| Objective | Retrieve the Calibration Key from the Verdant Meridian vault |
| Location | Oakwatch Grove → Verdant Meridian Dungeon |
| Reward | Calibration Key, Meridian Compass, 60 XP |
| Story Advancement | Verdant Meridian restored; Lira joins party; path west opens |
| Flag Variable | `VAR_MQ02_VERDANT` (0=not started, 1=Serea spoken, 2=key obtained, 3=Meridian restored) |

**Description:** Serea explains the Meridian system and asks Edyn to retrieve the Calibration Key from the overrun vault below the tower. Edyn (and Lira, who joins before entering) must navigate two dungeon floors and defeat the Corroded Timekeeper boss. Returning to Serea with the key restores the Verdant Meridian. Serea gives Edyn the Meridian Compass, which points west toward Stormhaven.

---

### MQ03: Storm Over Stormhaven

| Field | Detail |
|-------|--------|
| Quest Name | Storm Over Stormhaven |
| Given By | Captain Maren (Stormhaven Town) |
| Objective | Reach the Tidal Meridian and stop the storm loop |
| Location | Stormhaven → Cliff Path → Tidal Meridian Dungeon |
| Reward | Tideborn Relic, 80 XP, Storm breaks |
| Story Advancement | Tidal Meridian restored; Stormhaven harbor opens |
| Flag Variable | `VAR_MQ03_STORMHAVEN` (0=not arrived, 1=Maren spoken, 2=Corwin defeated, 3=Meridian restored) |

**Description:** Captain Maren explains the storm loop and that Keeper Corwin locked himself in the Tidal Meridian. Edyn must wait for a calm phase to cross the cliff path, navigate the water-themed dungeon, and confront the maddened Corwin. After subduing him and stabilizing his mind with the pocket watch, they restore the Tidal Core together.

---

### MQ04: Into the Marsh

| Field | Detail |
|-------|--------|
| Quest Name | Into the Marsh |
| Given By | Meridian Compass (points north) |
| Objective | Navigate the Ashenveil Marsh and restore the Hollow Meridian |
| Location | Ashenveil Marsh → Hollow Meridian Dungeon |
| Reward | Decay Edge (weapon), 120 XP, Marsh stabilized |
| Story Advancement | Hollow Meridian restored; Rook commits to journey |
| Flag Variable | `VAR_MQ04_HOLLOW` (0=not started, 1=entered marsh, 2=Rook joined, 3=boss defeated, 4=Meridian restored) |

**Description:** Edyn and Lira enter the Ashenveil Marsh. Rook is encountered fighting Bog Rats and joins the party. The team navigates the decay-ridden marsh, explores optional Architect Ruins for lore, and descends into the Hollow Meridian. The dead Keeper's journal is found. The Marsh Colossus boss guards the Core. After defeating it, the marsh stabilizes.

---

### MQ05: The Frozen Desert

| Field | Detail |
|-------|--------|
| Quest Name | The Frozen Desert |
| Given By | Meridian Compass (points east) |
| Objective | Cross the time-frozen Crystalfall Desert and restore the Prism Meridian |
| Location | Crystalfall Desert → Prism Meridian Dungeon |
| Reward | Crystal Wand (Lira weapon), 150 XP, Desert unfreezes |
| Story Advancement | Prism Meridian restored; Sable joins; 4 of 5 Meridians complete |
| Flag Variable | `VAR_MQ05_PRISM` (0=not started, 1=entered desert, 2=Sable met, 3=Illion spoken, 4=boss defeated, 5=Meridian restored) |

**Description:** The Crystalfall Desert is frozen in time. Edyn's pocket watch creates a bubble of normal time. Sable is unfrozen and joins as a support character. The Prism Meridian features light-beam puzzles. Keeper Illion offers a moral choice. The Refracted Guardian boss uses copy mechanics. Restoring the Prism Core unfreezes the entire desert.

---

### MQ06: Ironpeak Preparation

| Field | Detail |
|-------|--------|
| Quest Name | Ironpeak Preparation |
| Given By | Story progression (all 4 regional Meridians restored) |
| Objective | Travel to the Ironpeak Enclave and prepare for the Chronospire |
| Location | Ironpeak Mountains → Ironpeak Enclave |
| Reward | Access to best shops, crafting, lore reveals |
| Story Advancement | Vasael's full backstory learned; Rook's subplot climax; final preparation |
| Flag Variable | `VAR_MQ06_IRONPEAK` (0=not arrived, 1=arrived, 2=Dara spoken, 3=ready to depart) |

**Description:** The Ironpeak Enclave serves as the final preparation hub. Dara reveals Vasael's history and the Chronospire entrance requirements. The best shops and crafting are available. Rook's confrontation with Haldric occurs (if Rook's side quest is active). Quest completes when the player speaks to Captain Maren (who has traveled to Ironpeak) and confirms they are ready to cross the Stillwater Basin.

---

### MQ07: The Chronospire

| Field | Detail |
|-------|--------|
| Quest Name | The Chronospire |
| Given By | Story progression |
| Objective | Ascend the Chronospire, confront Vasael, rescue Alaric |
| Location | Stillwater Basin → Chronospire (5 floors) |
| Reward | Story completion, ending sequence |
| Story Advancement | Final boss defeated, ending plays |
| Flag Variable | `VAR_MQ07_CHRONOSPIRE` (0=not started, 1=crossing, 2=entered, 3=F1-F4 cleared, 4=Vasael defeated, 5=Alaric rescued) |

**Description:** The party crosses the Stillwater Basin and enters the Chronospire. Five dungeon floors, each with a unique mechanic (flashbacks, loops, decay, archive, boss). Vasael is confronted on Floor 5. After defeating him, Edyn descends to the Stasis Chamber and frees Alaric. The normal or true ending plays based on Keeper Fragment collection.

---

### MQ08: Heart of the Chronospire (True Ending Path)

| Field | Detail |
|-------|--------|
| Quest Name | Heart of the Chronospire |
| Given By | Automatic (if all 5 Keeper Fragments collected) |
| Objective | Enter the hidden sixth floor, face the Chronospire's Heart |
| Location | Chronospire Floor 6 (Heart) |
| Reward | Heart's Blessing, true ending, Aether depletion solved |
| Story Advancement | True ending sequence |
| Flag Variable | `VAR_MQ08_HEART` (0=not triggered, 1=entered, 2=boss defeated, 3=true ending complete) |

**Description:** If the player has all 5 Keeper Fragments when reaching the Frozen Archive (F4), a hidden door opens to Floor 6. The Chronospire's living consciousness speaks to Edyn and explains the Aether regeneration solution. The pocket watch is sacrificed. The Heart challenges Edyn to a final test (secret boss, hardest fight, no items). Victory triggers the true ending.

---

## Side Quests

### SQ01: Stormhaven Fishing

| Field | Detail |
|-------|--------|
| Quest Name | Stormhaven Fishing |
| Given By | Fisherman Garl (Stormhaven Town) |
| Objective | Catch a Loopfin during a storm phase |
| Location | Stormhaven Harbor docks |
| Reward | Lucky Coin (accessory, +10% Gold from battles), 50G |
| Availability | Only available BEFORE the Tidal Meridian is restored (the storm loop provides the rare fish) |
| Flag Variable | `VAR_SQ01_FISHING` (0=not started, 1=accepted, 2=Loopfin caught, 3=turned in) |

**Description:** Fisherman Garl explains that the storm loop has brought a rare Loopfin to the harbor — a fish that only exists in temporal anomalies. He asks Edyn to catch one during the storm phase. The player must interact with a specific dock tile during the storm cycle (timing-based). Once caught, return the Loopfin to Garl for the reward. This quest is missable — once the Tidal Meridian is restored, the storm stops and the Loopfin disappears.

---

### SQ02: Lost Traveler

| Field | Detail |
|-------|--------|
| Quest Name | Lost in the Marsh |
| Given By | Lost Traveler (Ashenveil Outer Bog, southwest corner) |
| Objective | Guide the Lost Traveler back to the Ashenveil North Road |
| Location | Ashenveil Outer Bog → Ashenveil North Road |
| Reward | 100G, Herbal Salve x3 |
| Availability | Any time after entering Ashenveil Marsh |
| Flag Variable | `VAR_SQ02_LOST` (0=not found, 1=spoken to, 2=guided to road, 3=rewarded) |

**Description:** A disoriented traveler is lost in the bog, unable to find their way due to the time distortions rearranging paths. After speaking to them, they follow Edyn as a trailing NPC. Lead them back to the North Road scene. On arrival, they thank Edyn and give the reward.

---

### SQ03: Rook's Redemption

| Field | Detail |
|-------|--------|
| Quest Name | Rook's Redemption |
| Given By | Rook (passive — triggers at specific story points) |
| Objective | Find evidence of Haldric's negligence, confront Haldric at Ironpeak |
| Location | Architect Ruins (evidence), Ironpeak Enclave (confrontation) |
| Reward | Rook's affinity +5, Haldric disgraced, Rook offered reinstatement (declines) |
| Availability | Rook must be in party; evidence in Architect Ruins, confrontation in Ironpeak |
| Flag Variable | `VAR_SQ03_ROOK` (0=not started, 1=evidence found, 2=confrontation triggered, 3=resolved) |

**Description:** In the Architect Ruins, an interactable scroll contains classified Enclave orders proving that Haldric sent Rook's squad into the marsh with deliberately falsified intelligence. When the party reaches Ironpeak, Haldric confronts Rook. If the evidence was found, Edyn can present it (dialogue choice). Haldric is publicly disgraced by Dara and the Enclave council. Rook is offered reinstatement but declines, choosing to finish Edyn's journey. If the evidence was NOT found, the confrontation still happens but Rook has no proof, and Haldric walks away. Rook's personal resolution is less satisfying but still occurs.

---

### SQ04: Lira's Herbs

| Field | Detail |
|-------|--------|
| Quest Name | Lira's Herbs |
| Given By | Lira (conversation trigger in Ashenveil Marsh) |
| Objective | Collect 3 Marsh Bloom herbs from the Outer Bog |
| Location | Ashenveil Outer Bog (interactable herb patches) |
| Reward | Bloom Rod (weapon for Lira, +9 ATK, healing +20), Lira affinity +3 |
| Availability | Lira must be in party, after entering Ashenveil Marsh |
| Flag Variable | `VAR_SQ04_HERBS` (0=not started, 1=accepted, 2=1 herb, 3=2 herbs, 4=3 herbs/complete) |

**Description:** Lira mentions she needs specific marsh herbs for her healing work — Marsh Blooms that only grow in areas of accelerated decay. Three herb patches are scattered across the Outer Bog (interactable tiles). Collecting all three and speaking to Lira triggers a crafting cutscene where she fashions the Bloom Rod from her staff and the herbs.

---

### SQ05: Sable's Delivery

| Field | Detail |
|-------|--------|
| Quest Name | Sable's Unfinished Delivery |
| Given By | Sable (after unfreezing in Crystalfall Desert) |
| Objective | Deliver Sable's Aether Crystal shipment to the Ironpeak Enclave |
| Location | Frozen Caravan (pickup) → Ironpeak Enclave (delivery) |
| Reward | 200G, Sable affinity +3, shop discount improved to 20% temporarily |
| Availability | Sable must be in party, crystals obtained from caravan, delivered at Ironpeak |
| Flag Variable | `VAR_SQ05_DELIVERY` (0=not started, 1=crystals obtained, 2=delivered) |

**Description:** Sable's caravan was carrying an Aether Crystal shipment to the Ironpeak Enclave when the desert froze. After the Prism Meridian is restored and the desert unfreezes, Sable asks Edyn to help complete the delivery. Interact with the caravan wagon in the Frozen Caravan scene (now unfrozen) to pick up the shipment. Deliver to Kira at the Ironpeak Market. Kira pays Sable, who splits the reward with Edyn.

---

### SQ06: The Dead Keeper's Legacy

| Field | Detail |
|-------|--------|
| Quest Name | The Dead Keeper's Legacy |
| Given By | Dead Keeper's Journal (Hollow Meridian F2) |
| Objective | Find the Keeper's hidden cache behind the bookshelf |
| Location | Hollow Meridian F2, Keeper's Quarters |
| Reward | Keeper Fragment 3 (Hollow), Marsh Hide (armor), 80G |
| Availability | During or after Hollow Meridian dungeon |
| Flag Variable | `VAR_SQ06_KEEPER_LEGACY` (0=journal not read, 1=journal read, 2=cache found) |

**Description:** Reading the dead Keeper's journal in the Hollow Meridian reveals a note about a hidden cache "behind the bookshelf in my quarters." Interacting with the bookshelf in the Keeper's Quarters triggers a scene where the shelf slides aside, revealing a small room with the Keeper Fragment, the Marsh Hide armor, and a chest of gold. This is technically part of the true ending path but functions as an optional discovery within the dungeon.

---

### SQ07: The Tideborn Blessing

| Field | Detail |
|-------|--------|
| Quest Name | The Tideborn Blessing |
| Given By | Storm-Watcher Nessa (Stormhaven rooftop) |
| Objective | Return to Stormhaven after restoring the Tidal Meridian and speak to Nessa |
| Location | Stormhaven Town (rooftop) |
| Reward | Tidal Shawl (armor for Lira, +7 DEF, +2 MP regen), 75G |
| Availability | After Tidal Meridian restoration, return to Stormhaven |
| Flag Variable | `VAR_SQ07_BLESSING` (0=not started, 1=Nessa spoken post-storm, 2=complete) |

**Description:** Nessa, the Storm-Watcher on the Stormhaven rooftop, was tracking the storm loop patterns. After the storm breaks, speaking to her triggers grateful dialogue about how she can finally stop watching. She gives Edyn the Tidal Shawl, a Tideborn artifact she has been keeping safe for "whoever fixed the Meridian."

---

### SQ08: Alaric's Notes

| Field | Detail |
|-------|--------|
| Quest Name | Alaric's Notes |
| Given By | Finding the first note (Verdant Meridian F1) |
| Objective | Find all 5 of Alaric's scattered notes throughout the game |
| Location | Verdant Meridian F1, Tidal Meridian F2, Architect Ruins, Prism Meridian F1, Chronospire F1 |
| Reward | +2 affinity with all companions (they comment on the notes), lore context |
| Availability | Throughout the entire game |
| Flag Variable | `VAR_SQ08_NOTES` (0-5, counting collected notes) |

**Description:** Alaric left research notes at each Meridian he visited over the years. Each note provides lore about the Meridian system, hints about the Aether depletion, and personal reflections. Collecting all 5 triggers a brief party dialogue where they reflect on Alaric's character and Edyn's connection to him. No tangible item reward, but provides deep story context and companion affinity.

Note locations:
1. Verdant Meridian F1 — On a workbench near the entrance
2. Tidal Meridian F2 — Pinned to a wall near the water wheel
3. Architect Ruins — Tucked into a stone tablet crack
4. Prism Meridian F1 — Embedded in a crystal formation
5. Chronospire F1 — On the floor of the Hall of Moments

---

## Quest Flag Variable Summary

| Variable | Quest | Values |
|----------|-------|--------|
| `VAR_MQ01_SHATTERING` | The Shattering | 0=not started, 1=in progress, 2=complete |
| `VAR_MQ02_VERDANT` | The Verdant Meridian | 0–3 (see above) |
| `VAR_MQ03_STORMHAVEN` | Storm Over Stormhaven | 0–3 |
| `VAR_MQ04_HOLLOW` | Into the Marsh | 0–4 |
| `VAR_MQ05_PRISM` | The Frozen Desert | 0–5 |
| `VAR_MQ06_IRONPEAK` | Ironpeak Preparation | 0–3 |
| `VAR_MQ07_CHRONOSPIRE` | The Chronospire | 0–5 |
| `VAR_MQ08_HEART` | Heart of the Chronospire | 0–3 |
| `VAR_SQ01_FISHING` | Stormhaven Fishing | 0–3 |
| `VAR_SQ02_LOST` | Lost in the Marsh | 0–3 |
| `VAR_SQ03_ROOK` | Rook's Redemption | 0–3 |
| `VAR_SQ04_HERBS` | Lira's Herbs | 0–4 |
| `VAR_SQ05_DELIVERY` | Sable's Delivery | 0–2 |
| `VAR_SQ06_KEEPER_LEGACY` | The Dead Keeper's Legacy | 0–2 |
| `VAR_SQ07_BLESSING` | The Tideborn Blessing | 0–2 |
| `VAR_SQ08_NOTES` | Alaric's Notes | 0–5 (count) |
| `VAR_MERIDIAN_VERDANT` | Verdant Meridian status | 0=broken, 1=restored |
| `VAR_MERIDIAN_TIDAL` | Tidal Meridian status | 0=broken, 1=restored |
| `VAR_MERIDIAN_HOLLOW` | Hollow Meridian status | 0=broken, 1=restored |
| `VAR_MERIDIAN_PRISM` | Prism Meridian status | 0=broken, 1=restored |
| `VAR_FRAGMENT_VERDANT` | Keeper Fragment 1 | 0=not collected, 1=collected |
| `VAR_FRAGMENT_TIDAL` | Keeper Fragment 2 | 0/1 |
| `VAR_FRAGMENT_HOLLOW` | Keeper Fragment 3 | 0/1 |
| `VAR_FRAGMENT_PRISM` | Keeper Fragment 4 | 0/1 |
| `VAR_FRAGMENT_CHRONO` | Keeper Fragment 5 | 0/1 |
| `VAR_LIRA_AFFINITY` | Lira companion affinity | 0–20 |
| `VAR_ROOK_AFFINITY` | Rook companion affinity | 0–20 |
| `VAR_ILLION_CHOICE` | Illion moral choice | 0=not made, 1=restore immediately, 2=chose vision |
| `VAR_SABLE_IN_PARTY` | Sable party status | 0=not joined, 1=joined |
| `VAR_COMP_ACTIVE` | Active companion | 0=none, 1=Lira, 2=Rook |
| `VAR_VISITED_VERDANT` | Region visited flag | 0/1 |
| `VAR_VISITED_STORMHAVEN` | Region visited flag | 0/1 |
| `VAR_VISITED_ASHENVEIL` | Region visited flag | 0/1 |
| `VAR_VISITED_CRYSTALFALL` | Region visited flag | 0/1 |
| `VAR_VISITED_IRONPEAK` | Region visited flag | 0/1 |
| `VAR_VISITED_CHRONOSPIRE` | Region visited flag | 0/1 |

---

*Chronospire: The Shattered Meridian — Quests and Progression Document*
