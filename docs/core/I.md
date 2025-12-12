# I — Intelligence (in I = P / R)

In this theory, **intelligence (I)** is the **efficiency of achieving useful prediction** (P) per **resources consumed** (R).

A key rule:

**Never state I without stating the envelope.**
I is always conditional: *I(system, envelope)*.

See: `docs/concepts/envelope.md`.

---

## What I is

**I answers:** “How much *action-relevant prediction/control* does this system achieve, for how much cost, within a defined envelope?”

- If P goes up with the same R → I increases.
- If R goes down with the same P → I increases.
- If both improve → I increases a lot.
- If a change adds overhead without increasing action-relevant prediction → I decreases.
- If a system reliably chooses the right model/heuristic for the situation (good *meta-prediction*), that typically increases I by improving P for a fixed budget (or reducing R for a fixed P).

---

## I is about utility, not truth

P is **utility-weighted** prediction. A model can be “false” in representation yet sufficiently useful in a given envelope.

See: `docs/concepts/truth-vs-utility.md`.

---

## Composite systems: I applies to combined units

A major strength of I=P/R is that it can evaluate **combined systems** as a single unit:

- human + tool
- driver + car + dashboard
- pilot + cockpit + procedures
- AI agent + tools + workflow
- organization + processes + instrumentation

**Design implication:** You can increase overall I by shifting burden from the agent to the tool (reducing R), or by surfacing better action-relevant state (increasing P).

Example: A well-designed car dashboard is an **embodied pre-filter** that compresses high-dimensional reality into a low-latency, high-SNR, human-actionable channel—raising effective I for the driver+car system.

---

## Failure modes to watch

### “Truth tax”
More detailed information can *increase R* without increasing actionable prediction, lowering I.

### “Crying wolf / trust collapse”
Low-precision signals train users to ignore them, reducing effective P and wasting R.

### “Overhead inflation”
If the interface/process consumes attention/time, it reduces the budget available for state tracking and control. This often increases R and also reduces realized P.

---

## Working definitions (for later refinement)

- **P (Prediction):** actionable forecasting/control of future outcomes (especially under intervention), within an envelope.
- **R (Resources):** time, attention, compute, energy, training, coordination, money—anything consumed to produce/maintain P.
- **Envelope:** the task scope (domain, horizon, conditions, actions, stakes).

---

## Optional formalization: (D, G, U) as a compact envelope

If you want a compact parameterization, treat the envelope as including:
- **D (Domain):** the class of situations/tasks
- **G (Granularity):** the abstraction/detail level at which D is modeled
- **U (Utility):** what counts as “good” prediction/control (loss/reward/constraints)

Then you can write:
- **I(system | D, G, U) = P(system | D, G, U) / R(system | D, G, U)**.

This is equivalent to *I(system | envelope)*, just with a smaller named tuple.

---

## Levels of formalization (how to use I=P/R without losing readability)

A key feature of this theory is that it works at multiple levels of detail.

At low resources, **I=P/R is intentionally coarse**: it’s a fast, legible lens for reasoning about systems.
As you invest more resources, you can increase the accuracy of your analysis by specifying the **envelope** and decomposing **resources** more carefully.

This is (nicely) self-referential: **analyzing I=P/R is itself subject to I=P/R**.
A quick model is often the highest-I move when resources are scarce; deeper formalization spends more R to increase predictive accuracy about the system.

### Tier 0: Default (human-usable, most of the time)
State intelligence as conditional on a scope:

- **I(system | envelope)**

Rule: never report I without at least a minimal envelope.

See: `docs/concepts/envelope.md`.

### Tier 1: Envelope specification (make “useful” explicit)
Define the envelope fields you are assuming:

- goals / objective bundle
- **constraints** (must-not-violate thresholds)
- **preferences** (tradeoffs within constraints)
- horizon / decision timescale
- allowed actions (observe-only vs intervene)
- conditions (noise, novelty, adversaries, distribution shift)
- stakes / cost of error

Constraints and preferences live in the envelope because they define what counts as “useful prediction.”

### Tier 2: Resource decomposition (when overhead matters)
When needed, split resources into parts instead of treating R as a single blob:

- **R_total**
  - **R_overhead** (interface/process/coordination tax; ambiguity; alert spam)
  - **R_pred** (resources available for state tracking, prediction, and control)

This clarifies a common real-world effect:
- increasing overhead raises R and often lowers *realized* P by starving state tracking.

### Tier 3: Prediction decomposition (when causality/robustness matters)
When needed, split prediction into conceptually distinct types:

- passive forecasting (“what happens next?”)
- interventional prediction (“what happens if I do X?”)

And connect to the truth/robustness ladder:

- predictive (in-distribution)
- causal (intervention-robust)
- mechanistic (generative fidelity)

See: `docs/core/P.md` and `docs/concepts/truth-vs-utility.md`.

### Guiding principle
Only add formal detail when it increases clarity or changes a decision.
Otherwise, the extra notation becomes overhead and defeats the purpose of having a usable theory.

---

## Additional axes: timescales and agency (often necessary for comparisons)

I collapses “how good” and “how costly” into one ratio within an envelope. In practice, comparisons often need additional descriptors:

- **Control timescale (Δt_c):** how quickly the system can act using its current model/policy.
- **Adaptation timescale (τ):** how quickly the system can durably improve/change its model/policy (in-system).
- **Agency (A):** how much the system internally selects goals, exploration, and self-improvement of P/R (not assumed scalar here).

These help distinguish:
1) **Tool-like intelligences**: high I in a narrow envelope; fast Δt_c; τ ≈ ∞; low A.
2) **Externally-optimized intelligences** (evolution/training loops): the inner system is relatively fixed at runtime; an outer process improves I over generations/versions.
3) **Self-adapting agentic intelligences**: nontrivial I across multiple envelopes with relatively fast τ and non-negligible A.


## Open questions / knobs

- How to score I in practice (qualitative vs quantitative proxies)?
- How to compare different resource types (time vs attention vs compute)?
- How to handle multi-objective envelopes (safety vs speed vs comfort)?