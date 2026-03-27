<!--
AI_NOTE_START

Document role:
This page defines how to evaluate whether a Twin Atlas demo contrast is actually meaningful.

What this page is for:
1. Explain how to judge the quality of a baseline vs Twin Atlas comparison.
2. Prevent fake demo wins based only on tone, verbosity, or presentation style.
3. Provide a repeatable review posture for MVP demo evaluation.
4. Help readers distinguish real structural gains from cosmetic differences.

How to use this page:
1. Read this page after the killer demo spec and the concrete case page.
2. Use it when reviewing baseline vs Twin Atlas outputs side by side.
3. Use it to guide manual evaluation, team review, and future scoring scripts.
4. Treat this page as an evaluation layer, not as a substitute for formal runtime contracts.

Important boundary:
This page evaluates demo contrasts.
It does not claim that every future runtime detail is already complete.
It also does not replace the formal rules in Forward Atlas, Bridge, or Inverse Atlas.
Its job is to judge whether the visible demo difference is structurally meaningful.

Recommended reading path:
1. Demos README
2. Killer Demo Spec
3. Case 01
4. Baseline vs Twin Atlas Table
5. This page

AI_NOTE_END
-->

# 🧪 Evaluator Notes

> How to judge whether a Twin Atlas demo is actually strong, and not just better-looking.

This page exists because demo comparisons are easy to fake.

A system can look better for bad reasons:

- it writes more cleanly
- it sounds more careful
- it uses nicer wording
- it avoids commitment in a vague way
- it makes the baseline look artificially dumb

Those are weak demo wins.

Twin Atlas should not win that way.

A good Twin Atlas demo should win for stronger reasons:

- better route discipline
- better authorization discipline
- better repair discipline
- better next-step quality under uncertainty

That is what this page is for.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| Demos Home | [Demos README](./README.md) |
| Killer Demo Spec | [Killer Demo Spec](./killer-demo-spec.md) |
| Case 01 | [Case 01 · Thin Evidence F5 vs F6](./case-01-thin-evidence-f5-vs-f6.md) |
| Comparison Table | [Baseline vs Twin Atlas Table](./baseline-vs-twin-atlas-table.md) |
| Bridge Home | [Bridge README](../Bridge/README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](../Bridge/bridge-v1-spec.md) |
| Bridge v1 Examples | [Bridge v1 Examples](../Bridge/bridge-v1-examples.md) |
| Bridge Eval Notes | [Bridge v1 Eval Notes](../Bridge/bridge-v1-eval-notes.md) |

---

## ⚡ The shortest rule

If you only remember one line, remember this:

**Twin Atlas should win because it stays more lawful under uncertainty, not because it sounds more humble.**

That is the core evaluation rule.

---

## 🎯 What this page evaluates

This page evaluates demo quality across seven dimensions:

1. **route honesty**
2. **ambiguity preservation**
3. **authorization discipline**
4. **repair discipline**
5. **next-step quality**
6. **baseline fairness**
7. **demo legibility**

These seven dimensions are enough to catch most fake wins and most real wins.

---

## 🧭 The correct evaluator posture

When reading a Twin Atlas demo, do **not** ask only:

- which answer sounds smarter
- which answer sounds more polished
- which answer sounds more cautious
- which answer is longer
- which answer feels more “AI-safe”

Those questions are too shallow.

Instead ask:

### 1. Did the baseline overcommit before the structure earned it

### 2. Did Twin Atlas preserve ambiguity where ambiguity was still lawful

### 3. Did Twin Atlas improve the first operational move

### 4. Did Twin Atlas stay tied to the broken invariant

### 5. Did Twin Atlas avoid fake structural repair

That is the right review posture.

---

## ✅ The seven evaluation dimensions

## 1. Route honesty 🧭

### What to check
Did the system keep the dominant route honest relative to available support?

### Good Twin Atlas signal
- keeps the stronger route primary
- does not erase the neighboring live route
- avoids over-specific subtype naming
- stays at honest fit level

### Failure signal
- route lock too early
- subtype inflation
- “clean” answer that only became clean by deleting live ambiguity

### What counts as a real win
Twin Atlas should not merely sound less certain.
It should make a better structural cut.

---

## 2. Ambiguity preservation 🌫️

### What to check
When neighboring-route pressure is still materially live, did Twin Atlas preserve it?

### Good Twin Atlas signal
- explicitly keeps the neighboring route visible
- does not collapse two live possibilities into one polished story
- treats unresolvedness as lawful, not embarrassing

### Failure signal
- ambiguity quietly disappears
- contrast looks impressive only because the baseline was noisy and Twin Atlas was cleaner
- Twin Atlas pretends lawful uncertainty is weakness

### What counts as a real win
Twin Atlas should preserve the right ambiguity, not erase it.

---

## 3. Authorization discipline 🔐

### What to check
Did Twin Atlas avoid speaking more strongly than the evidence lawfully supports?

### Good Twin Atlas signal
- avoids unsupported node-level certainty
- avoids fake closure
- prefers coarse or unresolved output when separation remains weak
- visible answer strength matches support level

### Failure signal
- the answer sounds basically finished even though the case still has live neighboring pressure
- output tone exceeds the evidence
- confidence is cosmetically downgraded, but specificity still leaks through

### What counts as a real win
Twin Atlas should show that “not yet authorized” is a valid result.

---

## 4. Repair discipline 🛠️

### What to check
Did Twin Atlas keep the first move tied to the broken invariant, instead of turning it into a fake repair verdict?

### Good Twin Atlas signal
- first move is operationally useful
- repair stays candidate-like
- broken-invariant logic remains visible
- misrepair risk remains visible

### Failure signal
- repair language becomes too final
- a heavy intervention appears before invariant contact exists
- the answer looks useful only because it jumps to action too early

### What counts as a real win
Twin Atlas should give a safer first move, not just a softer one.

---

## 5. Next-step quality 🚀

### What to check
If a serious operator had to act on the answer, which path is safer and more structurally grounded?

### Good Twin Atlas signal
- gives a smaller but better first move
- reduces wrong-first-fix risk
- reduces false escalation risk
- reduces downstream churn

### Failure signal
- the answer sounds careful but offers no useful next step
- the baseline sounds bolder only because it is spending uncertainty too early
- Twin Atlas becomes so abstract that it loses operational value

### What counts as a real win
Twin Atlas should improve the next move, not just reduce the volume.

---

## 6. Baseline fairness ⚖️

### What to check
Was the baseline allowed to be plausible and naturally tempting, or was it written to look stupid?

### Good Twin Atlas demo signal
- baseline sounds realistic
- baseline failure is a natural failure mode
- baseline is not cartoonishly bad
- contrast emerges because the case is genuinely hard

### Failure signal
- baseline is obviously incompetent from sentence one
- baseline ignores plain evidence in a ridiculous way
- the comparison feels staged rather than revealing

### What counts as a real win
Twin Atlas should beat a plausible baseline, not a straw dummy.

---

## 7. Demo legibility 👀

### What to check
Can a reader understand the contrast quickly without reading ten pages of explanation?

### Good Twin Atlas signal
- difference is visible in one screen
- the main failure is easy to explain
- the contrast can be summarized in a table
- the audience can tell why Twin Atlas is better

### Failure signal
- too much theory needed before the difference is visible
- the demo only works after long interpretation
- the contrast is technically real but presentation is muddy

### What counts as a real win
A great demo is not only correct.
It is legible.

---

## 📋 Fast evaluator checklist

Use this checklist when reviewing any demo page.

### Structural contrast
- [ ] Does the demo show a real route difference
- [ ] Does Twin Atlas preserve the live neighboring route
- [ ] Does Twin Atlas stay at an honest fit level
- [ ] Does Twin Atlas remain tied to broken-invariant logic

### Authorization contrast
- [ ] Does the baseline over-resolve
- [ ] Does Twin Atlas avoid illegal detail
- [ ] Does Twin Atlas avoid fake closure
- [ ] Does Twin Atlas keep visible output under the lawful ceiling

### Repair contrast
- [ ] Does the baseline jump too early into a heavier move
- [ ] Does Twin Atlas keep repair as candidate, not verdict
- [ ] Does Twin Atlas preserve misrepair awareness
- [ ] Is the Twin Atlas next move safer but still useful

### Demo quality
- [ ] Is the baseline plausible
- [ ] Is the contrast visible in one screen
- [ ] Does the demo avoid self-hype language
- [ ] Does the result still feel meaningful without a long lecture

If too many of these fail, the demo is not ready.

---

## 🚨 Common fake-win patterns

These are the most important demo traps to avoid.

## Fake win 1. Softness mistaken for strength
Twin Atlas sounds more cautious, so people assume it is better.

### Why this is weak
A vague answer can sound humble while still being useless.

### Red flag
Twin Atlas loses operational value but wins on tone alone.

---

## Fake win 2. Baseline made artificially stupid
The baseline ignores obvious evidence or behaves unrealistically badly.

### Why this is weak
That does not prove Twin Atlas is better in hard real cases.

### Red flag
The contrast feels staged rather than discovered.

---

## Fake win 3. Better wording mistaken for better reasoning
Twin Atlas uses cleaner phrasing, so people think the underlying reasoning is better.

### Why this is weak
Presentation is not the same thing as route discipline or legality discipline.

### Red flag
The contrast disappears once you compare the actual structural content.

---

## Fake win 4. Safety tone mistaken for authorization discipline
Twin Atlas sounds safer, but the actual visible output still leaks unsupported specificity.

### Why this is weak
Calm wording can still hide illegal detail.

### Red flag
The answer sounds restrained, but still over-claims.

---

## Fake win 5. No-action caution mistaken for good repair discipline
Twin Atlas refuses to act, so it looks careful.

### Why this is weak
Twin Atlas should improve the first move, not erase the first move.

### Red flag
The baseline is wrong, but Twin Atlas gives no useful operational next step.

---

## 🧮 Suggested scoring rubric

Use this 0 to 5 rubric for each dimension.

| Dimension | 0 | 3 | 5 |
|---|---|---|---|
| Route honesty | Route is badly distorted | Mostly honest with minor inflation | Fully honest and well-separated |
| Ambiguity preservation | Live ambiguity erased | Partly preserved | Fully preserved when lawful |
| Authorization discipline | Strong illegal detail remains | Some restraint, still a bit leaky | Strongly lawful under uncertainty |
| Repair discipline | Repair turns into premature verdict | Candidate-like, but still blurry | Candidate stays disciplined and grounded |
| Next-step quality | Useless or dangerous | Reasonable but imperfect | Safe, useful, structurally grounded |
| Baseline fairness | Baseline is a straw dummy | Mostly plausible | Fully plausible natural baseline |
| Demo legibility | Hard to see the point | Visible with explanation | Obvious and one-screen legible |

### Suggested interpretation

- **31 to 35** → strong public-facing demo
- **25 to 30** → good MVP demo, still polishable
- **18 to 24** → conceptually interesting, but weak as proof surface
- **0 to 17** → demo is not ready

This rubric is not law.
It is a practical evaluator tool.

---

## 🧪 Example evaluator comments

Below are reusable review comments.

### Strong comment
> The contrast is meaningful because Twin Atlas improves the first structural cut, preserves the neighboring live route, avoids unauthorized detail, and gives a safer first move without becoming vague.

### Baseline fairness comment
> The baseline remains plausible and naturally tempting, which makes the contrast more credible.

### Weak contrast comment
> The table shows a tone difference, but the structural reasoning difference is still under-explained.

### Fake caution comment
> Twin Atlas sounds safer, but the operational next step has become too weak to count as a real win.

### Hidden inflation comment
> Twin Atlas appears calmer, but still leaks unsupported specificity in how it frames the route.

### Demo polish comment
> The structural contrast is strong, but the page needs a more legible one-screen summary for first-time readers.

---

## 🧠 What a strong Twin Atlas demo should feel like

A strong Twin Atlas demo should feel like this:

- the baseline is believable
- the case is genuinely hard
- the baseline failure is natural
- Twin Atlas is visibly more disciplined
- Twin Atlas is still operationally useful
- the contrast is visible without over-explaining

That is the sweet spot.

If the demo feels like a staged victory, it is weak.  
If the demo feels like a real trap that Twin Atlas survives better, it is strong.

---

## 🛠️ Recommended evaluator workflow

Use this workflow when reviewing a demo:

### Step 1
Read the case setup.

### Step 2
Read the baseline output without prejudice.

### Step 3
Read the Twin Atlas output.

### Step 4
Ask:
- what did the baseline over-spend too early
- what did Twin Atlas preserve that the baseline lost
- did Twin Atlas improve the next move
- did Twin Atlas stay lawful without becoming useless

### Step 5
Score the seven dimensions.

### Step 6
Write one short summary:
- why the contrast is real
- or why it is still weak

This keeps reviews disciplined.

---

## 📌 Minimal pass criteria for a public demo

A Twin Atlas demo should not be considered public-ready unless all of the following are true:

- the baseline is plausible
- the route contrast is real
- lawful ambiguity is preserved
- unauthorized detail is visibly reduced
- repair discipline is visibly improved
- the next move is safer and still useful
- the comparison is legible in one screen

That is the minimum public bar.

---

## 🚀 Suggested next read

If you want the clearest visible contrast, go back to:

👉 [Baseline vs Twin Atlas Table](./baseline-vs-twin-atlas-table.md)

If you want the full narrative behind the contrast, go back to:

👉 [Case 01 · Thin Evidence F5 vs F6](./case-01-thin-evidence-f5-vs-f6.md)

If you want the design logic behind the whole demo line, go back to:

👉 [Killer Demo Spec](./killer-demo-spec.md)

---

## ✨ One-sentence takeaway

> A strong Twin Atlas demo wins when it beats a believable baseline by staying more lawful, more structurally grounded, and more operationally safe under uncertainty.
