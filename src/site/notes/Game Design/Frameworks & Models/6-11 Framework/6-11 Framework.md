---
{"dg-publish":true,"permalink":"/game-design/frameworks-and-models/6-11-framework/6-11-framework/","dg-note-properties":{}}
---

## Foundational Ontology

In game design theory, traditional structural frameworks like **MDA** (Mechanics, Dynamics, Aesthetics) establish how low-level rules generate emergent system behaviors. However, designers frequently encounter an analytical gap at the top layer: MDA’s "Aesthetics" tier often groups player emotion into broad, subjective categories (e.g., _Fantasy_, _Sensation_, _Challenge_) without explaining the underlying psychological mechanisms that trigger those feelings.

The **6–11 Framework**, created by Dr. Roberto Dillon, bridges this gap by grounding game design in evolutionary psychology and human affect theory. It operates on the principle that player delight, frustration, tension, and immersion are not random byproduct effects; they are the direct psychological result of mechanics stimulating specific **subconscious instincts**.

| **Stage** | **Pipeline Layer**              | **System Description / Inputs**                      |
| --------- | ------------------------------- | ---------------------------------------------------- |
| **1**     | **Atomic Verbs / Actions**      | Physical inputs, button presses, movement            |
| **2**     | **Gameplay Mechanics**          | Rules, hazards, spatial constraints, timers          |
| **3**     | **Subconscious Instincts (11)** | Survival, Greed, Protection, Exploration, etc.       |
| **4**     | **Elicited Emotions (6)**       | Fear, Anger, Excitement, Pride, Sadness, Joy         |
| **5**     | **Terminal State**              | Mastery, Fulfillment, Emotional Resonance, Retention |

### Analytical Role in the Crafting Play Architecture

The 6–11 Framework fulfills three structural functions:

1. **The Experience Engine for A.G.E.:** Serves as the explicit theoretical model for the **Experience** layer in Roberto Dillon’s _A.G.E. Framework_ (Actions, Gameplay, Experience).
    
2. **Granular Aesthetics Quantification:** Replaces abstract aesthetic labels in **MDA** and **RMDA** with measurable, repeatable emotional transitions.
    
3. **Intentional Pacing Tool:** Enables designers to map emotional arcs across mission structures, combat loops, and narrative beats, preventing cognitive exhaustion or mechanical monotony.
    

## The Core 6 Universal Emotions

Emotions act as the player's immediate psychological feedback receptors and internal motivators during play. Grounded in psychological treatises on primary human affect, the framework identifies **six universal emotions** that form the core spectrum of player experience:

### 1. Fear

- **Psychological Definition:** An acute state of apprehension and heightened alertness triggered by real, perceived, or impending threats to survival, status, or progress.
    
- **Systemic Function:** Forces hyper-focus, increases perceived stakes, and amplifies the emotional release of subsequent victory.
    
- **Mechanical Triggers:** Lethal hazards, limited visibility (fog of war), scarce ammunition, permadeath rules, and relentless AI pursuers.
    
- **Design Anti-Pattern:** Prolonged, unmitigated fear without moments of safety leads to sensory fatigue and player disengagement.
    

### 2. Anger

- **Psychological Definition:** A disruptive emotional reaction sparked when agency is thwarted, progress is unfairly revoked, or hostile obstacles obstruct a goal.
    
- **Systemic Function:** Serves as a powerful short-term re-engagement catalyst when tied to clear paths for mastery or retaliation.
    
- **Mechanical Triggers:** High-damage enemy attacks, setback penalties, loss of accumulated gear, or defeat by rival players/bosses.
    
- **Design Anti-Pattern:** Unfair or telegraph-lacking mechanics generate toxic anger, driving rage-quitting rather than revenge-driven determination.
    

### 3. Joy / Happiness

- **Psychological Definition:** Positive emotional release resulting from goal fulfillment, harmonious sensory feedback, unexpected good fortune, or playful discovery.
    
- **Systemic Function:** Validates effort, reinforces positive mechanical loops, and builds emotional warmth toward the game world.
    
- **Mechanical Triggers:** Completing questlines, acquiring desired loot, vibrant visual/audio celebrations, easter eggs, and cooperative synergy.
    
- **Design Anti-Pattern:** Trivial, unearned rewards degrade the value of joy, causing it to collapse into indifference.
    

### 4. Pride

- **Psychological Definition:** A deep sense of self-efficacy and accomplishment achieved through overcoming non-trivial adversity or mastering complex systems.
    
- **Systemic Function:** Fosters intrinsic competence, drives long-term retention, and transforms casual players into dedicated masters.
    
- **Mechanical Triggers:** Defeating difficult bosses, executing frame-perfect maneuvers, optimizing complex builds, and ascending competitive leaderboards.
    
- **Design Anti-Pattern:** Gating success behind paywalls or pure RNG deprives the player of genuine pride.
    

### 5. Sadness

- **Psychological Definition:** Reflective emotional gravity brought on by narrative loss, sacrifice, empathy, or poignant storytelling.
    
- **Systemic Function:** Anchors narrative weight, humanizes characters, and creates memorable, emotionally resonant milestones.
    
- **Mechanical Triggers:** Character death in story arcs, irreversible moral choices, decaying game worlds, and nostalgic environmental storytelling.
    
- **Design Anti-Pattern:** Forced, unearned melodrama that fails to connect with player actions feels cynical and breaks immersion.
    

### 6. Excitement

- **Psychological Definition:** An energetic state of arousal and anticipation sparked by speed, high stakes, dynamic feedback, or unpredictable outcomes.
    
- **Systemic Function:** Sustains adrenaline, maintains flow states, and keeps interaction pacing high.
    
- **Mechanical Triggers:** Time trials, close-call extractions, random critical hits, rapid movement mechanics, and high-frequency combat loops.
    
- **Design Anti-Pattern:** Perpetual excitement without quiet pacing breaks flattens the emotional experience and causes sensory exhaustion.
    

## The 11 Primal Instincts (Subconscious Triggers)

While the **6 Universal Emotions** define the player’s felt psychological state, **Instincts** act as the underlying behavioral drivers. In the 6–11 Framework, game systems do not generate emotion directly out of nothing; mechanics engage primal human instincts, and the satisfaction, frustration, or dynamic tension of those instincts produces the corresponding emotional state.

| **System Mechanic / Rule**        | **Subconscious Instinct** | **Primary Elicited Emotion Arc** | **Terminal Payoff**             |
| --------------------------------- | ------------------------- | -------------------------------- | ------------------------------- |
| **Scarce Ammo / Survival Hazard** | Survival                  | Fear → Joy                       | Relief                          |
| **Rare Boss Loot Drop**           | Greed / Collecting        | Excitement → Joy                 | Pride & Satisfaction            |
| **Defeat by Rival / Boss**        | Revenge                   | Anger → Pride                    | Victory & Retribution           |
| **Hidden Map Location / Lore**    | Exploration               | Excitement → Joy                 | Wonder & Discovery              |
| **Escort / Defense Objective**    | Protection / Care         | Fear → Pride                     | Attachment & Shelter Validation |
Below is the deconstruction of the **11 Primal Instincts**, detailing their evolutionary psychological basis, systemic mechanical implementations, resulting emotional payoffs, and industry design anti-patterns.

### 1. Survival (Fight or Flight)

- **Psychological Basis:** The primordial impulse to self-preserve when facing existential hazards, mortality, or loss of state.
    
- **Mechanical Verbs & Systems:** Health/stamina management, hazard avoidance, resource scarcity, cover mechanics, stealth toggles, permadeath.
    
- **Elicited Emotional Loop:** Initial **Fear** (vulnerability) $\rightarrow$ High **Excitement** (close call) $\rightarrow$ Terminal **Joy / Relief** upon reaching safety.
    
- **System Exemplar:** _Resident Evil 2 Remake_ — Restricted inventory capacity and unkillable pursuers (Mr. X) force constant survival calculus.
    
- **Design Anti-Pattern:** Infinite resources or absent fail states eliminate survival tension, rendering defensive systems trivial.
    

### 2. Self-Identification

- **Psychological Basis:** The psychological drive to project personal identity, agency, aesthetic style, and ethical values onto an avatar, faction, or role.
    
- **Mechanical Verbs & Systems:** Character creation, cosmetic customization, class/build specialization, branching dialogue choices, moral alignment meters.
    
- **Elicited Emotional Loop:** **Excitement** (creative expression) $\rightarrow$ Deep **Pride** and personal ownership over the character arc.
    
- **System Exemplar:** _Cyberpunk 2077_ / _Baldur's Gate 3_ — Extensive character build synergy and narrative choice alignment cultivate personal ownership.
    
- **Design Anti-Pattern:** Illusory choice (where distinct choices produce identical outcomes) breaks self-identification and creates cynical disengagement.
    

### 3. Collecting

- **Psychological Basis:** The intrinsic desire to seek out, gather, catalog, and complete sets of items, achievements, or information.
    
- **Mechanical Verbs & Systems:** Bestiaries, codex logs, set bonuses, card collection decks, achievement checklists, inventory management.
    
- **Elicited Emotional Loop:** **Excitement** during the hunt $\rightarrow$ **Joy** upon set completion $\rightarrow$ Long-term **Pride** in showcase fulfillment.
    
- **System Exemplar:** _Pokémon_ / _World of Warcraft_ — Mount, pet, and achievement collection logs drive meta-engagement spanning hundreds of hours.
    
- **Design Anti-Pattern:** Bloated, meaningless junk collection (e.g., hundreds of identical map feather pickups) transforms collecting into chore-like fatigue.
    

### 4. Greed

- **Psychological Basis:** The drive to acquire rare wealth, high-tier loot, or exponential power far beyond immediate operational survival needs.
    
- **Mechanical Verbs & Systems:** Rare drop tables (RNG), gold sinks, gacha mechanics, secret treasure vaults, auction houses, high-tier gear scaling.
    
- **Elicited Emotional Loop:** Anticipatory **Excitement** $\rightarrow$ Sudden **Joy** upon a rare drop (or temporary **Anger** on a bad roll).
    
- **System Exemplar:** _Diablo IV_ / _Path of Exile_ — Piles of randomized loot and glowing legendary beam drops exploit greed loops to power core retention.
    
- **Design Anti-Pattern:** Over-saturating the game economy with legendary drops destroys item scarcity, neutralizing the greed trigger.
    

### 5. Protection / Care / Nurture

- **Psychological Basis:** The protective impulse to shelter, heal, repair, or raise vulnerable allies, pets, bases, or companions.
    
- **Mechanical Verbs & Systems:** Escort missions, base defense fortification, companion healing spells, pet feeding loops, loyalty meters.
    
- **Elicited Emotional Loop:** Protective **Fear** (for the target's survival) $\rightarrow$ **Relief** and deep **Pride** / emotional warmth upon successful defense.
    
- **System Exemplar:** _The Last of Us_,  Protecting Ellie through dynamic AI interactions builds emotional bonds grounded in mechanical care.
    
- **Design Anti-Pattern:** Poor companion pathfinding or suicidal AI companion behavior converts care into intense, game-breaking **Anger**.
    

### 6. Aggressiveness

- **Psychological Basis:** The urge to project power, exert tactical force, initiate offensive combat, and physically or systemically dominate opponents.
    
- **Mechanical Verbs & Systems:** Melee combo strings, execution finishers, high-caliber weaponry, offensive stat buffs, destruction mechanics.
    
- **Elicited Emotional Loop:** High adrenaline **Excitement** $\rightarrow$ Sense of mechanical **Pride** and tactical empowerment.
    
- **System Exemplar:** _DOOM Eternal_ — The "Glory Kill" mechanic demands forward aggressive play to harvest health and ammo from enemies.
    
- **Design Anti-Pattern:** Defensive turtling meta-strategies that penalize aggressive play starve players of power fantasy satisfaction.
    

### 7. Revenge

- **Psychological Basis:** The targeted drive to retaliate against specific rivals, bosses, or enemy factions that previously inflicted defeat, loss, or insult.
    
- **Mechanical Verbs & Systems:** Nemesis tracking systems, death recaps, corpse runs, kill cams, rivalry match-ups, bounty lists.
    
- **Elicited Emotional Loop:** Defeat-induced **Anger** $\rightarrow$ Targeted **Revenge** drive $\rightarrow$ Exhilarating **Pride** upon defeating the rival.
    
- **System Exemplar:** _Middle-earth: Shadow of Mordor_ — The Nemesis System generates personalized enemy Orcs that remember past encounters and taunt the player upon re-engagement.
    
- **Design Anti-Pattern:** Eliminating victory feedback or preventing players from re-engaging their specific defeater leaves revenge unfulfilled.
    

### 8. Competition

- **Psychological Basis:** The desire to benchmark skill, strategic mastery, and performance against peers, automated challenges, or global rankings.
    
- **Mechanical Verbs & Systems:** Ranked matchmaking ladders, Elo/MMR scoring, speedrunning timers, public leaderboards, head-to-head PvP modes.
    
- **Elicited Emotional Loop:** High-stakes **Excitement** paired with loss-induced **Anger** $\rightarrow$ Long-term **Pride** upon tier ascension.
    
- **System Exemplar:** _VALORANT_ / _Street Fighter 6_ — Strict competitive ranking structures validate mechanical mastery and strategic growth.
    
- **Design Anti-Pattern:** Opaque matchmaking algorithms or unpunished cheating ruin competitive integrity, driving competition into frustration.
    

### 9. Communication

- **Psychological Basis:** The impulse to exchange information, coordinate tactical plans, negotiate, and build social relationships within a shared space.
    
- **Mechanical Verbs & Systems:** Contextual ping wheels, proximity voice chat, guild structures, emote wheels, trading markets, co-op synergy verbs.
    
- **Elicited Emotional Loop:** Social connection $\rightarrow$ Shared **Joy** and strategic **Pride** during coordinated team victories.
    
- **System Exemplar:** _Apex Legends_ — The non-verbal Ping System enables fluid tactical communication without requiring voice chat.
    
- **Design Anti-Pattern:** High friction or toxic social environments suppress positive communication, causing social burnout.
    

### 10. Exploration / Curiosity

- **Psychological Basis:** The intrinsic drive to map uncharted territory, uncover hidden secrets, decipher mysteries, and investigate novel environments.
    
- **Mechanical Verbs & Systems:** Fog of war, hidden passageways, environmental lore collectibles, landmark navigation, puzzle solving.
    
- **Elicited Emotional Loop:** Anticipatory **Excitement** $\rightarrow$ Sudden **Joy** and wonder upon discovering a hidden area.
    
- **System Exemplar:** _Elden Ring_ / _Outer Wilds_ — Minimal UI handholding encourages self-directed spatial and intellectual discovery.
    
- **Design Anti-Pattern:** Excessive map icon clutter ("checklist open worlds") strips away organic discovery and replaces curiosity with routine navigation.
    

### 11. Color / Sensory Appreciation

- **Psychological Basis:** Natural aesthetic attraction to visual harmony, striking color palettes, contrast, dynamic lighting, tactile "juice," and rich audio feedback.
    
- **Mechanical Verbs & Systems:** Color-coded item rarity tiers (e.g., Common Green to Exotic Gold), particle VFX, hit stop, adaptive audio, screen shake.
    
- **Elicited Emotional Loop:** Instantaneous **Joy** and aesthetic delight; heightens the emotional impact of all other 10 instincts.
    
- **System Exemplar:** _Hades_ / _Persona 5_ — Vibrant color palettes, dynamic UI animations, and sharp audio stingers elevate every action into sensory delight.
    
- **Design Anti-Pattern:** Visual noise or muddy readability that obscures critical gameplay information, causing visual fatigue.
    

### Summary Matrix: The 11 Primal Instincts

| Instinct | Mechanical Implementation | Primary Emotional Arc | Terminal Payoff |
| :--- | :--- | :--- | :--- |
| **1. Survival** | Scarce resources, health meters, hazards | Fear → Relief | Adrenaline release, survival validation |
| **2. Self-Identification** | Character creation, builds, moral choices | Excitement → Ownership | Autonomy, personal identity projection |
| **3. Collecting** | Codex logs, card sets, achievements | Excitement → Joy | Set completion, collection mastery |
| **4. Greed** | Rare loot drops, RNG chests, wealth sinks | Anticipation → Joy | Status amplification, power surge |
| **5. Protection / Care** | Companion defense, base repair, healing | Fear → Pride | Emotional bonding, shelter validation |
| **6. Aggressiveness** | Executions, combo chains, heavy firepower | Excitement → Pride | Power fantasy, tactical domination |
| **7. Revenge** | Nemesis trackers, death recaps, rivalries | Anger → Exhilaration | Retribution, grievance resolution |
| **8. Competition** | Ranked ladders, Elo ratings, leaderboards | Anxiety → Pride | Competence validation, ranking mastery |
| **9. Communication** | Contextual pings, voice chat, co-op actions | Connection → Shared Joy | Social cohesion, team synergy |
| **10. Exploration** | Fog of war, secrets, lore landmarks | Anticipation → Joy | Discovery, intellectual satisfaction |
| **11. Color / Sensory** | Item tier colors, juice VFX, adaptive audio | Instant Aesthetic Joy | Sensory immersion, tactile satisfaction |

## Section 4: Cross-Framework Systemic Integrations

The 6–11 Framework does not exist in isolation. Within the _Crafting Play_ ecosystem, it functions as a universal **Affective Engine**—a psychological translation layer that plugs into structural, narrative, UX, and pedagogical game design frameworks.

While structural frameworks define _how systems are built_ and narrative models define _what stories are told_, the 6–11 Framework defines _how those systems and stories feel to the human subconscious_.

| **Connected Framework**        | **Architectural Domain**   | **6–11 Functional Integration Role**                                     |
| ------------------------------ | -------------------------- | ------------------------------------------------------------------------ |
| **A.G.E. Framework**           | Architectural Pipeline     | Functions as the explicit theoretical model for the _Experience_ layer   |
| **MDA / RMDA**                 | Systemic Aesthetics        | Replaces abstract aesthetic labels with quantifiable emotional mechanics |
| **Clarity Model**              | Signal & UX                | Ensures game feedback communicates instinct triggers with low friction   |
| **Emotioneering / DDE / DORK** | Design & Decisioning       | Anchors player agency, narrative empathy, and prototyping loops          |
| **GEB / SSM Frameworks**       | Educational & System-Story | Bridges gamified learning and narrative lore with primal human drives    |

### 4.1 Integration with the A.G.E. Framework (Actions, Gameplay, Experience)

The **A.G.E. Framework** (developed by Dr. Roberto Dillon) structures game analysis along a strict three-tier architectural pipeline: **Actions** (micro physical inputs/verbs) $\rightarrow$ **Gameplay** (meso system rules and challenges) $\rightarrow$ **Experience** (macro psychological payoffs).

The 6–11 Framework provides the explicit theoretical content for the **Experience** tier in A.G.E.

| **A.G.E. Layer** | **System Scope** | **Mapping & Systemic Components**                                                                                                                                                                               |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Actions**      | Micro            | **Input Verbs:** Aim, shoot, reload, sprint, ping                                                                                                                                                               |
| **Gameplay**     | Meso             | **Rules & Constraints:** Enemy line-of-sight, ammunition limits, time-to-kill (TTK), extraction zone timer                                                                                                      |
| **Experience**   | Macro            | **6–11 Affective Engine:**<br>• _Triggered Instincts:_ Survival + Greed + Competition<br>• _Elicited Emotion Arc:_ Fear → Excitement → Pride<br>• _Terminal Payoff:_ Adrenaline release & competence validation |

#### Systemic Alignment Rules

1. **Mechanical Traceability:** Every low-level Action defined in A.G.E. must serve a Gameplay constraint that directly activates at least one of the 11 Primal Instincts.
    
2. **Experience Validation:** If an A.G.E. analysis reveals that a Gameplay loop fails to evoke a distinct 6–11 emotional arc, the loop is mechanically redundant or engaging in friction without payoff.
    

### 4.2 Integration with MDA & RMDA Frameworks

The **MDA Framework** (Mechanics, Dynamics, Aesthetics) and its extension, the **RMDA Framework** (Revised MDA), are foundational game design taxonomies. However, MDA’s "Aesthetics" layer often relies on broad, subjective categories (e.g., _Sensation, Fantasy, Narrative, Challenge, Fellowship, Discovery, Expression, Submission_).

Integrating 6–11 into MDA/RMDA replaces generic aesthetic taxonomy with quantifiable psychological mechanics.

|**MDA / RMDA Aesthetic Category**|**6–11 Primary Instinct Triggers**|**Elicited Emotional Arc**|**Systemic Design Target**|
|---|---|---|---|
|**Sensation**|Color / Sensory Appreciation|Instant Aesthetic Joy|Tactile feedback, hit stop, particle polish, adaptive audio|
|**Fantasy**|Self-Identification|Excitement → Pride|Role-play ownership, build specialization, aesthetic customization|
|**Challenge**|Competition + Survival + Revenge|Anger → Pride|Scaled difficulty gates, clear fail states, mastery validation|
|**Fellowship**|Communication + Protection|Connection → Shared Joy|Co-op synergy verbs, ping mechanics, team-based survival objectives|
|**Discovery**|Exploration / Curiosity|Anticipation → Joy|Unmarked secrets, fog of war, environmental storytelling|
|**Expression**|Self-Identification + Collecting|Excitement → Ownership|Modular cosmetics, housing systems, build diversity|
|**Submission (Abnegation)**|Collecting + Greed|Relaxed Joy / Satisfaction|Mindful grind loops, inventory sorting, routine resource farming|

#### Narrative Integration via RMDA

RMDA emphasizes narrative depth and player immersion. By applying 6–11 to RMDA, designers map narrative plot points directly to systemic mechanics:

- **Story Loss / Sacrifice:** Narrative beat triggers _Sadness_; mechanical loop engages _Protection / Care_ (defending the legacy/survivors), preventing narrative disconnect (ludonarrative dissonance).
    
- **Rivalry / Betrayal:** Narrative twist triggers _Anger_; mechanical loop activates _Revenge_ systems (Nemesis trackers or bounty quests) to give the player mechanical agency over story grievances.
    

### 4.3 Integration with the Clarity Model (UX & Cognitive Load)

The **Clarity Model** evaluates how effectively game state information is transmitted from the system to the player. It categorizes player mental processing through **Cognitive Load Theory**:

- **Intrinsic Load:** The desired mental effort required to master rules and solve challenges.
    
- **Germane Load:** The mental bandwidth used to build long-term skill schemas.
    
- **Extraneous Load:** Undesired cognitive friction caused by obscure UI, poor contrast, hidden rules, or delayed audio-visual feedback.

| **Design Metric**        | **High Clarity / Low Friction Path**                 | **Low Clarity / High Friction Path** |
| ------------------------ | ---------------------------------------------------- | ------------------------------------ |
| **Cognitive Processing** | Accurate Instinct Trigger _(Survival / Competition)_ | Extraneous Cognitive Overload        |
| **Systemic Challenge**   | Intrinsic Challenge                                  | Unintended UX Friction               |
| **Affective Outcome**    | **Intended Arc:** Fear → Excitement → Pride          | **Toxic State:** Anger & Confusion   |
| **Terminal Impact**      | Skill Mastery & Retention                            | Player Abandonment & Rage-Quitting   |
#### Systemic Interaction Rules

1. **Preserving Intrinsic Emotion:** To feel genuine **Fear** (Survival) or **Excitement** (Competition), the player must understand _why_ they are in danger. If a player dies due to muddy visual telegraphs, they experience **Extraneous Anger** aimed at the developer, rather than **Intrinsic Fear** aimed at the game world.
    
2. **Sensory Reinforcement (Instinct 11):** High visual readability and crisp audio cues immediately satisfy _Color / Sensory Appreciation_, converting cognitive parsing into instantaneous, intuitive action.
    

### 4.4 Integration with the DDE Model (Design, Dynamics, Experience)

The **DDE Model** emphasizes design intentionality, dynamic execution, accessibility, and universal usability.

When applied alongside 6–11:

- **Design Intent:** The designer specifies the targeted 6–11 emotional outcome during pre-production (e.g., "This level must move the player from _Fear_ to _Pride_ via _Protection_ mechanics").
    
- **Dynamics Audit:** Systems are playtested to verify that emergent behaviors actually activate the target instincts.
    
- **Universal Accessibility:** Accessibility settings (e.g., high-contrast UI, remappable controls, auto-hold toggles) reduce physical and sensory barriers without stripping away core 6–11 instinct triggers. For example, adding visual subtitle directionals preserves the _Survival_ instinct for hard-of-hearing players.
    

### 4.5 Integration with the DORK Model

The **DORK Model** focuses on player-centric decision-making, aligning player expectations through iterative prototyping, and balancing predictability with surprise.

| **Loop Stage**               | **Design Action**     | **Focus & Systemic Purpose**                                           |
| ---------------------------- | --------------------- | ---------------------------------------------------------------------- |
| **1. Player Expectations**   | Expectation Alignment | Mapping player expectations to core 6–11 instinct drives               |
| **2. Prototyping Iteration** | Grey-Box Build        | Implementing mechanics and rulesets for dynamic playtesting            |
| **3. 6–11 Affective Audit**  | Emotional Evaluation  | Auditing playtester affect (e.g., verifying _Excitement_ over boredom) |
| **4. Refine Mechanics**      | Systemic Tuning       | Eliminating friction and tuning feedback before cycling back           |

1. **Expectation Mapping:** Player genre expectations are rooted in instinctual desires (e.g., RPG players expect _Collecting_, _Self-Identification_, and _Exploration_).
    
2. **Iterative Affective Audits:** During grey-box prototyping, playtesters are evaluated not just for mechanical comprehension, but for emotional activation. If an exploration prototype produces boredom rather than _Excitement / Curiosity_, the DORK feedback loop triggers a redesign of environmental density or reward distribution.
    

### 4.6 Integration with the Emotioneering Model

Richard Freeman's **Emotioneering Model** provides techniques for infusing deep narrative emotion, character arc resonance, and player empathy into games.

Combining Emotioneering with 6–11 grounds narrative storytelling in mechanical interaction:

- **Empathy & Bond Building:** Narrative dialogue and character vulnerabilities trigger the _Protection / Care / Nurture_ instinct. When gameplay mechanics allow the player to heal, defend, or gift items to that NPC, emotional connection moves from passive observation to active agency.
    
- **Character Trauma & Morality:** Story beats that present heavy ethical dilemmas activate _Self-Identification_ and elicit **Sadness** or deep moral reflection, elevating the narrative experience above standard power fantasies.
    

### 4.7 Integration with the GEB Model (Gamified Educational Framework)

The **GEB Model** governs gamified learning, aligning educational outcomes with pedagogical engagement principles.

Educational games often fail when they rely on dry quiz mechanics wrapped in superficial points. The 6–11 Framework transforms educational design by driving learning through intrinsic primal instincts:

#### GEB Model Integration: Pedagogical Objectives & Affective Triggers

| GEB Pedagogical Objective         | 6–11 Instinct Engine                       | Resulting Emotional State     |
| :-------------------------------- | :----------------------------------------- | :---------------------------- |
| **Hypothesis Testing**            | Exploration / Curiosity (Uncovering rules) | Excitement → Joy              |
| **Knowledge Retention**           | Collecting (Cataloging concepts/cards)     | Pride (Mastery)               |
| **Skill Application**             | Competition (Peer benchmarks / speed runs) | Pride / Competence            |
| **Collaborative Problem Solving** | Communication (Team coordination)          | Shared Joy / Social Belonging |

### 4.8 Integration with the SSM Framework (System Space & Story Space)

The **SSM Framework** analyzes the interplay between **System Space** (ludic rules, mechanics, adaptive difficulty, state changes) and **Story Space** (narrative lore, world-building, character arcs).

A primary cause of player disconnect is dissonance between System Space and Story Space. The 6–11 Framework acts as the unifying psychological bridge ensuring emotional alignment between both spaces:

| **SSM Dimension**  | **Systemic & Narrative Components**                        | **6–11 Instinct Triggers** | **Elicited Emotion Arc**     |
| ------------------ | ---------------------------------------------------------- | -------------------------- | ---------------------------- |
| **System Space**   | Low health, intense boss attacks, scarce supplies          | Survival + Aggressiveness  | Fear / Excitement            |
| **Story Space**    | Protagonist is stranded, outnumbered, fighting for home    | Protection + Survival      | Fear / Desperation           |
| **Unified Output** | **HARMONIOUS IMMERSION** _(Zero Ludonarrative Dissonance)_ | Integrated Primal Drives   | Cohesive Emotional Resonance |

#### Cohesion Verification

- **Systemic-Narrative Synergy:** When System Space mechanics (e.g., permadeath or resource decay) trigger the _Survival_ instinct at the exact moment Story Space depicts an existential invasion, the player experiences total cognitive and emotional immersion.
    
- **Dissonance Prevention:** If Story Space frames a scenario as an urgent life-or-death crisis, but System Space provides infinite time, zero penalty, and easy mechanics, the _Survival_ instinct fails to trigger, exposing narrative artificiality.
    

### Cross-Framework Integration Summary Matrix

|**Framework / Model**|**Core Domain**|**6–11 Integration Function**|**Primary Value Delivered**|
|---|---|---|---|
|**A.G.E. Framework**|Mechanical Architecture|Powers the **Experience** tier from Actions & Gameplay|Traces micro inputs directly to macro emotional payoffs|
|**MDA / RMDA**|Systemic & Narrative Design|Defines explicit 6–11 psychological loops for **Aesthetics**|Replaces abstract aesthetic labels with actionable emotional mechanics|
|**Clarity Model**|UX & Cognitive Load|Ensures low extraneous load so **Instincts** trigger accurately|Prevents UI friction from causing unintended, toxic player anger|
|**DDE Model**|Design & Usability|Sets target emotional metrics for design intent & accessibility|Preserves core instinctual tension across inclusive control configurations|
|**DORK Model**|Player-Centric Iteration|Audits prototypes against expected instinctual drives|Validates emotional engagement during early grey-box playtesting|
|**Emotioneering**|Narrative Architecture|Anchors story empathy beats in interactive mechanical verbs|Bridges narrative character arcs with active player agency|
|**GEB Model**|Gamified Education|Converts educational tasks into intrinsic instinct loops|Drives learning through natural curiosity, collection, and mastery|
|**SSM Framework**|System vs. Story Space|Unifies System Space rules with Story Space narrative lore|Eliminates ludonarrative dissonance through shared affective targets|

## Mechanical Mapping Syntax & Industry Case Studies

To audit or author game mechanics using the 6–11 Framework, system architects trace interaction design through a standardized five-stage mapping pipeline:

$$\text{Action (Verb)} \longrightarrow \text{Gameplay Rule (System)} \longrightarrow \text{Triggered Instinct} \longrightarrow \text{Elicited Emotion} \longrightarrow \text{Terminal Payoff}$$

### 5.1 Standardized Tracing Pipeline

1. **Action (Micro / Verb):** Atomic physical player input or low-level command (e.g., _sprint_, _parry_, _loot_, _ping_, _craft_).
    
2. **Gameplay Rule (Meso / Constraint):** The systemic context, spatial constraint, timer, or AI rule governing that action (e.g., _tight parry window_, _3% drop rate_, _permadeath risk_).
    
3. **Triggered Instinct (Subconscious Drive):** The specific evolutionary drive stimulated by the mechanic (e.g., _Survival_, _Greed_, _Revenge_, _Protection_).
    
4. **Elicited Emotion (Affect State):** The primary psychological affect state produced during interaction (e.g., _Fear_, _Anger_, _Excitement_).
    
5. **Terminal Payoff (Macro Resolution):** The psychological state achieved upon successful execution or failure resolution (e.g., _Relief_, _Pride_, _Ownership_).
    

### 5.2 Genre Case Studies

#### Case Study A: Survival Horror / Extraction Base Building (_7 Days to Die_, _Escape from Tarkov_)

- **Primary Loop:** Day resource foraging shifting into night base defense and extraction survival.
    

|**Stage**|**Systemic Mapping**|
|---|---|
|**Action**|Harvesting metal/timber during daylight; barricading doorways at dusk.|
|**Gameplay Rule**|Nightfall increases AI aggressiveness by 300% and unlocks destructive horde behaviors against shelter walls.|
|**Triggered Instincts**|**Collecting** & **Exploration** (Daytime) → **Protection** & **Survival** (Nighttime)|
|**Elicited Emotion Arc**|Moderate **Excitement** (looting) → Acute **Fear** (nightfall hazard) → **Anger** (wall breach)|
|**Terminal Payoff**|Defending the structure until dawn resolves **Fear** into immense **Relief**, **Pride**, and base ownership.|

#### Case Study B: Tactical Action RPG / Boss Encounter (_Elden Ring_, _Dark Souls_)

- **Primary Loop:** High-difficulty boss encounter with multi-phase attack telegraphs and death penalties.
    

|**Stage**|**Systemic Mapping**|
|---|---|
|**Action**|Executing frame-perfect roll-dodges and heavy counter-attacks during recovery windows.|
|**Gameplay Rule**|Boss Phase 2 expands AoE hitboxes and increases damage output; death results in loss of unspent currency at the death marker.|
|**Triggered Instincts**|**Survival**, **Revenge**, **Aggressiveness**, and **Competition**|
|**Elicited Emotion Arc**|Defeat-induced **Anger** → Targeted **Revenge** drive → High-adrenaline **Excitement**|
|**Terminal Payoff**|Overcoming the boss transforms initial **Anger** and **Fear** into peak mechanical **Pride** and accomplishment.|

#### Case Study C: Hero Shooter / Ping & Co-op Synergies (_Apex Legends_, _Overwatch_)

- **Primary Loop:** High-speed squad combat relying on dynamic spatial awareness and team utility combos.
    

|**Stage**|**Systemic Mapping**|
|---|---|
|**Action**|Double-tapping the contextual ping button to flag an enemy flanker for teammates.|
|**Gameplay Rule**|Contextual ping places a distinct 3D visual marker and directional audio cue for all squad members without requiring voice chat.|
|**Triggered Instincts**|**Communication**, **Protection**, and **Aggressiveness**|
|**Elicited Emotion Arc**|Sudden **Fear** (spotted threat) → Social **Connection** (instant team alignment) → **Excitement**|
|**Terminal Payoff**|Collapsing on the target as a coordinated unit generates **Shared Joy** and tactical **Pride**.|

#### Case Study D: Gacha / Loot Box Progression System (_Genshin Impact_, _Diablo IV_)

- **Primary Loop:** Resource accumulation exchanged for randomized high-tier character/item drops.
    

|**Stage**|**Systemic Mapping**|
|---|---|
|**Action**|Spending accumulated premium currency to open a high-tier loot chest or gacha banner.|
|**Gameplay Rule**|Randomized drop table featuring a 0.6% drop rate for 5-star items with a 90-pull pity guarantee.|
|**Triggered Instincts**|**Greed**, **Collecting**, and **Color / Sensory Appreciation**|
|**Elicited Emotion Arc**|High-tension **Excitement** & anticipation → Gold visual light beam (Sensory Delight) → Sudden **Joy**|
|**Terminal Payoff**|Acquiring an elite item grants **Status Amplification** and reinforces the collection loop.|

### 5.3 Comparative Case Study Summary Matrix

|**Case Study / Genre**|**Primary Verbs**|**Key Instinct Triggers**|**Emotional Arc**|**Terminal Psychological State**|
|---|---|---|---|---|
|**Survival Horror**|Harvest, fortify, defend|Survival, Protection, Collecting|Fear → Tension → Relief|Relief & Shelter Pride|
|**Action RPG / Souls-like**|Dodge, parry, counter|Revenge, Aggressiveness, Survival|Anger → Excitement → Pride|Systemic Mastery & Exhilaration|
|**Hero Shooter**|Aim, ping, combo|Communication, Protection|Fear → Connection → Joy|Coordinated Team Pride|
|**Extraction / Loot**|Loot, open, extract|Greed, Collecting, Sensory|Excitement → Fear → Joy|Status Amplification & Wealth|


## Practical Implementation Checklist & Designer Workflow

To integrate the 6–11 Framework into an active game design pipeline, game directors and systems designers can follow a four-phase evaluation and tuning workflow. This process ensures that mechanics consistently engage subconscious instincts and resolve into meaningful emotional payoffs without causing player fatigue or frustration.

|**Phase**|**Audit Stage**|**Core Objective & Design Actions**|
|---|---|---|
|**Phase 1**|**Target Definition**|Define target emotional arc and core instinct triggers|
|**Phase 2**|**Mechanical Mapping**|Align atomic verbs and rules to selected instincts|
|**Phase 3**|**Pacing & Arc Audit**|Verify tension-and-release cycles (resolve negative states)|
|**Phase 4**|**Sensory Polish**|Elevate signals through visual/audio sensory appreciation|

### 6.1 Phase-by-Phase Design Workflow

#### Phase 1: Target Experience Definition

- **Identify Core Affective Objectives:** Define the exact emotional states the feature or level must produce (e.g., "This dungeon must shift the player from initial _Fear_ to eventual _Pride_").
    
- **Select Instinct Anchors:** Pick 2–4 primary instincts to drive the feature loop (e.g., _Survival_ + _Exploration_ + _Protection_). Avoid attempting to trigger all 11 instincts simultaneously in a single mechanic, as this dilutes design focus.
    

#### Phase 2: Mechanical Tracing & Rule Alignment

- **Audit Verbs Against Instincts:** Trace every low-level action (e.g., _crouch_, _harvest_, _parry_, _upgrade_) to confirm it directly services a target instinct.
    
- **Eliminate Frictionless Loops:** If an action satisfies an instinct without systemic friction or risk (e.g., resource collecting with zero inventory limits, zero hazards, and instant pickups), the loop risks collapsing into mindless repetition rather than evoking _Joy_ or _Pride_.
    

#### Phase 3: Emotional Pacing & Resolution Audit

- **Track the Tension/Release Cycle:** Ensure high-tension negative emotions (**Fear**, **Anger**) intentionally resolve into positive terminal states (**Pride**, **Relief**, **Joy**).
    
- **Mitigate Sensory Fatigue:** Prolonged high **Excitement** or constant **Fear** without calm intermissions causes emotional burnout. Insert quiet recovery zones (e.g., safe hubs, campfire rests, inventory sorting space) to reset player affect.
    
- **Prevent Toxic Anger:** Distinguish between _Intrinsic Challenge_ (fair difficulty that fuels the _Revenge_ instinct) and _Extraneous Friction_ (bad telegraphing, broken controls, or unclear rules). Extraneous friction causes toxic anger aimed at the developers rather than productive determination aimed at the game.
    

#### Phase 4: Sensory Polish & Feedback Escalation

- **Leverage Color & Audio (Instinct 11):** Use visual hierarchy, color coding (e.g., item rarity tiers), particle effects, and dynamic audio cues to reinforce mechanical success.
    
- **Juice Core Interactions:** Enhance the instant tactile feel of high-stakes actions (e.g., hit stop on a heavy attack, bass-heavy audio stingers on quest completion).
    

### 6.2 Designer Evaluation Checklist

#### 6–11 Feature Audit Checklist

#### 1. Instinct Alignment
- [ ] Does the core feature clearly stimulate at least 2 primal human instincts?
- [ ] Are player verbs directly tied to fulfilling or defending those instincts?
- [ ] Is there clear mechanical friction preventing instant, unearned instinct satisfaction?

#### 2. Emotional Arc & Pacing
- [ ] Does the feature establish a clear emotional arc (e.g., Fear → Tension → Relief)?
- [ ] Are negative emotional states (Fear, Anger) provided with clear, actionable paths to positive resolution (Pride, Joy)?
- [ ] Is there an appropriate "pacing break" following high-tension emotional spikes?

#### 3. Systemic Harmony & Clarity
- [ ] Are all telegraphs, hazards, and rewards visually and auditorily distinct (Clarity Model compliance)?
- [ ] Is player anger driven by intrinsic game challenge rather than confusing UI/UX?
- [ ] Does the feedback design leverage Color / Sensory Appreciation to amplify victory moments?

