# AI Contribution Log (SLE-4)

**Course:** 02AML204 – Introduction to Artificial Intelligence  
**Student Name:** Manthan Amol Soni  
**PRN:** 25UAM032  
**Division:** A  
**Date:** 11 October 2026  

---

## 1. AI Tools Utilized
* **Primary AI Engine:** Google Gemini
* **Purpose:** Formatting structural alignment with the course SLE-4 Student Guideline, drafting the ADR technical narrative, and brainstorming oral viva defense questions.

---

## 2. Granular Task Breakdown

### A. What AI Helped With
* Structuring the ADR sections (Context, Decision, Alternatives Considered, Rationale, Consequences) strictly according to Section 4 and Section 6 of the SLE-4 guideline.
* Translating profiling numbers from `SLE2_25UAM032_Manthan_Amol_Soni.docx` (2.152 ms vs. 32.418 ms; 74 nodes vs. 1,280 nodes) into formal comparative prose.
* Formulating likely viva defense prompts addressing trade-offs, state space scaling (e.g., 15-puzzle), and C4 Container boundaries.

### B. What I Did Myself (Direct Engineering Ownership)
* **Algorithm Implementation (SLE-1 & SLE-2):** Authored the Python 8-puzzle solver, implementing board representation as a 9-element flat tuple, calculating valid sliding-tile neighbor shifts via `divmod`, and writing the BFS and depth-bounded DFS traversal functions.
* **Benchmarking & Profiling (SLE-2):** Configured and executed test runs using `time.perf_counter()` and `py-spy` on my local machine. Captured empirical data across 5 iterations (BFS: 74 nodes, 2.152 ms; DFS: 1,280 nodes, 32.418 ms) and generated SVG flamegraphs.
* **C4 Architectural Modeling (SLE-3):** Designed the Context, Container, Component, and Code diagrams on draw.io, establishing the separation between the Search Engine Core, Frontier Traversal Memory, and Visited State Management containers.
* **Architectural Decision Synthesis:** Formulated the decision to select BFS over DFS based on measured execution speed and shortest-path guarantees.
* **Oral Viva Preparation:** Prepared to defend design decisions, explain flamegraph observations, and discuss memory trade-offs during faculty examination.

---

## 3. Academic Integrity Reflection
AI tools were employed solely as an editorial and structural drafting assistant. All core Python code, benchmark profiling measurements, architecture diagrams, and decision rationales represent my original, independent academic work.
