# 🔬 Qiskit Circuit Analysis of My first quantum programm

This README walks through the step-by-step analysis of a 5-qubit quantum circuit and explains why the simulation output gives two results with equal probability.

---

## 🧪 Initial Setup

We start with all qubits in the |0⟩ state:

\[
|\psi_0\rangle = |00000\rangle
\]

---

## 🧠 Gate-by-Gate Quantum State Evolution

### 1️⃣ Hadamard on Qubit 0

\[
H|0\rangle = \frac{1}{\sqrt{2}}(|0\rangle + |1\rangle)
\]

State becomes:
\[
|\psi_1\rangle = \frac{1}{\sqrt{2}}(|00000\rangle + |10000\rangle)
\]

---

### 2️⃣ Pauli-X on Qubit 1

Flips q1 from |0⟩ → |1⟩ in both branches:

\[
|\psi_2\rangle = \frac{1}{\sqrt{2}}(|01000\rangle + |11000\rangle)
\]

---

### 3️⃣ Pauli-Z on Qubit 2

No effect since q2 = 0.

---

### 4️⃣ Pauli-Y on Qubit 3

\[
Y|0⟩ = i|1\rangle
\]

\[
|\psi_3\rangle = \frac{i}{\sqrt{2}}(|01010\rangle + |11010\rangle)
\]

---

### 5️⃣ CNOT (control = q1, target = q0)

Since q1 = 1 in both states, q0 flips:

\[
|\psi_4\rangle = \frac{i}{\sqrt{2}}(|00010\rangle + |10010\rangle)
\]

---

### 6️⃣ S Gate on Qubit 4

No effect since q4 = 0.

---

### 7️⃣ Toffoli (CCX: controls = q1 & q2 → target = q3)

q2 = 0 in both paths → no effect.

---

### 8️⃣ SWAP between Qubits 2 and 3

Swapping q2 and q3:

- `00010` → `00100`
- `10010` → `10100`

Final quantum state before measurement:

\[
|\psi_5\rangle = \frac{i}{\sqrt{2}}(|00100\rangle + |10100\rangle)
\]

---

## 🧮 Measurement and Output Interpretation

Qiskit reads output in this order:  
**q4 q3 q2 q1 q0**  
(e.g., rightmost bit is q0)

### Based on Simulation Output:

