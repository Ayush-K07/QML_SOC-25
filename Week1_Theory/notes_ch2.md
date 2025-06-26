# 🧠 Quantum Computing Notes – Chapters 2 (Nielsen & Chuang)
## 📘 Chapter 2 – Introduction to Quantum Mechanics

### 🔢 Qubits and State Vectors

- A qubit is described by a unit vector in 2D complex Hilbert space:
  \[
  |\psi\rangle = \alpha|0\rangle + \beta|1\rangle \quad \text{where } \alpha, \beta \in \mathbb{C}, \quad |\alpha|^2 + |\beta|^2 = 1
  \]

- **Dirac notation**:  
  - \( |0\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix} \), \( |1\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix} \)  
  - General state: \( |\psi\rangle = \begin{bmatrix} \alpha \\ \beta \end{bmatrix} \)

---

### 🔄 Measurement

- Measurement collapses the qubit state:
  - Probability of 0: \( |\alpha|^2 \), Probability of 1: \( |\beta|^2 \)
- Post-measurement state collapses to \( |0\rangle \) or \( |1\rangle \)

---

### 🎯 Quantum Gates

| Gate | Matrix | Description |
|------|--------|-------------|
| **X** (NOT) | \( \begin{bmatrix}0 & 1 \\ 1 & 0\end{bmatrix} \) | Bit-flip |
| **Z** | \( \begin{bmatrix}1 & 0 \\ 0 & -1\end{bmatrix} \) | Phase-flip |
| **H** (Hadamard) | \( \frac{1}{\sqrt{2}}\begin{bmatrix}1 & 1 \\ 1 & -1\end{bmatrix} \) | Creates superposition |
| **CNOT** | Acts on 2 qubits: flips second if first is 1 | Entanglement gate |

---

### 🤝 Tensor Products

- To combine qubits:  
  \[
  |0\rangle \otimes |1\rangle = |01\rangle = \begin{bmatrix}0 \\ 1 \\ 0 \\ 0\end{bmatrix}
  \]
- 2-qubit state lives in a 4D complex space.

---

### 🔗 Entanglement

- Example: Bell State  
  \[
  |\Phi^+\rangle = \frac{1}{\sqrt{2}}(|00\rangle + |11\rangle)
  \]
- Not separable: cannot be written as a tensor product of two individual qubit states.

---

### 🔄 Unitary Evolution

- Quantum state evolves by a **unitary operator \( U \)**:  
  \[
  |\psi\rangle \rightarrow U|\psi\rangle
  \]
- \( U^\dagger U = I \): guarantees norm is preserved.

---

## 📌 Summary

| Concept | Classical Analog | Quantum Behavior |
|--------|------------------|------------------|
| Bit    | 0 or 1           | Superposition \( \alpha|0\rangle + \beta|1\rangle \) |
| Logic Gates | AND, OR, NOT | Unitary gates (X, Z, H, CNOT) |
| Memory | Bit string       | Quantum register (tensor product) |
| Output | Deterministic    | Probabilistic (via measurement) |

---
