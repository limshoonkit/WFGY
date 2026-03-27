<!--
AI_NOTE_START

Document role:
This page explains how to choose between the public runtime modes inside WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Clarify the difference between Basic, Advanced, and Strict.
2. Explain when each runtime mode should be used.
3. Show how runtime intensity relates to ambiguity, authorization pressure, and repair discipline.
4. Make mode switching easier for both vibe coders and serious engineers.

How to use this page:
1. Read this page after the Runtime README.
2. Use it when deciding which runtime form to apply to a case.
3. Use it as a quick operational reference during debugging, reasoning, or evaluation.
4. Treat this page as runtime guidance, not as a replacement for the deeper architecture docs.

Important boundary:
This page explains the public effective-layer runtime modes only.
It does not expose hidden internal reasoning substrate details.
It also does not claim that every future runtime behavior is already fully finalized.
Its job is to make the current runtime ladder legible and usable.

Recommended reading path:
1. Twin Atlas README
2. Runtime README
3. this page
4. twin-atlas-basic.txt
5. twin-atlas-advanced.txt
6. twin-atlas-strict.txt
7. Bridge docs
8. demo cases

AI_NOTE_END
-->

# 🎛️ Runtime Mode Notes

> How to choose between Basic, Advanced, and Strict inside WFGY 4.0 Twin Atlas Engine.

The runtime ladder exists because one mode is not enough for every case.

Some tasks need:

- lower friction
- faster adoption
- lighter structure

Other tasks need:

- stronger route discipline
- stronger ambiguity preservation
- stronger authorization discipline
- stronger repair discipline

That is why Twin Atlas exposes three public runtime forms:

- **Basic**
- **Advanced**
- **Strict**

This page explains how to choose between them.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| FAQ | [FAQ](../faq.md) |
| Roadmap | [Roadmap](../roadmap.md) |
| Release Notes | [Release Notes](../release-notes.md) |
| Runtime Home | [Runtime README](./README.md) |
| Basic Runtime | [Twin Atlas Basic](./twin-atlas-basic.txt) |
| Advanced Runtime | [Twin Atlas Advanced](./twin-atlas-advanced.txt) |
| Strict Runtime | [Twin Atlas Strict](./twin-atlas-strict.txt) |
| Coupling Flow | [Twin Atlas Coupling Flow](./twin-atlas-coupling-flow.md) |
| Bridge Home | [Bridge README](../Bridge/README.md) |
| Bridge v1 Spec | [Bridge v1 Spec](../Bridge/bridge-v1-spec.md) |
| Demos Home | [Demos README](../demos/README.md) |
| Case 01 | [Case 01 · Thin Evidence F5 vs F6](../demos/case-01-thin-evidence-f5-vs-f6.md) |

---

## ⚡ The shortest version

If you only remember one thing, remember this:

**Basic is for easier entry.  
Advanced is the main working mode.  
Strict is for cases where wrong certainty is expensive.**

That is the runtime ladder in one line.

---

# 🧭 Section 1 · Why three modes exist

Twin Atlas is not trying to force every case into one heavy governance shape.

That would be clumsy.

Different cases have different costs.

Some cases mainly need:
- better first structural cut
- a cleaner next move
- slightly better ambiguity handling

Other cases need much more:
- route preservation
- ambiguity preservation
- visible strength control
- repair candidate discipline
- stronger resistance to fake closure

The three modes exist because **governance intensity should scale with case cost**.

That is the design logic.

---

# 🟢 Section 2 · Basic Mode

## What Basic is

Basic is the lowest-friction public runtime form.

It is the easiest way to start using Twin Atlas without immediately moving into the heavier governance posture of the stronger modes.

Basic should feel:

- light
- usable
- practical
- disciplined
- not overloaded

It is meant to preserve the Twin Atlas flavor without forcing maximum strictness on every case.

---

## What Basic is good for

Basic is good for cases like:

- first-pass debugging
- everyday structured reasoning
- light workflow analysis
- early RAG diagnosis pass
- situations where normal prompting is too loose, but heavy governance is not yet necessary
- first-time Twin Atlas adoption

Basic is a very good first step when the case matters, but the cost of being wrong confidently is not yet extreme.

---

## What Basic emphasizes

Basic emphasizes:

- a better first structural read
- a visible best-current route
- basic neighboring-route awareness
- likely broken-invariant awareness
- a safer useful next move
- not spending certainty too early

Basic already resists:

- fake neatness
- fake subtype precision
- premature overcommitment

But it does so with lower ceremony and lower overhead.

---

## What Basic does not push as hard

Basic does not push the hardest version of:

- ambiguity preservation
- authorization discipline
- visible-state rigor
- repair candidate rigor
- lawful unresolvedness tolerance

That is intentional.

Basic is not weak.  
It is just the lightest public form.

---

## When Basic is the right choice

Use Basic when:

- you want a lower-friction entry
- the case is important but not highly adversarial
- the evidence is not extremely thin
- wrong-first-fix would be annoying but not catastrophic
- you want better structure without the heaviest runtime pressure

---

# 🟡 Section 3 · Advanced Mode

## What Advanced is

Advanced is the main working mode of Twin Atlas.

If Basic is the entry form, Advanced is the real daily-driver form for serious use.

Advanced should feel:

- sharper
- more structurally aware
- more ambiguity-aware
- more repair-disciplined
- more operationally serious

This is the mode most people should graduate into once they stop treating Twin Atlas as just something to try.

---

## What Advanced is good for

Advanced is good for:

- serious debugging
- workflow diagnosis
- RAG failure analysis
- agent-path reasoning
- ambiguity-heavy technical analysis
- cases where wrong-first-fix is meaningfully costly
- cases where support boundaries matter, but not yet at maximum risk level

If someone asks:

**“which mode is the real working mode?”**

the answer is usually:

**Advanced**

---

## What Advanced emphasizes

Advanced emphasizes:

- explicit route-first discipline
- preservation of the nearest live competing route
- stronger broken-invariant targeting
- stronger candidate-not-verdict repair posture
- stronger confidence and fit discipline
- stronger evidence-demand behavior when route separation is weak

Advanced is where Twin Atlas starts showing much more of its real engine character.

---

## What Advanced still avoids

Advanced still avoids becoming:

- too ceremonial
- too rigid
- too formal for normal use
- too abstract to act on

It is supposed to be stronger than Basic, but still practical enough for real engineering work.

---

## When Advanced is the right choice

Use Advanced when:

- the task is materially important
- the case is structurally messy
- a wrong first move could cost real time
- the baseline would likely overcommit
- ambiguity is real enough that you want it preserved explicitly
- you want the main Twin Atlas experience without going full highest-governance mode

---

# 🔴 Section 4 · Strict Mode

## What Strict is

Strict is the highest-governance public runtime form.

It is the mode you use when being wrong confidently is especially expensive.

Strict should feel:

- calm under pressure
- structurally serious
- visibly support-bounded
- resistant to fake closure
- comfortable with lawful unresolvedness

Strict is not timid mode.

It is the mode that refuses to spend certainty before the case has earned it.

---

## What Strict is good for

Strict is best for:

- thin-evidence cases
- high-risk debugging
- high-cost workflow decisions
- research-heavy reasoning
- scientific interpretation
- ambiguous retrieval or evidence cases
- emotionally pressured users pushing for strong closure
- cases where repair verdict leakage would be expensive

Strict is where Twin Atlas most clearly resists:

- fake finality
- unsupported detail
- fake repair legality
- ambiguity deletion

---

## What Strict emphasizes

Strict emphasizes:

- strongest neighboring-route preservation
- strongest visible-state discipline
- strongest evidence-boundary discipline
- strongest candidate-vs-verdict separation
- strongest resistance to dramatic wording pressure
- strongest tolerance for lawful coarse or unresolved answers

If Advanced is the main working mode, Strict is the mode for hardest cases.

---

## When Strict is the right choice

Use Strict when:

- evidence is thin or partial
- route separation is weak
- downstream action cost is high
- the user is demanding more certainty than the structure supports
- subtype temptation is strong
- the answer may trigger expensive engineering action
- the problem is research-heavy or scientifically sensitive

---

# ⚖️ Section 5 · Fast comparison table

| Dimension | Basic | Advanced | Strict |
|---|---|---|---|
| Friction | Lowest | Medium | Highest |
| Intended use | First entry, lighter hard cases | Main working mode | Highest-risk public mode |
| Route discipline | Present | Strong | Strongest |
| Neighbor preservation | Present, lighter | Stronger | Strongest |
| Authorization discipline | Present, lighter | Strong | Strongest |
| Repair discipline | Good | Strong | Strongest |
| Tolerance for unresolvedness | Moderate | Higher | Highest |
| Resistance to fake closure | Moderate | Strong | Strongest |
| Best for | Lower-risk structured use | Serious normal-use hard cases | Thin-evidence and high-cost cases |

This is the simplest comparison surface.

---

# 🧪 Section 6 · Mode selection logic

A simple way to choose a mode is to ask three questions.

## Question 1
How expensive would a wrong-first-fix be?

- low to moderate → Basic
- moderate to high → Advanced
- high to very high → Strict

## Question 2
How thin is the evidence?

- decent support, early structured use → Basic
- partial support, real ambiguity → Advanced
- weak or highly contested support → Strict

## Question 3
How dangerous would unsupported certainty be?

- manageable → Basic
- meaningfully costly → Advanced
- very costly → Strict

This is usually enough to choose a mode fast.

---

# 🌫️ Section 7 · Ambiguity handling differences

The easiest way to feel the mode differences is to look at how each mode handles ambiguity.

## Basic
Basic keeps ambiguity when needed, but with lighter pressure.

Good for:
- “X currently looks stronger than Y”

## Advanced
Advanced more deliberately preserves live neighboring routes and resists fake neatness.

Good for:
- “X is currently stronger, but Y remains materially live”

## Strict
Strict treats lawful unresolvedness as a first-class valid state.

Good for:
- “X is currently better supported, but route separation is still too weak to justify stronger commitment”

That difference is a major part of the ladder.

---

# 🔐 Section 8 · Authorization intensity differences

The modes are not only style variants.

They differ in **authorization pressure**.

## Basic
Asks:
- am I becoming too strong too early

## Advanced
Asks:
- am I becoming too strong too early, and am I preserving the live competing route honestly

## Strict
Asks:
- has this answer really earned this visible strength yet, or am I simulating resolution with clean wording and premature confidence

That is why Strict feels so different in hard cases.

---

# 🛠️ Section 9 · Repair discipline differences

The repair posture also gets stronger as the modes rise.

## Basic
Keeps a safer next move in view.

## Advanced
Actively ties the next move to the likely broken invariant and preserves misrepair risk more explicitly.

## Strict
Treats repair candidate vs repair verdict separation as a core law and resists all pressure toward fake repair finality.

This is important because many bad answers fail not only in route selection, but in the **first confident repair move**.

---

# 🔗 Section 10 · Relationship to the coupling flow

All three modes should still follow the same minimal Twin Atlas flow:

1. route construction
2. Bridge handoff
3. inverse recheck
4. visible output clamping
5. public answer

What changes across modes is not the existence of the flow.

What changes is how hard each mode pushes the laws inside that flow.

## Basic
Lighter enforcement.

## Advanced
Stronger enforcement.

## Strict
Strongest public-layer enforcement.

This is why the three modes are not three different engines.

They are three intensities of the same engine.

---

# 🚨 Section 11 · Common mode-selection mistakes

## Mistake 1
Using Basic for thin-evidence high-risk cases.

Why bad:
> Basic may still help, but it is not the strongest barrier against fake closure.

## Mistake 2
Using Strict for everything.

Why bad:
> This adds unnecessary friction and makes the engine feel heavier than it needs to be.

## Mistake 3
Thinking Advanced is just “Basic with fancier words.”

Why bad:
> Advanced is supposed to enforce stronger ambiguity preservation and repair discipline, not just sound more serious.

## Mistake 4
Choosing mode based only on emotional intensity of the user.

Why bad:
> The key variable is structural cost and evidence state, not how dramatic the user sounds.

## Mistake 5
Treating mode differences as tone differences only.

Why bad:
> The real difference is governance intensity, not cosmetics.

---

# ✅ Section 12 · Practical mode recommendations

If you want very short operational advice, use this:

## Use Basic when
- you are starting
- the case matters, but not maximally
- you want structure with low friction

## Use Advanced when
- the case is serious
- the ambiguity is real
- the next move matters
- you want the main Twin Atlas experience

## Use Strict when
- support is thin
- closure pressure is high
- downstream error cost is high
- you care more about lawfulness than fluency

This is the most practical ladder.

---

# 🧠 Section 13 · Mode-switch guidance

A healthy Twin Atlas workflow may move between modes.

For example:

### Start in Basic
when scoping a case quickly.

### Move to Advanced
when the case becomes real enough that route quality and wrong-first-fix risk matter.

### Move to Strict
when:
- evidence stays thin
- the cost of false certainty goes up
- the user pressures for stronger closure than the case supports

Mode switching is not a failure.

It is part of good engine use.

---

# 🚧 Section 14 · What these mode notes do not claim

This page should not be used to claim that:

- all mode behaviors are already fully implemented in every runtime environment
- every future transition rule is already frozen
- Basic, Advanced, and Strict are already production-equal in all contexts
- the hidden internal substrate is being fully described here

This page explains the current public ladder.

It does not pretend the deepest implementation work is already finished.

---

# 🧡 Section 15 · A vibe-coder-friendly summary

If you want the fastest version:

### Basic
good first ride

### Advanced
real working mode

### Strict
expert mode when fake certainty is dangerous

That is the ladder.

---

# 🚀 Suggested next read

After this page, the most useful next files are:

1. [Twin Atlas Basic](./twin-atlas-basic.txt)
2. [Twin Atlas Advanced](./twin-atlas-advanced.txt)
3. [Twin Atlas Strict](./twin-atlas-strict.txt)
4. [Twin Atlas Coupling Flow](./twin-atlas-coupling-flow.md)
5. [Case 01 · Thin Evidence F5 vs F6](../demos/case-01-thin-evidence-f5-vs-f6.md)

That sequence makes the runtime ladder much easier to feel in practice.

---

# ✨ One-sentence takeaway

> The runtime modes in Twin Atlas are not three writing styles, but three levels of governance intensity for how hard the engine protects route honesty, ambiguity preservation, repair discipline, and support-bounded visible output.

