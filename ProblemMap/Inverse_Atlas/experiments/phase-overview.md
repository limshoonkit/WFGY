<!--
AI_NOTE_START

Document role:
This page explains how the current Inverse Atlas MVP experiments are organized into phases and comparison groups.

What this page is for:
1. Explain the current experiment phase structure.
2. Explain the difference between Smoke, Core Stress, and Long-Context phases.
3. Explain the comparison groups used in the MVP stage.
4. Clarify what this phase structure is meant to test and what it is not yet meant to prove.

How to use this page:
1. Read this page after the experiments entry page.
2. Use this page when you want the cleanest overview of the current experiment design.
3. Use this page before reading any later results page or Colab page.
4. Treat this page as the current experiment-structure reference for the Inverse Atlas MVP.

Important boundary:
This page describes the current MVP experiment structure.
It should not be used to claim that the full benchmark program is already complete.
It should also not be used to claim that every phase has already been run at full scale unless later results pages explicitly support that claim.

Recommended reading path:
1. Inverse Atlas README
2. Versions
3. Quick Start
4. Experiments README
5. Repro in 60 Seconds
6. Phase Overview
7. Results and Current Findings

AI_NOTE_END
-->

# Phase Overview · Experiment Structure and Comparison Groups

> How the current Inverse Atlas MVP experiments are organized

This page explains the current phase structure of the Inverse Atlas experiments layer.

The goal of this structure is simple:

- start with a fast reality check
- move into harder stress cases
- then test whether the system stays lawful across longer multi-turn contexts

So the current design is not random.

It is intentionally layered.

The present MVP experiment structure has three main phases:

- **Smoke Phase**
- **Core Stress Phase**
- **Long-Context Phase**

It also uses comparison groups that help separate baseline behavior from inverse-governed behavior, and later from dual-layer behavior.

---

## Quick Links

| Section | Link |
|---|---|
| Inverse Atlas Home | [Inverse Atlas README](../README.md) |
| Versions | [Versions](../versions.md) |
| Quick Start | [Quick Start](../quickstart.md) |
| Experiments Home | [Experiments](./README.md) |
| Repro in 60 Seconds | [Repro in 60 Seconds](./repro-60-seconds.md) |
| Runtime Guide | [Runtime Guide](../runtime-guide.md) |
| Status and Boundaries | [Status and Boundaries](../status-and-boundaries.md) |
| Twin Atlas | [Twin Atlas](../../Twin_Atlas/README.md) |

---

## The shortest version

If you only want the fast summary, it is this:

### Smoke Phase
Checks whether the MVP is visibly alive.

### Core Stress Phase
Checks whether the legality layer still helps when the cases get harder.

### Long-Context Phase
Checks whether the system can stay lawful across multi-turn contamination and drift.

And the current comparison groups are:

- **A** = baseline
- **B** = inverse only
- **D** = forward plus inverse

That is the core structure.

---

## Why the experiments are split into phases

The phases exist because not all failures appear at the same difficulty level.

Some failures show up immediately in a short comparison.

Some only become clear when:

- ambiguity increases
- route competition becomes sharper
- fake repair becomes tempting
- context grows longer
- early weak assumptions start contaminating later reasoning

If everything is mixed into one giant bucket, it becomes harder to tell what the framework is already doing well and what still needs work.

So the phase structure is meant to answer three different questions in order:

1. **Is the MVP visibly doing anything real yet**
2. **Does it still help when pressure gets harder**
3. **Can it remain lawful across longer context chains**

---

## Smoke Phase

### Current size
**8 cases**

### Main purpose
Smoke Phase is the first standing check of the product line.

It exists to answer a simple but very important question:

**does the current MVP already behave differently enough to be worth testing seriously**

This phase is intentionally small.

It is not supposed to prove everything.
It is supposed to confirm that the artifact layer is already alive enough to show visible contrast.

### What Smoke Phase is good for
Smoke Phase is especially useful for:

- first dry runs
- quick product sanity checks
- visible baseline vs inverse contrast
- public demo selection
- catching obvious failure patterns fast

### What Smoke Phase is not for
Smoke Phase is not a finished benchmark.
It is not the final empirical story.
It is the first gate.

### Typical things to watch for
In Smoke Phase, you mainly watch for whether the inverse-governed pass already reduces:

- early over-resolution
- fake certainty
- false completion
- cosmetic repair inflation
- obvious public overclaim

If you cannot see a difference here, the MVP probably needs more work before harder testing.

---

## Core Stress Phase

### Current size
**32 cases**

### Main purpose
Core Stress Phase is where the framework gets pushed into more contested territory.

This phase matters because many interesting failures do not appear in easy prompts.

They appear when the model is forced into situations involving:

- route contestability
- weak evidence
- dangerous confidence
- repair temptation
- illegal specificity pressure
- structure that looks “almost settled” but is not

### What Core Stress Phase is good for
This phase is the main middle layer of the MVP experiments structure.

It is useful for:

- testing legality discipline under stronger pressure
- comparing baseline vs inverse on more serious cases
- selecting representative showcase examples
- seeing whether the inverse layer is only helpful in easy cases or still useful in hard ones

### What Core Stress Phase is not for
It is still not the same thing as a final full-scale benchmark suite.

It is a larger and more meaningful stress layer, but still part of the MVP stage.

### Typical things to watch for
In Core Stress Phase, you care more about:

- neighboring-route honesty
- refusal of illegal detail escalation
- downgrade into COARSE or UNRESOLVED when needed
- better distinction between structural repair and cosmetic repair
- stronger control of visible confidence ceiling

This phase is where the legality logic should start showing real teeth.

---

## Long-Context Phase

### Current size
**12 multi-turn cases**

### Main purpose
Long-Context Phase exists because some of the most expensive failures are not single-turn failures.

They emerge when:

- earlier weak assumptions linger
- provisional claims start behaving like settled facts
- contamination grows across turns
- the model forgets that prior steps were only tentative
- false completion becomes stronger over time

### What Long-Context Phase is good for
This phase is useful for:

- testing contamination resistance
- testing multi-turn legality discipline
- seeing whether provisional uncertainty is preserved
- observing whether early weak claims get silently upgraded into later false certainty

### What Long-Context Phase is not for
It is not just “more tokens.”
It is a structurally different pressure field.

That is why it deserves its own phase rather than being mixed into the same bucket as short-case stress tests.

### Typical things to watch for
In Long-Context Phase, you care about:

- context drift
- contamination
- false memory of prior certainty
- late-stage overclaim
- unresolved structure pretending to be resolved due to repetition

This phase matters a lot for later portability and real-world use.

---

## Comparison groups

The current MVP structure uses three important comparison groups.

### A · Baseline
This is the ordinary direct-answer condition.

No Inverse Atlas layer is applied.

A is important because it shows what a strong model tends to do when there is no legitimacy-first governance layer.

It is not there to be insulted.
It is there to establish the control condition.

### B · Inverse Only
This is the cleanest test of the Inverse Atlas line itself.

Only Inverse Atlas is applied.

B matters a lot because it helps answer the question:

**is the inverse legality gate already doing real work by itself**

If B is already meaningfully better than A on legality-centered pressure, that is strong evidence that the inverse line already stands as a real MVP product.

### D · Forward + Inverse
This is the dual-layer direction.

The forward Atlas contributes route-first guidance.
Inverse Atlas contributes legality-first governance.

But one rule must remain explicit:

**the forward output is a weak prior, not an authorization source**

That rule should never be blurred.

The forward side may help orient the structure, but lawful output still has to be governed by the inverse side.

---

## Why there is no C group here

At the current MVP stage, the main comparison interest is not to create a giant matrix for its own sake.

The current structure is centered on the most meaningful contrast lines:

- direct baseline
- inverse-only
- forward-plus-inverse

That is why A, B, and D are the high-value groups right now.

The point is to keep the MVP readable and useful.

If more groups become valuable later, they can be added in a cleaner next phase rather than bloating the present layer too early.

---

## What the current phase structure is trying to show

The current phase structure is meant to show something very specific:

that Inverse Atlas should not only look good on paper, but should change behavior under increasingly serious pressure.

So the phases are arranged to make visible whether the framework:

- works at all
- still works when cases get harder
- still works when context gets longer
- still works when route ambiguity and repair temptation both increase

This is the real reason the phase design matters.

---

## How this relates to Colab

A Colab version makes sense for this experiments layer.

But the role of Colab should stay simple:

**Colab is mainly for reproduction**

It is not required for understanding the project.

It is not the only way to see the value.

A later Colab can help users:

- choose a version
- run a small comparison
- inspect result shape
- reproduce the same case structure more easily

But it is perfectly acceptable for the repository itself to already show:

- the phase structure
- the representative cases
- the current observed findings
- the expected output pattern

That means people do not have to run the notebook just to understand what the framework is supposed to do.

### Important honesty rule
If a future Colab page shows **expected result patterns**, those should be labeled clearly as expected or illustrative.

If a page shows **actual observed findings**, those should be labeled clearly as current findings or observed results.

Do not mix those two categories.

That distinction keeps the experiments layer trustworthy.

---

## What should count as current findings vs expected pattern

This distinction matters a lot.

### Current findings
These are things you have already seen in dry runs, MVP passes, or documented comparisons.

Examples:

- B appears to suppress a meaningful class of illegal escalation behavior
- D appears stronger than B in some cases, provided the forward side remains only a weak prior
- A often over-resolves, over-completes, or overclaims under the same pressure

### Expected pattern
These are things you believe the framework should show if a reproduction is run properly.

Examples:

- Advanced should usually feel more balanced than Basic
- Strict should usually remain more conservative under legality pressure
- Long-context runs should reveal contamination resistance differences more clearly than short single-turn runs

Both are useful.

But they are not the same thing, and they should always be labeled differently.

---

## What this page does not claim

This page does not claim that:

- every phase has already been completed at final scale
- the current MVP phase design is already the final benchmark design
- the existence of a Colab notebook automatically proves the claims
- expected result shape is the same thing as actual measured results
- the dual-layer direction already means the full Bridge operating layer is complete

This page only defines the current experiment structure and how it should be read.

---

## Recommended reading order

If someone is new and wants the cleanest path, use this order:

1. read the [Experiments](./README.md) page
2. read the [Repro in 60 Seconds](./repro-60-seconds.md) page
3. read this phase overview page
4. then read the future results page

That order helps because:

- first you understand what this layer is
- then you see how to reproduce it quickly
- then you understand how the larger phase structure is organized
- then you look at findings

---

## If you need one sentence for outside use

If you want one compact sentence, use this:

> The current Inverse Atlas MVP experiments are organized into Smoke, Core Stress, and Long-Context phases, using baseline, inverse-only, and dual-layer comparison groups to test legality-centered behavior under increasing pressure.

That sentence is short, clear, and honest.

---

## Final Note

The phase structure matters because it gives the project a real testing spine.

It lets the current Inverse Atlas MVP be checked in layers:

- first for visible life
- then for harder stress behavior
- then for long-context discipline

That makes the project much easier to reproduce, explain, and extend later.

And if a Colab layer is added later, its job should stay what it should be:

a reproduction tool, not a substitute for clear documentation. 
