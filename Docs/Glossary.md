# Glossary (Semantic Atlas Hypothesis)

This glossary expands the short table in `../README.md` into a working set of shared definitions.

Each entry includes:
- **Definition**: the minimal meaning used in this repository
- **Example**: a concrete intuition anchor
- **See**: where the term is used or defined more formally (by README section number)

---

## Core: meaning, information, judgment

### Semantic (as used here)

- **Definition**: The *state of being ready-to-judge*; not the “amount of information”, but the condition under which additional explanation is no longer required for action.
- **Example**: A pilot hearing “GO AROUND” does not need a detailed causal explanation to act.
- **See**: README §4.1 (판단 종료 조건으로서의 Semantic)

### Meaning

- **Definition**: The cognitive organization that makes an output *actionable* under limited attention; meaning is the form information takes when it can be used without expanding the search space of interpretations.
- **Example**: “This error is safe to ignore” is meaning; the raw stack trace is information.
- **See**: README §4.1, §5.2

### Information vs. Logical Information

- **Definition**:  
  - **Information**: signals/data/observations (may be unstructured or ambiguous).  
  - **Logical information**: information arranged into explicit stepwise relations (premise → inference → conclusion) that can be followed, but may still fail to become meaning under human cognitive limits.
- **Example**: A long chain-of-thought can be logically consistent yet still not help a reviewer decide “ship or not”.
- **See**: README §1.1, §1.2, §3

### Judgability

- **Definition**: Whether an output is usable for a concrete decision *now* (given the human’s current cognitive constraints and context).
- **Example**: A summary that includes the decision options + risk tradeoffs is often more judgable than a fully detailed analysis.
- **See**: README §2.2, §7.1

### Judgment Termination Condition

- **Definition**: The recognized “stop condition” where further explanation is not required, and the decision can be made without opening new interpretive branches.
- **Example**: “We have enough evidence to rollback; do it now.”
- **See**: README §4.1

---

## Knowledge organization: explicit/tacit

### Explicit Knowledge

- **Definition**: Knowledge whose meaning is organized enough to be explainable/transmittable with clear termination conditions.
- **Example**: A checklist for incident response.
- **See**: README §4.2

### Tacit Knowledge

- **Definition**: Knowledge that is hard to verbalize but still supports reliable judgment; often a compressed form that preserves meaning without full expansion.
- **Example**: A senior engineer’s “this feels risky” signal based on pattern recognition.
- **See**: README §4.2

---

## Atlas, charts, and manifolds

### Local Chart

- **Definition**: The currently selected “mode of understanding” for a problem (e.g., narrative explanation, numeric comparison, rule-based checking, embodied intuition).
- **Example**: Debugging a performance regression via flame graphs (numeric/structural chart) vs. user stories (narrative chart).
- **See**: README §4.4

### Semantic Atlas

- **Definition**: A multi-chart structure of meaning: multiple local charts coexist, but humans can only operate within a small subset at a time; failures occur when the system forces the wrong chart or too many charts at once.
- **Example**: A report mixing metrics, legal nuance, and architecture tradeoffs without a chart-selection guide can increase semantic entropy.
- **See**: README §4.3, §4.4, §5

### Physical Atlas

- **Definition**: A framing for physical systems where most states should remain within control/estimation loops, and only some boundary states should be promoted to “meaning/judgment” space.
- **Example**: A robot’s joint torque spike is usually a control event; repeated anomalies may become a judgment event (“stop and ask for human inspection”).
- **See**: README §6.1

### Modality Manifold

- **Definition**: The (informal) space formed by multiple modalities (text, vision, action, proprioception, environment state) where adjacency does not imply human interpretability; chart selection is required to make it judgable.
- **Example**: Camera frames + IMU streams + natural language goals need different charts depending on the decision.
- **See**: README §6.1, §6.2 (used as an extension point for future formalization)

---

## Metrics and failure modes

### Semantic Entropy

- **Definition**: The degree of interpretive freedom in a given information set; higher semantic entropy makes judgment convergence harder.
- **Example**: Five plausible root causes with no prioritization increases semantic entropy even if all facts are correct.
- **See**: README §5.2

### Meaning collapse / interpretation breakdown (working term)

- **Definition**: A failure mode where additional information increases uncertainty or defers decision because chart selection and termination conditions are not provided.
- **Example**: “Here are 12 options” without a decision rubric leads to analysis paralysis.
- **See**: README §1.2, §3, §5.2

---

## System roles (Agentic AI)

### Agent (as used here)

- **Definition**: A termination-and-transition mechanism: it decides whether to continue automation, switch charts, stop, or request human input—rather than “doing everything”.
- **Example**: The agent halts deployment when evidence crosses a threshold and presents a minimal decision packet to a human.
- **See**: README §6.2, §7.1

