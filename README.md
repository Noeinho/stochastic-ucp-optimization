# Multi-Scenario Stochastic Unit Commitment Problem (UCP)

This project implements a stochastic MILP (Mixed-Integer Linear Programming) model to solve the Unit Commitment Problem under uncertainty. Instead of a deterministic approach, this model optimizes the **expected cost** across multiple scenarios while ensuring system reliability.

## 📄 Full Report
👉 **[Read the Full Report (PDF)](./Rapport_UCP_Stochastique.pdf)** *(Note: Technical report is in French; code and README are in English)*

## 💡 Project Scope
The goal is to schedule power plant generation (Commitment and Dispatch) to meet demand while accounting for the variability of renewable energy sources.

- **Objective Function:** Minimization of the **Expected Total Cost** (sum of start-up and operational costs weighted by scenario probabilities).
- **Constraints:** The model enforces strict demand satisfaction and technical limits (ramping, min up/down time) across **all scenarios** simultaneously.
- **Robustness:** By satisfying the most extreme scenarios within the stochastic set, the model inherently builds a safety margin (spinning reserves) compared to a deterministic forecast.

## 🛠 Tech Stack
- **Language:** Python
- **Modeling:** PulP
- **Solver:** CPLEX
- **Documentation:** LaTeX

## 📊 Methodology
1. **Scenario Generation:** Modeling uncertainty in demand and renewable production
2. **Stochastic Formulation:** Writing the extensive form of the stochastic MILP.
3. **Analysis:** Evaluation of the "Value of the Stochastic Solution" (VSS) and system behavior under stressed scenarios.
