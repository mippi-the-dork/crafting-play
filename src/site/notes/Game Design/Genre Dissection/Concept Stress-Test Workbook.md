---
{"dg-publish":true,"permalink":"/game-design/genre-dissection/concept-stress-test-workbook/","dg-note-properties":{}}
---

# How to Use This Workbook

### 1. Purpose & Mindset: The Architectural Stress-Test

Most early-stage game concepts fail not from a lack of creativity, but from **unexamined systemic friction**, mechanics, camera angles, pacing requirements, and scope demands that quietly fight each other under the hood.

This workbook is not a brainstorming tool, nor is it meant to kill your enthusiasm. It is an **operational filter**. Its sole purpose is to act as a simulated preproduction audit: exposing hidden structural faults, cognitive traps, and scope explosions _before_ you write a single line of code or sink months into prototyping.

### 2. Prerequisites: What to Bring to This Session

Before starting Phase 1, gather your raw material. This workbook is designed as the operational companion to the broader [[Game Design/Genre Dissection/Genre Dissection\|Genre Dissection]] section. If you haven't reviewed the core principles yet, start there to understand genre as scaffolding rather than a restrictive box.

- **The "Word Vomit" Pitch:** A raw document, bulleted list, or mental braindump containing every feature, mechanic, camera angle, moment, and idea you want in the game.
    
- **The Inspiration Triad:** 2 to 3 existing games that represent major pillars of your idea (e.g., _"Battlezone II for direct vehicle possession + Satisfactory for factory automation + Command & Conquer for map strategy"_).
    
- **Reality Constraints:** A candid assessment of your team size (e.g., solo indie, student pair), primary target platform, and available development time.
    

### 3. The 3-Step Micro-Framework

Every phase in this workbook uses a standardized 3-step loop. Work through each phase sequentially, do not skip ahead, as each phase builds directly on the outputs of the previous one.

|**Step**|**Phase Stage**|**Primary Action**|**Expected Output**|
|---|---|---|---|
|**Step 1**|**Concept Guardrail**|Read & Understand|Learn the core design principle and failure mode|
|**Step 2**|**Stress-Test Audit**|Analyze & Evaluate|Complete the audit table and run the Red Flag diagnostic test|
|**Step 3**|**Spec Sheet Entry**|Extract & Document|Copy the finalized, validated Markdown block to your vault|

#### Step 1: Read the Concept Guardrail

Each section begins with a plain-English explanation of a critical game design trap (e.g., _Cognitive Overload_, _Perspective Clashes_, _Multiplicative Scope_). Read this first to understand the theoretical failure state you are trying to avoid.

#### Step 2: Complete the Audit & Run Diagnostics

Fill out the provided Obsidian-compatible audit table using your game's specific features. Then, evaluate your entries against the **Red Flag Warning**.

- The Red Flag is a pass/fail diagnostic. If your entries trigger the Red Flag condition, you **must apply one of the Resolution Protocols** listed in that section before moving to the next phase.
    

#### Step 3: Copy the Spec Sheet Entry

Each phase ends with a modular Markdown block. As you complete and resolve each phase, copy its corresponding code block into your local design workspace (Obsidian, Notion, or local Markdown file). By the end of Phase 5, these entries will synthesize into a complete, buildable **Preproduction Brief**.

### 4. Protocol: How to Handle a Red Flag Warning

When an audit table triggers a **Red Flag Warning**, do not ignore it or assume "I'll figure it out during coding." An unresolved Red Flag in preproduction turns into a dead-end prototype in production.

When a Red Flag is triggered, choose one of three explicit actions:

|**Action Path**|**Operational Meaning**|**When to Use It**|
|---|---|---|
|**A. Apply Systemic Rule**|Invent a clear, hard-coded rule that resolves the clash (e.g., camera switches automatically, automated AI protects player during map view).|When the clash involves two mechanics that are both critical to the core fantasy.|
|**B. Revert to Convention**|Strip away your custom innovation on that mechanic and default to standard industry conventions (e.g., standard WASD, standard RTS minimap).|When the clash is caused by over-innovating on secondary systems (saving your Innovation Budget).|
|**C. Cut to MVG**|Move the conflicting mechanic out of the initial prototype scope and into the "Deferred / Post-Validation" list.|When the clash requires complex tech (e.g., dynamic multiplayer networking) that threatens the project's viability.|

### 5. Recommended Execution Flow

1. **Set aside 60–90 minutes** of uninterrupted focus time.
    
2. **Open your local notes app** (e.g., Obsidian) side-by-side with this workbook page.
    
3. **Work linearly:** Process Phase 1 through Phase 5, copying each completed Markdown block into a single master document titled `[Project Name] - Concept Stress-Test Brief`.
    
4. **Final Check:** Review your master deliverable against the scope boundaries set in Phase 5 before writing your first prototype task.
    



# Phase 1: Unpacking the Raw Pitch (Deconstruction)

### Step 1: Concept Guardrail

When inspiration strikes, high-concept pitches are usually expressed as a "feature heap", a loose collection of camera angles, reference games, mechanical wishlists, and cool moments (_"It's Battlezone meets Satisfactory with dynamic base building!"_).

The fatal mistake beginners make is treating all features on their wishlist as equally important. In reality, a game's architecture relies on a strict hierarchy. Before you can evaluate whether your genres collide, you must unpack your pitch into three distinct mechanical tiers:

1. **The Core Genre Engine (The 30-Second Loop):** The foundational mechanics the player performs constantly (e.g., aiming, driving, shooting, selecting units). This loop must account for **70% or more of moment-to-moment playtime** and must be fun in a blank grid environment with zero secondary systems active.
    
2. **Supporting / Enabling Loops:** Systems that create context, resource pipelines, or progression for the Core Engine (e.g., factory belts producing tank shells, base turrets defending spawn, tech trees unlocking heavy chassis).
    
3. **Cosmetic & Flavor Elements:** Visual, thematic, or custom flourishes that provide aesthetic satisfaction but carry zero systemic weight (e.g., vehicle paint jobs, destruction physics effects, lore entries).

>Not sure which genre bucket your mechanics belong to? Consult the [[Game Design/Genre Dissection/Genre Glossary\|Genre Glossary]] to review standardized genre definitions, primary mechanics, and typical secondary loops before filling out your audit table.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Creator

1. Take your raw "word vomit" pitch document.
    
2. List every single mechanic, system, camera perspective, and feature you envisioned into the table below.
    
3. Assign each feature to a category, estimate its moment-to-moment playtime footprint, and answer: **"If I delete this feature right now, does the core 30-second interaction break?"**
    

#### Phase 1 Audit Table (Case Study Example: FPS / RTS / Automation Hybrid)

|**Pitch Element / Mechanic**|**System Category**|**Est. Playtime %**|**Essential to 30s Loop?**|**Associated Genre**|
|---|---|---|---|---|
|First-person vehicle piloting & direct combat aiming|**Core Engine**|50%|**Yes**|FPS / Vehicle Action|
|Top-down tactical squad selection & map ordering|**Core Engine**|25%|**Yes**|Real-Time Strategy (RTS)|
|Factory automation & resource conveyor belts|Supporting Loop|15%|**No** (Feeds Ammo/Units)|Factory / Automation|
|Base building & defensive turret placement|Supporting Loop|10%|**No** (Defends Factory)|Base Builder / Tower Defense|
|Custom vehicle paint jobs & cosmetic chassis skins|Cosmetic / Flavor|0%|**No**|Visual Customization|

#### Red Flag Diagnostic 1.1: The Buried Core Engine

Evaluate your completed audit table against these two pass/fail conditions:

- **Condition A (Divergent Focus):** Is your _Core Engine_ category responsible for **less than 60%** of total estimated playtime?
    
- **Condition B (Tri-Engine Collision):** Does your _Core Engine_ category contain primary mechanics from **3 or more distinct genres** that require different camera angles or input schemes during the same 30-second window?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your pitch has triggered **Red Flag 1.1: The Buried Core Engine**. Your core loop is fractured, meaning players will feel confused about what the game actually _is_ at its moment-to-moment level.
>     

#### Resolution Protocol for Red Flag 1.1

If Red Flag 1.1 is triggered, you must execute one of the following two fixes before proceeding to Phase 2:

##### Protocol A: The Primary Anchor Assignment (Recommended)

You cannot have three "equal" core genres in a single moment-to-moment loop. You must choose **ONE Primary Anchor Genre** as your Core Engine, and demote the other genres to Supporting Loops.

- _Before (Unstable):_ Equal parts FPS (33%) + RTS (33%) + Automation (33%).
    
- _After (Stable):_ **FPS is the Anchor (70%)**. RTS map commands become a supporting tactical overlay (20%). Automation becomes a passive background pipeline (10%).
    

##### Protocol B: The 30-Second Gray-Box Isolation Test

Imagine a grey, untextured flat grid with no terrain, no base building, no factory belts, and no lore.

1. Place your player character and two enemies in that grey box.
    
2. What input are they making? (e.g., aiming and firing a tank cannon).
    
3. **Rule:** If that grey-box interaction is not inherently satisfying within 30 seconds, delete every Supporting Loop on your list until you fix the core interaction.
    

### Step 3: Spec Sheet Entry

Once your pitch is successfully deconstructed and validated, copy the code block below into your local notes app (Obsidian/Notion) and fill it out with your finalized values.

Markdown

```
### Phase 1: Concept Deconstruction
- **Working Title:** 
- **Primary Anchor Genre (Core Engine):** 
- **The 30-Second Core Loop (What the player does constantly):**
- **Supporting Systems (Secondary Loops):**
  1. 
  2. 
  3. 
- **Explicit Non-Essential List (Features removed from core loop):**
  - 
```



# Phase 2: Player Fantasy & Motivation Alignment

### Step 1: Concept Guardrail

Every video game genre satisfies a specific **psychological payback**. Players choose an FPS for the adrenaline of twitch mastery, an RTS for the satisfaction of strategic dominance, or an automation game for the serene feeling of bringing order to chaos.

The trap in multi-genre design is **Cognitive Discord**, combining mechanics that demand conflicting mental states at the exact same moment.

If your game asks a player to line up a high-precision headshot while simultaneously warning them that a factory belt 3 miles away has jammed, you aren't giving them two fun games at once. You are causing **attention fatigue**. To make a hybrid work, you must map the psychological drivers of your pitch and ensure their pacing requirements don't fight for the same brain space.

>To better understand how different genres satisfy specific psychological drives (e.g., Mastery, Strategy, Autonomy, Immersion), review [[Game Design/Genre Dissection/The Player Fantasy Motivation Framework\|The Player Fantasy Motivation Framework]]. Pay close attention to how conflicting pacing profiles create cognitive friction.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Creator

1. Look at the mechanics you categorized in Phase 1.
    
2. Identify the core **player fantasy** each mechanic fulfills.
    
3. Define the **Pacing Mode** (how fast the player must react) and **Cognitive Attention Profile** (how narrow or broad their focus must be) required by each system.
    

#### Phase 2 Audit Table (Case Study Example: FPS / RTS / Automation Hybrid)

|**Target Player Fantasy**|**Core Psychological Driver**|**Associated Genre**|**Required Pacing Mode**|**Cognitive Attention Profile**|
|---|---|---|---|---|
|**Frontline Ace**|Reflexive Mastery & Adrenaline|First-Person Action|High-Urgency Real-Time|**Hyper-Local:** Focused strictly on crosshair and immediate cover|
|**Field Commander**|Macro-Control & Strategic Triumph|Real-Time Strategy|Medium-to-High Real-Time|**Broad-Map:** Constant scanning of minimap, unit counts, flanks|
|**Factory Engineer**|Optimization, Order & Logic|Factory Automation|Low-Urgency / Reflective|**Deep-Systemic:** Focused on input/output ratios, logistics chains|

#### Red Flag Diagnostic 2.1: Cognitive Discord & Pacing Collision

Evaluate your completed table against these two pass/fail conditions:

- **Condition A (Pacing Clash):** Does your core loop require **High-Urgency Real-Time** reactions in one system while requiring **Low-Urgency Reflective** planning in another _simultaneously_?
    
- **Condition B (Attention Split):** Does the player need to maintain **Hyper-Local** focus (aiming/dodging) and **Broad-Map** awareness (RTS commanding) without a pause or safety mechanism?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your pitch has triggered **Red Flag 2.1: Cognitive Discord**. Players will experience panic, frustration, or decision paralysis because the game demands two incompatible mental states at once.
>     

#### Resolution Protocols for Red Flag 2.1

If Red Flag 2.1 is triggered, choose one of the following two structural fixes to restore psychological harmony:

##### Protocol A: Temporal Separation (Phase-Based Pacing)

Never force two conflicting cognitive modes to happen at the exact same second. Split your gameplay loop into explicit, alternating phases.

- _Example Implementation:_
    
    - **Phase 1: Build & Automate (Low Urgency / Deep-Systemic):** Players construct bases, set up conveyor belts, and queue troop production with zero enemy attacks occurring.
        
    - **Phase 2: Battle & Direct (High Urgency / Hyper-Local):** The wave begins. Base building is locked or automated. Players focus 100% on vehicle combat and commanding field troops.
        

##### Protocol B: Cognitive Abstraction (Automation & Delegation)

If all systems must occur in real-time, lower the mental burden of the secondary systems by delegating them to AI or simplifying their UI.

- _Example Implementation:_
    
    - Instead of requiring the player to manually fix factory bottlenecks during battle, introduce an **Auto-Logistics AI** that maintains basic ammo supply lines automatically unless custom overrides are commanded.
        

### Step 3: Spec Sheet Entry

Once your motivations and pacing profiles are aligned, copy the code block below into your local notes app and fill in your resolved values.

Markdown

```
### Phase 2: Player Fantasy & Motivation Alignment
- **Primary Fantasy (The Anchor):** 
- **Core Psychological Drive Satisfied:** 
- **Pacing Structure:** [ ] Phase-Based (Build then Fight) | [ ] Real-Time with Pauses | [ ] Fully Real-Time with AI Delegation
- **Attention Conflict Resolution Strategy:** 
  - *When in combat, secondary systems are handled by:* 
```



# Phase 3: Hybridization & Collision Matrix

### Step 1: Concept Guardrail

When you mash two or three genres together, mechanics rarely combine peacefully ($1 + 1 = 2$). Instead, they collide ($1 + 1 = \text{Friction}$).

**Systemic Friction** occurs when the fundamental rules of one genre directly undermine or destroy the functionality of another. For instance, a First-Person Shooter requires a narrow forward field of view and immediate physical awareness, while a Real-Time Strategy game requires broad spatial oversight and multi-unit selection. If you try to do both at the exact same time without a systemic translation rule, the mechanics don't complement each other, they break each other.

Phase 3 is where you identify every point where your combined genres smash together, analyze the friction type, and establish hard rules to resolve those clashes before writing code.

>When two genres collide, friction is inevitable. To study pre-cataloged collision patterns (like camera perspective clashes, control scheme overlaps, and state vulnerabilities), read [[Game Design/Genre Dissection/The Hybridization Collision Matrix\|The Hybridization Collision Matrix]].

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Creator

1. Map out the points where mechanics from different genres touch or overlap in your design.
    
2. Categorize the **Conflict Type** (Perspective, Input/Controls, Spatial Awareness, or Resource Allocation).
    
3. Draft a concrete **Systemic Rule** that resolves the conflict.
    

#### Phase 3 Audit Table (Case Study Example: FPS / RTS / Automation Hybrid)

|**Systemic Collision Point**|**Conflicting Genre Rules**|**Conflict Type**|**Impact on Player Experience**|**Proposed Systemic Rule**|
|---|---|---|---|---|
|**Direct Combat vs. Map Command**|FPS requires looking through gun sight; RTS requires bird's-eye map view.|Perspective / Camera|Player feels blind to overall battle while driving, or blind to incoming threats while commanding.|**Possession Camera:** Seamlessly scroll up to satellite map view, or double-click any unit to snap into its 1st-person cockpit.|
|**Player State During Map View**|RTS mode takes 100% of player inputs, leaving physical tank avatar unguided.|Avatar Vulnerability|Player's tank gets destroyed while they are busy giving orders to squad B on the map view.|**Local AI Guard Duty:** Disengaging direct control automatically puts the player's current vehicle into a defensive autopilot mode.|
|**Manual Combat vs. Factory Logistics**|FPS combat consumes ammo fast; Automation requires building belts to deliver ore.|Loop / Resource|Player runs out of ammo mid-fight because supply belts weren't manually hooked up to ammo depots.|**Standardized Supply Drops:** Factory belts route directly to central depots; player tanks automatically reload by driving near depots.|

#### Red Flag Diagnostic 3.1: The Unresolved Mechanical Contradiction

Evaluate your collision table against these two pass/fail conditions:

- **Condition A (Perspective Lockout):** Does entering the interface or view for System A render the player **completely blind** to catastrophic failures in System B?
    
- **Condition B (The Sitting Duck):** Does operating a strategic or management menu leave the player's physical avatar in the game world completely undefended and stationary in real-time?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your pitch has triggered **Red Flag 3.1: Unresolved Mechanical Contradiction**. This is the #1 cause of "jank" and player frustration in indie multi-genre games.
>     

#### Resolution Protocols for Red Flag 3.1

If Red Flag 3.1 is triggered, apply one of these three explicit design solutions to fix the collision:

##### Protocol A: The Possession & Autopilot Hand-Off (Recommended for Perspective Clashes)

Never leave the player's avatar in a mindless "braindead" state while they access secondary modes.

- **The Rule:** The instant the player disengages direct control (e.g., zooming out to RTS view), an **Autopilot AI** immediately assumes control of the player's current vehicle, executing a simple "Defend Area" or "Hold Position" behavior tree until the player snaps back in.
    

##### Protocol B: Physical Terminal Tethering (Contextual Safety)

If you cannot build autopilot AI, restrict access to the secondary mode so it can _only_ be opened in physically safe contexts.

- **The Rule:** The player cannot enter RTS command view anywhere on the map. They must dock inside a base command bunker or deploy a stationary "Command Rig" vehicle, creating an intentional, safe space to manage macro strategy.
    

##### Protocol C: Picture-in-Picture / Tactical HUD Overlay

Instead of switching cameras entirely, project the secondary system as a non-intrusive UI overlay on top of the primary view.

- **The Rule:** The FPS camera never closes. Pressing a button overlays a semi-transparent tactical map over the helmet visor, allowing basic squad commands using quick radial menus without losing 1st-person situational awareness.
    

### Step 3: Spec Sheet Entry

Once your mechanical collisions are identified and resolved with hard rules, copy the code block below into your local notes app.

Markdown

```
### Phase 3: Hybridization & Collision Rules
- **Primary Perspective Clash Identified:** 
- **Camera Transition Rule:** [ ] Full Camera Switch | [ ] Picture-in-Picture Overlay | [ ] Physical Terminal Only
- **Avatar Protection Protocol (The Sitting Duck Solution):** 
- **Resource Line Integration Rule (How secondary systems feed the core):**
```



# Phase 4: The 80/20 Innovation Budget

### Step 1: Concept Guardrail

Every video game has an **Innovation Budget**. When a player sits down with a new game, they rely on established genre conventions (e.g., WASD movement, red barrels explode, health bars are red or green, left-click shoots) to quickly process how the game works.

The biggest trap for passionate beginners is trying to reinvent everything at once. If you innovate on the control scheme, the camera perspective, the UI layout, _and_ the core gameplay loop simultaneously, your game becomes **illegible**. Players will spend their entire session fighting your controls rather than enjoying your mechanics.

To survive preproduction, you must enforce the **80/20 Rule**: Keep 80% of your game's foundational systems grounded in standard, recognizable genre conventions. Spend your entire 20% innovation budget exclusively on your game's core twist or "unique selling point."

>Before breaking a genre convention, learn why that convention exists in the first place. Read [[Game Design/Genre Dissection/The Convention Subversion Framework\|The Convention Subversion Framework]] to learn how to preserve player legibility while spending your 20% innovation budget effectively.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Creator

1. List the fundamental systems of your game (Controls, Camera, UI, Economy, Core Combat/Interaction).
    
2. For each system, define the standard industry convention.
    
3. State whether you are keeping that standard or subverting it.
    
4. Calculate your Innovation Risk Level.
    

#### Phase 4 Audit Table (Case Study Example: FPS / RTS / Automation Hybrid)

|**Game System**|**Standard Industry Convention**|**Your Planned Approach**|**Innovation Risk**|
|---|---|---|---|
|**Controls & Movement**|WASD + Mouse Aim for vehicles|**Keep Standard:** Use standard FPS vehicle controls.|Low|
|**Command System**|RTS drag-box selection & map pings|**Innovate (Core Twist):** Instant physical possession of any unit on the field.|High|
|**Economy / Crafting**|Gather ore -> refine -> build units|**Innovate:** Satisfactory-style physical conveyor belts feeding ammo to frontline bunkers.|High|
|**UI & HUD**|Minimap bottom-right, health bottom-left|**Innovate:** Diegetic 3D hologram terminal that pops up in front of the player's tank.|High|
|**Win Condition**|Destroy enemy base|**Keep Standard:** Annihilate the enemy HQ structure.|Low|

#### Red Flag Diagnostic 4.1: The Unreadable Design Warning

Evaluate your completed table against these pass/fail conditions:

- **Condition A (Over-Innovation):** Do you have "Innovate" or "High Risk" listed for **three or more** foundational systems?
    
- **Condition B (Control Subversion):** Are you forcing the player to learn a completely new input scheme for movement or camera control that breaks from 20 years of standard PC/Console design?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your pitch has triggered **Red Flag 4.1: The Unreadable Design Warning**. You have exceeded your Innovation Budget. Your game will fail its first playtest because players won't be able to figure out how to play it.
>     

#### Resolution Protocols for Red Flag 4.1

If Red Flag 4.1 is triggered, apply one of these fixes to restore legibility to your design:

##### Protocol A: The Reversion to Standard (Protecting the Core Twist)

Identify the one innovation that actually sells your game (e.g., _the FPS/RTS possession mechanic_). Protect that feature, and ruthlessly revert the other innovations back to standard conventions.

- _Example Fix:_ Scrap the custom diegetic 3D hologram UI. Revert to a standard 2D tactical HUD with a bottom-right minimap. The player is already learning a complex new mechanic; don't make them learn a new UI at the same time.
    

##### Protocol B: The Familiar Interface Bridge

If you _must_ innovate on a complex system (like automated logistics belts in an FPS), use a deeply familiar interface to teach it.

- _Example Fix:_ If your economy uses complex factory conveyor belts, use a standard RTS drag-and-drop radial menu to place them. Grounding the weird, new mechanic in a familiar, old control scheme lowers the mental barrier to entry.
    

### Step 3: Spec Sheet Entry

Once you have successfully reigned in your innovation budget, copy the code block below into your local notes app.

Markdown

```
### Phase 4: Innovation Budget (80/20 Rule)
- **The 20% Core Subversion (What makes this game entirely unique):** 
- **The 80% Familiar Foundation (Conventions we will copy exactly):**
  - *Controls:* 
  - *UI / HUD Layout:* 
  - *Objective / Win State:* 
- **Cut Innovations (Ideas we loved but reverted to standard for legibility):**
  1. 
```



# Phase 5: Minimum Viable Genre (MVG) Scope Stress-Test

### Step 1: Concept Guardrail

Single-genre games scale linearly in scope: adding a new gun to an FPS adds predictable, isolated work. Multi-genre hybrid games scale **multiplicatively**: adding a base-building mechanic to an FPS doesn't just mean building a base-building system, it means making enemy FPS AI interact with player-placed walls, making 1st-person physics handle custom collision grids, making weapon balance adapt to player-built turrets, and testing every combination for game-breaking exploits.

If Game A has 3 systems and Game B has 3 systems, combining them doesn't create 6 units of work, it creates $3 \times 3 = 9$ potential interaction points that all need bug fixing, UI support, and balancing.

The **Minimum Viable Genre (MVG)** is the absolute smallest, stripped-down prototype that proves your multi-genre loops actually work together. If your MVG isn't fun or functional with 1 unit, 1 resource, and 1 enemy type, adding 20 more units will only make a broken game take longer to finish.

>Multi-genre games scale multiplicatively ($N \times M$), not linearly. For a complete breakdown of production risk levels, load-bearing mechanics, and feature-cost estimation, read [[Game Design/Genre Dissection/The Genre Execution and Scoping Blueprint\|The Genre Execution and Scoping Blueprint]].

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Creator

1. Take every system from your deconstructed pitch in Phase 1.
    
2. Contrast your "Full Dream Vision" against the bare minimum required to test the core loop in a grey-box prototype.
    
3. Identify high-risk technical liabilities (e.g., custom multiplayer networking, dynamic pathfinding on player-built geometry, procedural generation).
    
4. Categorize each feature as **Keep (MVG)**, **Defer (Post-Validation)**, or **Cut (Removed entirely)**.
    

#### Phase 5 Audit Table (Case Study Example: FPS / RTS / Automation Hybrid)

|**System / Feature**|**Full Dream Vision**|**Minimum Viable Prototype (MVG)**|**Tech Risk Level**|**Scope Action**|
|---|---|---|---|---|
|**Playable Vehicles**|12 custom chassis types with upgrade trees|2 distinct classes (1 Light Scout, 1 Heavy Tank)|Low|**Keep (MVG)**|
|**Resource & Factory**|15 resource types, complex logistics belts|1 resource (Ore) feeding a central automatic ammo depot|Medium|**Trim to MVG**|
|**Enemy AI & Factions**|3 asymmetric AI factions with tech trees|1 basic wave-spawner with simple "Attack HQ" pathfinding|Medium|**Trim to MVG**|
|**Multiplayer / Co-op**|4-player online co-op with dedicated servers|Single-player local offline sandbox testbed|**Critical**|**Defer to Post-MVG**|
|**Base Building**|Modular walls, power grids, and custom turrets|Pre-placed turret pads where player deposits Ore|High|**Trim to MVG**|

#### Red Flag Diagnostic 5.1: Multiplicative Scope Explosion

Evaluate your completed table against these pass/fail conditions:

- **Condition A (The Multiplayer Trap):** For solo developers or student teams: Are you attempting to build online multiplayer in your initial prototype alongside multi-genre mechanics?
    
- **Condition B (Content Overload):** Does your initial prototype require more than 2 playable classes/units, more than 1 resource type, or more than 1 enemy type to be functional?
    
- **Condition C (High-Risk Tech Dependency):** Does your core loop rely on high-risk technical hurdles (e.g., dynamic AI pathfinding across real-time player-deformable terrain) before you have confirmed the core loop is fun?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to any of these conditions, your pitch has triggered **Red Flag 5.1: Multiplicative Scope Explosion**. Your project is currently mathematically improbable for your team size and timeline.
>     

#### Resolution Protocols for Red Flag 5.1

If Red Flag 5.1 is triggered, execute these non-negotiable scope cuts:

##### Protocol A: The Single-Player Quarantine

If you are a solo developer or student team, **strip multiplayer out of the preproduction scope completely**.

- **The Rule:** Prove the FPS/RTS/Automation loop works in single-player offline first. If the game isn't compelling against simple AI waves, networking it will only give you a laggy, broken game. If the single-player MVG succeeds, you can evaluate multiplayer architecture in a dedicated technical spike later.
    

##### Protocol B: The 50% Abstraction Rule

Replace complex physical simulation with systemic abstraction for the prototype phase.

- **Example Implementation:** Instead of building 3D conveyor belts that physically carry items along splines across your base (Satisfactory-style), replace them in the prototype with an **Instant Resource Counter** that generates +1 Ammo every 5 seconds when an Ore Extractor is active. Prove the combat loop works with the resource before spending weeks coding conveyor belt physics.
    

##### Protocol C: The "One of Each" Rule

Enforce strict content limits for your first playable build:

- **1** Playable Character / Vehicle.
    
- **1** Enemy Type.
    
- **1** Resource Type.
    
- **1** Flat Grey-Box Map.
    
- _If the core loop isn't fun with "One of Each," adding more content will not fix the underlying design._
    

### Step 3: Spec Sheet Entry

Once your scope is ruthlessly trimmed to a buildable MVG, copy the code block below into your local notes app.

Markdown

```
### Phase 5: Minimum Viable Genre (MVG) Scope
- **MVG Core Loop Goal (What the prototype must prove):** 
- **The "One of Each" Prototype Feature Set:**
  - *Playable Unit(s):* 
  - *Resource System:* 
  - *Enemy Type:* 
- **Deferred High-Risk Tech (Explicitly locked out until MVG succeeds):**
  1. 
  2. 
- **Explicit Cut List (Features removed to protect project survival):**
  - 
```




# Master Deliverable: The Complete Preproduction Brief

### How to Synthesis Your Results

Once you have completed the stress-test audits and diagnostics in Phases 1 through 5, copy the code block below into your local knowledge base (e.g., Obsidian, Notion, or local Markdown vault).

This document serves as your **Preproduction Brief**, the single source of truth that defines your game’s core loop, collision rules, innovation limits, and prototype scope before writing a line of code or building a single asset.

Markdown

```
# [Project Working Title] - Concept Stress-Test Brief

> **Status:** Preproduction / Concept Validation  
> **Author:** [Developer / Team Name]  
> **Date:** [YYYY-MM-DD]  
> **Primary Reference Triad:** [Game A] + [Game B] + [Game C]

---

## 1. Concept Deconstruction
- **Raw Pitch:** 
- **Primary Anchor Genre (Core Engine - 70%+ Playtime):** 
- **The 30-Second Core Loop:** 
- **Supporting / Enabling Loops:**
  1. 
  2. 
- **Non-Essential / Cosmetic Elements:** 

---

## 2. Player Fantasy & Motivation Alignment
- **Primary Player Fantasy:** 
- **Core Psychological Driver:** 
- **Pacing Profile:** [ ] Phase-Based | [ ] Real-Time with Pauses | [ ] Real-Time with AI Delegation
- **Attention Conflict Resolution Strategy:** 

---

## 3. Hybridization & Collision Rules
- **Primary Systemic Collision:** 
- **Camera Transition Rule:** [ ] Full Camera Switch | [ ] Picture-in-Picture | [ ] Terminal Only
- **Avatar Protection Protocol (The Sitting Duck Solution):** 
- **Resource / Supply Pipeline Integration Rule:** 

---

## 4. Innovation Budget (80/20 Rule)
- **The 20% Core Subversion (The Unique Selling Point):** 
- **The 80% Familiar Foundation (Industry Conventions Kept):**
  - *Controls & Inputs:* 
  - *UI & HUD Layout:* 
  - *Objective / Win State:* 
- **Cut / Reverted Innovations (Reverted for legibility):** 

---

## 5. Minimum Viable Genre (MVG) Scope
- **MVG Core Loop Objective (What the prototype must prove):** 
- **"One of Each" Prototype Feature Set:**
  - *Playable Unit / Character:* 
  - *Resource System:* 
  - *Enemy Type:* 
  - *Map / Environment:* 
- **Deferred High-Risk Tech (Locked out until MVG succeeds):** 
- **Explicit Cut List (Removed to protect project survival):** 
```

