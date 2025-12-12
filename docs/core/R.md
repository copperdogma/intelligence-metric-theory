# R — Resources (in I = P / R)

**R** is whatever the system must spend to produce/maintain useful prediction/control **within the envelope**.

R is not just compute. In many real systems, the binding constraint is time and attention.

---

## What counts as R

Common resource categories:
- **Time / latency:** decision deadlines, reaction time, processing time
- **Attention / bandwidth:** what can be tracked without losing the state
- **Working memory / cognitive load:** how much can be held and manipulated
- **Training / expertise:** learning the model, acquiring skill
- **Data:** samples/experience required to fit or update the model (including labeling/curation)
- **Compute / energy:** FLOPs, power, tokens, battery
- **Sensors / bandwidth:** measurement resolution, sampling, noise floors
- **Coordination overhead:** meetings, handoffs, bureaucracy, synchronization
- **Money / materials:** paid resources used to increase P

---

## Time is first-class

Time appears in two roles:
1) **As a cost** (time spent sensing/thinking/acting)
2) **As a constraint** (late predictions are not actionable and effectively don’t count)

A correct prediction delivered after the decision point is near-zero value.

---

## Overhead vs productive resources

A practical split:

- **R_overhead:** resources consumed that do not directly increase actionable prediction
  - UI confusion, alert spam, unnecessary process, unclear semantics
- **R_pred (or R_model):** resources applied to state tracking, prediction, and control

Design goal: minimize R_overhead so more budget can flow to R_pred.

This explains why “more instruments” can lower overall intelligence:
- it inflates overhead
- and starves state tracking
- lowering realized P

---

## Runtime vs “compiled” resources (system boundary matters)

Some systems achieve high realized P with near-zero *runtime* R because prediction is “compiled” into structure:
- evolution → morphology/instinct
- engineering → mechanisms/procedures
- training → weights/policy

Whether those upstream costs count in R depends on the **system boundary** you’re measuring.
Example: for an organism’s moment-to-moment intelligence, evolutionary cost is typically out-of-bound; for an AI product, training/infrastructure may be in-bound.

---

## R is envelope-dependent

The same system can have radically different R in different envelopes.

Example:
- diagnosing a car issue while parked (time-rich, attention available)
- driving on ice (time-poor, attention scarce)

---

## Practical measurement proxies (optional)

If you later want quantification, R can be proxied by:
- glance time / eyes-off-road time
- reaction latency
- error rates under time pressure
- training time to competence
- compute/time per decision
- coordination hours per outcome improvement

(Keep these as optional tools; the theory should stay usable without them.)