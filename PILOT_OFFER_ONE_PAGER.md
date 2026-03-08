# PILOT_OFFER_ONE_PAGER

Pilot collaboration entry for teams exploring WFGY in real AI workflows.

This page is a compact, buyer-facing summary of what a WFGY pilot can look like.

It is written for teams who already have a real system, a real failure pattern, or a real evaluation problem, and want to test whether WFGY is useful in practice.

For the broader collaboration entry, see [WORK_WITH_WFGY.md](./WORK_WITH_WFGY.md).  
For a historical view of how WFGY became publicly legible, see [EVIDENCE_TIMELINE.md](./EVIDENCE_TIMELINE.md).  
For a sample output shape, see [SAMPLE_DELIVERABLE.md](./SAMPLE_DELIVERABLE.md).

---

## What this page is

This page is a practical pilot overview.

Its job is simple:

help a serious team answer three questions quickly:

1. Is WFGY relevant to our situation
2. What would a small pilot actually look like
3. What would we likely get back at the end

This is not a pitch deck, not a customer logo page, and not a promise of enterprise deployment.

---

## Who this is for

WFGY pilots are best suited for teams that already have one of the following:

* a RAG system that keeps returning wrong answers even when infra looks normal
* an agent or multi-agent workflow with unstable behavior, drift, or brittle handoffs
* an evaluation workflow that can score outputs, but still cannot clearly explain failure structure
* a debugging process that is expensive, slow, and overly dependent on ad hoc intuition
* a research or platform team that wants a more structured way to classify failure modes

In short, this page is for teams with real questions, not for people looking for generic prompt advice.

---

## What WFGY is most useful for in a pilot

At the current stage, the strongest practical wedge for WFGY is structured diagnosis.

That usually means one or more of the following:

* classifying recurring failure modes in a RAG or agent pipeline
* separating retrieval, prompt assembly, orchestration, memory, and evaluation failures
* building a more stable debugging vocabulary across engineers, PMs, and researchers
* turning scattered symptoms into a smaller set of reproducible failure categories
* reducing guesswork before a team spends time on bigger architectural changes

This is especially useful when a team already knows that “something is wrong,” but cannot yet describe the failure in a way that leads to clean fixes.

---

## Pilot formats

A WFGY pilot will usually fit one of these formats.

### 1. Failure audit pilot

Best for teams with a live or recently failing RAG or agent workflow.

Typical goal:

map observed failures into a smaller set of structured categories, identify the likely layer where the problem actually lives, and suggest the smallest next debugging moves.

Typical inputs:

* failing examples
* run traces, logs, screenshots, or prompt chains
* brief architecture description
* known symptoms and current hypotheses

Typical outputs:

* structured failure classification
* likely root-cause layer analysis
* fix priority suggestions
* a clearer debugging route for the team

---

### 2. Triage workshop pilot

Best for teams that need fast alignment across internal stakeholders.

Typical goal:

use WFGY surfaces such as the Problem Map or Global Debug Card to create a shared language for triage, review, and prioritization.

Typical inputs:

* representative failure cases
* current internal workflow for debugging or review
* participating team roles
* constraints on time, tooling, or ownership

Typical outputs:

* a shared failure vocabulary
* a smaller triage decision surface
* candidate routing rules for common cases
* a cleaner handoff structure across team members

---

### 3. Design partner pilot

Best for teams exploring deeper protocol, tooling, or evaluation integration.

Typical goal:

test whether WFGY can serve as part of a reusable debugging, evaluation, or reasoning layer inside a broader product or research workflow.

Typical inputs:

* a clear use case
* target surface for integration or evaluation
* baseline workflow or benchmark
* practical constraints and success criteria

Typical outputs:

* pilot framing document
* integration hypotheses
* structured observations from the trial
* recommendation on whether deeper work is justified

---

## What a team usually needs to provide

A good pilot depends on concrete material.

The team does not need to provide everything at once, but a serious pilot usually needs:

* one clear system or use case
* several representative failures or stress cases
* enough context to understand where the system boundaries are
* the current debugging or evaluation workflow, even if it is messy
* one contact point who can answer follow-up questions

If the pilot is about a production system, confidentiality and scope should be discussed early.

---

## What WFGY usually provides

A WFGY pilot usually provides structure, not magic.

That structure may include:

* a clearer failure map
* a smaller set of meaningful categories
* sharper distinctions between surface symptoms and deeper causes
* a more reproducible debugging route
* a shared interpretive layer that makes future failures easier to discuss

Where relevant, WFGY may also provide draft artifacts such as:

* a case classification sheet
* a triage summary
* a debug routing proposal
* an evaluation framing note
* a recommended next-step sequence

For an example of the shape of outputs, see [SAMPLE_DELIVERABLE.md](./SAMPLE_DELIVERABLE.md).

---

## What this does not claim

A WFGY pilot does not automatically mean:

* full production integration
* guaranteed model quality improvement
* enterprise-grade support or SLA
* replacement of platform engineering, ML engineering, or security review
* one-step diagnosis of every failure in a complex system

WFGY is most useful when it helps a team see the failure structure more clearly.

That often improves decision quality, but it should not be described as a universal fix.

---

## Good fit and bad fit

### Good fit

A pilot is usually a good fit when:

* the team has real failure cases
* the problem is costly enough to matter
* the team wants sharper structure, not vague brainstorming
* the team is open to disciplined boundary-setting
* the team can provide enough evidence to reason from

### Bad fit

A pilot is usually a poor fit when:

* there is no concrete system yet
* the team only wants generic prompting advice
* the team wants guaranteed outcomes before sharing any evidence
* the problem is actually legal, security, compliance, or infra ownership only
* the team expects WFGY to replace core implementation work

---

## Suggested pilot flow

A small pilot can often be framed in four stages:

1. Scope  
   define the system, the problem surface, and the pilot question

2. Evidence intake  
   review examples, traces, and known symptoms

3. Structured analysis  
   map failures, isolate likely layers, and identify the most useful distinctions

4. Return package  
   provide a compact summary of findings, boundaries, and recommended next moves

This is intentionally small.

The purpose of a pilot is not to pretend the whole system is solved.  
The purpose is to learn whether WFGY creates real clarity and practical leverage.

---

## Best current reading of WFGY pilot value

Today, the safest and strongest claim is this:

WFGY is most legible as a structured reasoning and debugging layer for AI systems, especially where teams need better failure classification, cleaner triage, and more reproducible diagnosis.

That is the right starting point for a pilot.

Broader claims should only be made if later evidence supports them.

---

## Next step

If your team is exploring a pilot, start here:

* [WORK_WITH_WFGY.md](./WORK_WITH_WFGY.md) for the broader collaboration entry
* [CASE_EVIDENCE.md](./CASE_EVIDENCE.md) for how public cases should be read
* [ADOPTERS.md](./ADOPTERS.md) for the shortest public proof summary

If needed, this page can later evolve into a more formal outward-facing pilot brief.  
For now, its role is simpler:

to make the pilot path legible without overselling it.
