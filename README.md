# os-lastminute-revision

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
- FCFS  stands for first come first serve. It is the simplest algorithm that schedules according to the arrival time of processes.
#### SJF
- SJF stands for shortest job first. The process that has arrived first and which has less burst time that schedules first.

#### SRTF
-It is the preemptive mode of the SJF algorithm in which jobs are scheduled according to the shortest remaining time.
#### Round Robin
- Each process is assigned a fixed time, in a cyclic way.



  

