# Dynamic-Slippage-Minimization

## 📈 Budget Allocation with Market Impact

This project implements and compares trading strategies for optimal allocation of a fixed budget across multiple time steps under temporary market impact.

---

## 🔬 Part 1: Slippage Function Estimation and Approximation

In the first part, we compute the **temporary market impact function** \( g(x) \) based on the structure of the ask side of the order book. The function is:

- Initially constant, then piecewise **hyperbolic** as deeper levels are consumed  
- Approximated on each segment using **piecewise quadratic functions** for smoother modeling and easier evaluation

This allows us to transition from discrete market data to a continuous, differentiable representation of trading cost.

---

## 📊 Part 2: Allocation Algorithms

We implement two allocation strategies:

- **Smart adaptive allocation**  
  Dynamically adjusts purchases based on urgency (time remaining) and slippage favorability (current vs expected slippage)
  
- **Naive baseline allocation**  
  Buys a fixed average amount at each time step (remaining budget / remaining steps)

The objective is to **minimize cumulative slippage** while fulfilling the total purchase budget over a fixed time horizon (e.g., 390 minutes in a trading day).

---

## 🔍 Key Features

- Analytical modeling of slippage using order book data  
- Piecewise quadratic approximation of the slippage function  
- Smart adaptive allocation algorithm balancing urgency and slippage  
- Baseline naive allocation strategy for comparison  
- Visualizations of slippage functions and allocation behavior  

---

## 🧠 Goal

Minimize total slippage when buying a target number of shares within a fixed number of time intervals (e.g. 390 trading minutes).
