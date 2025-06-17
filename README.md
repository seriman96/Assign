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

