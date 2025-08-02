# 🧠 Reinforcement Learning Assignment 3: SARSA vs. Q-learning in Gridworld

This repository contains the implementation and analysis for Assignment 3 in the Reinforcement Learning course, taught by Prof. Alexander Y. Shestopaloff. The objective is to compare the performance of two model-free RL algorithms—**SARSA** and **Q-learning**—in a custom gridworld environment.

---

## 📁 Contents

- `RL_A3.ipynb` — Jupyter notebook with full implementation and plots
- `report.md` / `report.pdf` — Final report summarizing results and insights
- `README.md` — This file

---

## 📋 Environment Description

- Gridworld size: **5 × 5**
- **Start state**: Blue square (top-left)
- **Penalty states**: Red squares (−20 reward, return to start)
- **Terminal states**: Black squares (episode ends)
- **Other transitions**: −1 reward
- **Invalid moves**: −1 reward

The agent must learn to reach a terminal state while avoiding penalty zones and minimizing total negative reward.

---

## 🚀 Algorithms Implemented

- **SARSA (On-policy TD Control)**
- **Q-learning (Off-policy TD Control)**

Both use:
- ε-greedy action selection
- Learning rate (α): 0.1
- Discount factor (γ): 0.99
- Exploration rate (ε): 0.1
- 500 training episodes

---

## 📊 Results Summary

| Metric                     | SARSA     | Q-learning |
|---------------------------|-----------|------------|
| Avg Reward (All episodes) | −11.46    | −11.70     |
| Avg Reward (Last 50)      | **−7.12** | −8.16      |

- SARSA learns a safer, more stable path over time.
- Q-learning converges faster but stabilizes at a slightly lower performance.
- Both methods eventually avoid red penalty zones and reach terminal states efficiently.

---

## 🖼️ Visualizations

- Agent trajectory plots for both SARSA and Q-learning
- Sum of rewards per episode plotted across training
- Gridworld map visualization

> Sample trajectory comparison available in `RL_A3.ipynb`.

---

## 🧪 Reproducibility

To reproduce results:

1. Clone or download this repository  
2. Open the notebook: `RL_A3.ipynb`  
3. Run all cells from top to bottom

### 🔧 Requirements

Install required Python packages:
```bash
pip install numpy matplotlib
