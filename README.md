# Project: Domain Randomization in Reinforcement Learning

This repository contains the implementation, evaluation, and documentation for **Project 21: Domain Randomisation** from the Real-World RL Homework curriculum[cite: 1].

##  1. Problem Formulation
* **State Space:** Continuous 4-dimensional vector containing cart position, cart velocity, pole angle, and pole angular velocity.
* **Action Space:** Discrete binary actions: push the cart left (`0`) or right (`1`).
* **Reward Function:** $+1$ reward awarded for every time-step the pole remains upright.
* **Environment:** OpenAI Gymnasium `CartPole-v1` augmented with a custom wrapper that dynamically randomizes physical attributes (cart mass, pole mass, and force magnitude) on every episode reset to bridge the "reality gap."

---

##  2. Implementation & Methodology
* **Algorithm:** Proximal Policy Optimization (PPO) implemented via Stable-Baselines3.
* **Baseline:** A standard PPO agent trained on fixed, default physics parameters.
* **Domain-Randomized Agent:** Trained using a custom wrapper altering physics uniformly across episodes.

---

##  3. Results & Evaluation

### Robustness Comparison
![Domain Randomization Results](domain_randomization_results.png)
*The domain-randomized agent successfully adapts to unseen, extreme physical configurations, achieving maximum performance compared to the baseline.*

### Generalization Curve
![Generalization Curve](generalization_curve.png)
*Evaluation across escalating pole masses mapping the exact thresholds where standard baseline policies degrade.*

---
