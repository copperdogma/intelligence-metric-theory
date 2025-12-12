# P — Prediction (in I = P / R)

In this theory, **prediction is not the same as cognition** and not the same as “simulation.”
Prediction is about **useful, action-relevant anticipation of outcomes** within an envelope.

---

## What counts as prediction

A system has “P” if it reliably maps:
- current state (or observations/history)
- to actions or expectations
- in a way that matches future outcomes (within the envelope)

This can be achieved by:
- evolution (compiled into morphology/instinct)
- engineering (compiled into mechanism)
- learning/training (compiled into weights/policy)
- runtime inference/simulation (computed on the fly)

---

## Prediction does not require cognition

### Evolutionary / compiled prediction
A tree does not “simulate” the future. Its structure embodies what worked under selection pressure:
- slow adaptation timescale (τ)
- but effective local control behaviors (leaf orientation, chemical responses)

### Mechanical / engineered prediction
A purely mechanical tic-tac-toe solver can implement an optimal policy:
- no simulation required at runtime
- the “model/policy” is compiled into the mechanism

---

## Prediction is not necessarily simulation

Simulation is one implementation strategy:
- useful when environments are novel/variable
- costly in time/attention/compute

Compiled prediction is another:
- cheap at runtime
- less flexible outside the envelope

Both are “prediction” if they produce reliable outcome anticipation/control.

---

## Passive vs interventional prediction (critical split)

### Passive prediction (forecasting)
“Given what I observe, what will happen next?”
- useful for expectation and planning
- can be correlation-based

### Interventional prediction (control-grade)
“Given I do X, what will happen?”
- requires understanding of *levers* (what actions change)
- distinguishes correlation from causation
- dominates in tight control loops (driving)

**Cargo cults** are a canonical failure case:
- they copy surface correlates
- but lack control-grade predictive leverage
- interventions don’t produce the desired outcomes

---

## Dimensions of P (useful when comparisons get fuzzy)

P is not just “accuracy.” Common axes:

### Horizon
How far ahead the prediction/control remains reliable:
- short-horizon (tight control loops)
- medium-horizon (planning/coordination)
- long-horizon (strategy; slow dynamics)

The same system can have high P at one horizon and low P at another.

### Robustness (shift, novelty, adversaries)
How well P holds when conditions change:
- in-distribution only (fragile)
- distribution shift / novelty tolerance
- adversarial robustness (when the environment reacts to the predictor/controller)

### Depth / transfer ladder (predictive → causal → mechanistic)
How well predictions transfer under interventions and recombinations:
- **predictive** (correlational; can break under intervention)
- **causal** (intervention-robust when causal structure holds)
- **mechanistic** (generative; holds under deeper modifications/novel compositions)

This ladder interacts with the “utility not truth” point: mechanistic truth can be *one* way to get robust utility, but it’s not the only way.
See: `docs/concepts/truth-vs-utility.md`.

---

## Predictive power depends on envelope

P is only meaningful when scoped by:
- domain (what kinds of situations)
- horizon (how far ahead)
- allowed actions (observe-only vs intervene)
- conditions (noise, novelty, adversaries)
- stakes (cost of error)

See: `docs/concepts/envelope.md`.

---

## Realized P depends on available resources (P–R coupling)

Many systems (especially humans) have a fixed per-moment resource budget (attention/time).
If overhead consumes budget:
- **R increases**
- and **realized P often decreases** because state tracking and decision making are starved

This is why “noise” can functionally lower P: it inflates R and steals the bandwidth needed to maintain accurate situational models.

---

## Timescales matter

- **Control timescale:** how fast the system can act using its current model
- **Adaptation timescale (τ):** how fast the system can improve/change its model in a durable way

High P in a fast control loop can coexist with slow τ (trees) or infinite τ (fixed mechanisms).

(If useful as a standalone: `docs/concepts/timescales.md`.)

---

## Practical heuristics

- P is credited only if it is **actionable within the task’s decision time**.
- More “truth” is not automatically more P; often it is just more R.
- Interventional prediction is the “harder currency” than passive forecasting.