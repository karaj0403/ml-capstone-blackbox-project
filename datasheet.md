# Datasheet

## Function Overview

This datasheet describes the optimisation of multiple black-box functions (Function 1–8).

- Each function represents a simulated real-world optimisation scenario  
- Input dimensions range from 2D to 8D  
- Output represents a performance score  

---

## Nature of the Data

- Data consists of sequentially generated query points  
- Dataset grows with each iteration  
- No external noise assumptions explicitly modelled  
- Functions show varying behaviour:
  - some smooth  
  - some multi-modal  
  - some difficult to explore  

---

## Optimisation Strategy

- Pattern-based optimisation approach  
- Identification of promising regions (clusters)  
- Gradual refinement using smaller step sizes  
- Balance between exploration and exploitation  

Strategy evolved from:
- broad exploration → structured refinement  

---

## Data Handling

- No explicit scaling required (values already in [0,1])  
- No surrogate models used  
- Outliers were treated as informative signals  

---

## Weekly Learning

- Early rounds improved understanding of function landscape  
- Later rounds focused on refinement  
- diminishing returns observed  

If restarted:
- more adaptive exploration strategy  
- earlier identification of key dimensions  

---

## Performance

- Best results achieved through local refinement  
- confidence moderate (possible local optima)  
- results aligned with expected optimisation behaviour  

---

## Ethical & Practical Considerations

- Reflects real-world optimisation under uncertainty  
- limited data is a key constraint  
- strategy is scalable but may require automation for larger systems  
- risk of missing global optima due to limited exploration  
