# Symmetric-Node-Pairing-Circuit-SNPC-60106-
A deterministic quantum circuit that initializes qubits into superposition, entangles them in a linear chain, and applies a uniform Z‑rotation derived from a fixed classical constant. Designed to demonstrate symmetry, parity, and coherent phase application across all qubits.
✅ README (with Math Appendix)

You can paste this directly into GitHub.

---

Symmetric Node Pairing Circuit (SNPC‑60106)

A Deterministic, Symmetric Quantum Phase‑Injection Circuit

---

Overview

The Symmetric Node Pairing Circuit (SNPC‑60106) is a compact, deterministic quantum circuit designed to demonstrate:

- uniform initialization  
- linear entanglement  
- constant‑derived phase rotation  
- return to computational basis  
- optional measurement  
- reproducible statevector simulation  

All qubits undergo identical transformations, emphasizing symmetry, parity, and coherence across the system.

---

Features

- Deterministic Z‑rotation derived from a classical constant  
- Linear entanglement chain  
- Fully reproducible statevector simulation  
- Optional measurement layer  
- Clean, interpretable structure suitable for research and teaching  

---

Code Structure

1. integrity_angle()
Computes the rotation angle:

\[
\theta = \frac{60106}{10000}\pi
\]

2. buildintegritycircuit()
Constructs the full quantum circuit:

1. Hadamard on all qubits  
2. CNOT chain  
3. RZ(θ) on all qubits  
4. Hadamard on all qubits  
5. Optional measurement  

3. simulate_statevector()
Runs the circuit on Qiskit’s statevector simulator.

---

Mathematical Appendix

1. Rotation Angle

The phase rotation applied to each qubit is:

\[
\theta = \left(\frac{C}{S}\right)\pi
\]

Where:

- \(C = 60106.0\) (integrity constant)  
- \(S = 10000.0\) (scaling factor)  

Thus:

\[
\theta = 6.0106\pi
\]

---

2. Initialization

Each qubit is placed into uniform superposition:

\[
|0\rangle \xrightarrow{H} \frac{|0\rangle + |1\rangle}{\sqrt{2}}
\]

---

3. Entanglement Chain

For qubits \(q0, q1, \dots, q_{n-1}\):

\[
\text{CX}(qi \rightarrow q{i+1})
\]

This produces a linear entanglement topology.

---

4. Phase Rotation

Each qubit receives:

\[
R_Z(\theta) = 
\begin{bmatrix}
e^{-i\theta/2} & 0 \\
0 & e^{i\theta/2}
\end{bmatrix}
\]

---

5. Basis Return

A second Hadamard transforms the state back into the computational basis for measurement or simulation.

---

6. Statevector Simulation

The final statevector is obtained via:

\[
|\psi{\text{final}}\rangle = U{\text{SNPC}} |\psi_0\rangle
\]

Where \(U_{\text{SNPC}}\) is the full unitary of the circuit.

---
