# Prediction (expanded): beyond cognition and simulation

Prediction, in this theory, is broader than conscious forecasting.

**Prediction is any reliable structure or process that maps current conditions (and actions) to future outcomes within an envelope.**

---

## Four implementation modes of prediction

### 1) Evolution-compiled
- selection pressure searches over time
- structures encode “what works”
- low runtime cost, slow adaptation

Example: trees, immune systems, reflexes.

### 2) Engineering-compiled
- designer does the search/analysis
- policy is embedded into mechanism
- runtime is cheap; adaptation is external

Example: mechanical solvers, engineered controllers.

### 3) Learned-compiled
- training learns a mapping
- deployed system executes it cheaply
- adaptation depends on retraining or online learning

Example: neural networks, trained policies.

### 4) Runtime simulated/inferred
- system computes futures on the fly
- flexible, but resource-expensive
- useful for novelty and planning

Example: human deliberation, search/planning algorithms.

---

## Simulation is optional

Simulation is one way to generate prediction, not the definition of prediction.
Many systems predict via compiled structure without runtime simulation.

---

## Passive vs interventional prediction

- Passive: “what happens next?”
- Interventional: “what happens if I do X?”

Most real control problems (driving, piloting, surgery, governance interventions) require interventional prediction to be safe and effective.

---

## Why tools can increase intelligence

Tools can:
- reduce R by pre-filtering and compressing state
- increase P by surfacing action-relevant variables
- shift overhead away from the agent

A well-designed interface raises effective I of the combined system by matching:
- human bandwidth limits
- task timescale constraints
- signal semantics and trust requirements

---

## A simple design test (no math)

For any signal/instrument:
1) What action does it change?
2) At what timescale does it matter?
3) Is the meaning unambiguous?
4) How often is it wrong/noisy?
5) Will it train people to ignore it?

If it fails these, it likely increases R more than it increases P.