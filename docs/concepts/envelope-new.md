# Envelope: the scope of an intelligence claim

**Rule:** Never report I (or P) without stating the **envelope**.

An “envelope” is the set of constraints that define:
- what the system is trying to do
- how fast it must do it
- under what conditions
- with what actions available
- and what failure costs exist

Without an envelope, “intelligence” claims are usually accidental category errors.

---

## Envelope checklist (minimal)

When you make an I=P/R claim, specify:

1) **Goal / objective**
2) **Domain**
   - what situations count as “in scope”
3) **Horizon / decision timescale**
   - milliseconds vs seconds vs days vs generations
4) **Actions available**
   - observe-only vs intervene
   - what interventions are allowed
5) **Conditions**
   - noise, uncertainty, novelty, adversaries, distribution shift
6) **Stakes**
   - cost of being wrong (safety, money, reputation, etc.)

---

## Example envelopes

### Driving envelope
- goal: reach destination safely
- horizon: 0–5 seconds control loop
- actions: steering/brake/throttle
- conditions: weather, traffic, visibility
- stakes: high

### Diagnosis envelope
- goal: identify fault
- horizon: minutes to hours
- actions: inspect/test/measure
- conditions: time-rich, can consult manuals
- stakes: medium

### Evolutionary niche envelope (tree)
- goal: reproductive success
- horizon: seasons to generations
- actions: morphology/chemistry (fixed per organism)
- conditions: environmental variation
- stakes: existential but slow

---

## Why this matters

- It resolves debates like “tic-tac-toe machine vs human intelligence”:
  - machine: high I in a narrow envelope
  - human: broader envelope, different tradeoffs
- It prevents misuse of I=P/R as a universal ranking without context.