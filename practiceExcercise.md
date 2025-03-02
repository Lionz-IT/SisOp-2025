# Operating System Assignment

**Name**: Rafif Ahmad Yudhistira  
**Class**: 1 D3 IT B  
**NRP**: 3124500045  

## Questions and Answers

### 1.1 What are the three main purposes of an operating system?
1. **Resource management** – Managing computer hardware resources such as the CPU, memory, and I/O devices.  
2. **Program execution environment** – Providing an interface for executing applications.  
3. **User interaction facilitation** – Acting as an intermediary between users and hardware.  

### 1.2 When is it appropriate for the operating system to forgo efficient hardware usage and "waste" resources? Why is such a system not really wasteful?
It is appropriate when prioritizing user experience or system flexibility, such as in GUI-based systems or time-sharing environments. These systems are not truly wasteful since they improve usability and productivity.  

### 1.3 What is the main difficulty in writing an OS for a real-time environment?
The main challenge is ensuring that the system meets strict timing constraints (deadlines). Any delay in processing could lead to system failure.  

### 1.4 Should an operating system include applications like web browsers and mail programs?
#### **Arguments for inclusion:**
- Provides a better user experience with built-in applications.  
- Ensures security and compatibility.  

#### **Arguments against inclusion:**
- Can lead to software bloat and unnecessary dependencies.  
- Forces users to rely on specific applications instead of choosing their own.  

### 1.5 How does the distinction between kernel mode and user mode enhance security?
Kernel mode allows full access to hardware, while user mode restricts access. This prevents unauthorized applications from modifying critical system components, enhancing security.  

### 1.6 Which of the following instructions should be privileged?
- **(a) Set value of timer** -> Privileged  
- **(b) Read the clock** -> Non-privileged  
- **(c) Clear memory** -> Privileged  
- **(d) Issue a trap instruction** -> Non-privileged  
- **(e) Turn off interrupts** -> Privileged  
- **(f) Modify entries in device-status table** -> Privileged  
- **(g) Switch from user to kernel mode** -> Privileged  
- **(h) Access I/O device** -> Privileged  

### 1.7 Difficulties with early OS protection via memory partitioning
1. **Lack of flexibility** – The OS cannot be updated or patched without physical intervention.  
2. **Debugging issues** – If a bug exists, fixing it requires direct hardware modifications.  

### 1.8 What are two possible uses of multiple CPU modes?
1. **Access control** – Allows different levels of access for the OS, hypervisors, and user applications.  
2. **Enhanced security** – Additional modes can limit kernel access to reduce security vulnerabilities.  

### 1.9 How can timers be used to compute the current time?
The OS can configure a timer to interrupt the CPU at regular intervals. By counting the number of interrupts since a known starting time, the system can determine the current time.  

### 1.10 Why are caches useful? What problems do they solve? What problems do they cause?
#### **Advantages of caches:**  
1. Improve data access speed by storing frequently used data closer to the processor.  
2. Reduce the load on main memory and storage devices.  

#### **Problems caused by caches:**  
1. **Data inconsistency** – Cached data can become outdated if not properly synchronized with main storage.  
2. **Limited size** – Large caches require more power and expensive memory.  

#### **Why not replace storage with a cache-sized equivalent?**  
Caches use faster but more expensive technology. Expanding a cache to the size of a storage device would be cost-prohibitive and inefficient in terms of power consumption.  

### 1.11 Difference between client-server and peer-to-peer models
- **Client-server model**: A clear distinction exists between clients (service requesters) and servers (service providers).  
  - **Example**: Web browsing.  
- **Peer-to-peer model**: All nodes can act as both clients and servers, sharing resources directly.  
  - **Example**: Torrent networks.  

---

This document is formatted for clarity and readability on GitHub. Let me know if you need any modifications! 🚀

