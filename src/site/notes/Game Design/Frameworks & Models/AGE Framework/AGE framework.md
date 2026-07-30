---
{"dg-publish":true,"permalink":"/game-design/frameworks-and-models/age-framework/age-framework/","dg-note-properties":{}}
---

In game design theory, system architects frequently encounter a fundamental analytical challenge: bridging the gap between low-level physical interactions (pressing buttons, swinging analog sticks, timing inputs) and high-level player retention (emotional investment, flow states, and long-term mastery).

Traditional structural models often evaluate games either from a top-down perspective or focus purely on emergent dynamics. However, middle-tier system behavior can often become abstract, making it difficult for designers to trace precisely how specific atomic control verbs directly shape emergent systemic states and high-level player outcomes.

The **A.G.E. Framework** (Actions, Gameplay, Experience), created by Dr. Roberto Dillon, resolves this ambiguity by establishing a strict, upwardly cascading relational chain. It models interactive systems as a clean, three-tier pipeline where atomic physical inputs (**Actions**) interact through systemic rules, spatial constraints, hazards, and mechanics (**Gameplay**) to generate intended cognitive and emotional states (**Experience**).

### A.G.E. Architectural Pipeline

|**Pipeline Stage**|**Layer Tier**|**Scope & Systemic Description**|**Core Focus**|
|---|---|---|---|
|**Stage 1**|**Actions (Micro / Atomic)**|Physical inputs, raw control verbs, input responsiveness, and immediate tactile feedback _(e.g., button presses, aim, sprint, jump, haptics)_|Control feel, latency, animation buffering, and input satisfaction|
|**Stage 2**|**Gameplay (Meso / Structural)**|Systemic rules, spatial constraints, hazards, AI behaviors, resource limits, and win/loss conditions _(e.g., ammo caps, stamina decay, hitboxes, TTK)_|Tactical options, encounter design, balance curves, and emergent gameplay loops|
|**Stage 3**|**Experience (Macro / Experiential)**|Psychological payoffs, flow states, cognitive engagement, and emotional resolution _(e.g., tension, relief, mastery, satisfaction)_|Affective engagement, intrinsic motivation, and long-term retention|

### Core Analytical Functions

1. **Structural Traceability:** Connects micro control inputs directly to macro game loops through an unambiguous, bottom-up mechanical chain, establishing clear causality across all design layers.
    
2. **Layered Systemic Deconstruction:** Provides a clean lens to analyze features strictly at their operating tier, preventing design confusion between input execution (Actions), system rules (Gameplay), and player feeling (Experience).
    
3. **Diagnostic Grey-Box Auditing:** Establishes a root-cause diagnostic structure for prototyping failure. Designers can isolate whether an issue stems from unresponsive controls (**Actions breakdown**), uncalibrated rules or unchallenging loops (**Gameplay breakdown**), or unrewarding psychological payoffs (**Experience breakdown**).

## The Three Conceptual Layers of A.G.E.

The A.G.E. Framework divides all interactive systems into a three-tier upwardly cascading pipeline. Every player interaction originates at the physical input layer (**Actions**), flows through system rules and constraints (**Gameplay**), and terminates in psychological and emotional outcomes (**Experience**).

|**Pipeline Stage**|**Layer Tier**|**Scope & Systemic Description**|**Core Focus**|
|---|---|---|---|
|**Stage 1**|**Actions (Micro)**|Atomic Input Verbs|Physical inputs, control responsiveness, animation buffering, and tactile feedback _(e.g., button presses, aim, sprint, jump, haptics)_|
|**Stage 2**|**Gameplay (Meso)**|Structural Rules & Systems|System constraints, hazards, AI behaviors, resource limits, and win/loss conditions _(e.g., ammo caps, stamina decay, hitboxes, TTK)_|
|**Stage 3**|**Experience (Macro)**|Psychological Payoff|Affective response, flow states, cognitive engagement, and emotional resolution _(e.g., tension, relief, mastery, satisfaction)_|

### 2.1 Layer 1: Actions (Micro / Atomic Tier)

- **Definition:** The fundamental, lowest-level physical player inputs, raw control verbs, and immediate feedback mechanisms executed by the player.
    
- **System Scope:** Micro-scale interactions occurring on a frame-by-frame or second-by-second basis.
    
- **Core Design Elements:**
    
    - **Control Responsiveness:** Input latency, acceleration curves, dead zones, animation buffering, and cancellation windows.
        
    - **Atomic Verbs:** Physical mechanics such as _pressing a jump button_, _pulling a trigger_, _crouching_, _clicking an item_, or _steering a vehicle_.
        
    - **Tactile Feedback:** Controller haptics, button feel, camera shake, and frame-freeze (hit stop).
        
- **Design Focus:** Ensuring inputs feel crisp, intuitive, and mechanically satisfying before layering system complexity.
    

### 2.2 Layer 2: Gameplay (Meso / Structural Tier)

- **Definition:** The structured combination of atomic actions governed by systemic rules, spatial constraints, hazards, AI behaviors, and victory/defeat conditions.
    
- **System Scope:** Meso-scale game loops, combat encounters, spatial platforming courses, resource management systems, and mission objectives.
    
- **Core Design Elements:**
    
    - **Rules & Constraints:** Ammunition caps, stamina decay rates, enemy detection cones, line-of-sight checks, and timer limits.
        
    - **System Mechanics:** Tactical cover systems, crafting trees, stealth mechanics, economy inflation, and spatial navigation.
        
    - **Encounter Design:** Enemy wave compositions, boss telegraphing, arena layouts, and environmental hazards.
        
- **Design Focus:** Creating meaningful tactical choices, balanced difficulty curves, and dynamic systemic emergence.
    

### 2.3 Layer 3: Experience (Macro / Experiential Tier)

- **Definition:** The high-level psychological affect, emotional resonance, and cognitive state experienced by the player as they navigate gameplay challenges.
    
- **System Scope:** Macro-scale engagement, session retention, emotional arcs, and player mastery.
    
- **Core Design Elements:**
    
    - **Affective Payoffs:** The transformation of mechanical challenge into cognitive and emotional states, such as relief, pride, exhilaration, or tension.
        
    - **Need Satisfaction:** Engaging underlying psychological drivers, such as intrinsic competence, autonomy, and relatedness.
        
    - **Cognitive States:** Achieving psychological flow, immersion, and long-term retention.
        
- **Design Focus:** Ensuring that mechanical execution yields a satisfying, emotionally meaningful outcome rather than sterile repetition.
    

### Layer Deconstruction Matrix

|**A.G.E. Layer**|**System Scope**|**Primary Design Focus**|**Typical System Elements**|**Common Breakdown Point**|
|---|---|---|---|---|
|**Actions**|Micro (Atomic)|Input feel & tactile feedback|Button presses, movement verbs, animation buffering, haptics|Clunky controls, input lag, unresponsive movement|
|**Gameplay**|Meso (Structural)|Rules, constraints & challenge|Combat encounters, ammo limits, spatial platforming, resource decay|Boring loops, bullet-sponge enemies, uncalibrated difficulty|
|**Experience**|Macro (Experiential)|Psychological & emotional payoff|Flow state, sense of mastery, tension/relief, pride, immersion|Tedious grind, unearned rewards, lack of emotional resonance|

Got it. We will use the inline text notation `Word (Word) -> Word (Word) -> Word (Word)` for all pipelines and cascades across the documentation to ensure text stays cleanly within page margins.

Here is the revised **Section 3**, followed by **Section 4**.

## Section 3: Mechanical Cascades & Industry Case Studies

System deconstruction using the A.G.E. Framework relies on tracing mechanics along a strict bottom-up cascade:

Action (Micro Verb) -> Gameplay (Meso System / Rule) -> Experience (Macro Payoff)

By isolating mechanics at each level, game designers can evaluate whether low-level player inputs directly serve meso-level systemic challenges, and whether those challenges resolve into macro-level cognitive and emotional satisfaction.

### 3.1 The A.G.E. Tracing Pipeline

1. **Actions Layer (Micro):** Identify the atomic physical inputs, animation buffers, feedback haptics, and movement verbs available to the player.
    
2. **Gameplay Layer (Meso):** Identify the systemic rules, spatial constraints, AI behaviors, resource limits, and win/loss conditions governing those verbs.
    
3. **Experience Layer (Macro):** Evaluate the resulting psychological state—such as flow, tension, relief, strategic agency, or mastery—produced when the player navigates the gameplay challenge.
    

### 3.2 Genre Deconstruction Case Studies

#### Case Study A: Precision Platformer (_Celeste_)

- **System Focus:** High-frequency spatial traversal and recovery loops.
    

|**A.G.E. Layer**|**Systemic Element**|**Technical & Design Specification**|
|---|---|---|
|**Actions (Micro)**|Air Dash & Jump|8-directional dash input with 4-frame buffer, instant velocity reset, coyote time (jump grace frames), and crisp audio-visual feedback.|
|**Gameplay (Meso)**|Spatial Hazard Navigation|Navigating narrow, lethal spike corridors; stamina decay on wall climbs; instant screen-wipe respawn with zero reload delay.|
|**Experience (Macro)**|High-Frequency Flow & Pride|Rapid cycle of tension and instant failure resolution; eliminates downtime to foster a continuous flow state, culminating in deep mechanical pride and self-efficacy.|

#### Case Study B: Tactical Action RPG (_Elden Ring_)

- **System Focus:** High-stakes stamina management and melee boss combat.
    

|**A.G.E. Layer**|**Systemic Element**|**Technical & Design Specification**|
|---|---|---|
|**Actions (Micro)**|Heavy Parry / Dodge Roll|Button press mapped to invulnerability frames (i-frames) with committed recovery animations, stamina cost, and weapon impact audio.|
|**Gameplay (Meso)**|Telegraphed Boss Combo|Boss executes a multi-hit AoE attack with strict timing windows; mistimed dodges inflict 70% health penalties and stagger the player.|
|**Experience (Macro)**|High Tension to Exhilarating Mastery|Initial vulnerability and acute tension resolve into intense exhilaration and a sense of earned competence upon executing a perfect counter-sequence.|

#### Case Study C: Extraction Shooter (_Escape from Tarkov_)

- **System Focus:** High-stakes risk/reward navigation and gear persistence.
    

|**A.G.E. Layer**|**Systemic Element**|**Technical & Design Specification**|
|---|---|---|
|**Actions (Micro)**|Lean & Container Loot|Holding lean keys to peek corners; holding interaction verb to search containers with progressive slot reveal delays.|
|**Gameplay (Meso)**|Extraction Zone Timer & Permadeath|High time-to-kill (TTK) ballistics; limited extraction points gated by strict countdown timers; total loss of equipped gear upon death.|
|**Experience (Macro)**|Sustained Dread & High-Stakes Relief|Persistent environmental dread and hyper-alertness during traversal convert into overwhelming psychological relief and accomplishment upon successful extraction.|

#### Case Study D: Turn-Based Strategy (_Civilization VI_)

- **System Focus:** Spatial macro-planning and economic expansion.
    

|**A.G.E. Layer**|**Systemic Element**|**Technical & Design Specification**|
|---|---|---|
|**Actions (Micro)**|Tile Selection & Order Issuance|Mouse-clicking map hexes, dragging unit paths, selecting tech tree nodes, and confirming turn completion.|
|**Gameplay (Meso)**|Adjacency Yields & Fog of War|District placement rules based on terrain synergy; resource upkeep costs; competing AI nation expansion and turn limits.|
|**Experience (Macro)**|Long-Term Strategic Competence|Prolonged cognitive engagement ("one more turn" compulsion), intellectual mastery, and deep satisfaction from executing multi-turn macro strategies.|

### 3.3 Comprehensive Deconstruction Matrix Across Genres

|**Genre**|**Actions (Micro Inputs)**|**Gameplay (Meso Rules & Systems)**|**Experience (Macro Payoffs)**|
|---|---|---|---|
|**Precision Platformer**|Air dash, wall jump, climb hold|Spike hazards, stamina limits, instant respawn|High-frequency flow, tension, mechanical mastery|
|**Action RPG**|Parry, dodge roll, light/heavy attack|Boss attack windows, stamina decay, i-frames|High tension, exhilaration, earned competence|
|**Extraction Shooter**|Corner lean, crouch height adjust, loot hold|High TTK, permadeath gear loss, extraction timer|Persistent dread, hyper-alertness, profound relief|
|**Turn-Based Strategy**|Hex click, path drag, tech tree confirm|District adjacency yields, fog of war, turn limits|Intellectual agency, strategic mastery, session retention|
|**Survival Horror**|Aim, sprint, reload, inventory drag|Restricted inventory slots, unkillable AI pursuers|Acute vulnerability, resource anxiety, relief|

## Section 4: Systemic Design Workflows & Grey-Box Diagnostic Audits

To integrate the A.G.E. Framework into game development, designers utilize a bottom-up construction process paired with a top-down diagnostic audit.

```
Design Pipeline:     Actions (Micro) -> Gameplay (Meso) -> Experience (Macro)
Diagnostic Audit:    Experience (Macro) -> Gameplay (Meso) -> Actions (Micro)
```

### 4.1 The Diagnostic Grey-Box Audit Workflow

When a feature fails during playtesting or grey-box prototyping, designers conduct a top-down root-cause audit to locate the exact tier of systemic breakdown:

1. **Step 1: Experience Evaluation (Did it feel right?)**
    
    - _Audit Question:_ Did the player feel the intended cognitive state, tension, or satisfaction?
        
    - _Failure Symptom:_ Players express boredom, frustration, or indifference.
        
2. **Step 2: Gameplay Rule Inspection (Is the challenge calibrated?)**
    
    - _Audit Question:_ If the Experience failed, are the systemic rules, AI behaviors, resource constraints, or difficulty scaling functioning properly?
        
    - _Failure Symptom:_ Encounters are unchallenging, exploit-prone, overly penalizing, or lack meaningful tactical decisions.
        
3. **Step 3: Action Input Verification (Do the controls support the rule?)**
    
    - _Audit Question:_ If the Gameplay rules are sound but the feature still fails, are the atomic controls responsive, intuitive, and tactile?
        
    - _Failure Symptom:_ Latency, rigid animation locks, ambiguous button mapping, or lack of tactile feedback (haptics, audio-visual hit-stop).
        

### 4.2 Diagnostic Failure Matrix

|**Failure Symptom**|**Identified Breakdown Tier**|**Root Cause Example**|**Corrective Design Prescription**|
|---|---|---|---|
|Player feels no tension during a stealth section|**Gameplay Tier**|Enemy AI detection cones are too narrow and patrol paths are static|Expand detection vectors, randomize AI routines, or add noise mechanics|
|Player understands what to do but misses parry timing consistently|**Actions Tier**|Parry verb has a 200ms input delay and no animation buffering|Reduce input latency, extend i-frame grace windows, or add input buffering|
|Player defeats a major boss encounter but feels unrewarded|**Experience Tier**|The boss fight resolves immediately with no visual/audio payout or progression flag|Add dynamic audio stingers, camera focus, and tangible systemic progression rewards|

### 4.3 Designer Evaluation Checklist

### A.G.E. Feature Audit Checklist

#### 1. Actions Layer (Micro)
- [ ] Are input verbs responsive, with input latency minimized?
- [ ] Is appropriate animation buffering or coyote time provided for precision actions?
- [ ] Do actions provide immediate tactile, visual, or haptic feedback upon press?

#### 2. Gameplay Layer (Meso)
- [ ] Are rules, constraints, and victory conditions clearly communicated?
- [ ] Do system mechanics demand active player decision-making rather than passive execution?
- [ ] Is difficulty calibrated to prevent both trivialization and unfair friction?

#### 3. Experience Layer (Macro)
- [ ] Does successful navigation of gameplay challenges produce a distinct psychological payoff?
- [ ] Does the feature contribute to a sustained flow state or sense of mastery?
- [ ] Is the emotional arc properly resolved following high-tension gameplay beats?