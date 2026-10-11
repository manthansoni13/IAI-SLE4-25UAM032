# IAI-SLE4-25UAM032
# SLE-4: Final Viva & Architecture Decision Record (ADR) Defense
**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Class:** SY B.Tech CSE (AI & ML) | Division: A  
**Semester:** VI  
**Student Name:** Manthan Amol Soni  
**PRN:** 25UAM032  

---

## 📌 Repository Overview

This repository documents the deliverables for **SLE-4 (Self-Learning Exercise 4)**, the culminating synthesis of the course practical sequence (SLE-1 through SLE-4).

The primary objective of SLE-4 is to record and defend a formal **Architecture Decision Record (ADR)** justifying the primary search strategy selection for the **3×3 8-Puzzle Solver**, grounded in:
1. **Empirical profiling measurements** collected during **SLE-2** using Python's `timeit` and `py-spy`.
2. **Structural container and component boundaries** established in the **C4 Architecture Model** during **SLE-3**.

---

## 🔗 Related Repositories & References

* **SLE-2 (Profiling & Benchmarking):** [manthansoni13/SLE2_02AML204](https://github.com/manthansoni13/SLE2_02AML204.git)
* **SLE-3 (C4 System Architecture):** [manthansoni13/IAI-SLE3-25UAM032](https://github.com/manthansoni13/IAI-SLE3-25UAM032.git)
* **Peer Reference Repositories:**
  * [koustubhchorade-hub/IAI_SLE-4_25UAM042](https://github.com/koustubhchorade-hub/IAI_SLE-4_25UAM042.git)
  * [aniketmane2007/SLE---2-AI---NEW---Profilling](https://github.com/aniketmane2007/SLE---2-AI---NEW---Profilling)
  * [aniketmane2007/IAI-Agent-25UAM045](https://github.com/aniketmane2007/IAI-Agent-25UAM045)

---

## 🏗️ Architecture Decision Summary

* **ADR Title:** Selection of BFS Over DFS for State-Space Exploration in the 8-Puzzle Solver
* **Status:** Accepted
* **Core Decision:** Adopt Breadth-First Search (BFS) as the default search engine strategy using a FIFO queue (`collections.deque`) and a closed hash set for visited state detection, while retaining Depth-First Search (DFS) strictly as an alternative baseline.
* **Empirical Evidence (from SLE-2):**
  * **BFS** reached the goal expanding **33 nodes** in **0.0541 ms**.
  * **DFS** reached the goal expanding **2,927 nodes** in **3.2204 ms**.
  * BFS achieved a **~60× faster execution time** and expanded **~88× fewer states** on the identical initial-to-goal configuration.

---

## 📂 Repository Contents

```text
├── README.md                           # Project documentation & summary
├── AI_CONTRIBUTION_LOG.md              # Detailed human vs. AI contribution log
├── SLE4_25UAM032_Manthan_Amol_Soni.docx # Formal Word submission file
└── docs/
    └── viva_preparation.md            # Quick-reference notes for viva defense
