# SAMPLE_DELIVERABLE

Sample shape of a compact WFGY pilot return package.

This page shows what a small WFGY deliverable may look like in practice.

It is not a universal template for every engagement.  
It is a sample structure that makes the output shape legible before any formal collaboration begins.

For the pilot entry itself, see [PILOT_OFFER_ONE_PAGER.md](./PILOT_OFFER_ONE_PAGER.md).  
For the broader collaboration entry, see [WORK_WITH_WFGY.md](./WORK_WITH_WFGY.md).  
For historical context and public proof, see [EVIDENCE_TIMELINE.md](./EVIDENCE_TIMELINE.md).

---

## What this page is

This page is a sample output format.

Its purpose is simple:

show what a compact WFGY return package may contain after a small pilot, audit, or structured review.

This page is here to answer practical questions such as:

1. What would a team actually receive
2. How concrete would the analysis be
3. What kind of structure would WFGY impose on messy failures
4. What is included, and what is not

This is not a legal contract, not a guarantee of outcomes, and not a fixed statement of scope for every future collaboration.

---

## Best way to read this page

The sample below should be read as:

1. a shape example
2. a structure example
3. a boundary example

It is not meant to imply that every real engagement will have the same length, same inputs, or same number of findings.

The main point is to show that WFGY outputs are intended to be:

* structured
* bounded
* readable by mixed teams
* useful for next-step decisions

---

# Sample WFGY Return Package

## 1. Engagement snapshot

**Project type**  
RAG or agent workflow review

**Pilot type**  
Failure audit pilot

**Review window**  
Small scoped pilot based on a limited batch of representative cases

**Primary question**  
Why does the system keep producing wrong or unstable outputs even when the infrastructure appears mostly healthy

**Output goal**  
Turn scattered symptoms into a smaller set of structured failure categories, identify likely root-cause layers, and propose a practical next-step sequence

---

## 2. Inputs reviewed

A compact WFGY pilot may review material such as:

* representative failing cases
* selected logs, traces, screenshots, or prompt chains
* architecture notes or system sketches
* current debugging hypotheses from the team
* known constraints on tooling, ownership, or deployment

The exact input set may vary.  
The point is not to ingest everything.  
The point is to review enough evidence to form a disciplined structural reading.

---

## 3. System snapshot

This section gives a short plain-language description of the system under review.

Example:

The reviewed system is a retrieval-backed generation workflow with a multi-step prompt assembly path, a document store, a ranking layer, and a final answer-generation stage. The team reports recurring answer drift, occasional confident hallucinations, and unstable behavior across similar queries.

This section should be short.  
Its job is to establish context, not rewrite the team’s internal docs.

---

## 4. Observed failure surface

This section lists the visible symptoms before deeper classification.

Example:

1. Answers are often plausible in tone but wrong in content
2. Similar queries produce inconsistent retrieval and inconsistent final answers
3. Some failures appear to begin before generation, especially in retrieval selection or context assembly
4. The team’s current debugging process focuses heavily on model behavior, but evidence suggests multiple upstream layers may be involved

This section stays close to what was actually observed.  
It does not yet claim root cause.

---

## 5. Structured failure classification

This is one of the core sections in a WFGY-style deliverable.

Example:

### Primary category cluster

1. Retrieval-selection instability  
   The system appears to surface context that is variably relevant across similar requests.

2. Context assembly distortion  
   Even when useful material exists, the assembled context may over-compress, fragment, or misweight it before answer generation.

3. Final-answer overconfidence  
   The generation layer sometimes presents uncertain or weakly grounded outputs in a form that looks more stable than the evidence supports.

### Secondary category cluster

1. Evaluation blind spots  
   The current review loop may be catching obvious wrong answers, but not consistently separating retrieval failure from orchestration failure.

2. Triage vocabulary weakness  
   The team may be discussing several different failure layers under one generic label, making debugging slower and less reproducible.

This section is where WFGY becomes useful.  
Its role is to convert raw symptoms into a smaller set of meaningful buckets.

---

## 6. Likely root-cause layers

This section gives a disciplined reading of where the problem most likely lives.

Example:

### Highest-probability layers

1. Retrieval and selection layer  
   Evidence suggests that at least part of the failure begins before the model writes the answer.

2. Context construction layer  
   The prompt may be receiving material that is technically relevant but structurally misassembled.

3. Review and evaluation layer  
   The team’s current debugging loop may not yet isolate layer-specific failure signatures well enough.

### Lower-confidence but relevant layers

1. Memory or carryover behavior
2. Tool or handoff instability
3. Prompt framing side effects

This section should distinguish between:

* likely
* possible
* still unclear

That distinction matters a lot.

---

## 7. What this most likely means

This section translates the diagnosis into practical reading.

Example:

The current pattern does not look like a pure model-quality problem.  
It looks more like a layered systems problem in which retrieval quality, context assembly, and evaluation framing interact to produce unstable final answers.

This matters because the team may waste time if it continues to treat the issue only as “the model hallucinated.”  
The evidence suggests the debugging route should become more layered and more explicit.

This section is not supposed to sound dramatic.  
It is supposed to sharpen decision quality.

---

## 8. Recommended next moves

This section is the most actionable part of the package.

Example:

### Priority 1

Separate retrieval failure from generation failure using a smaller reviewed case set.  
Do not treat all incorrect answers as one category.

### Priority 2

Inspect context assembly rules for compression, ranking, and ordering artifacts.  
Check whether relevant material is being technically retrieved but practically neutralized before generation.

### Priority 3

Add a lightweight review frame that tags each failure by likely layer before discussing fixes.

### Priority 4

Use a shared internal vocabulary for repeated failure categories so that future triage is faster and less dependent on individual intuition.

These actions should be concrete, limited, and realistically sequenced.

---

## 9. What is still uncertain

This section is very important.

Example:

The reviewed material is enough to support a structured preliminary diagnosis, but not enough to make strong claims about long-run production behavior, security properties, or full-system robustness under all workloads.

The following remain uncertain:

1. Whether ranking logic or chunking logic is the dominant upstream driver
2. Whether memory effects are meaningful or incidental
3. Whether some failures are benchmark-specific rather than architecture-level

A good deliverable should say what it does not yet know.

---

## 10. What this does not claim

A sample WFGY return package should clearly state its boundaries.

Example:

This review does not claim:

* that every major failure has been found
* that all root causes are proven
* that the system is close to production readiness
* that architectural changes are unnecessary
* that a small pilot replaces engineering, security, or infra work

The purpose of the package is narrower:

to improve structural clarity, reduce debugging ambiguity, and make the next round of decisions more disciplined.

---

## 11. Possible follow-on outputs

Depending on scope, a future engagement might extend into outputs such as:

* a cleaner failure taxonomy for the team
* a triage protocol based on recurring patterns
* a lightweight debug worksheet
* a review rubric for future runs
* a pilot summary for decision-makers
* a deeper integration or design-partner proposal

Not every pilot needs these.  
They are possible extensions, not default promises.

---

## 12. Why this sample matters

This sample matters because many teams do not need more vague advice.  
They need a clearer way to turn messy failures into smaller, more meaningful decisions.

That is the main role of a WFGY deliverable.

At its best, it helps a team move from:

“something is wrong”

to:

“these are the likely failure layers, these are the boundaries, and these are the next moves worth trying.”

---

## Related pages

* [PILOT_OFFER_ONE_PAGER.md](./PILOT_OFFER_ONE_PAGER.md)
* [WORK_WITH_WFGY.md](./WORK_WITH_WFGY.md)
* [CASE_EVIDENCE.md](./CASE_EVIDENCE.md)
* [ADOPTERS.md](./ADOPTERS.md)
* [EVIDENCE_TIMELINE.md](./EVIDENCE_TIMELINE.md)

---

Maintained as a sample structure, not a fixed contract.
