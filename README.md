# Banker's Algorithm Simulator

This project is an implementation of the **Banker's Algorithm** in C. The Banker's Algorithm is a resource allocation and deadlock avoidance algorithm that tests the safety of a system state by simulating resource allocation for multiple processes.

---

## Overview

The program simulates a system with multiple processes and resources. It determines whether the system is in a **safe state** or an **unsafe state** by allocating resources dynamically and checking for potential deadlocks. 

Key functionalities include:
1. **Input**:
   - Number of processes and resources.
   - Maximum instances of each resource.
   - Allocated resources for each process.
   - Maximum required resources for each process.
2. **Output**:
   - Displays the system's resource allocation.
   - Shows whether the system is in a safe or unsafe state.
   - Provides the sequence of process execution if the system is in a safe state.

---

## Features

- **Resource Allocation**:
  - Calculates total allocated resources for all processes.
  - Determines available resources at any given time.
  
- **Safety Check**:
  - Evaluates the system state after every resource allocation.
  - Ensures that sufficient resources remain for other processes to complete safely.

- **Dynamic Execution**:
  - Simulates the execution of processes, releasing allocated resources upon completion.
  - Updates the availability of resources dynamically.

---

## Prerequisites

To compile and run the program, you need:
- A C compiler (e.g., GCC).
- Basic knowledge of C programming and operating systems.

---

## How It Works

1. **Initialization**:
   - The program initializes data structures for:
     - Current resource allocation.
     - Maximum resource requirements.
     - Available resources.
   - Inputs the number of processes and resources.

2. **Safety Algorithm**:
   - For each process:
     - Checks if the process's needs can be met with available resources.
     - Executes the process if possible, releasing its allocated resources back to the system.
   - Continues until all processes are executed or determines the system is in an unsafe state.

3. **Output**:
   - Prints the state of resources after each step.
   - Indicates whether the system is in a safe or unsafe state.

---

## File Structure

- **`OS_Project.c`**: The main implementation of the Banker's Algorithm.

---

## **Follow Prompts**:
   - Enter the number of processes and resources.
   - Provide the maximum instances of each resource.
   - Input the allocated resource table and maximum resource requirement table.

---

## Limitations

- The program assumes valid input from the user.
- Works with up to 5 processes and 5 resources by default. Modify the array sizes for larger systems.
- Does not account for processes with dynamic resource requirements during runtime.

---

## Applications

The Banker's Algorithm is widely used in:
- Operating systems for resource allocation and deadlock avoidance.
- Multi-threaded applications where resources are limited.
- Real-time systems requiring deterministic execution.

---

## Disclaimer

This implementation is for educational purposes and is not optimized for production systems.
