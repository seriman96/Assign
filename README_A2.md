# Assign 2

## Reinforcement Learning: Gridworld Assignment

### 📘 Overview
This project explores how fundamental Reinforcement Learning (RL) algorithms perform in a small 5×5 Gridworld environment. 

The objective is to estimate state values and derive optimal policies using:

Dynamic Programming methods

Monte Carlo methods

Experiments are conducted in two different settings:

Infinite-horizon (non-episodic) gridworld

Episodic gridworld with terminal states

### 🗺️ Environment Details

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

### ⚙️ Algorithms Implemented

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

### 📊 Key Observations

Blue state always has the highest value across all methods due to its high immediate reward.

Value Iteration converged faster than Policy Iteration.

Among MC methods, ε-soft policy gave the best performance (max V ≈ 4.6).

Off-policy control worked well but was more sensitive to variance in importance sampling.

### 📁 Files

Assign2_RL.ipynb – All code and visualizations are included in this Jupyter notebook.

### ▶️ How to Run

Clone this repo or open the notebook via GitHub.

Run all cells in order.

### Requirements:

numpy

matplotlib

pandas

seaborn

pip install numpy matplotlib pandas seaborn

### 📌 Conclusion

This project demonstrates how different RL strategies affect convergence and policy quality even in simple environments. 

It’s a practical exercise in applying foundational RL concepts using tabular methods.
