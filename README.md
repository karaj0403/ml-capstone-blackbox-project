# Black-Box Optimisation (BBO) Capstone Project

---
## 📌 Project Overview

This repository contains my work for the Imperial College London Black-Box Optimisation (BBO) Capstone Project. The goal of the project is to optimise eight unknown objective functions under a strict query budget using principled sequential decision-making.

Across ten optimisation rounds, I progressively refined a Bayesian optimisation strategy, balancing exploration and exploitation while analysing uncertainty, scaling effects and late-stage convergence behaviour.

---

## 🎯 Objectives

- Optimise eight hidden black-box functions  
- Apply Gaussian Process–based Bayesian Optimisation  
- Operate effectively under limited query budgets  
- Analyse diminishing returns and uncertainty patterns  
- Maintain transparency and reproducibility  

---

## 🧠 Optimisation Strategy

The optimisation pipeline follows a **sequential Bayesian optimisation framework** using Gaussian Process (GP) surrogates.

### Early Rounds (1–3)
- Broad exploration of the search space  
- Larger step sizes  
- High uncertainty weighting  

### Middle Rounds (4–7)
- Balanced exploration–exploitation  
- Increased reliance on surrogate predictions  
- Identification of promising regions  

### Late Rounds (8–10)
- Precision-oriented local refinement  
- Smaller, dimension-aware perturbations  
- Controlled exploitation with residual exploration  

Query selection was guided by the GP posterior mean and uncertainty to manage the exploration–exploitation trade-off.

In later rounds, the search process increasingly reflected Bayesian optimisation principles, using surrogate-based reasoning to guide uncertainty-aware query selection.

---

## 📊 Key Observations

- Faster convergence in low-dimensional functions  
- Slower improvement in higher dimensions (6D–8D)  
- Evidence of diminishing returns after ~15–18 samples  
- Increasing sensitivity to early sampling decisions  
- Trade-off between robustness and aggressive exploitation  

---

## 📄 Documentation

To support transparency and reproducibility:

- 📑 [Dataset Datasheet](datasheet.md)  
- 📘 [Model Card](model_card.md)

These documents describe the dataset construction, optimisation assumptions, limitations and intended use.

---

## 📂 Repository Structure

├── datasheet.md
├── model_card.md
├── README.md
└── (other project files)


---

## ⚠️ Limitations

- Limited query budget constrains global exploration  
- Gaussian Process assumes local smoothness  
- Sparse coverage in high-dimensional spaces  
- Possible sensitivity to early observations  
- Narrow global optima may remain undiscovered  

---

## 🔍 Transparency Note

All optimisation decisions were made using a Gaussian Process–based Bayesian optimisation framework. The accompanying datasheet and model card document the assumptions, data characteristics and decision logic to support interpretability and reproducibility.

---

## 🔬 Reproducibility

The optimisation process can be reproduced given access to:

- Query history  
- Function evaluations  
- GP surrogate configuration  
- Acquisition strategy parameters
- All query decisions are logged sequentially, enabling the optimisation trajectory to be reconstructed and audited.

See the model card for full methodological details.

---

## 📚 Course Context

This project was completed as part of the **Imperial College London Machine Learning/AI programme**, focusing on practical black-box optimisation under uncertainty and constrained evaluation budgets.

---

## 🤝 Feedback

Feedback and suggestions are welcome.
