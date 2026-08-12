---
{"dg-publish":true,"permalink":"/game-design/workbooks-and-tools/production-and-maintenance/design-health-check-workbook/","dg-note-properties":{}}
---

# How to Use This Workbook

### 1. Purpose & Mindset: The Mid-Dev Reality Check

You do not need a formal degree in game design to use this workbook. Whether you are a Lead Designer looking for an objective framework to align your team, a solo developer wearing every hat, or an engineer or artist forced to make design calls without formal training trying to figure out why a build isn't landing, this guide is designed for your workflow.

When a game in active production feels unrewarding, clunky, or overwhelming, the natural instinct for many teams is to **add more content**, more weapons, larger maps, or extra UI meters. In mid-production, this is almost always a mistake. Adding content on top of an unrefined core engine only multiplies your bug debt, slows down build iteration, and masks underlying design flaws.

Without a dedicated designer, cross-disciplinary teams often fall into **subjective design debates** (_"I think this mechanic is cool"_ vs. _"I think it's annoying"_). These arguments usually end in bad compromises where everyone's ideas stay in the build, leading to "Feature Soup."

The mindset of this workbook is **surgical reduction**:

- Replace subjective opinions with **observable, symptom-based diagnostics** from live playtest sessions.
    
- Identify and strip away "dead-weight" mechanics that eat up engineering time for zero playtest gain.
    
- Resolve systemic friction between combined genres so the game is inherently satisfying before you expand the content pipeline.
    

### 2. Prerequisites: What to Bring to This Session

Before starting Phase 1, gather your mid-production materials. You do not need formal design documentation, just real observations from your project:

- **A Playable Build:** A vertical slice, prototype, or alpha build playable for at least 10–15 minutes.
    
- **Playtest Observations:** Unfiltered notes, screen recordings, or bug reports from 3–5 playtesters (or your own candid notes during a play session).
    
- **The "Pain List":** A list of features players consistently ignore or complain about, alongside the features your engineering and art teams spend the most time bug-fixing.
    
- **Core Reference:** Keep [[Game Design/Genre Dissection/Genre Dissection\|Genre Dissection]] open if you need to review how genre conventions act as structural scaffolding rather than rigid rules.
    

### 3. The 3-Step Micro-Framework

Every phase in this workbook follows a standardized 3-step loop. Work through each phase sequentially with your team, do not skip ahead, as each diagnostic builds directly on the outputs of the previous section.

|**Step**|**Phase Stage**|**Primary Action**|**Plain-English Meaning**|**Expected Output**|
|---|---|---|---|---|
|**Step 1**|**Concept Guardrail**|Read & Understand|Learn the core design rule and the trap to avoid.|A clear mental model of the failure state.|
|**Step 2**|**Stress-Test Audit**|Analyze & Evaluate|Map your build's symptoms onto the audit table and run Red Flag tests.|An identified design flaw and recovery protocol.|
|**Step 3**|**Spec Sheet Entry**|Extract & Document|Copy the finalized Markdown block directly to your project vault.|An actionable task list for your team.|

### 4. Protocol: The 3 Recovery Action Paths

When an audit table triggers a **Red Flag Warning**, do not panic, ignore it, or try to fix it by adding more UI. Choose one of three explicit recovery actions to resolve the issue:

|**Recovery Path**|**Operational Meaning**|**When to Use It**|**Team Consensus Rule**|
|---|---|---|---|
|**Path A: Isolate & Re-tune**|Freeze new feature work; spend 1 sprint strictly fixing control responsiveness, sounds, visual feedback, and game feel for the core mechanic.|When a mechanic is conceptually correct, but feels floaty, unresponsive, or dull to play in live sessions.|_"We will not write new systems until pressing this button feels good in a grey box."_|
|**Path B: Mechanical Demotion**|Convert a complex, active player task into an automated or passive background system managed by code.|When a secondary feature forces players to multitask too much during high-stress combat moments.|_"If players ignore this menu during combat, the code will handle it automatically."_|
|**Path C: Surgical Cut**|Completely excise a feature from the build and re-route its resource inputs directly to systems that are already working.|When a feature takes massive programming/art time to maintain but adds almost no fun for the player.|_"If a feature costs 40% of our bug time but delivers 5% of the fun, it gets deleted."_|



# Phase 1: Core Loop & Playtest Reception Audit

### Step 1: Concept Guardrail

A mechanic can look brilliant on a pitch deck and still feel "dead" when played. In game development, **Game Feel** (or "Juice") is not mere polish, it is the primary language your game uses to communicate with the player's brain.

Every core interaction relies on a 4-part feedback chain:
>Input (Button Press) -> Action (Code Execution) -> Feedback (Visual / Audio / Haptics) -> Payoff (Player Satisfaction)


If any single link in this chain breaks down, non-designer playtesters won't use technical vocabulary. Instead, they will describe the game with broad complaints: _"The controls feel floaty," "Combat feels boring," "I couldn't tell if my weapon was hitting,"_ or _"I didn't realize I was taking damage."_

When a build isn't landing, developers often assume the game needs _more systems_. In reality, the existing core loop is usually suffering from a broken feedback chain. Before adding new mechanics or content, you must audit the physical feedback of your primary 30-second interaction in total isolation.

> Review [[Game Design/Genre Dissection/The Player Fantasy Motivation Framework\|The Player Fantasy Motivation Framework]] to verify whether your core loop's physical feedback matches the primary psychological driver you established during preproduction.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Boot up your current playable build.
    
2. Isolate your primary 30-second core mechanic (e.g., firing a vehicle turret, steering a mech, issuing a squad order, or placing a factory belt).
    
3. Observe a playtester (or yourself) performing that action 10 times in a row, mapping the observed symptoms onto the audit table below.
    

#### Phase 1 Audit Table (Playable Build Evaluation)

|**Core Action Audited**|**Input Responsiveness**|**Feedback / "Juice" Level**|**Playtester Symptom / Feedback**|**Identified Chain Failure**|
|---|---|---|---|---|
|**Direct Combat / Firing**|Instant|Low (Quiet sound, no hit marker, no enemy flinch)|_"I can't tell if my shots are actually connecting."_|**Link 3 Failure (Feedback)**|
|**Vehicle Piloting / Steering**|Sluggish (0.3s input lag before turn starts)|Low (No engine rumble, no camera lean on turns)|_"Driving feels slippery and hard to control."_|**Link 1 Failure (Input Delay)**|
|**Issuing Squad Orders**|High Friction (Requires opening a menu & 3 clicks)|Medium (Unit moves, but no audio confirmation)|_"I stopped giving orders because it took too long during fights."_|**Link 1 & 4 Failure (Input Friction)**|

#### Red Flag Diagnostic 1.1: The Flat Core Loop

Evaluate your live build against these two pass/fail conditions:

- **Condition A (Feedback Blindness):** Do players fail to notice important game events (e.g., landing a critical hit, taking damage, or completing a production queue) because the visual, audio, or haptic feedback is too subtle?
    
- **Condition B (Effort-to-Payoff Deficit):** Do playtesters actively avoid using a core feature because the button/menu effort required to trigger it is higher than the in-game reward they get in return?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your build has triggered **Red Flag 1.1: The Flat Core Loop**. Your core loop lacks responsiveness and physical feedback. Adding more levels, enemies, or narrative to this build will not fix player retention.
>     

#### Resolution Protocols for Red Flag 1.1

##### Protocol A: The Juice Sprint (Isolate & Re-tune)

Freeze all work on new levels or secondary features for 1 sprint. Focus 100% of team effort on amplifying the physical feedback of your primary core action:

- **Visuals:** Add screen shake, camera lean, muzzle flashes, impact sparks, hit-pause (freeze frames), and clear UI hit-markers.
    
- **Audio:** Replace weak placeholder sounds with punchy, distinct audio effects; add clear audio cues for success and failure states.
    
- **Feel:** Reduce input lag, widen animation cancel windows, and tighten movement stop/start responsiveness.
    
- **The Grey-Box Test:** Test this action in a blank, untextured grey-box environment. If pressing the button isn't inherently satisfying in a grey box, it isn't ready for the full game.
    

##### Protocol B: The Input Streamlining Pass

If playtesters avoid a feature due to menu or control frustration:

- Cut the required button presses or menu clicks in half.
    
- Convert multi-click sub-menus into a single contextual button press or quick radial wheel (e.g., point at a target and press one button to order a squad, rather than opening a tactical menu).
    

### Step 3: Spec Sheet Entry

Once Phase 1 is validated and resolved, copy the code block below into your team's project workspace (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 1: Core Loop & Playtest Reception Audit
- **Core Loop Action Audited:** 
- **Observed Playtester Symptom:** 
- **Primary Feedback Chain Failure:** [ ] Input Delay | [ ] Weak Feedback/Juice | [ ] High Input Friction
- **Selected Recovery Protocol:** [ ] Juice Sprint | [ ] Input Streamlining Pass
- **Action Items for Team:**
  1. 
  2. 
```



# Phase 2: Hybridization Friction & Cognitive Overload Diagnostic

### Step 1: Concept Guardrail

If you come from an engineering background, think of the player's brain as a **single-threaded CPU**. If you come from an art or UI background, think of the player's brain as a **focal canvas with limited screen real estate**.

When you combine multiple genres (e.g., FPS + RTS + Factory Automation), you are asking the player's "human CPU" to process radically different types of cognitive tasks at the exact same time:

- **Reflexive / Twitch Tasks (Action / FPS):** High urgency, hyper-local focus, immediate muscle memory.
    
- **Tactical / Overview Tasks (RTS / Strategy):** Medium-to-high urgency, broad map awareness, spatial management.
    
- **Systemic / Logic Tasks (Automation / Simulation):** Low urgency, deep problem-solving, input-to-output optimization.
    

When two or three of these tasks demand immediate attention simultaneously, the player experiences **Cognitive Overload**.

Trained designers use this phase to catch systemic friction early; non-designers can use it to settle team deadlocks (_"Why are players ignoring the RTS mechanics we spent three months coding?"_). The problem is rarely that a feature is "bad", it is that the game is asking the player to run two high-stress mental threads at the same second.

> When mechanics from different genres fight for the same mental thread or screen space, consult [[Game Design/Genre Dissection/The Hybridization Collision Matrix\|The Hybridization Collision Matrix]] to see pre-cataloged collision types and industry-standard resolution patterns.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Review your playtest recordings, bug reports, or internal team feedback.
    
2. Identify moments where mechanics from different genres overlap or fight for control during live gameplay.
    
3. Map the **observable playtest symptom** and the **internal team debate** onto the table below to uncover the root systemic friction.
    

#### Phase 2 Audit Table (Mid-Dev Collision Diagnostic)

|**Clashing Mechanics**|**Playtest Symptom (What Players Do)**|**Internal Team Argument**|**Real Systemic Friction Type**|
|---|---|---|---|
|**FPS Shooting + RTS Squad Command**|Players ignore squad commands completely and play it as a pure FPS.|_"Engineers spent weeks on squad AI, but players never order them during combat!"_|**Attention Split:** The player cannot look down a sniper scope and scan a minimap simultaneously.|
|**Direct Combat + Base Building**|Players get blown up while sitting motionless in a base-construction menu.|_"Artists want immersive menus; coders say players keep dying while browsing them."_|**Avatar Vulnerability:** The player's physical avatar is undefended while their mind is in a menu.|
|**Action Fighting + Supply Automation**|Players run out of ammo mid-boss fight because a factory belt jammed miles away.|_"The economy is broken because players can't fix factory bottlenecks during boss fights."_|**Pacing Contradiction:** High-urgency survival vs. low-urgency maintenance.|

#### Red Flag Diagnostic 2.1: The Human CPU Bottleneck

Evaluate your live build against these two pass/fail conditions:

- **Condition A (System Abandonment):** Do playtesters consistently ignore a major gameplay system (e.g., never issuing squad orders, never deploying turrets) during high-stress combat moments?
    
- **Condition B (Menu Death):** Do players regularly take damage or die while trying to navigate an interface, command wheel, or camera view required by a secondary genre?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your build has triggered **Red Flag 2.1: The Human CPU Bottleneck**. Your combined genres are fighting for the same mental thread. Adding more tutorial pop-ups will not fix this; you must change the systemic rules handling the collision.
>     

#### Resolution Protocols for Red Flag 2.1 (Objective Team Rules)

When your team is deadlocked on how to fix a clashing feature, do not compromise by adding more UI clutter. Apply one of these three hard rules:

##### Protocol A: Temporal Separation (The "One Thing at a Time" Rule)

Separate conflicting mechanics in time so they never demand high cognitive focus simultaneously.

- **Systemic Rule:** If System A requires high reflexes (combat) and System B requires deep planning (building/automation), split gameplay into distinct, alternating phases (e.g., _Phase 1: Safe Build/Planning Phase_ $\rightarrow$ _Phase 2: High-Urgency Defense Phase_).
    

##### Protocol B: Cognitive Offloading (Delegate to Code)

If two systems must occur at the same time, write code to automate or protect the secondary system so the player doesn't have to micromanage it under stress.

- **Systemic Rule:** When the player enters a top-down strategic view or menu, an **Autopilot AI** automatically takes over their physical character, causing it to duck into cover and enter defensive fire mode until the player returns.
    

##### Protocol C: HUD Abstraction (Simplify the View)

If secondary sub-menus distract from the primary action view, remove full-screen interfaces and replace them with rapid contextual overlays.

- **Systemic Rule:** Replace multi-click menus with a single 3D world ping or a quick radial wheel that executes in under 0.5 seconds without closing the primary 1st/3rd-person camera view.
    

### Step 3: Spec Sheet Entry

Once Phase 2 is resolved, copy the code block below into your team's project workspace (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 2: Hybridization Friction & Cognitive Overload
- **Clashing Mechanics Identified:** 
- **Observed Playtest Symptom:** 
- **Root Friction Type:** [ ] Attention Split | [ ] Avatar Vulnerability | [ ] Pacing Contradiction
- **Team Resolution Protocol Selected:** [ ] Temporal Separation | [ ] Cognitive Offloading (AI) | [ ] HUD Abstraction
- **Technical/Design Rule Implemented:**
  - *Example: When player opens tactical map, local vehicle auto-brakes and engages AI defensive turrets.*
```



# Phase 3: Design Debt & Parasite Feature Elimination

### Step 1: Concept Guardrail

In mid-production, the most dangerous systems aren't the ones that are obviously broken, they are **Parasite Mechanics**.

A Parasite Mechanic is a secondary system that consumes a massive portion of your team's programming, art, and QA bandwidth while contributing almost zero noticeable fun, depth, or retention for the player.

> High Maintenance Effort + Low Playtest Value = Parasite Feature



Teams usually fall into the **Sunk Cost Trap**: _"We spent three months coding custom physics for destructible base walls, so we can't just throw it away!"_

If an engineer spends 40% of their week fixing edge-case bugs on a feature that playtesters barely notice or actively complain about, that feature is actively starving your core engine of polish. Trained designers use this phase to run cold, objective audits on feature ROI; non-designer teams can use it to break sunk-cost paralysis and cut feature debt safely.

>To learn how to evaluate feature cost multipliers, system-dependency risk, and load-bearing mechanics, consult [[Game Design/Genre Dissection/The Genre Execution and Scoping Blueprint\|The Genre Execution and Scoping Blueprint]].

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Open your project backlog, bug tracker, or task board.
    
2. List every active secondary feature currently implemented in your build.
    
3. Rate each feature on two scales: **Maintenance & Bug Effort** (How often does it break or require custom work?) vs. **Playtest Value** (How much do players praise or rely on it?).
    

#### Phase 3 Audit Table (Feature ROI Matrix)

|**Implemented Feature**|**Maintenance & Bug Effort**|**Playtest Value / Fun Output**|**Team Reality / Symptom**|**Feature Classification**|
|---|---|---|---|---|
|**Direct Vehicle Combat**|Low (Stable core code)|**High** (Players love it)|Primary driver of player engagement.|**Core Engine (Keep)**|
|**Factory Conveyor Belts**|**High** (Spline bugs, pathing errors)|Medium (Niche appeal)|Eats 30% of engineering time; causes performance drops.|**High-Debt Supporting**|
|**Dynamic Weather & Mud**|**High** (Tire physics bugs, GPU load)|**Low** (Players don't care)|Constant physics glitches; zero impact on core tactics.|**Parasite Feature (Cut)**|
|**Manual Ammo Crafting**|Medium (UI & inventory bugs)|**Low** (Annoys players)|Players run out of ammo mid-fight and complain about menus.|**Parasite Feature (Cut)**|

#### Red Flag Diagnostic 3.1: The Parasite Feature Trap

Evaluate your live build against these two pass/fail conditions:

- **Condition A (Maintenance Imbalance):** Is your team spending **more than 30% of sprint time** fixing bugs on secondary or cosmetic systems while your primary core loop still feels unpolished?
    
- **Condition B (The Unread Log):** Is there a complex mechanics pipeline (e.g., crafting trees, weather simulation, diplomacy meters) that playtesters consistently ignore unless forced by a pop-up tutorial?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your build has triggered **Red Flag 3.1: The Parasite Feature Trap**. You are carrying design debt that will slow down your entire production pipeline.
>     

#### Resolution Protocols for Red Flag 3.1 (Surgical De-Escalation)

When a feature is classified as a Parasite Feature, apply one of these two recovery protocols:

##### Protocol A: Surgical Amputation (Delete & Replace with Static Values)

Remove the complex, bug-prone system entirely from code and replace its design purpose with a simple static variable or passive buff.

- **Example Fix:** Delete the bug-heavy dynamic mud/weather physics system. Replace it with a static +10% speed buff on paved roads and a simple visual particle spray. You gain 100 hours of engineering time back while preserving the visual fantasy.
    

##### Protocol B: Systemic Consolidation (Merge Weak Systems)

If two secondary features are individually weak and fiddly, collapse them into a single streamlined background loop.

- **Example Fix:** Instead of requiring manual ore mining _and_ manual ammo crafting in separate UI menus, consolidate them into a single passive "Supply Depot" structure that automatically converts collected Ore into Ammo over time.
    

### Step 3: Spec Sheet Entry

Once Phase 3 is completed, copy the code block below into your team's project workspace (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 3: Design Debt & Parasite Feature Elimination
- **Parasite Feature(s) Identified:** 
- **Bug/Maintenance Impact on Team:** 
- **Playtest Reception:** [ ] Ignored by Players | [ ] Source of Frustration | [ ] Low Value
- **Selected Recovery Protocol:** [ ] Surgical Amputation | [ ] Systemic Consolidation
- **Execution Plan:**
  - *Feature Removed:* 
  - *Simplified Replacement / Static Value:* 
```




# Phase 4: The Surgical Cut & Dependency Matrix

### Step 1: Concept Guardrail

When a team agrees that a feature needs to be cut or simplified, they immediately run into the primary engineering nightmare: **Cascade Dependency Risk**.

>Target Cut (Feature X) ──> Breaks Economy ──> Breaks UI ──> Breaks Enemy AI


Because game systems are interconnected, engineers often object to cuts by saying: _"If we delete the manual ammo crafting system, we have to rewrite the inventory UI, break the resource economy, re-balance all loot drops, and rewrite enemy wave spawning!"_

Faced with weeks of refactoring, teams frequently surrender and keep bad mechanics in the build.

The goal of Phase 4 is **safe systemic decoupling**. You do not need to rewrite your entire codebase to delete a bad feature. By using "Stubbing" techniques or reverting custom systems back to industry-standard conventions, you can isolate the bad mechanic, bridge the gap for dependent systems, and safely remove player-facing friction in a single afternoon.

> When replacing a broken custom mechanic with a familiar industry standard, consult [[Game Design/Genre Dissection/The Convention Subversion Framework\|The Convention Subversion Framework]] to preserve player legibility and control familiarity.


### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Take the feature(s) identified for removal or overhaul from Phase 3.
    
2. Map out every secondary system in your project that consumes data or resources from that feature.
    
3. Evaluate the technical breakage risk and assign a decoupling solution before deleting a line of code.
    

#### Phase 4 Audit Table (Dependency Mapping)

|**Target Feature to Cut**|**Connected Dependent Systems**|**Technical Breakage Risk**|**Decoupling / Bridge Solution**|
|---|---|---|---|
|**Manual Ammo Crafting Menu**|Weapons System, Loot Drops, Inventory UI|**High** (Guns crash if ammo pool isn't fed by crafting script).|**Stub & Bridge:** Remove the crafting menu. Make enemies drop flat ammo packs directly into the gun's existing ammo counter.|
|**Custom Vehicle Physics Script**|Vehicle Health, Driving UI, Enemy Pathfinding|**High** (AI relies on custom raycasts to track vehicles).|**Reversion to Standard:** Replace custom physics script with standard engine vehicle controller; pass identical transform data to AI.|
|**Complex Base Power Grid**|Turrets, Shield Generators, Factory Belts|**Medium** (Turrets check power grid state before firing).|**Static Override:** Remove power lines. Hard-code `isPowered = true` on all placed structures.|

#### Red Flag Diagnostic 4.1: Cascade Dependency Risk

Evaluate your live build against these two pass/fail conditions:

- **Condition A (Architecture Hostage):** Is your team keeping an unfun, high-maintenance feature in the build _solely_ because deleting it would require refactoring multiple dependent systems?
    
- **Condition B (Refactoring Paralysis):** Has an engineering task to "simplify a mechanic" expanded into a multi-week refactoring nightmare that touches UI, economy, and AI code simultaneously?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your project has triggered **Red Flag 4.1: Cascade Dependency Risk**. You are letting legacy code hold your game's design hostage.
>     

#### Resolution Protocols for Red Flag 4.1 (Decoupling Strategies)

Do not attempt a massive full-code refactor during mid-production. Apply one of these two decoupling protocols to execute a clean cut:

##### Protocol A: The Stub & Bridge Method (Hard-Coded Feeders)

Instead of deleting the underlying variables that dependent systems rely on, remove the complex player-facing mechanic and replace its output with a hard-coded "Stub" value.

- **The Rule:** If System B expects a value from System A (e.g., _Turrets require Power from Power Grid_), delete the player-facing Power Grid UI/building mechanic, but leave a simple background script that feeds a constant `Power = 100` to System B. Dependent code stays stable, but the player no longer suffers through a clunky mechanic.
    

##### Protocol B: Reversion to Industry Standard

If a custom-coded control scheme, inventory system, or camera transition is creating cascade bugs, scrap the custom solution entirely and drop in a standard, proven template or engine default.

- **The Rule:** Replace custom, fragile input/inventory code with standard engine components (e.g., Unity/Unreal default character controllers or standard 2D grid inventory assets). Grounding the game in standard conventions reduces code friction and instantly improves player legibility.
    

### Step 3: Spec Sheet Entry

Once Phase 4 is resolved, copy the code block below into your team's project workspace (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 4: The Surgical Cut & Dependency Matrix
- **Target Feature Cut:** 
- **Connected Dependent Systems:** 
- **Cascade Risk Level:** [ ] High | [ ] Medium | [ ] Low
- **Selected Recovery Protocol:** [ ] Stub & Bridge Method | [ ] Reversion to Industry Standard
- **Decoupling Action Items for Engineering:**
  1. *UI Action:* Remove player-facing interface for target feature.
  2. *Code Action:* Inject hard-coded stub value to keep dependent systems stable.
```



# Phase 5: Production Choke Points & Alpha Hardening

### Step 1: Concept Guardrail

The transition from Vertical Slice to Alpha is where projects either stabilize or quietly die of exhaustion. The primary killer of mid-production builds is **Design Ambiguity**.

When a core mechanic remains partially designed or subject to ongoing tweaks, it creates a massive production bottleneck across every discipline:

- **Art Waste:** Artists spend weeks modeling, texturing, and animating assets for a vehicle class or building tier that eventually gets cut or reworked.
    
- **Engineering Paralysis:** Coders build overly generic, complex architectures to "future-proof" against design ideas that haven't been finalized.
    
- **QA Fatigue:** Testers log bugs on features that are constantly shifting, creating noise that obscures game-breaking bugs in your core loop.
    

>Design Ambiguity ──> Engineering Over-Architecture + Wasted Art Assets ──> Production Choke Point


Alpha does not mean "polished and bug-free", it means **Feature Complete**. Once you enter the Alpha Hardening phase, the feature list is locked. No new mechanics, no extra sub-systems, and no "quick little ideas" are allowed into the build. 100% of team bandwidth shifts from _feature creation_ to _balancing, bug fixing, performance optimization, and feel tuning_.

>For strategies on calculating production velocity, setting hard feature boundaries, and preventing late-stage scope creep, consult [[Game Design/Genre Dissection/The Genre Execution and Scoping Blueprint\|The Genre Execution and Scoping Blueprint]].


### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Gather your entire feature backlog, active task boards, and wishlist items.
    
2. Audit every system that is currently listed as "In-Progress," "Half-Done," or "Planned for Alpha."
    
3. Evaluate whether each feature is truly load-bearing or if it is creating a production bottleneck for art and engineering.
    

#### Phase 5 Audit Table (Alpha Scope Alignment)

|**Feature / System**|**Current Build Status**|**Production Bottleneck Created**|**Playtest Necessity**|**Alpha Scope Action**|
|---|---|---|---|---|
|**Primary Vehicle Weapons**|80% Complete|Low (Stable code; needs balancing)|**Critical** (Core combat)|**Lock & Polish**|
|**Secondary Tech Tree Menu**|30% Complete|**High** (UI blocked waiting on final design rules)|Low (Confuses players)|**Quarantine / Cut**|
|**Destructible Terrain Physics**|50% Complete|**High** (Causes frame drops; blocks level art)|Medium (Nice to have)|**Freeze & Static Replace**|
|**Custom Emote / Cosmetic System**|0% (Planned)|Medium (Demands 3D animation time)|**Zero** (Cosmetic only)|**Hard Quarantine**|

#### Red Flag Diagnostic 5.1: Post-Slice Scope Creep

Evaluate your live project against these two pass/fail conditions:

- **Condition A (Moving Goalposts):** Is your team still designing or proposing new gameplay mechanics within 60 days of your target Alpha / Beta milestone?
    
- **Condition B (Interdisciplinary Blockers):** Are artists or programmers actively waiting on "design decisions" before they can finish core assets or close out major bug tickets?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your project has triggered **Red Flag 5.1: Post-Slice Scope Creep**. You are suffering from design ambiguity that will delay your launch or burn out your team.
>     

#### Resolution Protocols for Red Flag 5.1 (Alpha Hardening)

To clear production choke points and harden your build for launch, execute these non-negotiable protocols:

##### Protocol A: The Hard Feature Freeze

Declare an immediate, absolute freeze on new feature code.

- **The Rule:** No new systems, sub-menus, or mechanics may be added to the project repository. Any pull request containing a new mechanic is automatically rejected. All task boards are converted strictly to: _Bug Fixes, Performance Optimization, Sound/Juice Polish, and Numerical Balance_.
    

##### Protocol B: The Backlog Quarantine

Move all un-implemented or partially built wishlist items into a locked "Post-Launch / Sequel" archive.

- **The Rule:** If a feature is less than 50% functional in the build today, it is quarantined. If the game cannot function without it, apply **Phase 4: Protocol A (The Stub & Bridge Method)** to replace it with a simple static variable rather than spending 4 weeks trying to finish complex code.
    

### Step 3: Spec Sheet Entry

Once Phase 5 is resolved, copy the code block below into your team's project workspace (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 5: Production Choke Points & Alpha Hardening
- **Alpha Feature Lock Date:** 
- **Production Choke Points Cleared:** 
- **Quarantined / Postponed Features (Moved to Backlog Archive):**
  1. 
  2. 
- **Primary Focus for Remaining Sprints:** [ ] Bug Fixing | [ ] Game Feel & Juice | [ ] Balance & Tuning
```



# Master Deliverable: The Mid-Dev Design Health Brief

### How to Synthesize Your Diagnostic Results

Once you have completed the audits and diagnostics in Phases 1 through 5, copy the code block below directly into your project's knowledge base (Obsidian, Notion, or local Markdown vault).

This synthesized document serves as your **Mid-Dev Design Health Brief**, a clear, objective directive that captures all feature cuts, team agreements, stub bridges, and scope boundaries. It acts as an authoritative, single source of truth for your engineering, art, QA, and production leads as you harden your build for Alpha.

Markdown

```
# [Project Working Title] - Mid-Dev Design Health Brief

> **Status:** Mid-Production Audit / Alpha Hardening  
> **Build Version Audited:** [e.g., v0.4.2-alpha]  
> **Target Milestone:** [e.g., Vertical Slice / Alpha Lock]  
> **Lead / Team:** [Names / Disciplines Involved]  
> **Date:** [YYYY-MM-DD]

---

## 1. Core Loop & Feedback Diagnostic
- **Core Loop Action Audited:** 
- **Observed Playtester Symptom:** 
- **Identified Feedback Failure:** [ ] Input Lag | [ ] Weak Visual/Audio Juice | [ ] High Input Friction
- **Selected Recovery Protocol:** [ ] Juice Sprint | [ ] Input Streamlining Pass
- **Immediate Polishing Actions:**
  1. 
  2. 

---

## 2. Hybridization & Cognitive Load Resolution
- **Clashing Mechanics Identified:** 
- **Root Friction Type:** [ ] Attention Split | [ ] Avatar Vulnerability | [ ] Pacing Contradiction
- **Team Resolution Agreement (Systemic Rule):** 
  - *Example: When player opens map/menus, local vehicle auto-brakes and engages AI defensive turrets.*

---

## 3. Parasite Feature Cut List
- **Excised / Amputated Features (High Cost / Low Value):**
  1. 
  2. 
- **Simplified Replacement / Static Value Strategy:**
  - *Example: Removed dynamic mud physics; added static +10% speed buff on paved roads.*

---

## 4. Systemic Cuts & Stub Bridges
- **Target Feature Cut:** 
- **Connected Dependent Systems:** 
- **Decoupling Protocol Selected:** [ ] Stub & Bridge Method | [ ] Reversion to Industry Standard
- **Engineering Action Items:**
  1. *UI:* 
  2. *Code / Stub Feeder:* 

---

## 5. Alpha Feature Lock & Production Alignment
- **Hard Feature Freeze Date:** [YYYY-MM-DD]
- **Quarantined / Postponed Features (Moved to Backlog Archive):**
  1. 
  2. 
- **Primary Team Focus for Remaining Sprints:** [ ] Bug Fixing | [ ] Game Feel & Juice | [ ] Balance & Tuning
```
