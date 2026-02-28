\# Quantum Bit-Flip Repetition Code



\## Overview

This project demonstrates a \*\*manual implementation of a quantum bit-flip repetition code\*\* using \*\*Stim\*\*, a high-performance simulator for stabilizer circuits.  

The main goal is to showcase the ability to construct quantum error-correcting circuits from scratch, simulate realistic noise, and analyze logical error rates.



The project emphasizes:

\- Understanding of the \*\*physical and logical structure\*\* of repetition codes.

\- Ability to simulate quantum circuits with \*\*noise models\*\*.

\- Analysis of logical error rate scaling with \*\*code distance, number of rounds, and error probabilities\*\*.



---



\## Circuit Construction

\- \*\*Data and Ancilla Qubits:\*\* Data qubits store the logical information, while ancilla qubits are used for stabilizer (syndrome) measurements.  

\- \*\*Syndrome Measurement Rounds:\*\* Repeated rounds of nearest-neighbor parity measurements are performed to extract syndrome data.  

\- \*\*Full Syndrome Extraction:\*\* All ancilla qubits are measured after each round, without active error correction, to collect statistics.



---



\## Noise Model

The simulation includes realistic stochastic noise channels:



\- \*\*Gate noise:\*\* Single- and two-qubit depolarizing noise applied after each gate operation.  

\- \*\*Idle noise:\*\* Depolarizing noise applied to qubits that are idle during a given time layer.  

\- \*\*Measurement noise:\*\* Classical bit-flip (X) noise applied immediately after measurement.



This setup allows studying the effect of each noise source on the logical error rate.



---



\## Monte Carlo Simulation

\- \*\*Logical Error Rate Estimation:\*\* Uses a majority vote on data qubits at the end of the experiment to determine whether a logical error occurred.  

\- \*\*Syndrome Statistics:\*\* Computes the fraction of rounds with nonzero syndromes, average syndrome weight, and per-round syndrome rates.  

\- \*\*Parameter Sweeps:\*\* Can simulate different distances, number of rounds, and error probabilities to analyze scaling behavior.



---





\## Results



\### Example Noisy Circuit

The figure below shows an example of the \*\*noisy repetition code circuit\*\* that is analyzed in the experiments.  

This helps illustrate which circuit we are studying when analyzing the logical error rate for different noise types.



\[View noisy circuit](https://github.com/qvazarius648/quantum-bitflip-repetition-code/raw/main/results/noisy\_circuit.svg)



\*(If you prefer to display an image directly, you can convert the PDF to PNG and use an `<img>` tag.)\*



\### Logical Error Rate vs Gate Error Rate

The following plot shows the \*\*logical error rate\*\* as a function of \*\*gate error probability\*\* for different numbers of syndrome measurement rounds.



<img src="https://github.com/qvazarius648/quantum-bitflip-repetition-code/raw/main/results/LERvsGER.png" alt="Logical Error Rate vs Gate Error Rate" width="600">

## How to Run



1\. Install dependencies:

```bash

pip install -r requirements.txt

```



2\. Launch Jupyter Notebook:

```bash

jupyter notebook repetition\_from\_scratch.ipynb

```



3\. Run all cells to reproduce the experiments and plots.

## Project Highlights

\- \*\*Manual circuit construction:\*\* Demonstrates understanding of repetition codes from the ground up.

\- \*\*Stim-based simulation:\*\* Efficient simulation of stabilizer circuits with Monte Carlo sampling.

\- \*\*Noise modeling and analysis:\*\* Allows studying the impact of gate, idle, and measurement errors on logical qubits.

\- \*\*Reproducibility:\*\* Notebook and requirements allow anyone to reproduce results easily.

