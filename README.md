# Assign 1

# Multi-Armed Bandit Algorithms: Stationary and Non-Stationary Environments

This repository contains code and reproducible results for experiments comparing various multi-armed bandit algorithms on stationary and non-stationary environments. 

It accompanies the report: *"Multi-Armed Bandit Algorithms – Stationary and Non-Stationary Environments"*.

## Algorithms Implemented

- **Greedy**
- **ε-Greedy** (tuned ε values)
- **Optimistic Greedy**
- **Gradient Bandit** (tuned α values)

## Experiments

### Part 1 – Stationary Bandit Problem
- 10-armed testbed
- 1000 simulations × 2000 time steps
- Metrics: Average reward, % optimal action

### Part 2 – Non-Stationary Bandit Environments
- Gradual Drift  
- Mean-Reverting Drift  
- Abrupt Change (with and without reset)  
- Consistent seeds and permutations used for reproducibility

## Reproducibility

**Important**:  
- The same 10 random seeds were used across all simulations for generating drift noise and permutations.  
- This ensures that differences in results are due to algorithmic behavior, not to varying noise.

## How to Run

```bash
# Clone the repo
git clone https://github.com/seriman96/Assign.git
cd Assign

# (Optional) Create environment
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run experiments
python RL_Assign1.ipynb



# Assign 2

## Reinforcement Learning: Gridworld Assignment

## 📘 Overview

This project explores how fundamental Reinforcement Learning (RL) algorithms perform in a small 5×5 Gridworld environment. The objective is to estimate state values and derive optimal policies using:

Dynamic Programming methods
Monte Carlo methods
Experiments are conducted in two different settings:

Infinite-horizon (non-episodic) gridworld
Episodic gridworld with terminal states

## 🗺️ Environment Details

Grid Size: 5x5 (25 states)
Actions: Up, Down, Left, Right
Special States:
Blue: +5 reward, jumps to Red
Green: +2.5 reward, jumps to Red or Yellow (50/50)
Red / Yellow: Normal behavior
Step Reward:
Valid move: 0
Invalid (off-grid) move: -0.5
Discount Factor (γ): 0.95

## ⚙️ Algorithms Implemented

Part 1 – Dynamic Programming
Policy Evaluation:
Bellman Equation (solved via linear algebra)
Iterative Policy Evaluation
Policy Optimization:
Brute-force Policy Improvement
Policy Iteration
Value Iteration

Part 2 – Monte Carlo Methods (Episodic Environment)
MC Control with Exploring Starts
MC Control with ε-Soft Policy
Off-Policy MC Control using Importance Sampling

## 📊 Key Observations

Blue state always has the highest value across all methods due to its high immediate reward.
Value Iteration converged faster than Policy Iteration.
Among MC methods, ε-soft policy gave the best performance (max V ≈ 4.6).
Off-policy control worked well but was more sensitive to variance in importance sampling.
## 📁 Files

Assign2_RL.ipynb – All code and visualizations are included in this Jupyter notebook.
## ▶️ How to Run

Clone this repo or open the notebook via GitHub.
Run all cells in order.
Requirements:
numpy
matplotlib
pandas
seaborn
pip install numpy matplotlib pandas seaborn
## 📌 Conclusion

This project demonstrates how different RL strategies affect convergence and policy quality even in simple environments. It’s a practical exercise in applying foundational RL concepts using tabular methods.
