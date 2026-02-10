# LLM overgeneration vs. human cognition (analysis paralysis)

## 0) One-line summary

LLMs can produce extensive, logically structured explanations that still fail to become meaning because they expand interpretation space faster than the reader can close it.

## 1) Context

- Domain: knowledge work (engineering/product/legal)
- Setting: an LLM generates a long “comprehensive” answer with many options
- Decision: choose one plan and execute

## 2) What information existed

- Many correct facts and plausible options
- Stepwise reasoning for each option
- But no explicit chart selection (“we are optimizing for speed vs. safety vs. reversibility”)

## 3) Meaning breakdown

- Semantic entropy increases: the reader now has more branches to evaluate
- Termination condition missing: “what is sufficient to decide?”

## 4) Local charts involved

- Narrative chart: contextual explanation
- Decision chart: options + tradeoffs + recommendation + confidence
- Mismatch: output remains in narrative chart, but the user needs a decision chart

## 5) Semantic Atlas reframing

- Enforce a decision-first chart (recommendation + constraints + risks)
- Allow expansion only on-demand (progressive disclosure)

