# Open Experiments Board

This page is a lightweight coordination board for the Tension Universe MVP experiment layer.

Its purpose is practical:

- show which Tension Universe experiment pages already exist
- show where the current published MVP work can be reviewed
- clarify how contributors should choose the next experiment target
- help the 131-problem field expand one page at a time without duplicate work

This board is intentionally operational.

It is not a full theory index.
It is not a fake placeholder registry.
It is a working contribution board for real MVP pages under `TensionUniverse/Experiments/`.

## What this page means

The Tension Universe field points toward 131 problems in total.

However, this board does **not** list all 131 items up front with placeholder entries.

Instead, it does something simpler and more useful:

- it shows which MVP experiments are already published
- it points contributors to the current experiment collection
- it makes it clear that the next clean contribution is to choose a **valid unbuilt problem** that is not already covered

So the contribution logic is:

- if a problem already has a published MVP page, do not duplicate it unless you are proposing a scoped extension
- if a problem is valid and does not yet have a published MVP page, it is a candidate for the next contribution
- if sequencing matters, the maintainer may explicitly reserve certain items later

## Current published MVP set

At the moment, **10 Tension Universe MVP experiments are already published**.

These are the currently visible completed experiment pages:

- [TU Q091](../Experiments/Q091_MVP/README.md)
- [TU Q098](../Experiments/Q098_MVP/README.md)
- [TU Q101](../Experiments/Q101_MVP/README.md)
- [TU Q105](../Experiments/Q105_MVP/README.md)
- [TU Q106](../Experiments/Q106_MVP/README.md)
- [TU Q108](../Experiments/Q108_MVP/README.md)
- [TU Q121](../Experiments/Q121_MVP/README.md)
- [TU Q124](../Experiments/Q124_MVP/README.md)
- [TU Q127](../Experiments/Q127_MVP/README.md)
- [TU Q130](../Experiments/Q130_MVP/README.md)

If you want the current published set, the cleanest place to review it is:

- [Tension Universe experiment index](../Experiments/README.md)

That index is the actual source of truth for what already exists.

## What contributors should do next

If you want to help expand the experiment layer, the rule is simple:

**Do not start from the already completed items above.**
Start from another valid Tension Universe problem that does not yet have a published MVP page.

In practice, that means:

1. check the published experiment index first
2. confirm your target problem is not already covered
3. choose a valid Tension Universe problem outside the completed set
4. build one small, inspectable MVP page
5. submit a focused issue or PR

This keeps the board useful and prevents duplicate work.

## Where to check before building

Before you start, review these pages:

- [Tension Universe experiment index](../Experiments/README.md)
- [Contribution guide](./README.md)
- [Contributor credit format](./contributor-credit-format.md)

These links are enough to confirm:

- what already exists
- how MVP pages should be structured
- how contributor credit should be recorded

## Contribution scope

The expected contribution target is still small and strict.

A clean MVP contribution should usually be:

- one valid problem id
- one focused experiment folder
- one main `README.md`
- optional notebook, screenshots, or Colab link only if they directly support the page

The intended home is:

`TensionUniverse/Experiments/`

The preferred pattern is:

`TensionUniverse/Experiments/QXXX_MVP/README.md`

Here, `QXXX` is only a formatting template.
It is **not** a real problem id by itself.
Replace it with a valid Tension Universe problem number before creating the page.

## Status model

This board uses a small practical status model.

- `Completed`  
  A visible MVP page already exists in `TensionUniverse/Experiments/`.

- `In Progress`  
  A real experiment page is being drafted, revised, or expanded, but is not yet ready to be treated as a stable published MVP.

- `Open`  
  A valid problem has no published MVP page yet and is available for contribution.

- `Reserved by Maintainer`  
  A valid problem is intentionally held for sequencing, dependency, or release-planning reasons.

These labels are only for coordination.
They do not imply final scientific completion.

## Example entry format

If this board later tracks individual items more explicitly, each entry should use a compact real-id format like this:

## TU QXXX

Status: Open  
Title: Replace with the real working title  
Path: `TensionUniverse/Experiments/QXXX_MVP/README.md`  
Scope: One page MVP  
Difficulty: Easy / Medium / Hard  
Claim: One sentence describing what the experiment is testing.  
Claimed by: Unassigned / Maintainer / Contributor name

Important:

`QXXX` in this example is a template token only.
It is not a real listed Tension Universe problem unless replaced with a valid id.

## Practical rules

Before starting a new experiment, keep these rules in mind:

1. The page must map to a valid Tension Universe problem id.
2. Do not duplicate the already published completed set unless the work is a clearly scoped extension.
3. Keep the contribution inside MVP experiment scope.
4. The cleanest contribution is one folder plus one main `README.md`.
5. Small notebooks, screenshots, and Colab links are welcome when they directly support the MVP.
6. Avoid large unrelated edits outside the target experiment.

## Fastest clean path

If you want the fastest contribution path:

1. open the published experiment index
2. pick a valid problem that is not already completed
3. create `TensionUniverse/Experiments/QXXX_MVP/README.md`
4. keep the scope narrow and inspectable
5. submit a focused PR

One real page is better than a large unfinished dump.

## How this board should grow

This board does not need 131 placeholder entries on day one.

A cleaner long-term pattern is:

- keep the published experiment index updated as real pages are added
- use this board to clarify current contribution logic
- add explicit `In Progress` or `Reserved` entries only when they refer to real problem ids
- continue opening new ground by building valid unclaimed problems outside the completed set

That keeps the page readable, accurate, and useful.

## If you want to start now

Start by checking the completed set first.

If your target is already listed, pick another valid problem.

If your target is not yet built, keep the scope small, make one inspectable MVP page, and open a focused PR.

That is the cleanest way to expand the Tension Universe experiment layer.
