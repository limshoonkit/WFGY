<!--
AI_NOTE_START

Document role:
This page defines the minimal coupling flow for WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Show how Forward Atlas, Bridge, and Inverse Atlas should connect in sequence.
2. Make the minimal public effective-layer flow legible before full implementation is complete.
3. Provide a shared reference for runtime design, Bridge implementation, demo alignment, and future coupling work.
4. Clarify where structure is produced, where it is translated, where authorization is checked, and where visible output is clamped.

How to use this page:
1. Read this page after the Twin Atlas README and Bridge implementation notes.
2. Use it as the main coupling overview before writing implementation-facing logic.
3. Use it to align runtime behavior, Bridge behavior, and demo expectations.
4. Treat it as the minimal coupling design surface, not as proof that every future runtime detail is already fully complete.

Important boundary:
This page describes the public effective-layer coupling flow only.
It does not expose hidden internal reasoning substrate details.
It also does not claim that every future closed-loop runtime detail is already fully implemented.
This page defines the minimum disciplined flow that Twin Atlas is trying to preserve.

Recommended reading path:
1. Twin Atlas README
2. Bridge README
3. Bridge v1 Spec
4. Bridge Implementation Notes
5. Runtime README
6. This page
7. Demo cases

AI_NOTE_END
-->

# 🔗 Twin Atlas Coupling Flow

> The minimal public effective-layer coupling flow for WFGY 4.0 Twin Atlas Engine.

This page exists to answer one practical question:

**how do the major Twin Atlas layers actually connect?**

Not at the branding level.  
Not at the philosophy level.  
At the flow level.

Twin Atlas only becomes a real engine if these four things connect cleanly:

1. route-first structural mapping  
2. advisory-only handoff  
3. legitimacy-first authorization  
4. visible answer discipline

That is the coupling flow.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| FAQ | [FAQ](../faq.md) |
| Roadmap | [Roadmap](../roadmap.md) |
| Release Notes | [Release Notes](../release-notes.md) |
| Bridge Home | [Bridge README](../Bridge/README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](../Bridge/bridge-v1-spec.md) |
| Bridge Examples | [Bridge v1 Examples](../Bridge/bridge-v1-examples.md) |
| Bridge Eval Notes | [Bridge v1 Eval Notes](../Bridge/bridge-v1-eval-notes.md) |
| Bridge Implementation Notes | [Bridge Implementation Notes](../Bridge/bridge-implementation-notes.md) |
| Demos Home | [Demos README](../demos/README.md) |
| Killer Demo Spec | [Killer Demo Spec](../demos/killer-demo-spec.md) |
| Case 01 | [Case 01 · Thin Evidence F5 vs F6](../demos/case-01-thin-evidence-f5-vs-f6.md) |
| Runtime Home | [Runtime README](./README.md) |
| Basic Runtime | [Twin Atlas Basic](./twin-atlas-basic.txt) |
| Advanced Runtime | [Twin Atlas Advanced](./twin-atlas-advanced.txt) |
| Strict Runtime | [Twin Atlas Strict](./twin-atlas-strict.txt) |

---

## ⚡ The shortest version

If you only remember one thing, remember this:

**Forward Atlas decides what currently looks strongest.  
Bridge carries that forward without pretending it is already final.  
Inverse Atlas decides what is actually authorized.  
The visible answer must stay below what that authorization has earned.**

That is the minimal Twin Atlas flow.

---

# 🧭 Section 1 · Why a coupling flow is needed

Twin Atlas already has strong parts:

- Forward Atlas improves the first structural cut
- Bridge preserves route value as weak priors
- Inverse Atlas governs whether strong output is lawful

But without a clear coupling flow, those strengths can still drift apart.

Typical failure modes without a disciplined flow:

- the forward side becomes a beautiful but isolated classifier
- Bridge becomes a decorative middle layer
- the inverse side feels disconnected from route reality
- the visible answer quietly spends certainty too early
- the next move becomes stronger than the structure has earned

So this page exists to define the minimum sequence that keeps the architecture honest.

---

# 🧱 Section 2 · Minimal coupling flow

The minimal Twin Atlas coupling flow should be understood as:

```text
case intake
-> forward route construction
-> bridge validation and translation
-> inverse authorization and legality recheck
-> visible output clamping
-> public answer
````

This is the smallest clean version of the engine loop.

It is enough to define:

* where structure is created
* where structure is preserved
* where strength is checked
* where visible output is constrained

That makes it the correct MVP coupling flow.

---

# 🗺️ Section 3 · Stage-by-stage flow

## Stage 0 · Case intake 📥

This is the incoming task surface.

Typical inputs include:

* debugging reports
* workflow failure descriptions
* RAG mismatch cases
* reasoning problems
* research interpretation questions
* ambiguity-heavy analysis requests

The intake stage is not where authorization happens.

It is where the case becomes available for structural reading.

### Output of Stage 0

A case object or case surface ready for forward-side analysis.

### What this stage should not do

* it should not finalize route truth
* it should not authorize visible detail
* it should not jump directly to repair verdicts

---

## Stage 1 · Forward route construction 🗺️

This is the Forward Atlas stage.

Its job is to produce the strongest honest structural cut available from the current evidence.

It should answer questions like:

* what is the primary family
* what is the nearest competing family
* why does the primary currently win
* what is the likely broken invariant
* what is the honest best current fit
* what is the safest useful first move
* what is the main misrepair risk
* how strong is confidence relative to evidence

### Output of Stage 1

A canonical forward routing contract.

Typical fields:

```yaml
primary_family
secondary_family
why_primary_not_secondary
broken_invariant
best_current_fit
first_fix_direction
misrepair_risk
confidence
evidence_sufficiency
need_more_evidence
overlay
```

### What this stage should do well

* make an honest route cut
* preserve live neighboring pressure
* stay coarse when coarse is lawful
* avoid fake subtype precision
* tie the first move to the likely broken invariant

### What this stage should not do

* authorize stronger visible output
* treat a route prior as final truth
* turn first repair direction into repair legality
* act as if route quality alone is enough

---

## Stage 2 · Bridge validation and translation 🌉

This is the Bridge stage.

Its job is to transform the forward routing contract into a normalized weak-prior packet.

It must preserve structure while refusing hidden upgrade.

### Bridge must do

* validate required fields
* reject illegal inflation
* preserve primary route
* preserve neighboring route when live
* preserve broken invariant
* preserve first repair as candidate
* preserve misrepair shadow
* preserve confidence and evidence state honestly
* attach explicit advisory-only constraints

### Bridge must not do

* authorize stronger visible output
* finalize route truth
* finalize neighboring-cut separation
* finalize repair legality
* invent missing structure
* silently upgrade confidence or fit
* erase live ambiguity for neatness

### Output of Stage 2

A Bridge v1 weak-prior packet.

Typical shape:

```yaml
bridge_packet_version: v1

packet_status:
  state: ok

route_hint:
  primary_route_candidate: ...
  neighboring_route_hint: ...
  route_basis_hint: ...
  fit_level_hint: ...

repair_hint:
  broken_invariant_candidate: ...
  first_repair_candidate: ...
  misrepair_shadow_seed: ...

confidence_hint:
  route_confidence_hint: ...
  evidence_hint: ...

evidence_gap:
  need_more_evidence_hint: ...

overlay_hint:
  overlay_signal: ...

constraints:
  advisory_only: true
  authorization_granted: false
  requires_inverse_recheck: true
```

### Failure path

If validation fails, Bridge should emit `bridge_error` and return upstream or stop the packet from continuing.

That is fail-closed behavior, not failure of the architecture.

---

## Stage 3 · Inverse authorization and legality recheck 🔐

This is the Inverse Atlas stage.

It must treat the Bridge packet as **weak prior only**.

That means the inverse side must still do real work.

It should re-evaluate:

* problem constitution
* world legitimacy
* route legitimacy
* neighboring-cut separation
* repair legality
* visible-output ceiling

### Questions this stage should ask

* is the current route strong enough to support stronger visible commitment
* is the neighboring route still materially live
* is the current fit level strong enough to authorize subtype language
* is the proposed repair actually lawful and structurally grounded
* is the visible answer about to outrun the support state

### Output of Stage 3

An authorization-aware state.

This does not need to be exposed with identical formatting every time, but conceptually it should land in a state like:

* coarse
* unresolved
* route-leading but contested
* stronger visible answer tentatively supportable
* stronger visible answer blocked
* repair candidate only
* repair legality not yet established

### What this stage must not do

* blindly inherit the forward route as final truth
* blindly inherit Bridge packet phrasing as authorization
* allow the visible answer to exceed support
* let clean wording simulate earned structure

---

## Stage 4 · Visible output clamping 📏

This is the answer-strength control stage.

The visible answer must be clamped below what the current support has lawfully earned.

This stage is extremely important.

A system can appear careful and still fail here.

### This stage should control

* specificity
* confidence tone
* subtype naming
* repair finality
* closure style

### Good outcomes

* coarse but useful
* route-leading with live ambiguity preserved
* next move available before stronger closure
* evidence-demand before escalation
* candidate repair only

### Bad outcomes

* fake closure
* polished but unauthorized specificity
* strong repair verdict without legality
* dramatic confidence purchased by ambiguity deletion

### Output of Stage 4

The final public answer shape.

This is where the architecture becomes human-visible.

---

## Stage 5 · Public answer 🧾

This is the final visible layer.

The answer should now be:

* route-aware
* authorization-aware
* ambiguity-aware
* repair-disciplined
* practically useful

The final public answer does not need to show every internal stage.

But it should clearly reflect the flow.

That means a healthy answer often includes some version of:

1. what currently looks strongest
2. what is still materially live
3. what is likely broken
4. what the next move should be
5. why stronger closure is or is not authorized yet

That is the public effective-layer expression of the Twin Atlas flow.

---

# 🌫️ Section 4 · Core preservation laws across the flow

A healthy Twin Atlas coupling flow must preserve these laws across all stages.

## Law 1 · Route honesty

The strongest current route should be identified honestly.

## Law 2 · Neighbor preservation

A live competing route should not be erased for neatness.

## Law 3 · Broken-invariant continuity

The likely broken invariant should remain visible from route construction through action guidance.

## Law 4 · Candidate-not-verdict

Repair should remain candidate-like until stronger legality is earned.

## Law 5 · Support-bounded strength

Visible answer strength must remain bounded by support.

## Law 6 · Inverse necessity

Bridge must not make the inverse layer redundant.

These are the coupling laws that matter most.

---

# 🛑 Section 5 · Main ways the flow can break

The coupling flow can fail in several common ways.

## Failure 1 · Forward overreach

The forward side starts acting like authorization has already happened.

### Symptom

Subtype naming or repair finality appears too early.

---

## Failure 2 · Bridge inflation

Bridge preserves the packet but quietly upgrades tone, fit, or certainty.

### Symptom

The packet becomes cleaner than reality.

---

## Failure 3 · Bridge ambiguity deletion

Bridge removes neighboring-route pressure for readability.

### Symptom

A materially live competing route disappears.

---

## Failure 4 · Inverse pass-through

The inverse side stops rechecking seriously and just accepts the packet as truth.

### Symptom

Bridge begins to behave like the real judge.

---

## Failure 5 · Visible output overrun

The final public answer sounds more final than the support state allows.

### Symptom

The answer feels smooth, but structurally illegal.

These are the main failure classes the coupling flow must resist.

---

# 📊 Section 6 · Minimal implementation-facing flow rules

If someone is implementing the flow, the minimum rule set should look like this:

## Forward

* produce honest route contract
* preserve live competing route
* preserve broken invariant
* preserve misrepair risk
* do not overclaim fit

## Bridge

* validate
* reject if structurally unsafe
* normalize without mutation
* preserve route pressure
* preserve repair candidacy
* preserve evidence boundaries
* pass forward as weak priors only

## Inverse

* recheck from scratch
* preserve or revise route legitimacy
* preserve or revise ambiguity
* test repair legality
* determine visible answer ceiling

## Visible output

* do not outrun support
* do not fake finality
* do not convert candidate into verdict
* remain practically useful

That is enough to define a healthy MVP loop.

---

# 🎭 Section 7 · Demo alignment

This coupling flow is not only for architecture pages.

It should be visibly testable in the demo layer.

For the main MVP case, the flow should preserve behavior like this:

## Case 01 target

* Forward keeps F5 primary
* Forward keeps F6 live
* Bridge preserves F5/F6 structure
* Bridge preserves visibility-first first move as candidate
* Inverse refuses stronger boundary-style closure
* Visible answer remains coarse or route-leading rather than prematurely final

If the implementation-facing flow cannot support that pattern, the flow is not healthy yet.

The demos are not decoration.

They are coupling targets.

---

# ⚙️ Section 8 · Relationship to runtime variants

The same coupling flow should underlie all three runtime variants.

What changes is not the existence of the flow.

What changes is how hard each runtime form pushes it.

## Basic

* lighter route preservation
* lighter authorization pressure
* lower-friction public use

## Advanced

* stronger route discipline
* stronger ambiguity preservation
* stronger repair discipline

## Strict

* strongest support-boundary discipline
* strongest anti-fake-closure behavior
* strongest candidate-vs-verdict discipline
* strongest tolerance for unresolved lawful states

That means the runtime ladder is not three different engines.

It is three different intensities of the same flow.

---

# 🧠 Section 9 · What this flow is not

To keep the project honest, this flow should not be misunderstood as:

* the hidden internal reasoning substrate itself
* the final production loop in every technical detail
* a proof that all future coupling problems are already solved
* a guarantee that every runtime implementation will automatically stay clean
* a replacement for the formal Bridge or Inverse docs

This page defines the minimum disciplined flow.

It is not the total endpoint.

---

# ✅ Section 10 · Minimal success criteria

A Twin Atlas coupling flow should count as healthy if all of the following are true:

* Forward creates an honest route contract
* Bridge validates and preserves structure
* Bridge does not inflate or over-decide
* Inverse remains fully necessary
* visible output stays below unauthorized strength
* ambiguity is preserved when still lawful
* repair remains candidate-like unless stronger legality is earned
* demo targets remain supportable

That is enough for a meaningful first coupling milestone.

---

# 🚧 Section 11 · What comes next after this page

After the coupling flow is defined, the next meaningful work is:

## 1. Runtime alignment

Make sure the public runtime variants actually reflect this flow.

## 2. Bridge implementation tightening

Move Bridge from design notes into more operational behavior.

## 3. Demo enforcement

Use demo cases as real implementation targets.

## 4. Future state formalization

Define stricter state and transition language where useful.

That is the natural sequence.

Do not reverse it.

---

# 🧡 Section 12 · A vibe-coder-friendly mental model

If you want the fast builder version, think of the flow like this:

### Forward

“what currently looks strongest”

### Bridge

“carry that carefully without pretending it is already truth”

### Inverse

“has this really earned stronger visible force yet”

### Output

“only say what the structure has actually earned”

That is the Twin Atlas coupling flow in human language.

---

# 🚀 Suggested next read

After this page, the best next files are:

1. [Bridge Implementation Notes](../Bridge/bridge-implementation-notes.md)
2. [Twin Atlas Advanced Runtime](./twin-atlas-advanced.txt)
3. [Twin Atlas Strict Runtime](./twin-atlas-strict.txt)
4. [Case 01 · Thin Evidence F5 vs F6](../demos/case-01-thin-evidence-f5-vs-f6.md)

That sequence moves from coupling design to runtime behavior to proof surface.

---

# ✨ One-sentence takeaway

> Twin Atlas becomes a real engine when route construction, advisory handoff, authorization recheck, and visible answer clamping are connected as one disciplined flow instead of four isolated ideas.

