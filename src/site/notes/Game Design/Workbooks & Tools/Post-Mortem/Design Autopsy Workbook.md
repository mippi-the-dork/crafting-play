---
{"dg-publish":true,"permalink":"/game-design/workbooks-and-tools/post-mortem/design-autopsy-workbook/","dg-note-properties":{}}
---

# How to Use This Workbook

### 1. Purpose & Mindset: The Forensic Approach

Whether you are a Lead Designer conducting a post-mortem on a shipped title, a solo developer dissecting your last prototype, or an engineer analyzing a market competitor to understand why its mechanics clicked, this workbook is built for your workflow.

When evaluating a finished or released game, most post-mortems fall into the trap of subjective commentary (_"The combat was fun, but the pacing felt off"_). Broad observations don't help you build better games in the future. To extract real value from a shipped project or case study, you must adopt a **forensic mindset**: treating the game as a mechanical engine to be deconstructed, diagnosing exact causes for systemic failures, and cataloging the specific architectures that drove its successes.

The goal of this workbook is twofold:

- **Autopsy:** Pinpoint the precise structural reasons why certain mechanics failed, clashed, or bloated the build.
    
- **Extraction:** Identify the "load-bearing" design wins and turn them into permanent, reusable design rules for your team's vault.
    

### 2. Dual-Track Setup: Choose Your Subject

This workbook operates on two parallel tracks depending on your current objective:

- **Track A: Internal Post-Mortem (Your Game)**
    
    Use this track after shipping a commercial title, closing a prototype phase, or canceling a project. The focus is on auditing team assumptions against real player data, reviews, and bug logs to prevent repeating design mistakes on your next title.
    
- **Track B: External Game Teardown (Market Study)**
    
    Use this track to reverse-engineer an existing title—whether a smash hit, an underrated indie gem, or a high-profile commercial failure. The focus is on deconstructing another studio's systemic execution to learn from their triumphs and missteps.
    

### 3. Prerequisites: What to Bring to This Session

Before starting Phase 1, select your subject game and gather your reference materials:

- **Subject Data:**
    
    - _For Track A (Internal):_ Player telemetry, review scores/criticism, post-launch bug logs, and team retrospective notes.
        
    - _For Track B (External):_ 10–20 hours of hands-on play (or detailed long-form gameplay footage), community review consensus, and breakdown videos/articles.
        
- **Core Reference:** Keep [[Game Design/Genre Dissection/Genre Dissection\|Genre Dissection]] open as a structural baseline for evaluating genre conventions, motivation drivers, and hybridization matrices.
    

### 4. The 3-Step Micro-Framework

Every phase in this workbook uses a standardized 3-step loop:

|**Step**|**Phase Stage**|**Primary Action**|**Plain-English Meaning**|**Expected Output**|
|---|---|---|---|---|
|**Step 1**|**Concept Guardrail**|Read & Understand|Learn the forensic principle and analytical trap to avoid.|A clear lens for evaluating system interaction.|
|**Step 2**|**Stress-Test Audit**|Analyze & Evaluate|Map observed symptoms onto the audit table and run diagnostics.|An identified design win, collision, or subversion failure.|
|**Step 3**|**Spec Sheet Entry**|Extract & Document|Copy the finalized Markdown block directly to your project vault.|Permanent design rules for your knowledge base.|

### 5. The 3 Autopsy Classifications

During your analysis, every major system in the subject game will fall into one of three classifications:

|**Classification**|**Definition**|**Analytical Focus**|**Team Outcome**|
|---|---|---|---|
|**1. Load-Bearing Win**|A system or loop that directly drove player satisfaction and fulfilled the core fantasy.|Why did this work? How did feedback and math align?|**Archive & Replicate:** Turn into a standard design rule for future projects.|
|**2. Systemic Friction**|A collision between mechanics, camera views, or pacing structures that caused player fatigue or drop-off.|Where did the systems clash? Was it an attention split or cognitive overload?|**Redesign Protocol:** Execute a theoretical fix pass in Phase 4.|
|**3. Subversion Failure**|A broken or subverted genre rule that caused confusion rather than novelty.|Did the subversion break legibility without offering an equal payoff?|**Revert or Re-anchor:** Document the lesson to avoid fake innovation traps.|



# Phase 1: Core Fantasy & Load-Bearing Wins

### Step 1: Concept Guardrail

In architecture, a **load-bearing wall** is one that supports the weight of the entire building above it. Remove it, and the structure collapses. In game design, a **Load-Bearing Mechanic** is a core loop or feedback system that directly supports the player's core power fantasy or psychological motivation.

When analyzing a released game, you must separate **Load-Bearing Mechanics** from **Surface Polish**:

>Total Player Retention = Core Fantasy Realization (Load-Bearing Mechanics) + Surface Polish (Visuals, Audio, Narrative)


A game can have massive AAA budgets, stunning particle effects, and orchestral scores, yet still leave players feeling unengaged if its underlying loops lack systemic weight. Conversely, games with simple retro graphics or low budgets frequently become massive hits because their core mechanics realization is rock-solid.

When running a forensic teardown, your first job is to isolate the _exact systemic architecture_ that made the game satisfying, stripping away the visual/audio spectacle to see what mechanics were carrying the weight.

> Review [[Game Design/Genre Dissection/The Player Fantasy Motivation Framework\|The Player Fantasy Motivation Framework]] to map the subject game's primary load-bearing mechanics directly to fundamental player motivation drivers (e.g., Mastery, Autonomy, Expression, Destruction).

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Select the top 2–3 mechanics or loops that received the highest praise in playtests, user reviews, or critical reception.
    
2. Evaluate each feature in total isolation: _If we stripped away all high-end graphics, sound effects, and story context, would this core interaction still be inherently satisfying in a grey box?_
    
3. Map your findings onto the audit table below.
    

#### Phase 1 Audit Table (Load-Bearing Wins Audit)

|**System / Loop Audited**|**Surface Polish Level (Art/FX/Audio)**|**Grey-Box Systemic Depth**|**Player / Review Reception**|**Systemic Classification**|
|---|---|---|---|---|
|**Parry & Counter System**|High (Sparks, slow-mo, heavy sound)|**High** (Tight timing windows, posture damage system, high risk/reward)|_"Combat feels insanely crisp and rewarding."_|**Load-Bearing Win (Archive)**|
|**Loot & Inventory Manager**|Medium (Clean UI, rare item glows)|**Low** (Flat stat inflation, no meaningful mechanical choices)|_"Spent half the game sorting clutter for +2% stats."_|**Surface Mask (Do Not Copy)**|
|**Base Building / Customization**|High (Beautiful modular art assets)|**High** (Unlocks new automation routes and tactical defense options)|_"Building felt meaningful and drove the late game."_|**Load-Bearing Win (Archive)**|

#### Red Flag Diagnostic 1.1: The False Positive Trap

Evaluate your subject game against these two pass/fail conditions:

- **Condition A (Visual Masking):** Is a feature praised primarily for its animations, audio punch, or visual spectacle rather than the depth of its underlying mechanical choices?
    
- **Condition B (Gated Fun):** Is a core mechanic only satisfying after the player completes hours of grinding, upgrading, or reading tutorial text?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, you have identified a **False Positive**. Copying this mechanic into a new project without its massive production budget or polish budget will result in a flat, unengaging loop.
>     

#### Extraction Protocol for Load-Bearing Wins

When a feature is verified as a true **Load-Bearing Win**, extract its design rules using these three steps:

1. **Isolate the Math & Rules:** Identify the core variables (e.g., input buffering frames, risk/reward multipliers, resource conversion rates).
    
2. **Identify the Feedback Chain:** Document the exact combination of visual, audio, and gameplay state changes that communicated success to the player.
    
3. **Formulate the Reusable Rule:** Express the win as a clear, context-free design guideline for your team's permanent vault (e.g., _"High-risk defensive actions must reward immediate offensive action frames, not passive stat buffs"_).
    

### Step 3: Spec Sheet Entry

Once Phase 1 is complete, copy the code block below into your team's project vault (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 1: Core Fantasy & Load-Bearing Wins
- **Subject Game:** 
- **Verified Load-Bearing Win:** 
- **Primary Fantasy Driver Satisfied:** [ ] Mastery | [ ] Autonomy | [ ] Expression | [ ] Destruction
- **Why It Worked (Grey-Box Mechanics):** 
- **Extracted Design Rule for Future Vault:**
  - *Rule:* 
```



## Phase 2: Systemic Friction & Collision Autopsy

### Step 1: Concept Guardrail

When reviewing player feedback, critic reviews, or telemetry drop-off charts, you will rarely see players diagnose systemic design flaws directly. Instead, they report **symptoms**:

- _"The mid-game feels like an unbearable grind."_
    
- _"The combat got repetitive and exhausting after 5 hours."_
    
- _"I hated having to stop the action to manage my inventory."_
    

In forensic design, your job is to look past the surface complaint to find the **Root Cause**. Nine times out of ten, mid-game pacing crashes, combat fatigue, and menu frustration are caused by **Systemic Hybridization Collisions**—instances where two or more genre mechanics are actively fighting for the player's mental processing bandwidth or disrupting game pacing.

>Surface Symptom ("Boring Mid-Game") ──> Systemic Root Cause (Unseparated Pacing Contradiction)


Treating the symptom (e.g., adding more enemy types or lowering enemy health) will not fix a game with fundamental systemic collision. In this phase, you will trace negative player sentiment directly back to the architectural friction points that caused it.

> When analyzing collisions between sub-genres or perspective models, consult [[Game Design/Genre Dissection/The Hybridization Collision Matrix\|The Hybridization Collision Matrix]] to identify structural conflict patterns (such as Avatar Vulnerability, Pacing Contradiction, or Camera/Control Clashes).

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Collect negative player reviews, critical teardowns, or internal post-mortem pain points regarding the subject game.
    
2. Group the complaints by common themes (e.g., pacing, menu overload, difficulty spikes, mechanical confusion).
    
3. Trace each complaint back to its underlying genre collision using the audit table below.
    

#### Phase 2 Audit Table (Systemic Collision Diagnostic)

|**Observed Player/Review Symptom**|**Surface Level Complaint**|**Underlying Systemic Collision**|**Root Design Cause**|
|---|---|---|---|
|**Pacing Drop-off at Hour 10**|_"Game turns into a tedious chore list."_|**Pacing Contradiction:** High-urgency action vs. high-friction manual resource gathering.|Forcing real-time combat players to manually micro-manage factory lines without automation.|
|**Combat Fatigue / Frustration**|_"Boss fights feel cheap and overwhelming."_|**Attention Split:** 3rd-person reflex combat vs. full-screen skill tree selection.|Requiring real-time stance switching through multi-tier sub-menus during active boss attacks.|
|**High Player Drop-off at Chapter 2**|_"Stealth mechanics felt terrible and clunky."_|**Camera & Control Conflict:** Top-down tactical vision forced into 1st-person camera.|Demanding precision line-of-sight sneaking without providing spatial vision tools (e.g., radar/minimap).|

#### Red Flag Diagnostic 2.1: Fatal Systemic Friction

Evaluate your subject game against these two pass/fail conditions:

- **Condition A (Systemic Avoidance):** Did players regularly bypass or express hatred toward a mechanic that was required to complete the main progression loop?
    
- **Condition B (Cognitive Spike):** Did the game force players to juggle two high-urgency mechanics from different genres at the exact same moment without providing automation or pause states?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, the game suffered from **Fatal Systemic Friction**. The failure was not a lack of polish—it was a structural flaw in how genre rules were combined.
>     

#### Forensic Autopsy Protocol for Systemic Friction

When a major collision is diagnosed, run the following 3-part autopsy:

1. **Identify the Collision Class:** Was it an _Attention Split_ (competing focal points), _Avatar Vulnerability_ (menu death), or _Pacing Contradiction_ (conflicting mechanical urgency)?
    
2. **Determine the Failure State:** Did the collision cause players to quit (Choke Point), ignore a system (System Abandonment), or experience cognitive fatigue (Burnout)?
    
3. **Formulate the Lessons Learned:** Document what rule was broken so your team never attempts this specific mechanical combination without a proper mitigation framework.
    

### Step 3: Spec Sheet Entry

Once Phase 2 is complete, copy the code block below into your team's project vault (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 2: Systemic Friction & Collision Autopsy
- **Subject Game:** 
- **Observed Surface Symptom:** 
- **Identified Collision Type:** [ ] Attention Split | [ ] Avatar Vulnerability | [ ] Pacing Contradiction | [ ] Control Conflict
- **Root Cause Mechanics:** 
- **Forensic Lesson Extracted:**
  - *Never combine [Mechanic A] and [Mechanic B] without implementing [Mitigation Rule / Automation / Phase Separation].*
```



## Phase 3: Innovation & Convention Subversion Post-Mortem

### Step 1: Concept Guardrail

Genre conventions exist for a reason: they are **mental shortcuts** that allow players to instantly understand how to interact with your game without reading a manual. When a player sees a red barrel, they expect it to explode; when they press `R`, they expect to reload; when they open a map, they expect orientation icons.

Trained designers follow the **80/20 Rule of Innovation**:

Player Comfort = 80% Standard Scaffolding (Genre Conventions) + 20% Targeted Subversion (Unique Hook)


When a game breaks or subverts a standard convention, it incurs a **Legibility Tax**. If that subversion provides a massive, delightful psychological payoff (e.g., turning reload mechanics into a active timing minigame like _Gears of War_), the tax is worth paying.

However, if a game subverts a convention purely to be "different"—or fails to provide clear visual anchors for the new rule—the subversion becomes a **Gratuitous Innovation**. In this phase, you will evaluate the subject game's rule-breaking choices to determine whether they yielded true innovation or merely created legibility tax and player frustration.

> To analyze how genre conventions can be subverted cleanly without destroying player legibility, consult [[Game Design/Genre Dissection/The Convention Subversion Framework\|The Convention Subversion Framework]].

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. List 2–4 instances where the subject game intentionally broke, removed, or inverted standard conventions of its base genre.
    
2. Evaluate player reception: _Did players praise the change as fresh and innovative, or did they struggle with confusion, orientation loss, or control frustration?_
    
3. Map the subversions onto the audit table below.
    

#### Phase 3 Audit Table (Subversion Evaluation Matrix)

|**Subverted Genre Convention**|**Intended Design Goal**|**Player Legibility Impact**|**Observed Player / Review Result**|**Subversion Outcome**|
|---|---|---|---|---|
|**Removed UI Minimap in Open-World RPG**|Encourage organic environment exploration.|**High Friction** (Players lost spatial orientation).|_"I spent 30% of my playtime opening the main map menu."_|**Failed Subversion (High Legibility Tax)**|
|**Replaced XP Levels with Item-Based Mastery**|Encourage build experimentation over grinding.|**High Clarity** (Clear, tangible item choices).|_"Loved that my power was tied to gear synergies rather than level numbers."_|**Successful Innovation (High Payoff)**|
|**Removed Active Reloading Button**|Force strategic weapon-swapping in combat.|**Medium Friction** (Violated muscle memory).|_"Kept pressing 'R' by accident and dying during fights."_|**Gratuitous Innovation (Muscle Memory Conflict)**|

#### Red Flag Diagnostic 3.1: The Gratuitous Innovation Trap

Evaluate your subject game against these two pass/fail conditions:

- **Condition A (Legibility Tax):** Did playtesters or reviewers require extensive tutorial text, menu warnings, or hours of practice just to relearn a basic action that other genre games execute intuitively?
    
- **Condition B (Zero-Sum Subversion):** Did subverting a standard rule increase player friction without delivering a clear, distinct psychological payoff?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, the game suffered from **Gratuitous Innovation**. The development team paid a heavy legibility cost to subvert a rule that didn't need breaking.
>     

#### Forensic Autopsy Protocol for Subversion Failures

When a subversion failure is identified, run the following recovery protocol:

1. **Identify the Violated Contract:** What standard player expectation or muscle memory shortcut was broken (e.g., camera controls, health regeneration, inventory mapping)?
    
2. **Calculate the Payoff-to-Friction Ratio:** Did the novelty of the new mechanic outweigh the mental fatigue required to learn it?
    
3. **Formulate the Reversion/Anchor Rule:** Determine whether the fix requires **reverting to the industry standard** or **adding strong visual/audio legibility anchors** to support the subversion.
    

### Step 3: Spec Sheet Entry

Once Phase 3 is complete, copy the code block below into your team's project vault (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 3: Innovation & Convention Subversion Post-Mortem
- **Subject Game:** 
- **Subverted Convention Audited:** 
- **Intent vs. Reality:** 
- **Legibility Assessment:** [ ] High Payoff (Keep / Replicate) | [ ] Gratuitous Friction (Revert to Standard)
- **Extracted Design Lesson:**
  - *Lesson:* Subverting [Standard Convention] only succeeds if supported by [Legibility Anchor / Mechanical Payoff].
```



## Phase 4: Theoretical Redesign & Fix Protocols

### Step 1: Concept Guardrail

Identifying flaws in a shipped or post-mortem game is only half the exercise. The true test of design mastery is **Redesign Execution**: engineering concrete, systemic fixes for those flaws without destroying what made the game special in the first place.

The primary trap during a post-mortem redesign is **Over-Correction**:

Net Design Gain = Eliminated System Friction - Damage to Core Wins


If a game’s combat was praised for being visceral and chaotic (Load-Bearing Win), but players hated taking damage while navigating full-screen inventory menus (Systemic Friction), deleting the inventory system entirely or making combat slow and turn-based is an over-correction. You have eliminated the friction, but you destroyed the core fantasy in the process.

A successful redesign acts as surgical intervention: it isolates the broken systemic connection, replaces or decouples the clashing rules, and leaves the surrounding load-bearing mechanics intact.

> Review [[Game Design/Genre Dissection/The Genre Execution and Scoping Blueprint\|The Genre Execution and Scoping Blueprint]] to ensure your proposed redesign fix aligns with reasonable technical scope and systemic complexity.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Take the top systemic failures and failed subversions identified in Phase 2 and Phase 3.
    
2. For each failure, engineer a specific, rule-based redesign pass.
    
3. Stress-test your redesign against Phase 1: _Does this proposed fix preserve our primary load-bearing wins, or does it accidentally neutralize them?_
    

#### Phase 4 Audit Table (Theoretical Redesign Matrix)

|**Identified Systemic Failure**|**Original Broken Mechanic**|**Proposed Redesign Pass**|**Preserved Load-Bearing Win**|**Expected Outcome**|
|---|---|---|---|---|
|**Menu Death during Boss Fights** (Phase 2 Collision)|Full-screen skill tree and stance wheel required in real-time combat.|Convert stance switches to contextual 1-button triggers on dodge/parry.|Fast, fluid, visceral action combat.|Eliminates menu deaths while increasing combat momentum.|
|**Pacing Crash in Chapter 2** (Phase 2 Collision)|Manual resource mining required to fuel weapon crafting.|Replace manual mining with automated "Supply Drops" awarded via combat performance.|Deep weapon customization and synergy theorycrafting.|Removes tedious harvesting grind while reinforcing the combat loop.|
|**Spatial Disorientation** (Phase 3 Subversion)|Removed minimap and HUD navigation icons entirely.|Re-introduce a minimalist compass bar with distance pings; keep full minimap off screen.|Organic, immersive environmental discovery.|Restores navigation clarity without cluttering the screen view.|

#### Red Flag Diagnostic 4.1: The Over-Correction Trap

Evaluate your proposed redesigns against these two pass/fail conditions:

- **Condition A (Collateral Damage):** Does your proposed fix simplify a broken mechanic by removing or diluting the core risk/reward loop that players originally loved?
    
- **Condition B (Identity Erasure):** Does your fix make the game feel so safe and conventional that it loses its unique genre hook entirely?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your fix is an **Over-Correction**. You must adjust the redesign to protect the core fantasy while removing the friction.
>     

#### Redesign Protocols for Phase 4

When formulating a fix for a systemic failure, apply one of these three surgical protocols:

##### Protocol A: Surgical Isolation (Decouple & Separate)

If two systems fight for the player's immediate attention, do not delete either system—separate them into alternating phases or distinct camera states so they never collide.

- **Redesign Rule:** _When the player enters (State A), System B is paused or converted into an automated background process until (State A) resolves._
    

##### Protocol B: Cognitive Offloading (Delegate to Code)

If a secondary mechanic forces players to multitask beyond human CPU capacity during high-stress moments, write code logic to automate or streamline the secondary task.

- **Redesign Rule:** _Automate (Secondary Task) via contextual AI triggers whenever the player is actively engaged in (Primary High-Urgency Loop)._
    

##### Protocol C: Re-Anchoring (Provide Visual / Audio Scaffolding)

If a subverted rule caused player confusion, keep the subversion but add clear visual, audio, or tactile feedback anchors so the player instantly understands the new state.

- **Redesign Rule:** _Whenever (Subverted Rule) triggers, immediately play (High-Contrast Visual/Audio Cue) to anchor player legibility._
    

### Step 3: Spec Sheet Entry

Once Phase 4 is complete, copy the code block below into your team's project vault (Obsidian, Notion, or local notes file).

Markdown

```
### Phase 4: Theoretical Redesign & Fix Protocols
- **Subject Game:** 
- **Systemic Failure Addressed:** 
- **Original Mechanic:** 
- **Proposed Redesign Pass:** 
- **Redesign Protocol Selected:** [ ] Surgical Isolation | [ ] Cognitive Offloading | [ ] Re-Anchoring
- **Protected Load-Bearing Win:** 
  - *Verification:* Fix removes friction without degrading [Primary Fantasy / Core Loop].
```



## Phase 5: Transferable Design Rules & Vault Extraction

### Step 1: Concept Guardrail

The ultimate goal of a post-mortem or game teardown is not merely to critique the past—it is to build **institutional memory**.

In game development, the most expensive mistake a studio or developer can make is **Design Amnesia**: finishing a project (or moving to a new one) without codifying what was learned, causing the team to repeat the exact same systemic mistakes two years later on a new codebase.

To turn hindsight into foresight, you must convert the specific findings of your teardown into **Transferable Design Rules**. A transferable design rule is a concise, context-free imperative that can be pasted into your team's design vault or project wiki and applied directly to future prototypes.

Institutional Memory = Codified Design Rules / Total Post-Mortem Insights



If an insight cannot be stated as an actionable "If / Then" or "Never / Always" rule, it remains abstract commentary. Phase 5 is about extracting hard rules that will save your team hundreds of hours on your next project.

> Cross-reference your extracted rules with the [[Game Design/Genre Dissection/Genre Glossary\|Genre Glossary]] to standardize terminology across your team's documentation vault.

### Step 2: Stress-Test Audit & Diagnostics

#### Instructions for the Team

1. Review the outputs from Phase 1 (Load-Bearing Wins), Phase 2 (Systemic Collisions), Phase 3 (Subversion Failures), and Phase 4 (Redesign Passes).
    
2. Distill each finding down to a universal, context-free design directive.
    
3. Map your extracted rules onto the audit table below to verify their clarity and future applicability.
    

#### Phase 5 Audit Table (Rule Extraction Matrix)

|**Source Teardown Finding**|**Original Context**|**Universal Design Rule (Vault Directive)**|**Application to Future Projects**|
|---|---|---|---|
|**Parry Feedback Win** (Phase 1)|High-risk timing window with instant posture reward.|**Rule 1:** Defensive actions with narrow timing windows must yield immediate offensive action frames, never delayed stat buffs.|Standard directive for all future melee/action prototypes.|
|**Menu Death Collision** (Phase 2)|Player dying while managing inventory in combat.|**Rule 2:** Never require full-screen menu navigation while the player's avatar is vulnerable in real-time combat space.|Mandatory architectural constraint for UI/UX engineering.|
|**Minimap Subversion** (Phase 3)|Removing minimap caused spatial disorientation.|**Rule 3:** Removing standard navigation HUD elements requires providing spatial compass anchors or high-contrast visual landmarks.|Pre-production checklist item for open-world design.|

#### Red Flag Diagnostic 5.1: The Design Amnesia Trap

Evaluate your team's post-mortem process against these two pass/fail conditions:

- **Condition A (Vague Conclusions):** Are your post-mortem takeaways phrased as broad complaints (e.g., _"We need better pacing next time"_) rather than explicit, enforceable design rules?
    
- **Condition B (Siloed Knowledge):** Do post-mortem findings remain trapped in a presentation slide deck or retrospective doc that no engineer or designer consults when starting a new project?
    

> **DIAGNOSTIC STATUS:**
> 
> - If you answered **YES** to either condition, your team has triggered **Red Flag 5.1: The Design Amnesia Trap**. You are risking repeated design debt on your next production cycle.
>     

#### Rule Formulation Protocol

To ensure an extracted design rule is actionable for future projects, structure it using this 3-part blueprint:

1. **The Condition:** State the context or mechanic being implemented (_"When implementing real-time combat menus..."_).
    
2. **The Constraint:** State the non-negotiable design limitation (_"...never occupy more than 25% of screen space or obscure the player avatar..."_).
    
3. **The Payoff:** State the psychological or usability goal (_"...so that spatial awareness and combat reactivity remain uninterrupted."_).
    

### Step 3: Spec Sheet Entry

Once Phase 5 is complete, copy the code block below into your team's permanent design vault (Obsidian, Notion, or internal wiki).

Markdown

```
### Phase 5: Transferable Design Rules & Vault Extraction
- **Subject Game Audited:** 
- **Extracted Design Directive 1:** 
  - *Rule:* 
  - *Applicability:* [ ] Combat | [ ] Economy | [ ] UI/UX | [ ] World Structure
- **Extracted Design Directive 2:** 
  - *Rule:* 
  - *Applicability:* [ ] Combat | [ ] Economy | [ ] UI/UX | [ ] World Structure
- **Vault Location Updated:** 
```



## Master Deliverable: The Design Autopsy Brief

### Synthesizing Your Teardown into an Actionable Brief

Once you have completed the forensic audits across Phases 1 through 5, copy the Markdown block below into your team's knowledge base or project vault (Obsidian, Notion, or local wiki).

This synthesized **Design Autopsy Brief** consolidates your findings into a single, permanent reference document. It ensures that the load-bearing wins, systemic failure autopsies, proposed redesign fixes, and extracted design rules are cataloged for your current team and future projects.

Markdown

```
# [Game Title] — Design Autopsy & Teardown Brief

> **Status:** Post-Mortem / External Teardown Complete  
> **Subject Game:** [Title & Version/Build Audited]  
> **Teardown Type:** [ ] Internal Post-Mortem | [ ] External Game Teardown  
> **Core Genre Hybrid:** [e.g., FPS + RTS / Action RPG + Automation]  
> **Auditors / Analysts:** [Names / Disciplines]  
> **Date:** [YYYY-MM-DD]

---

## 1. Executive Summary & Core Fantasy
- **Primary Psychological Fantasy:** [e.g., Tactical Mastery / Creative Expression / High-Speed Destruction]
- **Core Loop Summary:** 
- **Overall Teardown Verdict:** [Brief 2-3 sentence overview of what made the game succeed or fail]

---

## 2. Verified Load-Bearing Design Wins (Archive & Replicate)
- **Primary Load-Bearing Win:** 
- **Why It Worked (Grey-Box Mechanics):** 
- **Primary Psychological Driver Satisfied:** [ ] Mastery | [ ] Autonomy | [ ] Expression | [ ] Destruction
- **Extracted Reusable Design Rule:** 
  - *Rule:* 

---

## 3. Autopsy of Systemic Failures & Collisions
- **Primary Systemic Friction Point:** 
- **Observed Surface Symptom:** [e.g., "Mid-game pacing crash at hour 10"]
- **Identified Collision Type:** [ ] Attention Split | [ ] Avatar Vulnerability | [ ] Pacing Contradiction | [ ] Control Conflict
- **Root Cause Mechanics:** 
- **Forensic Lesson Learned:** 

---

## 4. Innovation & Convention Subversion Post-Mortem
- **Subverted Genre Convention:** 
- **Legibility Assessment:** [ ] High Payoff (Keep / Replicate) | [ ] Gratuitous Friction (Revert to Standard)
- **Key Takeaway:** 

---

## 5. Theoretical Redesign Pass (The Surgical Fix)
- **Identified Failure Addressed:** 
- **Original Broken Mechanic:** 
- **Proposed Redesign Pass:** 
- **Redesign Protocol Selected:** [ ] Surgical Isolation | [ ] Cognitive Offloading | [ ] Re-Anchoring
- **Protected Load-Bearing Win:** [Verifying fix doesn't destroy the core fantasy]

---

## 6. Permanent Transferable Design Rules (Vault Directives)
*Copy these directives directly into your studio's permanent design wiki:*

1. **Directive 1 (Combat / Controls):** 
2. **Directive 2 (UI / UX / Cognitive Load):** 
3. **Directive 3 (Pacing / Economy):** 
```
