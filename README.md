# Banker's Algorithm Repository

This repository contains two different implementations of the **Banker's Algorithm**, a resource allocation and deadlock avoidance algorithm used in operating systems. These implementations simulate how a system manages resources to ensure safety and prevent deadlocks.

---

## Overview

The Banker's Algorithm is designed to:
1. Allocate resources to processes safely without entering an unsafe state.
2. Dynamically calculate if the system can execute all processes without leading to a deadlock.
3. Provide insights into resource utilization and process execution sequences.

### Key Features
- Simulates a system with multiple processes and resources.
- Checks if the system is in a safe or unsafe state.
- Dynamically updates the availability of resources as processes execute.
- Provides detailed insights into resource allocation, needs, and availability.

---

## Files in the Repository

### 1. **`BankersAlgorithm_ResourceAllocation.c`**
- **Purpose**: 
  - Implements the Banker's Algorithm with detailed prompts for input and an interactive display of the system’s resource allocation state.
- **Functionality**:
  - Accepts the number of processes and resources.
  - Inputs maximum resource claims, current allocations, and available resources.
  - Calculates the remaining needs for each process.
  - Simulates the execution of processes, releasing resources and updating the system state.
  - Determines if the system is in a safe or unsafe state after all processes are either executed or blocked.
- **Key Differentiator**:
  - Provides a tabular output of resource allocation and updates after each step of the algorithm.

### 2. **`BankersAlgorithm_Interactive.c`**
- **Purpose**:
  - A compact implementation of the Banker's Algorithm designed for dynamic and iterative resource allocation simulation.
- **Functionality**:
  - Inputs the number of processes, resources, maximum claims, current allocations, and available resources.
  - Computes the need matrix and determines whether processes can safely execute.
  - Builds a safe sequence of process execution if the system is in a safe state.
  - Stops execution and declares the system unsafe if any process cannot safely execute.
- **Key Differentiator**:
  - Focuses more on process execution order and explicitly constructs the safe sequence if the system is in a safe state.

---

## Concepts Covered

1. **Resource Allocation**:
   - Allocates and tracks resources among processes dynamically.
   - Prevents over-allocation to ensure that the system does not enter an unsafe state.

2. **Safe and Unsafe States**:
   - Defines a **safe state** as one where all processes can complete without deadlocks.
   - Identifies an **unsafe state** when the system cannot guarantee that all processes can complete safely.

3. **Deadlock Avoidance**:
   - Prevents the system from allocating resources in a way that could lead to a deadlock.
   - Ensures that enough resources are always available for the remaining processes.

4. **Dynamic Execution**:
   - Updates available resources and allocations dynamically as processes execute.
   - Reflects real-time resource management in an operating system.

---

## Applications

The Banker's Algorithm is widely used in:
- **Operating Systems**:
  - As a theoretical basis for managing multi-process environments and resource sharing.
- **Resource Management**:
  - Ensures that systems with limited resources allocate them safely and efficiently.
- **Multi-threaded Programming**:
  - Helps prevent deadlocks in concurrent applications.
- **Educational Tools**:
  - Serves as a foundational concept in operating systems courses.

---

## Limitations

- The implementations assume valid input from the user (e.g., positive integers, no mismatched dimensions).
- Designed for static inputs; real-world systems may have dynamically changing resource requirements.
- Supports up to 10 processes and resources by default (modifiable in the code).

---

## Future Enhancements

- Add support for dynamic process addition and resource changes during execution.
- Extend functionality to simulate real-world scheduling scenarios.
- Create a graphical or web-based interface for better visualization of the algorithm.

---

## License

This repository is licensed under the **MIT License**. You are free to use, modify, and distribute the code with proper attribution.
