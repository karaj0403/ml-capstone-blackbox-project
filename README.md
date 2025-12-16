# Black-Box Optimisation (BBO) Capstone Project

## Project Overview

This repository contains my work on the Black-Box Optimisation (BBO) Capstone Project, where the objective is to optimise eight unknown functions under strict query constraints. Each function can only be accessed through input–output evaluations, and no information is available about the underlying functional form, gradients, or noise structure.

The goal of the project is to **identify high-performing input configurations using as few queries as possible**. This setting closely mirrors real-world machine learning and optimisation problems such as hyperparameter tuning, experimental design, and system optimisation, where evaluations are expensive and full system knowledge is unavailable.

From a professional perspective, this project strengthens key data science skills such as **decision-making under uncertainty, iterative experimentation, and communicating technical strategies**, all of which are essential in applied ML and analytics roles.

## Inputs and Outputs

### Inputs
- Each function accepts an input vector with dimensionality ranging from **2 to 8**
- All input values are constrained to the range [0, 1]
- Queries must be submitted in the following format:

x1-x2-x3-...-xn

where each value:
- starts with `0`
- is specified to **six decimal places**

Example (4D input):
0.156433-0.285223-0.752660-0.225294

### Outputs
- Each query returns a **single scalar value**
- The output represents the function’s performance at the queried point
- No gradients, uncertainty estimates, or structural information are provided

## Challenge Objectives

The objective of the BBO capstone project is to **maximise the output of each of the eight unknown functions** under the following constraints:

- A limited query budget per function
- Unknown and potentially non-linear response surfaces
- No access to gradients or analytical structure
- Delayed feedback between query submission and receiving results

Given these constraints, the challenge is to **select each query carefully**, balancing information gain with performance improvement.

## Strategy Evolution Across Weeks 1–3

This section summarises how my optimisation strategy evolved across the first three weekly query submissions.

### Week 1 – Initial Exploration
In the first round, my focus was on **broad exploration**. Queries were selected to sample different regions of the input space in order to understand the general behaviour and scale of each function without making strong assumptions.

### Week 2 – Identifying Promising Regions
With additional outputs available, the second round focused on **identifying promising regions**. Queries were adjusted based on observed performance, beginning to refine areas that showed higher output values while still maintaining some exploration.

### Week 3 – Focused Refinement with SVM-Inspired Reasoning
By the third round, my strategy became more selective. I prioritised **exploitation of high-performing regions** using small perturbations around strong inputs, while still exploring uncertain areas for poorly performing or unstable functions.

At this stage, my reasoning was influenced by **classification-style thinking**, inspired by Support Vector Machines (SVMs). Instead of predicting exact function values, I began viewing the input space as regions of **high vs low performance**. Conceptually:
- A soft-margin SVM could be used to classify inputs above or below a performance threshold while tolerating noise
- Kernel-based SVM could help separate non-linear high-performance regions in higher-dimensional spaces

Although I did not implement SVMs directly in code, these ideas informed how I balanced exploration and exploitation.

## Exploration vs Exploitation

Given the limited query budget, my approach balances:
- **Exploitation:** refining inputs near known high-performing regions
- **Exploration:** sampling new regions for functions with uncertain or poor performance

This balance is adjusted per function depending on observed behaviour and stability across rounds.


## Limitations and Future Directions

As more data becomes available, several limitations become apparent:
- Heuristic reasoning alone may struggle in high-dimensional spaces
- Interactions between input dimensions can be difficult to identify manually
- Some dimensions may be less influential, but require formal modelling to confirm

Future iterations may incorporate:
- Lightweight surrogate models (classification or regression-based)
- Feature relevance analysis
- More formal decision rules for query selection

This README is intended as a living document and will continue to evolve as the project progresses.
