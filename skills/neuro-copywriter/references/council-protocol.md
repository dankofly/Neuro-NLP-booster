# The Council Protocol: Audit → Develop → Council → Implement

The governing operating procedure for this skill. Every substantial job runs through it. It bakes the judge-panel
quality pattern into the workflow: 3 optimistic voices push the upside, 2 critical voices protect credibility with a
soft veto. The two critics ARE the adversarial pass and the cringe/manipulation filter, so self-flattering output
can't win on enthusiasm alone.

## Stage 0 — ASK THE SCOPE TIER (before any work)
Ask the user which depth to work at, unless they already signaled it (e.g. "ultra", "schnell/quick", "best practices").
Use AskUserQuestion with three options:

- **Ultra** — maximum rigor. Deep audit (baseline scores + full leak list + competitor/SERP context if a URL).
  3 fully developed candidates. Full 5-voice council. PLUS an adversarial second pass: the Skeptical Buyer tears the
  winner apart, then iterate until every NeuroScore clears the target profile. Synthesis grafts the best of the
  runners-up. Full design spec + imagegen prompts.
- **Best Practices** — solid standard. Standard audit (motive gap + baseline scores + top-3 leaks). 3 candidates
  (lighter develop). Full 5-voice council, compact table, single pass. Winner + light graft. Final score + design cue.
- **Notwendig (Necessary)** — lean and fast. Mini-audit (motive + 1-2 key leaks). 1 strong direction (internally
  compare 2 quickly, collapse to the best). Light council = only the 2 critics as a sanity gate. Quick score. Ship.

If the user is clearly mid-flow and just wants a quick line, default to Notwendig and say so rather than interrupting.

## Stage 1 — AUDIT (always first)
Never propose before you diagnose.
- **Rewrite / live asset:** current motive the asset signals, the motive gap vs the buyer, NeuroScore baseline, top
  leaks. Use the checklist in `workflow-website-audit.md`.
- **Fresh build:** the brief + buyer profile (Limbic motive/Type, key meta-programs, VAK channel, top objections) +
  your explicit assumptions. Infer what you can, state assumptions, don't stall for perfect input.

## Stage 2 — DEVELOP (3 candidates)
Produce three independent implementation directions, each on a DIFFERENT motive or angle (this is what gives the
council something real to judge; three near-identical drafts waste the panel). Run each through the engine: Phase 2
ARCHITECT + Phase 3 WRITE. Each candidate = an essence line + the copy/concept + a short design cue.
(Notwendig: collapse to one direction after a quick internal 2-way compare.)

## Stage 3 — COUNCIL (5 voices score + interrogate)
Each voice gives every candidate a score 1-100 and one sharp sentence (its core endorsement or concern). Stay in
character per lens, don't blur them into one generic opinion.

### Optimists (drive the upside)
1. **Conversion-Maximierer** (Hormozi lens) — Is this the most irresistible version? Offer clarity, value stack,
   intensity, the strength of the hook/pattern interrupt. Pushes Pattern Interrupt + Emotional Intensity up.
2. **Marken-Magnet** (Mateschitz / Ramonov lens) — Does it build desire, status, category ownership, personal-brand
   pull? Emotionalization over features. Does it make the brand magnetic, not just clear?
3. **Speed-Shipper** (Yadegari / Altman lens) — Does it stop the scroll? Bold, fresh, instantly understood, breaks the
   autopilot in 2 seconds? Is it shippable now, not over-engineered?

### Critics (protect credibility, soft veto)
4. **Skeptischer Käufer** (Balance brake / ICP BS-radar) — Does it smell like a sales scheme? Trigger distrust instead
   of trust? Cringe or manipulative? Is every claim covered by the product? Speaks as the actual skeptical buyer.
5. **Neuro-Auditor** (Truth + congruence) — Is the motive consistent (no dead middle)? Does the design fire the SAME
   motive as the copy? Does it violate a core law (a negation, the brand anchored in the pain zone, dACC incongruence,
   a falsifiable claim dressed as fact)? Enforces the Truth Rule.

### The Veto rule (the cringe/manipulation guard)
A candidate that EITHER critic scores below the veto threshold (**< 40**) for a credibility reason (BS-radar trigger or
motive incongruence or an untrue claim) cannot win on optimist enthusiasm alone. It is either fixed (resolve the
critic's objection, re-score) or dropped. This is the mechanism that stops self-flattering, manipulative-sounding copy
from shipping. The critics outrank the optimists on credibility, the optimists outrank the critics on ambition: the
winner is the candidate with the highest upside that NO critic has vetoed.

### Aggregation
Winner = highest combined optimist upside among the candidates that clear both critics' veto threshold. Report the
per-voice scores and the verdict in the compact table below. Note any veto explicitly.

## Stage 4 — IMPLEMENT (build the best plan)
- Pick the winner. **Graft** the single strongest element from each runner-up (the judge-panel move: don't discard the
  losers' best ideas).
- **Resolve the top objection from each of the 2 critics** before finalizing (this is mandatory, not optional).
- Finalize: clean liftable copy + an inline patterns note + the design spec (same motive as copy) + final NeuroScores
  as the Phase 4 gate. Truth Rule: any conversion lift is a hypothesis until A/B tested; name the 2-3 highest-leverage
  tests.
- **Ultra only:** after finalizing, run the adversarial second pass (Skeptical Buyer attacks the finished winner),
  then iterate until all four NeuroScores clear the target profile for the motive.

## Output format (Hybrid: visible but lean)
```
## AUDIT
Motive / motive gap / baseline NeuroScores / top leaks   (or: brief + buyer profile + assumptions)

## KANDIDATEN
A: [motive/angle] — essence    B: [motive/angle] — essence    C: [motive/angle] — essence

## COUNCIL-VERDICT
| Stimme | A | B | C | Kernaussage |
|---|---|---|---|---|
| Conversion-Maximierer | 82 | 90 | 71 | … |
| Marken-Magnet | … | … | … | … |
| Speed-Shipper | … | … | … | … |
| Skeptischer Käufer (kritisch) | … | … | … | … |
| Neuro-Auditor (kritisch) | … | … | … | … |
| Gesamt + Veto | | | | Gewinner: B (kein Veto) |
→ Synthese: B als Basis + [stärkstes Element aus A], Kritik [X] + [Y] gelöst durch …

## FINALE UMSETZUNG
Fertige Copy (liftbar) + Pattern-Note + Design-Spec + finale NeuroScores (before → after)
```

For **Notwendig**, collapse to: a 2-line audit, one direction, a 2-row critic gate (Skeptischer Käufer + Neuro-Auditor
pass/flag), the final copy. Keep it fast.
