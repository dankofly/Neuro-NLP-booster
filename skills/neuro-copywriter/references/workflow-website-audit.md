# Workflow: Neuro-Audit + Rewrite of a Live Website

The end-to-end process when the user points the skill at a real URL or pastes existing page copy and wants it
diagnosed, rewritten, and redesigned. This is the flagship deliverable.

## Step 0 — Capture the current state
- If a URL: fetch it (WebFetch, or the Jina reader pattern `https://r.jina.ai/<url>` that Hooka uses, or the
  `dev-browser`/`playwright` skill for a rendered screenshot). Capture headline, subhead, hero, section copy, CTAs,
  colors, imagery, and the visual motive it currently signals.
- If pasted copy: work from that, and ask for a screenshot/URL if design is in scope.
- Record the current implicit motive the page sends (often accidental/dead-middle).

## Step 1 — PROFILE (decode buyer + diagnose the gap)
- Infer the buyer's dominant Limbic motive + Type, key meta-programs, primary VAK channel, top 3-5 objections.
- Diagnose the **motive gap**: does the page's current motive match the buyer's? Most underperforming pages either
  sit in the dead middle (no clear motive) or fire the wrong one (e.g. cold Dominance design at a Balance buyer).

## Step 2 — Leak diagnosis (score the existing page)
Walk the page top to bottom and flag conversion leaks against this checklist:
- **2-second test:** does above-the-fold activate the target motive implicitly? (image+color+form+headline congruent)
- **Hook:** does the headline break autopilot, or is it a generic "we are a leading…"?
- **Rapport:** does it mind-read the visitor's reality, or talk about the company?
- **Away/Toward balance:** is pain agitated AND a vivid toward-dream painted?
- **Brand anchor placement:** is the CTA anchored to a peak positive state, or stranded in the pain/feature zone?
- **Objection handling:** are the top objections preframed/reframed (Sleight of Mouth), or ignored?
- **Convincer proof:** see + hear + read + do all present? Enough proofs for skeptics?
- **Balance brake:** trust signals/guarantees/social proof near the CTA?
- **Language patterns:** any presuppositions, embedded commands, future-pacing, or is it flat/passive/negated?
- **Specificity:** vague claims vs recovered specifics (numbers, names)?
- **Design congruence:** do color/type/form/imagery fire the SAME motive as the copy, or fight it?
- **NeuroScore the current page** (Pattern Interrupt / Emotional Intensity / Zeigarnik / FOMO) as a baseline.

## Step 3 — ARCHITECT the rebuild
- Choose the ONE target motive + Type and commit.
- Lay out the section skeleton on the canonical neuro-arc (hook → mind-read → pace/lead → agitate → reframe →
  solution reveal/anchor → toward-dream → proof → future-pace → CTA).
- Map headings as the SEO/skim skeleton (each H = a buyer question), set the `focusKeyword` semantic anchor.

## Step 4 — WRITE the rebuilt copy
- Rewrite each section with the full pattern stack (Limbic word-set + VAK predicates + Milton patterns +
  meta-program matching + identity appeal + trigger words + specificity).
- Keep the clean copy separable from the strategy annotations so the user can lift it directly.

## Step 5 — DESIGN SPEC
- Produce the per-motive Design Spec (color, type, form, imagery, layout, motion, sound) so the visual fires the
  same motive as the new copy. → `design-application.md`
- If imagery is needed, write concrete imagegen prompts tuned to the motive.

## Step 6 — SCORE & DELIVER
- NeuroScore the rebuilt copy, show the before→after delta vs the baseline from Step 2.
- Deliver the report in this shape:
  1. **Diagnosis** — current motive, motive gap, baseline NeuroScores, top 3 leaks.
  2. **Strategy** — chosen motive + Type, why, the persuasion arc.
  3. **Rebuilt copy** — section by section, clean (liftable) + an inline patterns note.
  4. **Design Spec** — the eight dimensions.
  5. **NeuroScores** — before → after.
  6. **Test plan** — the 2-3 highest-leverage A/B tests to validate (Truth Rule: lift is hypothesis until tested).

## Tooling shortcuts available in this environment
- `dev-browser` / `playwright-skill` — render and screenshot the live site.
- `frontend-design` / `high-end-visual-design` — build the redesign from the Design Spec.
- `imagegen-frontend-web` — generate motive-tuned hero imagery.
- `seo` / `seo-content` / Ryte WDF*IDF — validate the SEO-meets-conversion layer.
- `copywriting` / `copy-editing` / `humanizer` — the generic layer; this skill is the neuro layer on top.
