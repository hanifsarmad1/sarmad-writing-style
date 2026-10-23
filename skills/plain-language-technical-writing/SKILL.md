---
name: plain-language-technical-writing
description: Write explanatory technical prose a newcomer can follow without a glossary - lecture slides, course notes, handouts, tutorials, READMEs, and design docs. Use when defining a term, motivating a method, walking through a worked example, or explaining why a model is built the way it is. Keeps text concrete, honest about assumptions, and reproducible.
license: MIT
metadata: {"version": "1.0", "origin": "distribution_system_course writing-style skill, generalized"}
---

# Plain-language technical writing

For prose whose job is to make a reader *understand*, not to convince a reviewer. Slides,
course notes, tutorials, onboarding docs, design rationale.

For manuscripts and reviewed publications, use `scientific-writing`. For slide *structure
and timing*, use `scientific-slides`.

## The seven habits

1. **Define before you use.** Every term or metric gets a one-line definition *with units*
   the first time it appears. "Demand is the average power over a stated averaging window
   (kW)" — not just "demand."
2. **Show the numbers.** A worked example carries real figures from start to finish. Never
   "it can be shown," never a formula with nothing plugged in. If you introduce a ratio,
   compute it once with actual inputs so the reader sees the size of the answer.
3. **Separate observation from interpretation.** First state what the data or equation
   shows; then, as a *separate sentence*, what it means. Do not weld the measurement and
   the conclusion into one clause.
4. **State assumptions and limits out loud.** Each method names what it assumes and where
   it breaks. "Allocation by transformer size assumes every unit is loaded equally hard —
   false, but rarely disastrous" is the model to follow.
5. **Make it reproducible.** Say where a number came from and how a reader could recompute
   it: the dataset, the equation, the command, or a back-reference. A figure a reader
   cannot trace is a figure they cannot trust.
6. **Pin quantities to each other.** When several numbers are related, write the
   relationship explicitly — `enrolled ≤ achievable ≤ technical`, or `F_C = 1/F_D`.
   Nesting and reciprocals stated in symbols prevent the confusion that similar-sounding
   names create.
7. **Land on a sentence a practitioner could say aloud.** End a hard passage with the
   plain-English takeaway — the one line someone would actually use in a meeting.

## Grounding

A reader can only follow a passage if every concept it leans on is already **grounded**:
either they walked in with it, or an earlier passage established it. The unit is the
concept, not the word — you can lose a reader with no jargon in sight.

Two levers, and they trade off:

- **Prerequisite** — assumed known. Demand too much and you shut readers out.
- **Introduced** — established in the text. Ground too much and the opening drowns in
  definitions.

Decide explicitly who the reader is before drafting, then keep a running list of what is
grounded. When a passage needs an ungrounded concept, that concept *is* the next thing to
write.

## Mechanics

- Expand every acronym on first use. After that, the acronym alone.
- A unit on every quantity.
- Short declarative sentences, one idea each. Prefer the active voice.
- **Physical intuition before mathematics.** Put the picture, the field fact, or the
  concrete case first; the formalism second.
- Introduce one symbol at a time. Do not stack three new notations in one display.
- Prefer a concrete example over an abstract statement of the same thing. If you need
  both, the example goes first.
- One quantitative example threaded across several pages beats a fresh set of numbers per
  page — the reader tracks one story.

## Anti-patterns — rewrite these on sight

- Jargon with no definition.
- "Obviously," "clearly," "it is easy to see," "simply," "just."
- A number with no unit, or no traceable source.
- Claim and evidence fused into one sentence ("the smooth curve proves coincidence").
- An assumption left implicit — especially a simplification carried silently into a
  context that violates it.
- A derivation with no worked number to anchor its scale.
- A sentence that only makes sense if you already know the answer.

## Quick check before shipping

- [ ] Could a reader who has never seen this topic follow it end to end?
- [ ] Does every symbol and acronym get introduced before it is used?
- [ ] Is there at least one fully worked number?
- [ ] Are the assumptions written down where the method is introduced?
- [ ] Is there a say-aloud takeaway at the end of each hard passage?
