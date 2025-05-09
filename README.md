# Quantum Computing Demonstrations

This repository contains implementations of fundamental quantum computing protocols using Qiskit, IBM's open-source quantum computing framework.

## Table of Contents
- [Overview](#overview)
- [Dependencies](#dependencies)
- [Bell States](#bell-states)
- [Superdense Coding](#superdense-coding)
- [Quantum Teleportation](#quantum-teleportation)
- [Results](#results)
- [Usage](#usage)

## Overview

This project demonstrates three fundamental quantum computing concepts:

1. **Bell States**: Creation and visualization of the four maximally entangled two-qubit states.
2. **Superdense Coding**: A protocol that allows sending two classical bits by manipulating a single qubit.
3. **Quantum Teleportation**: A technique to transfer the exact state of a qubit from one location to another using entanglement.

## Dependencies

To run the code in this repository, you'll need:

```
qiskit
qiskit-aer
matplotlib
numpy
IPython
```

Install all dependencies with:

```bash
pip install qiskit qiskit-aer matplotlib numpy IPython
```

## Bell States

Bell states are maximally entangled quantum states of two qubits. The four Bell states implemented are:

- **Ψ+ (|00⟩+|11⟩)**: The standard Bell state created with Hadamard + CNOT
- **Ψ- (|00⟩-|11⟩)**: Created by applying X gate to the second qubit
- **Φ+ (|01⟩+|10⟩)**: Created by applying X gate to the first qubit
- **Φ- (|01⟩-|10⟩)**: Created by applying X gates to both qubits

The code demonstrates how to prepare each Bell state and visualize their statevectors.

## Superdense Coding

Superdense coding is a quantum communication protocol that allows the transmission of two classical bits of information by sending only one qubit, provided that the sender and receiver share an entangled pair.

The implementation:
1. Creates an entangled Bell pair shared between sender (Alice) and receiver (Bob)
2. Alice encodes two classical bits (00, 01, 10, or 11) by applying quantum operations (I, X, Z, or XZ) to her qubit
3. Alice sends her qubit to Bob
4. Bob performs a Bell measurement on both qubits to decode the two classical bits

The protocol is tested with all possible combinations of Bell states and two-bit messages.

## Quantum Teleportation

Quantum teleportation transfers the quantum state of one qubit to another distant qubit using entanglement and classical communication.

The implementation:
1. Initializes a random quantum state to be teleported
2. Creates an entangled Bell pair shared between sender (Alice) and receiver (Bob)
3. Alice performs a Bell-state measurement on her qubit and the qubit to be teleported
4. Alice sends the classical measurement results to Bob
5. Based on these results, Bob performs conditional operations on his qubit
6. Bob's qubit now contains the original quantum state

The code verifies the teleportation by computing the fidelity between the original and teleported states.

## Results

### Bell States
The code generates and visualizes all four Bell states, showing their statevector representations.

### Superdense Coding
The results demonstrate successful transmission of all possible two-bit messages (00, 01, 10, 11) using the superdense coding protocol. The code includes visualizations of measurement outcomes for all combinations of Bell states and message pairs.

### Quantum Teleportation
The quantum teleportation protocol successfully transfers random quantum states with perfect fidelity (1.0), confirming that the state is teleported correctly.

## Usage

Each section of the code can be run independently:

```python
# For Bell States demonstration
# Run the bell_states.py code

# For Superdense Coding
# Run the superdense_coding.py code

# For Quantum Teleportation
# Run the quantum_teleportation.py code
```

Note: The actual files might need to be created from the code snippets in the original file.

## Acknowledgments

This project uses IBM's Qiskit framework for quantum computing simulations.
