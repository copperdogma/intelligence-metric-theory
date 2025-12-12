# Multi-objective / value-conflict envelopes

Many real-world envelopes are not single-goal. They involve:
- multiple objectives
- hard constraints
- tradeoffs and value conflicts
- stakeholders who disagree about priorities

This does not break I=P/R, but it requires an explicit upgrade:

**The envelope must include an objective structure, not just “the objective.”**

See: `docs/concepts/envelope.md`.

---

## The core issue

“Useful prediction” is goal-relative.

In single-objective domains, P is easy to interpret:
- “predict/control the outcome that wins”

In multi-objective domains, “winning” is not uniquely defined:
- safety vs speed
- accuracy vs latency
- privacy vs convenience
- efficiency vs robustness
- individual vs collective benefit

So two systems can differ in apparent intelligence because they optimize different tradeoffs.

---

## Make objectives explicit as a bundle (goal vector)

Define, in the envelope:
- **Objectives:** O1, O2, O3… (things you want more/less of)
- **Constraints (hard):** must not violate thresholds
- **Preferences (soft):** optimize once constraints are met

Then P becomes:

**P = ability to predict/control outcomes across the objective bundle under constraints.**

---

## Separate constraints from preferences (critical)

This avoids confusion and argument.

- **Constraints** define minimum acceptable behavior:
  - “don’t crash”
  - “don’t exceed budget”
  - “don’t leak private data”

- **Preferences** define optimization within constraints:
  - “arrive sooner”
  - “be comfortable”
  - “minimize fuel”

In I=P/R terms:
- constraint satisfaction is baseline competence (a floor)
- preference optimization is efficiency (how well you do once safe/legal/acceptable)

---

## Tradeoffs create a frontier (Pareto thinking, no math required)

With conflicting objectives, there is usually no single best solution.
There is a set of “non-dominated” tradeoffs (a frontier).

Comparisons must therefore specify:
- the constraint levels being held constant, and/or
- which part of the tradeoff frontier matters for this envelope

Otherwise “more intelligent” may simply mean “values different.”

---

## When one scalar I is not enough

If value conflicts are central, consider reporting:
- **I(system, envelope)** with explicit objective bundle and constraints, or
- multiple intelligence claims for different envelopes:
  - I_safety, I_speed, I_cost, I_privacy, etc.

This preserves comparability without pretending the values are settled.

---

## Values disagreement can be modeled as R

In social systems, disagreement about objectives increases resources required:
- negotiation
- legitimacy-building
- coordination
- enforcement and compliance overhead

So value conflict can show up as increased R even if predictive capability is high.

---

## Summary claim

Multi-objective domains do not invalidate I=P/R.
They require that envelopes explicitly define:
- the objective bundle
- hard constraints
- acceptable tradeoffs

Intelligence claims remain valid only relative to that declared structure.