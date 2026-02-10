# Robot grasping: affordance breakdown at the boundary

## 0) One-line summary

A grasp policy can succeed frequently, yet fail catastrophically when the environment shifts (reflective surfaces, deformable objects) unless boundary states are detected and escalated.

## 1) Context

- Domain: Physical AI / manipulation
- Decision: continue autonomous grasp attempts vs. replan vs. ask for human help

## 2) What information existed

- Vision depth + segmentation + grasp candidates
- Control loop can keep trying “nearby” grasps
- But the system lacks a meaning-level statement: “the affordance model is invalid here”

## 3) Meaning breakdown

- Repeated failures produce more logs and candidate grasps (more information)
- Human operator still cannot quickly judge what changed

## 4) Local charts involved

- Geometric chart: grasp poses, point clouds
- Semantic-affordance chart: “is this object graspable with this end-effector under current conditions?”
- Mismatch: geometric details overwhelm; the operator needs the affordance chart

## 5) Semantic Atlas reframing

- Detect boundary patterns (repeated slip, inconsistent depth, unstable contact)
- Escalate with a compact packet: “affordance invalid likely due to X; recommend Y”

