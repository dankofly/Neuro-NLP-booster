# Neuro-NLP Booster

A maximalist **NLP + Neuromarketing copywriting and web-design engine** for Claude Code, shipped as a Skill plus a
dedicated subagent. It engineers website copy, landing pages, hero sections, ads, emails, and hooks using
subconscious-influence techniques, then matches the visual design to the same emotional motive. Every asset is built
motive-first, judged by an internal council, scored, and optimized.

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
