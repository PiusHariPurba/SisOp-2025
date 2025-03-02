<div align="center">

# SISTEM OPERASI

## **PENGENALAN SISTEM OPERASI**

![Pens Logo](https://belajargiat.id/wp-content/uploads/2020/10/logo-PENS.png)

**Dosen Pengampu:**

Dr. Ferry Astika Saputra, S.T., M.Sc.

**Disusun Oleh:**

Pius Purba (3124521015)

## **PROGRAM STUDI D3 TEKNIK INFORMATIKA PSDKU LAMONGAN**  
DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER  
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA  
2025

</div>

---

### 1. What are the three main purposes of an operating system?

The purposes of an operating system can be divided into:
1. As a connector between software and hardware on the device.
2. As a provider of security features as well as a protector for the PC from all things dangerous and risky.
3. As an executor in running the device.
4. As a memory size regulator that can currently store, modify, copy, and delete files/data.

---

### 2. We have stressed the need for an operating system to make efficient use of the computing hardware. When is it appropriate for the operating system to forsake this principle and to "waste" resources? Why is such a system not really wasteful?

Because there are things that are more important/must be prioritized, such as user I/O. Data security and periodic checks for virus attacks, the needs during video/image/animation/effects creation, or even just to enhance user experience satisfaction, which must be done to achieve user convenience, security, and efficiency according to the conditions prevailing at that time.

---

### 3. What is the main difficulty that a programmer must overcome in writing an operating system for a real-time environment?

There are many, and I'll take the case in the control tower at the airport where programmers are required to create a system that can act quickly, responsively, without delay, even when given a heavy and non-stop workload

---

### 4. Keeping in mind the various definitions of operating system, consider whether the operating system should include applications such as web browsers and mail programs. Argue both that it should and that it should not, and support your answers!

On one hand (the pro side), if an operating system is made into application form or even a Gmail integration, it would have:
•	More guaranteed cybersecurity
•	Focused functions and objectives, making it easier for users/admins
•	Thus, it can enhance user experience
However, there are some weaknesses, such as:
•	Higher memory and system resource usage
•	Each publication from different companies will result in different features and look-and-feel, which can confuse users.

---


### 5. How does the distinction between kernel mode and user mode function as a rudimentary form of protection (security)?
Kernel mode and user mode actually have significant differences, such as in the area of system execution, ownership of access to software and hardware, and also security protection. Kernel mode, because its ownership of access covers most computer components, when there is a crash or system damage, it will affect all computer components, while user mode, because its access is limited, the damage caused does not affect all parts.

## 6. Which of the following instructions should be privileged?
- A. Set value of timer  
- B. Read the clock  
- C. Clear memory  
- D. Issue a trap instruction  
- E. Turn off interrupts  
- F. Modify entries in device-status table  
- G. Switch From user to kernel  
- H. Access I/O device  

### Privileged Instructions:
- A. Set value of timer  
- C. Clear memory  
- E. Turn off interrupts  
- F. Modify entries in device-status table  
- G. Switch From user to kernel  
- H. Access to I/O device

## 7. Some early computers protected the operating system by placing it in a memory partition that could not be modified by either the user job or the operating system itself. Describe two difficulties that you think could arise with such a scheme.
The problem is if the operating system cannot be modified, updated, or given additional patches because any changes required to the operating system will require a complete system reboot or a more complicated process to replace the entire operating system image. Additionally, this restraint also makes resource allocation inefficient due to its less effective use.

## 8. Some CPUs provide for more than two modes of operation. What are two possible uses of these multiple modes?
Firstly, it enables improved isolation and data security, as well as protection against malicious software. Additionally, PC performance can be optimized, such as through advanced caching or parallel processing, which have the potential to achieve energy efficiency and deliver better performance.

### 9. Timers could be used to compute the current time. Provide a short description of how this could be accomplished.
1.	Timer Initialization 
2.	Time Calculation can be done by using system functions to get the current time (e.g., gettimeofday() on Linux) and then save it as the start time. 
3.	Time Update. In the main program loop, periodically check the current time and then calculate the difference from the start time to get the elapsed time and then adjust it to real-time (usually constrained in seconds). 
4.	Format and Display

## 10. Give two reasons why caches are useful. What problems do they solve? What problems do they cause? If a cache can be made as large as the
- Practical considerations related to cost, volatility, capacity, performance, data management, and system architecture make it impractical to completely eliminate traditional storage devices/DISKs.

## 11. Distinguish between the client-server and peer-to-peer models of distributed systems

1. **Architecture**
   - In client-server mode, there is a clear separation between clients and servers. Clients send requests, while servers provide services or resources. The server functions as a central management point. In contrast, in the peer-to-peer model, all nodes (peers) have equal roles. Each peer can function as both a client and a server, sharing resources and services directly without a central authority.

2. **Scalability**
   - Scalability can be a challenge because the server can become a bottleneck as the number of clients increases in client-server mode. Adding clients requires increasing server capacity. P2P is more easily scalable because the load is distributed among all peers. Adding new peers increases the overall system capacity and performance.

3. **Resource Management**
   - In the Client-Server model, resource management is centralized. The server is responsible for managing data, resources, and access control, which can simplify administration but also create a single point of failure.
   - In P2P, resource management is decentralized. Each peer manages its own resources and shares them with other peers, which can increase redundancy but also complicate resource discovery and management.

4. **Fault Tolerance**
   - In the Client-Server model, if the server fails, clients cannot access services, resulting in a single point of failure. Redundancy can be implemented, but it requires additional infrastructure.
   - P2P is generally more fault-tolerant. If one peer is offline, other peers can still communicate and share resources, making the system more resistant to failures.

## 12. How do clustered systems differ from multiprocessor systems? What is required for two machines belonging to a cluster to cooperate to provide a highly available service?

- The distinction between a Cluster system and a multiprocessor system can be seen from the architectural aspect. A cluster system consists of several independent computers (nodes) connected via a network. Each node has its own operating system and resources such as CPU, memory, storage and operates as a separate entity. Nodes work together to perform tasks, which often appear to users as a single system. In contrast, a multiprocessor system consists of several processors (CPUs) within a single computer or server. These processors share the same memory and are tightly integrated, allowing for efficient communication and resource sharing. The operating system typically manages these processors as a single unit.

- In terms of scalability/capability, a cluster system is usually easier to scale because new nodes can be added to the cluster without significant changes to the existing infrastructure. A multiprocessor system can also be scaled by adding more processors, but it is often limited by physical hardware constraints and system architecture, which can lead to performance degradation as more processors are added, causing resource contention.

To achieve scaling, the following requirements must be met:
1. **Cluster Management Software**: Manages resources, monitors node health, and handles failover.
2. **Communication Mechanism**: Reliable communication protocols (such as TCP/IP) and heartbeat mechanisms to check node status.
3. **Shared Storage**: Shared storage systems or distributed file systems to ensure data consistency between nodes.
4. **Failover Mechanism**: Automated systems that transfer control from failed nodes to backup nodes, as well as application state management.
5. **Load Balancing**: Distribution of incoming traffic between nodes and health checks to ensure only healthy nodes receive requests.
6. **Configuration Management**: Ensuring consistent configurations across all nodes and managing configuration changes.
7. **Security Measures**: Secure communication channels, authentication, and data protection.
8. **Testing and Validation**: Regular testing to ensure failover processes and cluster performance meet established SLAs.

## 13. Consider a computing cluster consisting of two nodes running a database. Describe two ways in which the cluster software can manage access to the data on the disk. Discuss the benefits and disadvantages of each.

### 1. Master-Slave Replication
In a master-slave replication model, one node acts as the master (or primary) node, while the other nodes act as slave (or secondary) nodes. This setup helps manage data access effectively.
- **Write Operations**: All write operations are directed to the master node. The master node processes the write requests and updates the database. After a successful write, the master node replicates the changes to the slave nodes. This ensures that the slaves have an up-to-date copy of the data.
- **Read Operations**: Read operations can be distributed between the master and slaves. The master can handle read requests, but slaves can also serve read requests to reduce the load on the master and improve performance. However, there might be a slight delay in data consistency for reads from the slaves, as they may not have the latest updates until replication is complete.
- **Failover**: If the master node fails, the cluster can promote a slave node to become the new master, ensuring continued database availability. This requires mechanisms to detect failures and reconfigure the cluster.

**Advantages:**
- High Availability: If the master node fails, the system can promote a slave node to become the new master, ensuring continuous database availability.
- Read Load Balancing: Read operations can be distributed between the master and slaves, which can improve performance and reduce the load on the master node.
- Simplicity: The master-slave model is relatively easy to implement and understand, making it easier to manage and maintain.
- Data Redundancy: Slave nodes serve as backups for the master, providing data redundancy and protection against data loss.

**Disadvantages:**
- Write Bottleneck: All write operations must go through the master node, which can become a bottleneck, especially in write-heavy applications.
- Replication Lag: There may be a delay (replication lag) between when data is written to the master and when it is replicated to the slaves, causing potential inconsistencies in read operations from the slaves.
- Single Point of Failure for Writes: If the master node fails, write operations cannot be processed until a new master node is promoted, which can result in downtime.
- Complexity in Failover: Although failover can be automated, it adds complexity to the system, requiring mechanisms to detect failures and promote slaves.

### 2. Distributed Locking with Coordination Services
Distributed locking mechanisms can be implemented to manage concurrent access to data on disks. This approach ensures that only one node can modify a particular piece of data at a time.
- **Lock Management**: Coordination services (such as Apache ZooKeeper, etcd, or custom lock managers) can be used to manage locks. When a node wants to read or write data, it first requests a lock from the coordination service.
- **Lock Types**: Locking mechanisms can support various lock types:
  - Exclusive Locks: Prevent other nodes from accessing the data while the lock is held, ensuring that only one node can write to the data.
  - Shared Locks: Allow multiple nodes to read the data concurrently but prevent any node from writing to the data.
- **Lock Acquisition and Release**: Nodes attempt to acquire locks before performing read or write operations. After the operation is complete, the node releases the lock. If a node fails while holding a lock, the coordination service should have a mechanism to detect this and release the lock to prevent deadlocks.

**Advantages:**
- Data Consistency: Distributed locking ensures that only one node can modify a particular piece of data at a time, preventing race conditions and ensuring data integrity.
- Concurrency Control: This method allows for finer-grained control over data access, enabling multiple nodes to read data concurrently while preventing concurrent writes.
- Flexibility: Locking mechanisms can be tailored to specific use cases, allowing for various lock types (exclusive, shared) based on application needs.
- Fault Tolerance: Many coordination services (such as ZooKeeper) are designed to be fault-tolerant, providing reliability in managing locks.

**Disadvantages:**
- Performance Overhead: Locking mechanisms introduce latency, as nodes must wait to acquire locks before accessing data. This can lead to performance bottlenecks, especially in high-concurrency scenarios.
- Complexity: Implementing distributed locking mechanisms can be complex, requiring careful design to avoid deadlocks and ensure proper lock management.
- Single Point of Failure: If the coordination service fails, it can disrupt the entire locking mechanism, leading to potential data access issues.
- Scalability Issues: As the number of nodes increases, managing locks can become more challenging, potentially leading to contention and performance degradation.

## 14. What is the purpose of interrupts? How does an interrupt differ from a trap? Can traps be generated intentionally by a user program? If so, for what purpose?

**Interrupts** function to enable synchronous event handling, improve CPU utilization, facilitate real-time processing, manage multitasking, enable device communication, handle errors, and improve system responsiveness.

**Traps** are generated from the CPU itself in response to certain conditions during program execution. This can be caused by errors (such as division by zero, invalid memory access) or certain instructions such as system calls intended for error handling, debugging, and system calls.

Yes, traps can be generated intentionally by a user program for purposes such as system calls, error handling, and debugging.

## 15. Explain how the Linux kernel variables HZ and jiffies can be used to determine the number of seconds the system has been running since it was booted.

**Formula:**


\[ \text{Seconds} = \frac{\text{jiffies}}{\text{HZ}} \]



**Note:**
- **jiffies**: Total number of timer interrupts since the system was booted.
- **HZ**: Timer interrupt frequency per second.

## 16. Direct memory access is used for high-speed I/O devices in order to avoid increasing the CPU's execution load.

### a. How does the CPU interface with the device to coordinate the transfer?
- **DMA Controller**: 
  - The primary interface is the DMA controller. The CPU programs the DMA controller with information such as the source/destination memory addresses, the amount of data to transfer, and the direction of the transfer (from device to memory or vice versa).
  - The CPU issues an initial command to the DMA controller, which then takes control of the memory bus.
- **Control Signals**: 
  - The CPU and DMA controller use control signals on the system bus to coordinate the transfer. This includes signals for requesting and granting bus control, and signals to notify the CPU when the transfer is complete.

### b. How does the CPU know when the memory operations are complete?
- **Interrupts**: 
  - Upon completion of the DMA transfer, the DMA controller sends an interrupt signal to the CPU.
  - The CPU receives this interrupt and executes the appropriate interrupt handler routine to notify the operating system that the transfer is complete.
- **Status Flags**: 
  - In some cases, the DMA controller might set status flags that the CPU can check.
  - The CPU periodically checks these flags to determine if the transfer is complete.

### c. The CPU is allowed to execute other programs while the DMA controller is transferring data. Does this process interfere with the execution of the user programs? If so, describe what forms of interference are caused.
- Yes, there is interference.
  - Although the CPU can execute other programs during a DMA transfer, the DMA transfer utilizes the memory bus.
- **Forms of Interference**: 
  - **Cycle Stealing**: 
    - The DMA controller needs to access the memory bus to transfer data.
    - When the DMA controller uses the bus, the CPU must wait if it wants to access memory.
    - This is called "cycle stealing" because the DMA controller effectively "steals" bus cycles from the CPU.
    - This can slow down user program execution, especially if DMA transfers are frequent or involve large amounts of data.
    - Even so, DMA improves overall system performance, as the CPU does not need to be directly involved in data transfer.

## 17. Some computer systems do not provide a privileged mode of operation in hardware. Is it possible to construct a secure operating system for these computer systems? Give arguments both that it is and that it is not possible.
- **It is possible** if software virtualization & secure language can isolate and software security (sandboxing) limit program capabilities.
- **It is not possible** if there is no privileged mode, hardware isolation is weak so it is vulnerable to attacks, performance drops, and implementation is difficult.

## 18. Many SMP systems have different levels of caches; one level is local to each processing core, and another level is shared among all processing cores. Why are caching systems designed this way?
- To reduce memory latency and also to manage cache coherence to facilitate the implementation of coherence protocols.

## 19. Rank the following storage systems from slowest to fastest:
- a. Hard-disk drives
- b. Registers
- c. Optical disk
- d. Main memory
- e. Nonvolatile memory
- f. Magnetic tapes
- g. Cache

**Ranking (from slowest to fastest)**:
Magnetic tapes (slowest) → Optical disk → Hard-disk drives → Nonvolatile memory → Main memory → Cache → Registers (fastest)

## 21. Discuss, with examples, how the problem of maintaining coherence of cached data manifests itself in the following processing environments

### a. Single-processor systems
- **Manifestation**: 
  - The main issue is between the CPU cache and I/O devices using DMA.
  - Data changes in main memory by DMA can make the CPU cache stale.
- **Example**: 
  - A network card writes packet data to memory via DMA.
  - If the CPU has a copy of the data in its cache, the copy becomes invalid.
- **Solution**: 
  - Cache flushing or memory bus snooping.

### b. Multiprocessor Systems 
- **Manifestation**: 
  - Multiple processors/cores share main memory, each with a local cache.
  - Changes to data in one cache make other caches inconsistent.
- **Example**: 
  - CPU 1 and CPU 2 read the same variable into their caches.
  - CPU 1 changes the variable.
  - CPU 2's cache becomes stale.
- **Solution**: 
  - Cache coherence protocols (e.g., MESI).

### c. Distributed Systems
- **Manifestation**: 
  - Each node has local memory and cache.
  - Problems arise when multiple nodes access and store the same data, especially in DSM or distributed file systems.
- **Example**: 
  - Node A and Node B store the same file from a distributed file system.
  - Node A modifies the file.
  - Node B's cache becomes stale.
- **Solution**: 
  - Distributed cache coherence protocols, distributed file system protocols, and data versioning mechanisms.

## 22. Describe a mechanism for enforcing memory protection in order to prevent a program from modifying the memory associated with other programs.

### 1. Virtual Memory and Memory Management Unit (MMU)
- **Virtual Addresses**: Programs use virtual addresses, which are then translated into physical addresses by the MMU.
- **Page Tables**: The MMU uses page tables to map virtual pages to physical pages. Each process has its own page table.
- **Protection Bits**: Page table entries include protection bits that specify access permissions (read, write, execute) for each page.
- **Address Translation and Protection**: When a program tries to access a memory location, the MMU checks the corresponding page table entry. If the access violates the protection bits (e.g., a program tries to write to a read-only page), the MMU generates a page fault, which triggers an operating system exception.
- **Isolation**: Because each process has its own page table, one process cannot access the physical memory of another process unless explicitly allowed by the operating system.

### 2. Operating System Modes (Kernel Mode vs. User Mode)
- **Kernel Mode**: The operating system runs in kernel mode, which has full access to all system resources, including memory.
- **User Mode**: User programs run in user mode, which has limited access to memory and other resources.
- **Privileged Instructions**: Certain instructions (e.g., instructions that modify page tables) are privileged and can only be executed in kernel mode.
- **System Calls**: User programs must use system calls to request services from the operating system, which then executes the requested operations in kernel mode. This prevents user programs from directly manipulating critical system data.

### 3. Memory Segmentation
- **Segments**: Memory is divided into segments, each with its own base address and limit.
- **Segment Registers**: Segment registers store the base address and limit of each segment.
- **Address Translation and Bounds Checking**: When a program accesses memory, the MMU checks if the address is within the segment's bounds. If it exceeds the bounds, a segmentation fault occurs.
- **Protection Attributes**: Segments can also have protection attributes (e.g., read-only, execute-only).
- Although paging is more common now, segmentation was an important step in memory protection.

### 4. Memory Keys
- **Keys**: Each memory block is associated with a key, and each process has a key.
- **Matching**: When a process accesses memory, the MMU compares the process's key with the memory block's key.
- **Access Control**: Access is granted only if the keys match or if the process has a privileged key.
- This is less common in general-purpose systems but can be found in some specialized systems.

## 23. Which network configuration—LAN or WAN—would best suit the following environments?

### a. A campus student union
- LAN

### b. Several campus locations across a statewide university system
- WAN

### c. A neighborhood
- WAN or LAN+WAN

## 24. Describe some of the challenges of designing operating systems for mobile devices compared with designing operating systems for traditional PCs.

- **Power Consumption**: Battery optimization is crucial, requiring aggressive power management.
- **Resource Limitations**: Limited memory and processing power, demanding high efficiency.
- **Size and Interaction**: Touchscreen interface and small screen size require specialized UI/UX design.
- **Cellular Connectivity**: Complex cellular network management (3G/4G/5G) and connectivity changes.
- **Security and Privacy**: Sensitive personal data and mobile malware risks require robust security.
- **Device Diversity**: Wide variations in hardware require broad adaptation and compatibility.
- **Seamless Updates**: Operating system updates must be performed smoothly and without interrupting user activity.

## 25. What are some advantages of peer-to-peer systems over client-server systems?

### 1. Increased Resilience and Fault Tolerance
- In client-server systems, if the central server fails, the entire network can be disrupted. P2P systems distribute data and processing power among many peers. If one peer fails, others can continue to operate, ensuring greater resilience.

### 2. Improved Scalability
- Client-server systems can become bottlenecks as the number of clients increases, heavily burdening the server. P2P systems scale more effectively because each peer contributes resources, such as bandwidth and storage. As more peers join the network, the overall system capacity increases.

### 3. Cost-Effectiveness
- Client-server systems require expensive dedicated servers and infrastructure.

### 4. Decentralization and Reduced Central Control
- P2P systems eliminate the need for a central authority, which can be beneficial for applications requiring greater autonomy and freedom from censorship. This also eliminates single points of failure and control.

### 5. Efficient Resource Sharing
- P2P systems facilitate efficient resource sharing, such as files and bandwidth, among many users. This can lead to faster downloads and more efficient use of network resources.

## 26. Describe some distributed applications that would be appropriate for a peer-to-peer system.

### 1. File Sharing
- P2P applications are very effective for distributing large files such as movies, music, or software. Each user (peer) can download and upload portions of files, thus reducing the load on central servers. An example is BitTorrent.

### 2. Streaming Media
- P2P can be used to distribute streaming video or audio content. Users can share data streams with each other, improving streaming quality and reducing buffering.

### 3. Distributed Computing
- Applications like Folding@home use P2P to combine computing power from many computers to solve complex problems, such as protein folding simulations.

## 27. Identify several advantages and several disadvantages of open-source operating systems. Identify the types of people who would find each aspect to be an advantage or a disadvantage.

### Advantages of Open Source Operating Systems:
- **Free or Low Cost**: Many open-source operating systems, like Linux, are available for free or at very low cost.
  - **Type of People**: Users with limited budgets, non-profit organizations, and developers who want to experiment without cost.

- **Transparency and Security**: Open source code allows anyone to inspect and fix security vulnerabilities.
  - **Type of People**: Security experts, developers, and users who prioritize privacy and security.

- **Flexibility and Customization**: Users can modify and customize the operating system according to their needs.
  - **Type of People**: Developers, system administrators, and advanced users who want full control of their systems.

- **Strong Community**: A large and active community of developers and users provides support, documentation, and continuous development.
  - **Type of People**: Users seeking support, developers who want to collaborate, and anyone who values the spirit of community.

- **Innovation**: The open development model encourages innovation and collaboration, resulting in rapid updates and new features.
  - **Type of People**: Developers who want to contribute, users who want the latest technology, and organizations that need innovative solutions.

### Disadvantages of Open Source Operating Systems:
- **Lack of Official Support**: Unlike commercial operating systems, open source operating systems may lack official customer support.
  - **Type of People**: Novice users who need direct technical assistance, and organizations that rely on vendor support.

- **Hardware and Software Compatibility**: Some hardware and software may not be fully compatible with open source operating systems.
  - **Type of People**: Users who need compatibility with specific hardware or software, and organizations that use commercial applications.

- **Steep Learning Curve**: Open source operating systems, especially Linux, may have a steeper learning curve than commercial operating systems.
  - **Type of People**: Novice users who are accustomed to simple user interfaces, and anyone who lacks a strong technical background.

- **Fragmentation**: Due to its open nature, there are many Linux distributions (distros), which can confuse novice users.
  - **Type of People**: Novice users who are new to trying Linux.

- **Security**: Although open source code allows anyone to inspect and fix security vulnerabilities, it can also be an opening for irresponsible people to look for security holes.
  - **Type of People**: People with bad intentions, and also people who don't quite understand system security.

