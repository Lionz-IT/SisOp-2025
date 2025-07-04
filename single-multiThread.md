# Single Thread vs Multi-thread
## Nama
**Rafif Ahmad Yudhistira** (3124500045)

## Dosen Pengajar
**Dr Ferry Astika Saputra ST, M.Sc**

**Single-threaded** processes use a single execution flow where all program components (code, data, files, registers, stack, and PC) are exclusively managed by one thread. This linear execution model processes instructions sequentially, making it simple to implement but inefficient for parallel tasks. It's ideal for basic applications like command-line tools or simple scripts where task switching isn't required.

**Multi-threaded** processes contain multiple threads that share code, data, and files while maintaining separate registers, stacks, and PCs. This architecture enables concurrent task execution, improving performance on multi-core systems and responsiveness for complex applications like web servers or multimedia software. However, it introduces challenges like race conditions and requires careful synchronization when accessing shared resources.

![Image](https://github.com/user-attachments/assets/53f65478-9f44-4c9a-a8b6-fde230b8ee9b)
