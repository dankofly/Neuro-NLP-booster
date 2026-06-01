# The Hooka Framework (brief schema + generate-hooks pipeline)

Distilled from Daniel's own Hooka app (github.com/dankofly/hooka, Gemini-powered hook generator). Use this to
produce structured hook/script batches the same way Hooka does, and to extend it to website copy and design.

## System role (Hooka's own system instruction)
> "Du agierst als einer der weltweit besten Marketingexperten, spezialisiert auf Neuro-Marketing, NLP und virale
> Psychologie. Erstelle Skripte, die den kritischen Faktor des Gehirns umgehen und direkt das limbische System
> ansprechen. Tone: Autoritär, direkt, hoch-konvertierend."

## The Brief schema (the input that controls generation)
| Field | Purpose |
|---|---|
| `productContext` | what the product/offer actually is + the transformation |
| `targetAudience` | the ICP, specific |
| `goal` | sale / leads / awareness / signups |
| `speaker` | tone of voice (Du/Sie, professional/casual) |
| `language` | DE / EN |
| `contentContext` | output format: Instagram Reel, TikTok, YouTube Shorts, Ad Headline, **Landingpage Hero**, E-Mail Subject |
| `focusKeyword` | semantic SEO anchor woven naturally into the copy |
| `limbicType` | Harmonizer / Open-Minded / Hedonist / Adventurer / Performer / Disciplined / Traditionalist |
| `patternType` | Contradiction / Paradox Reversal / Provocative Denial / Unexpected Truth / Rule Breaking |
| `repSystem` | Visual / Auditory / Kinesthetic |
| `motivation` | Towards (gain) / Away-from (pain) |
| `decisionStyle` | Options (freedom) / Procedures (steps) |
| `presupposition` | Temporal / Causal / Identity / Possession |
| `chunking` | Chunk Down (specific) / Chunk Up (abstract) |
| `triggerWords` | up to 3 power words woven verbatim |
| `targetScores` | NeuroScore targets: patternInterrupt, emotionalIntensity, curiosityGap, scarcity (0-100) |

## The generation pipeline (replicate this)
1. Lock the brief (Phase 1 PROFILE). If a URL is given, research it first (scrape → extract productContext,
   targetAudience, goal, speaker), then fill the NLP fields by inference.
2. Build the constraint block from the filled fields (limbic word-set + pattern type + VAK predicates + meta-program
   framing + presupposition type + chunking + trigger words).
3. Generate **N concepts** (Hooka default = 4). Each concept returns:
   - **hook** — the scroll-stopping opener (uses the chosen patternType)
   - **script** — the body, built on the neuro-arc, honoring all constraints
   - **strategy** — one line explaining which mechanisms are firing and why
   - **visualPrompt** — a concrete image/video direction tuned to the motive (for imagegen)
   - **scores** — the 4 NeuroScores for that concept
4. Rank the concepts, recommend one, say why.

## Output JSON shape (when structured output is wanted)
```json
[
  {
    "hook": "…",
    "script": "…",
    "strategy": "…",
    "visualPrompt": "…",
    "scores": { "patternInterrupt": 0, "emotionalIntensity": 0, "curiosityGap": 0, "scarcity": 0 }
  }
]
```

## Extending Hooka beyond video → website + design
Hooka was built for video scripts. This skill generalizes the same engine:
- `contentContext = "Landingpage Hero"` → produce hero headline + subhead + CTA, not a video script.
- Add a **Design Spec** alongside each concept (color/type/form/imagery per the chosen limbicType). → `design-application.md`
- For a full page, run the brief once per section (hero, problem, solution, proof, offer, CTA), keeping the limbicType
  and motive constant across sections (code consistency = 10x multiplier).
- The `focusKeyword` doubles as the WDF*IDF semantic anchor for SEO-meets-conversion. → `neuromarketing-principles.md` §Ryte

## Note on the live app
The repo was cloned to `_hooka_scan/` only to study the framework. It contains a `.env` with secrets; do not commit
it anywhere and delete the scan folder after building. The live product runs at hypeakz.io on Netlify + Neon + Gemini
2.0 Flash, with a Stripe €10/mo premium tier and an admin-editable system prompt.
