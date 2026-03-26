<!--
AI_NOTE_START

Document role:
This page is the implementation plan for WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Turn the current Twin Atlas documentation stack into an actionable implementation plan.
2. Define the near-term build order for public layer completion, coupling work, runtime behavior, and demo alignment.
3. Clarify what belongs to the public effective layer and what remains hidden as internal substrate.
4. Provide a realistic implementation sequence that supports MVP progress without blocking on full formalization.

How to use this page:
1. Read this page after the roadmap, Bridge implementation notes, and coupling flow page.
2. Use it as the main implementation-facing planning surface for the next build phase.
3. Use it to align docs work, runtime work, Bridge work, and demo work.
4. Treat this page as a build plan, not as proof that all listed items are already complete.

Important boundary:
This page does not expose hidden internal reasoning substrate details.
It only describes the public effective-layer build plan and the implementation sequence around it.
It also does not claim that every future closed-loop runtime detail or formalization step is already complete.

Recommended reading path:
1. Twin Atlas README
2. FAQ
3. Roadmap
4. Bridge Implementation Notes
5. Twin Atlas Coupling Flow
6. This page
7. Runtime files
8. Demo files

AI_NOTE_END
-->

# 🛠️ Implementation Plan

> The implementation-facing plan for WFGY 4.0 Twin Atlas Engine.

Twin Atlas has already crossed an important threshold.

It is no longer only a concept cluster.

It now has:

- a public engine identity
- a Bridge specification layer
- a demo proof surface
- a runtime surface
- a coupling-flow definition
- a growing documentation stack that already behaves like a real product skeleton

That means the project now needs a real implementation plan.

Not just “more ideas later.”

A real plan.

This page defines that plan.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](./README.md) |
| FAQ | [FAQ](./faq.md) |
| Roadmap | [Roadmap](./roadmap.md) |
| Release Notes | [Release Notes](./release-notes.md) |
| Bridge Home | [Bridge README](./Bridge/README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](./Bridge/bridge-v1-spec.md) |
| Bridge Implementation Notes | [Bridge Implementation Notes](./Bridge/bridge-implementation-notes.md) |
| Demos Home | [Demos README](./demos/README.md) |
| Runtime Home | [Runtime README](./runtime/README.md) |
| Coupling Flow | [Twin Atlas Coupling Flow](./runtime/twin-atlas-coupling-flow.md) |
| Basic Runtime | [Twin Atlas Basic](./runtime/twin-atlas-basic.txt) |
| Advanced Runtime | [Twin Atlas Advanced](./runtime/twin-atlas-advanced.txt) |
| Strict Runtime | [Twin Atlas Strict](./runtime/twin-atlas-strict.txt) |

---

## ⚡ The shortest version

If you only remember one thing, remember this:

**the next phase is not identity invention.  
the next phase is implementation convergence.**

That means:

1. finish and stabilize the public effective layer  
2. align runtime behavior with the coupling flow  
3. turn Bridge from design surface into real handoff behavior  
4. use demo cases as implementation targets  
5. continue deeper formalization without blocking MVP progress

That is the implementation plan in one paragraph.

---

# 🧭 Section 1 · Implementation Philosophy

Twin Atlas should not be built in the wrong order.

The wrong order would be:

- chase full theoretical closure first
- delay usable surfaces
- delay demo surfaces
- delay runtime behavior
- delay coupling targets
- treat implementation as something that happens “after the real ideas”

That is not the right posture here.

The right order is:

### 1. stabilize the public effective layer
### 2. define a minimal healthy coupling loop
### 3. make runtime behavior reflect that loop
### 4. use demo cases as implementation targets
### 5. deepen formalization in parallel or after MVP stabilization

This order protects momentum and prevents theoretical ambition from blocking usable progress.

---

# 🧱 Section 2 · Build Boundary

Before the actual build sequence, the project boundary must stay clear.

## ✅ Public effective layer
This is what the current Twin Atlas docs and runtime files define.

It includes:

- Twin Atlas public architecture
- Bridge public role and spec
- demo surfaces
- runtime entry files
- coupling flow at the effective-layer level

This is the layer that should become increasingly usable and inspectable.

## 🔒 Hidden internal substrate
This is the internal reasoning substrate used to support deeper orchestration.

This layer should remain hidden.

It is not the public product surface.

That means the implementation plan should assume:

- public behavior can get stronger
- coupling can get deeper
- runtime can get better
- internal support can grow
- hidden substrate details do not need to be exposed in the public docs

This boundary is not cosmetic.

It is part of the architecture discipline.

---

# 🚀 Section 3 · Implementation Tracks

Twin Atlas should now be built across five implementation tracks.

## 1. 📘 Public layer track
Stabilize the public-facing docs, entry pages, and navigation surfaces.

## 2. 🌉 Bridge track
Turn Bridge from specification and examples into more operational handoff behavior.

## 3. ⚙️ Runtime track
Make Basic, Advanced, and Strict behave like real public runtime surfaces rather than static text assets only.

## 4. 🎭 Demo track
Make the demo layer stronger, more legible, and more aligned with implementation targets.

## 5. 🧠 Formalization track
Continue structural rigor and future mathematical packaging without blocking the practical build.

These tracks are connected, but they should not be forced to complete at the same time.

---

# ✅ Section 4 · What is already done

The implementation plan should start from what is already real.

## Already done at the public layer

### Core identity
- `README.md`
- `faq.md`
- `roadmap.md`
- `release-notes.md`

### Bridge
- `Bridge/README.md`
- `Bridge/bridge-v1-spec.md`
- `Bridge/bridge-v1-examples.md`
- `Bridge/bridge-v1-eval-notes.md`
- `Bridge/bridge-implementation-notes.md`

### Demos
- `demos/README.md`
- `demos/killer-demo-spec.md`
- `demos/case-01-thin-evidence-f5-vs-f6.md`
- `demos/baseline-vs-twin-atlas-table.md`
- `demos/evaluator-notes.md`

### Runtime
- `runtime/README.md`
- `runtime/twin-atlas-basic.txt`
- `runtime/twin-atlas-advanced.txt`
- `runtime/twin-atlas-strict.txt`
- `runtime/twin-atlas-coupling-flow.md`

This means the project is already in implementation territory.

The plan now is to converge these into a stronger build.

---

# 🎯 Section 5 · MVP Implementation Goal

The MVP implementation goal should be defined clearly.

It is **not**:

- full theoretical closure
- final production runtime
- total formalization
- universal benchmark proof

The MVP implementation goal **is**:

### A. A coherent public engine surface
A serious reader can understand the engine and navigate it cleanly.

### B. A coherent minimal coupling flow
Forward, Bridge, Inverse, and visible output are connected by a stable implementation logic.

### C. A usable runtime ladder
Basic, Advanced, and Strict can be used as meaningful public runtime surfaces.

### D. A visible proof surface
The demo layer makes the Twin Atlas difference visible and reviewable.

### E. A viable next-step development platform
The docs, specs, demos, and runtime surfaces are strong enough to support actual coupling work.

That is the right MVP bar.

---

# 🗂️ Section 6 · Build Sequence

This is the recommended build order.

## Phase 1 · Public layer stabilization ✅
Goal:
finish the readable public layer and make the engine easy to understand.

Main assets:
- identity docs
- FAQ
- roadmap
- release notes
- navigation
- folder entry pages

Status:
already strong and mostly in place

---

## Phase 2 · Bridge implementation convergence 🟡
Goal:
move Bridge from public design into more operational coupling behavior.

Main work:
- finalize validation logic
- finalize reject logic
- finalize structural normalization posture
- finalize packet shape assumptions
- align Bridge behavior with demos
- define implementation expectations for runtime handoff

Deliverables:
- stronger Bridge implementation notes
- implementation-facing packet rules
- implementation-facing logging and inspection strategy
- demo-aligned Bridge targets

---

## Phase 3 · Runtime alignment 🟡
Goal:
make the runtime surfaces behave like real mode variants rather than just documentation assets.

Main work:
- sharpen the difference between Basic, Advanced, and Strict
- define when each mode should be chosen
- align runtime behavior with coupling flow
- prevent drift between runtime files and actual architecture logic

Deliverables:
- runtime mode notes
- coupling-aware runtime refinement
- stronger runtime usage guidance
- future runtime test surfaces

---

## Phase 4 · Demo-to-implementation locking 🟡
Goal:
treat demo cases as implementation targets.

Main work:
- make sure Case 01 can be supported honestly by the intended flow
- add more demo cases across more family boundaries
- use the evaluator notes as review rules
- keep the comparison surface aligned with actual behavior

Deliverables:
- demo-aligned implementation targets
- more case coverage
- stronger evaluator consistency
- optional public proof pack

---

## Phase 5 · Deeper coupling maturation 🔜
Goal:
tighten how route value, ambiguity, authorization, and visible output strength interact.

Main work:
- define more explicit transition logic
- define stronger downgrade / unresolved behavior
- define stronger candidate-vs-verdict rules
- tighten the relationship between Bridge preservation and inverse-side strength control

Deliverables:
- stronger coupling notes
- stronger operational loop descriptions
- more mature mode behavior
- more reliable implementation targets

---

## Phase 6 · Formalization expansion 🔜
Goal:
push Twin Atlas toward stronger structural rigor without blocking practical progress.

Main work:
- state logic
- visible-state logic
- authorization logic
- repair legality conditions
- stronger coupling laws
- future mathematical packaging preparation

Deliverables:
- formalization notes
- stronger state language
- future mathematical direction surface

This is important, but it should not block the earlier phases.

---

# 🌉 Section 7 · Bridge Implementation Plan

Bridge is the first major implementation-facing layer that needs to tighten.

## Bridge implementation priorities

### Priority 1
Validation discipline

Bridge must reject bad forward packets instead of inventing meaning.

### Priority 2
Structural preservation discipline

Bridge must preserve:
- primary route
- neighboring route
- broken invariant
- first repair as candidate
- misrepair shadow
- evidence weakness
- fit honesty

### Priority 3
Anti-inflation discipline

Bridge must not silently:
- strengthen confidence
- strengthen specificity
- strengthen route finality
- strengthen repair finality

### Priority 4
Inverse necessity discipline

Bridge must still leave real work for the inverse side.

### Priority 5
Inspection discipline

Bridge should later be inspectable enough that reviewers can tell:
- what was preserved
- what was rejected
- whether anything was upgraded illegally

This is where the Bridge track should focus first.

---

# ⚙️ Section 8 · Runtime Implementation Plan

The runtime plan should not try to turn all three runtime files into giant philosophical blocks.

Instead, the goal is to make them behave as three meaningful intensities of the same engine.

## Basic
Goal:
lowest-friction entry form

Focus:
- easy adoption
- visible Twin Atlas flavor
- lower ritual overhead

## Advanced
Goal:
main working mode

Focus:
- stronger route discipline
- stronger ambiguity preservation
- stronger repair discipline
- stronger practical usefulness

## Strict
Goal:
highest-governance public form

Focus:
- strongest evidence-boundary discipline
- strongest anti-fake-closure behavior
- strongest candidate-vs-verdict separation
- strongest tolerance for lawful unresolvedness

Implementation priority here is not to make them different in style only.

Implementation priority is to make them different in **governance intensity**.

That distinction matters.

---

# 🎭 Section 9 · Demo Implementation Plan

The demo layer should now be treated as a serious implementation partner.

## Why
Because demos are not just presentation.

They are the clearest visible targets for whether the engine is behaving correctly.

## Main rule
If the implementation-facing flow cannot support the intended Twin Atlas behavior shown in the demo cases, the implementation is drifting.

## Demo priorities

### Priority 1
Case 01 must remain supportable.

That means:
- F5 remains primary
- F6 remains live
- evidence stays partial
- fit stays family-level
- repair stays candidate-like
- visible output does not overrun support

### Priority 2
Add more family boundary cases.

Recommended directions:
- F3 vs F4
- F1 vs F5
- research interpretation ambiguity
- mixed-route workflow cases

### Priority 3
Keep one-screen legibility.

The more implementation gets deeper, the more important it is to keep visible contrast easy to understand.

---

# 🔗 Section 10 · Runtime and Bridge alignment plan

This is one of the most important near-term tasks.

The runtime layer and Bridge layer must not drift apart.

That means the project should explicitly align these things:

## Runtime should reflect
- route honesty
- ambiguity preservation
- evidence-boundary discipline
- candidate-not-verdict repair posture

## Bridge should preserve
- the exact signals runtime behavior depends on
- without silently strengthening them

## Inverse should still decide
- whether stronger visible force is authorized
- whether stronger repair confidence is lawful
- whether unresolvedness should remain visible

This alignment plan is what turns a docs stack into a stronger engine direction.

---

# 📊 Section 11 · Suggested Milestones

The project should now aim for milestones that are concrete enough to track.

## Milestone A · Public surface complete
Meaning:
the main public pages, Bridge docs, demo docs, runtime docs, FAQ, roadmap, and release notes are stable enough for public reading.

## Milestone B · Bridge implementation-ready
Meaning:
Bridge has enough validation, preservation, reject, and inspection guidance to support implementation work.

## Milestone C · Runtime ladder stable
Meaning:
Basic, Advanced, and Strict behave like distinct and meaningful public runtime forms.

## Milestone D · Demo target alignment
Meaning:
Case 01 and the main comparison surface are clearly supportable by the intended coupling flow.

## Milestone E · Coupling maturation
Meaning:
Forward, Bridge, Inverse, and visible output behave like a cleaner engine loop rather than adjacent design ideas.

## Milestone F · Formalization expansion
Meaning:
the architecture starts receiving stronger state and legality structure without blocking runtime usefulness.

These milestones are easier to build against than vague “future progress.”

---

# 🚫 Section 12 · What should not happen

The project should avoid these implementation mistakes:

## Mistake 1
Trying to fully formalize everything before making the runtime and demos operationally meaningful.

## Mistake 2
Letting Bridge become a secret third judge.

## Mistake 3
Letting runtime files drift into tone variants instead of governance variants.

## Mistake 4
Letting demo pages drift into marketing theater instead of implementation targets.

## Mistake 5
Exposing hidden internal substrate details just because implementation is deepening.

## Mistake 6
Pretending MVP means total engine completion.

These mistakes would weaken the project.

---

# 🧠 Section 13 · Relationship to hidden substrate

The implementation plan should assume something important:

the public effective layer can keep getting stronger **without** exposing the hidden internal substrate.

That means:

- public behavior can mature
- coupling can get deeper
- runtime can get stronger
- demo support can improve
- formalization can progress

while the hidden substrate remains hidden

This is the correct posture for Twin Atlas.

The public engine does not need to spill its internal skeleton in order to become more real.

---

# ✅ Section 14 · What counts as implementation success right now

At the current stage, a good implementation step should count as successful if it does at least one of the following:

- makes Bridge more implementable without making it dirtier
- makes runtime more usable without making it shallower
- makes demos more legible without making them less honest
- makes coupling clearer without overclaiming closure
- makes the project more buildable without exposing hidden substrate details

That is the right success test.

---

# 🧡 Section 15 · A vibe-coder-friendly summary

If you want the fast builder version:

### Right now
The project already looks like a real engine.

### Next
Make Bridge and runtime behave more like the engine they already describe.

### After that
Use demo cases as hard targets and tighten the coupling loop.

### Long-term
Keep deepening the structure, and only then push harder formalization.

That is the build logic.

---

# 🚀 Suggested next read

After this page, the most useful next files are:

1. [Bridge Implementation Notes](./Bridge/bridge-implementation-notes.md)
2. [Twin Atlas Coupling Flow](./runtime/twin-atlas-coupling-flow.md)
3. [Twin Atlas Advanced](./runtime/twin-atlas-advanced.txt)
4. [Twin Atlas Strict](./runtime/twin-atlas-strict.txt)
5. [Case 01 · Thin Evidence F5 vs F6](./demos/case-01-thin-evidence-f5-vs-f6.md)

That sequence moves from implementation plan to coupling logic to public runtime to visible targets.

---

# ✨ One-sentence takeaway

> The implementation plan for Twin Atlas is now simple in principle: stabilize the public engine surface, tighten Bridge and runtime behavior, use demos as implementation targets, and deepen formalization only after the engine loop becomes more operationally real.
