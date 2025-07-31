#  Qiskit Circuit Analysis of My first quantum programm

This README walks through the step-by-step analysis of a 5-qubit quantum circuit and explains why the simulation output gives two results with equal probability.

---

##  Initial Setup

We start with all qubits in the |0⟩ state:

All qubits: `|00000⟩`

---

##  Gate-by-Gate Quantum State Evolution

### 1️ Hadamard on Qubit 0

 ψ₁ = (1/√2) × ( `|00000⟩` + `|10000⟩` )

---

### 2️ Pauli-X on Qubit 1

Flips q1 from |0⟩ → |1⟩ in both branches:

 ψ₂ = (1/√2) × ( `|01000⟩` + `|11000⟩` )

---

### 3️ Pauli-Z on Qubit 2

No effect since q2 = 0.

---

### 4️ Pauli-Y on Qubit 3

 ψ₃ = (i / √2) × ( `|01010⟩` + `|11010⟩` )

---

### 5️ CNOT (control = q1, target = q0)

Since q1 = 1 in both states, q0 flips:

 ψ₄ = (i / √2) × ( `|00010⟩` + `|10010⟩` )

---

### 6️ S Gate on Qubit 4

No effect since q4 = 0.

---

### 7️ Toffoli (CCX: controls = q1 & q2 → target = q3)

q2 = 0 in both paths → no effect.

---

### 8️ SWAP between Qubits 2 and 3

Swapping q2 and q3:

- `00010` → `00100`
- `10010` → `10100`

Final quantum state before measurement:

ψ₅ = (𝑖 / √2) × ( |00100⟩ + |10100⟩ )

---
##  Measurement

This final quantum state gives **equal probability** of collapsing to either `|00100⟩` or `|10100⟩`.  
Thus, in 4096 measurements (shots), we expect each state to occur approximately **2048 times**.  



