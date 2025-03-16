# Differences Between Multiprogramming and Multitasking

## Multiprogramming (Batch System)
Multiprogramming is a technique used to improve CPU efficiency by ensuring that the CPU always has a job to execute.

### Key Features:
- A **single user** cannot keep the CPU and I/O devices busy at all times.
- **Multiprogramming organizes jobs** (code and data) so that the CPU always has something to execute.
- Only a **subset of total jobs** is kept in memory.
- Jobs are selected and run using **job scheduling**.
- If a job needs to wait (e.g., for I/O operations), the **OS switches to another job**.

## Timesharing (Multitasking)
Timesharing is an extension of multiprogramming in which the CPU switches jobs frequently, allowing users to interact with running processes.

### Key Features:
- The CPU switches between jobs frequently, enabling **interactive computing**.
- **Response time** should be less than **1 second**.
- Each user has at least one program executing in memory, known as a **process**.
- When multiple jobs are ready to execute, **CPU scheduling** determines which one runs.
- If processes do not fit into memory, **swapping** moves them in and out.
- **Virtual memory** allows execution of processes that do not completely fit in memory.

## Comparison Table
| Feature             | Multiprogramming           | Multitasking |
|--------------------|---------------------------|-------------|
| CPU Utilization   | Maximized by organizing jobs | Maximized by frequent switching |
| User Interaction  | No direct user interaction  | Allows direct user interaction |
| Scheduling        | Job Scheduling (Batch Processing) | CPU Scheduling (Rapid Switching) |
| Response Time    | Not a primary concern      | Should be < 1 second |
| Memory Usage     | Limited by physical memory  | Uses virtual memory and swapping |

---
*Both multiprogramming and multitasking enhance CPU efficiency, but multitasking focuses on user interaction and real-time execution.* 
