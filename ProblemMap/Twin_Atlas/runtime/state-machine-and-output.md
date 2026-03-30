<!--
AI_NOTE_START

Document role:
This page explains the operational state model and final output structure of WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Show how Twin Atlas moves from architecture into actual runtime behavior.
2. Explain the different state planes inside the engine.
3. Clarify how legal transitions, downgrade logic, and final output structure work together.
4. Help new readers understand why the final output contract is part of the engine, not decoration.

What this page is not:
1. It is not the flagship landing page.
2. It is not the route-first routing page.
3. It is not the full hidden substrate.
4. It is not a benchmark page.
5. It is not proof that every future runtime branch is already complete.

Reading order:
1. Read the Twin Atlas README first.
2. Read the Runtime README second.
3. Read the Runtime Constitution and Inverse Governance Contract before this page if possible.
4. Read this page when you want to understand how Twin Atlas actually behaves as a governed runtime.

Important boundary:
This page presents the public state logic and output discipline of Twin Atlas.
It does not claim that every future extension, every downstream operating environment, or every hidden internal detail is already fully finalized here.

AI_NOTE_END
-->

# ⚙️ State Machine and Output

> Twin Atlas is not just a set of ideas. It is a governed runtime with distinct state planes, legal transitions, and a final output contract.

A lot of systems talk about reasoning as if it were one big invisible blob.

Twin Atlas does not do that.

WFGY 4.0 separates runtime behavior into different state planes because several things that often get mixed together are **not** the same thing:

- finding a route
- authorizing an answer
- judging repair legality
- shaping final output

If those planes collapse into one, the engine starts lying without noticing.

That is why this page matters.

---

## 🌍 Why the state model matters

Twin Atlas is built to stop a very common AI failure pattern:

the model finds something plausible,  
then treats that plausibility like permission,  
then turns that permission into a stronger answer than the evidence has actually earned.

That chain usually feels smooth.  
But smoothness is exactly why it is dangerous.

The state model exists to break that chain into inspectable pieces.

This lets the engine ask:

- how strong is the current route?
- how strong is the current authorization?
- how strong is the repair claim?
- how strong is the final visible output allowed to be?

Those are different questions.  
Twin Atlas treats them as different state planes.

---

## 🧩 The four state planes

Twin Atlas uses four main planes.

### 🗺️ 1. Route-Fit Plane
This plane describes how strong the current structural route is.

This is the part that answers:

**How far has the engine honestly earned its route interpretation?**

It does **not** automatically decide whether the system is allowed to release that interpretation strongly.

### ⚖️ 2. Authorization Plane
This plane describes how much visible output is currently lawful.

This is the part that answers:

**How strongly is the engine allowed to speak right now?**

It depends on more than route quality.  
It also depends on evidence, competing routes, legality, and ceiling.

### 🛠️ 3. Repair-Legality Plane
This plane describes what kind of repair language is currently lawful.

This is the part that answers:

**Is this repair only a candidate, only cosmetic, or actually structural?**

This is critical because a system can sound useful while still faking repair depth.

### 🧠 4. Hidden Decision-Posture Plane
This plane describes the engine’s internal convergence posture.

It helps the system decide whether it is:
- aiming toward a best unique answer
- leaning toward the most reasonable current answer
- or preserving open-result structure

This plane matters internally, but it must **not** be confused with public authorization.

That distinction is one of the core protections of Twin Atlas.

---

## 🗺️ Route-Fit Plane

The route-fit plane is the public runtime expression of the route-first side.

Its job is to answer:

**How far has the engine honestly earned the route itself?**

Twin Atlas uses these route-fit states:

### ⬛ ROUTE_NO_FIT
Use this when no honest family-level fit is defensible.

This is not a panic state.  
It is the correct state when forcing a route would create fake structure.

### 🟦 ROUTE_FAMILY_LEVEL
Use this when one family is stronger than the others, but narrower precision is not yet honest.

This is often the healthiest state under partial evidence.

### 🟨 ROUTE_UNRESOLVED_SUBTYPE
Use this when the broader family is stable enough, but subtype pressure is still unresolved.

This protects the system from premature precision.

### 🟩 ROUTE_NODE_LEVEL
Use this only when the narrower route has genuinely been earned.

A node-level route is stronger than family-level fit, but it is still **not** authorization by itself.

That last point matters a lot.

---

## ⚖️ Authorization Plane

The authorization plane is the public runtime expression of the legitimacy-first side.

Its job is to answer:

**How strong is the visible answer allowed to be right now?**

Twin Atlas uses four public authorization states.

### 🟥 MODE_STOP
The engine must stop.

Use this when:
- the problem frame is not stable enough
- world alignment is too weak
- route opacity is too high
- contamination is still active
- any useful visible answer would already exceed the ceiling

STOP is not a failure to be ashamed of.  
It is lawful success when stronger output would be illegal.

### 🟧 MODE_COARSE
The engine may speak, but only broadly.

Use this when:
- the route is only stable at a broad level
- neighboring pressure is still active
- detail would overreach
- finer output would become fake precision

### 🟨 MODE_UNRESOLVED
The engine has a leading route, but a competing route is still materially alive.

This is one of the most important states in Twin Atlas, because it protects the engine from fake singular closure.

### 🟩 MODE_AUTHORIZED
The engine has earned the right to speak more strongly.

Use this only when:
- the problem frame is stable enough
- the route is strong enough
- neighboring cuts are sufficiently separated
- the answer stays below the current ceiling

AUTHORIZED is not permission for dramatic certainty.  
It is simply the strongest lawful public state currently available.

---

## 🛠️ Repair-Legality Plane

Repair language is dangerous because it often feels more useful than it really is.

That is why Twin Atlas gives repair its own plane.

### ⬜ REPAIR_NONE
No repair claim is yet lawful or meaningful.

### 🟨 REPAIR_TENTATIVE
A repair direction exists, but it is still only a candidate.

This is the healthy state when:
- route pressure is still active
- evidence is still incomplete
- legality is not fully earned

### 🟦 REPAIR_COSMETIC_ONLY
The proposed change may improve wording, formatting, structure, or clarity, but it does not touch the structural failure condition.

This state is extremely important because a lot of fake “repair” is actually cosmetic.

### 🟩 REPAIR_STRUCTURAL
The proposal actually reaches the broken invariant, survives legality review, and plausibly reduces recurrence risk.

This is the strongest repair state, and it must be earned.

Twin Atlas refuses to let “helpful sounding” repair automatically become structural repair.

---

## 🧠 Hidden Decision-Posture Plane

Twin Atlas also has an internal convergence posture plane.

This plane is useful because not every runtime moment behaves the same way internally.

The system may be leaning toward:

### 🟢 DECISION_M1
Best unique convergence target

### 🟡 DECISION_M2
Most reasonable current convergence target

### 🔵 DECISION_M3
Open-result structure remains safer than premature convergence

This plane is useful internally.

But it must never be confused with public state.

That means:

- M1 is not the same thing as AUTHORIZED
- M2 is not the same thing as COARSE
- M3 is not the same thing as STOP

If those collapse into each other, Twin Atlas stops being honest.

---

## 🔄 Legal transitions

Twin Atlas is not only about choosing states.  
It is also about moving between them honestly.

### Upward transitions
Upward transitions happen only when support genuinely improves.

Examples include:

- ROUTE_NO_FIT -> ROUTE_FAMILY_LEVEL
- ROUTE_FAMILY_LEVEL -> ROUTE_UNRESOLVED_SUBTYPE
- ROUTE_UNRESOLVED_SUBTYPE -> ROUTE_NODE_LEVEL

- MODE_STOP -> MODE_COARSE
- MODE_COARSE -> MODE_UNRESOLVED
- MODE_UNRESOLVED -> MODE_AUTHORIZED

- REPAIR_NONE -> REPAIR_TENTATIVE
- REPAIR_TENTATIVE -> REPAIR_STRUCTURAL

The rule is simple:

**upgrade only when support upgrades first**

Not because the user wants it.  
Not because the answer sounds clean.  
Not because the runtime is tired of uncertainty.

### Downward transitions
Downward transitions happen when support weakens, competing pressure rises, legality deteriorates, or ceiling pressure becomes stronger.

Examples include:

- ROUTE_NODE_LEVEL -> ROUTE_UNRESOLVED_SUBTYPE
- ROUTE_UNRESOLVED_SUBTYPE -> ROUTE_FAMILY_LEVEL
- ROUTE_FAMILY_LEVEL -> ROUTE_NO_FIT

- MODE_AUTHORIZED -> MODE_UNRESOLVED
- MODE_UNRESOLVED -> MODE_COARSE
- MODE_COARSE -> MODE_STOP

- REPAIR_STRUCTURAL -> REPAIR_TENTATIVE
- REPAIR_TENTATIVE -> REPAIR_COSMETIC_ONLY
- REPAIR_COSMETIC_ONLY -> REPAIR_NONE

Twin Atlas must be willing to downgrade.

That willingness is part of what makes it governed.

---

## 🔻 Forced downgrade and restart

Downgrade is not optional when the state weakens.

A healthy Twin Atlas runtime must be able to say:

- “this route is less secure than it looked”
- “that competing route is still alive”
- “repair language needs to be downgraded”
- “the visible answer is drifting above the ceiling”
- “the local state is contaminated enough that restart is cleaner than pretending”

That is why restart exists.

Restart is not failure theater.  
Restart is structural hygiene.

Twin Atlas would rather restart than fake completion.

---

## 📦 The final output contract

One of the most important parts of Twin Atlas is that the final visible output is not just “whatever the model feels like saying.”

It is governed by a public contract.

That contract should preserve things like:

- `state_code`
- `problem_frame`
- `forward_route`
- `world_alignment`
- `route_judgment`
- `neighboring_cut_status`
- `resolution_status`
- `repair_status`
- `answer_payload`

This matters because Twin Atlas should show two things at once:

### 1. What the engine is structurally seeing
### 2. What the engine is lawfully allowed to say

Without that distinction, the whole system becomes blurry again.

---

## 🚫 What this page is protecting against

This page exists to defend against several major collapse patterns.

### 1. Route-fit into authorization collapse
A stronger route is not automatically stronger permission.

### 2. Confidence into legitimacy collapse
A more confident answer is not automatically a more lawful answer.

### 3. Candidate repair into structural repair collapse
A useful-sounding fix is not automatically structural.

### 4. Ambiguity into neatness collapse
A live competing route must not disappear just because neatness feels better.

### 5. Hidden posture into public mode collapse
Internal convergence posture must not silently become public authorization.

### 6. Final shaping into silent upgrade collapse
Readable output must not become stronger than what the state actually allows.

This is why the state machine matters.  
It is not paperwork.  
It is anti-self-deception infrastructure.

---

## ✅ What is already fair to say

At the current stage, these claims are fair:

- Twin Atlas already has a real public state model
- route-fit, authorization, repair legality, and final output are already treated as distinct governed surfaces
- legal transition logic already belongs to the public runtime story
- the final output contract is already a core part of WFGY 4.0, not decoration
- this state logic is already one of the clearest reasons Twin Atlas feels like an engine rather than a prompt

These are strong claims.

They are also disciplined claims.

---

## 🚧 What should not yet be claimed

This page should not be used to claim that:

- every future transition rule is already frozen
- every domain-specific output policy is already fully finalized
- every future runtime extension is already complete
- every hidden internal state is already publicly exposed
- the public state model alone proves universal production completion

This page makes the runtime legible.

It does not need to pretend the universe is already closed.

---

## ✨ One-sentence takeaway

> Twin Atlas uses distinct state planes, legal transitions, and a final output contract so that route, authorization, repair, and release strength do not collapse into one vague “reasoning” blur.

---

## 🧭 Final note

A lot of systems can generate answers.

Much rarer are systems that can show:

- how strong the route is
- how strong the authorization is
- how strong the repair claim is
- how much visible output is currently lawful

That is what this page is trying to make visible.

It is one of the clearest places where WFGY 4.0 stops looking like a strong idea and starts looking like a governed runtime.

---

## 🔗 Quick Links

### 🏠 Main entry
- [Twin Atlas README](../README.md)

### ⚙️ Runtime surfaces
- [Runtime README](./README.md)
- [Twin Atlas Runtime Constitution](./twin-atlas-runtime-constitution.md)
- [Inverse Governance Contract](./inverse-governance-contract.md)
- [Seal and Audit](./seal-and-audit.md)

### 🌉 Bridge surfaces
- [Bridge README](../Bridge/README.md)
- [Why Bridge Exists](../Bridge/why-bridge-exists.md)
- [Bridge v1 Contract](../Bridge/twin-atlas-bridge-v1.md)

### 🧭 Family surfaces
- [Troubleshooting Atlas / Forward Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md)
- [Inverse Atlas README](../../Inverse_Atlas/README.md)
- [Status and Boundaries](../status-and-boundaries.md)

### 🧪 Evidence surfaces
- [Evidence Hub](../evidence/README.md)
- [Results Summary](../evidence/results-summary.md)

### 🗺️ Next recommended page
- [Seal and Audit](./seal-and-audit.md)
