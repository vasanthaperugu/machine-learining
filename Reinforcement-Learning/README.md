# Reinforcement Learning: Multi-Armed Bandits & Q-Learning

Exploring fundamental RL algorithms through digital ad optimization and robot navigation problems.

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Status](https://img.shields.io/badge/status-complete-success.svg)

---

##  Project Overview

This project implements and analyzes two core reinforcement learning problems:

1. **Multi-Armed Bandit** - Optimizing ad campaign click-through rates
2. **Q-Learning Grid World** - Teaching a robot warehouse navigation

### Key Results

| Problem | Best Approach | Performance |
|---------|--------------|-------------|
| Bandit | Decaying ε-Greedy | 723.1 clicks |
| Q-Learning | α=0.1, γ=0.99 | 89.55 avg reward |

---

##  Multi-Armed Bandit

### Results

| Strategy | Clicks |
|----------|--------|
| Decaying ε-Greedy | 723.1 |
| ε-Greedy (ε=0.1) | 714.8 |
| ε-Greedy (ε=0.3) | 680.5 |
| UCB | 515.9 |
| Random | 444.2 |

**Key Finding:** Large gaps favor aggressive early exploration then heavy exploitation.

---

##  Q-Learning

- Convergence: 300 episodes
- Final Reward: 89.55
- Steps to Goal: ~10

**Critical Discovery:** γ=0.5 failed. With 8-step paths, goal reward discounts to 0.39!

---

##  Tech Stack

Python • NumPy • Pandas • Matplotlib • Jupyter

---

##  Quick Start
```bash
pip install -r requirements.txt
jupyter notebook notebooks/RL_Assignment.ipynb
```

---

## 👤 Author

**Vasantha**  
GitHub: [@vasanthaperugu](https://github.com/vasanthaperugu)
