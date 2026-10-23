---
name: house-voice
description: Use when drafting or revising explanatory prose for slides, course notes, handouts, READMEs, design docs, or papers, and when structuring a lecture deck or an individual slide. Also use when ordering the frames of a derivation, deciding where notation goes, presenting a result that should be derived instead, when a draft reads like generic AI output, or when titles have grown long and descriptive.
---

# House voice

Two rules underneath all of it.

**The page carries what is hard to say aloud; the speaker says what is easy to say aloud.**
Numbers, units, matrices, sources, and geometry go on the page because a listener cannot hold
them. Connective narrative stays in the mouth.

**The reader should be able to rebuild the result from the page alone.** Define the symbol
before using it, show the arithmetic rather than the answer, and say which assumption bought
each step. A slide that only reports a result is a slide the reader has to take on trust.

Every other convention here follows from those two.

This skill governs *voice, format, and structure*. It does not govern *content discipline* -
see `plain-language-technical-writing` for the grounding model (define with units, show the
numbers, separate observation from interpretation, state assumptions). The two are meant to
be loaded together. Where a project-scope style skill exists, that skill wins.

## Evidence base

Measured over weeks 1-4 of the distribution systems decks, 130,206 characters of body text:

| Measure | Value |
|---|---|
| Frame titles | 88, mean 4.1 words, **never over 8** |
| Frames built around a figure, table, or display equation | 75 of 88 |
| Frames closing with `takeaway` / `fieldanchor` / `validation` | 43 of 88 |
| Frames opening with a small-type lead-in | 33 of 88 |
| Frames laid out in two columns | 39 of 88 |
| Muted symbol-gloss lines under equations | 36 |
| Appendix frames in the one full derivation week | 5 |
| Hits against 48 common cliche and filler terms | **0** |
| Prose exclamation marks | **0** |
| `---` used as a trailing gloss vs. an interrupting pair | 136 vs. 7 |

These are not aspirations. They are what the corpus already does.

## Titles

Short, plain, lowercase after the first word. A title **names the object or poses the
question**; the slide body answers it. A title that states the conclusion has spent the
payoff before the reader arrives.

**Hard limits.** Four words is the target. Six is the ceiling. Sentence case, not Title
Case. No terminal period. **No dash of any kind inside a title.**

A step label, a part number, or a section number is not part of the title. It goes in the
muted lead-in line inside the frame, together with the rest of the scope-setting.

Eight patterns cover the good titles in the corpus:

| Pattern | Real examples |
|---|---|
| Bare noun phrase | `Notation` · `Typical ratings` · `Voltage drop` · `Sequence components` |
| Hanging what/why/where clause | `What a phasor is` · `Why complex power carries a conjugate` · `Where the voltage-drop rule comes from` |
| Direct question, for a decision moment | `So how big a transformer?` |
| Declarative, only when the point is a correction | `Peaks do not line up` · `The fundamentals are not academic` |
| X versus Y, or a list of three | `A net versus a tree` · `Radial, looped, networked` |
| Bare step name, no gloss | `Modified Carson` · `Kron reduction` · `Earth return` |
| Appositive after a comma | `The power system, end to end` · `Four numbers, one at a time` |
| `Reading <artifact>`, for interpret-the-output slides | `Reading $\Zprim$` · `Reading $\zabc^{601}$` |

**Rewrite these on sight:**

| Instead of | Write |
|---|---|
| `Introduction to Load Allocation Methods` | `Load Allocation` |
| `Understanding Diversity and Coincidence Factors in Distribution Planning` | `Diversity and coincidence` |
| `An Overview of RMS and Its Relationship to Peak Voltage` | `What the $\sqrt2$ does` |
| `Key Takeaways from Carson's Equations` | `Modified Carson` |
| `Step 3a --- earth return` | `Earth return` |
| `Validation --- two different claims, two different tolerances` | `Two claims, two tolerances` |
| `Exploring How Transformer Sizing Depends on Coincidence` | `So how big a transformer?` |

Banned title constructions: `Introduction to ...`, `Overview of ...`, `Understanding ...`,
`Exploring ...`, `A Deep Dive into ...`, `Key Takeaways ...`, any dash, any colon, and
Title Case of any kind except acronyms and proper nouns.

## The page is not the script

Build the slide around an **artifact** - a drawing, a chart, a table, or a display
equation - and let the prose point at it. Roughly six in seven slides should have one.

Prose on the page earns its place by being one of:

- a **number with a unit** the listener could not retain
- a **definition** stated once, with units
- a **symbol glossary** in muted small type under an equation
- a **source line** so the figure can be traced
- a **caption** that says what to look at and what follows from it
- the **landing sentence** in a takeaway block, which is the one place a full say-aloud
  line belongs, because it is the line the reader should leave with

Prose that does *not* earn its place, and the fix:

| Delete | Because |
|---|---|
| `In this lecture we will discuss...` | The title already said it. |
| `As we can see from the figure above...` | The reader can see. Say what follows instead. |
| `It is important to note that...` | If it were not important it would not be on the slide. |
| `Let us now explore...` | Narration of the act of teaching, not teaching. |
| `This slide shows...` | So does every slide. |

**Before**

> In this section, we will explore the important concept of the coincidence factor and
> understand how it fundamentally impacts transformer sizing decisions in distribution
> planning. As we can see, the coincidence factor is a crucial parameter.

**After**

> Two engineers size the same transformer. A adds the individual peaks:
> $27.0/0.95 = 28.4$ kVA, so 37.5 kVA. B applies the coincidence factor:
> $27.0 \times 0.60 / 0.95 = 17.1$ kVA, so 25 kVA - one size smaller.
>
> B is right, and the saving repeats across every transformer the utility owns.

Two named actors, real arithmetic carried end to end, a verdict. No narration.

## Deck spine

A derivation deck runs in this order. Announce the topics once, in the contract table, so a
reader who looks up mid-lecture can find where they are.

**Topics, not steps (user direction, Oct 2026).** Weeks 1-4 numbered their steps
(`Step 3b`). From Week 5 on, no step numbers appear in titles, lead-ins, or tables: the
contract lists topics, and each frame is titled with its topic.

| # | Frame | Job |
|---|---|---|
| 1 | `Where we are` | Roadmap graphic plus one muted line of scope |
| 2 | `Today` | The **contract**: a table of the topics, with Input and Output columns |
| 3 | `Notation` | Every symbol, grouped by the topic that introduces it |
| 4 | The concrete object | The specific feeder, config, or dataset the whole deck works on |
| 5 | Derivation | One frame per topic, titled with the topic: `Modified Carson` |
| 6 | `Reading <artifact>` | A whole frame spent interpreting what was just built |
| 7 | The worked result | The named case, checked against a published number |
| 8 | The second pass | Same steps, new geometry, so the method reads as a method |
| 9 | Comparison | Both results in one table, one row per quantity |
| 10 | Stress test | Where the standard shortcut quietly fails |
| 11 | Tool check | The engine reproducing the hand derivation |
| 12 | `HW N` | What the student runs the same steps on |
| 13 | `Next` | Reading plus a one-line preview of the following week |
| 14 | `\appendix` | Glossary, the algebra deferred out of the main line, and the experiments |

**Experiments go to a notebook and the appendix.** Parameter sweeps, light-load cases,
daily (chronological) runs, and exercises are run in a committed notebook; the slides that
report them sit in the appendix, each lead-in naming the notebook part. The main line
derives and reads, then stops at `Next`.

Three of these carry most of the weight:

- **The contract slide.** Week 4 opens with a four-row table: Step, Action, Input, Output.
  The reader can see the whole machine before the first equation. It also says what the
  steps do *not* need: "No load, no voltage, no direction of power flow enters these steps."
- **The second pass.** Deriving once shows a result. Deriving twice shows a method. Bridge
  the two with a diff table that holds the shared part fixed - Week 4's marks Step 3 as
  "identical --- same two equations" while Steps 1, 2, and 4 change.
- **The appendix.** Five frames in Week 4: `Glossary`, `Carson's constants`,
  `The $S_{ij}$ cancellation`, `Computing $\GMR$`, `The tape-shielded cable`. Heavy algebra
  lives here so the main line stays walkable, and the main slide points at it by name.

## Slide anatomy

Five slots, always in this order. Not every slide fills all five.

| Slot | Form | Frequency in weeks 1-4 |
|---|---|---|
| 1. Title | Names the object or poses the question | 88 of 88 |
| 2. Lead-in | One or two sentences: what is about to happen, and why | 33 of 88 |
| 3. Artifact | Drawing, chart, table, or display equation | 75 of 88 |
| 4. Gloss and reading | Muted symbol definitions, then bolded lead-in bullets | 36 gloss, 28 bullets |
| 5. Closing block | `takeaway`, `fieldanchor`, or `validation` | 43 of 88 |

Two columns are the default when a picture is involved: picture left, words right, 39 of 88
frames. The lead-in is set small and flush so it reads as a caption rather than a paragraph.

Bullets in slot 4 open with a **bolded question or claim**, then answer it:

> - **Why all three phase diagonals are identical.** The self formula contains no position,
>   only $r_i$ and $\GMR_i$...
> - **Why the neutral diagonal is bigger.** 4/0 ACSR is a smaller conductor...
> - **Where the asymmetry lives.** Only in the off-diagonal reactances, put there by
>   $D_{ij}$ alone...

The bold phrase is the finding. The sentence after it is the mechanism. A bullet that is
one undifferentiated sentence makes the reader hunt for which part matters.

## Notation before narrative

Symbols are defined before they are used, never after, and never by context alone.

- **A dedicated `Notation` frame before the first derivation.** Group symbols by the step
  that introduces them, not alphabetically. Week 4 groups them as "The wires (Step 1)",
  "Their positions (Step 2)", "What we build (Steps 3-4)", "Acronyms".
- **Three columns: Symbol, Reads as, Units.** "Reads as" rather than "Description" - the
  column tells the reader how to pronounce the thing, which is what they actually need.
- **A muted gloss under every display equation** naming each new symbol with its unit:
  "$L$ inductance, in henries; $R$ resistance, $X=\omega L$ reactance, $Z=R+\jj X$
  impedance, all in ohms."
- **New words get their own frame before the algebra**, headed plainly. Week 4 writes
  "**New vocabulary, before any algebra.**" and then defines *strand*, *concentric*, and
  *own neutral* with a labelled cross-section next to them.
- **Repeat the local symbol table at the point of use.** The front-of-deck frame sets scope;
  the in-place table does the work. Week 4's `UG Step 1` carries its own Symbol, Means,
  Value table even though `Notation` already ran.
- **One new symbol per display.** Three new notations stacked in one equation is three
  slides compressed into one.
- **Close the deck with a `Glossary`** in the appendix. Notation appears twice: scoped at
  the front, complete at the back.
- **Expand every acronym on first use**, then use the acronym alone. Mark the letters if the
  expansion explains the name: "**a**luminum **c**onductor, **s**teel-**r**einforced".

**Before**

> Applying Carson's equations with the GMR and the spacing gives $\hat z_{ij}$, which after
> Kron reduction yields $\zabc$.

Four undefined symbols, one of them silently carrying a hat that means something.

**After**

> A **hat** always means *primitive* - before the neutral is eliminated.
>
> | Symbol | Reads as | Units |
> |---|---|---|
> | $\GMR_i$ | geometric mean radius of conductor $i$ | ft |
> | $D_{ij}$ | centre-to-centre distance, $i$ to $j$ | ft |
> | $\hat z_{ij}$ | one entry of the primitive matrix | $\Omega$/mi |

## Derive, do not present

The final matrix is the least interesting thing on the slide. Seven moves, all observable in
weeks 2 and 4:

1. **Motivate the move before making it.** Pose the need, show the candidates, eliminate.
   Week 2 does not assert that complex power takes a conjugate. It says: we want one number
   whose real part is the constant term; multiplication offers exactly two candidates; the
   plain product swings when you restart the clock, so it cannot be a property of the
   circuit. The conjugate survives by elimination, and the reader watched it happen.

2. **Carry the arithmetic in the open.** Never "it can be shown". Write the chain:

   > $\ln(1/0.0313) = 3.4641 \to {+}7.93402 = 11.3982 \to {\times}0.12134 = \mathbf{1.3831} = X$

   The reader can recompute it on a phone. That is the point.

3. **State the physical assumption that licenses the step, on its own line, in alert.**

   > **The physical assumption:** the neutral is bonded to a ground rod at every pole, so
   > its rise along the span is $\mathbf{V}_n = \mathbf{0}$.

   Then immediately guard the misreading it invites: "$\mathbf{V}_n=\mathbf{0}$ does *not*
   make $\mathbf{I}_n$ zero - it makes it dependent on the phase currents."

4. **Spend a whole frame reading the object you just built.** Build the matrix on one slide,
   then title the next one `Reading $\Zprim$` and answer four questions about its shape. A
   matrix presented and not read is a picture of an answer.

5. **Quote before and after with a percentage and a mechanism.**

   > Resistance **rose** $0.2812 \to 0.3465$ ($+23\%$): the neutral's own $I^2R$ is now
   > charged to the phases. Reactance **fell** $1.3831 \to 1.0179$ ($-26\%$): a nearby
   > return path shrinks the current loop.

6. **Run the method twice on different inputs.** Overhead, then underground. Same four
   steps, visibly the same, so the method is what the reader remembers rather than the
   numbers.

7. **Defer the heavy algebra to the appendix, and name it from the main line.** "The next
   slide shows $S_{ij}$ cancelling out - derivation in the appendix." The main sequence
   keeps moving; nothing is hidden.

Then close the loop. Derive by hand, then check against the engine or the published table,
and mark it: `\checkmark matches the published IEEE 13-bus table`. Say what the agreement
does and does not prove - "closure proves the arithmetic, not which rule is right."

## Simple English

Technical content, ordinary words. The reader is spending their attention on the physics, so
do not also charge them for the prose.

- **One idea per sentence.** "Aluminum carries the current. The steel core carries the
  mechanical load." Not one sentence with two clauses and a subordinate.
- **Say the formula in words once.** RMS is "read right to left: square, mean, root."
- **Decode notation like a part number.** `556,500 26/7 ACSR` gets a Token / Meaning table:
  area in circular mils, 26 aluminum strands over 7 steel, the acronym spelled out.
- **Translate a symbol into a spoken question.** "$P_{ij}$ answers *how many volts does
  conductor $i$ rise per unit charge on $j$?*"
- **Name the obstacle plainly before solving it.** "That is a problem: inductance needs a
  loop area, and soil is a half-space with no edge." Then Carson's trick lands as a relief
  rather than a definition.
- **Prefer the short word and the concrete verb.** A conductor *hangs*. A fuse *blows*.
  Strands are *twisted together*. Nothing is *characterized*, *comprised*, or *exhibited*.
- **Keep the register level.** No jokes, no exclamation marks, no winking at the reader. The
  material is interesting enough that decoration reads as apology.

## Punctuation: the trailing dash

The em dash is a **single trailing dash that appends**, never a pair that interrupts.

```
Lightning arrester --- sends surges to ground.
$R$ and $X$ are the same order --- real power moves voltage too.
Both are looked up, not derived --- the manufacturer publishes them.
```

Two licensed uses, and only two:

1. **Label, then gloss.** A term or part number on the left, its one-line meaning on the
   right. Common in equipment lists, glossaries, and step headings. The left side is a
   **term, not a sentence**.
2. **Statement, then consequence** --- only when the left side is a short fragment.

**If the left side of the dash is a full sentence, use a period instead.** Sentence one
states the fact; sentence two gives the mechanism, and it opens with a noun rather than a
conjunction. This is the most overused construction in generated technical prose, and it
compounds: one per slide reads as a tic rather than a style.

| Do not write | Write |
|---|---|
| `Fault currents are quoted as RMS symmetrical amperes --- the asymmetric first cycle matters for breaker duty.` | `Fault currents are quoted as RMS symmetrical amperes. The asymmetric first cycle is larger; it sizes breaker duty.` |
| `Lightning arrester --- sends surges to ground.` | *(keep: label, then gloss)* |

Budget: at most three trailing dashes per document outside tables and glossaries.

**Banned: the bracketing pair.** Two dashes fencing a parenthetical mid-sentence is the
single loudest tell of generated prose. Use commas, or split the sentence.

| Do not write | Write |
|---|---|
| `The regulator --- which has 32 steps --- covers $\pm10\%$.` | `The regulator covers $\pm10\%$ in 32 steps.` |
| `Distribution --- unlike transmission --- is radial.` | `Distribution is radial. Transmission is not.` |

Also banned: exclamation marks in prose, rhetorical questions the text does not then answer,
and scare quotes around a term instead of defining it.

## Vocabulary

Zero hits across 48 tested terms in 130k characters. Keep it that way. The list, so it is
checkable rather than a matter of taste:

```
leverage  delve  crucial  vital  robust  seamless  journey  unlock  harness
holistic  synergy  paradigm  landscape  realm  testament  pivotal  myriad
plethora  cutting-edge  revolutionize  empower  streamline  facilitate  utilize
comprehensive  powerful  significant  critical  effectively  various  numerous
basically  essentially  fundamentally  obviously  clearly  simply put
it is important to note  it is worth noting  dive into  deep dive
key takeaway  at the end of the day  as we can see  in today's ...
```

Replacements are almost always shorter and more specific: `utilize` is `use`; `facilitate`
is the verb you actually mean; `crucial` is a number showing why; `various` is the count.
`obviously` and `clearly` are never fixes - they are a reader-blaming substitute for the
missing step.

Prefer the field's own word over the general one. A conductor **hangs**; a fuse **blows** and
**swings open**; a recloser **trips** and **re-closes**; a transformer **runs hot**, **ages**,
and **fails**. Concrete hardware verbs do the work that adjectives are usually asked to do.

## Sentence moves that are characteristic

- **Short declaratives, one idea each.** "Aluminum carries the current." "Voltage is raised
  for transport and lowered for use."
- **Second person for what the reader knows and does not know.** "You know the total and you
  know the individual pieces of energy. You do not know the power at any point in the middle."
- **Imperative for the reader's job.** "Pick any vertical slice and add the three."
  "Memorize that one; it reappears in voltage regulation." "Know when they fail."
- **Consequence in hardware, not in adjectives.** "The unit runs hot, ages early, and fails
  in a heat wave." Not "this is a significant reliability concern."
- **Named actors for a comparison.** Engineer A and Engineer B, rather than "one approach
  versus another approach."
- **Numbers first, verdict second.** State the arithmetic, then in a separate sentence say
  what it means.
- **Definition by negation, when the misconception is the obstacle.** "Not a black box you
  trust - the answer key you grade yourself against." "Steady state is an assumption, not a
  fact."
- **Deflationary honesty about limits.** "Assumes every transformer is loaded equally hard,
  which is false but rarely disastrous." "Closure proves the arithmetic, not which rule is
  right." "Citations measure influence, not correctness." Never oversell a method on the
  slide that introduces it.
- **Cross-references by slide title, not by week.** "The same fixed point as the
  forward-backward sweep", "see Bank placement". Week numbers go stale when the syllabus
  moves; the only week reference is the preview on `Next`. In visible text the unit is a
  **slide** ("the previous slide"), never a *frame*, which is LaTeX vocabulary.
- **One example threaded across slides.** The same five houses, the same feeder, the same
  16.2 kW. A fresh set of numbers per slide makes the reader restart.

## Common mistakes

| Mistake | Symptom | Fix |
|---|---|---|
| Title states the conclusion | `Coincidence Factor Reduces Required Transformer Size` | Name the object or pose the question: `So how big a transformer?` |
| Slide is a speaker script | Full sentences at body size, no artifact | Put the drawing or table in, cut the prose to a caption |
| Symbol used before it is defined | Reader meets $\GMR$ inside an equation | Notation frame first, muted gloss under the display |
| Result presented, not derived | The matrix appears with no arithmetic chain | Show one entry computed end to end |
| Matrix shown but never read | Slide ends at the boxed answer | Add a `Reading <artifact>` frame with bolded findings |
| Assumption buried in a clause | "assuming the neutral is grounded, ..." | Own line, alert-marked, plus the misreading it invites |
| Steps never announced | Reader cannot tell which topic a slide serves | Contract table on `Today`, topic as the frame title |
| Question announced, not answered | "The question here is ..." | State the claim; let the reasoning follow |
| Undefined everyday word used as a term | "after a delay", "teaching bank" | Name the symbol with unit and typical value; replace coined labels with general rules and a cited standard |
| A location claim with no picture | "the bank is best at 675" in text only | Feeder drawing with the candidate locations marked |
| Heavy algebra clogs the main line | Three slides of series expansion mid-derivation | Move to `\appendix`, point at it by name |
| Bracketing dash pair | `X --- which does Y --- is Z` | Comma, or two sentences |
| Adjective standing in for evidence | "significant voltage drop" | Give the number: "194 V, or 1.6%" |
| Hedged assumption | Method presented with no stated limit | Add the one line saying where it breaks |
| Restarting the example | New numbers every slide | Carry one worked case through |
| Title Case | `Common Measurements Across Distribution System` | `Common measurements` |

## Known drift in the corpus

Week 3 contains the exceptions, not the pattern. `Loading: The fundamental to Distribution
System Planning`, `Common Measurements Across Distribution System`, and `Energy and Power.`
(terminal period) are Title Case and over-long. Treat them as items to fix, not as
precedent.

## Related skills

- `plain-language-technical-writing` - the grounding model and content discipline this skill
  sits on top of. Load both.
- `scientific-slides` - slide budget for a given time slot, and the rendered-output review
  pass. Use it for *how many*; use this skill for *in what order* and *in what words*.
- `scientific-writing` - IMRaD and citation mechanics for papers. Orthogonal.
