# Pattern Taxonomy — Complete Reference Library

> Every pattern in this library has been observed across multiple unrelated domains.
> Cross-domain presence = strong signal of deep underlying law.

---

## STRUCTURAL PATTERNS (Geometry of Reality)

### P-01: The Power Law (Pareto / Zipf / Inverse Power)
**Formula:** P(x) ∝ x^(-α)  
**Observed in:** Word frequency (Zipf), city sizes, wealth distribution, earthquake magnitudes, book sales, social media followers, neural connection strengths, gene expression levels, meteor sizes  
**Core generator:** Preferential attachment — the rich get richer because early advantage compounds  
**Recognition signal:** When you plot on log-log axes and get a straight line  
**Implication:** Most effort is wasted. Find the 20% causing 80%. The top node matters disproportionately.  
**Questions it raises:** Why α? What determines the exponent?

---

### P-02: The Gaussian (Normal Distribution / Bell Curve)
**Formula:** P(x) ∝ e^(-(x-μ)²/2σ²)  
**Observed in:** Height, IQ scores, measurement errors, thermal noise, many biological traits  
**Core generator:** Sum of many independent random variables (Central Limit Theorem)  
**Recognition signal:** Outcomes cluster around mean; extremes are exponentially rare  
**CRITICAL:** Many phenomena that look Gaussian are actually power laws (financial returns, social influence). Misidentification is catastrophic — Gaussian tails are thin; power law tails are fat.  
**Implication:** If Gaussian: extremes are ignorable. If power law disguised as Gaussian: extremes will destroy you.

---

### P-03: Fractal Self-Similarity
**Formula:** D = log(N)/log(1/r) (fractal dimension)  
**Observed in:** Coastlines, mountain ranges, tree branching, lung structure, cardiovascular system, market price series, lightning, snowflakes, galaxy clustering, internet topology  
**Core generator:** Iterative application of a simple rule at all scales  
**Recognition signal:** Same structure at every zoom level; non-integer dimension  
**Implication:** The generator rule is always far simpler than the apparent complexity. Find the 3-5 line rule that creates the pattern.  
**Application:** If a phenomenon looks different at every scale, it's not fractal. If it looks the same → find the generator.

---

### P-04: Phase Transitions (Critical Points)
**Formula:** Order parameter ~ |T-Tc|^β near critical temperature  
**Observed in:** Water freezing/boiling, magnetic domains, population dynamics (collapse points), market crashes, species extinction cascades, opinion cascades, traffic jams, neural avalanches  
**Core generator:** System near a critical point where small changes produce large reorganization  
**Recognition signal:** Slowing down of fluctuations before transition; power law distributed fluctuations AT the transition  
**Implication:** Systems near critical points are maximally responsive (also maximally unpredictable). Evolution may push biological systems toward criticality because it maximizes information processing.  
**Warning signal:** When variance increases dramatically → system approaching phase transition

---

### P-05: Exponential Growth and Decay
**Formula:** N(t) = N₀ · e^(rt)  
**Observed in:** Population growth, compound interest, epidemic spread, radioactive decay, cooling, information diffusion, technological adoption curves  
**Core generator:** Current quantity is proportional to rate of change  
**Recognition signal:** Doubling time is constant  
**Critical distinction:** Exponential growth always looks slow at first, then suddenly explosive. Human intuition fails here catastrophically. The 30th doubling is a billion times the 1st.  
**Implication:** Early-stage exponential processes are systematically underestimated.

---

### P-06: S-Curves (Logistic Growth)
**Formula:** N(t) = K / (1 + e^(-r(t-t₀)))  
**Observed in:** Technology adoption, population growth with resource limits, species colonization, language spread, market penetration, skill acquisition  
**Core generator:** Exponential growth + carrying capacity constraint  
**Recognition signal:** Slow start → explosive middle → plateau  
**Implication:** Almost all growth processes are S-curves. The question is never "will it slow?" but "what is the K (ceiling)?" and "are we in the slow, fast, or plateau phase?"

---

### P-07: Oscillation and Resonance
**Formula:** d²x/dt² + 2γ(dx/dt) + ω₀²x = F(t)  
**Observed in:** Pendulums, predator-prey cycles, economic boom-bust, circadian rhythms, neural oscillations, cardiac rhythm, climate cycles, arms races  
**Core generator:** Feedback with delay (negative feedback + lag = oscillation)  
**Recognition signal:** Time-series crosses a mean value periodically  
**Resonance:** When external forcing matches natural frequency → catastrophic amplitude growth (Tacoma Narrows Bridge, debt spirals, emotional dysregulation)  
**Implication:** Find the natural frequency of the system. External forces matching it are uniquely powerful.

---

### P-08: Network Effects (Metcalfe's Law region)
**Formula:** Value ∝ n² (or n·log(n) in some formulations)  
**Observed in:** Telephone networks, social media, language standardization, market liquidity, legal systems, transportation hubs  
**Core generator:** Each new node adds connections to ALL existing nodes  
**Recognition signal:** Value or utility grows faster than membership  
**Implication:** Network effect markets converge to monopoly or duopoly. The winner is rarely the best product — it's the one that achieves network density first.

---

## DYNAMIC PATTERNS (How Systems Evolve)

### P-09: Punctuated Equilibrium
**Observed in:** Biological evolution (Gould & Eldredge), geology, technology history, organizational change, scientific paradigms  
**Pattern:** Long periods of stability → sudden rapid change → new stability  
**Core generator:** Systems accumulate stress/tension that is released discontinuously; small changes near critical points produce large effects  
**Recognition signal:** Long flatness then sudden jump in the data  
**Implication:** Most change doesn't happen gradually. Preparing only for gradual change leaves you exposed to punctuated change.

---

### P-10: Creative Destruction Cycles (Schumpeter)
**Observed in:** Technology industries, biological evolution, empires, scientific paradigms, art movements  
**Pattern:** Dominant form accumulates rigidity → challenger innovates at low end or different dimension → dominant form collapses → challenger becomes new dominant form → cycle repeats  
**Recognition signal:** The incumbent optimizes existing metrics while challenger creates new metrics  
**Key insight:** The incumbent cannot respond because the response would destroy their existing business/structure. The new framework always wins by changing what "winning" means.

---

### P-11: The Matthew Effect (Cumulative Advantage)
**Biblical source:** *"To him who has, more will be given"*  
**Observed in:** Scientific citation, wealth accumulation, talent identification in sports (relative age effect), language vocabulary, software library adoption, brand recognition  
**Core generator:** Early advantage → more exposure → more advantage → compounding  
**Recognition signal:** Success distribution is highly skewed; early movers dominate  
**Implication:** First is not always best, but first to network effects wins. Timing matters more than quality in Matthew Effect domains.

---

### P-12: Convergent Evolution
**Biological:** Eyes evolved independently ~40 times. Streamlined body shapes evolved independently in fish, dolphins, ichthyosaurs, penguins.  
**Broader pattern:** When the same environmental constraint exists, the same solution emerges independently.  
**Observed in:** Money (emerged independently in many cultures), writing (emerged independently in several places), democracy (multiple independent origins), calculus (Newton + Leibniz simultaneously)  
**Core generator:** Same problem + same constraints → same optimal solution  
**Implication:** If you see convergent evolution in a domain, the solution is not arbitrary — it is the local optimum under those constraints. Understand the constraints and you understand why the solution had to be what it is.

---

### P-13: The Red Queen Effect
**Source:** Evolution — prey must evolve to stay safe as predators evolve; predators must evolve to keep eating  
**Observed in:** Technology competition (constant innovation required just to maintain position), academic publishing, arms races, antibiotic resistance, social status competition  
**Pattern:** All parties run as fast as possible — just to stay in the same place  
**Recognition signal:** Enormous effort producing no relative progress  
**Implication:** Find the domains where Red Queen dynamics apply. In these domains, rest = loss. But also: find when everyone is Red-Queen racing and you can step out of the race.

---

## INFORMATION PATTERNS

### P-14: Signal-to-Noise Separation
**Core question:** Which variation is information; which is random?  
**Mathematical tool:** Shannon entropy, signal detection theory, Bayesian inference  
**Universal application:** In ANY domain with data (financial, medical, physical, social), most of what you observe is noise. Pattern recognition = distinguishing signal from noise.  
**Key principle:** More data reduces noise but never eliminates it. The question is always: how much evidence do I need before this pattern is real?  
**Practical tool:** If a pattern disappears when you double the sample size, it was noise.

---

### P-15: Information Compression (Kolmogorov Complexity)
**Principle:** The true complexity of a pattern is the shortest program that generates it.  
**Implication for pattern recognition:** If you have found a deep pattern, your description of it should be shorter than the data it explains.  
**Practical test:** Einstein's E=mc² — 5 characters explain an infinite number of specific mass-energy equivalences. That compression ratio signals deep truth.  
**When compression fails:** You haven't found the pattern; you've found a description.

---

### P-16: Emergence and Downward Causation
**Emergence:** The whole exhibits properties not present in the parts  
**Examples:** Consciousness from neurons, wetness from H₂O molecules, traffic jams from individual cars, markets from individual traders, life from chemistry  
**Downward causation:** The emergent level constrains the lower level (the organism constrains its chemistry; the market constrains individual traders)  
**Recognition signal:** You cannot predict the macro behavior from the micro rules (even in principle)  
**Implication:** Studying only the parts will never explain the whole. The pattern exists at the emergent level and must be studied there.

---

## HUMAN/SOCIAL PATTERNS

### P-17: The Hero's Journey (Campbell's Monomyth)
**Observed in:** Myths across all cultures and times, modern films/novels, personal transformation narratives, organizational change stories, scientific discovery narratives  
**Pattern:** Ordinary world → Call to adventure → Refusal → Crossing threshold → Tests → Ordeal → Reward → Return → Changed  
**Core generator:** Narrative structure that maps onto actual psychological transformation processes (initiation, death-of-old-self, rebirth)  
**Implication:** This structure persists because it describes something real about how humans change. Finding where you are in this structure in any change process is diagnostic.

---

### P-18: The Diffusion of Innovations (Rogers)
**Pattern:** Innovators (2.5%) → Early Adopters (13.5%) → Early Majority (34%) → Late Majority (34%) → Laggards (16%)  
**The Chasm:** Gap between Early Adopters and Early Majority — most innovations die here  
**Recognition signal:** Adoption S-curve; qualitative change in adopter type at each phase  
**Core generator:** Different groups have different risk tolerance and social network positions  
**Implication:** An innovation that has saturated Early Adopters has not proven it will cross the Chasm. Different strategy required for each phase.

---

### P-19: The Overton Window (Range of Acceptable Ideas)
**Pattern:** At any time, only a narrow range of ideas are politically/socially acceptable. Over time, this window shifts — often driven by ideas that start outside it.  
**Mechanism:** Radical ideas normalize moderate versions; crises shift the window rapidly; media attention shifts without formal endorsement  
**Recognition signal:** Today's heresy is tomorrow's orthodoxy (and vice versa)  
**Implication:** Ideas that seem impossible are often early — not wrong. Pattern: identify ideas just outside the window in the direction of movement.

---

### P-20: Dunbar's Number and Social Scaling
**Pattern:** Humans have cognitive limits on relationship complexity — ~5 intimate relationships, ~15 close friends, ~50 friends, ~150 stable social group  
**Observed in:** Hunter-gatherer bands, military companies, village sizes, optimal team sizes across many organizations  
**Core generator:** Neocortex size limits social complexity management  
**Implication:** Organizations above 150 people spontaneously develop bureaucracy, politics, and us-vs-them dynamics — because personal relationship networks break down. This is not a management failure; it is a cognitive architecture constraint.

---

## META-PATTERNS (Patterns About Patterns)

### MP-01: The Kuhn Cycle (Scientific Revolution Pattern)
**Stages:** Pre-science → Normal science → Anomaly accumulation → Crisis → Revolution → New normal science  
**Key insight:** Paradigm shifts don't happen by refuting the old paradigm — they happen by proposing a new one that subsumes it. The old guard doesn't convert; they die.  
**Pattern recognition use:** Identify which stage a field is in. Anomaly accumulation signals impending revolution. The next paradigm is often already being built in adjacent fields.

---

### MP-02: The Adjacent Possible (Kauffman)
**Principle:** At any moment, only certain next innovations are possible — those adjacent to what already exists. The adjacent possible expands as new things are created.  
**Implication:** Revolutionary ideas are not random — they are the next step in a combinatorial space. You can sometimes predict which new ideas are about to become possible by mapping what has recently become possible.  
**Application:** Find the prerequisites. If multiple prerequisites of an innovation are now in place, the innovation is in the adjacent possible. Build it before someone else does.

---

### MP-03: The Map Is Not the Territory (Korzybski)
**Principle:** Every pattern you recognize is a model — a simplified representation of reality. Reality has infinite complexity; your pattern has finite complexity. The pattern is always wrong somewhere.  
**Implication:** The question is not "is my pattern right?" but "where does my pattern break down?" Finding the breakdown defines the next discovery.  
**Practice:** Every pattern should have an explicit list of its known failure conditions. Absence of this list means the pattern-holder doesn't understand their pattern.

---

### MP-04: Fitness Landscape Navigation
**Concept (Wright, Kauffman):** Imagine a landscape of peaks (solutions) and valleys (failures). Evolution, learning, and optimization all navigate this landscape.  
**Key insight:** Local optima are not global optima. Once you climb a local peak, you must descend to find higher peaks.  
**Observed in:** Evolution, organizational strategy, machine learning, technological innovation, career optimization  
**Implication:** Long periods of optimization make paradigm shifts harder — you're far up a local peak. The most creative actors are often those who haven't over-optimized yet (beginners, outsiders, cross-domain thinkers).  
**Counter:** Deep expertise matters for navigating quickly once you know the peak to target.

---

## APPLICATION GUIDE

**When to apply which pattern:**

| Observation | First pattern to check |
|-------------|----------------------|
| A few items dominate | P-01 Power Law |
| System suddenly collapses/explodes | P-04 Phase Transition |
| Growth looks slow then suddenly fast | P-05 Exponential or P-06 S-Curve |
| Same solution in different contexts | P-12 Convergent Evolution |
| Everyone working hard with no relative gain | P-13 Red Queen |
| Group larger than 150 people | P-20 Dunbar's Number |
| Field seems stuck with many anomalies | MP-01 Kuhn Cycle |
| Multiple separate innovations happening simultaneously | MP-02 Adjacent Possible |
| Pattern breaks in an interesting case | MP-03 Map ≠ Territory → new discovery opportunity |
