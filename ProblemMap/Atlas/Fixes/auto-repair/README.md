# Auto Repair v1

🛠️ **Auto Repair v1** is the first structured extension layer built on top of the Atlas fix system.

This folder does **not** claim that fully autonomous repair is already solved.

What it does claim is simpler and more useful:

> the Atlas now has a clear path from  
> **route → first repair direction → repair planning architecture**

This folder exists to define that path clearly, safely, and in a way that can grow without breaking the current system.

---

## What Auto Repair means here

In this project, **auto repair** does **not** mean:

- an AI blindly changing prompts
- an AI guessing random fixes
- an AI claiming full root-cause closure by itself
- a magic one-shot repair engine

Instead, auto repair means:

> a structured repair layer that starts **after Atlas routing**
> and turns diagnosis into a controlled repair workflow

In practical terms, the intended flow is:

1. route the case with the Atlas  
2. identify the likely failure family and broken invariant  
3. choose the most appropriate first repair family  
4. generate a constrained repair plan  
5. validate whether the repair improved the case  
6. escalate, revise, or rollback if needed

So this folder is not a replacement for the Atlas.

It is a **next layer** that depends on the Atlas being correct first.

---

## Where this sits in the full system

The current system can be understood like this:

```text
Problem Map 3.0
→ Troubleshooting Atlas
→ Canonical Casebook
→ Atlas-to-AI Adapter
→ Fix Surface
→ Auto Repair
→ WFGY Deep Repair
````

The key distinction is:

* **Atlas** decides where the failure belongs
* **Fix Surface** suggests the first repair direction
* **Auto Repair** turns that into a structured repair workflow
* **WFGY Deep Repair** remains the deeper engine layer for harder and more abstract cases

This means Auto Repair is a **bridge layer**, not the final repair engine.

---

## Current status of v1

📌 **Current status: early structured planning layer**

Auto Repair v1 is intentionally limited.

At this stage, the folder is meant to define:

* what auto repair is
* what it is not
* how it relates to Atlas and WFGY
* which repair actions are safe enough to plan first
* which parts are still future work

So this v1 is mainly:

* architecture
* boundary setting
* schema thinking
* phased roadmap

It is **not yet**:

* a fully implemented repair engine
* a full autonomous execution loop
* a complete repair benchmark system

That limitation is intentional.

---

## Why this folder matters

🧭 The Atlas already does something very important:

* it classifies failures
* it distinguishes neighboring failure regions
* it suggests the first repair move

But there is still a gap between:

> “this is probably an F4 failure”

and

> “here is a safe, structured repair workflow for that F4 failure”

This folder exists to close that gap.

It is the place where the project begins to move from:

* diagnosis only

toward:

* diagnosis plus controlled repair planning

That shift is a very big deal, so it needs its own clear layer.

---

## Scope of Auto Repair v1

### Included in v1

✅ Auto Repair v1 is intended to cover:

* system positioning
* architecture explanation
* safety boundary
* phased roadmap
* repair action schema direction
* validation loop direction
* rollback thinking
* recommended first target families

### Not included in v1

⏳ Auto Repair v1 does **not** yet include:

* full executable repair code
* full autonomous patch generation
* full automated verification across all families
* fully closed repair loops
* aggressive high-risk repair for boundary-heavy families
* large-scale benchmark automation

This README is therefore a **foundation document**, not a claim of full completion.

---

## Phase plan

To keep this safe and buildable, Auto Repair is divided into phases.

### Phase 0 · Architecture and scope

This is the phase currently being established.

Focus:

* define the purpose
* define the boundaries
* define how Auto Repair fits the Atlas
* define what kind of repair actions should eventually exist

Deliverables:

* README
* architecture note
* safety note
* action-schema note
* roadmap

### Phase 1 · Repair planner

Goal:

Turn routed cases into a **structured repair plan**, without yet claiming fully autonomous execution.

Expected outputs:

* likely repair family
* 1 to 3 candidate repair actions
* misrepair risk
* what to validate next
* when to escalate to deeper WFGY repair

This is likely the first truly useful operational milestone.

### Phase 2 · Semi-auto repair execution

Goal:

Support limited repair execution in safer regions.

Examples may include:

* grounding repair suggestions
* execution-gate insertion suggestions
* observability uplift suggestions
* schema / container tightening suggestions

This phase should stay constrained and auditable.

### Phase 3 · Validation and rollback loop

Goal:

Evaluate whether a proposed repair actually improved the case.

This includes:

* before / after comparison
* invariant-level checking
* failure persistence detection
* rollback rules
* escalation logic

This is the hardest phase and should not be rushed.

---

## Safety boundary

⚠️ Auto Repair must stay disciplined.

A few rules are already clear even before implementation:

1. **Route first, repair second**
   Auto Repair should never skip Atlas routing.

2. **First move only, not fantasy closure**
   Early versions should focus on the first repair move, not pretend to solve everything.

3. **Validation is mandatory**
   A repair proposal without a validation path is incomplete.

4. **Rollback must exist**
   If a repair makes the system worse, the workflow must support backing out.

5. **Not all families are equally safe for early auto repair**
   Some family regions are much better first targets than others.

---

## Best early candidates

For early auto repair development, the safest starting regions are:

### F1 · Grounding & Evidence Integrity

Good early targets:

* re-grounding
* evidence filtering
* anchor re-check
* chunk-to-target correction

Why it is a good first target:

* the repair surface is often relatively concrete
* before / after comparison is easier
* misrepair is easier to detect

### F4 · Execution & Contract Integrity

Good early targets:

* readiness gate insertion
* ordering validation
* block-until-ready logic
* closure-path hardening

Why it is a good first target:

* many failures are workflow-structural
* repair actions are often explicit
* the success condition is often clear

### F7 · Representation & Localization Integrity

Good early targets:

* schema tightening
* JSON shell correction
* descriptor tightening
* container validation

Why it is a good first target:

* structure is often visible
* repair outcomes are inspectable
* replay demos are easier to build

---

## Higher-risk regions

Some areas should be treated much more carefully.

### F5

Auto Repair can help with:

* observability uplift
* trace insertion
* logging suggestions

But there is risk in mistaking visibility improvement for full repair.

### F3

Some continuity scaffolds may be possible, but deeper continuity repair can get complicated quickly.

### F6

🚫 This is **not** a good place for aggressive early auto repair.

Boundary-heavy cases often require:

* judgment
* intervention restraint
* explicit escalation
* stronger human review

Early F6 work should lean toward:

* planner mode
* warning mode
* stabilization suggestions

not full automatic execution.

---

## Recommended file growth inside this folder

As this layer grows, a reasonable structure would look like:

```text
auto-repair/
├── README.md
├── auto-repair-roadmap-v1.md
├── auto-repair-architecture-v1.md
├── auto-repair-safety-boundary-v1.md
├── repair-action-schema-v1.md
├── repair-validation-loop-v1.md
├── rollback-policy-v1.md
├── recipes/
├── prompts/
├── json/
└── demos/
```

Not all of these need to be created immediately.

The important thing is that the growth path is now clear.

---

## What this folder should achieve in the next step

The next useful milestone is **not** “full auto repair.”

The next useful milestone is:

> a clean and disciplined **repair planner layer**

That means the immediate next step should probably define:

* repair action schema
* repair planner prompt logic
* repair validation logic
* rollback discipline

If those are done well, later execution work will have a much stronger foundation.

---

## Official v1 interpretation

The correct interpretation of Auto Repair v1 is:

> the first structured planning layer for Atlas-based repair has been established,
> but autonomous repair execution remains a future-stage build.

This wording is strong, honest, and safe.

---

## One-line status

**Auto Repair v1 defines the architecture, scope, and staged roadmap for Atlas-based repair planning. Full autonomous repair remains future work.**

---

## Back to the Atlas

For the full atlas system, go back to:

* `ProblemMap/wfgy-ai-problem-map-troubleshooting-atlas.md`
* `ProblemMap/Atlas/README.md`

If you like the project, ⭐ star the repo and follow the Atlas branch as it grows.
