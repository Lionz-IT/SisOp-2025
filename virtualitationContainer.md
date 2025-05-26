# Virtualization and Containers

## Nama
- **Rafif Ahmad Yudhistira** (3124500045)

## Dosen Pengajar
**Dr Ferry Astika Saputra ST, M.Sc**

## Virtualization
Virtualization is the technology that allows operating systems (OSes) to run applications within other OSes. It enables better resource utilization and supports running multiple OS instances on a single physical machine.

### Key Concepts:
- Expanding and evolving industry.
- Provides the ability to run applications in isolated environments.
- Uses **Virtual Machine Monitors (VMMs)** to manage virtual machines.

### Types of Virtualization:
#### 1. **Emulation**
- Used when the source CPU type differs from the target CPU type (e.g., PowerPC to Intel x86).
- Generally the slowest method.
- Requires **interpretation** of machine language that is not natively compiled.

#### 2. **Virtualization**
- OS is natively compiled for the CPU.
- Supports running **guest OSes** that are also natively compiled.
- Example: **VMware** running Windows XP guests on a native Windows XP **host**.

### Use Cases of Virtualization:
- Running multiple OSes on laptops/desktops for compatibility testing.
- Developing applications for different OSes without needing multiple physical machines.
- **QA testing** applications across various environments.
- Managing cloud computing environments in **data centers**.

## Containerization
Containerization is an alternative to traditional virtualization that provides lightweight, efficient, and portable application environments.

### Key Features of Containers:
- **Containers share the host OS kernel** instead of requiring a separate OS instance like VMs.
- Faster startup time and lower resource consumption compared to VMs.
- Portable across different environments (development, testing, production).
- Popular containerization tools: **Docker, Kubernetes, LXC (Linux Containers)**.

### Virtual Machines vs. Containers
| Feature              | Virtual Machines (VMs)      | Containers           |
|---------------------|---------------------------|----------------------|
| OS Overhead        | Requires a separate OS per VM | Shares the host OS kernel |
| Startup Time       | Slower due to full OS boot | Fast, lightweight |
| Resource Usage     | Higher (each VM runs a full OS) | Lower (shares system resources) |
| Portability        | Less portable (depends on hypervisor) | Highly portable |
| Isolation          | Stronger (full OS per VM) | Lightweight isolation |

### Use Cases of Containers:
- Microservices architecture development.
- Cloud-native applications and CI/CD pipelines.
- Running applications in a consistent environment across different platforms.
- Large-scale distributed systems with **Kubernetes** orchestration.

---
*Virtualization and containerization both improve resource utilization, but containers offer a more efficient and lightweight approach for modern application deployment.* 

