# Truth vs Utility

## Core Question

"What kind of 'correctness' does P actually measure?"

**Answer**: Utility over truth. Wrong models can still be predictive enough for practical purposes. Cargo cults represent non-predictive bad models.

## The Predictive/Causal/Mechanistic Ladder

This ladder describes how deep the 'truth' needs to be for different kinds of usefulness, especially under interventions.

### Predictive (Correlational)
- **What it is**: Statistical patterns and correlations
- **Strengths**: Can achieve high accuracy for forecasting
- **Limitations**: May fail catastrophically under interventions
- **Example**: A model that predicts stock prices based on historical patterns, but fails when market structure changes

### Causal
- **What it is**: Understanding cause-effect relationships
- **Strengths**: Predictions hold under interventions that don't break causal structure
- **Limitations**: May fail when causal mechanisms themselves are modified
- **Example**: Understanding that smoking causes lung cancer allows prediction of intervention effects (quitting reduces risk)

### Mechanistic
- **What it is**: Deep understanding of underlying mechanisms
- **Strengths**: Predictions hold even when mechanisms are modified or combined in novel ways
- **Limitations**: Requires more resources to develop and maintain
- **Example**: Understanding the molecular mechanisms of drug action allows prediction of effects in novel combinations or contexts

## When Each Level is Sufficient

The required depth depends on the envelope (see [envelope.md](envelope.md)):

- **Low-stakes, in-distribution forecasting**: Predictive level may be sufficient
- **Interventions within known causal structure**: Causal level required
- **Novel interventions or mechanism modifications**: Mechanistic level required

## Wrong Models Can Still Be Useful

A model doesn't need to be "true" in a deep sense to be useful:

- **Useful approximations**: Models that are wrong but good enough for the task
- **Domain-specific accuracy**: Models that work well in their intended domain despite being incomplete
- **Pragmatic success**: Models that achieve goals even if they don't capture underlying truth

## Cargo Cults as Non-Predictive Bad Models

Cargo cults represent models that:
- Appear to have structure (rituals, behaviors)
- Lack predictive power (don't actually produce desired outcomes)
- Consume resources without delivering utility

This illustrates the distinction between having a model and having a useful model.

## Implications for Intelligence Measurement

1. **Utility-focused evaluation**: Intelligence is measured by practical outcomes, not theoretical correctness
2. **Context-dependent depth**: Required model depth depends on the envelope and stakes
3. **Efficiency matters**: Deeper models may be unnecessary if shallower ones achieve the same utility with fewer resources

## Related Documents

- See [P.md](../core/P.md) for how depth factors into predictive power
- See [envelope.md](envelope.md) for how stakes and intervention class determine required depth
- See [prediction.md](prediction.md) for broader discussion of prediction types

