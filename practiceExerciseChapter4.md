## Chapter 4 - Threads & Concurrency

### 4.1
**Question:** Provide three programming examples in which multithreading provides better performance than a single-threaded solution.  
**Answer:**
1. **Web Server:** Handling multiple client requests simultaneously.
2. **Image Processing:** Applying filters or transformations to different image sections in parallel.
3. **Game Development:** Separating game logic, rendering, and input handling into different threads for smoother gameplay.

### 4.2
**Question:** Using Amdahl's Law, calculate the speedup gain of an application that has a 60 percent parallel component for:
(a) two processing cores and (b) four processing cores.  
**Answer:**
Amdahl's Law formula:

```
Speedup = 1 / [(1 - P) + (P / N)]
```
Where:
- **P** = parallel portion (0.6)
- **N** = number of cores

(a) For **2 cores**:
```
Speedup = 1 / [(1 - 0.6) + (0.6 / 2)]
= 1 / [0.4 + 0.3]
= 1 / 0.7
≈ 1.43
```

(b) For **4 cores**:
```
Speedup = 1 / [(1 - 0.6) + (0.6 / 4)]
= 1 / [0.4 + 0.15]
= 1 / 0.55
≈ 1.82
```

### 4.3
**Question:** Does the multithreaded web server described in Section 4.1 exhibit task or data parallelism?  
**Answer:**
It exhibits **task parallelism** since each thread handles a different client request, which is a separate task.

### 4.4
**Question:** What are two differences between user-level threads and kernel-level threads? Under what circumstances is one type better than the other?  
**Answer:**
1. **Management:** User-level threads are managed by user-space libraries, kernel-level threads are managed by the operating system.
2. **Performance:** User-level threads have lower overhead but can't take advantage of multiprocessor systems easily; kernel-level threads can, but with higher management cost.

**When is one better?**
- User-level threads are better for apps needing fast, lightweight thread management.
- Kernel-level threads are better for apps needing true parallelism on multicore systems.

### 4.5
**Question:** Describe the actions taken by a kernel to context-switch between kernel-level threads.  
**Answer:**
1. Save the current thread's CPU context (registers, program counter).
2. Update the thread control block (TCB).
3. Select the next thread to run from the scheduler.
4. Load the new thread's CPU context.
5. Transfer control to the new thread.

---
