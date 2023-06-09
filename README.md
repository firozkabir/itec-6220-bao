---
marp: true
---

# Publication Review - Bao: Making Learned Query Optimization Practical

### Authors: 
- Ryan Marcus, MIT & Intel Labs <ryanmarcus@csail.mit.edu>
- Nesime Tatbul, MIT & Intel Labs <tatbul@csail.mit.edu>
- Parimarjan Negi, MIT <pnegi@csail.mit.edu>
- Mohammad Alizadeh, MIT <alizadeh@csail.mit.edu>
- Hongzi Mao, MIT <hongzi@csail.mit.edu>
- Tim Kraska, MIT <kraska@csail.mit.edu>

Presented at [SIGMOD ’21, June 20–25, 2021, Virtual - Event, China](https://doi.org/10.1145/3448016.3452838)

### Reviewed for ITEC-6220 by: Firoz Kabir

---
# Before We Get Started
- Practitioner's Lens
- Traditional Process
- Credit for Diagrams

---

# Traditional Optimization Process
- Identify slow sql
- Run explain plan
- Add hints to sql code 

---

# Learned Query Optimization
- Predict Performance
- Observe Actual
- Retrain


---

# Problem Description
- Long training time
- Inability to adjust to data and workload changes
- Tail catastrophe
- Black-box decisions
- Integration cost

---

# Deeper look at the problem
* Predict Performance
    - Inductive Bias
    - Tree Convolution
* Training 
    - Multi-Arm Bandit Problem (Exploration vs Exploitation)
    - Thompson Sampling
![Multi-Arm Bandit + Thompson Sampling](f_yt_bao_bandit.png)

---

# The Bao difference: 
- Short training time
- Robustness to schema, data, and workload changes
- Better tail latency
- Interpretability and easier debugging
- Low integration cost
- Extensibility

---

# Bao System Model:
![Bao System Model](f_02_bao_system_model.png)

---

# Bao Prediction Model: 
![Bao Prediction Model](f_05_bao_prediction_model.png)

---

![Bao Cost Comparison](f_07_bao_cost_comparison.png)

---

# Questions :question: