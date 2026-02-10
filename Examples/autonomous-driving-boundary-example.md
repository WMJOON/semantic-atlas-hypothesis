# Autonomous driving: control ↔ judgment boundary

## 0) One-line summary

Autonomy performs well in nominal conditions, but rare boundary states (construction zones, unclear signage) require a clean escalation to human judgment that many systems fail to structure.

## 1) Context

- Domain: Physical AI / autonomy
- Decision: keep autonomous control vs. request takeover vs. minimal-risk maneuver

## 2) What information existed

- Sensors provide abundant state estimates (lanes, obstacles, localization)
- Planning stack produces multiple candidate trajectories with costs
- Yet the system cannot reliably communicate *why now* requires judgment

## 3) Meaning breakdown

- The human receives late/unclear takeover prompts
- “More data” (extra visual overlays, more trajectories) increases confusion
- Missing termination condition: “this is the smallest sufficient reason to take over”

## 4) Local charts involved

- Numeric chart: costs / risk scores
- Visual/embodied chart: what the driver can quickly understand from the scene
- Mismatch: system stays in numeric chart while the human needs an embodied/scene-level chart

## 5) Semantic Atlas reframing

- Promote only boundary-relevant features into a judgment packet (what changed, what is uncertain, what action is requested)
- Provide a stable termination condition: “take over now because X uncertainty + Y hazard exceeds threshold”

## 6) Agent decision points

- Escalate earlier when boundary uncertainty rises persistently (not only at failure)
- Keep low-level control details in Physical Atlas space unless needed for the judgment packet

