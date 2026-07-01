# 8-Tile Problem using A* Search and Greedy Best First Search

This repository contains Python implementations of two informed search algorithms for solving the classic **8-Tile (8-Puzzle) Problem**.

## Overview

The 8-Tile Problem is a well-known Artificial Intelligence search problem consisting of eight numbered tiles and one blank space arranged on a 3×3 board.

The objective is to transform an initial configuration into the goal configuration by sliding tiles into the blank space.

This project implements:

- Greedy Best First Search (GBFS)
- A* Search

and compares their performance.

---

## Algorithms Implemented

### 1. Greedy Best First Search (GBFS)

**Heuristic Used**
- Number of Misplaced Tiles

**Evaluation Function**

```
f(n) = h(n)
```

GBFS expands the node that appears closest to the goal based solely on the heuristic value.

---

### 2. A* Search

**Heuristic Used**
- Manhattan Distance

**Evaluation Function**

```
f(n) = g(n) + h(n)
```

where:

- g(n) = path cost from the initial state
- h(n) = Manhattan Distance heuristic

A* guarantees an optimal solution when the heuristic is admissible.

---

## Initial State

```
4 1 _
2 6 3
7 5 8
```

## Goal State

```
1 2 3
4 5 6
7 8 _
```

---

## Project Structure

```
.
├── eight_puzzle_astar.py
├── eight_puzzle_gbfs.py
└── README.md
```

---

## Requirements

- Python 3.x

No external libraries are required.

---

## Running the Programs

### Greedy Best First Search

```bash
python eight_puzzle_gbfs.py
```

### A* Search

```bash
python eight_puzzle_astar.py
```

---

## Results

| Algorithm | Heuristic | Path Cost | Nodes Expanded |
|------------|-----------|-----------|----------------|
| Greedy Best First Search | Misplaced Tiles | 8 | 13 |
| A* Search | Manhattan Distance | 8 | 11 |

---

## Comparison

| Feature | GBFS | A* |
|----------|------|----|
| Evaluation Function | h(n) | g(n)+h(n) |
| Heuristic | Misplaced Tiles | Manhattan Distance |
| Optimal | No | Yes |
| Complete | No | Yes |
| Nodes Expanded | 13 | 11 |

---

## Conclusion

Both algorithms successfully solved the given 8-Tile Problem instance.

- Both reached the goal in **8 moves**.
- A* expanded **11 nodes**, while GBFS expanded **13 nodes**.
- A* performed better because it combines the path cost with the heuristic, making it both efficient and optimal.

---

## Author

**Jithin Mathew**

B.Tech – CSE (Artificial Intelligence & Machine Learning)

CHRIST (Deemed to be University)

Course: Introduction to Artificial Intelligence
