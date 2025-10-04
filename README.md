# Regional Office Optimization — Ram Wireless

## Project Overview
This project models a **regional office realignment optimization problem** for *Ram Wireless*, a telecommunications service provider.  
The goal is to determine the most cost-efficient assignment of store locations to regional offices and managers while minimizing **travel distance**, **salary cost**, and **workload imbalance**.  

The problem is formulated and solved using **Python (AMPL integration)** and supported by data-driven analysis in Excel.  
This project represents a complete **prescriptive analytics case**, applying **linear and mixed-integer optimization** techniques to a real-world-style business scenario.

---

## Business Problem
Ram Wireless operates several retail stores managed under different regional offices.  
The company seeks to redesign its regional alignment strategy to:
- Reduce total operational cost  
- Balance manager workload  
- Minimize travel distance between offices and assigned stores  

The decision involves reassigning stores to regional offices under constraints such as:
- Capacity and managerial limits  
- Geographical and workload considerations  
- Salary-based cost weights  

---

## Objectives
The model aims to:
1. **Minimize total cost**, including travel and managerial costs  
2. **Ensure workload balance** across managers and regions  
3. **Respect capacity constraints** and maintain feasible assignments  

---

## Model Formulation

**Decision Variables**
- `x_ij` = 1 if store *i* is assigned to regional office *j*, else 0  
- `y_j`  = 1 if regional office *j* is active, else 0  

**Objective Function**

Minimize Z = Σ (c_ij * x_ij) + Σ (f_j * y_j)

where:
- c_ij = cost of assigning store i to regional office j  
- f_j  = fixed cost of operating office j  

**Subject to**
1. Each store is assigned to exactly one office:  
   Σ_j x_ij = 1  for all i  

2. Workload balance and capacity limits:  
   Σ_i (workload_i * x_ij) ≤ capacity_j  for all j  

3. Binary restrictions:  
   x_ij ∈ {0,1},  y_j ∈ {0,1}  

---

## Methodology

| Phase | Focus | Tools | Deliverables |
|-------|--------|--------|--------------|
| **Phase I** | Cost-minimization realignment model | AMPL, Python | Optimal assignment with cost baseline |
| **Phase II** | Balanced workload optimization | AMPL, Python | Enhanced model integrating workload constraints |

---

## Implementation

### Tools and Technologies
- **AMPL** — for algebraic model formulation and solving  
- **Python (Google Colab)** — for data preprocessing and automation  
- **Excel** — for data setup and validation  
- **Linear & Mixed-Integer Programming (LP/MIP)** — for optimization  


---

## Results and Insights

| Phase | Objective | Key Result | Insights |
|-------|------------|------------|-----------|
| **Phase I** | Minimize total cost | **$192,000** | Derived optimal store–office assignment minimizing combined travel and salary costs. |
| **Phase II** | Balance workload + minimize cost | **$195,000** | Achieved improved workload distribution with only a marginal cost increase (~1.6%). |

**Key Findings**
- Workload balance improved significantly across regional managers.  
- The optimized configuration reduced excessive travel between certain store–office pairs.  
- The slight cost increase in Phase II was justified by better productivity and operational balance.

---

## Key Takeaways
- Demonstrates **end-to-end prescriptive analytics**: data preparation → model formulation → optimization → insight generation.  
- Applies **Linear & Mixed-Integer Programming** to a realistic business structure.  
- Integrates **AMPL** and **Python**, showcasing flexibility in analytical modeling.  
- Balances cost efficiency with workload equity — a real-world trade-off scenario.

---

## Author
**Shreya Mishra**  
Business Intelligence & Data Analyst  
MBA in Business Analytics | Excel | Python | AMPL | Optimization Modeling  
Richmond, VA  

---

### Disclaimer
All data and entities used in this project are **simulated for academic and research purposes**.  
They do not represent any real organization or confidential information.

