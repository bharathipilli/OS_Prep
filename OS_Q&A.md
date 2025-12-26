# Operating Systems – Complete Recap (Interview & Linux System Programming)

---

## 1. What is an Operating System?

**Q1. What is an Operating System?**  
An Operating System (OS) is system software that:
- Acts as an interface between user applications and hardware
- Manages CPU, memory, storage, I/O devices, and processes
- Provides services so programs execute safely and efficiently

---

## 2. Why Do We Need an Operating System?

**Q2. Why is an OS required?**

Without an OS:
- Programs directly access hardware → conflicts
- No multitasking
- No memory protection
- No file organization
- No security

OS solves this by:
- Schedules CPU time among processes
- Isolates running programs
- Manages memory allocation and protection
- Provides file systems for data storage
- Handles I/O devices
- Enforces security and access control

**In simple terms:**  
> OS = Resource Manager + Control Program   

### Conclusion

The Operating System acts as a **resource manager** and **control program**, ensuring stability, security, and efficient utilization of system resources.
---

## 3. Importance of Operating System

| Area | Importance |
|---|---|
| CPU | Efficient multitasking |
| Memory | Prevents crashes and overwrites |
| Storage | Organized file systems |
| Security | Access control and permissions |
| Performance | Optimal resource usage |
| Stability | Fault isolation |

---

## 4. Types of Operating Systems

### Batch Operating System

**Q1. What is a Batch OS?**
- Jobs executed in batches
- No user interaction

**Example:** Early mainframe systems

---

### Time-Sharing Operating System

**Q1. What is a Time-Sharing OS?**
- CPU shared among multiple users
- Fast response time

**Example:** UNIX, Linux

---

### Real-Time Operating System (RTOS)

**Q1. What is RTOS?**
- Strict timing constraints
- Deterministic response

**Example:** VxWorks, FreeRTOS

---

### Distributed Operating System

**Q1. What is a Distributed OS?**
- Multiple machines behave as a single system

---

### Network Operating System

**Q1. What is a Network OS?**
- Provides networking services

**Example:** Windows Server

---

## 5. Process Management – Interview Questions and Answers

### Process Basics

**Q1. What is a Process?**  
A process is a program in execution.

**Q2. Program vs Process?**
- Program: Passive (stored on disk)
- Process: Active (running in memory)

---

### Process States

**Q3. Process states?**
- New
- Ready
- Running
- Waiting
- Terminated

---

### Process Control Block (PCB)

**Q4. What is PCB?**
Stores:
- Process ID
- State
- Program counter
- Registers
- Memory info

---

### Context Switching

**Q5. What is Context Switching?**  
Saving one process state and loading another.

**Linux APIs:** `fork()`, `exec()`, `wait()`, `exit()`

---

## 6. Threads – Interview Questions and Answers

### Thread Basics

**Q1. What is a Thread?**  
Smallest unit of execution inside a process.

**Q2. Thread vs Process?**
- Threads share memory
- Processes have separate memory

---

### Types of Threads

**Q3. User-level vs Kernel-level threads?**
- User-level: Managed by libraries
- Kernel-level: Managed by OS

**Linux API:** `pthread_create()`

---

## 7. CPU Scheduling – Interview Questions and Answers

### Scheduling Algorithms

**Q1. What is CPU Scheduling?**  
Selecting a process for CPU execution.

**Algorithms:**
- FCFS
- SJF
- Priority
- Round Robin
- Multilevel Queue

---

### Scheduling Metrics

**Q2. Scheduling metrics?**
- Turnaround Time
- Waiting Time
- Response Time

---

## 8. Memory Management – Interview Questions and Answers

### Memory Basics

**Q1. Logical vs Physical Memory?**
- Logical: CPU-generated
- Physical: Actual RAM

---

### Virtual Memory

**Q2. What is Virtual Memory?**  
Using disk to extend RAM.

---

### Paging and Segmentation

**Q3. What is Paging?**  
Fixed-size memory blocks.

**Q4. What is Segmentation?**  
Logical memory division.

---

### Page Replacement

**Q5. Page replacement algorithms?**
- FIFO
- LRU

---

### Linux Memory APIs

**Q6. Stack vs Heap?**
- Stack: Function calls
- Heap: Dynamic allocation

---

## 9. Deadlocks – Interview Questions and Answers

### Deadlock Basics

**Q1. What is Deadlock?**  
Processes waiting indefinitely for resources.

---

### Necessary Conditions

**Q2. Deadlock conditions?**
1. Mutual exclusion
2. Hold and wait
3. No preemption
4. Circular wait

---

### Handling Deadlocks

**Q3. Deadlock handling methods?**
- Prevention
- Avoidance (Banker’s Algorithm)
- Detection and recovery

---

## 10. Synchronization – Interview Questions and Answers

### Synchronization Basics

**Q1. What is a Critical Section?**  
Code accessing shared data.

**Q2. What is a Race Condition?**  
Output depends on execution order.

---

### Synchronization Tools

**Q3. What is a Mutex?**  
Binary lock for mutual exclusion.

**Q4. What is a Semaphore?**  
Counter-based synchronization.

**Q5. Spinlock vs Mutex?**
- Spinlock: Busy waiting
- Mutex: Blocking

---

## 11. File System – Interview Questions and Answers

### File Basics

**Q1. What is a File?**  
Collection of related data on disk.

---

### Inode

**Q2. What is an Inode?**  
Stores file metadata.

---

### Linux File APIs

**Q3. File system calls?**
- `open()`
- `read()`
- `write()`
- `lseek()`

**Q4. What is a File Descriptor?**  
Integer representing an open file.

---

## 12. I/O Management – Interview Questions and Answers

### I/O Basics

**Q1. Blocking vs Non-blocking I/O?**
- Blocking: Waits
- Non-blocking: Returns immediately

---

### Linux Concept

**Q2. What does “Everything is a file” mean?**  
Devices and IPC are treated as files.

---

## 13. Inter-Process Communication (IPC)

**Q1. What is IPC?**  
Communication between processes.

**Types:**
- Pipes
- FIFOs
- Message Queues
- Shared Memory
- Signals
- Sockets

---

## 14. System Calls – Interview Questions and Answers

### Basics

**Q1. What is a System Call?**  
Interface to request kernel services.

---

### Execution Modes

**Q2. User mode vs Kernel mode?**
- User: Restricted
- Kernel: Full access

---

### Examples

**Q3. System call examples?**
- `read()`
- `write()`
- `fork()`

---

## 15. Virtualization and Containers

**Q1. What is Virtualization?**  
Running multiple OS on same hardware.

**Q2. What are Containers?**  
Process-level isolation using namespaces and cgroups.

---

## 16. OS Architecture Types

| Type | Description |
|---|---|
| Monolithic | All services in kernel (Linux) |
| Microkernel | Minimal kernel (QNX) |
| Hybrid | Combination (Windows, macOS) |

---

## 17. OS Concepts vs Linux APIs

| OS Concept | Linux API |
|---|---|
| Process | fork(), exec(), wait() |
| Thread | pthread |
| Memory | malloc(), mmap() |
| File System | open(), read(), write() |
| IPC | pipe(), shm, socket |
| Synchronization | mutex, semaphore |

---
