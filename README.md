# OS-lastminute-revision

### Operating system
- It is the interface between the user and computer hardware.

### Types of Os

#### Batch Os
- A set of similar jobs are stored in main memory for execution. A job gets assigned to the CPU, only when the execution of the previous job is completed.

#### Multiprogramming Os
- A Multiprogramming operating system is an operating system that supports the running of numerous programs simultaneously on a single processor machine. If one program waits for an input/ output transfer, the other programs are ready to utilize the CPU.
#### Multitasking Os
-Multitasking OS combines the benefits of Multiprogramming OS and CPU scheduling to perform quick switches between jobs. The switch is so quick that the user can interact with each program as it runs.

#### Time Sharing OS 
-Time-sharing systems require interaction with the user to instruct the OS to perform various tasks.

#### Real-Time OS 
– Real-time OS are usually built for dedicated systems to accomplish specific tasks within deadlines.

### Threads: 
A thread is a lightweight process and forms the basic unit of CPU utilization.

->A new thread, or a child process of a given process, can be introduced by using the fork() system call. A process with n fork() system calls generates 2^n – 1 child processes. There are two types of threads:

`User threads`
`Kernel threads`
### Differences between User threads and kernel threads
![image](https://github.com/Niltiwari7/os-lastminute-revision/assets/93751356/8a34448a-d542-4f72-8812-325494ed2c2c)

### Process:
A process is a program under execution. The value of the program counter (PC) indicates the address of the next instruction of the process being executed. Each process is represented by a Process Control Block (PCB).
![image](https://github.com/Niltiwari7/os-lastminute-revision/assets/93751356/e7ab9097-1473-4339-a469-efea79be543b)

#### States of process
![image](https://github.com/Niltiwari7/os-lastminute-revision/assets/93751356/c13950fb-78f8-438a-9dbb-e7f2531f7a6a)

### Different times with respect to the process
`Turn Around Time=Completion time-Arrival Time`

`waiting time=Turn around time-burst time`

### Objective of Process Scheduling Algorithm-

- Maximum CPU  Utilization.
- min response time
- min waiting time
- max throughput
- min turn around time

### Different scheduling algorithm
#### FCFS
- FCFS  stands for first come first serve. The simplest algorithm schedules according to the arrival time of processes.
#### SJF
- SJF stands for shortest job first. The process that has arrived first and which has less burst time than schedules first.

#### SRTF
-It is the preemptive mode of the SJF algorithm in which jobs are scheduled according to the shortest remaining time.
#### Round Robin
- Each process is assigned a fixed time, in a cyclic way.
  
#### Multilevel Queue Scheduling (MLQ):
According to the priority of process, processes are placed in different queues. Generally, high-priority processes are placed in the top-level queue. Only after the completion of processes from the top-level queue, are lower-level queued processes scheduled.

#### Multi-level Feedback Queue (MLFQ) Scheduling:
It allows the process to move in between queues. The idea is to separate processes according to the characteristics of their CPU bursts. If a process uses too much CPU time, it is moved to a lower-priority queue.

### The Critical Section Problem:
#### Critical Section – 
The portion of the code in the program where shared variables are accessed and/or updated.
#### Remainder Section – 
The remaining portion of the program excluding the Critical Section
#### Race around Condition –
The final output of the code depends on the order in which the variables are accessed. This is termed as the race-around condition.

A solution for the critical section problem must satisfy the following three conditions:

#### Mutual Exclusion
– If a process Pi is executing in its critical section, then no other process is allowed to enter into the critical section.
#### Progress 
– If no process is executing in the critical section, then the decision of a process to enter a critical section cannot be made by any other process that is executing in its remainder section. The selection of the process cannot be postponed indefinitely.
#### Bounded Waiting
– There exists a bound on the number of times other processes can enter into the critical section after a process has made a request to access the critical section and before the request is granted.
#### Synchronization Tools:
A Semaphore is an integer variable that is accessed only through two atomic operations, wait () and signal (). An atomic operation is executed in a single CPU time slice without any pre-emption. Semaphores are of two types:
#### Counting Semaphore
– A counting semaphore is an integer variable whose value can range over an unrestricted domain.
#### Mutex 
– A mutex provides mutual exclusion, either producer or consumer can have the key (mutex) and proceed with their work. As long as the buffer is filled by producer, the consumer needs to wait, and vice versa. At any point of time, only one thread can work with the entire buffer. The concept can be generalized using semaphore.


#### Deadlock:
A situation where a set of processes are blocked because each process is holding a resource and waiting for another resource acquired by some other process. Deadlock can arise if following four conditions hold simultaneously (Necessary Conditions):

Mutual Exclusion – One or more than one resource are non-sharable (Only one process can use at a time).
 
Hold and Wait – A process is holding at least one resource and waiting for resources.
 
No Preemption – A resource cannot be taken from a process unless the process releases the resource.
 
Circular Wait – A set of processes are waiting for each other in circular form.

#### Memory Management: These techniques allow the memory to be shared among multiple processes.

Overlays – The memory should contain only those instructions and data that are required at a given time.
Swapping – In multiprogramming, the instructions that have used the time slice are swapped out from the memory.

### Memory Management Techniques:
(a) Single Partition Allocation Schemes – The memory is divided into two parts. One part is kept to be used by the OS and the other is kept to be used by the users. 

(b) Multiple Partition Schemes –

Fixed Partition – The memory is divided into fixed-size partitions.
Variable Partition – The memory is divided into variable-sized partitions.

Variable partition allocation schemes:

First Fit – The arriving process is allotted the first hole of memory in which it fits completely.
Best Fit – The arriving process is allotted the hole of memory in which it fits the best by leaving the minimum memory empty.
Worst Fit – The arriving process is allotted the hole of memory in which it leaves the maximum gap.

#### Note-: 
-Best fit does not necessarily give the best results for memory allocation.
--The cause of external fragmentation is the condition in Fixed partitioning and Variable partitioning saying that the entire process should be allocated in a contiguous memory location. Therefore Paging is used.

#### Paging
– The physical memory is divided into equal-sized frames. The main memory is divided into fixed-size pages. The size of a physical memory frame is equal to the size of a virtual memory frame.
#### Segmentation 
– Segmentation is implemented to give users view of memory. The logical address space is a collection of segments. Segmentation can be implemented with or without the use of paging.

#### Page Fault:
A page fault is a type of interrupt, raised by the hardware when a running program accesses a memory page that is mapped into the virtual address space but not loaded in physical memory. 

#### Page Replacement Algorithms:
First In First Out (FIFO) – This is the simplest page replacement algorithm. In this algorithm, the operating system keeps track of all pages in the memory in a queue, the oldest page is in the front of the queue. When a page needs to be replaced page in the front of the queue is selected for removal.

Optimal Page Replacement – In this algorithm, pages are replaced that are not used for the longest duration of time in the future.
Least Recently Used (LRU) – In this algorithm, the page will be replaced which is least recently used.
#### File System: A file is a collection of related information that is recorded on secondary storage.

1. SINGLE-LEVEL DIRECTORY: In this a single directory is maintained for all the users.

2. TWO-LEVEL DIRECTORY: Due to two levels there is a path name for every file to locate that file.

3. TREE-STRUCTURED DIRECTORY: A directory is maintained in the form of a tree. Searching is efficient and there is a grouping capability. 

4. Continuous Allocation: A single continuous set of blocks is allocated to a file at the time of file creation.
   
5. Linked Allocation(Non-contiguous allocation): Allocation is on an individual block basis. Each block contains a pointer to the next block in the chain.
   
6. Indexed Allocation: It addresses many of the problems of contiguous and chained allocation. In this case, the file allocation table contains a separate one-level index for each file.
   
7. Seek Time: Seek time is the time taken to locate the disk arm to a specified track where the data is to be read or write.
    
8. Rotational Latency: Rotational Latency is the time taken by the desired sector of disk to rotate into a position so that it can access the read/write heads.
    
9. Transfer Time: Transfer time is the time to transfer the data. It depends on the rotating speed of the disk and number of bytes to be transferred.
    
10. Disk Access Time: Seek Time + Rotational Latency + Transfer Time
    
11. Disk Response Time: Response Time is the average of time spent by a request waiting to perform its I/O operation. Average Response time is the response time of all requests.
    
12. FCFS: FCFS is the simplest of all the Disk Scheduling Algorithms. In FCFS, the requests are addressed in the order they arrive in the disk queue
    
13. STF: In SSTF (Shortest Seek Time First), requests having the shortest seek time are executed first. So, the seek time of every request is calculated in advance in a queue and then they are scheduled according to their calculated seek time. As a result, the request near the disk arm will get executed first.
    
14. SCAN: In the SCAN algorithm the disk arm moves in a particular direction and services the requests coming in its path and after reaching the end of the disk, it reverses its direction and again services the request arriving in its path. So, this algorithm works like an elevator and hence also known as an elevator algorithm.
    
15. CSCAN: In the SCAN algorithm, the disk arm again scans the path that has been scanned, after reversing its direction. So, it may be possible that too many requests are waiting at the other end or there may be zero or few requests pending at the scanned area.
    
16. LOOK: It is similar to the SCAN disk scheduling algorithm except for the difference that the disk arm in spite of going to the end of the disk goes only to the last request to be serviced in front of the head and then reverses its direction from there only. Thus it prevents the extra delay that occurred due to unnecessary traversal to the end of the disk.
    
17. CLOOK: As LOOK is similar to SCAN algorithm, in a similar way, CLOOK is similar to the CSCAN disk scheduling algorithm. In CLOOK, the disk arm in spite of going to the end goes only to the last request to be serviced in front of the head and then from there goes to the other end’s last request. Thus, it also prevents the extra delay that occurs due to unnecessary traversal to the end of the disk. 
