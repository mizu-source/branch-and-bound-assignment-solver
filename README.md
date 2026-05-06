# branch-and-bound-assignment-solver
# Branch and Bound - Assignment Problem Solver

## Overview
This Python script solves the **Assignment Problem** using the **Branch and Bound** algorithm. Given a cost matrix where each agent must be assigned to exactly one task, it finds the optimal assignment that minimizes the total cost.

## Problem Description
The assignment problem involves assigning `n` agents to `n` tasks with a given cost matrix `C[i][j]` representing the cost of assigning agent `i` to task `j`. The goal is to find a one-to-one assignment that minimizes the total cost.

## Algorithm Features
- **Branch and Bound** with recursive exploration
- **Lower bound calculation** for pruning suboptimal branches
- **Real-time logging** of the search process
- **Backtracking** implementation
- **Optimal solution guaranteed** (exact algorithm)

## How It Works

### Lower Bound Calculation
For partial assignments, the algorithm calculates a lower bound by:
1. Summing costs of already assigned agent-task pairs
2. For each unassigned agent, adding the minimum possible cost among remaining tasks

### Pruning
If the lower bound for a partial assignment exceeds the current best solution, that branch is pruned (eliminated from further exploration).

## Usage

### Prerequisites
- Python 3.6 or higher
- No external dependencies (uses only `math` module)

### Running the Script
```bash
python assignment_solver.py
