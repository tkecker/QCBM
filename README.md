# QCBM
 Quantum Circuit Born Machine

# The Quantum Circuit Born Machine (QCMB) as a Market Generator
This code has been created based on the algorithm presented in chapter 9 of the book
#### Quantum Machine Learning and Optimisation in Finance by A. Jacquier and O. Kondratyev (2022, Packt Publishing)

A parametrised quantum circuit (PQC) is trained to generate synthetic data that will have a statistical distribution close to the original dataset, here chosen from finance, here daily log-returns of a stock index (German DAX). The PQC (ansatz) is trained using a genetic algorithm, instead of using a gradient based training algorithm. Starting from random sets of parameters $\theta$ ($12 \times 7$ matrices) for the PQC, these are improved by mutation, allowing one entry of each column to be altered with probability $\alpha$ in each step, where $\alpha$ decreases exponentially from generation to generation. With the trained circuit, new (synthetic) market data can be generated simply by sampling the circuit once for each new data point.