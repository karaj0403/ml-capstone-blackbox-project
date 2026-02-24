# Model Card — Sequential Bayesian Optimisation Strategy

## Overview

**Model name:** Sequential Bayesian Optimisation Strategy  
**Type:** Gaussian Process–based black-box optimiser  
**Version:** Round-10 workflow  

This approach performs sequential query selection to maximise unknown objective functions under a strict evaluation budget.

---

## Intended Use

### Appropriate Use Cases

This optimisation strategy is suitable for:

- Expensive black-box optimisation problems  
- Low- to moderate-dimensional continuous domains  
- Sequential experimentation under uncertainty  
- Educational demonstrations of Bayesian optimisation  

### Out-of-Scope Uses

This approach is **not recommended** for:

- Highly discontinuous objective functions  
- Extremely high-dimensional search spaces  
- Real-time optimisation with strict latency constraints  
- Safety-critical or production deployment without validation  

---

## Methodology and Evolution

The optimisation strategy evolved across ten rounds:

### Early Phase (Rounds 1–3)

- Broad space exploration  
- Larger step sizes  
- High uncertainty weighting  
- Limited structural assumptions  

### Middle Phase (Rounds 4–7)

- Balanced exploration–exploitation  
- Increased reliance on surrogate predictions  
- Identification of promising regions  
- Beginning of local refinement  

### Late Phase (Rounds 8–10)

- Precision-oriented adjustments  
- Smaller, dimension-aware perturbations  
- Gradual shift toward exploitation  
- Continued uncertainty monitoring in high dimensions  

Query selection was guided by Gaussian Process posterior mean and uncertainty estimates.

---

## Performance Summary

Performance was evaluated independently across the eight functions.

### Observed Trends

- Faster convergence in lower-dimensional functions  
- Slower and noisier improvement in 6D–8D cases  
- Evidence of diminishing returns after ~15–18 samples  
- Increased sensitivity to early sampling decisions  
- Persistent uncertainty in sparsely explored regions  

### Primary Metric

- Best objective value achieved per function over time  

---

## Assumptions

Key assumptions underlying the approach include:

- Local smoothness of objective functions  
- Informative uncertainty estimates from the GP surrogate  
- Moderately well-behaved noise  
- Independence between optimisation tasks  

These assumptions support efficient search but may not hold for highly irregular functions.

---

## Limitations and Failure Modes

Important constraints include:

- Limited query budget restricts global coverage  
- Gaussian Process may struggle with non-stationary behaviour  
- Sparse sampling in high dimensions  
- Sensitivity to early observations  
- Possible failure to detect narrow global optima  

Performance may degrade if the true function violates smoothness assumptions.

---

## Ethical and Transparency Considerations

Transparency is supported through:

- Full query history  
- Dataset datasheet  
- Explicit documentation of assumptions  
- Clear reporting of limitations  

Providing this model card helps prevent over-generalisation of results and supports responsible adaptation of Bayesian optimisation methods in real-world contexts.

---

## Reproducibility Notes

The optimisation workflow can be reproduced given:

- Query history  
- Observed outputs  
- GP kernel configuration  
- Acquisition strategy parameters  

Additional low-level hyperparameter logs would further improve exact reproducibility but are not required for conceptual replication.

---
