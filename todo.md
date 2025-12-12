# Add secondary layer to theory: domain, granularity, utility, timescales (control + adaptation), agency
20251205: From GPT51 chat: https://chatgpt.com/c/6933446a-4a94-8329-8b7a-87353766f5b4

1. Core definition

Intelligence

I = \dfrac{P}{R}
Intelligence is the predictive power P achieved per unit of resources R expended.

This is intentionally minimal. Everything else (domains, abstractions, agency, learning) sits under P and R.

⸻

2. Context parameters

Every measurement of intelligence is relative to a context:
	•	Domain D: the class of situations or tasks considered (e.g. “urban driving,” “arithmetic,” “short-term social interaction”).
	•	Granularity G: the level of abstraction or detail at which the domain is modeled (e.g. atoms vs rigid bodies vs traffic rules).
	•	Utility U: what counts as a good prediction in that context (e.g. safety, accuracy, reward, profit).

So more precisely, intelligence is:

I(D, G, U) = \dfrac{P(D, G, U)}{R(D, G, U)}

⸻

3. Prediction and resources

Predictive power P(D,G,U)
A measure of how well a system’s internal model matches what actually happens in domain D, at granularity G, under utility U.
	•	Practically: average score under some loss/utility function (accuracy, log-likelihood, expected reward, etc.) over the domain’s distribution of cases.

Resources R(D,G,U)
The total cost of achieving that predictive performance in that context.
	•	Can include: time, energy, computation, memory, data, money, human labor, etc.
	•	Defined at whatever system boundary you care about (single device vs entire training ecosystem).

⸻

4. Timescales

Two timescales matter:
	•	Control timescale \Delta t_c
	•	How quickly the system can act on the world using its current model.
	•	Examples:
	•	FSD control loop: milliseconds
	•	Manufacturing robot: milliseconds–seconds
	•	Tree physiology (stomata, leaf orientation): minutes–days
	•	Adaptation timescale \tau
	•	How quickly the system can change its model in a durable way to improve P/R.
	•	Examples:
	•	Calculator, deployed FSD model: \tau \to \infty (no self-update)
	•	Human learning: minutes–years
	•	Evolution acting on trees/animals: thousands–millions of years

Control is about using a model; adaptation is about changing it.

⸻

5. Agency

Agency A (qualitative, not a scalar here) describes how far a system:
	•	sets or reshapes its own goals,
	•	chooses where to explore in model/latent space,
	•	steers its own improvement of P/R.

Roughly:
	•	Low A: system is only optimized from the outside (evolution, engineers, training pipelines).
	•	High A: system can internally decide what to learn, where to explore, which errors to reduce.

⸻

6. Taxonomy under this framework

Given I(D,G,U) = P/R, \Delta t_c, \tau, and A, we can distinguish three broad classes:
	1.	Tool-like intelligences
	•	High I in a narrow domain.
	•	Fast control \Delta t_c.
	•	No meaningful self-adaptation (\tau \approx \infty).
	•	Near-zero agency A.
	•	Examples: calculators, manufacturing machines, a deployed FSD build, an LLM at inference.
	2.	Externally-optimized intelligences (evolution / training loops)
	•	Inner systems (organisms, models) have fixed or slow-changing behavior during their lifetime.
	•	An outer process (evolution, human engineers + GPUs) performs a slow search that improves I over generations/versions.
	•	Agency is mostly in the outer process, and even there can be very low (e.g. blind natural selection).
	3.	Self-adapting agentic intelligences
	•	Nontrivial I across multiple domains.
	•	Fast control \Delta t_c and relatively fast adaptation \tau within the same system.
	•	Non-negligible agency A: can pick goals, direct attention, and reorganize its own modeling to improve P/R.
	•	Example: humans (and, in principle, any future AI that can update its own models and training objectives online).

⸻

This keeps I = P/R as the core law, and treats:
	•	domains, granularities, and utilities as the coordinate system you measure in,
	•	timescales and agency as orthogonal dimensions that explain why calculators, trees, FSD, LLMs, and humans feel so different even though they’re all describable under the same metric.






# Research Questions and Tasks

# Unsorted (recategorize anything here first)
- Use Google Deep Research to aid researching: https://blog.google/products/gemini/google-gemini-deep-research/
- Theory could apply to the "intelligence" of systems, too. Like the scientific industry where they generate papers and patents. How "intelligent" is that system at creating actual value?
- Paper explaining predicitons < world models, so perhaps my predictions are not a great explanation for the core of intelligence and it should be upgraded to models? https://x.com/keyonV/status/1943730486280331460
- Systemic Intelligence: Add in more on innovation and systemic friction, like businesses fighting against innovation. Based on 2024 Nobel Prize in Economics. Wrote Journal entry + chatGPT convo: https://chatgpt.com/c/69178eea-64f4-8327-8475-7a9101b6ecf2

## Priority 1: Establish Novelty

### Initial Focus
1. [ ] Choose specific discipline for initial literature review
   - Evaluate candidate disciplines:
     - Cognitive Science (predictive processing, mental models)
       - **Note**: Good starting point due to multidisciplinary nature
     - AI/ML (universal intelligence measures)
     - Philosophy of Mind (intelligence theories)
     - Systems Theory (efficiency across scales)
     - Decision Theory (prediction and efficiency in decision-making)
   - Select ONE discipline based on:
     - Relevance to core theory
     - Accessibility of literature
     - Potential for establishing novelty
     - Connection to efficiency and prediction
   - Defer other disciplines for later investigation

2. [ ] Create separate Mental Models Theory project
   - Set up parallel project structure
   - Move mechanism-specific content there
   - Topics to cover:
     - Adaptability and updating mechanisms
     - Modular architecture
     - Model construction and refinement
   - Maintain connection to I = P/R as evaluation metric

### Foundational Questions
1. [ ] Address core theoretical questions (from Nicole):
   - Prediction vs. Problem Solving
     - How is prediction different than problem solving?
     - Is prediction a subset or superset of problem solving?
     - How do they relate in intelligence measurement?

   - Scope and Inclusivity
     - Are we explaining one type of intelligence or all types?
     - What makes our model particularistic or exclusivist?
     - How does it relate to other intelligence measurements?

   - Epistemological Foundations
     - What epistemological perspective does the theory assume?
     - How does it relate to behaviorism?
     - Investigate connections to positivism
     - Is our understanding constructionist/constructivist?

   - Success Metrics
     - How do we define success in prediction?
     - What value system underlies our assessment?
     - How do we measure efficiency across contexts?

2. [ ] Research positivism and its applications
   - Examine relevance to prediction-based intelligence
   - Consider implications for theory development

2. [ ] Research Decision Theory connections
   - Study relationship between decision-making and prediction
   - Examine efficiency in decision processes
   - Analyze how decision theory handles:
     - Resource constraints
     - Uncertainty
     - Meta-decision making
   - Consider implications for intelligence measurement

### Resource Access
1. [ ] Set up scholarly resource access through Nicole
   - Google Scholar access
   - Academic paper databases
   - Key journals in relevant fields

### Literature Review
1. [ ] Review and analyze existing predictive processing frameworks
   - Jeff Hawkins's On Intelligence
   - Karl Friston's free-energy principle
   - Bayesian brain theories

2. [ ] Study "The Embodied Mind: Cognitive Science and Human Experience" (from Nicole)
   - Analyze connections to prediction and efficiency
   - Consider implications for embodied cognition
   - Examine relationship between experience and intelligence
   - Note relevance to our theoretical framework

3. [ ] Study universal intelligence measures
   - Shane Legg and Marcus Hutter's work
   - Compare with our efficiency-based approach

4. [ ] Research metacognition
   - Review Wikipedia article and key papers
   - Connect to meta-prediction aspects

5. [ ] Analyze O1 mental models and missed connections
   - Review ChatGPT conversation
   - Identify potential gaps or oversights

### Differentiation Analysis
1. [ ] Document key differentiators from existing theories
   - Focus on efficiency-prediction integration
   - Highlight universal applicability
   - Emphasize resource independence

## Priority 2: Demonstrate Utility

### Intelligence Metrics
1. [ ] Develop metric: What's the least intelligent thing that can accomplish a given goal?
   - Consider efficiency in the context of minimal capabilities
   - Explore implications for measuring intelligence
   - Create practical measurement framework

2. [ ] Investigate intelligence across all scales
   - Going down: quantum systems, particles, atoms, molecules
   - Going up: societies, species, planets, galaxies, universe
   - As composable mental models: what is the collection of all of your mental models? How far can you decompose them?
   - Examine how predictive efficiency manifests at each level
   - Study emergence of collective intelligence across scales
   - Consider implications for universal laws of intelligence

### Case Studies
1. [ ] Document and analyze cases of ant colonies outperforming humans
   - Focus on collective intelligence implications
   - Compare predictive efficiency across species
   - Reference science.org article

2. [ ] Analyze real-world applications
   - Economic systems (capitalism vs. communism)
   - Government decision-making
   - AI systems

### Methodology Development
1. [ ] Design methods to measure predictive efficiency across different systems
2. [ ] Create frameworks for comparing intelligence while controlling for resources
3. [ ] Develop standardized metrics for cross-system comparison

### Mathematical Framework
1. [ ] Investigate implications of I = P/R formula
   - Define and measure P (Predictive Power)
     - Accuracy metrics
     - Scope/breadth of predictions
     - Time horizon considerations
   - Define and measure R (Resource Consumption)
     - Energy/computational resources
     - Time requirements
     - Memory/storage needs
   - Study edge cases:
     - Reflexes (high I through minimal R)
     - Supercomputers (potentially low I despite high P, due to massive R)
     - Collective intelligence (emergent P with distributed R)
   - Develop standardized measurement approaches
   - Consider implications for:
     - AI system design
     - Educational methods
     - Organizational decision-making

### Mental Models Theory Development
*Note: This is a separate theory about mechanisms of intelligence*
1. [ ] Research adaptability mechanisms
   - Study how systems update their models
   - Analyze costs and benefits of adaptation
   - Investigate modular architectures
   - Consider relationship to I = P/R measurement

2. [ ] Explore "Updater" model concept
   - How do systems evaluate new information?
   - What determines update costs?
   - How to measure update effectiveness?

3. [ ] Investigate modular intelligence
   - Study specialized prediction modules
   - Analyze module interaction costs
   - Consider architectural implications

## Priority 3: Theoretical Refinement

### Mental Models Investigation
1. [ ] Analyze mental models in the context of theory of mind
2. [ ] Work through a predictive model of a tree as case study
3. [ ] Investigate whether models always need inputs
4. [ ] Examine if mathematical equations possess intelligence through predictive power
   - Consider distinction between models and intelligent systems
   - Analyze role of organisms in using mathematical models for prediction

### Core Concepts
1. [ ] Clarify prediction definition for non-cognitive systems
   - Chemical reactions in slime molds
   - Collective behavior in ant colonies
   - Market dynamics

2. [ ] Explore relationship between creativity and predictive efficiency
   - Role of novelty in prediction
   - Balance between exploration and efficiency

3. [ ] Develop ethical framework for intelligence comparison
   - Consider implications for AI development
   - Address resource inequality issues

## Priority 4: Academic Development

### Literature Review
1. [ ] Review and summarize psychometrics literature
   - Focus on measurement methodologies
   - Identify applicable frameworks

2. [ ] Deep dive into metacognition research
   - Connect to meta-prediction aspects
   - Identify relevant experimental methods

### Paper Development
1. [ ] Outline academic paper structure
2. [ ] Identify target journals
3. [ ] Draft initial abstract

## Research Tasks

### Prediction in Non-Cognitive Systems
- [ ] Define formal criteria for distinguishing meaningful prediction from simple cause-effect responses
- [ ] Develop framework for analyzing predictive behavior in cellular automata and basic mechanical systems
- [ ] Research existing literature on prediction-like behaviors in simple organisms
- [ ] Create taxonomy of prediction types across different system complexities

### Meta-Prediction Formalization
- [ ] Research existing mathematical models of metacognition and self-regulatory systems
- [ ] Develop formal mathematical definition of meta-prediction vs standard prediction
- [ ] Design quantifiable measures for meta-predictive feedback loops
- [ ] Create framework for evaluating meta-predictive capabilities across different system types

### Empirical Validation Framework
- [ ] Design cross-domain intelligence comparison methodology
- [ ] Develop standardized metrics for measuring predictive efficiency
- [ ] Create testable predictions for theory validation
- [ ] Design pilot studies for different system types (biological, social, artificial)
- [ ] Identify key benchmarks for comparing intelligence across domains

### Ethical and Practical Considerations
- [ ] Analyze potential biases in efficiency-based intelligence measures
- [ ] Study implications for human-AI interaction and development
- [ ] Investigate ethical frameworks for intelligence measurement
- [ ] Examine potential societal impacts of universal intelligence metrics

### Case Studies
- [ ] Identify candidate systems for proof-of-concept studies
- [ ] Design comparative analysis framework
- [ ] Develop measurement protocols
- [ ] Create documentation templates for case study results

### Domain Analysis Framework
- [ ] Develop formal methodology for defining domain boundaries
- [ ] Create guidelines for domain-specific intelligence measurement
- [ ] Research how to properly weight and combine multiple domain scores
- [ ] Design validation framework for domain boundary definitions
- [ ] Study relationship between domain breadth and intelligence scores 