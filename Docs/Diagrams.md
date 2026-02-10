# Diagrams (Semantic Atlas Hypothesis)

These diagrams are intentionally simple and meant to support discussion, not to “prove” the hypothesis.

---

## 1) Physical Atlas → Boundary State → Semantic Atlas

```mermaid
flowchart TD
  PhysicalAtlas["Physical Atlas\n(control/estimation loops)"] --> BoundaryState["Boundary State\n(transition to judgment)"]
  BoundaryState --> SemanticAtlas["Semantic Atlas\n(multi-chart meaning space)"]
  SemanticAtlas --> HumanMeaning["Human Meaning\n(actionable decision)"]
  Agent["Agent\n(termination & transition)"] --> BoundaryState
  Agent --> SemanticAtlas
```

**Reading**: Most physical states should remain in control space. Only *boundary states* should be escalated into semantic space, where chart selection and judgment termination become the design focus.

---

## 2) Chart selection loop (minimal)

```mermaid
flowchart LR
  Observe["Observe / Output"] --> Candidates["Candidate charts\n(narrative / numeric / rules / intuition)"]
  Candidates --> Select["Select chart\n(by context + cognitive budget)"]
  Select --> Transform["Transform info\n(compress / expand / reframe)"]
  Transform --> Decide["Decide\n(termination condition met?)"]
  Decide -->|No| Candidates
  Decide -->|Yes| Action["Action / Commit"]
```

**Reading**: The core failure mode is not “lack of information”, but missing chart selection + termination conditions, which causes semantic entropy to grow and decisions to be deferred.

