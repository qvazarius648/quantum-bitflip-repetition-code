\# Quantum Bit-Flip Repetition Code



\## Overview

Manual implementation of a quantum bit-flip repetition code in Stim with realistic noise modeling and logical error rate scaling analysis.



\## Circuit Construction

\- Manual generation of data and ancilla qubits

\- Stabilizer measurement rounds



\## Noise Model

\- Depolarizing gate noise

\- Idle noise

\- Measurement X noise



\## Monte Carlo Simulation

\- Logical error rate estimation using majority vote

\- Syndrome statistics per round



\## Results



\### Logical Error Rate vs Gate Error Rate

!\[Logical Error Rate vs Gate Error Rate](https://github.com/qvazarius648/quantum-bitflip-repetition-code/raw/main/results/LERvsGER.png)

\## How to Run



1\. Install dependencies:

```bash

pip install -r requirements.txt

```



2\. Launch Jupyter Notebook:

```bash

jupyter notebook repetition\_from\_scratch.ipynb

```



3\. Run all cells to reproduce the experiments and plots.

