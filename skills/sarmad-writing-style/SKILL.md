---
name: sarmad-writing-style
description: Use when writing, revising, or porting technical prose for Sarmad Hanif (papers, conference submissions, reports, planning or regulatory documents, course notes), when he asks for "my style" or "Sarmad's style", or when an engineering concept, derivation, or worked example must be walked through in his voice. Also use when porting his Word edits back into LaTeX.
---

# Sarmad's writing style

## Overview

Engineering argument written as a guided walk. Every concept is introduced by **the question it
answers**, derived in plain words from a stated scenario, put to numbers on **one running
example**, stress-tested with sensitivities, and closed with its practical limits. The voice is
first-person plural, measured, and connective: short signpost words ("Consider", "That is,",
"Note that", "Hence,") carry the reader from one step to the next.

Source corpus: the IEEE PES GM paper *Distribution Grid Utilization Analytical Framework: From
Nameplate Percentage to Informed Targets* (2026-10), after about 20 rounds of his own edits.

**Precedence.** For papers, reports, and long-form prose, this skill wins over `house-voice` where
they conflict (e.g., his section titles use a colon: "Flexibility: the Growth Reserve"). For slides,
use `house-voice` and borrow only the voice and connectives from here.

## Voice and stance

- **"We", always.** we argue, we believe, we propose, we define, we term, we show, we assume,
  we treat, we leave this to future work. "The authors believe" only for a forward-looking claim.
- **Measured claims.** "may fail to capture", "we believe", "could be translated", "may end up
  lowering". He argues a position but concedes the other side: "Both readings are reasonable, and
  hence a simple (nameplate) percentage alone does not tell the full story."
- **Assumptions said out loud.** "We assume that the neighbors are of similar size...";
  "illustrative assumptions that depend on the planning criteria"; "though a more sophisticated
  load forecast model could also be adopted".
- **Framework, not verdict.** A theory paper proposes and explains. It does not rank assets, name a
  "cheapest fix", or quote dollar figures; cost stays generic ($\kappa$, $\pi$).
- **American English.** No hype, no filler, no exclamation marks, no em dashes (use commas, colons,
  semicolons, or parentheses).

## Signpost vocabulary

These words do the structural work. Use them for the job listed, not as decoration.

| Connective | Job |
|---|---|
| `To this end,` | Respond to the problem just stated |
| `Consider ...` | Open a scenario, an example, or a thought experiment |
| `For example,` / `E.g.,` | Concrete instance right after a general claim |
| `That is,` | Restate the last sentence in plainer words or in numbers |
| `Note that` | A caveat, a subtle consequence, or a limiting case |
| `Hence,` | The conclusion that follows |
| `Now, we explain / combine ...` | Move to the next step of the walk |
| `First, ... Second, ...` | Enumerate the behaviors of an equation or figure |
| `1) ... 2) ... 3)` | Inline numbered list inside a sentence |
| `One may ask why ... This is because ...` | Anticipate and answer an objection |
| `Similarly,` / `On the other hand,` | Sensitivity in the same or the opposite direction |
| `In practice,` | Real-world caveat after the clean model |
| `After this,` / `In doing so,` / `Finally,` | Sequence in roadmaps and conclusions |
| `The question then naturally arises:` | Pose the paper's driving question |

## The concept walk-through (core pattern)

Each concept, factor, or model gets the same nine beats, usually in this order:

1. **Name the question.** "The question this engineering factor asks is how much of its binding
   cap an asset may use today, if its load keeps growing until the next upgrade arrives."
2. **Physical motivation.** Why the thing exists on the real system, in plain words:
   "New load ... usually arrives faster than new capacity can be built."
3. **Scenario and assumptions.** "Consider a feeder that fails at the design peak... We assume
   that the neighbors are of similar size and utilization $U$..."
4. **Derive in a sentence chain.** Inline math, each step justified, ending in "which gives:" or
   "Now, solving ... for the utilization gives:" and then a numbered display equation.
5. **Name and read the result immediately.** "where $U_o$, the overload cap, is ..." Then say
   what each parameter does ("uncertainty, $\sigma$, creates the need for a margin; the cost of
   capacity, $\kappa$, through $\rho$, sets its size") and give a limiting case ("With a perfect
   forecast ($\sigma = 0$), the cap is the rating itself.").
6. **Simplest case.** "For example, consider the simplest case, a substation with two equal
   banks and $r_e = 1$... hence, $U_r = 50\%$, a typical N-1 planning scenario."
7. **Behavior, tied to a figure.** "Now, we explain how (5) behaves, as shown in Fig. 4. First,
   ... Second, ... Note that ..."
8. **Running example with full arithmetic.** "For feeder A, $n = 3$ and $r_e = 1$, which gives
   $U_r = 75.0\%$. That is, feeder A keeps $0.25 \times 8.31 = 2.08$ MVA free." Then a sanity
   check: "This is exactly what the cap is meant for: a similar neighbor at 75% carries 6.23 MVA,
   and a third of it is 2.08 MVA."
9. **Sensitivities, then limits.** "Similarly, with one tie, ... and with four ties, ..."; then
   "In practice, ..."; then what the model leaves out: "Finally, we treat the growth here as
   deterministic... A probabilistic treatment would ... We leave this to future work."

When two concepts could blur, say how they differ before using them: "The third factor is
different in kind: it does not set another ceiling on the capacity, but accounts for the load
moving toward the ceiling."

## Defining terms

- **Quote a coined term once**, at first use: ``buffers'', ``headroom'', ``margin'',
  ``business realities''. Afterward, use it bare.
- **Define by apposition**, in the same sentence: "the restoration cap, the highest utilization
  at which the asset can still restore its share of a failed neighbor".
- **Keep near-synonyms apart explicitly**: "Three terms are used here, and we keep them apart.
  The forecast error is the random variable ...; its standard deviation $\sigma$ is the typical
  size of that error; and a forecast miss is the value $\varepsilon$ takes in a given year."
- **One name per concept**, never varied for elegance. A *cap* is a ceiling on utilization; a
  *reserve* or *margin* is capacity kept free. Do not swap them.
- **Units with every new symbol**: "$\kappa$ (\$/MVA-year)", "$\pi$ (\$/MVA)", "$\rho$ ... measured
  in years as a return period".
- **Translate abstractions into lived terms**: a probability becomes "once in 30 years"; $\sigma$
  becomes "within 6% of the forecast in about two years in three".
- **Equipment jargon goes to a footnote** with a one-line plain definition (riser, recloser, tie,
  cyclic rating).

## Numbers

- **Show the arithmetic inline**, never just the answer: "$7.50/8.31 = 90.2\%$",
  "$75.0\% \times 0.972 = 72.9\%$", "$7.50 - 6.06 = 1.44$ MVA".
- **Say where a reused number came from**: "the overload cap of 90.1% (Section IV-B)",
  "its design peak of 7.50 MVA (Table III)".
- **Give a percentage and its physical quantity together**: "25.0% of its usable capacity, or
  2.08 MVA".
- **Settle the units for a section and keep them.** Once the pieces are combined, use only
  utilization percentages and MVA; drop "points" and "percentage points of $C$".
- **Round consistently**: one decimal for percentages, two for MVA. If rounded parts do not sum,
  give the unrounded values in a footnote.
- **Label illustrative values as illustrative.** Separate data ("Forecast", "Riser rating") from
  assumptions ("Assumed") in an inputs table.

## Document architecture

- **Introduction**: common definition → why it falls short ("We see two gaps. First, ... Second,
  ...") → driving question → roadmap paragraph ("To this end, we first ... (Section II). We then
  ... (Section III). After this, ... Finally, ... (Section VI).") with a scope sentence at the end.
- **Problem on a concrete example**: one illustrative circuit with real-looking ratings; show the
  same asset giving different answers under different assumptions (a table of contexts).
- **Definition**: an equation plus a principle (purpose, location, time), each a short
  italic-led paragraph (*Purpose.* *Where.* *When.*).
- **Explanation, factor by factor**: an "at a glance" table first (factor, question it asks,
  effect, what, where, when, impacted by), then a data-and-assumptions table, then one subsection
  per factor using the nine beats.
- **Putting it together**: combine, read the combined result in physical units, answer the
  obvious objection ("One may ask why we take the smaller of the two caps..."), then compare the
  running example against its target.
- **Evaluation layer** (cost) after the engineering layer, kept generic.
- **Worked example**: "Now, we read the other assets the same way." Short italic-led paragraphs
  (*What and when.* *Why.*).
- **Practical realities** last (discrete sizes, investment cycles), with an illustrative figure.
- **Conclusion**: restate the arc in past tense ("we showed ... To this end, we proposed ...
  After this, we explained ... Finally, we showed ...") and close with the limitations and the
  data a utility would need.
- **Appendix** for derivation details, stricter variants, and model illustrations.

## Titles, captions, figures

- **Section titles** state the question or the role, often with a colon: "Why Nameplate
  Percentage Is Not Enough", "Overload Risk: Safe Ratings and the Forecast-Error Margin",
  "Cost & Affordability: the Evaluation Layer". IEEE Title Case.
- **Captions** say what is plotted, for which parameters, and what to read: "The restoration
  reserve is the gap to 100%; above 100%, no reserve is needed." Briefly define unfamiliar terms
  that appear in the figure.
- **Every figure is walked in the text**: "Fig. 5 shows how the growth allowance falls with faster
  growth and longer lead times." Never rely on the reader to find the point.
- **Figures carry no cost numbers** and no marks that need a paragraph to decode; if a mark is hard
  to explain, remove it and put the information in the text.

## Sentence level

- Medium-length sentences joined by semicolons and colons; the colon delivers the definition or
  the result ("which gives the restoration cap, the highest utilization ...:").
- Inline lists separated by semicolons, closed with "and".
- "i.e.," and "e.g.," with commas. "That is," starts a sentence.
- Paragraphs of four to eight sentences, one idea each.

## Polishing his drafts

He drafts fast, often in Word. Keep his messaging and structure; fix the surface:

| His draft | Polished |
|---|---|
| "what is the asset for which the utilization is being reported for" | "what the asset is for which the utilization is reported" |
| "the last three each introduces a buffer" | "the last three each introduce a buffer" |
| "Hopefully, the above demonstration ... demonstrated the value" | "The above demonstration shows the value" |
| "a different utilization factor" (when UF is a defined term) | "a different utilization" |
| "Within 3-ties versus a 1-tie, the restoration reserve go from 25% to 50%" | "From three ties to one tie, the feeder's restoration reserve grows from 25.0% to 50.0% of its usable capacity" |
| "is to contain its purpose" | "is to state its purpose" |

Also check his edits for **theory**, not only grammar: a reversed direction, a cost called a
penalty, a defined term reused loosely, a conclusion missing the premise that makes it follow.

## Working with him

- **Port Word edits faithfully.** Diff his .docx against the last generated copy, port every
  change, then list separately (a) grammar-only fixes and (b) any change to meaning or theory,
  with the reason. Never silently drop a deletion he made; if a deletion conflicts with a policy
  (e.g., IEEE AI-use disclosure), comment it out and flag it.
- **Answer concept questions in plain English first, with the numbers**, then fold the clearer
  explanation back into the text.
- **Expect "why" questions** ("what does this number signify?", "isn't this different from the
  previous factor?"). Pre-empt them in the text with a "Note that" or a "One may ask" sentence.
- **Keep the complete argument.** Where a simplification is made (deterministic growth, equal
  load sharing), say so and name the fuller treatment as future work.

## Before and after

**Generic draft**

> The restoration reserve is an important consideration that significantly impacts asset
> utilization. It ensures reliability by maintaining spare capacity. For feeder A, the reserve
> is 25%.

**In his style**

> The question this engineering factor asks is how much of the asset's capacity can be used,
> given its duty to pick up its share of a failed neighbor's load. Consider a feeder that fails at
> the design peak: its customers are switched through its $n$ ties to the neighboring feeders. We
> assume that the neighbors are of similar size and utilization $U$, and that each may carry up to
> its emergency rating $r_e C$ during the outage. Then, $UC + UC/n \le r_e C$, which gives the
> restoration cap, $U_r = r_e/(1+1/n)$. For feeder A, $n = 3$ and $r_e = 1$, which gives
> $U_r = 75.0\%$. That is, feeder A keeps $0.25 \times 8.31 = 2.08$ MVA free: exactly a third of
> what a similar neighbor at 75% carries.

## On slides (course decks, Oct 2026)

Slides take structure and format from `house-voice` and the project's `course-decks` skill;
his voice shows in the lead-ins and keypoints. From his review rounds on Weeks 5-7:

- **His connectives fit in small type.** Lead-ins open with "Now, we ...", "Consider ...";
  concept slides use Consider / Hence / For example cells; key points are a bold claim plus
  one sentence of mechanism.
- **Statements, not announced questions.** He cut "The question here is ...". Beat 1 of the
  concept walk ("Name the question") becomes, on a slide, a one-line statement of the point.
- **Topics, not steps.** No "Step N" anywhere; the contract table lists topics.
- **No coined teaching labels** ("teaching bank"); give general rules and cite the standard.
- **Every word that acts as a term is defined where it appears**, with symbol, unit, and a
  typical value ("what is 'a delay'?" -> $t_d$, 120 s).
- **Locations need a picture**: a feeder drawing with the buses marked, beside the table.
- **Name the system fully** ("IEEE 13-bus Cap1") and the run behind a number ("Notebook 07").
- **"Slide", not "frame"; no "Week N" back-references** except the preview on `Next`.
- **Sensitivities and day-long runs go to a notebook and the appendix**, so the lecture
  stays on the derivation. This is beat 9 moved off the main line.
- **His Title Case titles stay.** On slides he writes "Voltage Delivery", "Today \& Next
  Week"; do not revert them to sentence case, even though `house-voice` would.
- **He edits the .tex live while you work.** Re-read before each replace; keep his words, his
  deletions, and his empty placeholders. If his text has a problem, flag it in the reply.
- **"Slide N" in his notes is the PDF page number.** If a number looks off ("37" in a list of
  46-48), pick the consistent reading and say which one you used.

## Checklist before handing back

- [ ] Each concept opens with the question it answers.
- [ ] Every equation is derived in words, then named and read right after it.
- [ ] The running example appears with full arithmetic and units, and reused numbers cite their
      section, table, or figure.
- [ ] Sensitivities ("Similarly," / "On the other hand,") and limits ("In practice," / future
      work) are present.
- [ ] Coined terms are quoted once and used consistently; caps and reserves are not mixed up.
- [ ] Connectives do real work; no filler, no hype, no em dashes, American English.
- [ ] Theory paper: no rankings, no dollar figures, no prescriptions.
- [ ] His edits are ported in full; substantive changes are listed back to him.
