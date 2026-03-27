<!--
AI_NOTE_START

Document role:
This page is the figure index and figure-guidance entry for WFGY 4.0 Twin Atlas Engine.

What this page is for:
1. Give the Twin Atlas figure folder a clear public entry point.
2. Explain what kinds of figures belong here.
3. Help readers understand how the architecture should be visualized.
4. Provide a clean navigation layer for future diagrams, figure notes, and visual explainers.

How to use this page:
1. Read this page if you want the visual map of Twin Atlas.
2. Use it to navigate to architecture figures, state figures, and future demo-support visuals.
3. Treat it as the figure-layer entry point, not as a replacement for the formal architecture docs.
4. Use it as the style and organization guide for future Twin Atlas diagrams.

Important boundary:
This page organizes the public figure layer only.
It does not expose hidden internal reasoning substrate details.
It also does not claim that every future figure is already complete.
Its job is to make the visual layer legible, navigable, and aligned with the public effective layer.

Recommended reading path:
1. Twin Atlas README
2. Runtime README
3. Bridge README
4. Demos README
5. This page
6. individual figure pages

AI_NOTE_END
-->

# 🖼️ Figures

> The visual layer for WFGY 4.0 Twin Atlas Engine.

Twin Atlas is a system that benefits a lot from visual explanation.

Why:

- there are multiple layers
- there is a forward side and an inverse side
- there is a coupling layer in between
- there is a visible-output discipline at the end
- there are state and boundary ideas that are easier to see than to describe

That means the figure layer is not decoration.

It is part of the public understanding surface.

This folder exists to keep that visual layer organized.

---

## 🔎 Quick Links

| Section | Link |
|---|---|
| Twin Atlas Home | [Twin Atlas](../README.md) |
| FAQ | [FAQ](../faq.md) |
| Roadmap | [Roadmap](../roadmap.md) |
| Release Notes | [Release Notes](../release-notes.md) |
| Bridge Home | [Bridge README](../Bridge/README.md) |
| Runtime Home | [Runtime README](../runtime/README.md) |
| Coupling Flow | [Twin Atlas Coupling Flow](../runtime/twin-atlas-coupling-flow.md) |
| Demos Home | [Demos README](../demos/README.md) |
| Killer Demo Spec | [Killer Demo Spec](../demos/killer-demo-spec.md) |
| Forward Atlas | [Problem Map 3.0 Troubleshooting Atlas](../../wfgy-ai-problem-map-troubleshooting-atlas.md) |
| Inverse Atlas Home | [Inverse Atlas README](../../Inverse_Atlas/README.md) |
| Inverse Atlas Figures | [Inverse Atlas Figure Notes](../../Inverse_Atlas/figures/README.md) |

---

## ⚡ The shortest version

If you only remember one thing, remember this:

**the figure layer exists to make Twin Atlas legible at a glance.**

Twin Atlas is not just one paragraph of philosophy.  
It is an architecture with:

- a forward map layer
- a bridge handoff layer
- an inverse authorization layer
- a visible answer layer
- a runtime ladder
- a demo proof surface

Some of that is easiest to understand visually.

That is why this folder matters.

---

# 🧭 Section 1 · What belongs in this folder

This folder should contain figures that directly explain the public effective layer of Twin Atlas.

That includes figures for:

### 🗺️ Architecture
The overall shape of the engine.

### 🌉 Coupling
How Forward Atlas, Bridge, and Inverse Atlas connect.

### 🔐 State and boundary logic
How visible output should be constrained by support and authorization.

### ⚙️ Runtime layer
How Basic, Advanced, and Strict relate to the same underlying flow.

### 🎭 Demo support visuals
Side-by-side contrast diagrams, proof-surface diagrams, or case summary visuals.

This folder should not become a random image dump.

It should stay tightly tied to the Twin Atlas architecture.

---

# 🧱 Section 2 · What this visual layer should help explain

Twin Atlas becomes easier to understand when readers can quickly see:

### 1. Forward vs Inverse are not duplicates
One maps likely structural route.  
One governs whether stronger visible output is lawful.

### 2. Bridge is an internal handoff layer
Bridge is not a third final judge.  
It is a disciplined coupling layer.

### 3. Visible output is not the same as internal route value
A plausible route is not automatically an authorized conclusion.

### 4. The runtime ladder is one engine, not three unrelated products
Basic, Advanced, and Strict should look like three intensity levels of one architecture.

### 5. Demo contrasts are structural, not cosmetic
Twin Atlas should visually read as:
- more lawful under uncertainty
- less fake-final
- safer on the first move

These are exactly the kinds of things figures are good at.

---

# 🗂️ Section 3 · Recommended figure categories

This is the recommended structure for the figure layer.

## Category A · Core architecture figures
These should answer:

- what is Twin Atlas
- what are its major layers
- how do those layers relate

Recommended figures:
- Twin Atlas high-level architecture
- Forward / Bridge / Inverse stack
- public effective-layer overview

---

## Category B · Coupling figures
These should answer:

- how does route value move forward
- where does Bridge sit
- where does authorization happen
- where is visible answer strength clamped

Recommended figures:
- minimal coupling flow diagram
- handoff discipline diagram
- route-prior vs authorization distinction diagram

---

## Category C · State and boundary figures
These should answer:

- what kinds of visible answer states exist
- what blocks stronger visible force
- what lawful unresolvedness looks like

Recommended figures:
- visible-state ladder
- boundary-pressure diagram
- support-bounded output diagram

---

## Category D · Runtime figures
These should answer:

- why there are three runtime modes
- how Basic, Advanced, and Strict relate
- how governance intensity scales

Recommended figures:
- runtime ladder
- governance-intensity comparison diagram
- mode-selection map

---

## Category E · Demo support figures
These should answer:

- how baseline differs from Twin Atlas
- where the contrast lives
- why the difference matters

Recommended figures:
- baseline vs Twin Atlas contrast board
- Case 01 summary figure
- one-screen proof surface figure

---

# 🎯 Section 4 · Recommended first figure set

If the public figure layer is being built in stages, the best first batch is probably this:

## Figure 01
**Twin Atlas high-level architecture**

Purpose:
Show the top-level relationship between:
- Forward Atlas
- Bridge
- Inverse Atlas
- visible output

This is the most important first figure.

---

## Figure 02
**Twin Atlas coupling flow**

Purpose:
Show the minimal flow:

- case intake
- forward route construction
- bridge translation
- inverse authorization
- visible output clamping
- public answer

This should match the coupling-flow page.

---

## Figure 03
**Runtime ladder**

Purpose:
Show that:
- Basic
- Advanced
- Strict

are three governance intensities of the same engine, not three unrelated tools.

---

## Figure 04
**Demo contrast board**

Purpose:
Show baseline vs Twin Atlas in one visible frame.

This is especially useful for public release and social-proof surfaces.

---

## Figure 05
**Visible-state / support-boundary figure**

Purpose:
Show that visible answer strength should remain bounded by support and route separation quality.

This is one of the most distinctive Twin Atlas ideas.

---

# 🎨 Section 5 · Figure style guide

Twin Atlas figures should follow a style that matches the architecture.

## Preferred style
- clean
- academic but not sterile
- minimal
- dark text on light background
- strong visual hierarchy
- high conceptual clarity
- desktop-friendly
- GitHub-friendly

## Good figure qualities
- easy to read at a glance
- not overloaded
- labels are meaningful
- arrows show logic, not decoration
- components are clearly separated
- tension between layers is visible when relevant

## Avoid
- excessive glow
- gaming-style chaos
- decorative icons that add no meaning
- overly marketing-looking “AI magic” styling
- overly dense unreadable blocks
- diagrams that only look good on mobile but become ugly on desktop

The figure layer should make the architecture clearer, not flashier.

---

# 💻 Section 6 · GitHub readability rules

Because this repo is mostly read on GitHub, the visual layer should stay GitHub-friendly.

That means:

### ✅ Good
- simple diagrams
- clean labels
- readable at laptop scale
- strong spacing
- balanced width
- useful captions
- text references from README to figure pages

### ❌ Bad
- hyper-narrow mobile-first layouts
- tiny unreadable labels
- giant decorative banners with no structure
- screenshots with no explanation
- diagrams that only make sense if someone already understands the system

The figures should support first-time understanding.

---

# 🧠 Section 7 · Relationship to the architecture docs

The figure layer is not a replacement for the written architecture.

It is a companion layer.

That means:

- README explains the engine in text
- Bridge docs explain the coupling in detail
- runtime docs explain public usage
- demo docs explain visible proof
- figures make the structure legible faster

A strong figure should reduce explanation cost, not replace all explanation.

---

# 🌉 Section 8 · Relationship to Bridge and runtime

Bridge and runtime are the two areas where figures matter most.

## For Bridge
Figures should help explain:
- advisory-only handoff
- weak priors vs authorization
- what must be preserved
- what must never be upgraded

## For runtime
Figures should help explain:
- mode differences
- governance intensity ladder
- same engine, different strictness
- coupling flow staying underneath all three modes

If the figure layer does this well, many readers will understand Twin Atlas much faster.

---

# 🎭 Section 9 · Relationship to demos

The demo layer and figure layer should support each other.

That means:

- demo pages provide detailed narrative and evaluation posture
- figures provide one-screen contrast and orientation

For example:

### Demo pages show
- what the case is
- why baseline fails
- why Twin Atlas behaves differently

### Figures show
- where the contrast lives
- which layer makes the difference
- why the result is structural, not stylistic

That is a strong division of labor.

---

# ✅ Section 10 · What is already fair to say

At the current stage, these statements are fair:

- Twin Atlas already benefits from a dedicated figure layer
- the architecture is already structured enough to support meaningful figures
- the first figure set can already be defined even if not every visual is finished yet
- figures will likely make the public layer much easier to understand
- the visual layer now belongs to the public Twin Atlas stack, not just to future polish work

These are strong statements, but still honest.

---

# 🚧 Section 11 · What should not yet be claimed

This page should not be used to claim that:

- every future Twin Atlas figure is already finished
- every visual state and transition is already fully formalized
- the figure layer is complete in every design detail
- the visual layer replaces the formal architecture docs
- all hidden internal substrate logic is intended to appear in diagrams

The figure layer is public and useful.

It is not the total internal blueprint.

---

# 🧡 Section 12 · A vibe-coder-friendly summary

If you want the fast version:

### README
tells you what Twin Atlas is

### Bridge docs
tell you how the handoff works

### Runtime docs
tell you how to use it

### Demo docs
show you why it matters

### Figures
make the whole thing easier to see in one glance

That is the figure layer.

---

# 🚀 Suggested next read

After this page, the most useful next files are:

1. [Twin Atlas Coupling Flow](../runtime/twin-atlas-coupling-flow.md)
2. [Runtime Mode Notes](../runtime/runtime-mode-notes.md)
3. [Bridge README](../Bridge/README.md)
4. [Demos README](../demos/README.md)

That sequence moves from architecture, to flow, to usage, to proof surface.

---

# ✨ One-sentence takeaway

> The figure layer exists to make Twin Atlas visually legible as an engine, so readers can understand the architecture, coupling, runtime ladder, and proof surface faster than text alone.

