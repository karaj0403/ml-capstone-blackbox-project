# Model Card

## Model Description

**Input:**  
Numerical vectors with dimensionality between 2 and 8, with values in the range [0,1].

**Output:**  
A scalar value representing the performance of the input configuration.

**Model Architecture:**  
This project does not use a fixed machine learning model. Instead, it uses a **data-driven optimisation strategy** based on:

- pattern recognition  
- iterative refinement  
- cluster-based reasoning  

---

## Performance

Performance was evaluated based on:

- improvement in output values across iterations  
- stability of results in later rounds  
- convergence toward high-performing regions  

Observations:
- Faster convergence in low-dimensional functions  
- Slower progress in higher dimensions  
- diminishing returns in later stages  

---

## Limitations

- Limited query budget restricts exploration  
- No explicit model for uncertainty estimation  
- Sparse data in high-dimensional spaces  
- possible convergence to local optima  

---

## Trade-offs

- Exploration vs exploitation  
- Stability vs discovery of new regions  
- simplicity vs model-based optimisation  

The chosen approach prioritised interpretability and adaptability over complex modelling.
