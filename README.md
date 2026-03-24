# Black-Box Optimisation (BBO) Capstone Project

---

## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

This project focuses on finding the best solutions when the system being studied is unknown and can only be tested through trial and error. By submitting different input values and analysing the results, I gradually identified patterns and improved my decisions over time. The approach involves exploring different possibilities early on and then refining promising solutions in later stages. This reflects real-world optimisation problems where decisions must be made with limited information and resources.

---

## DATA

The dataset consists of input-output pairs generated through iterative queries to eight unknown black-box functions.

- Inputs: Vectors ranging from 2 to 8 dimensions  
- Range: All values between 0 and 1  
- Outputs: Single scalar value representing performance  

The dataset grows over time as new queries are submitted in each iteration. No external datasets were used, and all data is generated within the optimisation process.

---

## MODEL

This project does not rely on a single predefined machine learning model. Instead, it uses an **iterative, pattern-based optimisation approach**.

Key ideas include:
- Identifying high-performing regions (clusters)  
- Observing directional trends across iterations  
- Refining solutions using smaller adjustments  

This approach was chosen because of:
- limited data  
- unknown function behaviour  
- need for interpretability  

---

## HYPERPARAMETER OPTIMISATION

Rather than tuning model hyperparameters, the optimisation focused on:

- Step size of parameter changes  
- Balance between exploration and exploitation  
- Selection of candidate regions for refinement  

Early rounds used larger variations (exploration), while later rounds used smaller, controlled adjustments (exploitation).

---

## RESULTS

The optimisation process showed:

- Rapid improvements in early rounds  
- Identification of stable high-performing regions  
- Diminishing returns in later rounds  

Key findings:
- High-performing inputs form clusters  
- Some dimensions influence results more strongly  
- Early exploration significantly impacts final results  
---
