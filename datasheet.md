# Dataset Datasheet — BBO Capstone Project

## Motivation

This dataset was created to support the Black-Box Optimisation (BBO) capstone project. The primary objective is to optimise eight unknown functions using a limited query budget while operating under complete structural uncertainty.

The dataset captures the sequential history of query submissions and corresponding function evaluations. It enables analysis of optimisation behaviour, exploration–exploitation trade-offs and surrogate model effectiveness in a constrained black-box setting.

---

## Composition

The dataset consists of:

- Query vectors submitted across multiple optimisation rounds  
- Corresponding scalar outputs returned by the evaluation system  
- Eight independent optimisation problems  
- Input dimensionality ranging from 2D to 8D  
- Approximately ten sequential rounds per function
- Across ten rounds, the dataset contains approximately 80 total query–evaluation pairs (eight functions evaluated sequentially).
- Each of the eight functions is treated as an independent optimisation task with its own query history. 

### Format

- Continuous numeric inputs in the range [0, 1]  
- Tabular structure (CSV-style logical organisation)  
- One record per query  

### Known Gaps and Characteristics

- Sparse coverage in higher-dimensional spaces  
- Increasing concentration near locally promising regions  
- Limited total evaluations per function  
- Uneven sampling density across the search space  

These characteristics reflect the strict query budget imposed by the capstone setting.

---

## Collection Process

Queries were generated sequentially using an uncertainty-aware optimisation strategy informed by Bayesian optimisation principles.

### Strategy Evolution

- Early rounds prioritised broad exploration  
- Middle rounds balanced exploration and exploitation  
- Later rounds focused on precision-oriented refinement  

Each new query was selected using the full history of prior observations.

### Time Frame

The dataset was accumulated progressively across ten optimisation rounds during the BBO capstone project.

---

## Preprocessing and Intended Uses

### Preprocessing

- No additional feature scaling required (inputs already bounded)  
- No label transformations applied  
- Data used directly for surrogate modelling  

### Intended Uses

This dataset is suitable for:

- Studying black-box optimisation behaviour  
- Evaluating Bayesian optimisation workflows  
- Analysing sequential decision-making under uncertainty  
- Educational demonstration of constrained optimisation  

### Inappropriate Uses

This dataset should **not** be used for:

- Supervised learning benchmarks  
- Claims of general optimisation superiority  
- Real-world system modelling without context  
- Safety-critical deployment scenarios  

---

## Distribution and Maintenance

### Availability

The dataset is available in this public GitHub repository as part of the BBO capstone project.

### Terms of Use

- Educational and research use only  
- No guarantees of real-world representativeness  

### Maintenance

Maintained by **Manoj Kumar**.  
Future updates may occur if additional optimisation rounds are performed.

---

## Transparency Statement

This datasheet is provided to improve reproducibility, interpretability and responsible reuse of the optimisation results. Known limitations and sampling biases are documented to prevent over-interpretation of performance.
