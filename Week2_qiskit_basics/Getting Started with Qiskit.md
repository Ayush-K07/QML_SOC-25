# 🧪 Week 2 – Getting Started with Qiskit

Welcome to **Week 2** of my quantum computing journey!  
This week focused on bridging **quantum theory** with practical coding by building quantum circuits using **Qiskit**, IBM’s open-source quantum programming framework.

---

## ✅ Week 2 Checklist

| Task                                         | Status | Description                                                                 |
|----------------------------------------------|--------|-----------------------------------------------------------------------------|
| Qiskit Installed                             | ✅     | Installed via `conda` and `pip`, tested in Jupyter Notebook                 |
| Basics of Quantum Information Course         | ✅     | Completed IBM's beginner course on qubits, gates, and measurements         |
| First Quantum Circuit Implemented            | ✅     | Designed and simulated a multi-qubit circuit using Qiskit                  |

---

## 📘 Notes – Nielsen & Chuang (Ch. 4.1–4.4)

### 4.1 – Quantum Circuit Model
- Quantum circuits are made of **quantum registers**, **classical registers**, and **gates**.
- Each gate is a **unitary transformation** on quantum state vectors.
- Measurement collapses the quantum state to a classical outcome.

### 4.2 – Quantum Gates
- **Single-Qubit Gates**: H (Hadamard), X (NOT), Y, Z, S, T
- **Multi-Qubit Gates**: CNOT, SWAP, Toffoli (CCX)
- Gates are represented as matrices and act on qubits as linear transformations.

### 4.3 – Circuit Diagrams
- Time flows from left to right.
- Qubits represented as horizontal wires.
- Gates are boxes or symbols (e.g. `⊕` for CNOT).

### 4.4 – Universality
- Any quantum computation can be constructed from combinations of **single-qubit gates + CNOT**.
- These form a **universal gate set**.

---
