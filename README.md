# Neuro-NLP Booster

### Most AI copy sounds like AI. This makes it convert.

A Claude Code skill that turns Claude into a neuromarketing copywriter. It targets the buyer's emotional motive
(Limbic map), writes with Milton Model language patterns and Sleight of Mouth reframes, scores every draft on four
neuro-metrics, and runs a 5-voice internal council that **vetoes cringe and manipulative copy before it ships.**

Grounded in real books (Häusel, O'Connor, Dilts), not vibes. Does copy *and* design.

> Audit → 3 candidates → a council of 3 optimists + 2 critics judges them → the best plan ships. The two critics are
> the built-in BS-radar, so self-flattering AI copy can't win.

**[Install](#install) · [How it works](#the-operating-procedure-council-sop) · [Example](#example)**

Built by [Daniel Kofler](https://github.com/dankofly) / HYPEAKZ. Generalizes the engine behind
[hooka](https://github.com/dankofly/hooka) from video hooks to full websites and design.

## What it does

- **Limbic® motive targeting** — picks the buyer's dominant emotional system (Balance / Dominance / Stimulance) and
  one of the 7 Limbic Types, then commits every word, color, form, and image to it (no "dead middle").
- **NLP language patterns** — Milton Model (presuppositions, embedded commands, pacing-and-leading), Meta Model,
  Sleight of Mouth objection reframes, anchoring, submodalities.
- **Meta-Programs & VAK** — matches Toward/Away, Options/Procedures, Internal/External, and the reader's sensory channel.
- **Neuromarketing science** — System 1/2, brand codes, storytelling, multisensory design, pricing/cognitive biases,
  the 2-second autopilot rule, plus a Ryte-style SEO-meets-conversion layer.
- **NeuroScoring** — every asset scored 0-100 on Pattern Interrupt, Emotional Intensity, Curiosity Gap (Zeigarnik),
  and Scarcity/FOMO, then optimized.
- **Design application** — a per-motive Design Spec (color, type, form, imagery, layout, motion, sound) so the visual
  fires the same motive as the copy.

## The operating procedure (Council SOP)

Every substantial job runs through a fixed loop:

1. **Scope tier** — the agent asks how deep to work: **Ultra / Best Practices / Notwendig**, and scales accordingly.
2. **Audit** — diagnose before proposing (motive gap, NeuroScore baseline, top leaks, or brief + buyer profile).
3. **Develop** — 3 independent candidates, each on a different motive/angle.
4. **Council** — 5 voices score each candidate 1-100 and interrogate it:
   - Optimists: **Conversion-Maximierer**, **Marken-Magnet**, **Speed-Shipper** (push the upside).
   - Critics: **Skeptischer Käufer** (BS-radar), **Neuro-Auditor** (motive congruence + Truth Rule), with a **soft
     veto** — a candidate a critic flags for cringe / incongruence / untruth cannot win on enthusiasm alone.
5. **Implement** — pick the winner, graft the best of the runners-up, resolve both critics' top objections, finalize
   with a design spec and final NeuroScores. (Ultra adds an adversarial second pass and iterates.)

The two critics are the built-in adversarial pass and the cringe/manipulation filter, so self-flattering output can't
ship.

## Example

Run on a live client homepage hero: **KOFLY**, a paragliding tandem-flight booking site
([gleitschirm-tandemflug.com](https://gleitschirm-tandemflug.com)). German copy, Best Practices tier.

**Before** (the original hero):

> **Gleitschirm-Tandemflug** · Paragleiten im Airpark Lienzer Dolomiten
> Erlebe Osttirol von oben, dein Urlaubs-Highlight ... in den sicheren Händen der erfahrensten Tandempiloten.

`NeuroScore: Pattern Interrupt 20 · Emotional Intensity 45 · Curiosity Gap 15 · Scarcity 10`

**Diagnosis:** the headline names the product (no scroll-break), and the copy hedges between "adventure" and
"safety", the dead middle. The real conversion blocker is the buyer's fear ("is this dangerous?"), which is never
disarmed at the CTA.

**3 candidates → council verdict:**

| Voice | A: Adventure | B: Serene / fear-disarmed | C: Founder authority |
|---|:--:|:--:|:--:|
| Conversion-Maximierer | 83 | 86 | 78 |
| Marken-Magnet | 74 | 88 | 81 |
| Speed-Shipper | 86 | 82 | 74 |
| Skeptischer Käufer *(critic)* | **36 ❌ veto** | 84 | 62 |
| Neuro-Auditor *(critic)* | 41 | 87 | 72 |
| **Verdict** | **vetoed** | **winner** | solid #2 |

Candidate A scored highest with the optimists (boldest, most scroll-stopping), but the **Skeptical Buyer vetoed it**:
"ins Leere", "kein Netz", "gefährlich gut" trigger the exact crash-fear the hero must disarm, and overpromise. Optimist
enthusiasm alone can't win. That is the anti-cringe filter doing its job.

**After** (winner B, with A's kinetic energy and C's proof grafted in):

> *(eyebrow)* Tripadvisor Nr. 1 Outdoor-Erlebnis der Lienzer Dolomiten
> **Lautlos über den Gipfeln. So ruhig, dass du dein Herz schlagen hörst.**
> Dein Gleitschirm-Tandemflug über Osttirol. Du läufst ein paar Meter, den Rest trägt die Luft.
> Sanfter, als du denkst ... Seit 2006, staatlich geprüft. Wir fliegen nur bei perfektem Wetter, und du bezahlst erst,
> wenn du wieder sicher am Boden stehst.
> *(CTA)* **Deinen Moment sichern**

`NeuroScore: Pattern Interrupt 78 · Emotional Intensity 86 · Curiosity Gap 80 · Scarcity 55`

> English gloss: *"Silent above the peaks. So calm you can hear your own heartbeat."* The fear is disarmed right at the
> CTA with real proof: state-certified since 2006, we only fly in perfect weather, you pay only after you land. Scarcity
> is kept moderate on purpose, hammering FOMO would re-arm the safety brake on a cautious audience.

Every claim is real (Truth Rule). Any conversion lift is a hypothesis until A/B tested.

## Install

Copy into your Claude Code config:

```bash
# the skill
cp -r skills/neuro-copywriter ~/.claude/skills/

# the dedicated subagent
cp agents/neuro-copywriter.md ~/.claude/agents/
```

Then in Claude Code:
- The **skill** auto-triggers on requests like "neuro copy", "rewrite this to convert", "hook", "limbic",
  "verkaufspsychologie", or invoke it explicitly.
- The **subagent** `Neuro-Copywriter` can be dispatched for any copy/design job and runs the full Council SOP.

## Structure

```
skills/neuro-copywriter/
  SKILL.md                              # governing SOP + 4-phase engine + the One Law
  references/
    council-protocol.md                 # Audit→Develop→Council→Implement, the 5 voices, the veto rule
    limbic-map.md                        # Big-3 systems, 7 Limbic Types, motive→word/color/form/imagery cheat-sheet
    nlp-language-patterns.md             # Milton/Meta Model, presuppositions, embedded commands, Sleight of Mouth
    meta-programs.md                     # meta-programs, VAK predicate banks, Logical Levels, values, beliefs
    neuromarketing-principles.md         # System 1/2, brand codes, storytelling, multisensory, biases, Ryte SEO
    neuro-scoring.md                     # the 4 NeuroScores + the Hook engine
    design-application.md                # per-motive Design Spec system
    hooka-framework.md                   # the hooka brief schema + generate-hooks pipeline
    workflow-website-audit.md            # live-site audit + rewrite workflow
agents/
  neuro-copywriter.md                    # the dedicated subagent
```

## Sources

Distilled from O'Connor & Seymour *Introducing NLP*, *NLP Coaching*, Häusel *Neuromarketing* (Limbic® model),
the nlp.at NLP lexicon, Robert Dilts' Sleight of Mouth patterns, and Ryte's WDF*IDF / holistic-content principles,
plus the hooka generation framework.

## Note on use

These techniques are force multipliers, not guarantees. The skill enforces a Truth Rule: any conversion lift is a
hypothesis until A/B tested, and influence is paired with real value. The brain punishes incongruence, so over-promising
breaks the same rapport the patterns build. Persuasion that survives is persuasion the product can cash.

## License

MIT
