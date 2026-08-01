---
{"dg-publish":true,"permalink":"/game-design/genre-dissection/the-genre-execution-and-scoping-blueprint/","dg-note-properties":{}}
---

# The Scope Reality of Genre Selection

When a team selects a target genre for a new project, they are doing far more than establishing a creative direction or player fantasy. They are locking in the **technical, financial, and ergonomic boundaries** of their entire production pipeline.

Every genre carries an invisible, non-negotiable footprint:
* A **Fighting Game** demands frame-accurate input processing, specialized hit-box collision engines, and rollback netcode architecture before a single character is modeled.
* An **Open-World Survival Crafting** game demands spatial streaming systems, vast asset generation pipelines, and deep inventory state serialization.
* A **Grand Strategy Game** demands asynchronous simulation thread management, complex AI evaluation loops, and high-density UI readability frameworks.

Pre-production failure rarely occurs because a team lacks creative ideas; it occurs because the team underestimates the baseline load-bearing technical demands of their chosen genre.

#### Genre as a Resource Constraint

Choosing a genre immediately locks in three major operational budgets:

| Operational Budget | Production Impact | Typical Scoping Failure |
| :--- | :--- | :--- |
| **Verb & Ergonomic Budget** | Limits how many simultaneous actions a player can perform without input thrashing or controller fatigue. | Bloating the control scheme with secondary verbs, leading to physical input paralysis. |
| **Technical Architecture Budget** | Defines the mandatory engineering prerequisites (netcode, state serialization, physics engines, spatial streaming) required for the engine. | Attempting to build a genre on an engine architecture ill-suited for its baseline execution needs. |
| **Asset & Content Pipeline Budget** | Dictates the sheer volume of art, audio, animation, and level design required to satisfy player expectations for genre length. | Underestimating the asset generation throughput required for open-world or story-driven RPG genres. |


#### The Feature Creep Trap

A common pitfall in pre-production is treating genre conventions as an à la carte menu of "standard features." Designers often assume that because a benchmark title includes a crafting system, skill trees, dodge rolls, and dynamic weather, their project must include all of them to be competitive.

Adding features without auditing their **verb density** and **architectural cost** creates severe scope bloat. Every added mechanic introduces:
1. Additional physical buttons the player must manage on a controller.
2. New edge-case interactions that must be debugged, balanced, and maintained.
3. Increased maintenance overhead for engineering and QA teams.

#### The Core Thesis

> **The Scoping Mandate:** Successful game execution is not about how many features you can pack into a genre; it is about strictly enforcing your **Verb Budget**, defining your **Minimum Viable Loop (MVL)**, and securing your **Technical Architecture** before writing a single line of production content.


# Verb Budgeting & Cognitive Ergonomics

Every interaction in a video game requires cognitive processing and physical execution from the player. **Verb Budgeting** is the pre-production discipline of capping the total number of actions a player must track and execute simultaneously, preventing input paralysis, controller thrashing, and physical fatigue.

#### 2.1 The Three-Tiered Verb System

To manage cognitive load effectively, categorize every action verb in your design into one of three operational tiers:

| Verb Tier | Execution Cadence | Cognitive Load | Typical Control Mapping | Examples |
| :--- | :--- | :--- | :--- | :--- |
| **Primary Verbs** | High frequency (multiple times per second or minute). | Muscle memory / Reflexive. | Triggers (RT/LT), face buttons, primary mouse buttons. | Jump, Shoot, Light Attack, Move, Accelerate. |
| **Secondary Verbs** | Moderate frequency (tactical or cooldown-based). | Situational awareness / Strategic choice. | Shoulder bumpers (RB/LB), D-Pad, secondary keys. | Dodge Roll, Reload, Special Ability, Cover, Quick-Swap. |
| **Tertiary Verbs** | Low frequency (meta-game or paused state). | Analytical / Strategic planning. | Start/Select, Touchpad, sub-menus, mouse UI. | Inventory Management, Skill Trees, Map Scouting, Quest Logs. |

##### The Verb Saturation Warning
> **The Rule of Ergonomic Overload:** If a game forces players to manage more than **3 Primary Verbs** simultaneously during high-velocity gameplay, execution error rates spike exponentially. Secondary verbs must complement, never fight for inputs with, primary verbs during intense encounters.

#### 2.2 Input Mapping & Physical Ergonomics

Physical control schemes operate under strict hardware constraints. Designing a control layout requires auditing physical ergonomics on modern input devices:

1. **Thumb-Stick Contention:** A player cannot manipulate the right thumb-stick (camera aim) while simultaneously pressing face buttons (A, B, X, Y / Cross, Circle, Square, Triangle) unless using an ergonomic modifier (like a claw grip or rear paddles). Mapping a primary aim-dependent verb to a face button forces input thrashing.
2. **Hold vs. Tap Latency:** When two verbs share a single button via hold vs. press states (e.g., Press to Tap Reload, Hold to Interact), input latency is introduced because the engine must wait for hold-threshold timers to resolve before executing the action.
3. **Finger Density Limits:** A standard controller layout comfortably supports **4 simultaneously ready index/middle finger inputs** (LB/RB/LT/RT). Assigning time-critical dodge or reaction verbs to D-Pad inputs forces players to temporarily abandon movement control on the left thumb-stick.

##### Target Hardware Constraints

Verb budgets and control layouts must adapt strictly to the physical input medium of your primary platform:

* **Console Gamepads:** High ergonomic comfort for spatial analog movement, but limited face-button density during camera tracking. Primary active verbs must live on triggers and bumpers.
* **PC (Keyboard & Mouse):** Extremely high verb density budget via dedicated hotkeys and precision mouse aiming, but lacks analog movement resolution (binary WASD directionality).
* **Mobile Touch Controls:** Lowest verb density budget. Lacks tactile physical feedback, requiring virtual thumb-stick areas to be cleared of action buttons and relying heavily on contextual tap targets, swipes, or auto-fire automation.

#### 2.3 The Verb Budgeting Matrix by Genre

Parent genres dictate the safe upper boundary for active verb density based on their baseline pacing and tension curves:

| Parent Genre                      | Max Active Primary Verbs | Max Secondary Verbs | Primary Ergonomic Bottleneck                                             | Benchmark Exemplar                  |
| :-------------------------------- | :----------------------: | :-----------------: | :----------------------------------------------------------------------- | :---------------------------------- |
| **Arena Shooter / FPS**           |          2 – 3           |        4 – 5        | Aim precision vs. jump/slide movement (requires trigger/bumper mapping). | *DOOM Eternal*, *Titanfall 2*       |
| **Character Action / Soulslike**  |            3             |        4 – 6        | Camera tracking during lock-on vs. dodging/attacking.                    | *Devil May Cry 5*, *Elden Ring*     |
| **Real-Time Strategy (RTS)**      |          4 – 6           |    10+ (Hotkeys)    | High Actions-Per-Minute (APM) requirement and spatial selection bounds.  | *StarCraft II*, *Age of Empires IV* |
| **Turn-Based RPG / Strategy**     |  Unlimited (Menu-gated)  |      Unlimited      | Cognitive menu density rather than physical execution speed.             | *Persona 5*, *Tactics Ogre*         |
| **Platformer / Precision Action** |            2             |        2 – 3        | Frame-accurate jump timing synchronized with spatial navigation.         | *Celeste*, *Hollow Knight*          |


# The Minimum Viable Loop (MVL) Audit

A primary driver of scope bloat in pre-production is the inability to distinguish between a genre’s **load-bearing systemic mechanics** and its **surface-level trim**. 

The **Minimum Viable Loop (MVL)** is the absolute smallest, most isolated combination of interaction mechanics required for a prototype to feel authentically like its target genre, *before* adding meta-progression, inventory crafting, skill trees, or narrative cutscenes.

#### 3.1 Isolating the Baseline Core

While a Minimum Viable Product (MVP) tests commercial market viability, a Minimum Viable Loop (MVL) tests **core mechanical fun and genre identity** in a greybox state.

If a game’s core interaction loop is not engaging in a gray block environment with zero art, sound, or numerical progression systems, adding secondary systems will only obscure underlying design flaws.

##### The MVL Isolation Test
To find your project's MVL, strip away systems until removing one more mechanic destroys the basic genre identity:

1. **Start with the full feature list:** Write down every planned mechanic (e.g., dodge, light attack, heavy attack, weapon crafting, health potions, lock-on, skill tree).
2. **Apply the Removal Audit:** Ask: *"If we strip this system completely out of a greybox prototype, does the game cease to function as [Target Genre]?"*
3. **Isolate the Core Engine:** The remaining 2 to 3 mechanics constitute your load-bearing baseline loop.

#### 3.2 Load-Bearing Mechanics vs. Surface Trim

Pre-production scoping requires categorizing planned features into structural necessities versus optional polish:

| Feature Category | Definition | Impact on Scope & Architecture | Examples by Genre |
| :--- | :--- | :--- | :--- |
| **Load-Bearing Mechanics** | Core interaction rules that define the fundamental spatial, tactical, or execution challenges of the genre. | **Non-Negotiable:** Must be prototyped, tuned, and architected first during pre-production. | • Precision collision & jump curves (Platformers)<br>• Frame-accurate hit/hurtboxes (Fighting Games)<br>• Resource generation & unit caps (RTS) |
| **Surface Trim & Meta Systems** | Secondary progression, customization, or visual layers wrapped around the primary loop. | **Negotiable:** Can be scaled, delayed, or cut entirely during production without breaking core playability. | • Weapon crafting sub-menus<br>• Stat-allocated talent trees<br>• Dynamic cosmetics & skin unlocks |

##### The Surface Trim Delusion
> **The Feature Mirage:** Designers often attempt to fix an unengaging core loop by adding surface trim (e.g., *"Combat feels a bit flat, but once we add loot drops and crafting, it will be fun"*). Secondary progression systems only amplify the quality of an existing loop; they cannot save a broken foundation.


#### 3.3 The MVL Stripping Exercise

To build an efficient execution plan, analyze benchmark titles in your target genre to identify their true, stripped-down MVL:

| Landmark Title | Full Release Feature Set | Stripped Minimum Viable Loop (MVL) | Lessons for Scoping |
| :--- | :--- | :--- | :--- |
| ***Vampire Survivors*** | Hundreds of weapons, achievements, passive items, character unlocks, stage hazards. | **Top-down directional movement + auto-firing directional projectiles against swelling hit-box clusters.** | The entire addictive core functions purely on spatial positioning and auto-trigger collision rules. |
| ***Monster Hunter: World*** | Deep gear crafting trees, cat companions, tracking bugs, camp cooking, story quests. | **Telegraphed weapon animation commitment vs. large monster hit-box patterns.** | Everything in the meta-game serves to funnel the player back into a high-stakes timing and spatial positioning test. |
| ***Hades*** | Boons, Olympian lore choices, weapon aspects, mirror progression, dialogue trees. | **Isometric dash-strike execution in a randomized arena layout.** | The fluid movement and hit-confirm cadence make fighting enjoyable even without meta-progression unlocks. |

#### The MVL Audit Checklist

Before exiting pre-production, ensure your core loop passes three basic checks:

* **The Greybox Test:** Can a player enjoy the core loop for 10 minutes in an untextured grey room with zero sound effects or UI UI popups?
* **The Progression Isolation Test:** Is the loop intrinsically rewarding without numerical stat increases or XP rewards?
* **The Single-Verb Validation:** Is your primary interaction verb expressive enough on its own to sustain tactical decision-making?


# Technical & Architectural Dependencies by Genre

Long before graphics rendering or narrative design begins, selecting a target genre dictates the core engineering architecture of your game engine. Attempting to force a genre onto an engine architecture ill-suited for its baseline demands results in severe performance bottlenecks, uncontrollable tech debt, or outright project cancellation.

Engine architecture must be chosen based on four critical technical vectors: **Netcode Topology**, **State Serialization**, **Spatial Streaming**, and **Physics Determinism**.

#### 4.1 Networking & Netcode Architecture

Multiplayer genres live or die by their network architecture. Netcode cannot be effectively "plugged in" late in development; it dictates how the engine processes inputs, syncs states, and handles latency.

* **Rollback Netcode (Frame-Accurate Execution):** Mandatory for Fighting games, Platform Fighters, and Precision Brawlers. The local client predicts inputs immediately, executing actions without latency. If remote inputs mismatch, the simulation "rolls back" game state seamlessly to correct discrepancies. Requires ultra-fast engine state saves and rewinds per frame.
* **Deterministic Lockstep (High-Entity Count Strategy):** Mandatory for RTS and MOBAs with thousands of simultaneous units. Instead of transmitting position data for 2,000 units every tick, players transmit only micro-second input commands. Demands 100% deterministic math logic across different CPUs to prevent desynchronization.
* **Server-Authoritative Client Prediction (Shooters & Battle Royales):** The server holds the ground truth of player positions and ballistics. The client predicts movement locally to mask latency, while the server reconciliation algorithm corrects discrepancies. Essential for anti-cheat protection and hit registration validity.

##### Cross-Platform Latency & Hardware Variance

When targeting cross-platform multiplayer (PC, Console, Mobile), network architecture must accommodate significant hardware performance differentials:

* **Floating-Point Non-Determinism:** Different CPU architectures (x86 vs. ARM) process floating-point math calculations differently. Lockstep architectures cross-playing between PC and Mobile must enforce fixed-point math libraries to prevent desynchronization.
* **Framerate & Latency Asymmetry:** Pairing a 144Hz PC client with a 30Hz or variable-framerate mobile/last-gen console client creates severe input buffer spikes. Server reconciliation algorithms must implement dynamic tick-rate adjustments and input buffer smoothing to prevent high-framerate players from gaining unfair spatial advantages.

#### 4.2 Engine Serialization & Systemic State Complexity

Single-player and simulation genres face massive CPU overhead not from rendering pixels, but from tracking state changes across thousands of dynamic game entities.

* **Deep State Serialization (RPGs, Grand Strategy, Colony Sims):** Games like *RimWorld*, *Crusader Kings III*, or *Civilization* must serialize millions of variable state values, NPC relationships, persistent item durability, world tile stats, and inventory arrays, into save files instantly without crashing memory or causing save-file bloat.
* **Asynchronous Simulation Threading:** Complex systemic games require decoupled simulation pipelines. The core AI pathfinding or economy simulation must run asynchronously on separate CPU worker threads so that frame rates do not drop when processing thousands of background NPC decisions.

#### 4.3 Spatial Streaming & Physics Engines

Action, Racing, and Open-World genres place massive stress on GPU memory bandwidth, level-streaming sectors, and collision geometry processing.

* **Continuous Spatial Streaming (Open-World / High-Speed Racing):** Requires dynamic memory management architectures (Level-of-Detail (LOD) swapping, memory cell loading/unloading, and occlusion culling) that can stream vast world data into RAM continuously without causing visual hitching or frame drops during fast traversal.
* **Physics Determinism & Hitbox Geometry:** Precision action games (*Souls*-likes, Character Action, Racing Sims) rely on high-frequency physics ticks and sub-frame collision evaluation. Simple bounding-box colliders are insufficient; engines require custom spatial partition structures (like BVH trees) to handle high-velocity raycasts and complex mesh collisions without phase-through bugs.

#### 4.4 The Technical Dependency Matrix

Map your intended parent genre to its non-negotiable engineering prerequisites during pre-production to avoid engine misalignment:

| Parent Genre | Primary Engineering Prerequisite | Network Architecture Demand | Engine Failure Vector | Benchmark Exemplar |
| :--- | :--- | :--- | :--- | :--- |
| **Fighting / Brawler** | Sub-frame rollback engine & dynamic state rewinding. | Rollback Netcode (GGPO pattern). | Input delay, frame drops during network sync, hit-box desync. | *Guilty Gear -Strive-*, *Street Fighter 6* |
| **Real-Time Strategy (RTS)** | Deterministic simulation math & multi-thread pathfinding. | Deterministic Lockstep. | Desynchronization locks, pathfinding grid lockup under high unit loads. | *StarCraft II*, *Stormgate* |
| **Grand Strategy / Colony Sim** | Deep object serialization & thread-decoupled AI loops. | Peer-to-Peer or Server state sync. | Severe late-game turn lag, save file corruption, memory leaks. | *Crusader Kings III*, *RimWorld* |
| **Tactical / Hero Shooter** | Server-authoritative hit-validation & client prediction. | Dedicated Servers + Client-side reconciliation. | Peeker's advantage, un-telegraphed hit registration, client exploitation. | *VALORANT*, *Counter-Strike 2* |
| **Open-World Survival Craft** | Asynchronous spatial streaming & persistent world state persistence. | Client-Server spatial partition sync. | Memory hitching during fast traversal, floating entity physics, world sync loss. | *Valheim*, *Rust* |


# Sensory Feedback & Pacing Alignment

A game’s execution loop does not end with code and input processing, it completes when the player receives and processes visual, auditory, and haptic feedback. **Sensory Feedback Alignment** ensures that the cadence, density, and clarity of in-game feedback match the temporal demands of the target genre.

#### 5.1 Frame-Accurate Feedback (Twitch & Execution Genres)

In high-velocity action genres (Fighting, Soulslike, Character Action, FPS), feedback must operate on sub-second or frame-accurate time scales. If sensory cues arrive too late or lack physical weight, the player perceives the game as sluggish, unresponsive, or unfair.

##### Key Feedback Mechanisms for Action Pacing:
* **Hit-Stop (Freeze Frames):** Pausing the movement of attacker and defender for 2–6 frames upon impact. Hit-stop communicates weapon weight and impact severity, confirming hit connection without delaying overall input processing.
* **Input Buffering:** Storing button presses made during an non-interruptible animation frame (e.g., during recovery from a dodge roll) and executing them on the very first actionable frame. This eliminates perceived "dropped inputs" and creates fluid control feel.
* **Telegraphing Cadences (Wind-up, Active, Recovery):** Animation design must clearly segment combat actions into readable phases:
  1. **Wind-up (Anticipation):** Distinct visual and audio cues warning the player of an incoming threat.
  2. **Active Phase (Execution):** The precise frames where hitboxes and hurtboxes collide.
  3. **Recovery (Vulnerability):** The post-attack cooldown phase where counter-play is possible.

#### 5.2 Environmental & UI Legibility (Strategy & Simulation Genres)

In low-velocity or high-complexity genres (RTS, Grand Strategy, Simulation, Turn-Based RPGs), the primary challenge shifts from frame-accurate reflexes to **information processing**. Sensory feedback must prioritize legibility and structural hierarchy over visual spectacle.

##### Managing Information Density:
* **HUD Visual Hierarchy:** Critical alerts (resource shortages, unit casualties, immediate threats) must occupy primary visual real estate, while ambient data (background economic growth, passive stats) is nested into secondary sub-menus or tooltips.
* **Visual Noise Reduction:** In tactical combat or macro management views, particle effects and environmental geometry must yield to entity readability. Over-rendering visual fluff obscures key tactical states.
* **Audio Layering & Ducking:** Prioritizing tactical cues (voice lines for "Unit Under Attack") over ambient background music or combat sound effects during high-intensity tactical events.

#### Sensory Feedback Alignment Matrix by Genre

| Parent Genre | Primary Feedback Cadence | Critical Feedback Tool | Common Sensory Failure Mode | Benchmark Exemplar |
| :--- | :--- | :--- | :--- | :--- |
| **Fighting / Brawler** | Frame-accurate (16ms windows) | Hit-stop, directional hit-sparks, audio impact cues. | Floatiness; lack of impact weight on successful hits. | *Street Fighter 6*, *Tekken 8* |
| **Action RPG / Soulslike** | Telegraphed animation phases | High-contrast wind-up animations, distinct audio cues. | Visual clutter obscuring boss wind-up tells. | *Elden Ring*, *Nioh 2* |
| **Real-Time Strategy (RTS)** | Systemic state notifications | Distinct audio barks, mini-map ping flashes, color-coded health bars. | Audio clutter; critical notifications buried under minor alerts. | *StarCraft II* |
| **Colony Sim / Grand Strategy** | Data density hierarchy | Progressive tooltips, color-coded status badges, ambient UI alarms. | Visual noise; vital stats hidden deep in nested menus. | *RimWorld*, *Crusader Kings III* |


# The Genre Execution Audit (Diagnostic Worksheet)

Before committing engineering and art resources to production, run your game concept through this four-step diagnostic execution audit. This framework evaluates whether your project’s scope, verb budget, and technical architecture align with production realities.

#### 6.1 The 4-Step Scoping & Execution Audit

Evaluate your project proposal sequentially through each diagnostic stage. Apply the required corrective action if any stage fails before greenlighting production assets.

| Audit Stage | Diagnostic Action | Passing Threshold | Corrective Action if Failed |
| :--- | :--- | :--- | :--- |
| **1. Verb Isolation & Budget Check** | Map out all primary, secondary, and tertiary verbs across your target controller layout. | Active primary verbs do not exceed the genre’s ergonomic density cap; no thumb-stick contention. | Cut secondary verbs or move time-critical actions off face buttons to dedicated triggers/bumpers. |
| **2. MVL Boundary Verification** | Strip all meta-progression, crafting, and visual polish from a greybox prototype. | The core loop remains inherently engaging for 10+ minutes without stat scaling or UI rewards. | **Stop:** Redesign core interaction mechanics; do not attempt to fix a flat loop with loot or skill trees. |
| **3. Technical Dependency Alignment** | Audit engine capabilities against non-negotiable genre technical prerequisites (netcode, serialization, streaming). | Engine architecture natively supports required netcode, serialization, or spatial streaming protocols. | Refactor engine baseline architecture immediately or select a game engine purpose-built for the genre. |
| **4. Ergonomic Stress Test** | Test greybox control schemes during high-velocity scenarios with target input hardware. | Zero input thrashing, dropped inputs, or awkward hand contortions during 30 minutes of continuous play. | Re-map inputs, implement input buffering, or adjust animation wind-up/recovery frame windows. |


#### 6.2 The Execution Risk & Scope Scorecard

Use this scoring rubric during greenlight reviews to evaluate your project’s scope risk profile before entering full production:

| Assessment Dimension | Rating Scale | Evaluation Criteria |
| :--- | :---: | :--- |
| **Verb Budget Discipline** | 1 – 5 | Are player interaction verbs cleanly categorized and within safe ergonomic limits? |
| **MVL Independence** | 1 – 5 | Is the greybox prototype intrinsically fun without relying on meta-progression or surface trim? |
| **Technical Alignment** | 1 – 5 | Does the target engine natively support the genre’s core networking, physics, and state requirements? |
| **Pipeline Feasibility** | 1 – 5 | Can your team realistic generate the required asset volume and content length for this genre? |
| **Total Execution Score** | **/ 20** | Sum of all four dimension ratings. |


#### Risk Level & Production Recommendation

| Total Score | Risk Level | Production Recommendation |
| :--- | :--- | :--- |
| **16 – 20** | **Low Risk** | **Greenlight:** High execution alignment. Scope is well-bounded, technical architecture is secure, and verbs are ergonomically tuned. |
| **11 – 15** | **Moderate Risk** | **Proceed with Safeguards:** Scope risk detected. Trim secondary verbs, secure technical prerequisites, or reduce target content length. |
| **5 – 10** | **Critical Risk** | **Stop & Redesign:** High risk of project cancellation. Severe mismatch between genre demands, engine architecture, or team resources. |


#### 6.3 Worked Case Study: "Project Aegis" (Ambitious Action-Crafting Pitch)

To see how the execution audit functions in practice, let's run a high-concept pitch through the framework.

##### Concept Elevator Pitch
> *"A high-speed, multiplayer 3D Character Action Game featuring frame-accurate sword combat, real-time voxel terraforming, deep survival crafting skill trees, and 100-player Battle Royale matches."*

##### Step-by-Step Diagnostic Audit

| Audit Stage | Diagnostic Assessment | Result |
| :--- | :--- | :---: |
| **1. Verb Isolation & Budget Check** | **Failure:** Tries to combine high-speed sword combos (3 primary verbs) with real-time building/voxel editing (4 secondary verbs) on one controller layout, causing extreme input thrashing. | **FAIL** |
| **2. MVL Boundary Verification** | **Failure:** The core sword combat feels clunky without the stat boosts and elemental weapon crafts unlocked in the mid-game skill tree. | **FAIL** |
| **3. Technical Dependency Alignment** | **Failure:** Frame-accurate sword combat requires Rollback Netcode, while 100-player voxel terraforming requires Server-Authoritative spatial partitioning. Combining both in one engine tick creates an impossible netcode conflict. | **FAIL** |
| **4. Ergonomic Stress Test** | **Failure:** Players must abandon camera control on the right stick to cycle building materials while dodging boss attacks. | **FAIL** |

##### Scorecard Evaluation (Initial Pitch)

| Assessment Dimension | Rating | Diagnostic Justification |
| :--- | :---: | :--- |
| **Verb Budget Discipline** | **1 / 5** | Severe verb saturation; attempts to layer complex building controls on top of twitch melee combat. |
| **MVL Independence** | **2 / 5** | Core melee loop relies on numerical progression to mask underlying timing issues. |
| **Technical Alignment** | **1 / 5** | Unreconcilable netcode collision between rollback melee state rewinds and 100-player voxel sync. |
| **Pipeline Feasibility** | **1 / 5** | Asset generation scope for a 100-player voxel open world exceeds team production throughput. |
| **Total Score** | **5 / 20** | **Critical Risk: Immediate Cancel or Complete Scope Pivot.** |

##### Corrective Resolution (Applying Scope Safeguards)

The team executes a radical scoping pivot to align technical requirements with their core strengths:

1. **Scope Refocus:** Drop the 100-player Battle Royale, voxel terraforming, and survival crafting systems entirely.
2. **Genre Re-alignment:** Re-scope as a **4-Player Cooperative Boss-Rush Action Game**.
3. **Verb Budget Correction:** Cap active primary verbs to 3 (Light Attack, Heavy Attack, Dodge Roll) mapped cleanly to triggers/bumpers to preserve camera control.
4. **Technical Alignment:** Utilize Server-Authoritative netcode optimized for small 4-player co-op lobby instances with high-frequency hit validation.

> **Post-Correction Compatibility Score:** **18 / 20 (Greenlight)**


# Architectural Execution Blueprints

To translate pre-production scoping theory into production reality, game teams should utilize established **architectural execution patterns**. These proven structural frameworks insulate development pipelines from scope creep, input ergonomic failures, and technical architecture deadlocks.

#### Pattern 1: The Vertical Slice MVL

* **The Core Mechanism:** Build and lock in the Minimum Viable Loop (MVL) in a completely isolated, untextured greybox environment before writing code for meta-progression, inventory management, or narrative cutscenes.
* **How It Protects Production:** Prevents teams from spending months building secondary content (item databases, skill trees, cosmetic assets) around an interaction loop that is fundamentally unengaging.
* **Architectural Execution:**
  1. Strip all visual art and numerical stat scaling from the test build.
  2. Implement strictly the primary interaction verbs and primary enemy/hazard reactions.
  3. Require the build to pass a 10-minute engagement audit with internal playtesters before approving secondary system development.
* **When NOT to Use This Pattern:** Purely narrative or choice-driven genres (Visual Novels, Interactive Fiction) where mechanical verb loops are secondary to dialogue trees and story pacing.
* **Exemplars:**
  * ***Celeste*: ** The jump, dash, and wall-climb physics were tuned for months in a minimalist block environment to ensure movement felt perfect before full level production began.
  * ***DOOM (2016)*:** The "Push-Forward Combat" loop (glory kills, mobility, resource drops) was validated in greybox combat arenas prior to building campaign environments.

#### Pattern 2: Systemic Modular Staging

* **The Core Mechanism:** Decouple core low-level engineering (netcode, physics, hitboxes, state serialization) from high-level content pipelines (level design, quest scripts, character modeling).
* **How It Protects Production:** Prevents content creators from building assets on unstable engineering foundations that will later change, causing massive rework and asset trashing.
* **Architectural Execution:**
  1. Freeze engine architecture updates (e.g., netcode protocols or collision partition structures) into stable releases.
  2. Expose modular data structures (ScriptableObjects, JSON schemas, Data Tables) to content designers so balance tweaks do not require engine code re-compilation.
* **When NOT to Use This Pattern:** Rapid, single-developer game jam projects where the overhead of decoupling systems creates unnecessary architectural overhead.
* **Exemplars:**
  * ***StarCraft II*: ** The deterministic engine architecture and unit data tables were completely finalized before mass production of campaign missions and unit models began.
  * ***Slay the Spire*: ** Card effect logic, status conditions, and relic triggers were built as modular data-driven hooks, allowing rapid content iteration without altering engine code.

#### Pattern 3: The Input Ergonomics Buffer

* **The Core Mechanism:** Map and stress-test control schemes on raw input primitives (gamepads, keyboard/mouse layouts) during peak-intensity scenarios *before* finalizing animation state machines.
* **How It Protects Production:** Prevents input thrashing, thumb-stick contention, and finger fatigue late in development when re-mapping controls would break existing animation timing and UI prompts.
* **Architectural Execution:**
  1. Map all primary, secondary, and tertiary verbs onto a physical controller heat-map.
  2. Verify that no time-critical secondary verb requires abandoning camera aim on the right thumb-stick unless an automatic lock-on camera system is active.
  3. Enforce strict input buffering windows (100ms–200ms) to ensure actions queue smoothly during recovery frames.
* **When NOT to Use This Pattern:** Turn-based or menu-driven genres where real-time physical execution latency and thumb-stick contention are non-factors.
* **Exemplars:**
  * ***Monster Hunter: World*: ** Radial menus and directional input buffers were specifically engineered to allow complex item usage without abandoning character movement during high-velocity hunts.
  * ***Titanfall 2*: ** Wall-running, slide-hopping, and aiming were mapped to maintain continuous thumb placement on movement and camera controls.

#### Pattern 4: Asset Scalability Gates

* **The Core Mechanism:** Establish modular, procedural, or reusable asset generation pipelines that scale content volume to match genre length expectations without linear team headcount growth.
* **How It Protects Production:** Prevents small or mid-sized teams from choking on the massive content generation demands of open-world, RPG, or simulation genres.
* **Architectural Execution:**
  1. Calculate the target game length (e.g., 20 hours) and determine required content density (e.g., unique encounters per hour).
  2. Build modular tile-sets, procedural layout tools, or systemic encounter tables that allow designers to construct varied scenarios from reusable primitives.
* **When NOT to Use This Pattern:** Hand-crafted, bespoke puzzle games (*The Witness*, *Baba Is You*) where content cannot be procedurally or modularly generated without ruining puzzle logic.
* **Exemplars:**
  * ***Deep Rock Galactic*: ** Combines procedurally generated cave networks with modular objective seeds, yielding near-infinite replayability with a compact art pipeline.
  * ***Dead Cells*: ** Uses hand-crafted combat room tiles stitched together procedurally to deliver the feel of a bespoke Metroidvania with infinite run variety.

#### Execution Pattern Summary Matrix

| Pattern Name | Core Friction Solved | Structural Execution | When NOT to Use | Benchmark Exemplar |
| :--- | :--- | :--- | :--- | :--- |
| **The Vertical Slice MVL** | Building secondary systems around a flat core loop. | Validate primary verb loop in greybox before writing meta-code. | Purely narrative genres (Visual Novels) lacking mechanical execution loops. | *Celeste*, *DOOM (2016)* |
| **Systemic Modular Staging** | Reworking assets due to changing engine architecture. | Decouple low-level netcode/physics from data-driven content pipelines. | Small solo game jams where decoupling overhead slows velocity. | *StarCraft II*, *Slay the Spire* |
| **Input Ergonomics Buffer** | Control thrashing, physical fatigue, and dropped inputs. | Heat-map input density and implement input buffering early. | Turn-based or menu-gated strategy/RPG titles. | *Monster Hunter: World*, *Titanfall 2* |
| **Asset Scalability Gates** | Getting crushed by genre asset volume requirements. | Deploy modular tile-sets, procedural generation, or systemic tables. | Bespoke hand-crafted puzzle games where procedural tools break logic. | *Deep Rock Galactic*, *Dead Cells* |


# Quick-Reference Matrix: Genre Technical & Scope Bottlenecks

When conducting pre-production planning across common parent genres, design and engineering teams must anticipate specific technical bottlenecks, scoping landmines, and ergonomic risks. 

Use this quick-reference matrix to identify primary failure vectors, recommended architectural resolution patterns, and benchmark exemplars across six major genre pillars.

#### Genre Technical & Scope Matrix

| Parent Genre Pillar | Primary Scope & Tech Bottleneck | Recommended Resolution Pattern | Benchmark Exemplar |
| :--- | :--- | :--- | :--- |
| **Character Action & Fighting** | **Hit-Box & Input Latency:** Sub-frame execution requirements and netcode rewinds causing hit registration desync. | **Vertical Slice MVL + Rollback Engine:** Freeze frame-accurate hit/hurtboxes and rollback netcode architecture in greybox before modeling characters. | ***Guilty Gear -Strive-***, ***Street Fighter 6*** |
| **First-Person / Hero Shooters** | **Input Ergonomics & Netcode:** Thumb-stick contention during high-mobility movement paired with server reconciliation. | **Input Ergonomics Buffer + Server-Authoritative Netcode:** Map movement/aiming to bumpers/triggers and build client-side prediction algorithms early. | ***Titanfall 2***, ***VALORANT*** |
| **Open-World Survival Craft** | **State Persistence & Spatial Streaming:** Memory hitching during rapid traversal and persistent item/building state serialization. | **Asset Scalability Gates + Spatial Partitioning:** Deploy modular procedural generation seeds and streaming LOD culling pipelines. | ***Valheim***, ***Deep Rock Galactic*** |
| **RTS & Grand Strategy** | **Multi-Thread AI & Thread Lock:** Late-game CPU slowdown, thread starvation, and sync loss in high-entity battles. | **Systemic Modular Staging + Lockstep:** Decouple async simulation AI threads from rendering and implement deterministic math logic. | ***StarCraft II***, ***Crusader Kings III*** |
| **Rogue-like & Deckbuilders** | **Synergy Scope Creep:** Exponential explosion of card/item edge-case interactions causing game-breaking balance bugs. | **Systemic Modular Staging:** Build modular data-driven hooks (JSON/ScriptableObjects) for card/status conditions to iterate without code rewrites. | ***Slay the Spire***, ***Hades*** |
| **Soulslike & Action RPGs** | **Animation Wind-Up & Visual Noise:** Visual clutter obscuring precise enemy telegraph tells, leading to perceived cheap deaths. | **Vertical Slice MVL + Telegraph Cadence:** Enforce strict Wind-up / Active / Recovery animation phases and test telegraph clarity in graybox arenas. | ***Elden Ring***, ***Nioh 2*** |


### 9. Conclusion: Scoping with Systemic Intent

Game design is fundamentally an art of meaningful constraints. Selecting a target genre is not merely picking a wrapper for creative ideas, it is choosing the rules of engagement for your team's technical architecture, physical input ergonomics, and production bandwidth.

By enforcing a strict **Verb Budget**, validating your **Minimum Viable Loop** in greybox, and securing your **Technical Dependencies** before scaling content, you transform genre selection from a source of production anxiety into a foundation for systematic innovation.


> **Final Takeaway:** Scope is not the enemy of creativity; it is its container. Define your boundaries early so your mechanics can shine within them.
