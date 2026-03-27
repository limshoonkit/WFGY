<!--
AI_NOTE_START

Document role:
This page defines how to review, score, and sanity-check Bridge v1 behavior inside WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Explain how to evaluate whether Bridge v1 is behaving correctly.
2. Turn the formal specification into practical review rules.
3. Help developers catch hidden inflation, hidden route erasure, and hidden legality leakage.
4. Provide a repeatable review mindset for Bridge packet quality.

How to use this page:
1. Read this page after Bridge README, Bridge v1 Spec, and Bridge v1 Examples.
2. Use it when reviewing Bridge outputs by hand.
3. Use it when building eval scripts, QA checks, or implementation sanity tests.
4. Treat it as an evaluation and review layer, not as the formal contract itself.

Important boundary:
This page explains how to evaluate Bridge v1 behavior.
It does not replace the formal contract in bridge-v1-spec.md.
It also does not make Bridge a judge.
Bridge remains advisory-only and all packets still require inverse-side recheck.

Recommended reading path:
1. Twin Atlas
2. Bridge README
3. Bridge v1 Spec
4. Bridge v1 Examples
5. This page
6. Killer Demo Spec

AI_NOTE_END
-->

# 🧪 Bridge v1 Eval Notes

> Review rules, sanity checks, and failure signals for the advisory-only coupling layer inside WFGY 4.0 Twin Atlas Engine.

Bridge v1 is easy to misunderstand if people only ask one question:

**"does the packet look neat?"**

That is the wrong question.

The right questions are:

- did Bridge preserve the structural value of the forward packet
- did Bridge avoid hidden inflation
- did Bridge avoid hidden deletion of live ambiguity
- did Bridge avoid acting like a third judge
- did Bridge keep the inverse side necessary

This page exists to make those review rules explicit.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| Bridge Home | [Bridge README](./README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](./bridge-v1-spec.md) |
| Bridge v1 Examples | [Bridge v1 Examples](./bridge-v1-examples.md) |
| Killer Demo Spec | [Killer Demo Spec](../demos/killer-demo-spec.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Inverse Atlas Home | [Inverse Atlas README](../../Inverse_Atlas/README.md) |

---

## 🧭 The shortest evaluation rule

If you only remember one thing, remember this:

**Bridge is good when it carries route value forward honestly, without turning that value into authority.**

That means Bridge should do both of these at the same time:

- preserve forward-side structure
- refuse hidden upgrade

If it fails either side, the handoff is bad.

---

## 🎯 What this page evaluates

This page evaluates Bridge v1 along six core dimensions:

1. **structural preservation**
2. **ambiguity preservation**
3. **confidence discipline**
4. **repair discipline**
5. **fail-closed behavior**
6. **inverse-side dependence**

These six dimensions are enough to catch most real Bridge failures.

---

## 🧱 Core review mindset

When reviewing Bridge, do **not** ask:

- does this packet sound smart
- does this packet sound more resolved
- does this packet sound cleaner than the forward packet

Instead ask:

### 1. Did Bridge preserve the important structure
Examples:
- primary route pressure
- secondary route pressure
- broken invariant candidate
- first repair direction as candidate
- misrepair shadow
- evidence weakness
- fit-level honesty

### 2. Did Bridge avoid illegal upgrade
Examples:
- weak to partial inflation
- partial to sufficient inflation
- family-level to node-level inflation
- candidate to verdict inflation
- plausible route to authorized conclusion inflation

### 3. Did Bridge stay in its own lane
Bridge should not:
- authorize
- classify repair legality
- finalize neighboring-cut separation
- produce final user-facing answer

That is the main review posture.

---

## ✅ The six evaluation dimensions

## 1. Structural preservation 🧩

### What to check
Bridge should preserve the meaningful structure from the forward routing contract.

At minimum, check whether Bridge kept:

- `primary_family`
- `secondary_family` when materially live
- `broken_invariant`
- `first_fix_direction` as candidate
- `misrepair_risk`
- `confidence`
- `evidence_sufficiency`
- `best_current_fit`

### Pass signal
The bridge packet still reflects the same structural situation.

### Fail signal
Bridge produces a packet that feels cleaner, but has silently deleted or weakened important route structure.

### Common failure smell
"looks nicer, but actually lost the hard part"

---

## 2. Ambiguity preservation 🌫️

### What to check
If a neighboring route is still materially live, Bridge must keep it visible.

### Pass signal
The packet preserves competing-route pressure honestly.

### Fail signal
Bridge erases the secondary route for neatness, readability, or fake confidence.

### Common failure smell
"it now sounds decisive, but only because it deleted the second live possibility"

---

## 3. Confidence discipline 📏

### What to check
Bridge must not make the packet sound stronger than the evidence allows.

Check:

- does `route_confidence_hint` match the forward confidence
- does `evidence_hint` match the forward evidence state
- does the wording imply stronger support than the packet contains
- did fit level get upgraded quietly

### Pass signal
Weak stays weak. Partial stays partial. Honest fit level stays honest.

### Fail signal
Any hidden strengthening of confidence, support, or specificity.

### Common failure smell
"same packet, but suddenly it reads like the case is basically solved"

---

## 4. Repair discipline 🛠️

### What to check
Bridge must preserve repair direction as **candidate only**.

Check:

- does the packet keep the repair as a next move
- does it avoid calling the repair structural
- does it keep `misrepair_shadow_seed`
- does it preserve broken-invariant contact logic

### Pass signal
The packet carries repair direction forward without pretending legality has been established.

### Fail signal
Bridge behaves like repair judgment is already done.

### Common failure smell
"the packet turned a suggested first move into a repair verdict"

---

## 5. Fail-closed behavior 🛑

### What to check
Bridge must reject bad forward packets instead of inventing legality.

Review whether Bridge correctly rejects cases where:

- required fields are missing
- confidence exceeds evidence
- fit level is over-specified
- neighboring route is missing even though pressure is live
- misrepair shadow is absent
- translation would require semantic invention

### Pass signal
Bridge emits `bridge_error` and rejects.

### Fail signal
Bridge tries to patch, guess, soften, or creatively rewrite its way past invalid input.

### Common failure smell
"the packet should have been rejected, but Bridge tried to be helpful"

---

## 6. Inverse-side dependence 🔐

### What to check
Bridge must leave the inverse layer necessary.

That means the packet should still require:

- constitution rebuild
- world-legitimacy recheck
- neighboring-cut separation check
- repair-legality check
- public-ceiling clamp

### Pass signal
The packet is useful, but the inverse layer still has real work to do.

### Fail signal
Bridge output already reads like the case is basically decided.

### Common failure smell
"why do we even need the inverse layer now"

---

## 📋 Fast review checklist

Use this checklist when reading any Bridge packet.

### Structural checks
- [ ] Primary route candidate preserved
- [ ] Secondary route candidate preserved when live
- [ ] Broken invariant candidate preserved
- [ ] Fit level preserved honestly
- [ ] Misrepair shadow preserved

### Discipline checks
- [ ] Confidence not inflated
- [ ] Evidence state not inflated
- [ ] Repair remains candidate only
- [ ] No authorization leakage
- [ ] No final-route leakage

### Runtime checks
- [ ] Packet still requires inverse-side recheck
- [ ] No neighboring-cut judgment was finalized by Bridge
- [ ] No repair-legality judgment was finalized by Bridge
- [ ] Reject state used where needed

If any critical box fails, Bridge should not be considered healthy.

---

## 🚨 Common Bridge failure patterns

Below are the most important failure patterns to watch for.

## Failure pattern 1. Hidden confidence inflation
Bridge preserves the same fields, but rewrites them in a way that sounds much stronger.

### Why it matters
This is dangerous because it looks subtle and professional.

### Red flag
The packet "feels more certain" than the forward packet even though no new support exists.

---

## Failure pattern 2. Ambiguity deletion
Bridge removes `secondary_family` or weakens neighboring-route pressure for readability.

### Why it matters
This destroys lawful uncertainty.

### Red flag
The packet is suddenly cleaner than the situation deserves.

---

## Failure pattern 3. Fit-level inflation
Bridge changes family-level reality into node-level flavor.

### Why it matters
This makes the inverse layer start from polluted specificity.

### Red flag
Subtype language appears even though the forward packet stayed coarse.

---

## Failure pattern 4. Repair verdict leakage
Bridge turns `first_fix_direction` into something that sounds like already-approved structural repair.

### Why it matters
This collapses the separation between handoff and legality.

### Red flag
The packet reads like "this is the fix" instead of "this is the next move candidate"

---

## Failure pattern 5. Misrepair shadow loss
Bridge drops or weakens the tempting wrong-first-fix signal.

### Why it matters
This removes one of the most useful caution signals in the entire handoff.

### Red flag
The packet preserves route, but forgets the likely wrong move.

---

## Failure pattern 6. False helpfulness
Bridge sees an incomplete packet and tries to "helpfully" invent missing structure.

### Why it matters
Bridge is not allowed to hallucinate missing legality.

### Red flag
The packet looks coherent even though the source packet was insufficient.

---

## 🧮 Suggested scoring rubric

If you want a fast manual scoring pass, use this 0 to 5 rubric.

| Dimension | 0 | 3 | 5 |
|---|---|---|---|
| Structural preservation | Major structure lost | Mostly preserved with minor issues | Fully preserved honestly |
| Ambiguity preservation | Live ambiguity erased | Partly preserved | Fully preserved when lawful |
| Confidence discipline | Strong inflation present | Slight inflation risk | No inflation |
| Repair discipline | Candidate became verdict | Some blur remains | Candidate stays candidate |
| Fail-closed behavior | Bad packets pass | Mixed behavior | Rejects correctly |
| Inverse dependence | Inverse mostly bypassed | Some overreach | Inverse still clearly necessary |

### Suggested interpretation

- **26 to 30** → healthy Bridge behavior
- **20 to 25** → usable, but review carefully
- **14 to 19** → unstable, likely handoff pollution
- **0 to 13** → Bridge is functionally broken

This rubric is not the contract itself.  
It is a practical review tool.

---

## 🧪 Review workflow for a single packet

Use this review flow when checking a packet manually.

### Step 1
Read the forward packet first.

### Step 2
Underline the non-negotiable structure:
- primary family
- secondary family
- broken invariant
- best current fit
- first fix direction
- misrepair risk
- confidence
- evidence sufficiency

### Step 3
Read the Bridge packet.

### Step 4
Ask four questions in order:

1. what did Bridge preserve
2. what did Bridge compress
3. what did Bridge upgrade, if anything
4. what did Bridge wrongly decide, if anything

### Step 5
If you see upgrade without justification, fail the packet.

### Step 6
If the packet seems to make the inverse layer unnecessary, fail the packet.

That sequence catches most important issues very quickly.

---

## 🔬 Example review notes

Below are short example review comments you can reuse.

### Healthy comment
> Bridge preserved F5 as primary, kept F6 live, retained the broken invariant, preserved the misrepair shadow, and did not upgrade fit level or confidence. Inverse-side recheck remains clearly necessary.

### Inflation comment
> Bridge preserved the route labels but upgraded the tone and specificity. The packet sounds more settled than the forward evidence allows.

### Ambiguity-loss comment
> Bridge deleted the live neighboring route. This makes the packet cleaner, but structurally less honest.

### Repair-leakage comment
> Bridge turned the first repair direction into something that reads like a structural repair verdict. That crosses the handoff boundary.

### Reject-needed comment
> This input should have failed closed. Bridge should reject instead of filling the missing legality gap with a smoother packet.

---

## 🧠 What a great Bridge packet feels like

A great Bridge packet feels like this:

- clearer, but not more inflated
- tighter, but not cleaner than reality
- easier to consume, but not more authorized
- more structured, but not more final

That is the right vibe.

If it feels "suddenly resolved," something probably went wrong.

---

## 🛠️ Recommended test set categories

If you want a practical eval pack, build cases from these categories:

### Category 1
Thin evidence, live ambiguity

### Category 2
High drama wording, weak trace support

### Category 3
Family-level fit only, subtype temptation

### Category 4
Strong wrong-first-fix temptation

### Category 5
Missing secondary family under live pressure

### Category 6
Confidence stronger than evidence

### Category 7
Incomplete packet, reject expected

These categories are enough to stress most important Bridge behaviors.

---

## 📌 Minimal pass criteria for Bridge v1

Bridge v1 should not be considered release-healthy unless all of the following are true:

- it preserves structurally important forward signals
- it preserves ambiguity when ambiguity is still lawful
- it does not inflate confidence or specificity
- it keeps repair as candidate, not verdict
- it rejects bad packets instead of inventing legality
- it still leaves meaningful work for the inverse layer

That is the minimum bar.

---

## 🚀 Suggested next read

After this page, the best next file is:

[Bridge v1 Examples](./bridge-v1-examples.md)

Why:

- examples show what healthy packets look like
- this page shows how to judge whether those packets are actually healthy

Together, they make the Bridge folder much more actionable.

---

## ✨ One-sentence takeaway

> A good Bridge packet is not the one that sounds the smartest, it is the one that preserves the most structure while pretending to know the least beyond what the forward packet has actually earned.
