---
{"dg-publish":true,"permalink":"/game-design/workbooks-and-tools/ideation-and-discovery/unfiltered-ideation-and-the-context-dump/","dg-note-properties":{}}
---

In a studio environment, high-level game vision is forged through casual conversation. Developers gather, pitch wild scenarios, debate edge cases, and ask "what if?" long before writing a single spec. Working solo or in small teams, however, often leads to designing in a vacuum. Without that collaborative ping-pong, you end up laying track directly in front of a moving train, building mechanics and tuning systems without a clear, shared map of where the game is actually headed.

When high-level intent, potential mechanics, and unresolved design questions live exclusively in your head, they remain invisible to collaborators, playtesters, and external tools. Prematurely forcing these loose ideas into rigid documentation or code usually kills creativity or results in scope creep.

This worksheet provides a structured method for **Unfiltered Ideation**, a process designed to extract every loose concept, conditional feature, emotional hook, and unsolved design problem out of your head and onto the page without judgment or self-censorship.


> ### **Worksheet Objectives**
> 
> 1. **Externalize High-Level Vision:** Turn abstract "maybe" ideas into documented design intent.
>     
> 2. **Uncover Invisible Dependencies:** Identify hidden design bottlenecks (e.g., _"We can't solve character progression until we settle economy scaling"_) before touching code.
>     
> 3. **Establish Project Anchor Points:** Filter raw enthusiasm down into non-negotiable design pillars and explicit out-of-scope guardrails.
>     
> 4. **Create a Living Context Brief:** Produce a single, comprehensive source of truth that communicates the overall direction and philosophy of your project to anyone, or anything, assisting in its development.
>     

## Instructions & Mindset

Before proceeding to the exercises, adopt the following rules for this stage:

- **Silence the Producer Mind:** Do not worry about budget, technical complexity, or timeline right now. Feasibility filtering happens later.
    
- **Embrace the "Maybes":** If a feature is something you _might_ add down the line, write it down alongside the condition that would trigger it (e.g., _"Maybe add an durability system IF combat feels too forgiving"_).
    
- **Prioritize Raw Intent Over Organization:** Messy clarity is better than pristine ambiguity. Don't worry about formatting, grammar, or polished terminology during the dump phase.

## Phase 1: The Unfiltered Spew (Stream-of-Consciousness Capture)

The objective of this phase is speed and total externalization. You are not writing documentation; you are clearing out working memory. Do not correct grammar, format paragraphs, or evaluate whether an idea is "too hard to program."

### Execution Rules

1. **Set a Timer:** Block off 20 to 30 minutes without interruptions.
    
2. **Use High-Speed Capture:** Use voice-to-text on your phone/computer, a recorded audio log, or rapid typing in a raw text file (`.txt` or Scratchpad). Speak or type as fast as you think.
    
3. **Never Backspace or Edit:** If you contradict yourself, keep going. Record the contradiction (e.g., _"Actually, scratch that, what if it's turn-based instead?"_).
    
4. **Log the Hesitations:** If you aren't sure about something, log the _reason_ you are unsure (e.g., _"I want active reload, but it might distract from tactical positioning"_).
    

### Trigger Prompts for the Capture Session

If you hit a wall during the dump, talk through these five prompt categories in order, hopefully these start the snowball effect of creating the mental vomiting of your ideas:

#### 1. Core Fantasy & Emotional Hook

- What is the absolute coolest thing a player will do in this game?
    
- What specific feeling should the player have during a high-stakes moment (e.g., panicking, feeling like a tactical mastermind, relaxed exploration)?
    
- If a player is telling a friend about their play session, what specific story or moment are they describing?
    

#### 2. Mechanics, Systems, & "Maybes"

- What are all the mechanical systems floating around in your head, confirmed or unconfirmed?
    
- What are the "maybe" features? List them alongside their conditional triggers (e.g., _"Maybe add hunger mechanics IF the game feels too easy"_).
    
- What controls or inputs feel non-negotiable?
    

#### 3. Steals, Inspirations, & Genre Irritations

- What exact moments or mechanics are you stealing from other games?
    
- What annoys you about existing games in this genre that this project will fix or do differently?
    
- What games does this look like on the surface, and where does it break away from them?
    

#### 4. Unsolved Dependencies & Blockers

- What design problems are currently keeping you up at night?
    
- What are the "We can't decide X until we solve Y" bottlenecks currently sitting in your path?
    
- What edge cases are you worried might break the core loop?

## Phase 2: Signal Extraction & Clustering

Once the raw capture is complete, you will have a disorganized wall of text or a rough audio transcript. In this phase, parse that text and group the raw thoughts into five functional design buckets.

### The 5 Context Buckets

Review your raw capture and highlight or move statements into the following categories:

|**Bucket**|**Definition**|**What to Extract**|
|---|---|---|
|**1. Emotional Thesis**|The core fantasy, tone, and player feelings.|Desired player emotions, pacing notes, fantasy tropes to embrace or subvert.|
|**2. Signature Beats**|Specific moments, scenarios, or set-pieces envisioned.|"The player drops into a dark room with only a flare," "Executing a perfect combo chains across three enemies."|
|**3. Core Loop & Active Features**|Mechanics that must exist for the game to function at a baseline level.|Primary movement, primary verbs, win/loss conditions, core progression loops.|
|**4. Feature Backlog & Conditions**|Unconfirmed "maybe" ideas and experimental mechanics.|Any feature logged with a conditional trigger (e.g., "Add weapon durability _if_ ammo scarcity isn't enough").|
|**5. Design Blockers & Dependencies**|Open questions, missing system connections, and unresolved logic.|"How do players acquire new skills?", "Does inventory pause the game or run in real-time?"|

## Phase 3: High-Level Vision Anchoring

With your ideas categorized into buckets, Phase 3 condenses that raw material into hard project constraints. This step establishes non-negotiable boundaries that protect your scope, resolve design ties, and prevent feature creep during development.

### 1. The Core Fantasy Statement (1–2 Sentences)

Combine your **Emotional Thesis** and **Signature Beats** into a single statement describing what the game is and how it feels to play.

- **Formula:** _"(Game Title) is a (Genre) where players experience (Core Emotional Hook) by (Primary Verbs), featuring (Key Differentiator)."_
    
- **Example:** _"Project Void is a tactical survival horror game where players experience overwhelming vulnerability by scavenging space stations with failing power, relying on sound cues rather than firepower to survive."_
    

### 2. Establish Design Pillars (3–4 Max)

Design pillars are fundamental, non-negotiable rules derived from your raw dump. When faced with two competing design ideas later in development, these pillars determine which choice wins.

- **Criteria for a Good Pillar:**
    
    - It must be specific enough to reject features (e.g., _"Movement is always momentum-based"_ is actionable; _"Gameplay is fun"_ is useless).
        
    - It must reflect the emotional thesis established in Phase 2.
        
- **Format:**
    
    - **Pillar 1: (Name)** - (1-sentence explanation of how this dictates design).
        
    - **Pillar 2: (Name)** - (1-sentence explanation of how this dictates design).
        
    - **Pillar 3: (Name)** - (1-sentence explanation of how this dictates design).
        

### 3. Define Out-of-Scope Guardrails ("What We Are NOT Doing")

Explicitly defining what your project avoids is just as important as defining what it includes. Identify elements common to your genre that you are intentionally excluding to protect scope or vision.

- _Example:_ _"We are NOT making a multiplayer game; all mechanics must support a single-player focus."_
    
- _Example:_ _"We are NOT implementing deep crafting; equipment is acquired strictly through combat or exploration."_
    

## Phase 4: The Living Context Brief (Master Template)

The final output of this workbook is the **Living Context Brief**. This document sits at the root of your project repository, serving as the master context source for you, your collaborators, playtesters, and external tooling.

Copy and fill out the template below using the results from Phases 1–3:

Markdown

```
# [Project Working Title] - Living Context Brief

## 1. High-Level Vision Anchor
* **Core Fantasy Statement:** [Insert 1-2 sentence fantasy statement]
* **Target Audience / Mood:** [Target emotional response, e.g., Tense, Methodical, Fast-Paced]
* **Design Pillars:**
  1. **[Pillar 1 Title]:** [Short description]
  2. **[Pillar 2 Title]:** [Short description]
  3. **[Pillar 3 Title]:** [Short description]

## 2. Explicit Out-of-Scope Guardrails
* [Guardrail 1: e.g., No procedural generation; maps are hand-crafted.]
* [Guardrail 2: e.g., No real-time combat; all encounters are strictly turn-based.]
* [Guardrail 3: e.g., No cosmetic customization system.]

## 3. Confirmed Core Loop & Active Features
* **Primary Loop:** [Step 1] -> [Step 2] -> [Step 3]
* **Active Systems:**
  * **[System 1]:** [Brief overview of functionality]
  * **[System 2]:** [Brief overview of functionality]

## 4. Exploration Sandbox (Conditional & "Maybe" Features)
| Feature / System Idea | Conditional Trigger (When do we build this?) | Status |
| :--- | :--- | :--- |
| [e.g., Weapon Durability] | [If playtesters report combat feels too low-stakes] | Exploring |
| [e.g., Skill Tree] | [If flat stat upgrades lack long-term progression depth] | On Hold |

## 5. Active Design Blockers & Open Dependencies
* **[Blocker 1]:** [e.g., How does health recovery work without breaking the tension loop?]
  * *Current Hypotheses:* [Option A vs Option B]
* **[Blocker 2]:** [e.g., We cannot lock down ammo distribution until enemy health pools are balanced.]
```


## Section 5: Document Lifecycle & Readiness Checklist

A Living Context Brief is not a static design document that gets written once and archived. It functions as active working memory for your project. As prototyping begins and ideas collide with actual playtesting, this document must adapt.

  
### Living Document Protocol (Keeping It Alive)

1. **The Sandbox Rule:** Every new idea that emerges during development must enter the **Exploration Sandbox** table first. Never move an untested idea directly into the **Confirmed Core Loop** without a clear validation trigger.
    
      
    
2. **Monthly Scope Audits:** Review Section 2 (Out-of-Scope Guardrails) at the start of every sprint or milestone. If a new system has crept into development without explicitly clearing your design pillars, kill it or force it through the sandbox process.
    
      
    
3. **Resolving Blockers:** As design blockers in Section 5 are solved through prototyping, record the winning hypothesis and move the resulting mechanic into Section 3 (Active Features).
    
      
    

### Readiness Audit Checklist

Before using your Living Context Brief to write technical specifications, build prototypes, or feed external tooling, verify that it passes this readiness check:

|**Check**|**Requirement**|**Status**|
|---|---|---|
|**High-Level Clarity**|Can a collaborator or playtester read Section 1 and immediately explain the game's core hook without asking for clarification?|[ ]|
|**Pillar Actionability**|Does every Design Pillar pass the "Rejection Test"? (Does it provide enough clarity to actively reject an out-of-scope feature?)|[ ]|
|**Guardrail Strictness**|Are there at least 3 explicit "NOT doing" rules defined to protect scope?|[ ]|
|**Conditional Triggers**|Does every feature in the Exploration Sandbox have a clear condition attached to it rather than just a vague "maybe"?|[ ]|
|**Explicit Bottlenecks**|Are all known "We can't solve X until Y" design dependencies logged with current hypotheses?|[ ]|

## Section 6: Next Steps in the Pipeline

With your **Living Context Brief** established, you now have a high-level anchor for your project's vision, boundaries, and open questions.

  

To take these ideas from initial capture to technical validation, proceed to the next workbook in the pipeline:

- **Next Workbook:** [[Game Design/Workbooks & Tools/Pre-Production/Concept Stress-Test Workbook\|Concept Stress-Test Workbook]] - _Deconstruct your core mechanics, evaluate technical feasibility, and stress-test your design assumptions before committing to production._

- **Related Models:** [[Game Design/Frameworks & Models/DORK Model/DORK Model\|DORK Model]] | [[Game Design/Frameworks & Models/MDA Framework/MDA Framework\|MDA Framework]]


## Section 7: Worked Example (From Raw Spew to Context Brief)

To see how this process works in practice, consider this example walk-through for a hypothetical solo-developed project, **Project Rust & Shadow**.

### Step 1: The Raw Voice-to-Text Spew (Snippet)

> _"Okay so I want to make this game where you play as an old mech pilot trapped on a scrap planet. It's top-down or maybe isometric, super gritty. You're scavenging parts, but every time you move it makes noise, right? So sound is like super important. Maybe if you sprint your engine overheats and blips on enemy radar. What if there's no UI for heat and you have to listen to the engine whining? That'd be sick. Wait, is it an extraction shooter? No, I don't want forced multiplayer. Single-player only. But I want that feeling of high-stakes extraction where if you die you lose your haul. Maybe a durability system for parts? Actually, durability sucks if it feels tedious, so only break parts if you take critical heat damage. We can't figure out how the scrap economy works until we know how many parts drop per encounter though. Need to solve that."_
> 
>   

### Step 2: Signal Extraction & Clustering

Using the 5 Context Buckets, the developer parses the raw dump:


- **Emotional Thesis:** High-stakes tension, methodical stealth through sound management, feeling like a vulnerable mech scavenger.  
    
- **Signature Beats:** Engine audio cues indicating heat level instead of UI meters; scrambling to extract before enemy radar locks on.
    
- **Core Loop & Active Features:** Top-down/isometric movement; scavenging scrap; heat/sound emission loop; high-stakes single-player extraction. 
    
- **Feature Backlog & Conditions:** Part durability system _(Condition: Only apply durability penalties if the player overheats the engine, not on standard wear-and-tear)_.
    
- **Design Blockers & Dependencies:** Scrap economy scaling is locked behind determining average part drop rates per encounter.
    

### Step 3: The Resulting Living Context Brief

Markdown

```
# Project Rust & Shadow - Living Context Brief

## 1. High-Level Vision Anchor
* **Core Fantasy Statement:** Project Rust & Shadow is a single-player tactical survival game where players pilot a rickety scrap mech, balancing noise emission and engine heat while scavenging high-value salvage from hostile zones.
* **Target Audience / Mood:** Tense, Methodical, Paranoiac.
* **Design Pillars:**
  1. **Audio as Primary UI:** Engine stress and enemy threats are communicated through positional audio cues rather than heavy HUD elements.
  2. **Risk-Driven Locomotion:** Every movement choice balances speed against noise signature; fast movement is a tactical liability.
  3. **High-Stakes Salvage:** Extraction is always opt-in, but failure means losing collected loot.

## 2. Explicit Out-of-Scope Guardrails
* **No Multiplayer / PVP:** The game is strictly a single-player offline experience.
* **No Tedious Durability:** Parts do not degrade through normal use, only via critical thermal overload.
* **No Direct Dogfighting:** Mechs are slow and vulnerable; head-on combat is a failure state, not the primary loop.

## 3. Confirmed Core Loop & Active Features
* **Primary Loop:** Deploy into drop zone -> Scavenge scrap while managing heat/sound -> Reach extraction point -> Upgrade mech at home base.
* **Active Systems:**
  * **Thermal & Acoustic Emission:** Mech movement generates heat and sound, triggering enemy AI alerts.
  * **Audio-Driven Engine State:** Whines and rattles signal engine stress without on-screen meters.

## 4. Exploration Sandbox (Conditional & "Maybe" Features)
| Feature / System Idea | Conditional Trigger (When do we build this?) | Status |
| :--- | :--- | :--- |
| Critical Component Damage | If playtesters find overheating has no real consequences | Exploring |
| Dynamic Weather Interference | If radar mechanics need more tactical variance in late game | On Hold |

## 5. Active Design Blockers & Open Dependencies
* **[Blocker 1]:** Scrap Economy Balance.
  * *Current Hypotheses:* We cannot lock down component upgrade costs until average loot yield per run is benchmarked in greybox testing.
```