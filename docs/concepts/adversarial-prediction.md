# Adversarial prediction (deception) in I=P/R

Deception and adversarial environments do not break I=P/R, but they force one critical clarification:

**In adversarial worlds, “prediction” must be evaluated against reality/causal outcomes, not against appearances.**

Adversaries specifically try to make observations non-diagnostic.

---

## The core failure mode: predicting appearances

In non-adversarial settings, predicting observations often correlates with predicting reality.

In adversarial settings, an opponent can make *appearances* highly predictable while steering you wrong:
- a con artist’s reassuring story
- spoofed sensors
- propaganda narratives that predict their own messaging

So “P” cannot mean merely “predict what I will see/hear.”

---

## Split: appearance prediction vs outcome prediction under intervention

This is a conceptual split (no math required):

### Appearance prediction (easy to game)
“How well do I predict what I’m going to observe?”

- Can be high even when you’re being manipulated.
- High appearance prediction does not imply intelligence.

### Interventional / outcome prediction (harder to fake)
“If I act, what will actually happen?”

This is the “hard currency” of prediction in hostile environments:
- intervention forces contact with reality
- correlation traps are exposed by probes
- deceptive channels are less useful when actions test causal structure

This aligns with the earlier split in `docs/core/P.md`:
- passive forecasting vs prediction under intervention

---

## Adversaries increase R (verification overhead)

Adversarial pressure does not only reduce realized prediction; it often increases resource costs:
- verification
- redundancy
- audits
- secure channels
- slower decisions / higher latency
- cross-checking and triangulation

Net effect:
- **R increases**
- **realized P often decreases**
- therefore **I decreases**, matching the intuition that adversarial worlds are “harder.”

---

## Envelope additions for adversarial settings

To make I(envelope) honest in hostile environments, add:

1) **Adversary model**
   - is there an opponent?
   - what can they manipulate (signals, incentives, physical state)?
   - what capabilities and costs do they have?

2) **Verification budget**
   - what checks/interventions are allowed?
   - what latency is tolerable?
   - how costly is verification?

These fields prevent “intelligence” claims from accidentally assuming a friendly channel.

See: `docs/concepts/envelope.md`.

---

## Trust as a learned channel (cry-wolf dynamics)

Signals are only useful if users learn that they predict something worth acting on.

If a channel has frequent false positives:
- users rationally down-weight it to save attention (R optimization)
- the channel becomes ineffective in real danger
- effective P decreases

Example: stale construction signage trains drivers to ignore signs, increasing risk when signs become true again.

---

## Practical heuristics for adversarial robustness (math-free)

In hostile envelopes, higher-I systems tend to:

- **Triangulate**: prefer independent sources/channels
- **Track track-records**: weight sources by historical reliability
- **Probe cheaply**: small interventions to force reality-contact
- **Audit incentives**: “who benefits if I believe this?”
- **Resist Goodharting**: don’t optimize solely on gameable metrics
- **Minimize surface correlation reliance**: prefer causal levers

These heuristics increase outcome-prediction under intervention per unit of verification cost.

---

## Summary claim

**Adversarial environments require efficient prediction under manipulation.**
That typically means spending some R on verification to preserve reliable interventional prediction, while minimizing verification overhead.

This fits naturally into I=P/R without changing the core framing.