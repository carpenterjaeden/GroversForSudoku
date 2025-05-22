# Quantum Sudoku Solver: Grover's Algorithm on a 2×2 Puzzle

This project implements **Grover's algorithm** using [Qiskit](https://qiskit.org/) to find valid solutions to a **2×2 Sudoku puzzle** using a quantum circuit and simulates the results.

---

## Problem Statement

The solution to the 2x2 Sudoku grid is a 2x2 grid of 1s and 0s where no row or column contains the same number twice. 

### Marked Solutions

The solution is writted as a vector of 4 numbers where the first 2 numbers are the first row and the last 2 numbers are the second row. The following vectors are the two possible solutions to the puzzle:

- `|1001⟩`
- `|0110⟩`


---

## What This Notebook Does

1. **Imports Libraries**
   - Uses Qiskit for quantum programming and Matplotlib for visualization.

2. **Defines the Oracle**
   - Marks the two Sudoku-valid bitstrings by flipping their phase using multi-controlled gates.

3. **Applies the Diffuser**
   - Implements amplitude amplification to boost the probability of measuring a valid Sudoku solution.

4. **Measures the System**
   - Collapses the quantum state to classical results and displays the quantum circuit.

5. **Runs Simulation**
   - Uses the `qasm_simulator` from Qiskit Aer to simulate 1024 measurement shots.

6. **Displays a Histogram**
   - Shows which outcomes occurred most frequently. The valid Sudoku states should dominate.

---

## Results

You should see a histogram where the bitstrings `1001` and `0110` have the highest probabilities — these correspond to valid 2×2 Sudoku solutions identified by Grover’s algorithm.

---

## ▶️ How to Run

1. **Install Required Packages**

```bash
pip install qiskit qiskit-aer matplotlib
