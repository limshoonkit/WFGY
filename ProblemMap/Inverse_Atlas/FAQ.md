<!--
AI_NOTE_START

Document role:
This page is the main FAQ page for the current Inverse Atlas MVP.

What this page is for:
1. Answer the most common practical and conceptual questions about Inverse Atlas.
2. Explain why Inverse Atlas exists, how it differs from the forward Atlas, and how it should be used.
3. Summarize important ideas from the framework paper in a more accessible product-facing form.
4. Help readers avoid common misunderstandings about MVP scope, legality-first governance, and future architecture.

How to use this page:
1. Read this page after the main Inverse Atlas README if you want a faster, question-based overview.
2. Use this page when deciding which version to try, whether to use Colab, and how to think about Twin Atlas.
3. Use this page as a practical explanation layer, not as the formal boundary source. For strict claim boundary, see Status and Boundaries.
4. Use this page when you want the “paper, but in FAQ form” version of the project.

Important boundary:
This page explains the current MVP clearly and confidently, but it should not be used to claim that the full Bridge layer, the full WFGY 4.0 closed-loop system, or universal benchmark superiority are already complete unless other pages explicitly support those claims.

Recommended reading path:
1. Inverse Atlas README
2. FAQ
3. Versions
4. Quick Start
5. Runtime Guide
6. Experiments
7. Status and Boundaries
8. Twin Atlas

AI_NOTE_END
-->

# FAQ ❓ Common Questions About Inverse Atlas

> A practical guide to what Inverse Atlas is, why it exists, and how to use it

This page answers the most common questions about Inverse Atlas in a more direct format.

If the main README is the front door, this page is the conversation you have after walking in.

It is also the easiest place to understand why Inverse Atlas exists at all:

**because the forward troubleshooting atlas was already useful at route-first classification and structural orientation, and that success revealed the next problem**

That next problem was this:

even if a model gets better at mapping the likely failure region, it can still speak too strongly, resolve too early, overclaim, and present cosmetic repair as if it were structural.

So the natural next move was to turn the atlas logic around and ask a different question:

**not only “where is the problem?” but also “has the system actually earned the right to answer this strongly yet?”**

That is where Inverse Atlas comes from. :contentReference[oaicite:1]{index=1}

---

## Quick Links 🔎

| Section | Link |
|---|---|
| Inverse Atlas Home | [Inverse Atlas README](./README.md) |
| Versions | [Versions](./versions.md) |
| Quick Start | [Quick Start](./quickstart.md) |
| Runtime Guide | [Runtime Guide](./runtime-guide.md) |
| Dual-Layer Positioning | [Dual-Layer Positioning](./dual-layer-positioning.md) |
| Status and Boundaries | [Status and Boundaries](./status-and-boundaries.md) |
| Experiments | [Experiments](./experiments/README.md) |
| Repro in 60 Seconds | [Repro in 60 Seconds](./experiments/repro-60-seconds.md) |
| Paper Notes | [Paper Notes](./paper/README.md) |
| Figure Notes | [Figure Notes](./figures/README.md) |
| WFGY 4.0 Entry | [Twin Atlas](../Twin_Atlas/README.md) |

---

## 1. What is Inverse Atlas ⚖️

Inverse Atlas is a **pre-generative governance framework** for AI legitimacy.

That means it does not start by asking:

“how do we improve the answer after it appears?”

It starts earlier and asks:

**should the system be allowed to answer at this level at all**

The paper frames this as a shift from default generation to authorized generation. In other words, generation is not treated as an automatic right. It is treated as an act that must first pass legality checks. :contentReference[oaicite:2]{index=2}

---

## 2. Why does Inverse Atlas exist at all 🧭

It exists because the forward troubleshooting atlas already showed something important:

**route-first structural mapping is useful, but it is not enough**

The forward Atlas helps a system ask:

- what structural region are we probably in
- what failure family seems active
- what broken invariant is likely involved
- what first repair direction seems promising

That is powerful.

But it still leaves a second failure class untouched:

- premature closure
- false precision
- unresolved neighboring routes being collapsed too early
- cosmetic repair being presented as structural repair
- public output exceeding what has actually been earned

So Inverse Atlas appears because the success of the troubleshooting atlas revealed the next missing layer:

**governance before answer emission**. :contentReference[oaicite:3]{index=3}

---

## 3. What is the shortest way to explain it 🧩

Use this:

### Forward Atlas
Where is the failure most likely located?

### Inverse Atlas
Has the system actually earned the right to resolve that failure this strongly yet?

That is the shortest correct explanation of the difference between the two layers. :contentReference[oaicite:4]{index=4}

---

## 4. Is Inverse Atlas just a stricter prompt ❌

No.

It is not just “be more careful” rewritten in prettier language.

The framework paper is explicit that Inverse Atlas should be understood as a **governance layer**, not just a style layer. Its runtime imposes an order of operations, state modes, legality constraints, de-escalation laws, and public-ceiling control. That is why the paper describes the runtime artifact as more like a governance shell than a generic carefulness prompt. :contentReference[oaicite:5]{index=5}

---

## 5. What problem is it mainly trying to solve 🚨

The core target is not generic answer quality.

The main target is **illegitimate generation**.

That includes cases where a model:

- resolves too early
- sounds more certain than the support allows
- treats a plausible route as if it were already final
- presents cosmetic repair as structural repair
- emits public-facing conclusions beyond current support

The paper explicitly reframes many costly AI failures as failures of pre-generative legitimacy rather than only output quality defects. :contentReference[oaicite:6]{index=6}

---

## 6. What are the main legality checks 🛠️

At the public framework level, Inverse Atlas is built around a legality-first chain that includes:

- problem constitution
- world alignment
- collapse geometry or route estimation
- neighboring-cut review
- resolution authorization
- repair legality
- public emission ceiling control

These are the core structural gates described in the paper. :contentReference[oaicite:7]{index=7}

---

## 7. What are STOP, COARSE, UNRESOLVED, and AUTHORIZED 🚦

These are the four main runtime governance states.

They are not style labels.

They are legal output modes.

### STOP
The system is not currently entitled to produce substantive resolution.

### COARSE
A broad structural judgment is possible, but finer detail would overreach.

### UNRESOLVED
A leading route exists, but a nearby competing route is still materially alive.

### AUTHORIZED
The current problem frame, world alignment, route separation, and repair legality are strong enough to justify the current level of public output.

The paper explicitly treats these as governance modes rather than cosmetic answer tags. :contentReference[oaicite:8]{index=8}

---

## 8. What is “problem constitution” and why does it matter 🧱

Problem constitution is the first legality gate.

It means the system should not jump straight from raw prompt surface to detailed answer.

Instead, it should first form a minimally lawful problem frame, including:

- core conflict
- core question
- scope boundary
- key unknown

This matters because many bad answers are really bad **problem frames** in disguise. The paper explicitly argues that this stage is jurisdictional, not just interpretive. :contentReference[oaicite:9]{index=9}

---

## 9. What is “world alignment” here 🌍

World alignment here means:

is the system sufficiently coupled to the world it is about to describe

At the MVP level, the paper describes checks such as:

- evidence status
- referent stability
- target binding
- goal alignment
- claim ceiling status

This is important because a model can sound plausible while still having weak world contact. The framework treats weak alignment as a hard limiter on lawful resolution strength. :contentReference[oaicite:10]{index=10}

---

## 10. What is “neighboring-cut review” and why is it special ✂️

This is one of the signature moves of Inverse Atlas.

A leading route is not enough.

The system must also identify the nearest competing route and judge whether the leading route is actually separated enough to justify stronger closure.

That matters because a lot of false certainty is not random nonsense.
It is locally plausible overcommitment inside a contested region.

The paper explicitly treats preserved ambiguity here as disciplined governance, not embarrassment. :contentReference[oaicite:11]{index=11}

---

## 11. What is “repair legality” 🔧

Repair legality asks a harder question than “did the answer sound helpful?”

It asks:

**did the proposed fix actually touch the broken invariant, or did it only improve the surface**

The paper distinguishes:

- structural repair
- tentative repair
- cosmetic-only repair

This is one of the most valuable parts of the framework, because fake repair is one of the most expensive and misleading AI behaviors. :contentReference[oaicite:12]{index=12}

---

## 12. What is “public emission ceiling” 📏

Public emission ceiling means:

**the final visible answer should never be stronger than what the earlier legality checks have actually earned**

This is one of the core asymmetries of the framework.

A model may hold a provisional internal route.

But that does not automatically mean it is allowed to publicly emit that route as if it were final.

The paper treats public restraint as a positive runtime behavior rather than a failure of confidence. :contentReference[oaicite:13]{index=13}

---

## 13. Does Inverse Atlas replace the forward Atlas ❌

No.

The paper is very clear on this point.

Inverse Atlas is designed to **complement** a forward troubleshooting atlas, not replace it.

The forward layer is route-first and map-first.

The inverse layer is legitimacy-first and authorization-first.

One gives the map.
The other governs the right to speak from within the map. :contentReference[oaicite:14]{index=14}

---

## 14. What is Twin Atlas then 🪞

Twin Atlas is the paired architecture view.

It means:

- the forward Atlas is one wing
- Inverse Atlas is the other wing
- together they form the current family-level architecture of WFGY 4.0
- the future Bridge layer belongs inside that shared architecture

So Twin Atlas is not “yet another atlas.”
It is the family frame that explains why the two lines belong together.

---

## 15. What is Bridge supposed to do 🌉

Bridge is the internal handoff layer inside Twin Atlas.

Its job is to help the system decide how route priors and legitimacy judgments should talk to each other.

In short:

- the forward side offers orientation
- the inverse side governs authorization
- Bridge handles handoff discipline between them

The paper already establishes the logic for this asymmetry by stating that the forward layer may inform the inverse layer through weak priors, but not directly authorize public output. :contentReference[oaicite:15]{index=15}

---

## 16. Why does the forward side only count as a weak prior 🔐

Because route suggestion and lawful authorization are not the same act.

The paper explicitly says that the forward layer can accelerate structural orientation, but it does not dominate the inverse layer.
The inverse side keeps the right to downgrade, preserve ambiguity, remain coarse, reject repair finality, or stop entirely.

This is one of the most important architectural laws of the whole system. :contentReference[oaicite:16]{index=16}

---

## 17. What artifacts already exist in the MVP 📦

At the current MVP stage, the paper already identifies a real artifact layer, including:

- deployable runtime prompt
- structured output contract
- evaluator artifact
- demo harness
- minimal case pack

That is why Inverse Atlas is already more than a conceptual proposal. It already has a public-layer operational object. :contentReference[oaicite:17]{index=17}

---

## 18. Why do you have Basic, Advanced, and Strict versions 🎛️

Because different users want different balances between friction and discipline.

### Basic
For easy daily use and lower-friction onboarding.

### Advanced
The most balanced public default.

### Strict
For audit, research, and hard pressure testing.

This version strategy is product-facing, not accidental.  
It helps the framework become usable without collapsing everything into one rigid surface.

---

## 19. Which version should I use first 🌟

For most serious users:

**start with Advanced**

That is the best current default.

Use Basic if you want the easiest entry.

Use Strict if you are doing audit, benchmark-style comparison, or hard legality testing.

---

## 20. What does the 60-second reproduction actually prove ⏱️

It does not prove everything.

Its job is much narrower:

**make the first contrast visible**

It is a product-facing reproduction path that lets a person compare:

- one ordinary answer
- one inverse-governed answer

and see whether the governed version is better at:

- refusing illegal escalation
- staying coarse or unresolved lawfully
- avoiding fake repair inflation
- keeping confidence under the lawful ceiling

So it is a first demonstration surface, not the final empirical story.

---

## 21. Why is evaluator mode important ⚖️

Because a strong-looking answer can still be less lawful than a restrained answer.

The paper explicitly introduces the evaluator artifact so that candidate outputs can be judged on legality-oriented dimensions, such as:

- problem-frame legality
- neighboring-cut honesty
- resolution discipline
- repair legality
- public-ceiling compliance

That is what lets the framework be criticized and audited rather than only admired. :contentReference[oaicite:18]{index=18}

---

## 22. What does the experiments layer actually test 🧪

It does not mainly test generic fluency.

It mainly tests whether the framework reduces the kinds of illegitimate-generation behaviors it was designed to regulate.

Current high-value pressure areas include:

- illegal resolution escalation
- false structural closure
- cosmetic repair pretending to be substantive repair
- public output that exceeds what has been lawfully earned

This is exactly the legality-centered evaluation philosophy described in the paper. :contentReference[oaicite:19]{index=19}

---

## 23. What are the main experiment groups 📊

Right now, the most meaningful MVP comparison lines are:

### A
Baseline direct answering

### B
Inverse-only

### D
Forward plus inverse

And one rule must stay explicit:

**forward output is a weak prior, not an authorization source**

That rule is what keeps the dual-layer architecture honest.

---

## 24. What phases do the current experiments use 🧱

The current MVP structure is organized into three main layers:

- Smoke Phase
- Core Stress Phase
- Long-Context Phase

That split exists because not all failures appear at the same difficulty level.

Some show up immediately.

Some only become visible under stronger ambiguity, route contestability, fake repair pressure, or long-context contamination.

---

## 25. Do I need to run Colab to understand the project 💻

No.

Colab should be understood as a **reproduction tool**, not as the only path to understanding.

The repo itself should already make clear:

- what the framework is
- how the phases work
- what current findings are
- what expected patterns are
- what the honesty boundary is

Colab is useful because it makes public reproduction easier.

But it is not required in order to understand the architecture.

---

## 26. So what should Colab do then 🧪

The cleanest role for Colab is:

- help users choose a version
- run a quick baseline vs inverse comparison
- reproduce a representative case
- inspect result shape more easily

It should make reproduction easier.

It should not replace clear documentation.

---

## 27. Can you show expected results without pretending they are already proven 📐

Yes, but only if you separate them clearly.

A good public structure is:

### Current findings
What has already been seen in dry runs, MVP comparisons, or artifact-level testing.

### Expected patterns
What the framework is designed to show if reproduction is run properly.

These two categories must not be mixed.

That separation is part of the framework’s honesty layer.

---

## 28. What are the current findings, in the safest form ✅

The safest current reading is:

- the inverse layer already appears to suppress a meaningful class of expensive illegitimate-generation behaviors
- the inverse-only group already appears strong enough to show that the legality gate is doing real work
- the forward-plus-inverse direction appears stronger still, provided the weak-prior rule is preserved
- the current evidence is MVP-stage and dry-run-centered, not yet the same thing as large-scale external validation

That is strong, but still honest.

---

## 29. What does Inverse Atlas not yet claim ⛔

It does **not** currently claim that:

- the full Bridge layer is already complete
- the full WFGY 4.0 closed-loop system is already complete
- universal benchmark superiority is already proven
- every model family has already been fully tested
- the MVP already equals a final production operating system
- all hallucination problems are universally solved

Those stronger claims belong to later layers, not to the current MVP.

---

## 30. Why does the paper matter if the repo already has the artifacts 📄

Because the paper gives the framework public theoretical shape.

The repo gives you the operating surface:

- runtime
- demo
- evaluator
- case pack
- docs

The paper gives you the explanatory surface:

- reframing
- legality chain
- state modes
- dual-layer logic
- artifact design
- evaluation philosophy
- honesty boundary

Together, they make the line much easier to inspect, discuss, and extend. :contentReference[oaicite:20]{index=20}

---

## 31. Is this trying to become a benchmark, a product, or a framework 📚

Right now, it is all three at different layers.

### As a framework
It gives a new way to think about pre-generative legitimacy.

### As a product line
It already exists as a usable MVP artifact family.

### As an evaluation seed
It already has the beginning of a legality-centered experiments layer.

So the clean answer is:

**it is a framework with a product-facing MVP and a benchmark seed**

---

## 32. What is the single most important idea to remember 🌱

This one:

**The real question is no longer only whether a model can answer.  
It is whether the model has earned the right to answer at the requested level of resolution.**

That is the central shift of the whole Inverse Atlas line. :contentReference[oaicite:21]{index=21}

---

## Recommended reading order 📚

If you are new, use this order:

1. read the [Inverse Atlas README](./README.md)
2. read this FAQ page
3. read the [Versions](./versions.md)
4. read the [Quick Start](./quickstart.md)
5. read the [Runtime Guide](./runtime-guide.md)
6. read the [Experiments](./experiments/README.md)
7. read the [Status and Boundaries](./status-and-boundaries.md)
8. then continue to [Twin Atlas](../Twin_Atlas/README.md)

---

## Final Note 🌌

Inverse Atlas exists because route-first troubleshooting turned out to be useful enough to reveal the next missing layer.

Once you can map the likely failure region better, the next question becomes unavoidable:

**what gives the system the right to speak strongly from within that map**

That is the problem Inverse Atlas is trying to solve.

And that is why it is not just a side feature.

It is the legitimacy-first half of a much larger architecture.
