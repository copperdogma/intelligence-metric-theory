# Envelope: The Scope Template

## Why Envelope is First-Class

The question "I for what domain / timescale / conditions?" is foundational. Without explicit envelope specification, the theory risks becoming "I is whatever I feel like today."

Every intelligence measurement must specify its envelope—the complete scope of conditions under which the measurement applies.

## Envelope Template

Every example and document should reference this template when defining intelligence measurements:

### 1. Domain + Goal
- **Domain**: The class of situations or tasks considered (e.g., "urban driving," "arithmetic," "short-term social interaction")
- **Goal**: What the system is trying to achieve or optimize for

### 2. Horizon
- **How far ahead**: The temporal scope of predictions
  - Immediate: next 200ms, next second
  - Short-term: next minute, next hour
  - Medium-term: next day, next week
  - Long-term: next month, next year
  - Evolutionary: next generation, thousands of years

### 3. Intervention Class
- **Observe-only**: System only predicts what will happen (passive forecasting)
- **Act-and-see**: System predicts consequences of its own actions (interventional prediction)

Most real-world intelligence involves act-and-see scenarios.

### 4. Distribution Assumptions
- **In-distribution**: Predictions only tested under conditions similar to training/development
- **Out-of-distribution**: Predictions must hold under novel conditions, distribution shifts, or unexpected scenarios

### 5. Stakes
- **Cost of being wrong**: The consequences of prediction failure
  - Low-stakes: Minor inconvenience, easily corrected
  - Medium-stakes: Moderate cost, some recovery possible
  - High-stakes: Severe consequences, difficult or impossible to recover

Stakes determine the required accuracy and robustness of predictions.

## Example: Car Dashboard Intelligence

**Envelope:**
- **Domain + Goal**: Urban driving, avoiding collisions while maintaining reasonable speed
- **Horizon**: Next 200ms to next 5 seconds
- **Intervention Class**: Act-and-see (predicting consequences of steering, braking, accelerating)
- **Distribution Assumptions**: Must work in-distribution (normal driving conditions) and some out-of-distribution scenarios (unexpected obstacles, weather changes)
- **Stakes**: High (safety-critical, potential for serious injury or death)

## Example: Tree Physiology

**Envelope:**
- **Domain + Goal**: Survival and growth, optimizing resource acquisition
- **Horizon**: Minutes to days (stomata control), years to decades (growth patterns)
- **Intervention Class**: Act-and-see (predicting consequences of opening/closing stomata, orienting leaves)
- **Distribution Assumptions**: Evolved to work across seasonal variations and environmental changes
- **Stakes**: High (survival depends on efficient resource use)

## Example: LLM Text Generation

**Envelope:**
- **Domain + Goal**: Natural language text generation, producing coherent and relevant responses
- **Horizon**: Next token to next paragraph (seconds to minutes of reading time)
- **Intervention Class**: Observe-only (predicting next tokens given context, no direct world action)
- **Distribution Assumptions**: Trained on broad distribution, but may fail on novel domains or edge cases
- **Stakes**: Variable (low for casual use, high for medical/legal applications)

## Using the Envelope

When documenting any intelligence measurement:
1. Always specify the complete envelope
2. Compare systems only within the same envelope
3. Note when envelope boundaries are being tested or expanded
4. Recognize that intelligence scores are meaningless without envelope specification

## Related Documents

- See [I.md](../core/I.md) for how envelope parameters factor into intelligence measurement
- See [P.md](../core/P.md) for how envelope affects predictive power requirements
- See [truth-vs-utility.md](truth-vs-utility.md) for how envelope relates to required depth of understanding

