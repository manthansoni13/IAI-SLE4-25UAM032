# IAI-SLE4-25UAM032
# SLE-4: Final Viva & Architecture Decision Record (ADR) Defense
**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Class:** SY B.Tech CSE (AI & ML) | Division: A  
**Semester:** III 
**Student Name:** Manthan Amol Soni  
**PRN:** 25UAM032  

---

## 📌 Repository Overview

This repository hosts the final deliverables for **SLE-4 (Self-Learning Exercise 4)**, which serves as the capstone evaluation for the course practical progression (SLE-1 through SLE-4).

The core objective of SLE-4 is to formally document and defend an **Architecture Decision Record (ADR)** that justifies the key algorithmic and structural decisions adopted for the **3×3 8-Puzzle Solver System**. This decision is directly grounded in:
1. **Empirical Benchmarking Metrics (SLE-2):** Real execution times captured using `time.perf_counter()` and node expansions verified via `py-spy` call-stack flamegraphs.
2. **C4 Architectural Modeling (SLE-3):** Modular decomposition across Context, Container, Component, and Code levels isolating the Search Engine, Frontier Memory, and State Manager.

---

## 🔗 Related Repositories

* **SLE-2 (Performance Profiling & Flamegraphs):** [manthansoni13/SLE2_02AML204](https://github.com/manthansoni13/SLE2_02AML204.git)
* **SLE-3 (Full C4 Architecture Model):** [manthansoni13/IAI-SLE3-25UAM032](https://github.com/manthansoni13/IAI-SLE3-25UAM032.git)

---

## 🏗️ Architecture Decision Record (Summary)

* **ADR Title:** Selection of Breadth-First Search (BFS) over Depth-First Search (DFS) for State-Space Exploration in the 3×3 8-Puzzle Solver
* **Status:** Accepted
* **Core Decision:** Adopt Breadth-First Search (BFS) utilizing a FIFO queue (`collections.deque`) and an in-memory hash set for closed-state tracking as the primary operational search engine. Retain Depth-First Search (with a depth limit of $d=15$) solely as a secondary benchmark baseline.
* **Empirical Grounding:** In an identical 5-move optimal test configuration, BFS reached the goal in **2.152 ms** expanding **74 nodes**, whereas DFS required **32.418 ms** and expanded **1,280 nodes**—demonstrating a **~15× execution speedup** and an **~17× reduction in state expansions**.

---

## 📂 Repository Contents

```text
├── README.md                           # Overview, benchmark tables, and architecture context
├── AI_CONTRIBUTION_LOG.md              # Granular record of human vs. AI contributions
